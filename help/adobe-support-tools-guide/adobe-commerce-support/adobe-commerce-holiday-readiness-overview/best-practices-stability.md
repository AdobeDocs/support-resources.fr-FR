---
title: Bonnes pratiques et stabilité
description: Recommandations de bonnes pratiques et de stabilité pour aider les commerçants Adobe Commerce à préparer leurs environnements aux événements à trafic élevé tels que la saison des fêtes.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# Bonnes pratiques et stabilité

Cette section fournit des recommandations techniques pour la préparation des environnements Adobe Commerce (Commerce sur infrastructure cloud et sur site) pour les événements à trafic élevé tels que la saison des fêtes.

>[!NOTE]
>
>Les étapes marquées **(cloud uniquement)** s’appliquent à Commerce sur les infrastructures cloud. La plupart des autres recommandations s’appliquent également aux déploiements sur site.

## Mise à niveau vers la dernière version d’Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

Assurez-vous que votre site ne se trouve pas sur une version d’Adobe Commerce non prise en charge, ce qui peut affecter les performances de votre site et augmenter la vulnérabilité aux problèmes de sécurité. Effectuez une mise à niveau vers la dernière version d’Adobe Commerce pour être sécurisé et prêt pour la saison des fêtes.

La [dernière version](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/notes/overview) d’Adobe Commerce comprend de nombreux [correctifs de sécurité critiques](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/notes/security-patches/overview), y compris des améliorations et des problèmes atténués, qui bénéficieront à votre projet lors de la mise à niveau à partir d’une version précédente.

Pour plus d’informations sur les versions d’Adobe Commerce non prises en charge, consultez la [Politique de cycle de vie d’Adobe Commerce](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/planning/lifecycle-policy).

## Installer les derniers outils ECE et l&#39;outil de correction de la qualité (QPT) {#install-latest-ece-tools-and-quality-patch-tool-qpt}

Assurez-vous que le dernier module `ece-tools` et ses modules dépendants sont installés à l’aide du commutateur `--with-dependencies`, de sorte que tous les correctifs cloud requis soient correctement installés pour votre version d’Adobe Commerce. Pour connaître les étapes à suivre, voir [Mise à jour du module ECE-Tools](https://experienceleague.adobe.com/fr/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package).

Consultez la liste des correctifs disponible dans l’outil de correctifs de la qualité et assurez-vous que les correctifs de performances compatibles avec votre version d’Adobe Commerce ont été appliqués. Voir [Outil de correctifs de qualité : rechercher des correctifs](https://experienceleague.adobe.com/fr/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview).

>[!NOTE]
>
>QPT est disponible pour les installations sur site et les infrastructures cloud d’Adobe Commerce. Les commandes d&#39;installation et d&#39;utilisation diffèrent entre les deux : pour Cloud, QPT est inclus avec le package ECE-Tools.

## Vérifier et nettoyer les fichiers journaux {#review-and-clean-log-files}

Passez en revue les fichiers journaux dans l’environnement cloud (par exemple, les fichiers journaux de l’application sous `~/var/log`) et identifiez les enregistrements fréquemment consignés qui sont écrits dans les fichiers journaux par défaut ou personnalisés. Pour plus d’informations, voir [Affichage et gestion des journaux](https://experienceleague.adobe.com/fr/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

* Consultez les fichiers journaux par défaut suivants et corrigez les erreurs récurrentes : `~/var/log`, `~/var/log/exception.log`, `~/var/log/support_report.log`, `~/var/log/system.log`, `~/var/report`.
* Supprimez les journaux de débogage qui ont été précédemment ajoutés pour résoudre les problèmes passés.

Ces journaux sont également disponibles dans [!DNL New Relic], consultez [Gestion des journaux New Relic](https://experienceleague.adobe.com/fr/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Surveillance de la croissance de la taille du disque {#monitor-disk-size-growth}

Votre Adobe Commerce sur l’infrastructure cloud comporte deux volumes de disque principaux. Surveillez ces volumes pour vous assurer qu&#39;ils disposent d&#39;un espace libre suffisant en cas de trafic important. Adobe Commerce affiche un avertissement lorsque l’un des volumes dépasse 70 % d’utilisation.

* `/mnt/shared` (fichiers partagés, y compris les journaux et les fichiers multimédias)
* `/data/mysql` (volume de la base de données)

Pour plus d’informations, voir [Gérer l’espace disque](https://experienceleague.adobe.com/fr/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space).

## Vérifier les demandes de base de données les plus lentes {#review-slowest-database-requests}

Il est important de surveiller et d’examiner régulièrement les transactions de base de données qui prennent le plus de temps en [!DNL New Relic]. Examinez les requêtes et les composants considérablement lents.

* **Vérifiez les transactions les plus chronophages :** Accédez à **[!UICONTROL New Relic]** > **[!UICONTROL APM &amp; Services]** > sélectionnez l’environnement > **[!UICONTROL Bases de données]**, puis triez les transactions les plus chronophages.

* **Vérifiez le journal des requêtes lentes de MySQL :** vérifiez `mysql-slow.log` les requêtes lentes enregistrées par le système. Ces journaux sont également disponibles dans [!DNL New Relic] : accédez à **[!UICONTROL New Relic]** > **[!UICONTROL Journaux]** et filtrez par `filePath:"/var/log/mysql/mysql-slow.log"`.

Consultez régulièrement les journaux des requêtes lentes [!DNL MySQL] pour confirmer que les requêtes lentes ne s’exécutent pas fréquemment. Pour connaître les étapes de résolution des requêtes que vous identifiez comme problématiques, consultez [Résolution des problèmes de performances des bases de données](https://experienceleague.adobe.com/fr/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues).

## Configuration des tâches cron {#configure-cron-jobs}

Toutes les opérations asynchrones dans Commerce sont effectuées à l’aide de la commande cron Linux.

Commerce dépend de la configuration appropriée des tâches cron pour les fonctions système importantes, y compris les opérations d’indexation et de mise en file d’attente des clients. Si cette configuration n’est pas effectuée correctement, Commerce ne fonctionnera pas comme prévu.

Il est essentiel que Commerce cron soit configuré correctement, en utilisant l’utilisateur Unix approprié dans le fichier crontab Unix. Chaque utilisateur Unix possède son propre fichier crontab, qui correspond à la configuration utilisée pour exécuter les tâches cron pour cet utilisateur. Pour connaître les étapes, voir [Configuration et exécution des tâches cron](https://experienceleague.adobe.com/fr/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs).

Le script `dev/tools/cron.sh` ne peut plus être exécuté, car il a été supprimé.

## Optimiser les paramètres côté client {#optimize-client-side-settings}

Pour améliorer la réactivité du storefront de votre instance Commerce, configurez les paramètres ci-dessous sous **[!UICONTROL Magasins]** > **[!UICONTROL Configuration]** > **[!UICONTROL Avancé]** > **[!UICONTROL Développeur]**, disponible uniquement en mode Développeur :

* **[!UICONTROL Paramètres de grille]** > **[!UICONTROL Indexation asynchrone]** : *[!UICONTROL Activer]*
* **[!UICONTROL Paramètres CSS]** — **[!UICONTROL Minimiser les fichiers CSS]** : *[!UICONTROL Oui]*
* **[!UICONTROL Paramètres JavaScript]** — **[!UICONTROL Minimiser les fichiers JavaScript]** : *[!UICONTROL Oui]*
* **[!UICONTROL Paramètres JavaScript]** — **[!UICONTROL Activer le regroupement JavaScript]** : *[!UICONTROL Oui]* (non activé par défaut)
* **[!UICONTROL Paramètres de modèle]** — **[!UICONTROL Minimiser HTML]** : *[!UICONTROL Oui]*

Étant donné qu’Adobe Commerce sur le cloud s’exécute toujours en mode Production, définissez plutôt chaque option à partir de la ligne de commande (par exemple, `bin/magento config:set --lock-config dev/css/minify_files 1`), puis validez la modification de `app/etc/config.php` et le redéploiement qui en résultent. Pour obtenir la liste complète des chemins d’accès à l’interface de ligne de commande, voir [Optimisation des fichiers de ressources](https://experienceleague.adobe.com/fr/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files).
