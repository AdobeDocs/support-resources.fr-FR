---
title: Obtention et application d’un [!UICONTROL &#x200B; correctif de sécurité &#x200B;]
description: Cet article fournit des instructions sur la manière d’obtenir et d’appliquer un [!UICONTROL correctif de sécurité] qui a été publié, mais les instructions ne sont pas disponibles.
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 9a4d96e06b949e4c229fdf0f084810b27bf8b346
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Obtention et application d’un [!UICONTROL correctif de sécurité]

>[!NOTE]
>Si vous disposez d’une installation On-Premise et que vous n’utilisez pas de systèmes de contrôle de version tels que [!DNL CVS] ou GitHub pour gérer votre code, votre hôte web peut vous aider à appliquer le correctif. N’hésitez pas à les contacter pour obtenir de l’aide.

Cet article fournit des instructions sur la manière d’obtenir et d’appliquer un [!UICONTROL correctif de sécurité] qui a été publié, mais les instructions ne sont pas disponibles.

## Produits et versions concernés

Infrastructure on-premise et cloud Adobe Commerce - toutes les versions prises en charge


## Cause

Pour les bulletins de sécurité Adobe Commerce, Adobe fournit uniquement un fichier de correctif ou un correctif logiciel isolé lorsque cet artefact est explicitement publié dans le bulletin. Si aucun correctif ou correctif isolé n’est publié ou référencé dans les documents du bulletin, Adobe ne crée pas de correctif autonome distinct par la suite.

En effet, les correctifs de sécurité sont conçus, validés et publiés ensemble dans le cadre de la version de sécurité prise en charge pour la ligne de version applicable.

Par conséquent, le chemin de mise à jour pris en charge consiste à appliquer la mise à jour de sécurité officielle pour la ligne de version concernée ou à effectuer une mise à niveau vers une version contenant déjà le correctif.

## Solution


### Cas I :

* Si un fichier de correctif ou un correctif logiciel isolé est mentionné dans les [notes de mise à jour](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite), téléchargez le fichier à partir de la section de téléchargement de [https://account.magento.com](https://account.magento.com/downloads/view/). Les utilisateurs d’accès partagé doivent d’abord recevoir des privilèges de téléchargement de la part du propriétaire du compte ou du titulaire de licence.

**Avertissements:**

* Adobe Commerce 2.4.6 reste pris en charge sous Prise en charge étendue jusqu’au 30 août 2027.

* Adobe Commerce 2.4.5 reste sous prise en charge étendue jusqu’au 11 août 2026. Passée cette date, Adobe ne fournit les correctifs de sécurité que jusqu’au 31 mai 2027.

* Adobe Commerce 2.4.4 ne bénéficie plus de la prise en charge étendue. Adobe fournit des correctifs de sécurité uniquement jusqu’au 31 mai 2027.

* Pour Adobe Commerce 2.4.4 et 2.4.5, Adobe fournit uniquement des fichiers de correctifs de sécurité. Ces mises à jour n’incluent pas les éléments suivants :

   * Assistance technique ou assistance technique Adobe Commerce
   * Correctifs de qualité
   * Mises à jour des dépendances de la plateforme ou du système d’exploitation

Les versions non prises en charge (2.3.x et 2.4.0 à 2.4.3) ne sont pas éligibles à la prise en charge. Vous pouvez effectuer une mise à niveau vers une version prise en charge pour recevoir les derniers correctifs de sécurité.

### Cas II :

Les correctifs isolés ne sont fournis que dans des cas exceptionnels et ne constituent pas la méthode privilégiée pour implémenter des correctifs de sécurité.

Si un fichier de correctif ou un correctif logiciel isolé n’est pas mentionné dans les notes de mise à jour, suivez ces instructions :

>[!IMPORTANT]
>
>Si un fichier de correctif ou un correctif logiciel isolé n’est pas explicitement publié pour un problème de sécurité, mettez à niveau l’application Adobe Commerce complète vers la dernière version de correctif logiciel applicable pour la ligne de version concernée.

**Cloud:**

1. Certains [!UICONTROL correctifs de sécurité] peuvent être inclus/publiés dans la dernière version de Cloud Tools Suite (outils ECE) sous Cloud Patches pour Commerce. Vérifiez les [notes de mise à jour](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) et si un correctif de sécurité est mentionné dans la version, mettez à niveau le package vers cette version.
1. Si les notes de mise à jour ne mentionnent pas de correctif de sécurité, poursuivez la lecture.

**Infrastructure cloud ou On-Premise :**

* Si aucun fichier de correctif ou correctif logiciel isolé n’est disponible, [mettez à niveau la version Adobe Commerce sur l’infrastructure cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X vers la dernière version du correctif 2.4.X-pY.
* Si aucun fichier de correctif ou correctif logiciel isolé n&#39;est disponible, [mettez à niveau la version On-Premise d&#39;Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X vers la dernière version de correctif 2.4.X-pY.

## Lecture connexe

* Voir [Notes de mise à jour de la suite d’outils Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) dans le *Guide d’Adobe Commerce sur les infrastructures cloud*.
* Voir [Mise à niveau de la version d’Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) dans le *Guide d’Adobe Commerce sur les infrastructures cloud*.
