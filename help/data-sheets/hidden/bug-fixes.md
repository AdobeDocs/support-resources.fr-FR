---
title: Correctifs de bogues (masqué)
description: Page de test à des fins de test interne
hide: true
hidefromtoc: true
source-git-commit: d6b478e07ca1c0525cda103f3b65bec459911508
workflow-type: tm+mt
source-wordcount: '1841'
ht-degree: 27%

---

# Correctifs

## UGP-10584 Les badges intégrés ne fonctionnent pas

Ces badges doivent se trouver sur la même ligne que les éléments de puce.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Remarques]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tableaux]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Guide de style de syntaxe]{type=Positive}

## UGP-10560 - Badges dans les sections réductibles

+++ Versions précédentes

### Version 1.16

_13 février 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Les vidéos de produit sont désormais prises en charge par l’API Catalog Service.
![Correction](assets/package.png) Les produits groupés avec des prix fixes sont désormais pris en charge.
![Correction](assets/package.png) Les options en rupture de stock s’affichent désormais dans le widget PDP.

#### Limites connues

Ces fonctionnalités ne sont pas encore prises en charge :

* La taille maximale de la charge utile des attributs dynamiques est de 9 Mo.
* Prix du produit de groupe. Peuvent être calculées avec des prix de produit simples.
* Dans un tableau d’images, seule la première image contient des rôles.

Les limites suivantes peuvent être résolues à l’aide du maillage de l’API et de l’API Core GraphQL :

* Prix publicitaire minimal
* [Prix de niveau](https://www.adobe.com)

### Version 1.13

_vendredi 12 octobre 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Le service de catalogue prend en charge la variable `inStock` Indicateur pour les variantes de produits.
![Nouveau](assets/package.png) `urlKey` et `externalId` ont été ajoutés au schéma GraphQL.
![Nouveau](assets/package.png) Les produits téléchargeables et les cartes-cadeaux sont désormais pris en charge.

### Version 1.12

_mercredi 19 septembre 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](https://www.adobe.com).
![Correction](assets/package.png) Cette version contient des correctifs et des améliorations du côté service.

### Version 1.11

_mercredi 18 juillet 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Le service de catalogue prend désormais en charge la variable [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) Requête GraphQL pour le Recommendations de produit.

### Version 1.10

_mercredi 27 juin 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) L’API Catalog Service prend désormais en charge les &quot;produits associés&quot;.

### Version V1.7

_jeudi 12 avril 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Le service de catalogue nettoie désormais les variantes de produits supprimées.
![Correction](assets/package.png) Évolutivité de l’infrastructure et améliorations des performances.

### Version V1.6

_mercredi 28 mars 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Ajout d’échantillons aux [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) requête.
![Nouveau](https://www.adobe.com).

### Version V1.5

_mardi 6 mars 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Ajout [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) Fonctionnalité de GraphQL.
![Correction](assets/package.png) Amélioration des performances et de l’évolutivité des API.

### Version V1.4

_mercredi 7 février 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Mise en page du métaphorage du service de catalogue pour simplifier les étapes d’installation.
![Correction](assets/package.png) Améliorations de l’évolutivité et des performances des API.

### Version V1.3

_mercredi 17 janvier 2023_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Simplification et amélioration de l’intégration.
![Nouveau](assets/package.png) De nouveaux points de terminaison d’environnement de test client sont disponibles pour les tests de pré-production.
![Nouveau](assets/package.png) Ajout de la prise en charge des produits virtuels
![Correction](assets/package.png) Améliorations de l’évolutivité et des performances des API.

### Version V1.1

_samedi 18 novembre 2022_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Le service de catalogue prend désormais en charge les Adobes [Mesh de l’API](https://developer.adobe.com/graphql-mesh-gateway/).
![Correction](assets/package.png) Amélioration de l’évolutivité des API et des performances globales.

### Version V1.0

_mercredi 4 octobre 2022_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Prise en charge des produits regroupés et regroupés.
![Nouveau](assets/package.png) Ajout de remplacements de visibilité B2B. Les produits peuvent désormais faire l’objet de recherches et peuvent être ajoutés au panier pour des groupes de clients spécifiques.
![Correction](assets/package.png) Le service est désormais plus stable et offre de meilleures performances.

### Version 0.3 - Bêta+

_mardi 12 septembre 2022_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) Prise en charge des images pour les variantes : les images de produit sont renvoyées en fonction des options sélectionnées.
![Nouveau](assets/package.png) Rôles de prise en charge des prix : permettent uniquement aux membres de groupes de clients spécifiques de voir le prix des produits.
![Correction](assets/package.png) Stabilité et performances améliorées du service
![Nouveau](assets/package.png) Des mises à jour sont reçues lorsque des produits sont supprimés du catalogue.

### Version bêta

_9 août 2022_

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](assets/package.png) La variable `products` et `refineProduct` les requêtes renvoient les données suivantes :

* Attributs de produit prédéfinis (système).
* Attributs de produit dynamiques et filtrez-les par rôle (page d’affichage de produit/page de liste de produits).
* Options du produit.
* Images de produit et filtrez-les par rôle (PDP/PLP).
* Un prix spécifique pour les produits simples et des plages de prix pour les produits configurables.
* Prix des groupes clients et plages de prix. Ils renvoient un prix par défaut de secours aux acheteurs sans groupe de clients.
* Types de produits qui utilisent la tarification spécifique aux clients B2B.

+++

## [!BADGE Obsolète]{type=negative}

Voir l’en-tête ci-dessus. Et la suivante.

## Test de l’activation automatique

J&#39;ai ajouté ceci vendredi après-midi, mais je n&#39;ai pas cliqué sur Publier maintenant.

### [!BADGE Version bêta]{type=Informative}

Bob

## UGP-10565 - Mise en surbrillance de texte

Texte avant `<div class="preview">`

<div class="preview">

### Ajout de champs natifs Workfront

Vous pouvez ajouter des champs natifs Workfront à vos formulaires personnalisés. Lorsque le formulaire personnalisé est associé à un objet, le champ est renseigné à partir des données de l’objet. Par exemple, le champ Description d’un formulaire personnalisé joint à un projet extrait la description du projet. (Le champ peut afficher &quot;S.O.&quot; si aucune donnée n’est disponible.)

1. Dans la partie gauche de l’écran, recherchez **Champ natif** et faites-le glisser vers une section de la zone de travail.
1. Dans la partie droite de l’écran, configurez les options du champ personnalisé :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Libellé</td> 
      <td> <p>(Obligatoire) Saisissez un libellé descriptif à afficher au-dessus du champ. Vous pouvez modifier le libellé à tout moment.</p> <p><b>IMPORTANT</b>: évitez d’utiliser des caractères spéciaux dans ce libellé. Elles ne s’affichent pas correctement dans les rapports.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nom</td> 
      <td> <p>(Obligatoire) Ce nom est la manière dont le système identifie le champ.</p><p> Lorsque vous configurez le champ pour la première fois et que vous saisissez le libellé, le champ Nom est automatiquement renseigné pour qu’il corresponde. Mais les champs Libellé et Nom ne sont pas synchronisés, ce qui vous donne la possibilité de modifier le libellé que vos utilisateurs voient sans avoir à modifier le nom que le système voit.</p>
      <p><b>IMPORTANT</b>:
      <ul> 
      <li>Bien qu’il soit possible de le faire, nous vous recommandons de ne pas modifier ce nom une fois que vous ou d’autres utilisateurs aurez commencé à utiliser le formulaire personnalisé dans Workfront. Si vous le faites, le système ne reconnaîtra plus le champ où il peut maintenant être référencé dans d’autres zones de Workfront.</p> </li>
      <li> <p>Chaque nom de champ doit être unique dans l’instance Workfront de votre entreprise. Ainsi, vous pouvez réutiliser un formulaire déjà créé pour un autre formulaire personnalisé.</p> </li>
      <li><p>Il est recommandé de ne pas utiliser le caractère point/point dans le nom du champ personnalisé afin d’éviter toute erreur lors de l’utilisation du champ dans différentes zones de Workfront.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Instructions</td> 
      <td> <p>Saisissez des informations supplémentaires sur le champ. Lorsque les utilisateurs remplissent le formulaire personnalisé, ils peuvent placer le pointeur de la souris sur l’icône de point d’interrogation pour afficher une info-bulle contenant les informations saisies ici.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Champ de référence</td> 
      <td><p>(Obligatoire) Sélectionnez un champ natif Workfront.<p><p>Seuls les champs natifs des objets de formulaire sont disponibles. Par exemple, si la liste Types d’objet située en haut du concepteur de formulaire affiche Projet, vous pouvez sélectionner des champs natifs pour les projets, mais pas des champs spécifiques aux tâches.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Taille</td> 
      <td>(Facultatif) Modifiez la taille d’affichage du champ selon vos besoins.</td> 
     </tr> 
    </tbody> 
   </table>

1. Pour enregistrer vos modifications, cliquez sur **Appliquer** et passez à une autre section pour continuer à créer votre formulaire.

   ou

   Cliquez sur **Enregistrer et fermer**.

</div>

Texte après mise en surbrillance

## UGP-10566 - Le texte du lien est plus petit que le texte normal dans les tableaux de HTML.

Voir aussi UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>Entrée dans</td>
<td>Description</td>
<td>Disponible pour </td>
</tr>
<tr> 
    <td role="rowheader">Libellé</td> 
    <td> <p>(Obligatoire) Saisissez un libellé descriptif à afficher au-dessus du champ personnalisé. Vous pouvez modifier le libellé à tout moment. Pour plus d’informations, voir <a href="https://www.adobe.com" class="MCXref xref">Ajouter un champ personnalisé à un formulaire personnalisé</a> dans cet article.</p> <p><b>IMPORTANT</b>: évitez d’utiliser des caractères spéciaux dans ce libellé. Elles ne s’affichent pas correctement dans les rapports.</p> </td> 
    <td>
    <ul>
    <li>Boutons radio. Pour plus d’informations, voir <a href="https://www.adobe.com">Ajouter un champ personnalisé à un formulaire personnalisé</a> dans cet article. (Aucune classe)</li>
    <li>Groupe de cases à cocher</li>
    <li>Liste déroulante</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Ancien bogue

La balise &quot;span&quot; ne fonctionne pas très bien dans une REMARQUE (et une liste).

Pour plus d’informations sur les fonctionnalités disponibles dans la nouvelle expérience de commentaire et sur les objets, voir [Nouvelle expérience de commentaire](note-test.md).

1. Accédez à l’objet auquel vous souhaitez ajouter une réponse.
1. Cliquez sur **Mises à jour**, puis cliquez sur le bouton **Commentaires** pour l’objet et recherchez le commentaire ou la réponse à laquelle vous souhaitez répondre.

   Ou

   <span class="preview">Cliquez sur le bouton **Tous** , puis cliquez sur **Réponse aux commentaires** pour ouvrir le commentaire dans l’onglet Commentaires et y répondre. Vous ne pouvez pas répondre dans l’onglet Tout .</span>

1. (Facultatif) Pour inclure le texte d’une mise à jour précédente dans votre réponse, cliquez sur le bouton **Plus** dans le coin supérieur droit du commentaire auquel vous souhaitez répondre, puis cliquez sur **Réponse entre guillemets**. Le texte de la mise à jour précédente apparaît dans la zone de saisie, marquée d’une ligne grise verticale.
1. Cliquez sur **Répondre**.

   ![](assets/package.png)

   Vous pouvez voir les utilisateurs qui participent activement à la conversation en bas de la page **Ajouter une réponse...** et vous pouvez ajouter d’autres éléments ou supprimer ceux qui ne sont plus pertinents. Ces utilisateurs, ainsi que tous les utilisateurs abonnés à l’objet, reçoivent une notification chaque fois qu’une mise à jour ou une réponse est apportée à l’objet. Vous pouvez également baliser d’autres utilisateurs pour les inclure dans votre réponse.  Pour baliser davantage d’utilisateurs, voir [Balisage des autres sur les mises à jour](note-test.md).

   >[!TIP]
   >
   >   Pour ajouter des réponses supplémentaires à une réponse existante, vous pouvez commencer à saisir dans la variable **Ajouter une réponse ...** ou cliquez sur **Répondre** sur le commentaire original. Votre réponse est ajoutée à la fin du thread.

1. Commencez à saisir votre réponse et utilisez toutes les options supplémentaires de la barre d’outils Texte enrichi. Pour plus d’informations sur l’utilisation du texte enrichi ou d’autres fonctionnalités de mise à jour, voir [Mise à jour du travail](note-test.md).

1. Cliquez sur **Envoyer** pour enregistrer la réponse.

1. (Facultatif) Cliquez sur le **Plus** dans le coin supérieur droit du commentaire auquel vous souhaitez répondre pour plus d’options de gestion de la réponse. Pour plus d’informations, voir [Mise à jour du travail](note-test.md).


## UGP-10614 - Tables problématiques avec les images

Je pense que la `{width="20"}` pose des problèmes dans les tables.

## Comparaison des plans d’assistance Expert et Ultimate

|  | Plan d’assistance Expert | Plan d’assistance Ultimate |
|--- |--- |--- |
|  | Grâce au plan d’assistance Expert, vous pouvez accéder à l&#39;**assistance dʼexpertes et d’experts 24h/24 et 7j/7** pour obtenir des conseils techniques et des solutions sur les problèmes critiques de votre entreprise. Vous pouvez également trouver des solutions rapides en accédant à nos ressources autoguidées, à nos bonnes pratiques exclusives ainsi qu’à une communauté en ligne d’expertes et d’experts et de pairs d’Adobe. <p> *Inclus avec toutes les licences Adobe Experience Cloud* | Grâce au plan d’assistance Ultimate, vous obtiendrez des **conseils stratégiques et une assistance technique proactive pour offrir des expériences numériques hautement performantes**. Votre environnement Adobe sera pris en charge par une équipe d’expertes et experts qui connaissent bien votre activité et qui se concentrent sur l’exécution d’une feuille de route alignée sur vos objectifs et vos priorités pour un meilleur impact commercial. |
| **Équipe d’assistance** | Équipe d’ingénieurs d’assistance regroupés | Inclut : <ul><li> Gestionnaire de compte technique désigné </li><li> Gestionnaire de succès client désigné </li><li> Gestionnaire des services d’assistance désigné</li><li> Ensemble d’ingénieurs techniques et d’expertes et experts stratégiques fournissant des accélérateurs de succès </li><li> Équipe d’ingénieurs d’assistance regroupés </li></ul> |
| **Support technique et opérationnel proactif** | ![icône Non inclus](../assets/Cross_red_circle.svg){width="20"} Non inclus | Inclut : <ul><li>Études de mise à niveau et de migration, préparation des versions </li><li>Études de feuilles de route du produit</li><li> Alignement des feuilles de route techniques et stratégiques</li><li>Préparation et planification d’événements clés</li><li>Planification d’une activation pertinente et opportune</li><li>Bonnes pratiques techniques et conseils du secteur</li><li>Promotion/alignement avec les équipes produits</li><li>Plan unifié pour atteindre les principaux objectifs commerciaux - Plan d’action mutuel (PAM)</li></ul> |
| **Assistance technique** | Inclut : <ul><li>**P1** : prise en charge des problèmes 24 h/24, 7 j/7</li><li>**P2, P3, P4** : service d’assistance pendant les heures de bureau</li><li>Gestion des pannes standard</li><li>Gestion des réaffectations groupées</li></ul> | Inclut : <ul><li>**P1** : prise en charge des problèmes 24 h sur 24 et 7 j sur 7</li><li>**P2/P3** : prise en charge des problèmes 24 heures sur 24 et 5 jours sur 7</li><li>**P4** : service d’assistance pendant les heures de bureau</li><li>Gestion prioritaire des pannes</li><li>Gestion de la réaffectation par un expert ou une experte désigné(e)</li></ul> |
| **Accélérateurs de succès** | ![icône Non inclus](../assets/Cross_red_circle.svg){width="20"} Non inclus | Accélérateurs de succès planifiés régulièrement par le TAM et le CSM<p>*(voir Catalogue des accélérateurs de succès pour plus d’informations)* |
| **Canaux d’assistance** | En ligne, téléphone, Experience League, forums | Portail en ligne personnalisé, ligne téléphonique prioritaire, Experience League, forums |

{style="table-layout:fixed"}

## Modules complémentaires d’assistance

| Modules complémentaires | Plan d’assistance Expert | Plan d’assistance Ultimate |
|--- |--- |--- |
| **Module complémentaire de gestion des événements**<br> Fournit un leadership et une assistance de bout en bout nécessaires à la gestion de l’ensemble du cycle de vie des événements clés. | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icône disponible](../assets/Plus_blue.svg){width="20"} Disponible |
| **Module complémentaire Directeur/directrice du compte technique**<br> Votre principale ressource technique qui assure la supervision du leadership, gère l’engagement des dirigeants et dirigeantes et assure la gouvernance pour optimiser les résultats commerciaux. | ![icône Non disponible](../assets/Cross_red_circle.svg){width="20"} Non disponible | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible |
| **Module complémentaire Assistance cloud avancée**<br> Assistance et assurance basée sur la valeur de premier ordre pour les clients et clientes d’Adobe Experience Manager as a Cloud Service. | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible |
| **Module complémentaire Sessions de mentors**<br> Dispense des formations basées sur les compétences selon une méthode de formation Juste à temps. | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icône Disponible](../assets/green_checkmark.svg){width="20"} Inclus |
| **Module complémentaire Coup de pouce aux développeurs et développeuses**<br> Permet d’accéder à des experts et expertes en ingénierie de terrain pouvant aider à résoudre les problèmes. | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icône Inclus](../assets/green_checkmark.svg){width="20"} Inclus |
| **Module complémentaire du lot de file d’attente de priorité**<br> Coupez la file d’attente pour que vos tickets soient traités en premier et bénéficiez d’un accès supplémentaire aux Sessions de mentors et Coups de pouce aux développeurs et développeuses | ![icône Disponible](../assets/Plus_blue.svg){width="20"} Disponible | ![icône Inclus](../assets/green_checkmark.svg){width="20"} Inclus |

{style="table-layout:fixed"}
