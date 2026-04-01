---
title: Créer des rapports d’attribution de licence pour plusieurs organisations et produits
description: Générez, affichez et téléchargez des rapports d’attribution de licence pour plusieurs organisations et produits à partir de Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e3380a89-8529-473f-bd17-efb05466eab9
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Créer des rapports d’attribution de licence pour plusieurs organisations et produits

Découvrez comment les administrateurs globaux peuvent générer et télécharger des rapports de licence détaillés pour plusieurs organisations et produits pour des périodes spécifiques, afin de faciliter le suivi précis de la configuration des licences.

>[!NOTE]
>
>Pour créer, afficher et exporter un rapport d&#39;attribution de licence, connectez-vous à [&#128279;](https://global-admin-console.adobe.com/), puis accédez à **[!UICONTROL Insights]** > **[!UICONTROL Rapports]** > **[!UICONTROL Attribution de licence]**.

## Création d’un rapport

Les rapports d’attribution de licence vous permettent de surveiller de manière proactive le provisionnement des licences et de réduire le suivi manuel. Les administrateurs globaux peuvent créer un rapport d’attribution de licence pour certains produits afin de surveiller les données de configuration des licences logicielles dans tous les services.

1. Accédez à l’onglet **[[!UICONTROL Insights &#x200B;]](https://global-admin-console.adobe.com/insights)** dans le Global Admin Console.
1. Sur la page **[!UICONTROL Attribution de licence]**, sélectionnez **[!UICONTROL Créer un rapport]**.
1. Sélectionnez les organisations et sélectionnez **[!UICONTROL Suivant]**. Vous pouvez sélectionner individuellement chaque organisation ou sélectionner toutes les organisations enfants au sein d’un parent à l’aide du bouton **[!UICONTROL Tout sélectionner]**.

   >[!NOTE]
   >
   >**Savoir pourquoi vous ne pouvez pas sélectionner certaines organisations** :
   >Si une organisation enfant n’a pas de contrat ou a un contrat d’entreprise distinct avec le même produit que celui de l’organisation parent, elle est désactivée de la création d’un rapport d’affectation de licence. Par exemple, si le contrat de l’organisation parent inclut Adobe Acrobat et que l’organisation enfant en fait de même dans le cadre d’un autre contrat, l’affectation du produit est limitée. Par conséquent, il est également limité pour la création de rapports dans le Global Admin Console. [Découvrez comment effectuer le suivi de l’approvisionnement de ces organisations à l’aide de leurs Admin Console respectives](https://helpx.adobe.com/fr/enterprise/using/assignment-reports.html).

   >[!NOTE]
   >
   >Vous ne pouvez créer des rapports d&#39;affectation que pour les organisations ayant un contrat actif.

1. Sélectionnez les produits à inclure dans le rapport, puis sélectionnez **[!UICONTROL Suivant]**.

   >[!NOTE]
   >
   >**Savoir pourquoi vous ne pouvez pas sélectionner certains produits** :
   >Les produits qui ne peuvent pas être affectés dans le Global Admin Console ne sont pas inclus pour la création de rapports. Cela inclut actuellement certains produits d’expérience digitale tels que [!DNL Workfront], [!DNL Adobe Experience Manager] et [!DNL Adobe Experience Platform], ainsi que des produits tels que [!DNL Adobe Firefly Services], [!DNL Acrobat Sign] et [!DNL Adobe Stock]. [Utilisez le Adobe Admin Console pour rechercher les données d’attribution de licence de ces produits](https://helpx.adobe.com/fr/enterprise/using/assignment-reports.html).

1. Choisissez d’agréger le rapport par mois ou par année.
1. Sélectionnez une période personnalisée ou choisissez parmi des options prédéfinies. Vous pouvez sélectionner n’importe quelle date de début, du 18 juin 2020 à la date précédente, à condition qu’elle ne précède pas la date de début de votre contrat.
1. Sélectionnez **[!UICONTROL Télécharger]** pour exporter le rapport au format CSV.

Le rapport commence le traitement et s’affiche sur la page **[!UICONTROL Attribution de licence]** avec des détails tels que le nom, le créateur, l’heure de création, la période et le statut. Une fois prêt, vous recevez une notification par e-mail et le rapport est automatiquement téléchargé.

Tout administrateur global peut télécharger le rapport à tout moment une fois qu’il est prêt, à l’aide de l’icône **[!UICONTROL Télécharger]** située en regard du nom du rapport.

>[!NOTE]
>
>- Pour vous assurer que les dernières données sont prises en compte, générez des rapports 48 heures après toute allocation.
>- Les rapports sont conservés pendant 90 jours après leur génération.

## Affichage et téléchargement des rapports précédemment générés

Les administrateurs globaux peuvent afficher et télécharger les rapports d’attribution de licence générés par tout autre administrateur global de votre organisation. Toutefois, les observateurs globaux ne peuvent afficher que la liste des rapports d’attribution de licence.

1. Accédez à l’onglet **[[!UICONTROL Insights &#x200B;]](https://global-admin-console.adobe.com/insights)** dans le Global Admin Console.
1. Sur la page **[!UICONTROL Attribution de licence]**, tous les rapports sont répertoriés avec les détails suivants :

   | Champ | Description |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | Nom | Généré automatiquement et ne peut pas être modifié. |
   | Créateur | Administrateur global qui a généré le rapport. |
   | Heure de création | Heure système à laquelle le rapport a été créé. |
   | Date range (Plage de dates) | Période sélectionnée pour le rapport. |
   | État | **Réussite** si le rapport est prêt à être téléchargé, ou **Traitement** s’il est toujours en cours de génération. |

1. Pour exporter le rapport au format CSV, cliquez sur l’icône **[!UICONTROL Télécharger]** en regard du rapport.

## Connaître votre rapport d’attribution de licence

Le rapport que vous téléchargez contient les informations suivantes pour chaque événement :

| Champ | Description |
| -------------------------------- | -------------------------------------------------------- |
| ID d’organisation | ID unique lié à l’organisation parent |
| Nom d’organisation | Nom de l’organisation parent |
| ID d’organisation enfant | Identifiant unique de l’organisation enfant sélectionnée |
| Nom de l’organisation enfant | Nom de l’organisation enfant |
| ID de licence | ID unique de la licence de produit |
| Nom du produit | Nom du produit sélectionné |
| Date | Sélection de la date |
| Qté totale de la licence | Nombre total de licences au niveau de l’organisation parent |
| Licences enfants | Nombre de licences allouées à l’organisation enfant |
| Qté attribuée maximale mensuelle/annuelle | Valeur agrégée de la configuration de la licence (mensuelle/annuelle) |
