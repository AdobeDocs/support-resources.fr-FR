---
title: Surveillance et observabilité
description: Recommandations de surveillance et d’observabilité pour aider les commerçants Adobe Commerce à préparer leurs environnements aux événements à trafic élevé, tels que la saison des fêtes.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
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
source-wordcount: '517'
ht-degree: 2%
---

# Surveillance et observabilité

Cette section fournit des recommandations techniques pour la surveillance des environnements Adobe Commerce en vue de la préparation aux événements à trafic élevé tels que la saison des fêtes.

>[!NOTE]
>
>Les étapes marquées **(cloud uniquement)** s’appliquent à Commerce sur les infrastructures cloud. La plupart des autres recommandations s’appliquent également aux déploiements sur site.

## Surveillance du trafic avec New Relic (cloud uniquement) {#monitor-traffic-with-new-relic}

Adobe Commerce sur les infrastructures cloud comprend un abonnement à la plateforme d’observabilité [!DNL New Relic], qui incorpore de manière transparente la diffusion en continu des journaux [!DNL Fastly] dans les [!DNL New Relic] en temps quasi réel. Cette intégration vous permet de surveiller vos modèles et tendances de trafic en temps réel, afin que vous puissiez prendre des mesures correctives.

Utilisez ces journaux pour :

* Identifiez les pays d’où proviennent vos requêtes web.
* Identifiez les adresses IP ou les agents utilisateurs abusifs qui explorent à votre site.
* Identifiez le trafic malveillant ciblant des points d’entrée spécifiques, tels que le paiement.
* Créez des rapports sur les types d’appareils et de navigateurs utilisés par vos clients.

Par exemple, surveillez le pays source de votre trafic pour confirmer qu’il reflète l’emplacement géographique de vos promotions et de vos clients :

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

Modifiez cette requête en fonction de vos besoins, segmentez-la davantage ou transformez-la en tableau de bord pour un suivi centralisé. Pour plus d’informations, consultez la section [Gestion des journaux &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Personnalisation des alertes New Relic (cloud uniquement) {#customize-new-relic-alerts}

Outre les alertes gérées définies par Adobe Commerce sur les infrastructures cloud, vous pouvez définir un large éventail d’alertes et de notifications pour votre plateforme pendant la haute saison des ventes. Par exemple, vous informer du trafic de robots ou d’un temps de réponse accru sur une requête GraphQL. Consultez [Alertes gérées pour Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce) pour obtenir la liste complète des alertes intégrées.

Les alertes [!DNL New Relic] et l’IA prennent en charge les structures de requête NRQL. Configurez des alertes personnalisées depuis le tableau de bord [!DNL New Relic] sous **[!UICONTROL Alertes et IA]**.

## Examiner le score Apdex (cloud uniquement) {#review-apdex-score}

Le score Apdex mesure la satisfaction des utilisateurs quant au temps de réponse de vos applications et services web. Vous pouvez consulter le score Apdex de votre Adobe Commerce sur l’infrastructure cloud à l’aide de [!DNL New Relic].

Un score Apdex est compris entre 0 et 1. Un score de 0 est le pire score possible, ce qui signifie que 100 % des temps de réponse ont été **frustrés**. Un score de 1 est le meilleur score possible, ce qui signifie que 100 % des temps de réponse ont été **satisfaits**. [!DNL New Relic] signale à la fois un score du serveur d’applications, qui reflète les performances du serveur principal, et un score de l’utilisateur final, qui reflète les performances côté client.

Un score Apdex de 0,5 ou inférieur justifie une enquête. Un score inférieur à 0,4 est considéré comme une panne.

Avec Apdex, [!DNL New Relic] fournit toute une gamme de statistiques pour analyser les problèmes de performances d’Adobe Commerce sur les infrastructures cloud. Pour connaître les étapes, voir [Dépannage des performances à l’aide de New Relic sur Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce).

## Vérifier les informations d’assistance (rapport SWAT) {#review-support-insights-swat-report}

Pour obtenir un rapport plus détaillé sur votre environnement, générez un rapport SWAT (Site-Wide Analysis Tool). Pour plus d’informations sur l’outil SWAT, voir [&#x200B; Outil d’analyse à l’échelle du site &#x200B;](https://experienceleague.adobe.com/fr/docs/commerce-operations/tools/site-wide-analysis-tool/intro).