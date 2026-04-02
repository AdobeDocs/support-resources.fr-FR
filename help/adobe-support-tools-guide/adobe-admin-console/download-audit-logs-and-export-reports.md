---
title: Téléchargement des journaux d’audit et des rapports d’exportation
description: Découvrez comment les administrateurs globaux affichent, filtrent et exportent les journaux d’audit et les rapports dans Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 7211d382c6cfba6070c8c3203956a1193f64ffbe
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 3%

---

# Téléchargement des journaux d’audit et des rapports d’exportation

S’applique à l’entreprise.

Découvrez comment les administrateurs globaux affichent, filtrent et exportent les journaux d’audit et les rapports à l’aide de Global Admin Console.

Pour commencer, connectez-vous à [](https://global-admin-console.adobe.com/). Accédez ensuite à l’onglet **[!UICONTROL Insights]** et sélectionnez **[!UICONTROL Journaux d’audit]** pour suivre toutes les modifications apportées à l’échelle des organisations.

## Affichage et téléchargement des journaux d’audit

En tant qu’administrateur global, vous disposez d’une visibilité complète sur les modifications apportées dans Global Admin Console. Vous pouvez rechercher dans les journaux d’audit de toutes les organisations les actions entreprises au cours des 90 derniers jours, y compris le moment où elles se sont produites et qui les a effectuées.
- Les journaux d’audit permettent d’assurer une conformité continue en vous protégeant contre les accès inappropriés au système et en auditant les comportements suspects au sein de votre entreprise.
- Les journaux disponibles dans Global Admin Console incluent uniquement les événements auxquels un administrateur global peut accéder. Ils n’incluent pas les affectations d’utilisateurs ni les événements utilisateur. [En savoir plus](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) sur les différentes fonctionnalités offertes par chaque console.
- Les journaux couvrent les événements de toutes les organisations de la hiérarchie, ce qui vous permet de rechercher simultanément des journaux d’audit dans toutes les organisations.

>[!NOTE]
>
> En tant qu’administrateur système dans une organisation [](https://adminconsole.adobe.com), vous pouvez utiliser le [ Journal d’audit](https://helpx.adobe.com/enterprise/using/audit-logs.html) pour consulter les affectations d’utilisateurs et les événements utilisateur. Les actions effectuées par les administrateurs système dans les organisations enfants de l’organisation sélectionnée sont également incluses dans les journaux d’audit. Découvrez comment les administrateurs et administratrices système peuvent [suivre les modifications](https://helpx.adobe.com/enterprise/using/audit-logs.html) effectuées dans Admin Console.

Pour afficher ou télécharger les journaux d’audit de votre organisation :

1. En tant qu&#39;administrateur global, connectez-vous à [](https://global-admin-console.adobe.com/insights).
1. Sélectionnez **[!UICONTROL Informations]** > **[!UICONTROL Journaux d’audit]**.

Les journaux d’audit affichent les informations suivantes pour les événements filtrés :

| Champ | Description |
|------ |-------------|
| Date | Date et heure de l’événement, affichées dans le fuseau horaire local. |
| Nom de l’événement | Description de l’action effectuée. |
| Détails de l’événement | Détails supplémentaires sur l’événement, le cas échéant. |
| Nom de l’objet | Nom du produit, profil de produit ou groupe d’utilisateurs impliqué dans l’événement, selon le cas. |
| Utilisateur affecté | Adresse électronique de l’utilisateur concerné, le cas échéant. |
| Administration | Adresse électronique de l’administrateur qui a exécuté l’action. *Système* s’affiche si l’action a été effectuée par un système principal Adobe. |
| Adresse IP | Adresse IP de la machine sur laquelle l’action a été effectuée. Cela reflète généralement l’emplacement physique, mais il peut s’agir d’un serveur proxy ou d’une adresse VPN. |
| Organisation | Nom de l’organisation concernée par l’événement. |

1. Vous pouvez filtrer les journaux d’audit à l’aide des options suivantes :

   - Recherchez par utilisateur ou administrateur affecté.
   - Sélectionnez une ou plusieurs organisations.
   - Définissez une période.
   - Filtrez par nom d’événement.
   - Combinez des filtres pour limiter les résultats, par exemple en affichant les événements des sept derniers jours pour une organisation spécifique.

   ![journaux-d’audit](assets/audit-logs.png)

   *Filtrez les journaux d’audit en fonction du nom de l’événement, de l’organisation affectée ou de la période.*

   ![select-organization](assets/select-organizations.png)

   *Sélectionnez les organisations pour filtrer les journaux d’audit.*

1. Pour exporter les journaux d’audit, sélectionnez **[!UICONTROL Exporter au format CSV]** afin d’exporter les résultats filtrés. Les résultats sont téléchargés au format CSV.

Pour plus d’informations sur les champs inclus dans l’exportation, voir [Schéma du journal](#log-schema).

>[!NOTE]
>
>Les rapports du journal d’audit exportés sont conservés pendant 90 jours après avoir été générés.


## Présentation du rapport du journal d’audit {#log-schema}

Le rapport du journal d’audit exporté comprend les champs suivants pour chaque organisation :

| Champ | Description |
|------|------------|
| identifiant | Identifiant d’événement |
| eventTime | Date et heure de l&#39;événement (fuseau horaire local) |
| eventType | Nom de l’événement |
| eventSubType | Détails supplémentaires sur l’événement, le cas échéant |
| actorEmail | Adresse électronique de l’administrateur qui a exécuté l’événement. *Système* s’affiche si l’événement a été effectué par un système principal Adobe. |
| targetUserEmail | Adresse électronique de l’utilisateur affecté, le cas échéant |
| targetGroupName | Groupe d’utilisateurs affecté, le cas échéant |
| targetProductName | Produit concerné, le cas échéant |
| targetProfileName | Profil de produit affecté, le cas échéant |
| ipAddress | Adresse IP de la machine sur laquelle l’action a été effectuée. Reflète généralement l’emplacement physique, mais il peut s’agir d’un serveur proxy ou d’une adresse VPN. |
| organizationName | Nom de l’organisation concernée |

## Téléchargement de rapports d’exportation

Lorsqu&#39;un administrateur global exporte des données d&#39;organisation à partir de [](https://global-admin-console.adobe.com/insights), le rapport est traité et rendu disponible sous l&#39;onglet **[!UICONTROL Insights]** dans **[!UICONTROL Exporter des rapports]**.

Tous les rapports générés par un administrateur global sont disponibles au même endroit. La fonctionnalité de rapports d’exportation est utile dans les scénarios suivants :

- Si vous disposez d’une hiérarchie volumineuse avec de nombreuses organisations, il n’est plus nécessaire d’attendre que le fichier d’exportation soit traité. Vous pouvez utiliser les rapports générés par vos collègues administrateurs.
- Vous n’avez plus besoin de conserver ou d’enregistrer ces rapports pour les comparer ultérieurement. Les rapports sont conservés pendant 90 jours et vous pouvez les télécharger à tout moment pour les comparer.


Pour télécharger un rapport d’exportation :

1. Connectez-vous à [](https://global-admin-console.adobe.com/insights) et accédez à **[!UICONTROL Insights]** > **[!UICONTROL Exporter des rapports]**.

   Les rapports générés au cours des 90 derniers jours s’affichent. Au bout de 90 jours, vous pouvez générer à nouveau le rapport. Découvrez comment générer des rapports pour la [structure de l’organisation](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-the-organization-structure).


   | Champ | Description |
   |------|------------|
   | Rapport | Date et heure de génération du rapport (fuseau horaire local) |
   | Format | Format du fichier (CSV, JSON, XLSX) |
   | Taille | Taille du fichier |
   | Créée par | Adresse électronique de l’administrateur qui a généré le rapport |
   | Action | Lien pour télécharger le rapport |

1. Pour télécharger un rapport, sélectionnez **[!UICONTROL Télécharger]**.

   Si le rapport que vous venez de générer n’apparaît pas dans la liste, sélectionnez **[!UICONTROL Actualiser]**.

   ![export-reports](assets/export-reports.png)

*Téléchargez tout rapport généré au cours des 90 derniers jours.*
