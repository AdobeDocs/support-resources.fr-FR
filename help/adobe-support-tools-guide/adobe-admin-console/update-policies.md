---
title: Mettre à jour les politiques d’organisation dans le Global Admin Console
description: Découvrez comment un administrateur global peut définir et modifier des politiques pour une organisation et ses enfants dans Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
source-git-commit: 90807a4e803de702c9e0975df551efefc254030a
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 1%

---

# Mettre à jour les politiques d’organisation dans le Global Admin Console

**S’applique à :** Entreprise

Découvrez comment un administrateur global peut définir et modifier des politiques pour une organisation et ses enfants dans Global Admin Console.

>[!NOTE]
>
>Dans [](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html), sélectionnez une organisation dans la hiérarchie et accédez à l’onglet **Politiques** pour autoriser ou refuser les politiques, ou les verrouiller.
>
> [Connexion au Global Admin Console](https://global-admin-console.adobe.com/)

Les politiques sont associées à une organisation et limitent les opérations qui peuvent être effectuées sur cette organisation. Lorsqu’une valeur de politique est définie, elle limite ou active les actions à partir de ce moment.
Par exemple, si la politique **Demander les domaines** est définie sur *non autorisé*, aucun domaine supplémentaire ne peut être demandé, mais les domaines demandés avant de définir la valeur de la politique ne sont pas affectés.

## Configurer Des Politiques

Pour modifier les politiques d’une organisation, procédez comme suit :

1. Dans le Global Admin Console, [sélectionnez une organisation](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) à modifier, puis accédez à l’onglet **[!UICONTROL Politiques]**.
1. Sélectionnez le bouton (bascule) de la politique appropriée à autoriser ou non. Vous pouvez également verrouiller une politique de sorte que seul un administrateur global de l’[organisation sélectionnée](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) ou de son organisation parent puisse la modifier ou la déverrouiller.
1. Pour verrouiller une politique, sélectionnez l’icône **[!UICONTROL Verrouiller]** ![Verrouiller](./assets/lock.png). Survoler le verrou affiche le nom de l’organisation sélectionnée. En savoir plus sur les [verrous de politique](#policy-locks).
1. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]** une fois la modification des organisations terminée. Après la révision, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Verrous de stratégie {#policy-locks}

Lorsqu’une politique est verrouillée, sa valeur ne peut pas être modifiée tant que la politique n’est pas déverrouillée. Le Global Admin Console mémorise l’[organisation sélectionnée](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) dans le sélecteur d’organisation comme étant l’organisation à partir de laquelle la politique a été verrouillée. Tout administrateur global de cette organisation sélectionnée ou de toute organisation située plus haut dans l’arborescence est autorisé à déverrouiller la politique. Les administrateurs globaux dont l’étendue est inférieure à celle de cette organisation ne sont pas autorisés à déverrouiller et à modifier les valeurs de politique.

Pour créer un environnement verrouillé, définissez les valeurs de politique souhaitées sur vos organisations enfants, puis verrouillez-les. Les administrateurs globaux de ces organisations enfants ne pourront pas modifier les valeurs de la politique.

### Exemple : Un Environnement Verrouillé

Si Elissa, l’administrateur global de *Division Acme*, crée des organisations enfants *Marketing* et *Ingénierie*, ajoute Robert en tant qu’administrateur global de *Marketing* et Sarah en tant qu’administrateur global de *Ingénierie*. Ensuite, elle définit plusieurs politiques sur *Interdit* et *verrouille*. Elissa peut ensuite déverrouiller et modifier les valeurs de politique lorsqu’elle choisit *Division Acme* comme organisation sélectionnée, mais Robert et Sarah ne peuvent pas déverrouiller les politiques sur les organisations dont ils sont administrateurs globaux, car les politiques sont verrouillées par l’organisation *Division Acme*.

## Détails de la politique

### Gestion de l’organisation

| Nom de la stratégie | Description |
| --- | --- |
| **Créer des organisations enfants** | Permet aux administrateurs globaux de créer des organisations enfants. Si *désactivé*, aucune organisation enfant ne peut être créée. |
| **Renommer l’organisation** | Si cela est autorisé, un administrateur global ou système peut renommer l’organisation. Il contrôle également la modification du pays/de la région de l’organisation. Le chemin d&#39;accès d&#39;une organisation peut également être modifié indépendamment de ce paramètre de stratégie si une organisation parent est renommée ou si l&#39;organisation ou un ancêtre de l&#39;organisation est reparé. |
| **Supprimer organisations** | Permet aux administrateurs globaux de supprimer les organisations enfants. Cela devient plus important lorsque les organisations disposant d’un stockage d’entreprise sont activées en raison du risque de suppression des ressources utilisateur. |

### Gestion de l’administrateur

| Nom de la stratégie | Description |
| --- | --- |
| **Ajouter ou supprimer des administrateurs** | Permet aux administrateurs globaux d’ajouter de nouveaux administrateurs à une organisation. Si *désactivé*, les nouveaux administrateurs ne peuvent pas être ajoutés. |
| **Hériter des administrateurs système du parent lors de la création de l’organisation enfant** | Lorsque les administrateurs globaux créent des organisations enfants, les administrateurs système du parent deviennent automatiquement les administrateurs système de la nouvelle organisation. Cette politique est *désactivée* défaut. |
| **Gérer les administrateurs** | Permet aux administrateurs globaux de modifier ou de supprimer/modifier les autorisations d’administrateur. |

### Gestion des utilisateurs

| Nom de la stratégie | Description |
| --- | --- |
| **Hériter des utilisateurs des répertoires gérés par l’organisation parent** | Cette politique doit être activée *activée* et active avant de créer l’organisation enfant. Lorsqu’une organisation enfant est créée, les utilisateurs de l’organisation parent sont disponibles en tant qu’utilisateurs dans l’organisation enfant. En d’autres termes, cette politique établit automatiquement une relation de confiance entre le parent et l’enfant lorsque le nouvel enfant est créé dans GAC. Pour les organisations existantes, toute relation de confiance avant d’être ajoutée au GAC restera une fois introduite dans le GAC. S’il n’existe aucune relation d’approbation en place, le processus habituel de demande d’approbation doit être suivi. Pour que cette politique soit efficace, l’administrateur global qui crée la nouvelle organisation doit également être un administrateur système de l’organisation parent avec le domaine revendiqué. Dans le cas contraire, la relation d’approbation de domaine ne sera pas héritée dans l’organisation nouvellement créée. |
| **Ajouter des utilisateurs Adobe ID** | Si cette option est définie, l’organisation ne peut pas ajouter d’utilisateurs de type Adobe ID via Admin Console, l’API User Management (UMAPI) ni aucun mécanisme de synchronisation. |
| **Gérer les groupes d’utilisateurs** | Si cela est autorisé, les administrateurs globaux, système et des groupes d’utilisateurs peuvent créer, modifier et supprimer des groupes d’utilisateurs. |

### Application des répertoires et des domaines

| Nom de la stratégie | Description |
| --- | --- |
| **Demander des domaines** | S’il est défini, les administrateurs système peuvent demander des domaines sur l’Admin Console. |
| **Modifier la configuration d’identité** | S’il est défini, les administrateurs système peuvent modifier le paramétrage de la configuration de l’identité utilisateur sur Admin Console. |

### Attribution du produit

| Nom de la stratégie | Description |
| --- | --- |
| **Gérer les produits** | Permet aux administrateurs globaux d’ajouter ou de supprimer des produits et de modifier les subventions de ressources de produit. |

### Partage de ressources

| Nom de la stratégie | Description |
| --- | --- |
| **L’administrateur du système ou du stockage peut modifier les paramètres de partage des ressources** | Si cela est autorisé, les administrateurs du stockage et du système peuvent modifier les paramètres de partage des ressources, y compris les contacts de sécurité, la politique de mot de passe et la politique de stockage. |
| **Hériter de la politique de partage d’un parent lorsqu’une organisation est créée** | Si cela est autorisé, les paramètres de partage des ressources sont hérités du parent lors de la création d’une organisation enfant. Les paramètres de partage des ressources incluent les contacts de sécurité, la politique de mot de passe et la politique de stockage. Cela s’applique uniquement aux organisations nouvellement créées au moment de leur création. Elle est définie sur un parent et affecte la création des organisations enfants sous ce parent. |
