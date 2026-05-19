---
title: Comment demander une mise à niveau temporaire d’Adobe Commerce sur une infrastructure cloud
description: Si votre organisation prévoit un événement en ligne générant un trafic élevé, ou si vous constatez soudainement que votre site fait l’objet d’un événement à trafic élevé, vous pouvez déposer un [ticket d’assistance] (https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) pour demander une capacité cloud supplémentaire temporaire pour votre Adobe Commerce sur le magasin d’infrastructure cloud.
solution: Commerce
exl-id: 203882c0-929a-4bb3-afff-738bc518b46b
TQID: https://experienceleague.adobe.com/9--JwGLuX01kXR569r1OjVrkiTd2BQa-j-gOTs9oKGY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: d1c3158bb425e7966ccc5e5d79457c6b33e00063
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 1%

---

# Comment demander une mise à niveau temporaire d’Adobe Commerce sur une infrastructure cloud

Si votre organisation prévoit un événement en ligne générant un trafic élevé, ou si vous constatez soudainement que votre site fait l’objet d’un événement à trafic élevé, vous pouvez déposer un [ticket d’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) afin de demander une capacité cloud supplémentaire temporaire pour votre boutique Adobe Commerce sur l’infrastructure cloud.

>[!NOTE]
>
>Un préavis de 48 heures ouvrables est requis pour les demandes de mise à niveau non urgentes. Les mises à niveau pour les campagnes promotionnelles ne sont pas considérées comme des urgences à moins que le site ne soit complètement non fonctionnel ou reçoive un trafic beaucoup plus élevé que prévu et que les performances aient été gravement dégradées.

## Produits et versions concernés

* Adobe Commerce sur les infrastructures cloud, toutes les [versions prises en charge](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Comment identifier les événements à trafic élevé

Dans les alertes New Relic, vous pouvez utiliser des conditions d’alerte de base pour définir des seuils qui s’adaptent au comportement de vos données.

Les alertes de ligne de base sont utiles pour créer des conditions d’alerte qui :

* Ne vous avertissez que lorsque les données se comportent de manière anormale.
* S’adapter de manière dynamique aux données et aux tendances changeantes, y compris les tendances quotidiennes ou hebdomadaires

En outre, les alertes de base fonctionnent bien avec les nouvelles applications lorsque vous n’avez pas encore de comportements connus.

Suivez ce lien pour en savoir plus sur New Relic [détection des anomalies avec intelligence appliquée](https://docs.newrelic.com/docs/alerts-applied-intelligence/applied-intelligence/anomaly-detection/anomaly-detection-applied-intelligence/).

Si vous recevez une notification d’alerte suggérant un événement de trafic élevé, vous devrez peut-être envisager de [soumettre un ticket d’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) pour demander une capacité supplémentaire. Procédez comme suit.

## Comment surveiller les performances de votre site

Adobe fournit un ensemble de politiques d’alerte New Relic pour Adobe Commerce sur les infrastructures cloud, Pro plan architecture et Adobe Commerce sur les infrastructures cloud, Starter plan architecture Environnements de production permettant le suivi des mesures de performances clés suivantes :

* [Score Apdex](https://docs.newrelic.com/docs/apm/new-relic-apm/apdex/apdex-measure-user-satisfaction)
* Taux d’erreurs
* Espace disque (disponible sur les environnements de production Pro Architecture uniquement)

Basées sur les bonnes pratiques du secteur, ces politiques définissent des seuils pour les conditions d’avertissement et critiques qui affectent les performances. Lorsque votre site rencontre un problème d’infrastructure ou d’application qui déclenche un seuil d’alerte, New Relic envoie des notifications d’alerte afin que vous puissiez résoudre le problème de manière proactive. Pour utiliser ces politiques, vous devez configurer des canaux de notification pour recevoir les messages d’alerte.

Suivez ce lien pour découvrir comment [configurer des alertes basées sur les performances](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/new-relic-service#monitor-performance-with-managed-alerts).

## Étapes de demande de mise à niveau temporaire

Pour demander une capacité cloud supplémentaire temporaire, envoyez un [ticket d’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) au Centre d’assistance Adobe Commerce avec les informations suivantes :

>[!NOTE]
>
>Le choix *Holiday Surge Request* n&#39;est possible que pendant les mois d&#39;octobre à décembre.

1. Sélectionnez le produit [!DNL Adobe Commerce] pour lequel vous avez besoin d’une assistance :
   * [!DNL Commerce Cloud]
   * [!DNL Commerce on Managed Service]

1. Renseignez les champs suivants :
   * **[!UICONTROL Titre du cas]**
   * **[!UICONTROL Description du cas]** *(assurez-vous qu’elles décrivent clairement le problème et le contexte.)*

1. Sélectionnez *Demande de modification d’infrastructure* dans le menu déroulant **[!UICONTROL Motif de l’événement]**.

1. Sélectionnez **[!UICONTROL Environnement]** dans le menu déroulant.

1. Sélectionnez la **[!UICONTROL version du produit]** appropriée dans le menu déroulant.

1. Sélectionnez *Redimensionnement du projet cloud (vCPU)* dans le menu déroulant **[!UICONTROL Quelle modification d’infra-système vous souhaitez effectuer aujourd’hui]**.

1. **Sélectionnez l’option [!UICONTROL Architecture]** :
   * *Architecture par défaut :* sélectionnez *Taille disponible suivante* dans le menu déroulant **Sélectionner la taille**.
   * *Architecture à l’échelle :* lorsque cette option est sélectionnée, l’écran se modifie pour afficher deux champs supplémentaires :
      * *Taille du nœud web*
      * *Taille du nœud de service* *(saisissez les tailles souhaitées pour chaque nœud)*

1. Saisissez la **[!UICONTROL Date de début]** au format UTC (date et heure).

1. Saisissez la **[!UICONTROL Date de fin]** au format UTC (date et heure).

1. Fournissez **[!UICONTROL URL du projet]** *(disponible sous https://accounts.magento.cloud/, généralement au format `https://[REGION].magento.cloud/projects/PROJECT_ID`)*

1. Saisissez l’**[!UICONTROL ID du projet]**.

1. Indiquez **[!UICONTROL URL concernée]** *(doit commencer par `http://` ou `https://`.)*

1. Sélectionnez **[!UICONTROL Priorité]**.

1. Sélectionnez **[!UICONTROL Impact commercial]**.

1. Confirmez **[!UICONTROL Fuseau horaire]** *(par exemple, `(UTC-5:00) Indiana (East)`)*

1. Saisissez **[!UICONTROL Numéro de téléphone]** *(par exemple, `+12015550123`)*

1. Cliquez sur **[!UICONTROL Soumettre]** pour finaliser votre dossier d’assistance.

>[!NOTE]
>
>Une fois la mise à niveau planifiée, un système automatisé ajuste la taille de votre instance cloud. Vous ne pouvez pas recevoir de notification de ticket une fois la procédure terminée. Vous pouvez utiliser l’outil Observation pour Adobe Commerce pour afficher vos types d’instances AWS ou Azure afin de [vérifier la modification](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/check-vcpu-using-observation-for-adobe-commerce).

## Afficher l&#39;historique de vos uptailles

Vous pouvez afficher l’historique des redimensionnements demandés en demandant les informations à votre **CSM (Customer Success Manager)**.
Les informations suivantes sont disponibles pour chaque demande de redimensionnement :

* **Date de début de la taille** : date de la demande de mise à niveau.
* **Date de fin de la taille** : date à laquelle le cluster a été rétabli à sa taille précédente.
* **taille du processeur virtuel** : taille du cluster après la mise à niveau.
* **Utilisation en jours** : nombre de jours pendant lesquels le cluster a été mis à niveau.
* **Période vCPU** : modification de la taille du vCPU en fonction du nombre de jours d&#39;utilisation. (par exemple, la taille de vCPU 192 par 25 jours est égale à 4 800).


## Lecture connexe

* Pour obtenir des informations, des méthodes et des exemples sur la manière de mesurer et d’améliorer les performances du site, reportez-vous aux articles détaillés suivants de notre base de connaissances d’assistance :
   * [calcul de l’allocation de CPU pour Adobe Commerce sur le cloud](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-cpu-allocation-calculation)
   * [Vérifiez si une mise à niveau des instances de l’hôte est nécessaire pour Adobe Commerce sur le cloud](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-if-upsize-for-hosts-instances-is-needed)
   * [Vérifiez la configuration CPU de l’hôte pour Adobe Commerce sur le cloud.](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-hosts-cpu-configuration)
* Pour plus d’informations sur l’identification des pannes, reportez-vous à la section [Identification et mesure des pannes pour Adobe Commerce sur le cloud](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/how-to-identify-outages) dans notre base de connaissances du support.
* Pour plus d’informations sur l’amélioration des performances du site afin d’éviter d’avoir à utiliser une augmentation de la capacité, consultez ces articles dans la documentation destinée aux développeurs :
   * [Dimensionnement de l’image](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#product-image-resizing)
   * [Mise en cache complète de la page](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cache-management#full-page-caching)
   * [Outils CEE](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/package-overview)
