---
description: Connexion à Widget Data Warehouse - Documentation du produit
title: Connexion à Widget Data Warehouse
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 4145889fe291e80fa8d295368ead3e0075917e86
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Connexion à Widget Data Warehouse {#connecting-to-the-widget-data-warehouse}

## Nouveau test

Juin 27

<ol><li>Utilisez la variable « {{name}} ».</li></ol>

<ol><li>Utilisez la variable &amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace;.</li></ol>

## Test imbriqué

**First**

>[!NOTE]
>
>Vous ne pouvez pas supprimer les éléments suivants :
>
>* Les états intégrés Planification, En cours et Terminé. Vous pouvez mettre à jour leurs noms, modifier leurs couleurs et les verrouiller ou les déverrouiller, mais ils ne peuvent pas être supprimés.
>* Statuts qui sont en attente d&#39;approbation pour au moins un objet de votre système.

**Second**

>[!NOTE]
>
>Vous ne pouvez pas supprimer les éléments suivants :
>
>* Les états intégrés Planification, En cours et Terminé. Vous pouvez mettre à jour leurs noms, modifier leurs couleurs et les verrouiller ou les déverrouiller, mais ils ne peuvent pas être supprimés.
>
>  C&#39;est entre les deux
>
>* Statuts qui sont en attente d&#39;approbation pour au moins un objet de votre système.

## Lien d’accès au widget {#widget-access-link}

Pour accéder à votre entrepôt de données de widgets, vous devez accéder à l’URL spécifique à votre compte de widgets.  Pour obtenir ce lien d’accès, connectez-vous à Marketo Measure et suivez les étapes ci-dessous pour accéder à la page d’informations de Data Warehouse.

1. Dans Marketo Measure, en haut de la page, cliquez sur **Mon compte** > **Paramètres**.

   ![](assets/adobe-logo-old.png)

1. Dans le menu de gauche, sous Sécurité, cliquez sur **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. Sur cette page, vous trouverez le lien vers votre entrepôt de données Widget et votre nom d&#39;utilisateur.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Il s’agit d’un compte en lecture seule disponible pour votre entreprise et pas seulement pour un utilisateur individuel. Tout utilisateur de votre organisation ayant accès à Marketo Measure peut utiliser ce compte pour se connecter au compte de lecteur Data Warehouse Widget.

1. Cliquez sur le lien fourni dans l’URL du widget pour accéder à la page de connexion du widget, où vous pouvez saisir votre nom d’utilisateur et votre mot de passe. _Si vous ne disposez pas de votre mot de passe, suivez les étapes ci-dessous pour le réinitialiser_.

   ![](assets/adobe-logo-old.png)

1. Une fois connecté, cliquez sur **Feuilles de calcul** en haut de la page.

   ![](assets/adobe-logo-old.png)

1. Les objets de base de données BIZIBLE_ROI_V3 se trouvent sur le côté gauche de l’écran.  Saisissez l’entrepôt de données, la base de données et le schéma dans les options de liste déroulante en haut de la fenêtre de requête.  Il ne doit y avoir qu’une seule option pour chacune.  Vous êtes maintenant prêt à exécuter des requêtes dans l’éditeur de requêtes de widget.

   ![](assets/adobe-logo-old.png)

## Réinitialiser votre mot de passe {#reset-your-password}

Marketo Measure n’a pas accès à votre mot de passe de connexion au widget.  Si vous devez réinitialiser votre mot de passe, cliquez sur le bouton Réinitialiser le mot de passe sur la page d’informations de Data Warehouse, puis suivez les instructions. Un mot de passe temporaire s’affiche immédiatement dans l’interface utilisateur. Vous serez invité à créer votre propre mot de passe lors de votre prochaine connexion à l’entrepôt de données.

>[!NOTE]
>
>* La réinitialisation du mot de passe le réinitialise pour tous les utilisateurs Marketo Measure de votre organisation, et pas seulement pour l’utilisateur actuellement connecté.
>* Nous n’affichons que le mot de passe temporaire dans l’interface utilisateur. Aucun e-mail ne sera envoyé.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Connexion à Widget via des outils tiers {#connecting-to-widget-via-third-party-tools}

Vous devrez saisir quelques informations pour connecter votre entrepôt de données de widgets à un outil tiers.

>[!NOTE]
>
>Chaque outil a des exigences de connexion différentes. Il est recommandé de consulter la documentation de l’outil spécifique que vous essayez de connecter.

* **URI** (toujours requis)
   * Il s’agit du nom de domaine du compte Widget.  Il se trouve dans une partie du lien de connexion du widget.
* **Nom d’utilisateur** (toujours requis)
   * Le nom d’utilisateur est répertorié dans la page d’informations Data Warehouse de Marketo Measure.
* **Mot de passe** (toujours obligatoire)
   * Il s’agit du mot de passe que vous avez défini la première fois que vous vous êtes connecté à votre compte Widget.  Pour réinitialiser votre mot de passe, reportez-vous aux étapes décrites ci-dessus.
* **Nom de la base de données** (pas toujours obligatoire)
   * C’est la base de données qui stocke les données dans Widget. Il s’agit de la ressource de stockage. Le nom de la base de données est répertorié dans la page d’informations Data Warehouse de Marketo Measure.
* **Nom de l’entrepôt de données** (pas toujours obligatoire)
   * C’est l’entrepôt qui exécute les requêtes dans le widget . C&#39;est la ressource informatique.  Le nom de l’entrepôt de données est répertorié dans la page d’informations Data Warehouse de Marketo Measure.

  ![](assets/adobe-logo-old.png)

## Partage direct du widget Data Warehouse {#widget-data-warehouse-direct-share}

**Conditions**

Pour que Marketo Measure puisse configurer un partage direct vers l’entrepôt de données, vous devez répondre aux exigences suivantes.

* Vous disposez de votre propre instance Widget.
* Votre instance de widget se trouve dans la région Azure East US 2 Widget .
* Vous fournissez à Marketo Measure votre identifiant de compte Widget.

**Limites**

Pour que Marketo Measure puisse configurer un partage direct, le compte demandant l’accès doit être situé dans Azure East US 2. Nous savons que Widget offre une solution de réplication des données entre les régions, mais nous ne la prenons pas en charge de notre côté, car nous hébergeons uniquement des données dans la région Azure East US 2. Vous pouvez tirer parti de cette fonctionnalité en configurant votre propre instance dans Azure East US 2 et [en répliquant les données entre les régions](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} vers votre instance existante. Cependant, la fonctionnalité de réplication des données de Widget n’est disponible que sur les tables. Pour utiliser cette fonctionnalité, vous devez donc d’abord copier les données de nos vues dans vos propres tables.

**Accès au partage**

Une fois le partage créé pour l’identifiant de compte fourni, vous devez suivre les [étapes de configuration](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} dans votre instance de widget afin d’accéder aux données.

>[!NOTE]
>
>Vous pouvez choisir le nom de base de données de votre choix. Vous pouvez attribuer les privilèges à n’importe quelle règle de votre choix, à condition qu’elle existe dans votre instance de widget.

* Utiliser le rôle d’administrateur de compte

```
USE ROLE ACCOUNTADMIN
```

* Afficher les actions disponibles (ceci affichera le nom de l&#39;action accordée)

```
SHOW SHARES
```

* Créer une base de données pour le partage

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Octroi de privilèges sur la base partagée

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Pour obtenir des instructions et des étapes plus détaillées pour accomplir ces étapes à partir de l’interface utilisateur du widget, reportez-vous directement à la documentation de [Widget](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
