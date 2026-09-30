---
title: Présentation de la préparation des vacances Adobe Commerce
description: Conseils de niveau exécutif pour préparer Adobe Commerce aux environnements d’infrastructure cloud pour les événements à trafic élevé tels que la saison des fêtes.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
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
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Présentation de la préparation des vacances Adobe Commerce

Ce playbook fournit des conseils pour la préparation des environnements Adobe Commerce aux événements à trafic élevé, comme la saison des fêtes. Il regroupe les recommandations techniques en cinq domaines stratégiques :

- Optimisation des performances
- Bonnes pratiques et stabilité
- Surveillance et observabilité
- Planification de l’évolutivité et des capacités
- Préparation opérationnelle

Ces domaines d’intervention permettent de s’assurer que votre plateforme reste stable, sécurisée et performante en cas de pic de charge.

## Optimisation des performances

Voici un aperçu des étapes recommandées pour optimiser les performances. Pour plus d’informations, consultez [Préparation des vacances Adobe Commerce > Optimisation des performances](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md).

* Optimiser la mise en cache des demandes Fastly : normalisez vos paramètres de suivi promotionnel, vérifiez que vos pages de destination peuvent être mises en cache et utilisez GraphQL GET pour les storefronts PWA ou découplés afin d’augmenter votre taux d’accès au cache Fastly.
* Activer Fastly IO : activez Fastly Image Optimization et Deep IO afin que les transformations d’image s’exécutent à la périphérie du réseau de diffusion de contenu plutôt qu’à l’origine, ce qui réduit le temps de rendu de la page sur les storefronts riches en images.
* Activer le cache L2 : stockez les données du cache localement sur chaque nœud web pour réduire la latence et les appels réseau à Redis/Valkey, en fonction de votre version d’Adobe Commerce. Le cache Redis n’est pas pris en charge pour Adobe Commerce 2.4.9 ou pour les versions de correctif ultérieures à 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 et 2.4.8-p4.
* Activer les connexions esclaves : acheminez les requêtes lourdes en lecture vers les nœuds de réplication avec `MYSQL_USE_SLAVE_CONNECTION` et `REDIS_USE_SLAVE_CONNECTION` ou `VALKEY_USE_SLAVE_CONNECTION` afin que les bases de données maîtres ne soient pas le goulot d&#39;étranglement en cas de charge.
* Activer le traitement asynchrone des commandes et des e-mails : le placement des commandes en file d’attente, les mises à jour de la grille de données de commande et les e-mails de passage en caisse doivent s’exécuter en arrière-plan dans trois paramètres distincts, de sorte que le passage en caisse reste rapide sous un volume de commande élevé.
* Basculez les indexeurs sur le mode Mise à jour selon le calendrier : déplacez les indexeurs de la Mise à jour lors de l’enregistrement vers le mode Mise à jour selon le calendrier piloté par cron pour éviter le verrouillage lors de mises à jour de catalogue fréquentes, à l’exception de l’indexeur customer_grid.
* Envisagez une architecture à l’échelle (partage) : si les correctifs de niveau de code et de réglage laissent CPU sous charge, passez à une configuration à six nœuds à plusieurs niveaux qui met à l’échelle les nœuds web et de base de données indépendamment.

## Bonnes pratiques et stabilité

Voici un aperçu des bonnes pratiques pour garantir la stabilité de votre instance. Pour obtenir des instructions détaillées sur chacune de ces étapes, consultez [Préparation d’Adobe Commerce pour les fêtes > Bonnes pratiques et stabilité](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md).

* Mise à niveau vers la dernière version d’Adobe Commerce : bénéficiez d’une version prise en charge pour conserver les correctifs de sécurité et les améliorations de performances fournis par Adobe dans chaque version.
* Installez les derniers outils ECE et l&#39;outil de correctifs de qualité (QPT) : Mettez à jour les outils ECE avec ses dépendances et confirmez que les correctifs de l&#39;outil de correctifs de qualité applicables sont appliqués, pour les installations cloud et sur site.
* Vérifier et nettoyer les fichiers journaux : supprimez les journaux de débogage et surveillez les erreurs récurrentes afin d’éviter toute surutilisation du disque et d’améliorer la visibilité des journaux.
* Surveillez la croissance de la taille du disque : conservez les fichiers partagés et les volumes de base de données utilisés à moins de 70 % afin que la croissance du stockage ne déclenche pas de panne.
* Examinez les requêtes de base de données lentes : utilisez l’outil APM et le journal de requêtes lentes MySQL pour rechercher et corriger les requêtes coûteuses avant qu’elles ne se multiplient lors du pic de trafic.
* Configurez les tâches cron correctement : vérifiez que cron s’exécute toutes les minutes sous le bon utilisateur ou la bonne utilisatrice, car chaque opération asynchrone dans Commerce en dépend.
* Optimiser les paramètres côté client : activez la minification et le regroupement CSS, JavaScript et HTML pour accélérer les temps de chargement du storefront.

## Surveillance et observabilité

Vous trouverez ci-dessous les méthodes recommandées pour surveiller votre instance Adobe Commerce pendant la haute saison. Pour obtenir des étapes détaillées pour chacune de ces recommandations de surveillance et d’observabilité, reportez-vous à [Préparation des vacances Adobe Commerce > Surveillance et observabilité](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md).

* Surveillez le trafic avec New Relic : utilisez la diffusion en continu des journaux Fastly dans New Relic pour détecter les anomalies de trafic, les adresses IP abusives, les requêtes malveillantes ciblant des points d’entrée tels que le paiement et les tendances relatives aux appareils/navigateurs.
* Personnaliser les alertes New Relic : configurez vos propres alertes NRQL pour le trafic inhabituel, les requêtes GraphQL lentes ou les taux d’erreur croissants, en plus des alertes gérées par Adobe.
* Suivre le score Apdex : regardez le score Apdex (cible ≥ 0,85) pour conserver les temps de réponse back-end et front-end dans une plage que les utilisateurs jugent satisfaisante.
* Examinez les informations d’assistance (rapport SWAT) : exécutez un rapport SWAT avant et après les pics d’événements pour identifier les risques au niveau du système et les domaines d’amélioration.

## Planification de l’évolutivité et des capacités

Pour obtenir des étapes détaillées pour chacune de ces recommandations en matière d&#39;évolutivité et de planification des capacités, consultez [Préparation des vacances Adobe Commerce > Planification de l&#39;évolutivité et des capacités](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md).

* Planifiez la mise à niveau du cluster au plus tôt : demandez une mise à niveau temporaire du calcul à l’assistance Adobe au moins 10 jours ouvrables avant une promotion majeure.
* Activer le blindage d’origine Fastly : acheminez les requêtes non mises en cache via un Shield POP près de votre origine afin que moins de requêtes atteignent directement le serveur d’origine.
* Réalisation de tests de chargement et de basculement : testez les scénarios de chargement et de récupération avant les campagnes majeures afin de confirmer que vos plans de mise à l’échelle et de restauration tiennent la route.

## Préparation opérationnelle

* Appliquez tous les correctifs de sécurité et de performances : terminez tous les correctifs avant le gel du code afin d’éviter toute interruption ultérieure des déploiements.
* Exécutez les contrôles d’intégrité avant le jour férié : testez les sauvegardes, l’intégrité du cron et les scripts de préchauffage du cache pour que les opérations s’exécutent correctement en cas de forte charge.
* Établissez des playbooks de surveillance : documentez les seuils d’alerte, les chemins d’escalade et les contacts 24h/24 et 7j/7 afin que l’équipe puisse répondre rapidement pendant les heures de pointe.
* Documentez les plans de restauration : conservez les stratégies de restauration versionnées prêtes afin de pouvoir récupérer rapidement d’un déploiement incorrect.