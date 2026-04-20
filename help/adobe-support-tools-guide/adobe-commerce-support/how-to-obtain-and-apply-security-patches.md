---
title: Obtention et application d’un [!UICONTROL &#x200B; correctif de sécurité &#x200B;]
description: Cet article fournit des instructions sur la manière d’obtenir et d’appliquer un [!UICONTROL correctif de sécurité] qui a été publié, mais les instructions ne sont pas disponibles.
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: eee15976f3dd402e84774ec5b769d952259c8dff
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Obtention et application d’un [!UICONTROL correctif de sécurité]

>[!NOTE]
>Si vous disposez d’une installation On-Premise et que vous n’utilisez pas de systèmes de contrôle de version tels que [!DNL CVS] ou GitHub pour gérer votre code, votre hôte web peut vous aider à appliquer le correctif. N’hésitez pas à les contacter pour obtenir de l’aide.

Cet article fournit des instructions sur la manière d’obtenir et d’appliquer un [!UICONTROL correctif de sécurité] qui a été publié, mais les instructions ne sont pas disponibles.

## Produits et versions concernés

Infrastructure on-premise et cloud Adobe Commerce - toutes les versions prises en charge


## Cause

La plupart des [!UICONTROL correctifs de sécurité] sont publiés sans correctif ou correctif isolé à appliquer et nécessitent une mise à niveau vers la version [!UICONTROL correctif de sécurité].

Pour les bulletins de sécurité Adobe Commerce, Adobe ne fournit un fichier de correctif/correctif physique distinct que lorsqu’il est explicitement publié/mentionné dans le cadre de la publication du bulletin. Si le bulletin n&#39;inclut pas (ou ne fait pas référence) à un correctif ou à un package de correctif isolé, nous ne sommes pas en mesure d&#39;en générer et d&#39;en fournir un après coup.

En effet, les correctifs de sécurité sont développés, testés et livrés ensemble dans le cadre de la version de sécurité prise en charge (par exemple, une version de correctif), et ils ne sont pas conçus pour être clairement séparés/découplés en fichiers de correctifs CVE individuels sans risquer une couverture incomplète ou des régressions.

Le chemin de mise à jour pris en charge continue d’appliquer la mise à jour de sécurité officielle pour votre ligne de version (ou d’effectuer une mise à niveau vers une version qui comprend les correctifs).

## Solution


### Cas I :

* Si un fichier de correctif ou un correctif logiciel isolé est mentionné dans les [notes de mise à jour](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite), téléchargez le fichier à partir de la section de téléchargement de [https://account.magento.com](https://account.magento.com/downloads/view/). Les utilisateurs d’accès partagé doivent d’abord recevoir des privilèges de téléchargement de la part du propriétaire du compte ou du titulaire de licence.

**Avertissements:**

Si vous utilisez une ancienne version d’Adobe Commerce (2.4.4), vous aurez automatiquement reçu la prise en charge étendue. Votre version doit être l&#39;une des versions non prises en charge suivantes pour pouvoir appliquer les derniers correctifs de sécurité disponibles :

2.4.4 - 2.4.4-p11

Les versions non prises en charge (2.3.x, 2.4.0 à 2.4.3) ne sont pas éligibles à la prise en charge. Vous devez d’abord effectuer une mise à niveau vers une version prise en charge pour tirer parti des derniers correctifs de sécurité.

Si vous ne disposez pas de la prise en charge étendue, vous pouvez demander à l’assistance de partager les correctifs avec vous, mais ils ne pourront pas résoudre les problèmes/erreurs que vous pourriez rencontrer lors de leur application.

### Cas II :

Les correctifs isolés ne sont fournis que dans des cas exceptionnels, et il ne s&#39;agit pas de la forme préférée de mise en œuvre de correctifs de sécurité.

Si un fichier de correctif/correctif isolé n’est pas mentionné dans les notes de mise à jour :

* **Cloud:**

1. Certains [!UICONTROL correctifs de sécurité] peuvent être inclus/publiés dans la dernière version de Cloud Tools Suite (outils ECE) sous Cloud Patches pour Commerce. Vérifiez les [notes de mise à jour](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) et si un correctif de sécurité est mentionné dans la version, mettez à niveau le package vers cette version.
1. Si les notes de mise à jour ne mentionnent pas de correctif de sécurité, poursuivez la lecture.

* **Infrastructure cloud ou On-Premise :**

* Si aucun fichier de correctif ou correctif logiciel isolé n’est disponible, [mettez à niveau la version Adobe Commerce sur l’infrastructure cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X vers la dernière version du correctif 2.4.X-pY.
* Si aucun fichier de correctif ou correctif logiciel isolé n&#39;est disponible, [mettez à niveau la version On-Premise d&#39;Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X vers la dernière version de correctif 2.4.X-pY.

## Lecture connexe

* Voir [Notes de mise à jour de la suite d’outils Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) dans le *Guide d’Adobe Commerce sur les infrastructures cloud*.
* Voir [Mise à niveau de la version d’Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) dans le *Guide d’Adobe Commerce sur les infrastructures cloud*.
