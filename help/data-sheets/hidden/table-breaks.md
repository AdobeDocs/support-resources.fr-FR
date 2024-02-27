---
title: Sauts de tableau
description: Test de différents sauts de table
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# Sauts de tableau

## Tableau des balises standard avec `<br>`

**FIXED`Green<br>Red<br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br>Rouge<br>bleu |
| Maria | 23 | Jaune<br>Brown |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br>Rouge<br>bleu |
| Maria | 23 | Jaune<br>Brown |

{style="table-layout:auto"}

## Tableau Markdown avec double `<br>`s

**FIXED`Green<br><br>Red<br><br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br><br>Rouge<br><br>bleu |
| Maria | 23 | Jaune<br><br>Brown |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<br><br>Rouge<br><br>bleu |
| Maria | 23 | Jaune<br><br>Brown |

{style="table-layout:auto"}

## Tableau Markdown avec `<p>`

**FIXED`Green<p>Red<p>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<p>Rouge<p>Bleu |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:fixed"}

**AUTO`Green<p>Red<p>Blue`**

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | Vert<p>Rouge<p>Bleu |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:auto"}

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | C&#39;est la couleur **vert** et il est destiné à encapsuler une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. <p>C&#39;est la couleur **red** et il est destiné à encapsuler une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. <p>C&#39;est la couleur **bleu** et il est destiné à encapsuler une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:fixed"}

|  | Nombre | Couleurs |
|---|---|---|
| Juanya | 17 | C&#39;est la couleur **vert** et il est destiné à encapsuler une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. <p>C&#39;est la couleur **red** et il est destiné à encapsuler une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. <p>C&#39;est la couleur **bleu** et il est destiné à encapsuler une autre ligne comme matière et/ou moyen de tester les sauts de paragraphe prévus. |
| Maria | 23 | Jaune<p>Brown |

{style="table-layout:auto"}
