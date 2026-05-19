---
title: Comment inclure un membre de l’équipe dans les notifications d’assistance
description: Cet article explique comment inclure un membre de l’équipe dans les notifications d’assistance.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

---


# Comment inclure un membre de l’équipe dans les notifications d’assistance

Cet article explique comment inclure une personne membre de l’équipe pour que cette dernière reçoive automatiquement les mises à jour d’assistance via des notifications par e-mail.

## Produits et versions concernés

* Adobe Commerce sur les infrastructures cloud, toutes les [versions prises en charge](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Cause

* Le membre d&#39;équipe n&#39;a pas été ajouté à la [!DNL cloud project] avec les privilèges nécessaires.
* Le membre de l’équipe ne dispose pas d’un compte d’assistance.

## Solution

1. Accédez à la **[!DNL Cloud Project URL]** (exemple : `https://us-3.magento.cloud/projects/xxxxxx/edit`).
1. Vérifiez si le membre de l&#39;équipe a été ajouté au projet et s&#39;il est un [!DNL Project Admin].

S’ils n’ont pas été ajoutés au projet, vous devrez les ajouter en tant que [!DNL Project Admin] et accorder la [!DNL Shared Access] :

* [Gérer l’accès utilisateur](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=fr) dans notre guide de l’utilisateur.
* [Impossible d’ajouter un utilisateur ou une utilisatrice au projet cloud Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=fr) dans notre base de connaissances Commerce.
* [Guide de l&#39;utilisateur du centre d&#39;aide Adobe Commerce : accès partagé](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=fr#shared-access) dans notre base de connaissances Commerce.

S’ils ont été ajoutés à la [!DNL cloud project], mais ne disposent pas du [!DNL Project Admin role], mettez à jour leur [!DNL role] en conséquence dans [Gérer l’accès utilisateur](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=fr).

Si vous souhaitez permettre à un membre de l’équipe d’être observateur sur tous les cas ouverts pour votre organisation, envoyez un ticket [support](https://experienceleague.adobe.com/home?lang=fr&support-tab=home#support).

## Lecture connexe

[Les anciens membres de l’équipe reçoivent des e-mails de notification Adobe Commerce Cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html?lang=fr)
