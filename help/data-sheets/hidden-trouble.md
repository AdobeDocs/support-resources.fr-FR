---
title: Résolution des problèmes masquée
description: Problème caché
type: Troubleshooting
hide: true
hidefromtoc: true
exl-id: dfb54d2d-e4f4-420f-8e91-f1aba704cb31
source-git-commit: a9acc52cf5469ffeb9711ac6f4b52d54bb99086f
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# Résolution des problèmes masquée

Des `type: Troubleshooting` sont appliquées à cette page. A-t-il un volet gauche ?

## Table des codes

**en dehors du tableau**

```json
PrimaryIdentities [
  {"id": "ccid-2", "namespace": "CCID"},
  {"id": "ecid-1", "namespace": "ECID"},
  {"id": "ecid-2", "namespace": "ECID"}
  ]
NonPrimaryIdentities [
  {"id": "ccid-1", "namespace": "CCID"},
  {"id": "ecid-3", "namespace": "ECID"}
  ]
  "id": "ccid-1",
    "namespace": "CCID"
```

**code droit dans le tableau**

<table>
    <tr>
      <th>Liste des identités triées</th>
      <th>Identité sélectionnée</th>
    </tr>
    <tr>
      <td><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</code> </td>
      <td><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</code> </td>
    </tr>
  </table>

**utilisation du code pre-lang dans le tableau**

<table>
    <tr>
      <th>Liste des identités triées</th>
      <th>Identité sélectionnée</th>
    </tr>
    <tr>
      <td><pre lang="json"><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</pre></code> </td>
      <td><pre lang="json"><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</pre></code> </td>
    </tr>
  </table>

## Liens profonds avec le nouvel onglet

Cliquez ici : [Lien relatif vers l’article ouvert dans un nouvel onglet](hidden/bug-fixes.md#test-for-autoactivate){target=_blank}

```
Click here: [Relative link to article open in new tab](hidden/bug-fixes.md#test-for-autoactivate){target=_blank}
```
