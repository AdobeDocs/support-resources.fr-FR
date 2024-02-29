---
title: Page de test masquée
description: Cette page est masquée de la recherche et de la table des matières.
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Télécharger Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# Page de test masquée

Souhaitez-vous l’activer ? Nouvel envoi vers 15 h 10. Sera-t-il activé à 15 h 30 ?

## Boutons

[Valeur par défaut du bouton](https://www.adobe.com/)

**[Principal de bouton](https://www.adobe.com/)**

_[Bouton Secondaire](https://www.adobe.com/)_

**_[Bouton Tertiaire](https://www.adobe.com/)_**

## Problème de prévisualisation

Le rendu du paragraphe suivant échoue dans la prévisualisation VSC. Je ne connais pas la raison.

Si votre mot de passe est géré par [!DNL Adobe], vous pouvez [modifier le mot de passe dans votre compte Adobe](https://helpx.adobe.com/fr/manage-account/using/change-or-reset-password.html){target="_blank"}.

## Types de notes

Tous les types de notes pris en charge.

>[!NOTE]
>
>Il s’agit d’un bloc NOTE standard.

>[!TIP]
>
>Il s’agit d’un conseil standard.

>[!IMPORTANT]
>
>Il s’agit d’une note importante.

>[!WARNING]
>
>Il s’agit d’un avertissement.

>[!CAUTION]
>
>Il s’agit d’une mise en garde.

>[!ADMIN]
>
>Il s’agit d’une note de l’administrateur ou de l’administratrice qui s’affiche en tant qu’ADMINISTRATION. EXL uniquement.

>[!AVAILABILITY]
>
>Il s’agit d’une note de disponibilité. EXL uniquement.

>[!PREREQUISITES]
>
>Il s’agit d’une note de conditions préalables. EXL uniquement.

>[!INFO]
>
>Il s’agit d’une note d’information. EXL uniquement.

>[!ERROR]
>
>Il s’agit d’une note d’erreur. EXL uniquement.

>[!SUCCESS]
>
>Il s’agit d’une note de succès. EXL uniquement.

>[!MORELIKETHIS]
>
>* Page 1
>* Page 2

## Badges

Un badge est un libellé coloré utilisé comme indicateur de contenu. Par exemple, vous pouvez ajouter un badge pour marquer un article en version _Bêta_ ou une section _Premium_. Vous pouvez modifier la couleur d’un badge et associer une URL et une info-bulle.

[!BADGE Exemple de badge]

Il existe deux types of de badges, chacun avec une syntaxe différente :

* **Métadonnées** : affiche le badge près du haut d’une page.
* **Intégré** : affiche le badge là où la syntaxe se trouve.

### Badges de métadonnées

L’ajout de la syntaxe du badge dans les métadonnées place un badge au-dessus du titre de la page (H1) dans l’article.

Vous pouvez nommer des badges en utilisant par exemple _badge1_ ou _badge2_. Vous pouvez laisser parler votre créativité (à condition que le nom commence par _badge_).

Exemples de métadonnées :

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium :** cet exemple affiche un badge Premium avec une URL et une info-bulle.

* **badgeExam :** cet exemple affiche un badge sombre avec un numéro d’ID d’examen.

#### Badges intégrés

Indiquez les informations du badge sur sa propre ligne ou dans un en-tête, un tableau ou un autre élément de page.

Voici la syntaxe d’un badge intégré avec un libellé bêta, une couleur bleue, une URL et une info-bulle :

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### Couleurs de badge disponibles

Les badges utilisent des couleurs définies dans Adobe Spectrum :

| Type | Badge |
|---|---|
| Informatif (par défaut) | [!BADGE Version bêta]{type=Informative url="https://www.example.com"} |
| Positif | [!BADGE Nouvelle fonctionnalité]{type=Positive url="https://www.example.com" tooltip="Go to example.com"} |
| Négatif | [!BADGE Arrêté]{type=negative tooltip="Cette fonctionnalité est maintenant en fin de vie"} |
| Neutre | [!BADGE Peut-être]{type=tooltip neutre="Un cavalier est tombé du cheval..."} |
| Attention | [!BADGE Attention]{type=Caution tooltip="État jaune"} |

Exemples de syntaxe

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### Conditions requises pour les badges

* Seuls deux badges sont autorisés dans les métadonnées. Cette règle est configurable. Indiquez-nous donc si vous avez besoin d’une exception.
* Seul le libellé du badge est requis. Les paramètres `type`, `url` et `tooltip` sont facultatifs. Le paramètre `type` détermine la couleur. Le paramètre `url` permet aux utilisateurs et aux utilisatrices de cliquer sur le badge pour ouvrir un article ou une page. Le paramètre `tooltip` affiche le texte de l’info-bulle lorsque vous passez dessus.
* Ajouter un badge au fichier `TOC.md` affiche le badge sur chaque article du guide. Si vous spécifiez une URL pour le badge afin d’accéder à un article, veillez à utiliser un lien racine (par exemple, `/help/guide/article.md`) et non un lien relatif (par exemple, `article.md`) pour tenir compte des articles dans différents dossiers.
* Ajouter un badge à `metadata-new.md` affiche le badge sur chaque article dans un référentiel.
* Pour les badges de métadonnées, assurez-vous que toutes les valeurs sont comprises entre des guillemets. Pour les badges intégrés, assurez-vous que l’`url` et l’`tooltip` sont comprises entre des guillemets.
* Les valeurs de type valides incluent : *Informatif* (par défaut, bleu), *Positif* (vert), *Négatif* (rouge), *Neutre* (gris foncé) et *Attention* (jaune).
* Les libellés de badge sont localisés.
* Si plusieurs badges de métadonnées sont spécifiés, ils s’affichent par ordre alphabétique en fonction du nom du badge, comme `badge1:` ou `badgeWeb`.
* Si vous souhaitez que l’URL s’ouvre dans un nouvel onglet, utilisez la syntaxe suivante :

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  Rendu :

  [!BADGE Ouvrir dans un nouvel onglet]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Ouvrir adobe.com dans un nouvel onglet"}

## Surbrillance du texte

L’équipe Workfront a demandé à pouvoir utiliser la mise en surbrillance jaune pour indiquer l’aperçu des fonctionnalités à venir. Voilà comment cela fonctionne.

Exemple 1 :

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Rendu :

Ce paragraphe entier ne doit PAS être mis en surbrillance. <span class="preview">Ce mot est en **gras** dans une phrase surlignée.</span>Et ceci n’est que la dernière phrase.

Exemple 2 :

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

Rendu :

La mise en surbrillance doit commencer après ce paragraphe.

<div class="preview">

Début de DIV.

Il s’agit d’un nouveau paragraphe, puis d’une image.

![Image.](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Dernier élément en surbrillance.

</div>

Aucune mise en surbrillance

## Mise en surbrillance de syntaxe pour les blocs de code

Experience League prend en charge la mise en surbrillance de la syntaxe pour les blocs de code. Veillez à spécifier un langage tel que `java` après avoir placé un ensemble d’accents graves pour vous assurer que la syntaxe est correctement mise en surbrillance. Pour obtenir la liste des langages valides, consultez [https://prismjs.com](https://prismjs.com/#supported-languages). Si vous ne trouvez pas certains langages, veuillez soumettre un ticket jira.

### Numérotation des lignes dans les blocs de code

Ajoutez `{line-numbers="true"}` après le langage pour activer la numérotation des lignes.

Exemple avec numéros de ligne (&grave;&grave;&grave;`html {line-numbers="true"}`) :

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Commencer la numérotation sur la ligne _**

Ajoutez `start-number="n"` après la syntaxe du numéro de ligne pour commencer la numérotation sur un numéro autre que 1.

Exemple avec une nouvelle ligne de départ (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`) :

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Mise en surbrillance des lignes dans les blocs de code

Ajoutez `highlight="n"` après la syntaxe du numéro de ligne pour mettre en surbrillance les lignes dans un bloc de code. Spécifier `11-13, 16` mettra en évidence les lignes 11 à 13 et 16.

Exemple avec mise en surbrillance de ligne (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`) :

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```
