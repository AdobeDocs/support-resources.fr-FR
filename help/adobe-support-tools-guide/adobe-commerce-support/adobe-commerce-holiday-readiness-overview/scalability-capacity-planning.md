---
title: Planification de l’évolutivité et des capacités
description: Recommandations en matière de planification de l’évolutivité et de la capacité pour aider les commerçants Adobe Commerce à préparer leurs environnements aux événements à trafic élevé tels que la saison des fêtes.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# Planification de l’évolutivité et des capacités

Cette section fournit des recommandations techniques pour la mise à l’échelle des environnements Adobe Commerce en vue de la préparation aux événements à trafic élevé tels que la saison des fêtes.

>[!NOTE]
>
>Les étapes marquées **(cloud uniquement)** s’appliquent à Commerce sur les infrastructures cloud. La plupart des autres recommandations s’appliquent également aux déploiements sur site.

## Planifier la mise à niveau anticipée du cluster (cloud uniquement) {#plan-cluster-upsize-early}

Pour les clients Commerce sur les infrastructures cloud , une mise à niveau temporaire de cluster alloue davantage de ressources informatiques pour gérer les pics de trafic en haute saison. Préparez un ticket d’assistance à l’avance, en indiquant la période et la taille de cluster requise, et assurez-vous de consulter votre gestionnaire de compte dédié sur la consommation et les exigences actuelles en matière de ressources. Envoyez la demande au moins 48 heures ouvrables avant que la capacité ne soit nécessaire. En particulier pendant la période des fêtes, envoyez-la le plus tôt possible, car la capacité pendant le Black Friday et le Cyber Monday est limitée. Voir [Comment demander une mise à niveau temporaire &#x200B;](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize).

Par exemple, un client Pro-architecture avec une base quotidienne de 24 cœurs (24 processeurs virtuels, 96 Go de RAM) passant à 96 cœurs pendant 7 jours utiliserait environ 4 fois plus de ressources (96 processeurs virtuels, 384 Go de RAM), soit une consommation incrémentielle d’environ 504 jours processeur virtuel (96×7 − 24×7).

## Blindage d&#39;origine rapide {#fastly-origin-shielding}

L’objectif du blindage d’origine d’Adobe Commerce [!DNL Fastly] est de réduire le trafic directement à l’origine Adobe Commerce. Lorsqu’une requête est reçue, un emplacement de périphérie [!DNL Fastly] (point de présence) vérifie le contenu mis en cache et le diffuse. S’il n’est pas mis en cache, il continue vers le Shield POP pour vérifier s’il y est mis en cache. Si le contenu a déjà été demandé, même à partir d’un autre POP global, il sera mis en cache. Enfin, s’il n’est pas mis en cache sur le Shield POP, il se rendra uniquement sur le serveur d’origine.

[!DNL Fastly] blindage d’origine peut être activé dans l’administration Adobe Commerce, dans les paramètres du serveur principal de configuration [!DNL Fastly]. Choisissez un emplacement de protection le plus proche de votre centre de données d’origine Adobe Commerce pour obtenir les meilleures performances. Pour plus d’informations, consultez [Configuration des back-ends et du blindage d’origine](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding). Par défaut, le blindage d&#39;origine [!DNL Fastly] n&#39;est pas activé.

## Test de chargement et de basculement {#conduct-load-and-failover-tests}

Effectuez des tests de chargement et de récupération avant les campagnes majeures afin de valider les configurations de mise à l’échelle et les plans de restauration.