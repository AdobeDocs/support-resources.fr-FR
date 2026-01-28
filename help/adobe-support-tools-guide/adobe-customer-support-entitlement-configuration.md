---
title: Configuration des droits du service clientèle d’Adobe
description: Comment les clients Adobe peuvent-ils configurer les droits d’assistance pour activer la soumission de cas ?
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 009be3353a4bd690a7cf395e7e95540808058b39
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Droits du service clientèle Adobe

Pour configurer les droits d’assistance pour votre organisation, ajoutez ou invitez d’abord l’utilisateur par le biais d’Admin Console.

## Ajout de rôles de droits d’assistance à une organisation

Le rôle d’administrateur de l’assistance est un rôle non administratif qui a accès aux informations relatives à l’assistance. Les administrateurs de l’assistance peuvent afficher, créer et gérer des rapports d’événement.

Pour ajouter ou inviter un administrateur :

1. Dans Admin Console, choisissez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Administrateurs]**.
1. Cliquez sur **[!UICONTROL Ajouter un administrateur]**.
1. Saisissez un nom ou une adresse e-mail.

   Vous pouvez rechercher des utilisateurs existants ou ajouter un nouvel utilisateur en spécifiant une adresse e-mail valide et en renseignant les informations à l’écran.

   ![Ajouter un administrateur](assets/admin-console-add-admin.png)

1. Cliquez sur **[!UICONTROL Suivant]**. Une liste des rôles d’administrateur s’affiche.

Pour attribuer un rôle d’administrateur de l’assistance à un utilisateur (permettre à un utilisateur de contacter l’assistance) :

1. Sélectionnez l’option **[!UICONTROL Assistance de l’administrateur]**.

   ![Modifier droits d’administrateur](assets/edit-admin-rights.png)

1. Sélectionnez l’une des deux options suivantes :

   * Option 1 : **[!UICONTROL administrateur de l’assistance de base]**. Sélectionnez cette option si vous souhaitez donner à l’utilisateur ou à l’utilisatrice l’accès au support pour toutes les solutions (à l’exception de Marketo Engage).
   * Option 2 : **[!UICONTROL administrateur de l’assistance produit]** : sélectionnez cette option pour la prise en charge de Marketo Engage. Sélectionnez les instances Marketo Engage auxquelles accorder l’accès au support technique de l’utilisateur.

   ![Modifier Marketo des droits d’administration](assets/edit-admin-rights-advanced.png)

1. Une fois les sélections effectuées, cliquez sur **[!UICONTROL Enregistrer]**.

L’utilisateur reçoit une invitation par e-mail concernant les nouveaux privilèges d’administration de `message@adobe.com`.

Les utilisateurs doivent cliquer sur **[!UICONTROL Commencer]** dans l’e-mail pour rejoindre l’organisation. Si les nouveaux administrateurs n’utilisent pas le lien **[!UICONTROL Commencer]** dans l’invitation par e-mail, ils ne pourront pas se connecter à Admin Console.

Dans le cadre du processus de connexion, les utilisateurs peuvent être invités à configurer un profil Adobe s’ils n’en ont pas déjà un. Si plusieurs profils sont associés à leur adresse e-mail, les utilisateurs doivent choisir **[!UICONTROL Rejoindre l’équipe]** (si vous y êtes invité), puis sélectionner le profil associé à la nouvelle organisation.

![Confirmation des droits d’administrateur](assets/admin-rights-confirmation.png)

Pour plus d’informations, reportez-vous aux instructions [modifier le rôle d’administrateur d’entreprise](admin-roles.md#add-enterprise-role) dans la documentation sur les rôles d’administration. Notez que seul un administrateur système pour votre organisation peut attribuer ce rôle. Pour plus d’informations sur la hiérarchie administrative, consultez la documentation [rôles administratifs](admin-roles.md).
