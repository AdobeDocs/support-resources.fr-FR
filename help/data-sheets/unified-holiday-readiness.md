---
title: Guide de préparation unifiée aux vacances pour les solutions Adobe DX
description: 'Préparation d’Adobe DX pour les vacances : AEP, AJO, CJA, Commerce, AEM, Marketo, Workfront, Campaign, Analytics et Target pour vous aider à planifier, mettre à l’échelle, sécuriser et optimiser.'
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
index: true
source-git-commit: 3d8acc3aabdb7de154ecce45f28c493033193096
workflow-type: tm+mt
source-wordcount: '3827'
ht-degree: 2%

---

# Guide de préparation unifiée aux vacances pour les solutions Adobe DX


Le Guide de préparation unifié aux vacances pour les solutions DX d’Adobe vous aide à vous préparer à la période des fêtes en vous concentrant sur une planification proactive plutôt que sur la résolution réactive de problèmes. Elle fournit des étapes pratiques pour s’assurer que vos instances sont prêtes, ce qui réduit au minimum les problèmes potentiels avant qu’ils ne se produisent. L’équipe d’Adobe dispose d’une expertise technique, d’un large éventail de fonctionnalités et de méthodes éprouvées pour vous offrir le niveau d’assistance et de conseils adapté, à la fois technique et stratégique, afin que votre entreprise soit bien préparée.

Suivez ces bonnes pratiques pour vous assurer que vos solutions d’expérience digitale Adobe sont résilientes, sécurisées et prêtes à faire face au trafic de pointe des vacances :

* Planifiez l’augmentation du trafic.
* Évitez les modifications majeures pendant les périodes de pointe et planifiez les mises à jour avant ou après la saison des fêtes.
* Utilisez des tableaux de bord et des alertes pour surveiller les performances et détecter les goulots d’étranglement dès le début.
* Vérifiez que vos contacts d’assistance autorisés sont à jour.
* [Contactez l’assistance Adobe](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket) à l’avance si possible.

Pour obtenir des recommandations spécifiques à Adobe sur le niveau de préparation aux fêtes, reportez-vous aux sections suivantes.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>Cliquez sur chaque section pour la développer.


## Guide de préparation des vacances pour Adobe Experience Platform (AEP) {#aep}

+++**Cliquez pour afficher les recommandations de préparation des vacances pour Adobe Experience Platform (AEP).**

Adobe Experience Platform (AEP) joue un rôle essentiel pour alimenter l’expérience client en temps réel. À l’approche de la saison des fêtes, il est essentiel de vous assurer que votre implémentation d’AEP est optimisée pour l’augmentation du trafic, la gestion sécurisée des données et l’ingestion évolutive.

### Prévoir la demande saisonnière

Pour se préparer aux pics de trafic saisonniers, Adobe recommande de planifier la capacité et de surveiller l’ingestion des profils de streaming. Cela inclut la prévision des volumes de données et la garantie que votre système peut gérer un débit accru. Pour référence, consultez [Planification de la capacité et du trafic saisonnier](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile).

### Préparation pour la mise à l’échelle

Adobe propose plusieurs stratégies pour vous assurer que votre environnement est prêt pour le trafic des fêtes :

* Augmentez la capacité allouée pour les sandbox.
* Identifiez les flux de données à débit élevé dans le [tableau de bord de surveillance](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) et appliquez une limitation ou un filtrage si nécessaire.
* Utilisez l’ingestion par lots pour les cas d’utilisation à faible latence afin d’optimiser les performances, comme décrit dans la section [ Utilisation et capacités des licences : bonnes pratiques relatives au débit en flux continu ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions).

Ces pratiques permettent de maintenir la fiabilité de l’ingestion et de réduire la latence pendant les périodes de pointe.

### Bonnes pratiques et mécanismes de sécurisation

Pour respecter les limites opérationnelles et éviter toute interruption de service, Adobe recommande les mécanismes de sécurisation suivants pour l’ingestion et les profils :

* [Bonnes pratiques relatives au débit en flux continu](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions)
* [Mécanismes de sécurisation pour l’ingestion de données](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/guardrails)
* [Mécanismes de sécurisation par défaut pour les données de profil client en temps réel et la segmentation](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails)
* [Plans Directeurs AEP : Mécanismes De Sécurisation](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### Sécurité et gouvernance

Adobe met l’accent sur les bonnes pratiques de sécurité et de gouvernance, en particulier pendant les saisons de trafic élevé où la sensibilité des données est renforcée.

Pour obtenir des recommandations sur la protection des données clients, l’application des contrôles de confidentialité et le maintien de la conformité dans l’ensemble de votre implémentation AEP, consultez la section [ Gouvernance, confidentialité et sécurité dans Adobe Experience Platform : Sécurité ](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/governance-privacy-security/overview#security) .

En suivant ces directives et en utilisant la documentation publique d’Adobe, les entreprises peuvent s’assurer que leur Adobe Experience Platform est résilient, sécurisé et prêt à offrir des expériences client exceptionnelles tout au long de la saison des fêtes.

+++

## Guide de préparation des vacances pour Adobe Journey Optimizer (AJO) {#ajo}

+++**Cliquez pour afficher les recommandations de préparation des vacances pour Adobe Journey Optimizer (AJO).**


Pour préparer Adobe Journey Optimizer à la saison des fêtes, les entreprises doivent anticiper les pics d’événements et la complexité cross-canal, configurer les règles de parcours et de fréquence et assurer l’hygiène des données et la logique de prise de décision. Ils doivent également valider les performances à grande échelle, appliquer des mécanismes de sécurisation d’API et de sécurité, et appliquer des informations post-pic pour affiner les campagnes futures.

### Prévoir la demande

* En fonction des compressions de la saison des fêtes et du volume plus important de la campagne, attendez-vous à :
   * Pic des événements en temps réel et des parcours déclenchés (abandon de panier, offres de dernière minute)
   * Risques de saturation des messages (opt-outs plus élevés, fatigue)
   * Augmentation de la complexité cross-canal (e-mail + push + SMS + in-app)
* Utilisez les mesures de l’année écoulée (taux d’ouverture/de clic/d’opt-out, volumes d’entrée sur le parcours) pour modéliser les charges prévues et définir des seuils pour vos systèmes de messagerie.
* Identifiez les « fenêtres calmes » probables ou les périodes de faible performance (par exemple : les week-ends, les jours fériés) et planifiez les volumes d&#39;envoi en conséquence.

### Préparation pour la mise à l’échelle

* Assurez-vous que toutes les configurations de canal dans AJO sont correctement configurées : e-mail, notification push, SMS, web, in-app. Pour plus d&#39;informations, consultez la section [Configuration des canaux](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces).
* Configurez le capping de la fréquence et les règles de capping pour contrôler les volumes de messages. Voir l’article [Capping de la fréquence](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules).
* Configurer des ensembles de règles de canal/parcours : voir la section [Utilisation d’ensembles de règles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets).
* Préparez vos flux d’événements et structures de segmentation d’hygiène des données/en temps réel.
* Vérifiez que vous avez défini des audiences cibles pour les campagnes de vacances, telles que :
   * clients à forte valeur ajoutée
   * segments fidèles
   * personnes abandonnant leur panier
   * primo accédants
* Précharger ou préparer des modèles pour les parcours de vacances, exploiter la logique de prise de décision (offres/contraintes) afin que vous puissiez vous adapter dynamiquement en fonction de l’inventaire, des offres sensibles au facteur temps et des préférences de canal. Voir l’exemple dans l’article [Ajouter des contraintes à une offre](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints).
* Préparation technique : confirmer la capacité de chargement de l’API/du point d’entrée, les règles de limitation/plafonnement pour les actions personnalisées et les intégrations externes. Pour plus d&#39;informations, consultez la section [Mécanismes de sécurisation et limitations](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/guardrails).

### Tester et valider

* Utilisez votre framework d’expérimentation pour tester les modifications des variables clés :
   * heure d&#39;envoi
   * type d’offre
   * mélange de canaux
Reportez-vous aux [bonnes pratiques AJO Experimentation Accelerator](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices).
* Effectuez une validation du parcours de bout en bout :
   * déclencheurs d’événement
   * entrée de segmentation
   * Flux de chemin de parcours
   * logique de personnalisation
   * contraintes d’offre
   * critères de sortie
* Vérifiez les règles de plafonnement et de conflit. Reportez-vous à l’article plafonnement et arbitrage du Parcours [](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/journey-capping).
* Test de résistance des volumes mis à l’échelle pour les envois de pointe ou les pics : Simulez des volumes de déclenchement élevés pour valider le comportement du système en cas de charge.
* Valider la délivrabilité : préchauffez les domaines/expéditeurs des e-mails, confirmez les configurations des notifications push mobiles et vérifiez les canaux de secours pour les SMS/in-app.

### Bonnes pratiques

* Utilisez l’orchestration omnicanal. Consultez l’article de blog [parcours clients omnicanaux essentiels pour l’engagement et la croissance](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) qui présente un exemple de saison des fêtes avec AJO.
* Hiérarchisez les déclencheurs en temps réel, le cas échéant. Par exemple : abandon de panier, abandon de navigation et alertes de stock, car les acheteurs de vacances sont plus réactifs.
* Tirez parti de la segmentation et de la personnalisation : ciblez les segments à forte intention, personnalisez les offres en fonction du comportement d’achat passé et des préférences.
* Fatigue minimale des messages : appliquez des limites et des heures calmes pour éviter une sur-sollicitation. Reportez-vous à l’article de blog [Améliorer l’expérience client avec le capping de la fréquence quotidienne dans AJO](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510).
* Le timing est important : le plan envoie les messages plus tôt dans la fenêtre de vacances (en fonction de la saison compressée) et aligne les canaux sur les fuseaux horaires et le comportement de l’audience locale.
* Proposez des offres dynamiques/à durée limitée pour créer une urgence, mais coordonnez-les entre les canaux pour éviter la duplication et les conflits.
* Utilisez la logique de suppression : supprimez les audiences qui viennent d’acheter ou appliquez des parcours après achat pour éviter les messages redondants.

### Sécurité et gouvernance

* Assurez-vous que le contrôle d’accès et les autorisations sont configurés de sorte que seuls les utilisateurs requis puissent déployer des parcours ou modifier des règles métier.
* Surveiller et appliquer le capping des appels/des connexions API : par exemple, consultez l’API [Capping | Article de Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/connect-systems/external-systems/capping).
* Utilisez des données propriétaires propres et assurez-vous que l’assemblage des identités est correct, de sorte que la messagerie soit axée sur le client ou la cliente et non dupliquée/incorrectement alignée.
* Assurez-vous que les domaines de délivrabilité sont préchauffés et que des mesures anti-spam sont en place, en particulier pour les envois de vacances volumineux.
* Examinez fréquemment les journaux d’audit et les changements de parcours pendant la haute saison pour détecter les erreurs d’exécution ou les parcours errants au début.

### Apprentissages post-pic

* Après les pics de charge, passez en revue le nombre d’entrées sur le parcours, le nombre de suppressions, les taux d’opt-out, les mesures de délivrabilité et les performances du canal.
* Nettoyez les segments supprimés et mettez en pause ou supprimez les parcours créés pour la fenêtre de vacances afin d’éviter la fatigue liée aux reports.
* Utilisez les informations des performances en temps réel pour affiner la planification de l’année prochaine (par exemple : ajustements de l’heure d’envoi, mélange de canaux et volume des messages).

En anticipant la demande saisonnière, en configurant les canaux et les règles, en validant les performances du parcours et en appliquant la sécurité et la gouvernance, les entreprises peuvent s’assurer que Adobe Journey Optimizer offre des expériences client transparentes, personnalisées et résilientes tout au long de cette saison de fêtes et au-delà.

+++

## Guide de préparation des vacances pour Customer Journey Analytics (CJA) {#cja}

+++**Cliquez pour voir les recommandations de préparation des vacances de Customer Journey Analytics (CJA).**

Customer Journey Analytics utilise les 5 points de suspension pour préparer les fêtes et la haute saison.

### Préparation pour la mise à l’échelle

* Examinez les connexions CJA et les vues de données ; déterminez quelles connexions et vues de données nécessitent une surveillance et un approvisionnement améliorés.
* Confirmez que la mise en service est suffisante pour les vacances ; augmentez les connexions critiques et les vues de données selon les besoins. Voir [Gérer les connexions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/manage-connections) pour plus d’informations.

### Surveillance des performances

* Tirez parti de la RAM ([[!UICONTROL Gestionnaire des activités de rapport] présentation](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) pour surveiller en temps réel les demandes de création de rapports actives et en file d’attente, identifier les connexions à capacité maximale et repérer les goulets d’étranglement.
* Recherchez une latence accrue pendant la charge maximale à l’aide des articles [ Guide de dépannage et d’erreurs ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) et [limites connues](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations).
* Permet aux administrateurs de suspendre ou d’annuler de manière préventive les requêtes longues/bloquées via la RAM. Reportez-vous à l’article [Annuler des demandes de création de rapports dans CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests).

### Bonnes pratiques

* Planifiez des exportations/rapports pendant les périodes de faible trafic afin de lisser la charge et de minimiser la latence. Reportez-vous à l’article [Rapports planifiés](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/scheduled-projects-manager).
* Demandes réparties : planifiez des rapports à différents intervalles tout au long de la journée.
* Réduisez les panneaux, simplifiez les segments, raccourcissez les périodes et évitez le nombre excessif de tâches simultanées. Consultez l’article [ Optimisation des performances de CJA Workspace ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance) pour plus d’informations.

### Résolution des problèmes

* Lors de la résolution des erreurs de l’espace de travail, reportez-vous aux messages d’erreur pour la cause et les actions recommandées ; utilisez la RAM ([!UICONTROL Gestionnaire des activités de rapport]) pour supprimer les goulets d’étranglement et gérer efficacement les accès simultanés. Voir [Gestion des erreurs CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) pour plus d’informations.
* Utilisez la RAM ([[!UICONTROL Gestionnaire des activités de rapport] dans CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) pour identifier les utilisateurs, les requêtes ou les projets problématiques ; donnez la priorité aux utilisateurs et annulez-les si nécessaire.

### Apprentissages post-pic

* Après la période de vacances/de pointe, passez en revue les performances et les journaux d’incidents pour évaluer l’impact des bonnes pratiques fournies.
* Passez en revue les requêtes lentes et les tâches des utilisateurs et utilisatrices afin d’identifier les modèles/tendances qui peuvent être optimisés pour la saison suivante.
* Collectez les commentaires des utilisateurs et des parties prenantes : mettez à jour vos propres runbooks et plans de préparation à l’aide des informations nouvellement acquises.
* Envoyez vos commentaires aux équipes d’Adobe par l’intermédiaire de votre équipe de compte.

+++

## guide de préparation des vacances Adobe Commerce {#commerce}

+++**Cliquez pour afficher les recommandations de préparation des vacances d’Adobe Commerce.**

Pour assurer une saison de pointe réussie pour votre organisation, il est essentiel de préparer votre vitrine numérique Adobe Commerce à un trafic élevé.

### Prévoir la demande

* Pendant la période de pic des ventes pendant les vacances (de mi-novembre à mi-janvier), Adobe recommande à tous les commerçants Adobe Commerce hébergés sur notre infrastructure cloud de planifier de manière proactive une augmentation du nombre de visiteurs en soumettant des demandes de capacité de pointe pendant les vacances. Pour plus d’informations, consultez [Demandes de capacité de pointe pour les fêtes pour Adobe Commerce sur notre infrastructure cloud](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud).

### Préparation pour la mise à l’échelle

Suivez les recommandations du guide [Planification et réorientation : approche stratégique du pic de saison 2025](https://experienceleague.adobe.com/en/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025), qui fournit des stratégies exploitables à l’aide d’Adobe Commerce (et d’outils Adobe Experience Cloud facultatifs) pour vous aider à planifier, réorienter et offrir des expériences client exceptionnelles pendant la période la plus chargée de l’année.

### Bonnes pratiques

* Suivez le guide d’Adobe [Comment préparer votre infrastructure pour un trafic élevé : les 5 points de performance de la haute saison](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic).
* Consultez les [Conseils techniques pour une préparation aux vacances Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness) pour obtenir des conseils sur la préparation de votre infrastructure à un trafic élevé, la prévention des temps d’arrêt et l’optimisation des performances pendant la période de vacances.

+++

## Guide de préparation des vacances pour Adobe Experience Manager (AEM) {#aem}

+++**Cliquez pour afficher les recommandations de préparation des vacances pour Adobe Experience Manager (AEM).**

La saison des fêtes approche à grands pas et pour de nombreux clients d’Adobe, cela signifie l’apparition de périodes de pic des ventes. Dans notre engagement envers votre réussite, nous voulons nous assurer que vous êtes pleinement préparés à la prochaine augmentation du trafic.

### Services cloud de Adobe Experience Manager (AEM)

Si votre entreprise connaît ses moments les plus chargés pendant la saison des fêtes, vous pouvez réfléchir à la manière d’optimiser votre site Adobe Experience Manager pour répondre au trafic de pointe. Heureusement, avec les services cloud Adobe Experience Manager, votre site est déjà équipé de la fonctionnalité de mise à l’échelle automatique, ce qui garantit une expérience transparente pour vos visiteurs et visiteuses, peu importe s’il y a des changements soudains dans le trafic.

#### Préparation pour la mise à l’échelle

* Pour obtenir des informations détaillées et des conseils sur la préparation à un trafic élevé avec les services cloud Adobe Experience Manager, reportez-vous aux liens suivants :

   * [Réseau CDN dans AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [Mise en cache AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/caching/overview)

* Si vous êtes un client Ultimate Success et que vous avez récemment partagé des informations de prévision de volume avec l’équipe de votre compte Adobe, ne vous inquiétez pas de nous les renvoyer, car nous avons déjà une vue.

Nous sommes là pour vous accompagner à chaque étape de votre parcours. Pour toute question ou préoccupation, n’hésitez pas à [envoyer un ticket d’assistance](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Pour vous préparer à une campagne marketing pendant la saison des fêtes, consultez la documentation du [Guide de l’utilisateur d’AEMaaCS : Introduction - Paramètres de campagne marketing](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters) .

#### Sécurité et gouvernance

Pour plus d’informations sur la sécurité/protection du trafic sur les sites web AEM, reportez-vous à l’article [Présentation - Protection des sites web AEM](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) dans les tutoriels AEM as a Cloud Service.

#### Planification de la maintenance des vacances

Adobe a planifié des périodes d’exclusion de maintenance pour assurer un service ininterrompu pendant les périodes de vacances critiques :

* **Aucune mise à jour automatique** n’aura lieu entre :
   * 24 novembre 2025 - 2 décembre 2025
   * 15 Décembre 2025 - 2 Janvier 2026

Cela garantit la stabilité pendant les périodes de trafic élevé. Pour connaître le calendrier de publication complet et les fenêtres de maintenance, reportez-vous à la feuille de route de la version [AEM](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap).


### Adobe Experience Manager (AEM) avec Adobe Managed Services (AMS)

Les clients AEM qui utilisent Adobe Managed Services peuvent travailler de manière proactive avec leurs ingénieurs du service client pour planifier les besoins de couverture des fêtes.

++++

## Guide de préparation des vacances Adobe Marketo {#marketo}

+++**Cliquez pour afficher les recommandations de préparation des vacances d’Adobe Marketo.**

Pour garantir le succès des campagnes de vacances avec Adobe Marketo, les équipes doivent vérifier les paramètres d’authentification des e-mails, nettoyer et sécuriser leur base de données, optimiser la logique et la planification des campagnes, tester minutieusement le rendu et la délivrabilité des e-mails et rationaliser la préparation de l’assistance pour des performances et un engagement optimaux.

### Préparation pour la mise à l’échelle

* Vérifiez vos paramètres SPF/DKIM et assurez-vous que tout est toujours configuré et fonctionne correctement. Pour plus d’informations, consultez l’article [ Configurer SPF et DKIM pour la délivrabilité des e-mails ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability) .
* Contrôlez et nettoyez votre base de données Marketo en purgeant les enregistrements inactifs/non valides. Cela augmentera les chances que vos envois arrivent dans les boîtes de réception de vos prospects les plus prêts pour la vente. Pour plus d’informations, consultez l’article Contrôle de l’intégrité de la base de données [Marketo et Comment la garder propre ](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563) .
* Vérifiez que les membres de votre équipe disposent des autorisations appropriées pour effectuer des tâches et empêcher tout accès ou modification involontaire des e-mails. Que vous apportiez des modifications par le biais de l’**[!UICONTROL Admin]** ou de l’Admin Console ****, tout est prêt pour vous. Consultez l’article [ Gestion des rôles utilisateur et des autorisations ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions) .
* Passez en revue vos intégrations Launchpad pour vous assurer de leur authentification correcte et résolvez toutes les erreurs potentielles avant de les utiliser. Consultez l’article Guide du développeur de Marketo [Authentification](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication) .

### Bonnes pratiques

L’efficacité commence par la compréhension exacte de la manière dont Marketo priorise et traite les campagnes. Offrez à vos campagnes la vitesse nécessaire grâce à ces conseils d’optimisation.

* Il est essentiel de comprendre comment Marketo donne la priorité au traitement des étapes de flux de campagne pour éviter de retarder par inadvertance des e-mails urgents ou à priorité élevée. Consultez l’article [Fonctionnement du traitement de Campaign](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Gardez à l’esprit la logique de liste dynamique pour vous assurer que vos campagnes s’exécutent rapidement et avec des performances optimales. Consultez l’article [ Bonnes pratiques pour les listes dynamiques ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists) .
* **[!UICONTROL Démarrage rapide]** ou **[!UICONTROL Fuseau horaire du destinataire]** peuvent commencer à créer des e-mails avant votre envoi, ce qui réduit les retards et fournit un temps de préparation supplémentaire pour les prospects admissibles avec une logique à ressources élevées. Pour plus d’informations[ consultez les articles ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs)Démarrage rapide des programmes de messagerie et [Planification de programmes de messagerie avec fuseau horaire du destinataire](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone).
* Votre campagne est active, et les prospects arrivent, puis vous remarquez une erreur avec l’étape de flux . Il est tentant de corriger avec un ajustement rapide, mais être conscient de ce qui se passe lorsque vous modifiez une étape d&#39;attente en direct ou que vous réorganisez vos flux peut vous aider à éviter beaucoup de maux de tête et de nettoyage plus tard. Consultez l’article [ Modification d’un flux de campagne avec des membres dans des étapes d’attente ](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

### Tester et valider

Avant d’appuyer sur **[!UICONTROL Envoyer]**, assurez-vous que l’apparence et les performances de vos e-mails sont conformes à vos attentes.

* Marketo propose plusieurs méthodes pour tester l’apparence d’un e-mail afin de vous assurer qu’il ressemble exactement à ce que vous avez imaginé.
   * Utilisez la fonction **[!UICONTROL Aperçu]** pour vous assurer que le contenu dynamique et les jetons sont correctement rendus en les prévisualisant par segmentation ou prospects individuels. Voir l’article [Prévisualisation d’un e-mail avec du contenu dynamique](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content).
   * Envoyez rapidement et facilement un e-mail direct à vos enregistrements de test pour voir comment votre e-mail apparaît sur différents clients/appareils. Consultez l’article [Exécution d’une étape de flux unique à partir d’une liste dynamique](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list).
   * Pour les utilisateurs [!DNL Litmus], il est maintenant plus facile que jamais d’intégrer votre compte et de lancer des tests de rendu directement à partir de l’éditeur d’e-mail. Consultez l’article [Tester le rendu des e-mails avec [!DNL Litmus]](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering) .
* Consultez la fonctionnalité Rapport sur les courriers indésirables qui s’intègre à [!DNL SpamAssassin] pour examiner le contenu de votre e-mail et attribuer un score sur la probabilité qu’il atteigne la boîte de réception ou soit marqué comme *spam*. Voir l’article [ Rapport sur les courriers indésirables ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report).
* Surveillez [!UICONTROL File d’attente de Campaign] pour vous assurer que vos campagnes traitent et hiérarchisent correctement les éléments de haute urgence. Pour plus d&#39;informations, consultez la section [ Ma campagne est-elle en cours ?](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662) article.

### Rationaliser votre expérience d’assistance

En cas de problème, la vitesse a son importance et l’assistance Marketo est là pour vous aider ! Incluez ces détails dans votre dossier de support afin d’éviter les allers-retours et d’aider notre équipe à trouver une solution plus rapide. Consultez l’article [ Bonnes pratiques relatives à l’utilisation de la prise en charge de Marketo ](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491).

Grâce à ce guide, vous pouvez vous reposer un peu plus facilement en sachant que vous commencez en position de force pour stimuler l&#39;engagement et les conversions pendant cette période critique. Les enjeux sont élevés, mais votre stress n&#39;a pas à l&#39;être. Commencez vos préparatifs dès aujourd&#39;hui et faites de cette période des Fêtes votre saison la plus réussie.

+++

## guide de préparation des vacances Adobe Workfront {#workfront}

+++**Cliquez pour afficher les recommandations de préparation des vacances d’Adobe Workfront.**

Pour préparer Adobe Workfront pour les fêtes de fin d’année, les équipes doivent mettre à jour les contacts d’assistance, aligner les plannings internes avec Adobe, éviter les modifications majeures pendant les périodes de pointe et surveiller de manière proactive les automatisations et les intégrations pour assurer le bon fonctionnement.

### Préparation pour la mise à l’échelle

Pour garantir un support fluide pendant les vacances :

* Passez en revue et mettez à jour vos contacts d’assistance autorisés à l’avance.
* Vérifiez que les principales parties prenantes sont disponibles pour collaborer avec l’assistance en cas de problèmes critiques.
* Si vous planifiez des modifications de produit ou de workflow pendant la période des vacances, pensez à les planifier avant la mi-novembre ou après le début du mois de janvier, afin de bénéficier de meilleurs délais.
* Communiquez les horaires de vacances internes à vos contacts Adobe pour assurer l’alignement.

### Tester et valider

Tenez-vous informé des versions de Workfront et testez les nouvelles fonctionnalités dans les environnements Sandbox :

* [Préparation à une version d’Adobe Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Archive des notes de mise à jour de Workfront](https://experienceleague.adobe.com/fr/docs/workfront/using/product-announcements/product-releases/product-releases)
* [Présentation De La Version Du Premier Trimestre 2025](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* Enregistrement du webinaire de mise à jour de [Workfront](https://experienceleague.adobe.com/en/docs/events/workfront-recordings/releases/25-1-release-webinar)

### Bonnes pratiques

* Planification proactive : identifier les dépendances du système ou les automatisations planifiées qui peuvent être affectées par les calendriers de congés internes.
* Communication continue : informez vos équipes internes et l’assistance Adobe de la maintenance planifiée ou des événements clés.
* Utilisez des tableaux de bord : surveillez les intégrations et les automatisations clés afin de détecter les premiers signes de problèmes de performances.
* Transmission anticipée : si vous anticipez ou constatez une dégradation du service, ouvrez immédiatement un ticket d’assistance - n’attendez pas qu’il devienne critique.

En planifiant, en maintenant une communication claire et en réagissant rapidement aux problèmes, les entreprises peuvent minimiser les perturbations et s’assurer que Workfront continue à prendre en charge les workflows critiques tout au long de la période de vacances.

+++

## guide de préparation des vacances Adobe Campaign {#campaign}

+++**Cliquez pour afficher les recommandations de préparation des vacances d’Adobe Campaign.**


Pour préparer Adobe Campaign aux fêtes de fin d’année, les équipes doivent valider de manière proactive les paramètres de délivrabilité, optimiser la segmentation des audiences et la fréquence des messages, assurer l’évolutivité de l’infrastructure et tester l’orchestration des campagnes cross-canal pour gérer efficacement les pics de volume et d’engagement saisonniers.

### Conseils d’experts pour que vos campagnes de vacances se démarquent

Comme il n’est jamais trop tôt pour commencer vos achats de vacances, il n’est jamais trop tôt non plus pour commencer à planifier une campagne marketing largement réussie pour les vacances. Avec Adobe Campaign, vous pouvez concevoir, planifier et exécuter des campagnes qui réaliseront tous les vœux de vacances de votre entreprise. Mais connaissez-vous tous les conseils pour lancer des campagnes qui termineront l’année en apothéose ? Regardez cette vidéo, [Conseils d’experts pour que vos campagnes de vacances se démarquent](https://experienceleague.adobe.com/en/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03), qui aborde les bonnes pratiques en matière de délivrabilité et d’exécution et vous montrera comment tout faire dans Adobe Campaign.

### Considérations et préparatifs pour la période de vacances

Cette vidéo, [Adobe Campaign : préparation des vacances - Considérations et préparations pour la période des vacances](https://helpx.adobe.com/customer-care-office-hours/campaign/campaign-holiday-readiness.html), couvre les sujets suivants :

* Impliquer la communauté Campaign
* Délivrabilité - Points à prendre en compte pour les fêtes et au-delà !
* Recommandations techniques pour Adobe Campaign Classic (ACC) et Adobe Campaign Standard (ACS)

Pour qu’Adobe Campaign soit prêt pour la haute saison des fêtes, les entreprises doivent finaliser les contrôles de délivrabilité, valider les configurations des campagnes et s’assurer que l’infrastructure évolutive et l’orchestration cross-canal sont en place pour exécuter en toute confiance des campagnes à volume élevé et sensibles au facteur temps tout au long de la saison des fêtes.

+++

## guide de préparation des vacances Adobe Analytics {#analytics}

+++**Cliquez pour afficher les recommandations de préparation des vacances d’Adobe Analytics.**

À l’approche de la saison des fêtes, les entreprises qui utilisent Adobe Analytics doivent prendre des mesures proactives pour garantir la précision des données, les performances de la plateforme et la fiabilité des rapports pendant les périodes de pointe du trafic. Adobe fournit plusieurs ressources et bonnes pratiques pour aider les équipes à se préparer efficacement.

### Prédire le trafic

Afin d’assurer une allocation matérielle et une réactivité système adéquates, Adobe recommande d’envoyer à l’avance les **volumes d’accès/d’appels au serveur par heure de pointe et quotidiens**.

* Vérifiez [la planification des pics de trafic et les délais d’allocation du matériel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times), car il est essentiel de comprendre la rapidité avec laquelle les données sont disponibles pour la prise de décision en temps réel pendant les périodes de volume élevé.

* Découvrez les impacts sur la disponibilité et la latence des données dans Adobe Analytics dans la [présentation de la latence des données d’Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/technotes/latency) y compris les pics de trafic inattendus et les problèmes matériels, et découvrez les stratégies recommandées pour réduire les retards de données.

### Bonnes pratiques

Pour les équipes qui utilisent les flux de données pour exporter des données analytiques brutes, Adobe fournit des conseils sur l’optimisation des configurations de flux et la prévention des pièges courants.

* [Bonnes pratiques relatives aux flux de données Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

Pour garantir la création de rapports rapide et fiable pendant les vacances, Adobe recommande les mesures suivantes :

* [Optimisation des performances d’Analysis Workspace](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Dépannage et bonnes pratiques pour Report Builder : recommandations pour l’optimisation des requêtes](https://experienceleague.adobe.com/en/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Guide des composants Analytics : file d’attente des rapports planifiés](https://experienceleague.adobe.com/en/docs/analytics/components/scheduled-reports-admin)

### Planification de la maintenance des vacances

Adobe applique généralement les **fenêtres d’exclusion de maintenance** pendant les périodes de pointe des vacances afin d’assurer la continuité du service. Les clients doivent surveiller les calendriers de publication et de maintenance d’Adobe via Experience League et se coordonner avec les équipes de compte Adobe pour la planification de l’assistance.

En suivant ces directives et en utilisant la documentation publique d’Adobe, les entreprises peuvent s’assurer que leur implémentation d’Adobe Analytics est robuste, réactive et prête à répondre aux exigences de la période des fêtes.

+++

## guide de préparation des vacances Adobe Target {#target}

+++**Cliquez pour afficher les recommandations de préparation des vacances d’Adobe Target.**

La saison des fêtes apporte son lot d’opportunités d’engagement passionnantes, mais elle s’accompagne également de défis tels que les augmentations de trafic et la demande accrue sur les systèmes de personnalisation. Afin de vous aider à offrir des expériences transparentes pendant cette période critique, nous avons compilé des recommandations essentielles pour nous assurer que votre implémentation d’Adobe Target est prête.

### Prévoir la demande

Commencez par anticiper les pics de trafic de 20 à 50 % ou plus et par vérifier que votre infrastructure peut gérer la charge. Prévoyez l’activité et les volumes de données dans Adobe Target, Analytics et AEP pour éviter les surprises.

Il est également important d’identifier les parcours essentiels à la mission (tels que la commande, les recommandations de produits et les offres promotionnelles) afin que les efforts de personnalisation se concentrent là où ils comptent le plus.

Pour plus d&#39;informations, consultez la section [Bonnes pratiques d&#39;optimisation avec Adobe Target](https://experienceleague.adobe.com/en/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization).

### Préparation pour la mise à l’échelle

* Prévoyez l’augmentation du trafic sur le site web et les appareils mobiles et informez l’équipe d’assistance de Target afin d’augmenter la capacité du serveur et d’éviter tout appel bloqué.
* Pour tout test de chargement/ouverture, l’équipe d’assistance de Target doit être informée à l’avance.
* Effectuez la mise à niveau vers les dernières versions de l’API `at.js`/Delivery.
* Geler les modifications non critiques ; préparer les expériences de secours.
* Aligner les processus d’assistance et de réaffectation et activer les alertes proactives.

### Tester et valider

Validez la diffusion de contenu à l’aide des liens [QA](https://experienceleague.adobe.com/en/docs/target/using/activities/activity-qa/activity-qa) pour confirmer que tout fonctionne comme prévu. Utilisez le bouton (bascule) **[!UICONTROL Faire correspondre les règles d’audience pour afficher les expériences]** afin de vous assurer que la bonne audience est admissible pour l’activité que vous testez. Vérifiez à nouveau que votre configuration **[!UICONTROL mesure d’objectif]** est alignée sur l’**[!UICONTROL objectif]** de l’activité. Et toujours avoir un plan de sauvegarde prêt - juste au cas où.

### Bonnes pratiques

Maintenez votre implémentation dans les [limites d’Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/troubleshoot/target-limits) et vérifiez à l’avance la conformité [au RGPD et au CCPA](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation) avant de lancer. Conservez moins de 100 activités actives et archivez les plus anciennes pour rationaliser les opérations. Tirez parti de l’**[!UICONTROL affectation automatique]**/**[!UICONTROL ciblage automatique]** pour une optimisation pilotée par l’IA. Établissez des plans de restauration et des tableaux de bord de surveillance en temps réel.

### Sécurité et gouvernance

Avant de personnaliser les expériences, vérifiez que le consentement est conforme au RGPD et au CCPA. Évitez de stocker des informations d’identification personnelle dans les paramètres de profil et validez la sécurité de l’API pour protéger les données client.

+++
