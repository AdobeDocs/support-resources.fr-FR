---
title: Tableaux
description: Utilisation des tables de balisage et des tables d’HTML.
hide: true
hidefromtoc: true
exl-id: 5ce746fc-6835-4bee-85c5-5ad5176baca0
source-git-commit: 6893d1e41c3899c3ab6a9b02b305161eb3f7e049
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 17%

---

# Tableaux

Matt était là encore et encore.

EDS

Standard Markdown ne prend en charge que les tableaux de base. Pour AdobeDocs Markdown, vous disposez des options suivantes :

* Tableaux Markdown de base
* HTML des tableaux
* Tables Markdown avec une syntaxe d’HTML limitée pour les sauts de paragraphe (`<p>`), les sauts de ligne (`<br>`) et les listes de base (`<ul>`, `<ol>`).

## Conversion de tableaux HTML en tableaux Markdown

Dans certains cas, vous souhaiterez convertir un tableau HTML en tableau Markdown ou en texte Markdown. Vous devrez peut-être améliorer l’aspect, résoudre une erreur de validation ou faciliter la modification à l’avenir.

Malheureusement, nous n’avons pas pu trouver un seul outil qui convertisse correctement les tables d’HTML. Nous utilisons généralement une combinaison d&#39;outils pour assembler une table Markdown correcte.

| Outil | Fonctionnement |
|--- |--- |
| [Générateur de tables Markdown](https://www.tablesgenerator.com/markdown_tables) | C’est une bonne méthode pour créer des tableaux Markdown à partir de zéro. |
| [Convertisseur de table avancé](https://tableconvert.com/html-to-markdown) | Convertissez des tableaux de n’importe quel format. <p>**Remarque :** Les liens et les images sont aplatis lors d&#39;une conversion. |
| [Table de base html > convertisseur du markdown](https://jmalarcon.github.io/markdowntables/) | Convertisseur d’HTMLS simple <p>**Remarque :** Les liens et les images sont aplatis lors d&#39;une conversion. |
| [ HTML non table > convertisseur Markdown](https://codebeautify.org/html-to-markdown) | Convertit les tableaux HTML en syntaxe de balisage non tabulaire. Utilisez en combinaison avec les outils ci-dessus pour copier des liens, des images et tout autre élément aplati. |

## Tableaux Markdown de base

* Veillez à ajouter au moins trois tirets à la deuxième ligne qui déterminent les propriétés du tableau. Exemple : `|--- |--- |--- |` pour un tableau à 3 colonnes.
* Les tableaux Markdown doivent comporter au moins une rangée d’en-tête et une rangée de contenu. Vous ne pouvez pas créer de tableau de balisage d’une ligne ou d’une cellule (utilisez plutôt HTML).
* Assurez-vous que chaque ligne comporte le même nombre de caractères de barre verticale ( &amp;vert; ). Si vous devez inclure une barre verticale dans une cellule d’un tableau, placez-la dans une séquence d’échappement en la précédant avec une barre oblique inverse (`\|`) ou en utilisant le code d’entité d’HTML (`&vert;`).
* Soyez prudent lorsque vous utilisez des blocs de code dans des tableaux. Les blocs de code intégrés peuvent entraîner des largeurs de colonne disproportionnées.
* Vous pouvez modifier le mode de rendu du tableau en spécifiant Auto ou Fixe. Voir [Modification du rendu des tables](#table-rendering).

## Création de tableaux Markdown avec HTML supplémentaire

Pour faciliter la migration, nous avons étendu les tables Markdown afin de prendre en charge les sauts de paragraphe d’HTML (`<p>`), les sauts de ligne (`<br>`) et les listes d’HTMLS de base (`<ul>` et `<ol>`) dans les tables Markdown.

**Table Markdown avec sauts de ligne et listes**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**Exemple**

| En-tête 1 | En-tête 2 | En-tête 3 |
|--- |--- |--- |
| Ligne normale | row 1 column 2 | row 1 column 3 |
| Saut de ligne | première ligne dans la cellule<br>seconde ligne dans la cellule | row 1 column 3 |
| Liste à puces | Liste à puces :<ul><li>Élément 1</li><li>Élément 2</li><li>Élément 3</li></ul> | row 2 column 3 |
| Liste à puces avec saut de ligne | Liste à puces :<ul><li>Élément 1</li><li>Élément 2</li><li>Élément 3</li></ul><br>Il s’agit d’une nouvelle ligne après la liste à puces. | row 2 column 3 |

>[!IMPORTANT]
>
>Si vous décidez d’utiliser l’HTML dans les tables natives, veillez à utiliser la syntaxe d’HTML appropriée. Les erreurs de syntaxe d’HTML génèrent des erreurs de validation difficiles à comprendre. Vérifiez deux fois votre travail.

## Utilisation des tables d’HTMLS

L’outil de migration a essayé de conserver le plus possible de formatage à partir du tableau d’origine. La plupart de cette syntaxe d’HTML est ignorée, tandis que certaines de ces syntaxes génèrent des erreurs de validation.

**Exemple de table d’HTMLS migrée**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**Rendered**

<table> 
 <tbody>
  <tr>
   <th>Propriété</th> 
   <th>Type</th> 
   <th>Valeur Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Obligatoire)</i> Chaîne à plusieurs valeurs d’images de badge jusqu’au nombre de badgingLelevels. Les chemins des images du badge doivent être triés afin que le premier soit attribué au plus haut expert. S’il existe moins de badges qu’indiqué par badgingLelevels, le dernier badge du tableau remplit le reste du tableau. Exemple d’entrée :</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLelevels</td> 
   <td>Long</td> 
   <td><p><i>(Facultatif)</i> Indique les niveaux d’expertise à attribuer. Par exemple, s’il doit y avoir un <code>expert </code> et un <code>almost expert</code> (deux badges), la valeur doit être définie sur 2. Le badgingLevel doit correspondre au nombre d’images de badge associées à un expert répertoriées pour la propriété badgingPath. La valeur par défaut est 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>Chaîne</td> 
   <td><p><i>(Obligatoire)</i> Identifie le moteur de notation comme "de base" ou "avancé". Défini sur "advanced" sinon la valeur par défaut est "basic".</p></td> 
  </tr>
 </tbody>
</table>

**Quand utiliser les tables d&#39;HTML**

* Pour équilibrer les colonnes.
* Pour omettre les en-têtes de tableau (les tableaux de Markdown doivent comporter une rangée d’en-tête).
* Pour supprimer la bordure d’une table d’une ligne (`<tr style="border: 0;">`).
* Pour ajouter des étendues de colonnes ou de lignes.
* Pour aligner le texte dans une cellule d’un tableau.

**Notes pour l’utilisation des tables d’HTML**

* N’utilisez pas la syntaxe Markdown dans les tables d’HTML. Par exemple, si vous ajoutez `[!NOTE]` à une table d’HTML, elle est rendue telle quelle (`[!NOTE]`). Utilisez plutôt la syntaxe des HTMLS pour des annotations et des images.

  Les balises Loc constituent une exception à cette règle, car les balises UICONTROL et DNL sont supprimées avant le rendu des pages.

* La syntaxe des HTMLS n’est pas prise en charge dans tous les tableaux. La largeur, la hauteur, la couleur et d’autres éléments de syntaxe d’HTML sont ignorés lors du rendu dans EXL. Vous pouvez laisser ces valeurs dans à moins qu’elles ne génèrent des erreurs de validation.
* Pour aligner le texte, utilisez `align: "left|center|right"` dans HTML. Par exemple, pour centrer le contenu d’une cellule de tableau, utilisez `<td align="center">`.
* Les tableaux d’HTML ne peuvent pas inclure de tableaux imbriqués.

>[!TIP]
>
>Si vous souhaitez désactiver une bordure pour un tableau d’HTML d’une ligne, utilisez la syntaxe suivante :
>
>```
><table>
><tr style="border: 0;">
>```

## Spécification du mode de rendu des tableaux {#table-rendering}

Nous pouvons générer des tableaux de deux manières différentes :

* **Fixe** (actuellement la valeur par défaut) : comprend des règles personnalisées pour les tables de rendu, y compris les tables d’HTML avec des images. Les tableaux sont rendus en pleine largeur sans défilement, ce qui entraîne parfois un chevauchement de texte.
* **Auto** - Similaire à Markdown (GFM) avec goût Git. Les tableaux sont autorisés à faire défiler, de sorte que le texte ne se chevauche pas.

Dans la plupart des cas, le rendu des tableaux est identique. Cependant, si votre tableau contient du texte qui se chevauche, vous souhaiterez appliquer la balise `auto`. Ou, si le rendu de votre table d’HTML avec cartes d’images n’est pas correct, vous pouvez appliquer la balise `fixed`.

Nous envisageons de remplacer la valeur par défaut `fixed` par `auto`.

## Modification de tableaux Markdown

Si vous souhaitez spécifier le mode de rendu d’un tableau Markdown natif, ajoutez l’une des lignes de syntaxe suivantes APRÈS le tableau, avec des lignes vides avant et après :

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![table-rendering](assets/table-render.png)

### Modification de tableaux d’HTML

Si vous souhaitez spécifier le mode de rendu d’un tableau d’HTML, utilisez l’une des lignes de syntaxe suivantes dans la première ligne du tableau :

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### Quand utiliser Auto ou Fixe

**Texte de chevauchement**

Utilisez `auto` pour les tables contenant de longs blocs de code ou du texte qui entraînent le chevauchement du texte lorsque `fixed` (valeur par défaut) est sélectionné.

*Fixe (Par défaut)*

| Mesure Statistiques | Description | Paramètre de requête d’identifiant |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Nombre total de messages « type » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.range.count** | Nombre total de messages « plage » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.format.count** | Nombre total de messages « format » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.pattern.count** | Nombre total de messages « modèle » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.presence.count** | Nombre total de messages « présence » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.enum.count** | Nombre total de messages « énumération » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |

{style="table-layout:fixed"}

*Auto*

| Mesure Statistiques | Description | Paramètre de requête d’identifiant |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Nombre total de messages « type » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.range.count** | Nombre total de messages « plage » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.format.count** | Nombre total de messages « format » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.pattern.count** | Nombre total de messages « modèle » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.presence.count** | Nombre total de messages « présence » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |
| **timeseries.data.collection.validation.category.enum.count** | Nombre total de messages « énumération » non valides pour un jeu de données ou tous les jeux de données. | Identifiant du jeu de données |

{style="table-layout:auto"}

**HTML des tables avec des images équilibrées**

Utilisez `fixed` pour les tables d’HTML qui nécessitent des images équilibrées qui deviennent déséquilibrées lorsque `auto` est sélectionné. Dans cet exemple, les images ont des tailles identiques, mais la colonne du milieu contient plus de texte.

*Auto*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Workflow pour les pistes d’Adobe</strong></a>
    </div>
    <em>Workflow de modification principal pour les auteurs de piste.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Peu fréquent" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Workflow pour les utilisateurs peu fréquents</strong></a>
    </div>
    <em>Vous n'êtes pas un rédacteur en chef ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validation" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validation</strong></a>
    </div>
    <em> Découvrez comment résoudre les erreurs de validation.</em>
    <br>
  </td>
</tr>
</table>

*Fixe (de plusieurs façons)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Workflow pour les pistes d’Adobe</strong></a>
    </div>
    <em>Workflow de modification principal pour les auteurs de piste.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Peu fréquent" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Workflow pour les utilisateurs peu fréquents</strong></a>
    </div>
    <em>Vous n'êtes pas un rédacteur en chef ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validation" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validation</strong></a>
    </div>
    <em> Découvrez comment résoudre les erreurs de validation.</em>
    <br>
  </td>
</tr>
</table>
