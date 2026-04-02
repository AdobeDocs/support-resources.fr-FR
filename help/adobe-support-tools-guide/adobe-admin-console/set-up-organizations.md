---
title: Gérer la hiérarchie de l’organisation
description: Découvrez comment les administrateurs globaux peuvent gérer la hiérarchie de l’organisation dans Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# Gérer la hiérarchie de l’organisation

S’applique à l’entreprise.

Découvrez comment les administrateurs globaux peuvent gérer la hiérarchie de l’organisation dans Global Admin Console.

Une fois que vous avez obtenu [accès au [!DNL Global Admin Console]](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), vous pouvez créer de nouvelles organisations, ajouter des organisations existantes à la hiérarchie, supprimer des organisations et modifier une organisation parent. Accédez ici à [connexion au Global Admin Console](https://global-admin-console.adobe.com/)

Une organisation est une structure utilisée pour gérer les produits et les utilisateurs Adobe. Le [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) permet aux administrateurs de gérer le déploiement et la configuration des produits et des utilisateurs au sein de leur organisation. Le [[!DNL Global Admin Console]](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration) permet aux administrateurs globaux de créer, gérer et supprimer plusieurs organisations.

## Créer une organisation enfant

En tant qu’[administrateur global](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), vous pouvez créer des organisations enfants de n’importe quelle organisation dans la hiérarchie et définir le nom, le pays, les groupes d’utilisateurs, les produits, les profils de produits, les administrateurs et administratrices et les politiques.

Lorsqu’une nouvelle organisation enfant est créée, les éléments suivants sont automatiquement hérités du parent immédiat :

- Paramètres [politique](https://helpx.adobe.com/fr/enterprise/global-admin-console/update-policies.html) de l’entreprise (y compris les verrous le cas échéant).
- La liste des administrateurs système (contrôlée par le **[!UICONTROL Hériter des administrateurs système à la création]** [politique](https://helpx.adobe.com/fr/enterprise/global-admin-console/update-policies.html)).
Les éléments suivants peuvent empêcher les administrateurs système d’être hérités :
   - Absence de [confiance de domaine](https://helpx.adobe.com/fr/enterprise/using/directory-trust.html).
   - Restrictions de type d’utilisateur (ajout de politiques d’utilisateurs Adobe ID / Enterprise ID / Federated ID). En savoir plus sur les [détails de la politique](https://helpx.adobe.com/fr/enterprise/global-admin-console/update-policies.html).
- Accès aux utilisateurs [[!DNL Federated ID]] ou [[!DNL Enterprise ID]] à partir des domaines auxquels l’organisation parent a accès. Cela rend les utilisateurs du domaine dans le parent disponibles dans l’organisation enfant. L’héritage de l’accès des utilisateurs est contrôlé par **Hériter des utilisateurs des répertoires gérés par l’organisation parent** [politique](https://helpx.adobe.com/fr/enterprise/global-admin-console/update-policies.html).
- Politique de partage, politique de mot de passe et contacts de sécurité (contrôlés par **Hériter des paramètres de partage des ressources lors de la création de l’organisation enfant** [politique](https://helpx.adobe.com/fr/enterprise/global-admin-console/update-policies.html)).

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/). Dans l’onglet **[!UICONTROL Organisations]**, sélectionnez l’organisation à laquelle vous souhaitez ajouter une organisation enfant.
2. Sélectionnez l’icône **[!UICONTROL Ajouter+]** .
   ![Ajouter une organisation](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Indiquez un **nom** et le **pays** de l’organisation.\
   Le nom simple de l’organisation doit comporter entre 4 et 100 caractères ; la longueur maximale du chemin d’accès est de 255 caractères.
   ![Ajouter une organisation enfant](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. Sélectionnez **[!UICONTROL Enregistrer]**.
5. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/execute-jobs.html).

## Supprimer une organisation enfant

En tant qu’[administrateur global](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), vous pouvez supprimer les organisations enfants. L’opération de suppression ne peut pas être annulée et l’organisation racine ne peut pas être supprimée. Les ressources allouées à l’organisation supprimée sont renvoyées à son organisation parent. Avant qu&#39;une organisation ne soit supprimée, son parent devient automatiquement le parent de toutes ses organisations enfants.

Une organisation ne peut être supprimée que si les critères suivants sont remplis :

- Il n’existe aucun compte Sign, aucun achat Adobe Stock ni référentiel de stockage dans l’organisation.
- Il n’y a aucun domaine demandé dans l’organisation.
- Il n’existe aucun produit instancié dans l’organisation.
- Il n’existe aucun produit Experience Cloud pouvant inclure des instanciations dans l’organisation.

>[!WARNING]
>
>La suppression d’une organisation a une incidence sur vos utilisateurs. Assurez-vous qu’aucun accès ni aucune information ne sera perdu lors de la suppression d’une organisation.

1. Connectez-vous à l’[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) . Accédez à l’onglet **[!UICONTROL Organisations]** et sélectionnez l’organisation à supprimer.
1. Sélectionnez l’icône **[!UICONTROL Supprimer]**.
   ![Supprimer l’organisation](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. Dans la boîte de dialogue **[!UICONTROL Supprimer l’organisation]**, sélectionnez **[!UICONTROL OK]**.
1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/execute-jobs.html).

## Renommer une organisation

Le nom de l’organisation est le nom officiel de votre société ou institution, défini lors de l’achat. Les utilisateurs voient ce nom lors de la sélection d’un profil lors de la connexion, en particulier s’ils ont accès aux produits Adobe de plusieurs organisations ou s’ils doivent choisir entre un profil professionnel et un profil personnel.

En tant qu&#39;[administrateur global](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), vous pouvez modifier le nom d&#39;une organisation parent ou enfant afin d&#39;aider les utilisateurs à identifier le profil correct lors de la connexion aux produits et services [[!DNL Creative Cloud]].

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/). Dans l’onglet **[!UICONTROL Organisations]**, sélectionnez l’organisation à renommer.
1. Sélectionnez l’icône **[!UICONTROL Modifier]**.
   ![Renommer l’organisation](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Mettez à jour le nom de votre organisation et sélectionnez **[!UICONTROL Enregistrer]**.

>[!TIP]
>
>Utilisez un nom d’organisation clair et reconnaissable pouvant contenir jusqu’à 255 caractères pour aider les utilisateurs à sélectionner le profil correct. Évitez d’utiliser des caractères spéciaux et pensez à inclure la région, le service ou le droit. Évitez également les acronymes peu courants et les noms vagues ou similaires dans la hiérarchie de votre organisation.

Les modifications sont consignées dans le journal d’audit, tous les utilisateurs sont avertis par e-mail et le nom ne peut plus être mis à jour pendant 24 heures. [Découvrez comment afficher et télécharger les journaux d’audit](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports).

## Modifier le parent d’une organisation

Par [[!DNL Global Administrator]](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), vous pouvez représenter une organisation dans la hiérarchie des organisations à l&#39;aide du bouton **[!UICONTROL Modifier la hiérarchie]**.

La modification du parent d’une organisation a l’impact suivant :

- Le fait de reparenter une organisation déplace l’ensemble de la sous-arborescence basée sur l’organisation reparée avec celle-ci. Les chemins d’accès de l’organisation représentée et de ses enfants sont mis à jour pour refléter leur nouvel emplacement.
- Organisation [politiques](https://helpx.adobe.com/fr/enterprise/global-admin-console/update-policies.html) des organisations déplacées sont mises à jour afin que tous les verrous des politiques soient conservés par une organisation dans la nouvelle hiérarchie.
- La modification de la position d’une organisation dans la hiérarchie peut modifier les administrateurs globaux de cette organisation. Les rôles d’administration globale sont hérités dans la hiérarchie, de sorte que tous les administrateurs globaux de la nouvelle organisation parent deviennent automatiquement administrateurs globaux de l’organisation déplacée. De même, les administrateurs globaux peuvent perdre leur rôle dans l’organisation déplacée s’ils avaient ce rôle en vertu de leur fonction d’administrateur global de l’ancien parent. Les rôles d’administration globaux hérités ne sont pas répertoriés dans le volet Administrateurs de l’organisation.
- La réorganisation des parents affecte également les produits disponibles dans les organisations déplacées. Lorsque cela est possible, les [allocations de produits](https://helpx.adobe.com/fr/enterprise/global-admin-console/allocate-products.html) sont mises à jour afin qu’elles proviennent du nouvel emplacement parent.
- Si les allocations de produits ne peuvent pas être mises à jour pour provenir du nouveau parent, les produits sont supprimés avec les profils de produits de ces produits. Les utilisateurs peuvent perdre l’accès en raison de cette opération. Pour que le produit soit disponible dans le nouvel emplacement, l’ancêtre commun le plus proche de l’ancien et du nouvel emplacement doit disposer du produit.

>[!WARNING]
>
>Si des produits sont supprimés à la suite du reparentage, les utilisateurs perdent l’accès à ces produits.

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/). Dans l’onglet **[!UICONTROL Organisations]**, sélectionnez **[!UICONTROL Modifier la hiérarchie]** pour activer le repérage des organisations.
2. Sélectionnez **[!UICONTROL OK]** dans l’écran pop-up qui s’affiche.
3. Pour effectuer un rendu, faites glisser l’organisation enfant au-dessus de l’organisation souhaitée.
4. Sélectionnez **[!UICONTROL Enregistrer]** lorsque vous avez terminé de recomposer vos organisations.
5. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/execute-jobs.html).

Une fois la tâche terminée, vous pouvez accéder à Affectation des produits et [modifier les valeurs d’octroi](https://helpx.adobe.com/fr/enterprise/global-admin-console/allocate-products.html) pour refléter la modification de l’affectation des ressources de produit.

## Ajouter des organisations existantes à l’aide du mappeur d’organisation

En tant qu’[administrateur global](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), vous pouvez ajouter à la hiérarchie des organisations des organisations qui ne font pas actuellement partie de votre hiérarchie Global Admin Console.

Vous pouvez également ajouter des organisations d’équipe à la hiérarchie de l’organisation. Les organisations d’équipe ne participent pas à l’affectation de produits ni au cumul de l’utilisation des produits, et la gestion des organisations d’équipe dans le Global Admin Console est limitée. Vous pouvez les ajouter à la hiérarchie de l’organisation pour les suivre et avoir une visibilité sur les produits qu’ils achètent. Les organisations d&#39;équipes ne peuvent pas avoir d&#39;organisations enfants sous elles et ne disposent pas de nombreuses fonctionnalités des organisations d&#39;entreprise.

En savoir plus sur les [limitations sur l’attribution de produits](https://helpx.adobe.com/fr/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Vous pouvez uniquement ajouter des organisations enfants aux organisations racines basées sur le même modèle de stockage. Ainsi, les organisations enfants basées sur le modèle de stockage utilisateur ne peuvent être ajoutées qu’aux organisations racines basées sur le modèle de stockage utilisateur. De plus, les organisations enfants basées sur le modèle de stockage d’entreprise ne peuvent être ajoutées qu’aux organisations racines basées sur le modèle de stockage d’entreprise.

L’onglet **[!UICONTROL Mappeur d’organisation]** affiche les éléments suivants :

1. Liste déroulante avec une liste d’organisations parents possibles dans laquelle vous pouvez ajouter une organisation enfant. Il s’agit d’organisations pour lesquelles vous êtes un administrateur global.
1. Liste des organisations enfants pouvant être ajoutées sous le parent sélectionné à l’étape 1. Il s’agit d’organisations pour lesquelles vous êtes administrateur système et qui ne sont pas déjà enfants d’une autre organisation.

Lorsqu’une organisation est ajoutée à l’administration globale, les produits des organisations qui sont ajoutés à l’aide du mappeur d’organisation restent des achats ; les numéros [&#x200B; Affectation de produit](https://helpx.adobe.com/fr/enterprise/global-admin-console/allocate-products.html) ne sont plus cumulés dans ces organisations.

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/) et accédez à **[!UICONTROL Mappeur d’organisation]**.
2. Sélectionnez une organisation parente dans la liste déroulante.\
   Il s’agit des organisations pour lesquelles vous êtes directement ajouté en tant qu’administrateur global. Dans la liste déroulante, si vous ne voyez pas une organisation que vous souhaitez utiliser comme parent, sélectionnez-en une plus haut dans la hiérarchie. Une fois l&#39;opération du mappeur d&#39;organisation terminée, vous pouvez utiliser [Modifier la hiérarchie](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization) pour déplacer la nouvelle organisation vers le bas de l&#39;arborescence afin d&#39;avoir le parent que vous souhaitez utiliser.
3. Sélectionnez les organisations à ajouter en tant qu’enfants de l’organisation sélectionnée à l’étape précédente.
4. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]**. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/fr/enterprise/global-admin-console/execute-jobs.html).
5. Après avoir appliqué les modifications, vous pouvez répéter les étapes ci-dessus pour ajouter d’autres organisations enfants à la hiérarchie de votre organisation.

Une fois qu’une organisation se trouve dans la hiérarchie, vous pouvez ajuster ses politiques, ses administrateurs ou d’autres paramètres en accédant à l’onglet **[!UICONTROL Organisations]**.
