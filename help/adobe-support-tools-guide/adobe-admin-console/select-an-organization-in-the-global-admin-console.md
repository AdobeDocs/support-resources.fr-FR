---
title: Sélectionner une organisation dans le Global Admin Console
description: Découvrez comment choisir une organisation à modifier dans le Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 2%

---

# Sélectionner une organisation dans le Global Admin Console

Découvrez comment choisir une organisation à modifier dans le Global Admin Console.

>[!NOTE]
>
>Après avoir accédé au [&#128279;](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), vous pouvez commencer par sélectionner une organisation pour afficher et gérer le nom de l&#39;organisation, les groupes d&#39;utilisateurs, les profils de produit, les administrateurs et les politiques d&#39;organisation. Pour vous connecter au Global Admin Console, [cliquez ici](https://global-admin-console.adobe.com/).

Global Admin Console fait office de hub de gestion central pour les ressources Adobe au sein d’une organisation. Les administrateurs globaux peuvent :

- Créer des organisations enfants sous leur organisation
- Affectez des administrateurs système pour les gérer.
- Distribuer des ressources aux organisations enfants pour la gestion et l&#39;affectation aux utilisateurs de ces organisations

>[!NOTE]
>
> Les utilisateurs et les administrateurs d’une organisation n’ont pas de visibilité sur les utilisateurs, le stockage ou d’autres ressources en dehors de leur organisation.

## Sélectionnez votre organisation

Les organisations répertoriées dans la liste déroulante **[!UICONTROL sélecteur d’organisation]** sont celles pour lesquelles vous êtes explicitement administrateur global, c’est-à-dire celles pour lesquelles vous avez été ajouté à la liste des administrateurs de cette organisation avec un rôle d’administrateur global ou de visionneuse globale. Vous êtes implicitement un administrateur global (ou un observateur global) de toutes les organisations situées sous ce point de la hiérarchie, mais ces organisations ne sont pas répertoriées dans le [!UICONTROL sélecteur d’organisation].

![Sélecteur d’organisation](/help/adobe-support-tools-guide/assets/org-picker.png)

Si vous souhaitez qu’ils soient répertoriés, ajoutez-vous en tant qu’administrateur global pour les organisations que vous souhaitez inscrire. Lorsque vous sélectionnez une organisation dans le [!UICONTROL sélecteur d’organisations], vos autorisations administratives reposent sur le statut d’administrateur global de l’organisation sélectionnée. Vous pouvez également être répertorié en tant qu’administrateur global d’une organisation parente plus haut dans l’arborescence, ce qui pourrait vous donner plus d’autorisations. Vous devez sélectionner cette organisation de niveau supérieur pour obtenir les autorisations supplémentaires.

Dans Global Admin Console, après avoir sélectionné une organisation dans l’arborescence [!UICONTROL hiérarchie], vous pouvez commencer à modifier les informations d’une organisation particulière.

**Les modifications peuvent affecter :**

- Nom de l’organisation
- Groupes d’utilisateurs
- Profils de produit
- Administrateurs
- Politiques d’organisation

**Les modifications ne peuvent pas affecter :**

- Utilisateurs (à l’exception de la suppression de groupes ou de profils de produits)
- Ajout d’utilisateurs (sauf pour les administrateurs)

Lorsqu’une organisation est sélectionnée dans l’arborescence, les informations suivantes s’affichent :

- Nom de l’organisation
- Région
- Nombre d’utilisateurs
- Liste des produits
- Profils de produit
- Groupes d’utilisateurs
- Administrateurs
- Domaines revendiqués
- Valeurs de la politique de l’organisation

Pour afficher ou modifier des produits, des groupes d’utilisateurs, des administrateurs, des domaines, des politiques ou des modèles de politique, sélectionnez l’onglet approprié. Dans la plupart des cas, vous pouvez utiliser le champ [!UICONTROL recherche] pour localiser un élément spécifique dans l’onglet.

![Modifier une organisation](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

Tous les administrateurs ajoutés ou supprimés d’une organisation reçoivent une notification par e-mail. Certaines modifications de politique apportées à une organisation entraînent une notification dans le [!DNL Admin Console] de cette organisation.

## En savoir plus sur les contraintes et conditions nécessaires

- La profondeur maximale pour l’imbrication des organisations est de cinq. Ainsi, a/b/c/d/e est autorisé, mais a/b/c/d/e/f est une erreur. Par exemple, Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London est autorisé, mais Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair est une erreur.

- La longueur maximale du nom de chemin (y compris toutes les organisations) est de 255 caractères (y compris « / »). La longueur maximale d’un nom d’organisation unique est comprise entre 4 et 100 caractères.

- Le chemin d’accès de l’organisation est unique, mais le nom simple n’est unique que parmi ses frères. Il se peut qu’il existe des organisations portant le même nom simple ailleurs dans la hiérarchie d’organisation.

- Vous pouvez uniquement afficher la liste des domaines liés à l’organisation sélectionnée à l’aide de la console d’administration globale. Si vous êtes un administrateur système de l’organisation sélectionnée, sélectionnez l’option **[!UICONTROL Ouvrir dans Admin Console]** pour [gérer les domaines](https://helpx.adobe.com/fr/enterprise/using/manage-domains-directories.html). Pour comprendre les informations affichées dans l’onglet Domaines , consultez [exportation et importation de schémas](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas).

- IE 11 n’est pas pris en charge pour l’accès à l’administration globale. Utilisez un autre navigateur ou une version plus récente du navigateur IE.
