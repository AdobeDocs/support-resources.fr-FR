---
title: Application d’un correctif de compositeur fourni par Adobe
description: Cet article explique comment appliquer un correctif de compositeur pour Adobe Commerce On-premise, Adobe Commerce sur l’infrastructure cloud et Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
source-git-commit: fa46bb7187c55a0c7d75930868c74bf8ba072c41
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Application d’un correctif de compositeur fourni par Adobe

Cet article explique comment appliquer un correctif de compositeur pour Adobe Commerce On-premise, Adobe Commerce sur l’infrastructure cloud et Magento Open Source.

>[!WARNING]
>
>Nous vous recommandons vivement d’appliquer et de tester le correctif dans l’environnement d’évaluation/d’intégration avant de l’appliquer à la production. Nous vous recommandons également de disposer d’une sauvegarde récente avant toute manipulation.

## Application d’un correctif de compositeur pour Adobe Commerce sur une infrastructure cloud {#cloud}

1. Si la racine du projet ne contient pas de répertoire nommé `m2-hotfixes`, créez-en un.
1. Copiez le(s) fichier(s) `%patch_name%.composer.patch`(s) dans le répertoire `m2-hotfixes`.
1. Ajoutez, validez et transmettez vos modifications de code :

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.composer.patch patch"
   ```

   ```git
   git push origin
   ```

Pour plus d’informations sur l’application de correctifs aux projets cloud, consultez [Application de correctifs](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches) dans notre documentation destinée aux développeurs et développeuses.

## Application d’un correctif de compositeur pour Adobe Commerce On-Premise et Magento Open Source {#commerce}

1. Chargez le correctif dans votre répertoire racine Adobe Commerce On-Premise ou Magento Open Source.
1. Exécutez la commande SSH suivante :

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   (Si la commande ci-dessus ne fonctionne pas, essayez d’utiliser `-p2` au lieu de `-p1` )

1. Pour que les modifications soient prises en compte, actualisez le cache dans l’Admin sous **[!UICONTROL Système]** > **[!UICONTROL Gestion du cache]**.