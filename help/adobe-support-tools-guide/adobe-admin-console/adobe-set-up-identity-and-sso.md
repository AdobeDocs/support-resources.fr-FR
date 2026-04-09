---
title: Configurer l'identité et l'authentification SSO
description: Découvrez comment les administrateurs du système d’organisation peuvent configurer l’identité utilisateur et l’authentification unique (SSO) dans Adobe Admin Console à l’aide d’Adobe ID, d’Enterprise ID ou de Federated ID.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# Configurer l&#39;identité et l&#39;authentification SSO

**S’applique à :** Entreprise

Découvrez comment configurer une identité dans le Adobe Admin Console. Comparez Adobe ID, Enterprise ID et Federated ID, puis configurez l’authentification unique (SSO) pour un accès sécurisé aux applications Adobe.

Configurez l’identité et configurez l’authentification unique (SSO) pour que les employés puissent [se connecter](https://adminconsole.adobe.com/settings/) avec les informations d’identification existantes de l’entreprise.

Voici le tutoriel vidéo expliquant comment [Configurer une identité et une authentification unique (YouTube)](https://youtu.be/V57lU4zaSBs).

## Termes et concepts clés

### Répertoire

Un répertoire dans Admin Console est une entité qui contient des ressources telles que des utilisateurs et des politiques telles que l’authentification. Ces répertoires sont similaires à LDAP ou Active Directory.

### Fournisseur d’identité (IdP)

Un fournisseur d’identité (IdP) est le fournisseur d’identité de votre organisation, tel que :

- Active Directory
- Microsoft Azure
- Ping
- Okta
- En Commun
- Shibboleth

### Personnes impliquées

| Rôle | Responsabilité |
|------|----------------|
| Administrateur système | Fonctionne avec les gestionnaires d’annuaires IdP et les gestionnaires DNS pour configurer l’identité dans Admin Console. |
| Gestionnaire DNS | Met à jour les jetons DNS pour valider la propriété du domaine. |
| Gestionnaire de répertoires du fournisseur d’identité (IdP) | Gère le portail IdP et les connecteurs associés. |

### Adobe ID

Créé, détenu et géré par l’utilisateur final. Adobe effectue l’authentification et l’utilisateur final gère l’identité. En fonction du [modèle de stockage](https://helpx.adobe.com/enterprise/using/storage-for-business.html), les utilisateurs et les entreprises conservent le contrôle des fichiers et des données.

Pour les organisations qui ont été mises à jour vers le modèle de stockage d’entreprise, les ressources et les données sont contrôlées par l’organisation. Pour les organisations qui n’ont pas été mises à jour, la personne possède et contrôle les ressources d’Adobe ID.

### Enterprise ID

Créé, détenu et géré par une organisation. Adobe héberge Enterprise ID et effectue l’authentification, mais l’organisation conserve Enterprise ID. Les administrateurs créent une Enterprise ID et l’émettent à un utilisateur. Les administrateurs peuvent révoquer l’accès aux produits et services en reprenant le compte ou en supprimant l’Enterprise ID pour bloquer définitivement l’accès aux données associées. Pour en savoir plus, cliquez [ici](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html).

### Federated ID

Créé et détenu par une organisation, et lié à l&#39;annuaire d&#39;entreprise via une fédération. L’entreprise gère les informations d’identification et traite l’authentification unique via un fournisseur d’identité SAML2 (IdP).

Voici quelques exigences et scénarios pour lesquels les Federated ID sont recommandés :

- Si vous souhaitez configurer les utilisateurs en fonction de l’annuaire d’entreprise de votre entreprise.
- Si vous souhaitez gérer l’authentification des utilisateurs.
- Si vous devez maintenir un contrôle strict sur les applications et les services disponibles pour un utilisateur.

## Configurer l&#39;identité sans l&#39;authentification SSO

Vous pouvez utiliser Adobe ID ou Enterprise ID si votre organisation n’utilise pas actuellement la connexion unique dans d’autres applications.

## Utilisation d’Adobe ID

Adobe met à jour toutes les organisations vers le [modèle de stockage d’entreprise](https://helpx.adobe.com/enterprise/using/storage-for-business.html). Cela permet à votre entreprise de mieux contrôler les ressources et les données de vos utilisateurs.

Commencez avec [ajout d’utilisateurs](https://helpx.adobe.com/fr/enterprise/using/users.html) à Admin Console.

## Configurer l’identité avec Enterprise ID

Vous pouvez configurer un annuaire Enterprise ID si vous souhaitez mieux contrôler les données de vos utilisateurs sans utiliser la connexion unique. Seuls les administrateurs créent une Enterprise ID et l’émettent à un utilisateur.

Voir [Configuration de l’organisation avec Enterprise ID](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html) pour connaître les exigences et les étapes de création des répertoires Enterprise ID.

## Configurer l&#39;identité avec l&#39;authentification SSO

Vous devez configurer l’identité utilisateur avec les comptes Federated ID pour utiliser la connexion unique.

Les Federated ID sont recommandés dans les cas suivants :

- Vous devez maintenir un contrôle strict sur les applications et les services disponibles pour un utilisateur.
- Vous souhaitez gérer l’authentification des utilisateurs et utilisatrices.
- Vous souhaitez configurer les utilisateurs en fonction de l’annuaire d’entreprise de votre entreprise.

## Configurer une nouvelle intégration SSO

Vous pouvez utiliser des fournisseurs d’identité populaires tels que Microsoft Azure AD, Google ou d’autres fournisseurs d’identité SAML pour configurer la connexion unique entre votre entreprise et les produits Adobe.

**Azure AD** (recommandé) - [Configurez l’authentification unique et la synchronisation des utilisateurs avec le connecteur Azure AD](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html)

**Autre IdP SAML** - [Configuration de la connexion unique avec d’autres fournisseurs SAML](https://helpx.adobe.com/enterprise/using/create-directory.html)

**&#x200B;**&#x200B;(Recommandé) - [Configurez l’authentification unique et la synchronisation des utilisateurs à l’aide du connecteur Google](https://helpx.adobe.com/enterprise/using/setup-sso-google.html)

## Gérer la configuration SSO existante

Une fois la connexion unique configurée entre votre organisation et Adobe, utilisez les méthodes suivantes pour gérer et modifier votre configuration.

Découvrez comment gérer vos domaines et répertoires :

- [Gérer les utilisateurs](https://helpx.adobe.com/fr/enterprise/using/users.html) les utilisatrices et les [groupes](https://helpx.adobe.com/enterprise/using/user-groups..html)
- [Lier des domaines à des répertoires](https://helpx.adobe.com/enterprise/using/add-domains-directories.html#link-domains-to-directoies) pour contrôler l’accès des utilisateurs aux applications, services et paramètres.
- [Gérer l’approbation d’annuaire](https://helpx.adobe.com/enterprise/using/directory-trust.html) pour utiliser des domaines demandés par une autre organisation

Découvrez comment modifier votre fournisseur d’identité :

- [Modifiez votre IdP](https://helpx.adobe.com/enterprise/using/migrate-authentication-provider.html) sans interrompre le travail de vos utilisateurs
- [Déplacement de domaines dans des répertoires](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [Supprimer les utilisateurs de l’annuaire hérité](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [Supprimer les anciens domaines/domaines non réclamés et les répertoires vides](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#delete)

## Erreurs et questions courantes

Solutions aux questions et erreurs courantes lors de la configuration et de la gestion de la connexion unique :

### Azure AD - FAQ et dépannage

#### Questions fréquentes

- [FAQ sur le connecteur Azure AD](https://helpx.adobe.com/enterprise/using/azure-ad-connector-faq.html)
- [Supprimer des répertoires et des domaines](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### Dépannage

- [Accès refusé aux utilisateurs](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)
- [&#x200B; Problèmes de synchronisation &#x200B;](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)

### Autres SAML IdP - FAQ et dépannage

#### Questions fréquentes

[FAQ sur l’intégration SAML](https://helpx.adobe.com/enterprise/using/sso-faq.html)

#### Dépannage

- [Dépannage général de l’authentification unique](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [’erreur « Accès refusé »](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [’erreur « Un autre utilisateur est actuellement connecté »](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [Effectuer une trace SAML](https://helpx.adobe.com/enterprise/kb/perform-a-saml-trace.html)

### GOOGLE - FAQ

- [FAQ sur le connecteur &#x200B;](https://helpx.adobe.com/enterprise/using/google-federation-faq.html)
- [Supprimer des répertoires et des domaines](https://helpx.adobe.com/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## Rejoignez la conversation

Pour collaborer, poser des questions et discuter avec d’autres administrateurs, utilisez la [Communauté d’entreprise et d’équipes](https://www.adobe.com/go/entcom).

## Mentions légales et confidentialité

- [Mentions légales](https://helpx.adobe.com/legal/legal-notices.html)
- [Politique de confidentialité en ligne](https://www.adobe.com/fr/privacy.html)
