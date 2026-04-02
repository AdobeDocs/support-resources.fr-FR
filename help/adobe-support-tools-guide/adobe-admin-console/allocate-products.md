---
title: Allouer des produits à des organisations enfants à l’aide de Global Admin Console
description: Découvrez comment les administrateurs globaux peuvent distribuer des ressources aux organisations enfants, ce qui permet une gestion efficace des ressources et une affectation des utilisateurs au sein de chaque organisation.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: f14254a77ce3620208389b36222f89be8f9d15b6
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Allouer des produits à des organisations enfants à l’aide de Global Admin Console

S’applique à l’entreprise.

Découvrez comment les administrateurs globaux peuvent distribuer des ressources aux organisations enfants, ce qui permet une gestion efficace des ressources et une affectation des utilisateurs au sein de chaque organisation.

Dans le [](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration), accédez à l&#39;onglet **[!UICONTROL Affectation de produit]**, puis sélectionnez un produit à affecter aux organisations enfants.

Connectez-vous à [](https://global-admin-console.adobe.com).

>[!NOTE]
>
>**[!UICONTROL Attribution de produit]** est disponible uniquement pour les contrats de contrat de licence temporaire pour entreprise (ETLA).

La distribution et l’administration des produits Adobe entre les organisations impliquent notamment le partitionnement des ressources achetées en allocations de ressources entre les organisations à gérer. Vous pouvez distribuer l’administration des ressources de produit à d’autres organisations en fournissant la totalité ou une partie de la ressource. Toutes les ressources de tous les produits ne peuvent pas être allouées ; certains produits ne peuvent pas être distribués à d’autres organisations. Ces produits apparaissent dans l’onglet **[!UICONTROL Affectation de produit]** mais ne disposent d’aucun contrôle pour les ajouter à d’autres organisations.

>[!WARNING]
>
>Vous ne pouvez pas allouer de produits à une organisation enfant à partir d&#39;un contrat qui a **expiré** ou si l&#39;organisation est dans un état **inactif**. En savoir plus sur l’[expiration du contrat](https://helpx.adobe.com/enterprise/using/contract-expiry.html) ou contactez l’administrateur ou l’administratrice de votre société pour obtenir de l’aide afin d’empêcher les utilisateurs et utilisatrices de l’organisation enfant de perdre l’accès à leurs applications et services Adobe.

## Stockage en pool

Cela s’applique aux clients qui disposent d’un onglet Stockage dans leur Admin Console. Si vous ne voyez pas d’onglet Stockage, cela signifie que votre Admin Console n’a pas encore été mise à jour vers le modèle de stockage d’entreprise. Une fois la migration de votre organisation effectuée, les modifications suivantes s’affichent :

- Les administrateurs globaux ont accès au quota et à l’utilisation du stockage dans l’ensemble de la hiérarchie et peuvent allouer du stockage aux organisations à l’aide de l’onglet **[!UICONTROL Allocation de produit]** dans le [Global Admin Console](https://adminconsole.adobe.com/).
- Les administrateurs système et les administrateurs de stockage contrôlent et voient le stockage de l&#39;ensemble de l&#39;entreprise. Il peut suivre et gérer le stockage à l’aide de l’onglet **[!UICONTROL Stockage]** dans le [Adobe Admin Console](https://adminconsole.adobe.com/).

Grâce aux mises à jour du stockage Adobe Creative Cloud, les quotas de stockage sont flexibles pour les utilisateurs finaux, jusqu’à la quantité de stockage achetée par l’entreprise. [En savoir plus](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html).

## Attribuer des produits

L’onglet **[!UICONTROL Affectation de produit]** de Global Admin Console affiche les unités d’affectation des produits achetés dans l’ensemble de la hiérarchie de l’organisation. En tant qu&#39;[administrateur global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), vous pouvez allouer ces ressources de produit à une autre organisation dans l&#39;arborescence de l&#39;organisation et spécifier la quantité allouée. En tant que [visionneuse globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), vous pouvez afficher et exporter les données, mais ne pouvez pas les mettre à jour.

Pour allouer des produits à une organisation, procédez comme suit :

1. Connectez-vous à [](https://global-admin-console.adobe.com) puis accédez à **[!UICONTROL Attribution de produits]**.
1. Sélectionnez un produit dans la liste déroulante pour voir comment il est attribué à différentes organisations.\
   Si une organisation ne dispose pas du produit actuellement, l’icône **[!UICONTROL Ajouter +]** s’affiche.

   >[!NRemarque]
   >
   >Si l&#39;organisation enfant a déjà un contrat d&#39;achat, l&#39;allocation de produits de l&#39;organisation parent à cette organisation enfant peut être limitée. [En savoir plus](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. Pour allouer le produit, sélectionnez l’icône **[!UICONTROL Ajouter +]** de l’organisation appropriée.\
   Certains produits incluent plusieurs ressources pouvant être allouées. Dans ce cas, plusieurs ressources sont répertoriées dans la boîte de dialogue et vous devez fournir des valeurs pour chacune d’elles. Par exemple, Adobe Stock peut inclure des crédits Image Adobe Stock et des crédits Premium.
   ![Images ](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. Dans la boîte de dialogue qui s’affiche, indiquez la quantité de produit.
1. Sélectionnez **[!UICONTROL Enregistrer]**.
1. Pour autoriser ou non la suraffectation d’une ressource, sélectionnez le bouton (bascule) approprié.
   ![Suraffectation](/help/adobe-support-tools-guide/assets/overallocation.png)
1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois l’affectation des ressources terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Attribuer et distribuer des licences utilisateur ou des transactions Adobe Acrobat Sign

Le Global Admin Console vous permet d’allouer et de distribuer des licences utilisateur ou des transactions Acrobat Sign à l’ensemble de la hiérarchie organisationnelle. Chaque organisation de la hiérarchie à laquelle sont attribuées des licences ou des transactions Acrobat Sign crée son propre compte Acrobat Sign.

- Chaque compte Acrobat Sign créé est indépendant et compartimenté en termes d’administration et de contenu.
- Chaque compte Acrobat Sign ne connaît pas les autres comptes Acrobat Sign (par exemple, dans les organisations parentes ou sœurs).

En savoir plus sur la [gestion de Adobe Acrobat Sign dans Admin Console](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html).

Pour gérer les modules complémentaires d’authentification tels que l’authentification basée sur les connaissances (KBA) et l’authentification téléphonique (PA), contactez votre représentant Adobe ou le responsable du succès client (CSM).


## Restrictions relatives à l’allocation de produits

L&#39;allocation d&#39;une organisation parent à une organisation enfant est limitée dans les cas suivants :

- Si les deux organisations ont des contrats différents et que le produit que vous essayez d’allouer existe dans les deux, il n’est pas autorisé de mélanger la même offre entre les contrats.
- Si les deux organisations ont le même contrat, vous pouvez demander l’autorisation d’allouer le produit en contactant votre représentant Adobe ou en [soumettant un dossier d’assistance](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html) en spécifiant que l’**[!UICONTROL allocation du produit]** dans Global Admin Console est bloquée.

## Suraffectation

En tant qu’[administrateur global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), vous pouvez autoriser la suraffectation de ressources.

Une politique [politique](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies) d’affectation associée au produit et à l’organisation indique si la suraffectation est autorisée.

La suraffectation permet d’accorder plus de ressources de produit à une organisation enfant que ce qui est disponible dans l’organisation parent. Cela s’avère utile lorsque les allocations sont approximatives et que l’administrateur ne souhaite pas avoir à maintenir le cumul des allocations de ressources.
Si la suraffectation est désactivée pour une ressource de produit dans une organisation, la somme des octrois enfants ne peut pas dépasser l&#39;octrois parent. Les demandes de surallocation d’une ressource marquée comme surallocation désactivée ne sont pas exécutées.
Lorsque le bouton de suraffectation passe de activé à désactivé, les valeurs d&#39;octroi doivent être ajustées pour éliminer la suraffectation avant que les mises à jour d&#39;octroi puissent être exécutées, si une situation de suraffectation est présente dans les quantités d&#39;octroi d&#39;une ressource.

![Suraffectation](/help/adobe-support-tools-guide/assets/overallocation.png)

## Contrats expirés dans la hiérarchie

Vous ne pouvez pas allouer de produits à une organisation enfant à partir d’un contrat ETLA arrivé à expiration. Les bannières et notifications in-app, telles que celles qui suivent, sur les pages **[!UICONTROL Aperçu]** et **[!UICONTROL Affectation du produit]** indiquent clairement quand le contrat sur une ou plusieurs organisations enfants va expirer, a expiré ou est inactif.

![Affectation de produits](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[!IImportant]
>
>Une fois qu’un contrat ETLA qui fait partie de la hiérarchie est inactif, les produits sont supprimés des pages **[!UICONTROL Aperçu]** et **[!UICONTROL Affectation des produits]**.

[En savoir plus sur l’expiration du contrat](https://helpx.adobe.com/enterprise/using/contract-expiry.html) ou contactez l’administrateur ou l’administratrice de votre société pour obtenir de l’aide afin d’empêcher les utilisateurs et utilisatrices de l’organisation enfant de perdre l’accès à leurs applications et services Adobe.
