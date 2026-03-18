---
title: Gestion des groupes d’utilisateurs dans Global Admin Console
description: Découvrez comment créer, partager, modifier et supprimer des groupes d’utilisateurs dans Global Admin Console afin de rationaliser la gestion des utilisateurs dans l’ensemble des organisations.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: f81a20fd6d9d64443f4708b3fc17de7240d1bc61
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---


# Gestion des groupes d’utilisateurs dans Global Admin Console

Créez, gérez et partagez des groupes d’utilisateurs dans Global Admin Console afin de rationaliser la gestion des utilisateurs en regroupant les utilisateurs avec les mêmes autorisations, ce qui vous permet de gagner du temps et d’assurer la cohérence.

Dans [Global Admin Console](https://helpx.adobe.com/fr/enterprise/global-admin-console/adopt-global-administration.html), sélectionnez une organisation et accédez à **[!UICONTROL Groupes d’utilisateurs]**. Partagez des groupes dans plusieurs organisations à l’aide d’une seule source User Management pour synchroniser les utilisateurs et les groupes.

[Connexion au Global Admin Console](https://global-admin-console.adobe.com)



## Création de groupes d’utilisateurs

Vous pouvez [créer des groupes d’utilisateurs](https://helpx.adobe.com/fr/enterprise/using/user-groups.html) individuellement ou en bloc, ou [les synchroniser directement à partir d’une annonce publicitaire Azure établie](https://helpx.adobe.com/fr/enterprise/using/add-azure-sync.html) vers un répertoire fédéré dans Adobe Admin Console. Dans Global Admin Console, vous pouvez définir des groupes d’utilisateurs auxquels des profils de produit pertinents sont attribués, auxquels les administrateurs des groupes d’utilisateurs peuvent ensuite ajouter des utilisateurs à l’aide d’Admin Console.

1. Connectez-vous à [Global Admin Console](https://global-admin-console.adobe.com/), sélectionnez une organisation à modifier, puis accédez à l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

2. Sélectionnez **[!UICONTROL Ajouter un groupe d’utilisateurs]**.

   ![Onglet Organisations dans le Global Admin Console avec l’onglet Groupes d’utilisateurs sélectionné.](assets/add-user-group.png "Ajouter un groupe d’utilisateurs")

   _Ajoutez des groupes d’utilisateurs à une organisation pour rationaliser la gestion des utilisateurs._

3. Saisissez ce qui suit dans la boîte de dialogue **[!UICONTROL Ajouter un groupe d’utilisateurs]** qui s’affiche :
   - **[!UICONTROL Nom]** : spécifiez un nom pour le groupe d’utilisateurs.
   - **[!UICONTROL Profils de produit]** : si vous souhaitez accorder l’accès au produit aux membres actuels ou futurs du groupe d’utilisateurs, cliquez sur la flèche déroulante pour sélectionner un profil de produit dans la liste ou saisissez le nom du profil de produit et sélectionnez-le dans la liste déroulante qui s’affiche. Si vous souhaitez ajouter un profil de produit qui n’a pas encore été créé, vous devez d’abord le faire à l’aide de l’onglet [Profils de produit](https://helpx.adobe.com/fr/enterprise/using/global-admin-edit-organizations.html#profiles).
   - **[!UICONTROL Administrateurs]** : cliquez sur la flèche déroulante pour sélectionner un administrateur dans la liste, ou saisissez l’adresse e-mail de l’administrateur et sélectionnez-la dans la liste déroulante qui s’affiche. Si vous souhaitez ajouter un nouvel administrateur qui n’a pas encore été créé, vous devez d’abord le créer à l’aide de l’onglet [Admins](#share-user-groups).

   Les profils de produit que vous spécifiez sont affectés au groupe d’utilisateurs. Les administrateurs que vous spécifiez deviennent les administrateurs du groupe d’utilisateurs pour le groupe. Les administrateurs du groupe d’utilisateurs peuvent utiliser le Adobe Admin Console pour l’organisation appropriée afin de gérer le groupe.

4. Sélectionnez **[!UICONTROL Enregistrer]**.

5. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** pour vérifier les mises à jour. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Les administrateurs globaux peuvent [affecter des profils de produit et des administrateurs de groupe d’utilisateurs](#review-user-groups) aux groupes d’utilisateurs à l’aide de Global Admin Console. Avec Adobe Admin Console, les administrateurs système et les administrateurs de groupe d’utilisateurs peuvent [ajouter des utilisateurs et affecter des administrateurs et des profils de produits](https://helpx.adobe.com/fr/enterprise/using/user-groups.html) au groupe d’utilisateurs.



## Partage de groupes d’utilisateurs

La projection de groupes vous permet de synchroniser les groupes d’utilisateurs et d’utilisatrices et leurs utilisateurs associés à partir d’une seule source de gestion vers plusieurs Admin Console. Les administrateurs globaux peuvent partager des groupes d’utilisateurs avec les descendants hiérarchiques de l’organisation source, en travaillant vers le bas, et non vers le haut ou côte à côte.

1. Connectez-vous à [Global Admin Console](https://global-admin-console.adobe.com/), sélectionnez une organisation et accédez à l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

2. Cochez les cases des groupes d’utilisateurs que vous souhaitez partager.

   Les groupes peuvent être désactivés pour le partage dans les cas suivants :
   - Le groupe d’utilisateurs est partagé à partir d’une autre organisation. Pour partager ou modifier le groupe, sélectionnez l’organisation qui le possède dans la hiérarchie de l’organisation.
   - L’organisation n’utilise pas le stockage [Adobe pour entreprise](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html), qui est actuellement déployé à l’échelle mondiale par phases.
   - La politique d’organisation est désactivée. Accédez à l’onglet **[!UICONTROL Politiques]** pour activer la politique **[!UICONTROL Gérer les groupes d’utilisateurs partagés]**.
   - L’organisation ne dispose d’aucune organisation enfant avec laquelle partager des groupes d’utilisateurs.

3. Sélectionnez **[!UICONTROL Partager le groupe d’utilisateurs]**.

4. <a id="review-user-groups"></a>Examinez les groupes d’utilisateurs à partager avec d’autres organisations. Si vous êtes également administrateur système dans l’organisation sélectionnée, sélectionnez l’option **[!UICONTROL Ouvrir dans Admin Console]** <img src="assets/icon-open-in-admin-console.png" alt="Icône Ouvrir dans Admin Console" width="14" height="14"> l’icône pour consulter la liste des membres du groupe d’utilisateurs dans le Adobe Admin Console.

   >[!NOTE]
   >
   >Pour éviter les conflits, assurez-vous que les organisations avec lesquelles vous envisagez de partager des groupes d’utilisateurs ne disposent pas déjà de groupes portant le même nom.

5. Sélectionnez **[!UICONTROL Suivant]**.

6. Sélectionnez les organisations avec lesquelles partager des groupes d’utilisateurs et sélectionnez **[!UICONTROL Suivant]**.

7. S’il n’existe aucun conflit, sélectionnez **[!UICONTROL Partager les groupes d’utilisateurs]**.

   En cas de conflits (il existe des groupes d’utilisateurs portant le même nom dans l’organisation cible), choisissez l’une des options suivantes, puis sélectionnez **[!UICONTROL Partager les groupes d’utilisateurs]** :
   - **[!UICONTROL Ignorer (par défaut)]** : ignore les groupes des organisations cibles portant le même nom.
   - **[!UICONTROL Ajouter uniquement]** : fusionnez les groupes d’utilisateurs en ajoutant de nouveaux utilisateurs aux groupes d’utilisateurs existants sans supprimer d’utilisateurs.
   - **[!UICONTROL Groupe miroir]** : ajustez les groupes de l’organisation cible pour qu’ils correspondent au groupe partagé en ajoutant ou en supprimant des utilisateurs.

8. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** pour vérifier les mises à jour. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   Les événements de projection de groupe sont consignés à titre de référence. Découvrez comment [afficher et télécharger les journaux d’audit](https://helpx.adobe.com/fr/enterprise/global-admin-console/insights.html).


Lorsque vous partagez un groupe d’utilisateurs, le groupe et ses utilisateurs sont ajoutés à l’organisation cible. Toutefois, le *groupe d’utilisateurs source) contrôle* les groupes d’utilisateurs partagés et leurs utilisateurs. Les affectations d’administrateur et de profil de produit ne sont *pas* synchronisées entre les organisations.

Les modifications apportées au nom du groupe d&#39;utilisateurs projeté ou aux utilisateurs associés du groupe d&#39;utilisateurs source sont automatiquement mises à jour dans l&#39;organisation cible. Bien que le groupe d’utilisateurs partagé ne puisse pas être géré directement, un administrateur de l’organisation cible peut affecter des profils de produit à un groupe partagé, ce qui donne un accès sous licence aux utilisateurs du groupe.



## Révoquer l’accès aux groupes partagés

1. Connectez-vous à [Global Admin Console](https://global-admin-console.adobe.com/), sélectionnez une organisation et accédez à l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

2. Sélectionnez **[!UICONTROL Gérer l’accès partagé]** pour le groupe d’utilisateurs approprié.

3. Sélectionnez les organisations dont vous souhaitez révoquer l’accès.

4. Sélectionnez **[!UICONTROL Révoquer l’accès]**.

5. Lors de la révocation de l’accès, vous pouvez choisir de supprimer le groupe d’utilisateurs et les utilisateurs ou de laisser une copie dans les organisations cibles :
   - Lors de la suppression, le groupe d’utilisateurs est supprimé des organisations cibles. Les utilisateurs qui ne sont pas membres d’autres groupes partagés sont supprimés des organisations cibles et perdent l’accès à tous les produits, services et ressources.
   - Lorsqu’ils laissent une copie, le groupe d’utilisateurs et les utilisatrices restent dans les organisations cibles, conservant toutes les affectations intactes. Cependant, le groupe d’utilisateurs ne sera plus synchronisé et pourra être géré par les administrateurs des organisations cibles.

6. Sélectionnez **[!UICONTROL Révoquer l’accès]**.

7. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** pour vérifier les mises à jour. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).



## Modifier les groupes d’utilisateurs

1. Connectez-vous à [Global Admin Console](https://global-admin-console.adobe.com/), sélectionnez une organisation et accédez à l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

2. Sélectionnez l’option **[!UICONTROL Plus d’options]** <img src="assets/icon-more-options.png" alt="Icône Plus d’options" width="14" height="14" style="vertical-align:middle"> l’icône du groupe d’utilisateurs approprié, puis sélectionnez **[!UICONTROL Modifier le groupe d’utilisateurs]**.

   >[!NOTE]
   >
   >Vous ne pouvez pas modifier des groupes d’utilisateurs qui ne sont pas détenus par l’organisation sélectionnée.

   ![Organisation sélectionnée avec l’option Modifier le groupe d’utilisateurs mise en surbrillance sous l’onglet Groupes d’utilisateurs.](assets/edit-user-group.png "Modifier le groupe d’utilisateurs")

   _Modifiez les groupes d’utilisateurs pour mettre à jour le nom du groupe d’utilisateurs, les profils de produit ou les administrateurs._

3. Mettez à jour le nom du groupe d’utilisateurs, les profils de produit ou les administrateurs. Sélectionnez ensuite **[!UICONTROL Enregistrer]**.

   >[!NOTE]
   >
   >Dans l’assistant **[!UICONTROL Modifier le groupe d’utilisateurs]**, vous ne pouvez affecter des rôles d’administrateur qu’aux utilisateurs qui disposent déjà d’un rôle d’administrateur affecté dans cette organisation. Découvrez comment [&#x200B; ajouter de nouveaux administrateurs &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/manage-admins.html).

4. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** pour vérifier les mises à jour. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Si vous modifiez le nom d’un groupe d’utilisateurs partagé, les modifications sont automatiquement mises à jour dans l’organisation cible.



## Supprimer des groupes d’utilisateurs

1. Connectez-vous à [Global Admin Console](https://global-admin-console.adobe.com/), sélectionnez une organisation et accédez à l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

2. Sélectionnez l’option **[!UICONTROL Plus d’options]** <img src="assets/icon-more-options.png" alt="Icône Plus d’options" width="14" height="14" style="vertical-align:middle"> l’icône du groupe d’utilisateurs approprié, puis sélectionnez **[!UICONTROL Supprimer le groupe d’utilisateurs]**.

   >[!NOTE]
   >
   >Vous ne pouvez pas supprimer des groupes d’utilisateurs que l’organisation sélectionnée ne possède pas.

3. Sélectionnez **[!UICONTROL Ok]** dans la boîte de dialogue qui s’affiche.

   >[!CAUTION]
   >
   >La suppression d’un groupe d’utilisateurs peut avoir un impact sur vos utilisateurs. Assurez-vous qu’aucun accès ni aucune information ne sera perdu lors de la suppression du groupe d’utilisateurs.

4. Après avoir modifié les organisations, sélectionnez **[!UICONTROL Examiner les modifications en attente]** pour les examiner. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).
