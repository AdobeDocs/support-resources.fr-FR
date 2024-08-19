---
title: Blocages dans les blocs de code UGP-11189
description: Blocages dans le test UGP-11189 des blocs de code
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# Blocage de code

1. Exécutez la commande :

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Étape suivante

Pas dans le bloc de code

état vendor/bin/magento-patches -n |grep &quot;27015\|Status&quot;

Barre oblique inverse :

état vendor/bin/magento-patches -n |grep &quot;27015&amp;bsol;|Status&quot;
