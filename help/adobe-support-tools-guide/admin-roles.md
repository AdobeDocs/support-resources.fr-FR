---
title: Rôles administratifs
description: Grâce à Adobe Admin Console, les entreprises peuvent définir une hiérarchie administrative flexible qui permet une gestion affinée de l’accès et de l’utilisation des produits Adobe.
source-git-commit: 13e89a152d9387a8b23544e6b6c6e3cad5856666
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 1%

---

# Rôles administratifs

Grâce à Adobe Admin Console, les entreprises peuvent définir une hiérarchie administrative flexible qui permet une gestion affinée de l’accès et de l’utilisation des produits Adobe. Un ou plusieurs administrateurs système, configurés lors du processus d’intégration de l’entreprise, se trouvent en haut de la hiérarchie. Ces administrateurs système peuvent déléguer des responsabilités à d’autres administrateurs, tout en conservant le contrôle global.

Les rôles administratifs offrent les principaux avantages suivants aux entreprises :

* Décentralisation contrôlée des responsabilités administratives
* Aperçu rapide des affectations de produits, par utilisateur et par produit
* Fonctionnalité d’attribution de quotas aux administrateurs de produit

## Hiérarchie administrative

Application : clients Adobe Grands comptes.

La hiérarchie administrative peut être utilisée pour répondre aux besoins uniques de votre entreprise. Par exemple, une entreprise peut nommer différents administrateurs pour gérer les droits aux offres Adobe Creative Cloud et Adobe Marketing Cloud. Une entreprise peut également disposer de différents administrateurs pour gérer les droits des utilisateurs appartenant à différentes unités commerciales.

>[!NOTE]
>
>La hiérarchie administrative ne s’applique pas aux équipes et aux clients. Les clients Teams disposent d’un rôle **Administrateur système** unique. Le propriétaire du contrat (_précédemment appelé&#x200B;**administrateur de Principal**_) est l&#39;administrateur système qui a accès aux détails du contrat et à l&#39;historique de facturation. Si vous êtes le propriétaire actuel du contrat, vous pouvez nommer un administrateur système existant (_ précédemment appelé **administrateur secondaire**_) comme propriétaire du contrat.

![image admin](assets/storage_admin.png)

_Hiérarchie des rôles d’administrateur_

| Rôle | Description |
|--- |--- |
| **Administrateur système** | Super utilisateur ou utilisatrice de l’organisation ; autorisé à effectuer toutes les tâches administratives dans Admin Console.<br>Dispose également des autorisations pour déléguer les fonctionnalités administratives suivantes à d’autres utilisateurs : administrateur de produit, administrateur de profil de produit, administrateur de groupe d’utilisateurs, administrateur de déploiement et administrateur d’assistance. |
| **Administrateur de produit** | Administre les produits affectés à cet administrateur et toutes les fonctions administratives associées, qui incluent :<ul><li>Création de profils de produit</li><li>Ajoutez des utilisateurs et des groupes d’utilisateurs à l’organisation, mais ne les supprimez pas</li><li>Ajouter ou supprimer des utilisateurs et des groupes d’utilisateurs des profils de produit</li><li>Ajouter ou supprimer des administrateurs de profil de produit des profils de produit</li><li>Ajouter ou supprimer d’autres administrateurs de produit du produit</li><li>Ajout ou suppression d’administrateurs de groupe dans des groupes</li></ul> |
| **Administrateur de profil de produit** | Gère les descriptions du profil de produit attribuées à cet administrateur et toutes les fonctions administratives associées, notamment :<ul><li>Ajoutez des utilisateurs et des groupes d’utilisateurs à l’organisation, mais ne les supprimez pas</li><li>Ajouter ou supprimer des utilisateurs et des groupes d’utilisateurs des profils de produit</li><li>Attribuer ou révoquer des autorisations de produit aux utilisateurs et aux groupes d’utilisateurs à partir des profils de produit</li><li>Gérer les rôles de produit des utilisateurs et des groupes d’utilisateurs pour les profils de produit |
| **Administrateur de groupe d’utilisateurs** | Administre les descriptions des groupes d’utilisateurs affectées à cet administrateur et toutes les fonctions administratives associées, qui comprennent :<ul><li>Ajout ou suppression d’utilisateurs à des groupes</li><li>Ajouter ou supprimer des administrateurs de groupe d’utilisateurs des groupes |
| **Administrateur de déploiement** | Crée, gère et déploie des packages logiciels et des mises à jour pour les utilisateurs finaux. |
| **Administrateur de l’assistance** | Rôle non administratif qui a accès à des informations relatives à l’assistance, telles que les rapports de problèmes signalés par les clients et les clientes. |
| **Administrateur de stockage** | Gère l’administration du stockage de l’organisation. L’administrateur peut afficher la consommation de stockage des utilisateurs actifs et inactifs et transférer le contenu à d’autres destinataires. |

Pour obtenir la liste détaillée des autorisations et des privilèges associés à chaque rôle d’administrateur, voir [Autorisations](#enterprise-admins-permissions-matrix).

## Ajouter un rôle d’administrateur d’entreprise {#add-enterprise-role}

Application : clients Adobe Grands comptes.

En tant qu’administrateur, vous pouvez attribuer un rôle d’administrateur à d’autres utilisateurs en leur donnant les mêmes privilèges que vous possédez ou des privilèges pour un rôle sous votre rôle d’administrateur dans la hiérarchie, comme décrit [ci-dessus](#administrative-hierarchy). Par exemple, en tant qu’administrateur de produit, vous pouvez accorder des privilèges d’administrateur de produit ou des privilèges d’administrateur de profil de produit à un utilisateur, mais pas des privilèges d’administrateur de déploiement. Pour connaître les autorisations relatives à Admin Console, consultez la [matrice des autorisations](#enterprise-admins-permissions-matrix).

Pour ajouter ou inviter un administrateur :

1. Dans **[!UICONTROL Adobe Admin Console](https://adminconsole.adobe.com/)**, choisissez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Administrateurs]**.

   Vous pouvez également accéder au produit, au profil de produit ou au groupe d’utilisateurs approprié et accéder à l’onglet **[!UICONTROL Administrateurs]**.

1. Cliquez sur **[!UICONTROL Ajouter un administrateur]**.
1. Saisissez un nom ou une adresse e-mail. Vous pouvez rechercher des utilisateurs existants ou ajouter un nouvel utilisateur en spécifiant une adresse e-mail valide et en renseignant les informations à l’écran.
1. Cliquez sur **[!UICONTROL Suivant]**. Une liste des rôles d’administrateur s’affiche.

   >[!NOTE]
   >
   >* Les options de cet écran dépendent de votre compte et de votre rôle d’administrateur. Vous pouvez soit accorder les mêmes privilèges que vous, soit accorder des privilèges pour un rôle sous le vôtre dans la hiérarchie.
   >* En tant qu’administrateur système d’une équipe, vous ne pouvez affecter qu’un seul rôle d’administrateur : Administrateur système.

1. Sélectionnez un ou plusieurs rôles d’administrateur.
1. Pour les types d’administrateur tels que Administrateur de produit, Administrateur de profil de produit et Administrateur de groupe d’utilisateurs, sélectionnez respectivement les produits, profils et groupes spécifiques.

   >[!NOTE]
   >
   >Pour un administrateur de profils de produit, vous pouvez inclure des profils pour plusieurs produits.

   ![ajouter un administrateur](assets/add-admin.png)

1. Vérifiez les rôles d’administrateur attribués à l’utilisateur et cliquez sur **Enregistrer**.

L’utilisateur reçoit une invitation par e-mail concernant les nouveaux privilèges d’administration de `message@adobe.com`.

Les utilisateurs doivent cliquer sur **[!UICONTROL Commencer]** dans l’e-mail pour rejoindre l’organisation. Si les nouveaux administrateurs n’utilisent pas le lien **[!UICONTROL Commencer]** dans l’invitation par e-mail, ils ne pourront pas se connecter à Admin Console.

Dans le cadre du processus de connexion, les utilisateurs peuvent être invités à configurer un profil Adobe s’ils n’en ont pas déjà un. Si plusieurs profils sont associés à leur adresse e-mail, les utilisateurs doivent choisir « Rejoindre l’équipe » (si cela vous est demandé), puis sélectionner le profil associé à la nouvelle organisation.

![image des droits d’administration](assets/admin-get-started-email.png)

## Ajouter un administrateur d’équipes {#add-admin-teams}

Application : clients des équipes Adobe.

En tant qu’administrateur, vous pouvez attribuer le rôle d’administrateur système à d’autres utilisateurs, leur donnant ainsi les mêmes privilèges que vous.

Pour ajouter ou inviter un administrateur système :

1. Dans **[!UICONTROL Adobe Admin Console]**, choisissez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Administrateurs]**.

   Une liste des administrateurs existants s’affiche.

1. Cliquez sur **[!UICONTROL Ajouter un administrateur]**.

   L’écran **[!UICONTROL Ajouter un administrateur]** s’affiche.

1. Saisissez un nom ou une adresse e-mail. Vous pouvez rechercher des utilisateurs existants ou ajouter un nouvel utilisateur en spécifiant une adresse e-mail valide et en renseignant les informations à l’écran.

   Par défaut, Administrateur système est sélectionné.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

![image d’administration d’équipes](assets/teams-admin.png)

Comme tous les utilisateurs d’une organisation en équipes sont des utilisateurs Business ID, ils reçoivent une invitation par e-mail concernant les nouveaux privilèges d’administration de `message@adobe.com`.
Les utilisateurs doivent cliquer sur Commencer dans l’e-mail pour rejoindre l’organisation.

Dans le cadre du processus de connexion, les utilisateurs peuvent être invités à configurer un profil Adobe s’ils n’en ont pas déjà un. Si plusieurs profils sont associés à leur adresse e-mail, les utilisateurs doivent choisir « Rejoindre l’équipe » (si cela vous est demandé), puis sélectionner le profil associé à la nouvelle organisation.

![image des droits d’administration](assets/admin-get-started-email.png)

## Modifier le rôle d’administrateur d’entreprise

Application : clients Adobe Grands comptes.

En tant qu’administrateur, vous pouvez modifier le rôle d’administrateur pour d’autres administrateurs qui se trouvent sous vous dans la hiérarchie administrative. Par exemple, vous pouvez supprimer les privilèges d’administration d’autres administrateurs.

Pour modifier des rôles d’administrateur :

1. Dans **[!UICONTROL Adobe Admin Console]**, choisissez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Administrateurs]**. La liste des administrateurs existants s’affiche.

   Vous pouvez également accéder au produit, au profil de produit ou au groupe d’utilisateurs approprié et accéder à l’onglet **[!UICONTROL Administrateurs]**.

1. Cliquez sur le nom de l’administrateur à modifier.
1. Dans le **[!UICONTROL Détails de l’utilisateur]**, cliquez sur ![icône](assets/one-console-ellipses.png) dans la section **Droits d’administration** et sélectionnez **[!UICONTROL Modifier les droits d’administration]**.

   ![modifier droits d’administration](assets/admin-rights-section.png)

1. Modifiez les droits d’administration et enregistrez vos modifications.

## Modifier le rôle d’administrateur d’équipes

Application : clients des équipes Adobe.

En tant qu’administrateur système d’équipes, vous pouvez supprimer les privilèges d’administrateur système des autres administrateurs.

Pour révoquer les privilèges d’administrateur système :

1. Dans **[!UICONTROL Adobe Admin Console]**, choisissez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Administrateurs]**.

   La liste des administrateurs existants s’affiche.

1. Dans le **[!UICONTROL Détails de l’utilisateur]**, cliquez sur ![icône](assets/one-console-ellipses.png) à droite de la section **[!UICONTROL Droits d’administration]** et choisissez **[!UICONTROL Modifier les droits d’administration]**.

   ![modifier droits d’administration](assets/admin-rights-section.png)

1. Modifiez les droits d’administration et enregistrez vos modifications.

## Supprimer un administrateur

Application : clients Grands comptes des équipes Adobe.

Pour révoquer les autorisations d’administrateur, sélectionnez un utilisateur, puis cliquez sur **[!UICONTROL Supprimer l’administrateur]**.

![supprimer l’image d’administrateur](assets/remove-admin.png)

>[!NOTE]
>
>La suppression d’un administrateur ne supprime pas l’utilisateur d’Admin Console, mais supprime uniquement les privilèges associés au rôle d’administrateur.

## Matrice des autorisations des administrateurs d’entreprise

Application : clients Adobe Grands comptes.

Le tableau suivant répertorie toutes les autorisations pour les différents types d’administrateurs, classés selon les domaines de fonctionnalité suivants :

### Identity Management

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Ajouter un domaine (demander/demander un domaine) | ✔ | |
| Affichage de la liste des domaines et des domaines | ✔ | |
| Gestion des clés de chiffrement de domaine | ✔ | |
| Gestion de la politique de mot de passe par défaut de l’organisation | ✔ | |
| Afficher la politique de mot de passe d’organisation par défaut | ✔ | |

### Gestion des utilisateurs et utilisatrices

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Ajouter un utilisateur à l’organisation | ✔ | |
| Supprimer un utilisateur de l’organisation | ✔ | |
| Affichage des détails de l’utilisateur et de la liste | ✔ | |
| Modifier le profil utilisateur | ✔ | |
| Ajouter un profil de produit à un utilisateur ou à un groupe | ✔ | |
| Supprimer le profil de produit d’un utilisateur ou d’un groupe | ✔ | |
| Ajouter un profil de produit à plusieurs utilisateurs | ✔ | |
| Affichage des profils de produit pour un utilisateur | ✔ | |
| Afficher la liste des utilisateurs de produits | ✔ | |
| Ajout en bloc d’utilisateurs à l’organisation | ✔ | |

### Gestion des administrateurs

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Octroi du statut d’administrateur d’organisation à un utilisateur | ✔ | |
| Révoquer l’administrateur d’organisation d’un utilisateur | ✔ | |
| Octroyer une licence de produit à un utilisateur | ✔ | |
| Révoquer l’administrateur de licences de produit d’un utilisateur | ✔ | |
| Octroyer le statut d’administrateur de déploiement à un utilisateur | ✔ | |
| Révoquer l’administrateur de déploiement d’un utilisateur | ✔ | |
| Octroi du statut d’administrateur de groupe d’utilisateurs à un utilisateur | ✔ | |
| Révoquer l’administrateur de groupe d’utilisateurs d’un utilisateur | ✔ | |
| Octroyer l’administration du propriétaire du produit à un utilisateur | ✔ | |
| Révoquer l’administrateur du propriétaire du produit d’un utilisateur | ✔ | |

### Gestion de la configuration des licences de produit

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Accorder le droit au produit à l’organisation | | |
| Supprimer les droits de produit de l’organisation | | |
| Afficher le nombre total de licences détenues par l’organisation | ✔ | |
| Afficher les produits et les familles de produits disponibles | ✔ | |
| Modifier les descriptions/données de licence de produit | ✔ | |
| Configurer la licence de produit pour un utilisateur | ✔ | |
| Retirer la licence de produit d’un utilisateur | ✔ | |
| Ajouter une nouvelle configuration de licence de produit | ✔ | |
| Modifier la configuration du service de licence de produit | ✔ | |
| Supprimer la configuration du service de licence de produit | ✔ | |
| Supprimer l’accès au produit d’un utilisateur (supprimer de toutes les configurations) | ✔ | |

### Gestion du stockage

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Affichage des dossiers d’utilisateurs actifs et inactifs | ✔ | |
| Suppression des dossiers d’utilisateurs inactifs et transfert de contenu | ✔ | |

### Déploiement

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Onglet Afficher/utiliser des packages | ✔ | |

### Support technique

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Afficher l’onglet d’assistance | ✔ | |
| Gestion des cas d’assistance | ✔ | ✔ |

### Gestion des groupes d’utilisateurs

| Autorisation | Administrateur système | Administrateur du support technique |
|--- |--- |--- |
| Créer un groupe d’utilisateurs | ✔ | |
| Supprimer un groupe d’utilisateurs | ✔ | |
| Ajouter un utilisateur à un groupe d’utilisateurs | ✔ | |
| Supprimer un utilisateur du groupe d’utilisateurs | ✔ | |
| Affecter un groupe d’utilisateurs à une licence de produit | ✔ | |
| Supprimer un groupe d’utilisateurs de la licence de produit | ✔ | |
| Afficher le membre du groupe d’utilisateurs | ✔ | ✔ |
| Afficher la liste des groupes d’utilisateurs | ✔ | ✔ |