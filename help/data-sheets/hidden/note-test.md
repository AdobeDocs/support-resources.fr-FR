---
description: Connexion au Data Warehouse de widgets - Documentation produit
title: Connexion au Data Warehouse de widgets
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Connexion au Data Warehouse de widgets {#connecting-to-the-widget-data-warehouse}

## Nouveau test

<ol><li>Utilisez la variable `{{name}}`.</li></ol>

<ol><li>Utilisez la variable &location;&location;<code>name</code>&brace;&rbrace;&rbrace; .</li></ol>

## Test imbriqué

**First**

>[!NOTE]
>
>Vous ne pouvez pas supprimer les éléments suivants :
>
>* Les états intégrés Planification, Actuel et Terminé. Vous pouvez mettre à jour leurs noms, modifier leurs couleurs, les verrouiller ou les déverrouiller, mais ils ne peuvent pas être supprimés.
>* Statuts en attente d’approbation pour au moins un objet de votre système.

**Second**

>[!NOTE]
>
>Vous ne pouvez pas supprimer les éléments suivants :
>
>* Les états intégrés Planification, Actuel et Terminé. Vous pouvez mettre à jour leurs noms, modifier leurs couleurs, les verrouiller ou les déverrouiller, mais ils ne peuvent pas être supprimés.
>
>  C&#39;est entre les
>
>* Statuts en attente d’approbation pour au moins un objet de votre système.

## Lien d’accès au widget {#widget-access-link}

Pour accéder à votre entrepôt de données de widgets, vous devez accéder à l’URL spécifique de votre compte de widget.  Vous pouvez trouver ce lien d’accès en vous connectant à Marketo Measure et en suivant les étapes ci-dessous pour accéder à la page d’informations du Data Warehouse.

1. Dans Marketo Measure, en haut de la page, cliquez sur **Mon compte** > **Paramètres**.

   ![](assets/adobe-logo-old.png)

1. Dans le menu de gauche, sous Sécurité, cliquez sur **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. Sur cette page, vous trouverez le lien vers votre entrepôt de données de widgets et votre nom d’utilisateur.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Il s’agit d’un compte en lecture seule disponible pour votre organisation, et pas seulement pour un utilisateur individuel. Tout utilisateur de votre entreprise ayant accès à Marketo Measure peut utiliser ce compte pour se connecter au compte de lecteur du Data Warehouse de widgets.

1. Cliquez sur le lien fourni dans l’URL du widget. Vous accédez alors à la page de connexion du widget où vous saisissez votre nom d’utilisateur et votre mot de passe. _Si vous n&#39;avez pas votre mot de passe, reportez-vous aux étapes ci-dessous pour le réinitialiser_.

   ![](assets/adobe-logo-old.png)

1. Une fois connecté, cliquez sur **Feuilles de calcul** en haut de la page.

   ![](assets/adobe-logo-old.png)

1. Les objets de base de données BIZIBLE_ROI_V3 se trouvent sur le côté gauche de l’écran.  Saisissez l’entrepôt, la base de données et le schéma dans les options de liste déroulante situées en haut de la fenêtre de requête.  Il ne doit y avoir qu’une seule option pour chacune d’elles.  Vous êtes maintenant prêt à exécuter des requêtes dans l’éditeur de requêtes de widgets.

   ![](assets/adobe-logo-old.png)

## Réinitialisation de votre mot de passe {#reset-your-password}

Marketo Measure n’a pas accès à votre mot de passe de connexion de widget.  Si vous devez réinitialiser votre mot de passe, cliquez sur le bouton Réinitialiser le mot de passe dans la page d’informations du Data Warehouse, puis suivez les instructions. Un mot de passe temporaire s’affiche immédiatement dans l’interface utilisateur. Vous serez invité à créer votre propre mot de passe lors de la prochaine connexion à l’entrepôt de données.

>[!NOTE]
>
>* La réinitialisation du mot de passe le réinitialise pour tous les utilisateurs Marketo Measure de votre entreprise, et pas seulement pour l’utilisateur actuellement connecté.
>* Le mot de passe temporaire s’affiche uniquement dans l’interface utilisateur. Un email ne sera pas envoyé.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Connexion à un widget via des outils tiers {#connecting-to-widget-via-third-party-tools}

Vous devrez saisir quelques informations pour connecter votre entrepôt de données de widgets à un outil tiers.

>[!NOTE]
>
>Chaque outil a des exigences de connexion différentes. Il est recommandé de consulter la documentation de l’outil spécifique que vous essayez de connecter.

* **URI** (toujours requis)
   * Il s’agit du nom de domaine du compte de widget.  Elle se trouve dans une partie du lien de connexion du widget.
* **Nom d’utilisateur** (toujours requis)
   * Le nom d’utilisateur est répertorié sur la page d’informations du Data Warehouse dans Marketo Measure.
* **Mot de passe** (toujours requis)
   * Il s’agit du mot de passe que vous définissez la première fois que vous vous connectez à votre compte de widget.  Pour réinitialiser votre mot de passe, consultez les étapes décrites ci-dessus.
* **Nom de la base de données** (pas toujours requis)
   * La base de données est ce qui stocke les données dans le widget. Il s’agit de la ressource de stockage. Le nom de la base de données est répertorié dans la page d’informations du Data Warehouse de Marketo Measure.
* **Nom de l’entrepôt** (pas toujours requis)
   * L’entrepôt est celui qui exécute les requêtes dans le widget. C&#39;est la ressource informatique.  Le nom de l’entrepôt est répertorié sur la page d’informations du Data Warehouse dans Marketo Measure.

  ![](assets/adobe-logo-old.png)

## Partage direct du Data Warehouse de widgets {#widget-data-warehouse-direct-share}

**Conditions**

Pour que Marketo Measure puisse configurer un partage direct vers l’entrepôt de données, vous devez respecter les conditions suivantes.

* Vous disposez de votre propre instance de widget.
* Votre instance de widget se trouve dans la région Azure East US 2 Widget.
* Vous fournissez à Marketo Measure l’identifiant de compte du widget.

**Limites**

Pour que Marketo Measure puisse configurer un partage direct, le compte demandant l’accès doit se trouver dans Azure Est US 2. Nous sommes conscients que Widget offre une solution de réplication de données entre les régions, mais nous ne la prenons pas en charge depuis notre côté, car nous hébergeons uniquement des données dans la région Azure East US 2. Vous pouvez tirer parti de cette fonctionnalité en configurant votre propre instance dans Azure East US 2 et [en répliquant les données entre les régions](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} vers votre instance existante. Cependant, la fonction de réplication des données du widget n’est disponible que sur les tableaux. Par conséquent, pour utiliser cette fonction, vous devez d’abord copier les données de nos vues dans vos propres tableaux.

**Accès au partage**

Une fois que le partage a été créé pour l’identifiant de compte fourni, vous devez effectuer les [étapes de configuration](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} dans votre instance de widget pour accéder aux données.

>[!NOTE]
>
>Vous pouvez choisir le nom de la base de données de votre choix. Vous pouvez attribuer les privilèges à n’importe quelle règle de votre choix, tant qu’elle existe dans votre instance de widget.

* Utilisation du rôle d’administrateur de compte

```
USE ROLE ACCOUNTADMIN
```

* Afficher les partages disponibles (le nom du partage accordé s’affiche)

```
SHOW SHARES
```

* Créer une base de données pour le partage

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Octroi de privilèges sur la base de données partagée

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Pour obtenir des instructions plus détaillées et pour accomplir ces étapes à partir de l’interface utilisateur du widget, reportez-vous à la [documentation du widget directement](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
