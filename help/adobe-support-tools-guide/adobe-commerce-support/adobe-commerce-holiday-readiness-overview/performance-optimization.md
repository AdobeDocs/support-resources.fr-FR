---
title: Optimisation des performances
description: Recommandations d’optimisation des performances pour aider les commerçants Adobe Commerce à préparer leurs environnements aux événements à trafic élevé, tels que la saison des fêtes.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 8b0e99848d1e5798cce52e21f9052b2b57c73b38
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# Optimisation des performances

Cette section fournit des recommandations techniques pour la préparation des environnements Adobe Commerce (Commerce sur infrastructure cloud et sur site) pour les événements à trafic élevé tels que la saison des fêtes.

>[!NOTE]
>
>Les étapes marquées **(cloud uniquement)** s’appliquent à Commerce sur les infrastructures cloud. La plupart des autres recommandations s’appliquent également aux déploiements sur site.

## Optimisation de la mise en cache des requêtes Fastly (cloud uniquement) {#optimize-fastly-request-caching}

[!DNL Fastly] met en cache les réponses à la périphérie pour réduire la charge sur votre serveur d’origine. Pendant la haute saison, quelques vérifications de configuration vous aident à tirer le meilleur parti de ce cache, en particulier lorsque vous exécutez des promotions avec des paramètres de suivi ou un storefront découplé. Pour consulter la référence complète de la configuration, voir [&#x200B; Personnaliser la configuration du cache &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration).

* Normaliser les paramètres de tracking : pendant la saison des fêtes, vous exécuterez probablement des campagnes sociales et payantes, telles que Google Ads, Facebook et X, qui ajoutent des chaînes de tracking uniques à chaque URL. Chaque chaîne unique crée une entrée de cache distincte pour ce qui est autrement la même page, ce qui réduit votre taux d’accès au cache. Ajoutez ces paramètres à la liste **[!UICONTROL Paramètres d’URL ignorés]** dans la configuration [!DNL Fastly] de l’administration Adobe Commerce afin que [!DNL Fastly] les traite comme équivalents.
* Vérifiez que vos pages de destination peuvent être mises en cache : vérifiez l’en-tête de réponse `x-cache` sur chaque page de destination de promotion. Une page pouvant être mise en cache renvoie une `HIT` ou une paire `HIT`/`MISS` lors des chargements suivants. Si l’en-tête renvoie `MISS, MISS`, la page ne se met pas en cache et nécessite une enquête.
* Utiliser des requêtes GET pour les requêtes GraphQL : si vous exécutez un storefront PWA ou découplé, envoyez des requêtes GraphQL en tant que requêtes `GET` avec la requête incluse dans l’URL, plutôt qu’en tant que requêtes `POST`. [!DNL Fastly] ne met en cache que `GET` requêtes dans lesquelles la requête fait partie de l’URL. Une requête `GET` avec la requête envoyée dans le corps n’est pas mise en cache.

>[!NOTE]
>
>[!DNL Fastly] blindage d’origine affecte également les performances du cache. Pour plus d’informations sur la configuration, voir [Fastly origin shielding](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

## Activer Fastly IO (cloud uniquement) {#enable-fastly-io}

[!DNL Fastly]’E/S décharge le redimensionnement des images et la conversion des formats sur le réseau Edge de [!DNL Fastly] plutôt que sur l’origine Adobe Commerce. Cela réduit la charge du serveur et améliore la vitesse de rendu des pages pour les storefronts riches en images, un goulot d’étranglement courant pendant les périodes de vente à trafic élevé. Pour connaître les options de configuration, voir [Optimisation rapide des images](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization).

Avant de commencer, vérifiez que le blindage d’origine est configuré. [!DNL Fastly] Les E/S nécessitent au préalable un blindage d&#39;origine. Pour plus d’informations sur la configuration, voir [Fastly origin shielding](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

Pour activer les E/S [!DNL Fastly] :

1. Dans Admin, accédez à la page **[!UICONTROL Configuration Fastly]** et sélectionnez **[!UICONTROL Configurer]** en regard de **[!UICONTROL Options de configuration d’E/S par défaut]**.
1. Vérifiez que le fragment de code d’E/S [!DNL Fastly] est activé.
1. Dans la configuration **[!UICONTROL Optimisation des images]**, définissez **[!UICONTROL Activer l’optimisation d’image profonde]** sur *[!UICONTROL Oui]*. Ce paramètre désactive le redimensionnement d’image intégré d’Adobe Commerce et transfère la tâche vers [!DNL Fastly].
1. Vérifiez que l&#39;emplacement du bouclier est correctement défini. Pour plus d’informations sur la configuration, voir [Fastly origin shielding](#fastly-origin-shielding).

>[!NOTE]
>
>L’optimisation des images profondes redimensionne uniquement les images du produit. Les images CMS, telles que les bannières et les blocs de contenu, ne sont pas affectées et continuent à utiliser le redimensionnement intégré d’Adobe Commerce.

Pour vérifier que [!DNL Fastly] E/S fonctionne, vérifiez les en-têtes de réponse sur une demande d’image de produit :

* L’en-tête `x-cache` renvoie `HIT`.
* Les en-têtes `fastly-io-info` et `fastly-stats` sont renseignés.
* L’URL de l’image n’inclut pas de répertoire `/cache/` dans le chemin d’accès.

## Implémentation du cache L2 Redis {#implement-redis-l2-cache}

Implémentez des pratiques de mise en cache efficaces afin que votre boutique fonctionne de manière fiable pendant les saisons de trafic élevé. [!DNL Redis] Le cache L2 réduit la bande passante du réseau à [!DNL Redis] en stockant les données de cache localement sur chaque nœud web. Pour en savoir plus sur le fonctionnement du cache L2, consultez [Cache de niveau 2](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/level-two-cache).

Sur Commerce sur les infrastructures cloud, activez cette option en définissant la variable de déploiement `REDIS_BACKEND` . Pour connaître les étapes de configuration, consultez [REDIS_BACKEND](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend) dans le guide Commerce sur les infrastructures cloud. Sur site, configurez-le directement dans `app/etc/env.php`.

>[!NOTE]
>
>[!DNL Redis] n’est pas pris en charge en tant que serveur principal de cache L2 sur Adobe Commerce version 2.4.9 ou ultérieure, ou sur les versions de correctif ultérieures à 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 ou 2.4.8-p4. Sur ces versions, utilisez plutôt `VALKEY_BACKEND`.

## Activer les connexions esclaves MySQL et Redis (Cloud uniquement) {#enable-mysql-and-redis-slave-connections}

Les connexions esclaves [!DNL Redis] et [!DNL MySQL] déchargent le trafic de lecture vers les nœuds de réplication, ce qui réduit la charge sur la connexion maître pendant les périodes de trafic élevé. Pour les étapes de configuration, voir [MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection) et [REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection) ou [VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection), selon votre version d’Adobe Commerce.

### Redis les connexions esclaves

Une connexion esclave [!DNL Redis] est une connexion en lecture seule à une instance [!DNL Redis], ce qui permet au trafic de lecture d’être diffusé à partir d’un nœud non maître. Si elle n’est pas activée, [!DNL MySQL] pouvez rencontrer un goulot d’étranglement à forte charge. Vérifiez le graphique APM Overview de [!DNL New Relic] pour identifier les temps de réponse croissants comme signe précoce, puis confirmez dans l’onglet **[!UICONTROL Base de données]** en triant par transaction la plus longue pour identifier les requêtes de `SELECT` de [!DNL MySQL] lentes. Activez cette option en définissant la variable de déploiement `REDIS_USE_SLAVE_CONNECTION` sur `true`.

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION` est pris en charge uniquement dans les environnements de cluster Staging et Production Pro. Il n’est pas pris en charge sur les projets d’architecture de démarrage ou de mise à l’échelle (partage). Son activation sur une architecture mise à l’échelle entraîne des erreurs de connexion [!DNL Redis] ; utilisez [!DNL Redis] cache L2 à la place sur cette architecture. Voir la section [&#x200B; Implémentation du cache Redis L2](#implement-redis-l2-cache-implement-redis-l2-cache) ci-dessus.

### Connexions esclaves MySQL

Activez l&#39;indicateur `MYSQL_USE_SLAVE_CONNECTION` sur les environnements de cluster Pro pour diriger des requêtes de base de données spécifiques en lecture seule vers une connexion esclave, déchargeant l&#39;exécution des requêtes de la connexion maître.

>[!CAUTION]
>
>Chargez le test avant d’activer l’un des paramètres en production. Dans les environnements à charge normale, les connexions esclaves peuvent ralentir les performances de 10 à 15 %. Dans les environnements soumis à une charge lourde et soutenue, elles peuvent améliorer les performances dans une mesure similaire. Évaluez le trafic en haute saison attendu avant d’activer.

## Activer le traitement asynchrone des commandes et des e-mails {#enable-asynchronous-order-and-email-processing}

Utilisez le traitement asynchrone pour mettre en file d’attente et exécuter des opérations liées aux commandes de gros volumes en arrière-plan, ce qui réduit la latence frontale pendant le trafic de pointe. Cela couvre trois paramètres associés mais distincts. Pour une présentation, reportez-vous à la section [&#x200B; Bonnes pratiques de configuration &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration).

* Passation de commande asynchrone : le module de commande asynchrone marque une commande comme reçue, la place dans une file d’attente et traite les commandes premier entré, premier sorti. Cette fonctionnalité est désactivée par défaut. Activez-la à partir de la ligne de commande :

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  Une fois activée, les détails de la commande ne sont pas disponibles immédiatement. La commande reste en file d’attente jusqu’à ce que le client `placeOrderProcess` la vérifie par rapport à l’inventaire (activé par défaut) et la mette à jour. Avant de désactiver ce module, vérifiez que le traitement de toutes les commandes asynchrones en cours est terminé. Pour plus d’informations, consultez [Bonnes pratiques relatives aux performances de passage en caisse](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/high-throughput-order-processing).

* Traitement asynchrone des données de commande : les ventes de storefront intensives et le traitement intensif des commandes peuvent créer des conflits au niveau de la base de données. L’activation de ce paramètre permet de distinguer les deux modèles de trafic, de sorte que les commandes soient placées en stockage temporaire et déplacées en bloc vers la grille Order Management sans conflits. Cette planification met à jour, par cron, les grilles Commandes, Factures, Livraisons et Avoirs, évitant ainsi les blocages et réduisant le temps de traitement. Pour de meilleurs résultats, configurez cron pour qu’il s’exécute une fois par minute.

>[!NOTE]
>
>La méthode d’activation dépend de votre mode de déploiement. Par défaut, les environnements d’évaluation et de production d’Adobe Commerce sur les infrastructures cloud s’exécutent en mode Production, où ce paramètre n’est pas disponible via l’administration. En mode Production, exécutez `bin/magento config:set dev/grid/async_indexing 1` à la place. En mode par défaut, accédez à **[!UICONTROL Magasins]** > **[!UICONTROL Configuration]** > **[!UICONTROL Avancé]** > **[!UICONTROL Développeur]** > **[!UICONTROL Paramètres de grille]** et définissez **[!UICONTROL Indexation asynchrone]** sur *[!UICONTROL Activer]*.

Pour plus de détails, voir [Opérations de commande planifiées](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations).

* Notifications par e-mail asynchrones : ce paramètre déplace les notifications par e-mail de passage en caisse et de traitement de commande vers l’arrière-plan. Activez-le à l’adresse **[!UICONTROL Magasins]** > **[!UICONTROL Configuration]** > **[!UICONTROL Ventes]** > **[!UICONTROL E-mails commerciaux]** > **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Envoi asynchrone]**.

## Configuration des indexeurs pour une mise à jour selon le calendrier {#configure-indexers-for-update-on-schedule}

Définissez les indexeurs pour qu’ils s’exécutent en mode planifié afin d’éviter le verrouillage de la base de données et d’améliorer la réactivité lors des mises à jour fréquentes des catalogues. Pour plus d’informations, consultez [Bonnes pratiques relatives à la configuration de l’indexeur](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration).

Un indexeur peut s’exécuter en mode **[!UICONTROL Mise à jour lors de l’enregistrement]** ou **[!UICONTROL Mise à jour selon le calendrier]**.

* **[!UICONTROL Mise à jour lors de l’enregistrement]** indexe immédiatement chaque fois que le catalogue ou d’autres données sont modifiés. Elle suppose une faible intensité de mise à jour et de navigation, et peut entraîner des retards importants et une indisponibilité des données sous une charge élevée.
* **[!UICONTROL Mise à jour selon le calendrier]** est recommandé pour la production. Il stocke des informations sur les mises à jour de données et les réindexations en arrière-plan via une tâche cron dédiée.

Définissez le mode de mise à jour de chaque indexeur indépendamment à l’adresse **[!UICONTROL Système]** > **[!UICONTROL Outils]** > **[!UICONTROL Gestion des index]**.

>[!IMPORTANT]
>
>Les modes pris en charge par l’indexeur `customer_grid` dépendent de votre version d’Adobe Commerce. Dans les versions antérieures à la version 2.4.8, la grille client prend uniquement en charge **[!UICONTROL Mise à jour lors de l’enregistrement]**—ne la définissez pas sur **[!UICONTROL Mise à jour selon le calendrier]**. Dans Adobe Commerce 2.4.8 et les versions ultérieures, la grille cliente prend en charge les deux modes et utilise désormais par défaut **[!UICONTROL Mise à jour selon le calendrier]**.

## Désactiver et évaluer la table plate du catalogue {#disable-and-evaluate-catalog-flat-table}

L&#39;utilisation de tables plates pour les produits et les catégories n&#39;est pas recommandée. Cette fonctionnalité obsolète peut entraîner une dégradation des performances et des problèmes d’indexation. Pour plus d’informations, consultez la section [Catalogues plats](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/catalog-flat).

Pour désactiver le catalogue plat, accédez à **[!UICONTROL Magasins]** > **[!UICONTROL Configuration]** > **[!UICONTROL Catalogue]** > **[!UICONTROL Catalogue]** > **[!UICONTROL Storefront]**, définissez **[!UICONTROL Utiliser la catégorie de catalogue plat]** à *[!UICONTROL No]*, définissez **[!UICONTROL Utiliser le produit de catalogue plat]** à *[!UICONTROL No]*, puis cliquez sur **[!UICONTROL Enregistrer la configuration]**.

Certains modules tiers et certaines personnalisations nécessitent des tableaux plats pour fonctionner correctement. Évaluez l’impact et le risque de continuer à utiliser ces extensions avant de désactiver les tables plates.

## Étudier l’architecture mise à l’échelle (partage) (cloud uniquement) {#consider-scaled-split-architecture}

Si, après l’application de la configuration et des optimisations au niveau du code précédentes, les tests de charge ou les performances de l’infrastructure en direct montrent toujours que CPU et d’autres ressources sont à leur maximum, envisagez de passer à une architecture à l’échelle (partagée). Pour plus d’informations, consultez [Architecture mise à l’échelle](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture).

>[!NOTE]
>
>L’architecture évolutive est disponible uniquement pour les comptes disposant d’un cluster Pro 48 ou d’un niveau supérieur.

L’architecture à niveaux partagés utilise au moins six nœuds : trois nœuds de service exécutant [!DNL OpenSearch] ou [!DNL Elasticsearch], [!DNL MariaDB] et [!DNL Redis] ou [!DNL Valkey], et trois nœuds web exécutant `php-fpm` et `NGINX`.

* Les nœuds de service ne peuvent être dimensionnés que verticalement, en augmentant la taille du serveur (CPU et mémoire). Le cluster de base de données étant conçu pour offrir une haute disponibilité, les nœuds de service ne peuvent pas être dimensionnés horizontalement de manière fiable.
* Les nœuds web peuvent être mis à l’échelle verticalement et horizontalement, ajoutant ainsi des serveurs web pour gérer l’augmentation du volume de requêtes.

Vous pouvez ainsi étendre l’infrastructure à la demande pendant les périodes de forte charge, en dimensionnant chaque niveau indépendamment. Pour passer à une architecture à plusieurs niveaux avant une période de charge importante, contactez l’équipe chargée de votre compte Adobe.
