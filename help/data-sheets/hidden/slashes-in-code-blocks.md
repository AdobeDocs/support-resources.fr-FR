---
title: Blocages dans les blocs de code UGP-11189
description: Blocages dans le test UGP-11189 des blocs de code
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Blocage de code

1. Exécutez la commande :

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Exécutez la commande (avec échappement) :

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

Pas dans le bloc de code

état vendor/bin/magento-patches -n |grep &quot;27015\|Status&quot;

Échappé :

état vendor/bin/magento-patches -n |grep &quot;27015&amp;bsol;|Status&quot;

