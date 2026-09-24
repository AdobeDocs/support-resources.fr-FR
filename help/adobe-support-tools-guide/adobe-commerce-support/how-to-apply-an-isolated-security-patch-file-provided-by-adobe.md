---
title: Application d’un correctif isolé fourni par Adobe
description: Cet article explique comment appliquer un correctif isolé pour Adobe Commerce On-premise, l’infrastructure Adobe Commerce sur Cloud et Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
    internal-label: Compliance
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 125c1f49-aefd-5f34-a252-288937f95f6b
    internal-label: Marketing Tools
subfeature_v2:
  - id: c4af0798-d497-5e6b-8380-19812c26d00a
    internal-label: Console
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%
---
# Application d’un correctif isolé fourni par Adobe

Cet article explique comment appliquer un correctif isolé pour Adobe Commerce On-premise, l’infrastructure Adobe Commerce sur Cloud et Magento Open Source.

>[!WARNING]
>
>Nous vous recommandons vivement d’appliquer et de tester le correctif dans l’environnement d’évaluation/d’intégration avant de l’appliquer à la production. Nous vous recommandons également de disposer d’une sauvegarde récente avant toute manipulation.

## Application d’un correctif isolé pour Adobe Commerce sur une infrastructure cloud {#cloud}

1. Si la racine du projet ne contient pas de répertoire nommé `m2-hotfixes`, créez-en un.
1. Copiez le(s) fichier(s) `%patch_name%.patch`(s) dans le répertoire `m2-hotfixes`.
1. Ajoutez, validez et transmettez vos modifications de code :

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

Pour plus d’informations sur l’application de correctifs aux projets cloud, voir [Application de correctifs](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches).

## Application d’un correctif isolé pour Adobe Commerce On-premise et Magento Open Source {#commerce}

1. Chargez le correctif dans votre répertoire racine Adobe Commerce On-Premise ou Magento Open Source.
1. Exécutez la commande SSH suivante :

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   (Si la commande ci-dessus ne fonctionne pas, essayez d’utiliser `-p2` au lieu de `-p1`)

1. Pour que les modifications soient prises en compte, actualisez le cache dans le [!UICONTROL Admin] sous **[!UICONTROL Système]** > **[!UICONTROL Gestion du cache]**.
