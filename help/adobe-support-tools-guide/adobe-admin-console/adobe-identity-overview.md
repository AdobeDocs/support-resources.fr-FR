---
title: Présentation des identités
description: Découvrez et choisissez les types d’identité (Federated ID, Enterprise ID, Adobe ID et Personal Adobe ID) pour votre organisation et gérez l’accès des utilisateurs dans Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 5%

---


# Présentation des identités

S’applique aux entreprises et aux équipes.

Le système Identity Management d’Adobe permet aux administrateurs de créer et de gérer l’accès des utilisateurs aux applications et services. Adobe propose ces types d’identité ou comptes pour authentifier et autoriser les utilisateurs.

## Types d’identité sur Adobe Admin Console

Les types d’identité permettent à l’organisation de contrôler à différents niveaux les comptes et données des utilisateurs. Le choix du modèle d’identité a un impact considérable sur la manière dont votre organisation stocke et partage les ressources. Alors que les modèles Federated ID et Enterprise ID sont créés et gérés par l’organisation, les Adobe ID sont créés et gérés par la personne concernée.

Le tableau suivant vous guide pour choisir le modèle d’identité qui convient le mieux à votre organisation.

>[!NOTE]
>Si votre organisation n’a pas été mise à jour vers le modèle de stockage d’entreprise Adobe et que vous utilisez toujours des Adobe ID pour les individus, consultez la description dans le tableau [types d’identité](https://helpx.adobe.com/enterprise/using/identity.html#using-personal-adobe-id) ci-dessous.

<table>
<thead>
<tr>
<th scope="col">Types d’identité</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Icône Federated ID"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Principales offres</strong></th>
<td>Créé, détenu et géré par l’organisation. L’entreprise gère les informations d’identification des utilisateurs et utilisatrices et utilise l’authentification unique (SSO) via un fournisseur d’identité SAML2 (IdP).</td>
<td>Créé, détenu et géré par l’organisation. L’organisation conserve les droits exclusifs de création de comptes d’utilisateurs sur les domaines vérifiés.</td>
<td>Créé, détenu et géré par l’utilisateur final. Adobe effectue l’authentification et l’utilisateur final gère l’identité. En fonction du <a href="https://helpx.adobe.com/enterprise/using/storage-for-business.html">modèle de stockage</a>, les utilisateurs et les entreprises conservent le contrôle des fichiers et des données. Les comptes Adobe ID sont créés sur des domaines non vérifiés, publics ou approuvés. Voir le point 2 de la section « Notes » ci-dessous.</td>
</tr>
<tr>
<th scope="row"><strong>Propriété du compte et des données</strong></th>
<td colspan="2">Détenu et contrôlé par l’organisation</td>
<td>Détenu par l’entreprise pour le stockage d’entreprise et par l’utilisateur pour le stockage utilisateur</td>
</tr>
<tr>
<th scope="row"><strong>Sécurité et surveillance</strong></th>
<td colspan="2">
  <ul>
    <li>Journaux d’audit</li>
    <li>Logs de contenu</li>
    <li>Restrictions de partage</li>
    <li>Paramètres d’authentification de l’entreprise</li>
  </ul>
</td>

<td>
  <ul>
    <li>Logs de contenu</li>
    <li>Restrictions de partage</li>
    <li>Politique de mot de passe</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>Réinitialiser le mot de passe</strong></th>
<td colspan="2">Non pris en charge</td>
<td><a href="https://helpx.adobe.com/fr/manage-account/using/change-or-reset-password.html">Réinitialiser le mot de passe de votre compte</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud abonnement Entreprise et Document Cloud abonnement Entreprise</strong></th>
<td colspan="3">Pris en charge</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud pour les équipes et Document Cloud pour les équipes</strong></th>
<td colspan="2">Non pris en charge</td>
<td>Pris en charge</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">Pris en charge</td>
</tr>
<tr>
<th scope="row"><strong>Recommandé pour</strong></th>
<td>
  <ul>
    <li>Organisations qui utilisent déjà SSO ou SAML</li>
    <li>Services d’annuaire existants (par exemple Google et Azure AD)</li>
    <li>Nécessite une intégration facile à des services autres qu’Adobe</li>
    <li>Peut démontrer la propriété du domaine</li>
  </ul>
</td>
<td>
  <ul>
    <li>Peut démontrer la propriété du domaine</li>
    <li>Ne pas exiger une authentification unique</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud pour les équipes</li>
    <li>L’entreprise préfère utiliser des domaines qu’elle ne possède pas</li>
    <li>Domaines publics (par exemple Hotmail, Gmail)</li>
    <li>Accéder à des applications telles qu’Adobe Experience Manager Mobile</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Commencer</strong></th>
<td><a href="https://helpx.adobe.com/fr/enterprise/using/set-up-identity.html">Configurer l’identité</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/add-domains-directories.html#claim-domains">Demander des domaines</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">Ajouter un utilisateur ou une utilisatrice</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. La politique de mot de passe pour Creative Cloud pour les équipes est identique à celle de Creative Cloud pour les individus.
>1. Les utilisateurs d’Adobe ID s’authentifient avec leurs informations d’identification Adobe ID ou selon le modèle d’authentification de leur organisation (SSO, 2FA, etc.). Dans de tels scénarios, les utilisateurs sont redirigés vers la page de l’authentification unique de l’organisation propriétaire. Après l’authentification, les utilisateurs peuvent devoir [choisir un profil professionnel](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#choose-profile).

## Utilisation des ID Adobe personnels

Adobe met à jour toutes les équipes et tous les clients d’entreprise pour utiliser le modèle de stockage d’entreprise Adobe. Consultez le tableau suivant si votre organisation compte des utilisateurs qui utilisent des identifiants Adobe personnels pour accéder aux applications et services Adobe de leur entreprise ou de leur école.

### Adobe ID personnelle

<table>
<thead>
<tr>
<th scope="col">Type d’identité</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  Adobe ID personnelle
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Principales offres</strong></th>
<td>Créé, détenu et géré par l’utilisateur final. Adobe effectue l’authentification et l’utilisateur final gère l’identité.</td>
</tr>
<tr>
<th scope="row"><strong>Propriété du compte et des données</strong></th>
<td>Contrôlé par l'utilisateur</td>
</tr>
<tr>
<th scope="row"><strong>Sécurité et surveillance</strong></th>
<td>Politique de mot de passe. Se reporter au point 1 de la note ci-dessous.</td>
</tr>
<tr>
<th scope="row"><strong>Réinitialiser le mot de passe</strong></th>
<td><a href="https://helpx.adobe.com/fr/manage-account/using/change-or-reset-password.html">Réinitialiser le mot de passe de votre compte.</a> Se reporter au point 2 de la note ci-dessous.</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud abonnement Entreprise et Document Cloud abonnement Entreprise</strong></th>
<td>Pris en charge</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>Pris en charge</td>
</tr>
<tr>
<th scope="row"><strong>Disponible uniquement pour / Recommandé pour</strong></th>
<td>
  <ul>
    <li>Clients Grands comptes et équipes intégrés avant la migration</li>
    <li>Creative Cloud pour les équipes</li>
    <li>Souhaite un contrôle dans la main de l’utilisateur</li>
    <li>Accès à des applications telles que Digital Publishing Suite</li>
    <li>Les utilisateurs possèdent des ressources après leur séparation de l’organisation.</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Commencer</strong></th>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">Ajouter un utilisateur ou une utilisatrice</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. La politique de mot de passe pour Creative Cloud pour les équipes est identique à celle de Creative Cloud pour les individus.
>1. Pour les clients Creative Cloud abonnement Entreprise qui utilisent [stockage d’entreprise](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html), les administrateurs peuvent ajouter des utilisateurs Adobe ID à Admin Console, mais ne peuvent pas les ajouter aux profils de produits. Les administrateurs doivent migrer les utilisateurs d’Adobe ID vers un autre type d’identité.
>1. Certains produits et services, tels que **Adobe Licensing Website, ne prennent en charge que** Adobe ID.

## Autres informations similaires

- [Configurer l’identité](https://helpx.adobe.com/fr/enterprise/using/set-up-identity.html)
- [Changer d’identité utilisateur](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)
- [Présentation d’](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [FAQ sur l’éducation](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [Ajouter et gérer des utilisateurs](https://helpx.adobe.com/fr/enterprise/using/users.html)