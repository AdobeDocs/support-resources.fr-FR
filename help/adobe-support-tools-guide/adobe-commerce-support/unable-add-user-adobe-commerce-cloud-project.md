---
title: Impossible d’ajouter un utilisateur ou une utilisatrice au projet cloud Adobe Commerce
description: Cet article fournit une solution pour les cas où vous ne pouvez pas ajouter un utilisateur à un projet cloud Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Impossible d’ajouter un utilisateur ou une utilisatrice au projet cloud Adobe Commerce

Cet article fournit une solution pour le cas où vous essayez d’ajouter un utilisateur à un projet cloud, mais qu’il échoue avec une erreur : *L’utilisateur XXX n’existe pas*.

## Produits et versions concernés

* Adobe Commerce sur les infrastructures cloud, [toutes les versions prises en charge](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problème

Cet article fournit une solution pour les cas où vous ne pouvez pas ajouter un utilisateur à un projet cloud Adobe Commerce.

## Cause

Le compte de l’utilisateur doit d’abord être créé à l’adresse [https://accounts.magento.cloud](https://accounts.magento.cloud) et lié à son authentification unique Adobe avant de pouvoir être ajouté en tant qu’utilisateur au projet. Si l’utilisateur possède un compte Adobe, mais pas de compte Commerce (magento.com), il doit d’abord en créer un.

## Solution

1. Demandez à l&#39;utilisateur de se connecter à [https://accounts.magento.cloud](https://accounts.magento.cloud). L’utilisateur doit déjà être enregistré auprès d’Adobe à l’aide de la même adresse e-mail.
   >[!NOTE]
   >La création ou l’existence d’un compte sur [https://account.adobe.com](https://account.adobe.com) ne signifie pas automatiquement que l’utilisateur possède un compte sur [https://accounts.magento.cloud](https://accounts.magento.cloud). L’utilisateur doit d’abord [créer son compte Commerce](https://experienceleague.adobe.com/fr/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Si l’utilisateur possède déjà un compte Adobe mais ne parvient pas à se connecter, demandez-lui d’envoyer une [demande d’assistance](https://experienceleague.adobe.com/home?lang=fr#support) avec le [!UICONTROL Motif de l’événement] défini sur *Gestion utilisateur*.

1. Une fois l’utilisateur connecté à [https://accounts.magento.cloud](https://accounts.magento.cloud), vous pouvez l’ajouter au projet. Pour obtenir des instructions détaillées, voir [Ajout d’utilisateurs et gestion de l’accès](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) dans le guide Commerce sur les infrastructures cloud.

## Lecture connexe :

* [Gérer l’accès des utilisateurs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=fr) dans notre Guide de Commerce sur les infrastructures cloud.
* [Impossible de se connecter au support Adobe Commerce ou au compte cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=fr)
