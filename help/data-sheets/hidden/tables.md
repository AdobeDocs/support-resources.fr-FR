---
title: Tableaux
description: Utilisation des tableaux Markdown et HTML.
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 18%

---

# Tableaux

Matt était là encore et encore

Standard Markdown ne prend en charge que les tableaux de base. Pour AdobeDocs Markdown, vous disposez des options suivantes :

* Tableaux Markdown de base
* Tables de HTMLs
* Tableaux Markdown avec une syntaxe de HTML limitée pour les sauts de paragraphe (`<p>`), sauts de ligne (`<br>`), et les listes de base (`<ul>`, `<ol>`).

## Conversion de tableaux de HTML en tableaux Markdown

Dans certains cas, vous souhaiterez convertir un tableau HTML en tableau Markdown ou en texte Markdown. Vous devrez peut-être améliorer l’aspect, résoudre une erreur de validation ou faciliter la modification à l’avenir.

Malheureusement, nous n’avons pas pu trouver un seul outil qui convertisse correctement les tableaux de HTML. Nous utilisons généralement une combinaison d&#39;outils pour assembler une table Markdown correcte.

| Outil | Effets |
|--- |--- |
| [Générateur de tableaux Markdown](https://www.tablesgenerator.com/markdown_tables) | C’est une bonne méthode pour créer des tableaux Markdown à partir de zéro. |
| [Convertisseur de tableau avancé](https://tableconvert.com/html-to-markdown) | Convertissez des tableaux de n’importe quel format. <p>**Remarque :** Les liens et les images sont aplatis lors de la conversion. |
| [Tableau de base html > convertisseur du markdown](https://jmalarcon.github.io/markdowntables/) | Convertisseur de HTML simple <p>**Remarque :** Les liens et les images sont aplatis lors de la conversion. |
| [HTML non tableau > convertisseur Markdown](https://codebeautify.org/html-to-markdown) | Convertit les tableaux de HTML en syntaxe de balisage non tabulaire. Utilisez en combinaison avec les outils ci-dessus pour copier des liens, des images et tout autre élément aplati. |

## Tableaux Markdown de base

* Veillez à ajouter au moins trois tirets à la deuxième ligne qui déterminent les propriétés du tableau. Exemple : `|--- |--- |--- |` pour un tableau à 3 colonnes.
* Les tableaux Markdown doivent comporter au moins une rangée d’en-tête et une rangée de contenu. Vous ne pouvez pas créer de tableau de balisage d’une ligne ou d’une cellule (utilisez plutôt HTML).
* Assurez-vous que chaque ligne comporte le même nombre de caractères de barre verticale ( &amp;vert; ). Si vous devez inclure une barre verticale dans une cellule d’un tableau, placez-la en séquence d’échappement en la précédant avec une barre oblique inverse (`\|`) ou à l’aide du code d’entité de HTML (`&vert;`).
* Soyez prudent lorsque vous utilisez des blocs de code dans des tableaux. Les blocs de code intégrés peuvent entraîner des largeurs de colonne disproportionnées.
* Vous pouvez modifier le mode de rendu du tableau en spécifiant Auto ou Fixe. Voir [Modification du rendu des tableaux](#table-rendering).

## Création de tableaux Markdown avec HTML bonus

Pour faciliter la migration, nous avons étendu les tableaux Markdown afin de prendre en charge les sauts de paragraphe de HTML (`<p>`), sauts de ligne (`<br>`) et les listes de HTMLS de base (`<ul>` et `<ol>`) dans les tableaux Markdown.

**Tableau Markdown avec sauts de ligne et listes**

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
| Saut de ligne | première ligne dans la cellule<br>2e ligne dans la cellule | row 1 column 3 |
| Liste à puces | Liste à puces :<ul><li>Élément 1</li><li>Élément 2</li><li>Élément 3</li></ul> | row 2 column 3 |
| Liste à puces avec saut de ligne | Liste à puces :<ul><li>Élément 1</li><li>Élément 2</li><li>Élément 3</li></ul><br>Nouvelle ligne après la liste à puces | row 2 column 3 |

>[!IMPORTANT]
>
>Si vous décidez d’utiliser le HTML dans les tables natives, veillez à utiliser la syntaxe de HTML appropriée. Les erreurs de syntaxe des HTMLS génèrent des erreurs de validation difficiles à comprendre. Vérifiez deux fois votre travail.

## Utilisation des tables de HTMLS

L’outil de migration a essayé de conserver le plus possible de formatage à partir du tableau d’origine. La plupart de cette syntaxe de HTML est ignorée, tandis que certaines de ces syntaxes génèrent des erreurs de validation.

**Exemple de tableau de HTMLS migrés**

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

**Généré**

<table> 
 <tbody>
  <tr>
   <th>Propriété</th> 
   <th>Type</th> 
   <th>Valeur Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>Chaîne[]</td> 
   <td><p><i>(Obligatoire)</i> Chaîne à plusieurs valeurs d’images de badge jusqu’au nombre de badgingLelevels. Les chemins des images du badge doivent être triés afin que le premier soit attribué au plus haut expert. S’il existe moins de badges qu’indiqué par badgingLelevels, le dernier badge du tableau remplit le reste du tableau. Exemple d’entrée :</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLelevels</td> 
   <td>Long</td> 
   <td><p><i>(Facultatif)</i> Indique les niveaux d’expertise à attribuer. Par exemple, si une variable <code>expert </code>et un <code>almost expert</code> (deux badges), alors la valeur doit être définie sur 2. Le badgingLevel doit correspondre au nombre d’images de badge associées à un expert répertoriées pour la propriété badgingPath. La valeur par défaut est 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>Chaîne</td> 
   <td><p><i>(Obligatoire)</i> Identifie le moteur de notation comme "de base" ou "avancé". Défini sur "advanced" sinon la valeur par défaut est "basic".</p></td> 
  </tr>
 </tbody>
</table>

**Quand utiliser les tableaux de HTML**

* Pour équilibrer les colonnes.
* Pour omettre les en-têtes de tableau (les tableaux de Markdown doivent comporter une rangée d’en-tête).
* Pour supprimer la bordure d’un tableau d’une ligne (`<tr style="border: 0;">`).
* Pour ajouter des étendues de colonnes ou de lignes.
* Pour aligner le texte dans une cellule d’un tableau.

**Remarques relatives à l’utilisation des tables de HTMLS**

* N’utilisez pas la syntaxe Markdown dans les tables de HTML. Par exemple, si vous ajoutez `[!NOTE]` dans un tableau HTML, il est rendu tel quel (`[!NOTE]`). Utilisez plutôt la syntaxe des HTMLS pour des annotations et des images.

  Les balises Loc constituent une exception à cette règle, car les balises UICONTROL et DNL sont supprimées avant le rendu des pages.

* La syntaxe des HTMLS n’est pas prise en charge dans tous les tableaux. La largeur, la hauteur, la couleur et d’autres éléments de syntaxe de HTML sont ignorés lors du rendu dans EXL. Vous pouvez laisser ces valeurs dans à moins qu’elles ne génèrent des erreurs de validation.
* Pour aligner le texte, utilisez `align: "left|center|right"` en HTML. Par exemple, pour centrer le contenu d’une cellule de tableau, utilisez `<td align="center">`.
* Les tableaux de HTML ne peuvent pas inclure de tableaux imbriqués.

>[!TIP]
>
>Si vous souhaitez désactiver une bordure pour un tableau de HTML d’une ligne, utilisez la syntaxe suivante :
>
>```
><table>
><tr style="border: 0;">
>```

## Spécification du mode de rendu des tableaux {#table-rendering}

Nous pouvons générer des tableaux de deux manières différentes :

* **Fixe** (actuellement la valeur par défaut) : inclut des règles personnalisées pour les tableaux de rendu, y compris les tableaux de HTML avec des images. Les tableaux sont rendus en pleine largeur sans défilement, ce qui entraîne parfois un chevauchement de texte.
* **Auto** - Semblable à Git-Flavored Markdown (GFM). Les tableaux sont autorisés à faire défiler, de sorte que le texte ne se chevauche pas.

Dans la plupart des cas, le rendu des tableaux est identique. Cependant, si le texte du tableau se chevauche, vous souhaiterez appliquer la variable `auto` balise . Ou, si le rendu de votre tableau de HTML avec cartes d’image n’est pas correct, vous pouvez appliquer l’événement `fixed` balise .

Nous envisageons de modifier la valeur par défaut de `fixed` to `auto`.

## Modification de tableaux Markdown

Si vous souhaitez spécifier le mode de rendu d’un tableau Markdown natif, ajoutez l’une des lignes de syntaxe suivantes APRÈS le tableau, avec des lignes vides avant et après :

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![rendu de tableau](assets/table-render.png)

### Modification de tableaux de HTML

Si vous souhaitez spécifier le mode de rendu d’un tableau de HTML, utilisez l’une des lignes de syntaxe suivantes dans la première ligne du tableau :

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

Utilisation `auto` pour les tableaux contenant de longs blocs de code ou du texte qui entraînent le chevauchement de texte lorsque `fixed` (valeur par défaut) est sélectionné.

*Fixe (par défaut)*

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

**Tables de HTML avec images équilibrées**

Utilisation `fixed` pour les tableaux de HTML qui nécessitent des images équilibrées qui deviennent déséquilibrées lorsque `auto` est sélectionnée. Dans cet exemple, les images ont des tailles identiques, mais la colonne du milieu contient plus de texte.

*Auto*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Prospect" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Workflow pour les pistes d’Adobe</strong></a>
    </div>
    <em>Processus de modification principal pour les auteurs de piste.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Peu fréquent" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Processus pour les utilisateurs peu fréquents</strong></a>
    </div>
    <em>Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validation" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validation</strong></a>
    </div>
    <em>Découvrez comment résoudre les erreurs de validation.</em>
    <br>
  </td>
</tr>
</table>

*Corrigé (de plusieurs façons)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Prospect" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Workflow pour les pistes d’Adobe</strong></a>
    </div>
    <em>Processus de modification principal pour les auteurs de piste.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Peu fréquent" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Processus pour les utilisateurs peu fréquents</strong></a>
    </div>
    <em>Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions. Pas un écrivain de premier plan ? Découvrez les moyens les plus simples d’effectuer des contributions.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validation" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validation</strong></a>
    </div>
    <em>Découvrez comment résoudre les erreurs de validation.</em>
    <br>
  </td>
</tr>
</table>
