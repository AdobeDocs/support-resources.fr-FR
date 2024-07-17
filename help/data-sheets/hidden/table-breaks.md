---
title: Sauts de tableau
description: Test de différents sauts de table
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# Sauts de tableau

Pas grand-chose à voir ici.

## Tableau de balisage standard avec `<br>`

**FIXED`Green<br>Red<br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br>Rouge<br>Bleu |
| Maria | 23 | Jaune<br>Brown |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br>Rouge<br>Bleu |
| Maria | 23 | Jaune<br>Brown |

{style="table-layout:auto"}

## Table Markdown avec `<br>` doubles

**FIXED`Green<br><br>Red<br><br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br><br>Rouge<br><br>Bleu |
| Maria | 23 | Jaune<br><br>Brown |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br><br>Rouge<br><br>Bleu |
| Maria | 23 | Jaune<br><br>Brown |

{style="table-layout:auto"}

## Table Markdown avec `<p>`

**FIXED`Green<p>Red<p>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<p>Rouge<p>bleu |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:fixed"}

**AUTO`Green<p>Red<p>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<p>Rouge<p>bleu |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:auto"}

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Il s’agit de la couleur **verte** qui est censée s’encapsuler sur une autre ligne comme matière et ou moyen de tester les sauts de paragraphe prédéfinis. <p>Il s’agit de la couleur **rouge** qui est censée s’encapsuler sur une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. <p>Il s’agit de la couleur **bleu** qui est censée s’encapsuler sur une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:fixed"}

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Il s’agit de la couleur **verte** qui est censée s’encapsuler sur une autre ligne comme matière et ou moyen de tester les sauts de paragraphe prédéfinis. <p>Il s’agit de la couleur **rouge** qui est censée s’encapsuler sur une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. <p>Il s’agit de la couleur **bleu** qui est censée s’encapsuler sur une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:auto"}
