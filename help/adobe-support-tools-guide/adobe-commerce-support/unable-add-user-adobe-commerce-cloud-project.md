---
title: Impossible d’ajouter un utilisateur ou une utilisatrice au projet cloud Adobe Commerce
description: Cet article fournit une solution pour les cas où vous ne pouvez pas ajouter un utilisateur à un projet cloud Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 00451af3-7b97-5414-9992-3a6c269e413f
    internal-label: Paas
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
---
# Impossible d’ajouter un utilisateur ou une utilisatrice au projet cloud Adobe Commerce

Cet article fournit une solution pour le cas où vous essayez d’ajouter un utilisateur à un projet cloud, mais qu’il échoue avec une erreur : *L’utilisateur XXX n’existe pas*.

## Produits et versions concernés

* Adobe Commerce sur les infrastructures cloud, [toutes les versions prises en charge](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problème

Cet article fournit une solution pour les cas où vous ne pouvez pas ajouter un utilisateur à un projet cloud Adobe Commerce.

## Cause

Le compte de l’utilisateur doit d’abord être créé à l’adresse [&#128279;](https://accounts.magento.cloud) et lié à son authentification unique Adobe avant de pouvoir être ajouté en tant qu’utilisateur au projet. Si l’utilisateur possède un compte Adobe, mais pas de compte Commerce (magento.com), il doit d’abord en créer un.

## Solution

1. Demandez à l&#39;utilisateur de se connecter à [&#128279;](https://accounts.magento.cloud). L’utilisateur doit déjà être enregistré auprès d’Adobe à l’aide de la même adresse e-mail.
   >[!NOTE]
   >La création ou l’existence d’un compte sur [&#128279;](https://account.adobe.com) ne signifie pas automatiquement que l’utilisateur possède un compte sur [https://accounts.magento.cloud](https://accounts.magento.cloud). L’utilisateur doit d’abord [créer son compte Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Si l’utilisateur possède déjà un compte Adobe mais ne parvient pas à se connecter, demandez-lui d’envoyer une [demande d’assistance](https://experienceleague.adobe.com/home#support) avec le [!UICONTROL Motif de l’événement] défini sur *Gestion utilisateur*.

1. Une fois l’utilisateur connecté à [&#128279;](https://accounts.magento.cloud), vous pouvez l’ajouter au projet. Pour obtenir des instructions détaillées, voir [Ajout d’utilisateurs et gestion de l’accès](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) dans le guide Commerce sur les infrastructures cloud.

## Lecture connexe :

* [Gérer l’accès des utilisateurs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) dans notre Guide de Commerce sur les infrastructures cloud.
* [Impossible de se connecter au support Adobe Commerce ou au compte cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)
