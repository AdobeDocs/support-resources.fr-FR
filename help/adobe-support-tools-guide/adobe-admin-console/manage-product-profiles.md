---
title: Gestion des profils de produit dans Global Admin Console
description: Découvrez comment les administrateurs globaux peuvent ajouter, modifier et supprimer des profils de produit dans Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 1%

---

# Gestion des profils de produit dans Global Admin Console

**S’applique à :** Entreprise

Les administrateurs globaux peuvent ajouter, modifier et supprimer des profils de produit dans le [](https://global-admin-console.adobe.com/).

>[!NOTE]
>
>Dans [](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), sélectionnez une organisation et accédez à **[!UICONTROL Produits]**. Vous pouvez activer tous les services ou certains services pour un produit à l’aide des profils de produit.

Comme dans la version standard d’Admin Console, les profils de produit vous permettent d’affiner l’utilisation des produits au sein d’une organisation. Vous pouvez également affecter des administrateurs, appelés **[!UICONTROL administrateurs de profil de produit]**, aux profils de produit. Ces administrateurs peuvent ajouter des utilisateurs finaux aux profils de produits qu’ils gèrent.

Pour gérer les profils de produit, sélectionnez un produit. Les commandes d’ajout, de modification et de suppression des profils de produit s’affichent.

>[!NOTE]
>
>Pour certains produits, vous ne pouvez pas créer ni modifier de profils de produit dans le Global Admin Console. Dans ce cas, utilisez plutôt [](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview).

## Ajouter un profil de produit

1. Dans [](https://global-admin-console.adobe.com/), sélectionnez une organisation à modifier, puis accédez à l’onglet **[!UICONTROL Produits]**.
1. Sélectionnez un produit auquel ajouter un profil de produit.
1. Sélectionnez **[!UICONTROL Ajouter un profil]**.
1. Dans la boîte de dialogue **[!UICONTROL Ajouter un profil]**, saisissez les informations suivantes :

   | Champ | Description |
   |---|---|
   | **[!UICONTROL Nom]** | Nom unique du profil de produit au sein de l’organisation, distinct des autres profils de produit et groupes d’utilisateurs. |
   | **[!UICONTROL Quota]** | Nombre cible de licences attribuées pour ce profil. |
   | **[!UICONTROL Groupes d’utilisateurs]** | Sélectionnez dans la liste déroulante ou saisissez un nom de groupe d’utilisateurs. Si le groupe d’utilisateurs n’existe pas encore, commencez par le créer à partir de l’onglet [**[!UICONTROL Groupes d’utilisateurs ]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html). |
   | **[!UICONTROL Administrateurs]** | Sélectionnez dans la liste déroulante ou saisissez l’adresse e-mail d’un administrateur. Si l’administrateur n’existe pas encore, créez-le d’abord via l’onglet [**[!UICONTROL Admins ]**](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators). |

   Le profil de produit est attribué aux [!UICONTROL groupes d’utilisateurs] spécifiés. Les administrateurs spécifiés deviennent les **[!UICONTROL administrateurs de profil de produit]**, qui peuvent gérer le profil via le Adobe Admin Console pour l’organisation appropriée.

   ![Ajouter un profil](./assets/manage-product-profiles_add-profile.png)

1. Utilisez le bouton (bascule) **[!UICONTROL Notifications]** pour activer ou désactiver les notifications par e-mail. Lorsque cette option est activée, les utilisateurs sont avertis par e-mail lorsqu’ils sont ajoutés ou supprimés du profil.
1. Utilisez les boutons (bascule) individuels **[!UICONTROL Services]** pour activer ou désactiver des services spécifiques pour le profil de produit. Pour plus d’informations, voir [Activation/désactivation des services pour un profil de produit](https://helpx.adobe.com/enterprise/using/enable-disable-services.html).
1. Sélectionnez **[!UICONTROL Enregistrer]**.
1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Modification d’un profil de produit

1. Sélectionnez une organisation à modifier, accédez à l’onglet **[!UICONTROL Produits]** et sélectionnez un produit.
1. Sélectionnez l’icône **[!UICONTROL Plus d’options]** ![Plus d’options](./assets/manage-product-profiles_more-options.png) pour le profil de produit approprié, puis sélectionnez **[!UICONTROL Modifier le profil]**.
1. Mettez à jour les détails du profil de produit selon vos besoins et sélectionnez **[!UICONTROL Enregistrer]**.
1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Suppression d’un profil de produit

>[!WARNING]
>
> La suppression d’un profil de produit supprime l’accès au produit de tous les utilisateurs qui étaient membres de ce profil ou qui appartenaient à des groupes d’utilisateurs associés à ce profil.

1. Sélectionnez une organisation à modifier, accédez à l’onglet **[!UICONTROL Produits]** et sélectionnez un produit.
1. Sélectionnez l’icône **[!UICONTROL Plus d’options]** ![Plus d’options](./assets/manage-product-profiles_more-options.png) pour le profil de produit approprié, puis sélectionnez **[!UICONTROL Supprimer le profil]**.
1. Sélectionnez **[!UICONTROL OK]** dans la boîte de dialogue de confirmation.
1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).


## Lecture connexe

- [Adopter une administration mondiale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)
- [Gérer les administrateurs](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)
- [Gérer les groupes d’utilisateurs](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-user-groups)
- [Allouer des produits aux organisations enfants](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/allocate-products)
- [Exécution des traitements en attente](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [Activer/désactiver des services](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Présentation d’](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
