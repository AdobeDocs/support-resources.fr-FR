---
title: Gérer les administrateurs
description: Comment les clients Adobe peuvent-ils configurer et gérer des administrateurs dans Global Admin Console pour contrôler l’accès des utilisateurs, les licences de produits et les ressources d’organisation ?
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 7e5c601a5edd2558d16bfb7b2d508bcf8f976f51
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Gérer les administrateurs

*S’applique à l’entreprise.*

Explorez les fonctionnalités d’administration globale et apprenez à déléguer et à distribuer l’administration des utilisateurs, des licences de produit et des groupes aux administrateurs pour chaque organisation individuelle.

Dans le Global Admin Console, vous pouvez sélectionner une organisation et accéder à l’onglet **[!UICONTROL Administrateurs]** pour ajouter, modifier ou supprimer des droits d’administrateur. Pour en savoir plus, consultez la section [Adopter l’administration globale](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html). Accédez à [Global Admin Console](https://global-admin-console.adobe.com/) pour vous connecter.


Le Global Admin Console introduit un rôle appelé « administrateur global ». Ce rôle est distinct de celui d’un administrateur système et vous permet d’effectuer les opérations suivantes :

- Affichez le panorama mondial de votre investissement Adobe total sur toutes les Admin Consoles ajoutées à la hiérarchie de Global Admin Console.
- Surveillez les affectations et l’utilisation des licences et des ressources Adobe sur plusieurs Admin Console.
- Créez des Admin Consoles ou des organisations.
- Attribuez des licences de produit d’une Admin Console racine ou parente à des Admin Console enfants situées sous dans la hiérarchie.
- Gérer les opérations quotidiennes pendant que les administrateurs système continuent à gérer leurs propres Admin Console. Par exemple, un administrateur global peut attribuer un produit à un enfant Admin Console, mais ne peut pas l’affecter aux utilisateurs. L’administrateur système recevra les places au sein de son Admin Console et attribuera les produits à ses utilisateurs.
- Vous pouvez éventuellement appliquer des politiques d’organisation à l’une des Admin Console de la hiérarchie.

## Tâches administratives fondamentales

Global Admin Console est conçu pour fonctionner sur plusieurs organisations et Admin Consoles. Le tableau suivant décrit les différentes fonctionnalités et l’emplacement où elles peuvent être exécutées (Admin Console ou Global Admin Console).

<table>
  <tr>
    <th colspan="2">Tâche</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">Créer, représenter et supprimer des organisations enfants</td>
    <td align="center">Oui</td>
    <td align="center">Non</td>
  </tr>

<tr>
    <td colspan="2">Utilisation de plusieurs organisations</td>
    <td align="center">Oui</td>
    <td align="center">Non</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">Gérer les administrateurs</td>
    <td>Pour une ou plusieurs organisations</td>
    <td align="center">Oui</td>
    <td align="center">Non</td>
  </tr>

<tr>
    <td>Pour une organisation</td>
    <td align="center">Oui</td>
    <td align="center">Oui</td>
  </tr>

<tr>
    <td colspan="2">Gestion des profils de produit et des groupes d’utilisateurs</td>
    <td align="center">Oui</td>
    <td align="center">Oui</td>
  </tr>

<tr>
    <td colspan="2">Définir et gérer des politiques</td>
    <td align="center">Oui</td>
    <td align="center">Non</td>
  </tr>

<tr>
    <td colspan="2">Allouer des produits à l’ensemble des organisations</td>
    <td align="center">Oui</td>
    <td align="center">Non</td>
  </tr>

<tr>
    <td colspan="2">Attribuer des produits aux utilisateurs</td>
    <td align="center">Non</td>
    <td align="center">Oui</td>
  </tr>

<tr>
    <td colspan="2">Gérer les utilisateurs et les utilisatrices</td>
    <td align="center">Non</td>
    <td align="center">Oui</td>
  </tr>

<tr>
    <td colspan="2">Gestion des packages</td>
    <td align="center">Non</td>
    <td align="center">Oui</td>
  </tr>

<tr>
    <td colspan="2">Configurer des domaines et des répertoires</td>
    <td align="center">Non</td>
    <td align="center">Oui</td>
  </tr>

<tr>
    <td colspan="2">Gestion du stockage et du chiffrement de l’entreprise</td>
    <td align="center">Non</td>
    <td align="center">Oui</td>
  </tr>
</table>

## Gérer les administrateurs

Vous pouvez créer une hiérarchie administrative flexible qui permet une gestion affinée de l’accès et de l’utilisation des produits Adobe. Tout comme le Adobe Admin Console, le Global Admin Console vous permet d’ajouter des administrateurs système, des administrateurs de produit, des administrateurs de profil de produit, des administrateurs de groupe d’utilisateurs, des administrateurs de déploiement, des administrateurs d’assistance et des administrateurs de stockage. Ces administrateurs peuvent effectuer leurs tâches administratives respectives dans les organisations dont ils sont administrateurs. Outre ces rôles, il existe deux nouveaux rôles pour l’administration globale : administrateur global et observateur global.

L’administrateur global est un rôle transitif. Le fait de faire d’un utilisateur l’administrateur global d’une organisation fait automatiquement de cet utilisateur l’administrateur global de tous les enfants de cette organisation, directement ou indirectement. En outre, si une nouvelle organisation est créée dans la hiérarchie des organisations, tous les administrateurs globaux des parents de cette organisation deviennent immédiatement des administrateurs globaux de l’organisation nouvellement créée.

Voici les fonctionnalités du rôle d’administrateur global :

- Créer et supprimer des organisations enfants
- Définition et modification de politiques
- Définition et modification des rôles d’administration
- Ajouter et supprimer des produits dans les organisations enfants
- Définir ou modifier les allocations de ressources pour les organisations enfants
- Gestion des profils de produit et des groupes d’utilisateurs

Voici les fonctionnalités du rôle Observateur global :

- Affichez la liste des groupes d’utilisateurs, des produits, des profils de produit, des administrateurs, des jeux de politiques et des ressources de l’organisation et des organisations enfants.

## Administration distribuée

En gérant les administrateurs, un administrateur global peut déléguer et distribuer l’administration des utilisateurs, des licences de produit et des groupes aux administrateurs pour chaque organisation individuelle. L’administrateur ajouté à une organisation par un administrateur global peut gérer l’organisation sans avoir de visibilité sur l’administration des autres organisations. Ainsi, l’administrateur global peut déléguer l’administration des ressources et des utilisateurs en maintenant les données de ces ressources et utilisateurs isolées.

Un administrateur global peut créer des organisations, distribuer des ressources telles que des produits et du stockage à ces organisations, gérer la configuration des identités, et créer et appliquer des modèles de politiques d’organisation. Un administrateur système ajouté à une organisation par un administrateur global peut affecter des produits aux utilisateurs, intégrer des utilisateurs, créer et gérer des profils de produit et effectuer d’autres tâches administratives au sein de cette organisation.

## Ajouter un administrateur

1. Dans le [Global Admin Console](https://global-admin-console.adobe.com/), sélectionnez une organisation à modifier, puis accédez à l’onglet **[!UICONTROL Admins]**.

1. Sélectionnez **[!UICONTROL Ajouter un administrateur]**.

   ![ajout d’un administrateur à la console d’administration globale](../assets/global-admin-console-add-admin.png)

1. Dans la boîte de dialogue **[!UICONTROL Ajouter un administrateur]**, saisissez les **[!UICONTROL Détails de l’utilisateur]** : e-mail, prénom, nom, type de compte et code de pays.

   Si vous essayez d’ajouter un utilisateur existant en tant qu’administrateur, choisissez le même type de compte que l’utilisateur existant, sinon l’opération d’ajout échouera.

   > [ !NRemarque]
   > 
   > Les organisations peuvent avoir des restrictions sur les types de compte qui peuvent être ajoutés. Ils peuvent être basés sur des [politiques](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) ou sur d’autres paramètres de configuration d’une organisation. Les entreprises ne permettent pas d’ajouter simultanément des utilisateurs Adobe ID et Business ID . En règle générale, il ne doit pas y avoir d’utilisateurs des deux types dans une organisation, mais selon l’ordre dans lequel les règles sont définies, certains utilisateurs d’un type de compte particulier peuvent être antérieurs à l’application des politiques ou des règles.

1. Sélectionnez un ou plusieurs rôles d’administrateur dans la section **[!UICONTROL Droits d’administrateur]**.

   Pour des rôles tels que l’administrateur de produit, l’administrateur de profils de produit et l’administrateur de groupes d’utilisateurs, sélectionnez les produits, profils et groupes spécifiques, respectivement.

   ![ajout d’un administrateur à la console d’administration globale](../assets/global-admin-console-add-admin-detail.png)

1. Sélectionnez **[!UICONTROL Enregistrer]**.

1. Après avoir modifié les organisations, sélectionnez **[!UICONTROL Vérifier les modifications en attente]**, puis sélectionnez **[!UICONTROL Envoyer les modifications]** pour [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) les modifications.

Lorsqu’un rôle d’administrateur est ajouté, l’utilisateur reçoit une notification par e-mail l’informant du changement de son rôle.

Une fois l’administrateur ajouté, il reçoit un e-mail l’invitant à accepter son rôle et lui donnant un lien vers l’Admin Console. S’ils sont ajoutés en tant qu’administrateurs globaux et en tant qu’autres rôles, ils recevront deux invitations, l’une à l’Admin Console globale et l’autre à l’Admin Console.

## Modifier un administrateur

1. Sélectionnez une organisation à modifier et accédez à l’onglet **[!UICONTROL Administrateurs]**.

1. Sélectionnez l’icône **[!UICONTROL Plus d’options]** (⋮) de l’administrateur approprié, puis sélectionnez **[!UICONTROL Modifier l’administrateur]**.

   ![droits d’administration de modification de global admin console](../assets/global-admin-console-edit-admin-right.png)

1. Mettez à jour les détails de l’administrateur, puis sélectionnez **[!UICONTROL Enregistrer]**.

1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée.

Une commande distincte apparaît dans la liste des modifications en attente pour chaque rôle d’administrateur ajouté ou supprimé. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Supprimer les droits d’administrateur

1. Sélectionnez une organisation à modifier et accédez à l’onglet **[!UICONTROL Administrateurs]**.

1. Sélectionnez l’icône **[!UICONTROL Plus d’options]** (⋮) de l’administrateur approprié, puis sélectionnez **[!UICONTROL Supprimer les droits d’administrateur]**.

   ![global admin console supprime les droits d’administrateur](../assets/global-admin-console-remove-admin-right.png)

1. Sélectionnez **[!UICONTROL OK]** dans la boîte de dialogue de confirmation.

1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Après la suppression d’un administrateur, l’utilisateur ou l’utilisatrice reçoit une notification par e-mail l’informant de la perte d’accès à Admin Console de cette organisation.

