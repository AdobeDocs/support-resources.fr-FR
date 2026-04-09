---
title: Utilisateurs de Adobe Admin Console
description: 'Planifiez votre stratégie de gestion des utilisateurs sur Adobe Admin Console : ajoutez des administrateurs et des utilisateurs finaux, choisissez une méthode de gestion des utilisateurs et attribuez des licences.'
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 4%

---

# Utilisateurs de Adobe Admin Console

S’applique aux entreprises et aux équipes.

Faire face à l&#39;un de ces problèmes ? Sélectionnez un événement pour afficher la résolution.

- [Gérer les rôles d’administrateur](https://helpx.adobe.com/fr/enterprise/using/admin-roles.html)
- [Problèmes de téléchargement-installation](https://helpx.adobe.com/download-install.html)
- [Réinitialiser le mot de passe de l’utilisateur Enterprise ID](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#faq)
- [Résoudre les erreurs Federated ID](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [Supprimer un utilisateur ou restaurer un utilisateur supprimé](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - Utilisateurs** — [Regarder sur YouTube](https://youtu.be/w8b36YX2TEM)

## Pourquoi ajouter des utilisateurs à Adobe Admin Console ?

>[!NOTE]
>
>En tant qu’administrateur sur Adobe Admin Console, après avoir choisi votre [type d’identité](https://helpx.adobe.com/fr/enterprise/using/identity.html) et [configuré l’identité](https://helpx.adobe.com/fr/enterprise/using/set-up-identity.html), votre tâche suivante consiste à ajouter des utilisateurs à Admin Console.

Adobe entreprise et équipes définit globalement deux types d’utilisateurs :

### Administrateurs (administrateurs)

Les administrateurs d’entreprise ou d’équipe effectuent des tâches administratives sur Admin Console. Ajoutez des administrateurs pour définir une hiérarchie administrative flexible qui permet une gestion affinée de l’accès au produit Adobe, de son utilisation et d’autres tâches administratives.

Tous les administrateurs doivent être ajoutés à Admin Console. Lors de leur ajout, les privilèges d’administration sont basés sur leurs [&#x200B; rôles d’administration &#x200B;](https://helpx.adobe.com/fr/enterprise/using/admin-roles.html).

### Utilisateurs finaux

Les utilisateurs finaux sont les utilisateurs de votre organisation ou institution qui utilisent les produits et services Adobe obtenus par votre organisation ou institution dans le cadre du contrat avec Adobe.

## Choix de votre stratégie de gestion des utilisateurs

Selon vos besoins, vous pouvez ajouter, supprimer ou mettre à jour des utilisateurs *individuellement* ou utiliser l’une des méthodes de chargement en bloc *disponibles*. Utilisez le tableau suivant comme guide pour planifier votre gestion des utilisateurs.

>[!NOTE]
>
>Si vous êtes un nouveau client d’Adobe Grands comptes ou Équipes, nous vous recommandons de parcourir ce tableau avant de commencer à gérer vos utilisateurs sur Admin Console. Les clients existants peuvent l’utiliser, en particulier s’ils envisagent de migrer d’un type d’identité à un autre (voir [Modifier le type d’identité](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)).

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>Individuellement (Admin Console)</strong></th>
<th scope="col"><strong>CSV Bulk upload (Admin Console)</strong></th>
<th scope="col"><strong>Connecteurs Azure/Google</strong></th>
<th scope="col"><strong>Outil de synchronisation des utilisateurs</strong></th>
<th scope="col"><strong>API REST User Management</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Application</strong></th>
<td colspan="2">équipes Adobe et clients Grands comptes</td>
<td colspan="3">clients d’Adobe enterprise</td>
</tr>
<tr>
<th scope="row"><strong>Description</strong></th>
<td>Gérez les utilisateurs individuellement dans Admin Console.</td>
<td>Gérez les utilisateurs avec le chargement de fichiers CSV dans Admin Console.</td>
<td>Gérez les utilisateurs (et les groupes) en fonction de votre portail Azure AD existant ou de votre fédération Google.</td>
<td colspan="2">Gérez les utilisateurs (et les groupes) en fonction du protocole LDAP de votre entreprise.</td>
</tr>
<tr>
<th scope="row"><strong>Ajouter des utilisateurs</strong></th>
<td><strong>Onglet Utilisateurs</strong> dans <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/fr/enterprise/using/manage-users-individually.html#add-users">En savoir plus</a>.</td>
<td>Utilisez <strong>Ajouter des utilisateurs par fichier CSV</strong> dans <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">En savoir plus</a>. <em>(utilisez le modèle CSV par défaut)</em></td>
<td>Ajoutez des utilisateurs dans <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html"></a> ou <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>. Ou via <strong></strong>.</td>
<td colspan="2">Les utilisateurs doivent être ajoutés dans le LDAP de votre organisation.</td>
</tr>
<tr>
<th scope="row"><strong>Supprimer des utilisateurs</strong></th>
<td>Sélectionnez et supprimez un utilisateur dans <strong></strong>. <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#remove-users">En savoir plus</a>.</td>
<td>Choisissez <strong>Supprimer des utilisateurs par fichier CSV</strong> dans l’onglet <strong>Utilisateurs</strong> de <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#remove-users">En savoir plus</a>. <em>(utilisez le modèle CSV par défaut)</em></td>
<td>Les utilisateurs doivent être supprimés dans <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure ou </a>Google<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html"> </a>.</td>
<td colspan="2">Vérifiez que les informations utilisateur sont synchronisées. <strong>Attention :</strong> les utilisateurs qui ne figurent pas dans le LDAP de votre organisation sont supprimés d’Admin Console.</td>
</tr>
<tr>
<th scope="row"><strong>Modifier les détails de l’utilisateur</strong></th>
<td>Sélectionnez l’utilisateur, puis <strong>Modifier les détails de l’utilisateur</strong> dans Admin Console. <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#edit-user-details">En savoir plus</a>.</td>
<td>Choisissez <strong>Modifier les détails de l’utilisateur par fichier CSV</strong> dans l’onglet <strong>Utilisateurs</strong> de <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#edit-user-details">En savoir plus</a>. <em>(utilisez le modèle CSV par défaut)</em></td>
<td>Toutes les informations utilisateur doivent être modifiées dans <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html"></a> ou <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Vérifiez que les informations utilisateur sont synchronisées.</td>
</tr>
<tr>
<th scope="row"><strong>Types d’identité pris en charge</strong></th>
<td colspan="2">Toutes</td>
<td>Federated ID</td>
<td colspan="2">Federated ID et Enterprise ID</td>
</tr>
<tr>
<th scope="row"><strong>Durée max. mises à jour par opération</strong></th>
<td>10</td>
<td>25 000 (5 000 <em> pour des performances optimales</em>)</td>
<td colspan="3">Illimité (Associe au LDAP de votre organisation)</td>
</tr>
<tr>
<th scope="row"><strong>Requiert</strong></th>
<td>Adobe Admin Console</td>
<td>Création et mise à jour de formats de fichiers .csv, de préférence avec Microsoft Excel</td>
<td>Vous devez configurer Azure AD ou Google Federation</td>

<td>
  <ul>
    <li>macOS Terminal ou invite de commande Windows</li>
    <li>Compréhension de LDAP</li>
  </ul>
</td>

<td>Connaissances opérationnelles d’un langage de programmation (tel que Python) pour utiliser les API REST</td>
</tr>
<tr>
<th scope="row"><strong>En savoir plus</strong></th>
<td><a href="https://helpx.adobe.com/fr/enterprise/using/manage-users-individually.html">Gestion des utilisateurs individuels</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">
        Gérer les utilisateurs | Charger en bloc un fichier CSV
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        Résolution des problèmes de chargement CSV d’utilisateur en bloc
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">
        Connecteur Azure AD
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">
        Connecteur de fédération Google
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        À propos de la synchronisation des utilisateurs
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Référentiel Git
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/user-sync.html">
        Guide détaillé
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">À propos de l’UMAPI</a></td>
</tr>
</tbody>
</table>

## Étapes suivantes

### Créer des packages

Une fois ajoutés, vos utilisateurs sont prêts à se voir attribuer leurs applications et services désignés.

Attribuez des licences aux utilisateurs finaux en fonction de votre méthode de licence :

- **Licences utilisateur nommées :** ajoutez ces utilisateurs aux **produits** ([pour les équipes](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)) ou **profils de produit** ([pour les entreprises](https://helpx.adobe.com/fr/enterprise/using/manage-product-profiles.html)) pour leur accorder des droits sur les produits et services Adobe. Pour plus d’informations, consultez les sections [Création de packages de licences utilisateur nommées](https://helpx.adobe.com/enterprise/using/create-nul-packages.html) et [Profils de produit](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#create-product-profile).
- **Licences d’appareil partagé :** [utilisateurs ajoutés](https://helpx.adobe.com/enterprise/using/sdl-deployment-guide.html#add-users-admin-console) peut utiliser les appareils partagés configurés qui sont accessibles par les utilisateurs de l’**organisation uniquement**. Pour plus d’informations, voir [Création de packages SDL](https://helpx.adobe.com/enterprise/using/create-sdl-packages.html).

### Déployer des packages

Une fois le package créé, déployez-le sur les ordinateurs clients à l’aide de l’une des méthodes suivantes :

- Accédez à l’ordinateur client et double-cliquez sur le fichier de package (Windows ou macOS).
- Utilisez l’invite de commande Windows ou le terminal macOS.
- Utilisez des outils tiers :
   - [Microsoft Intune](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Microsoft System Center Configuration Manager (SCCM)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-sccm.html)
   - [Bureau à distance Apple (ARD)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ard.html)
   - [&#x200B; JAMF Pro &#x200B;](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki &#x200B;](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-munki.html)

## Lecture connexe

- [Gérer les utilisateurs | Individuellement](https://helpx.adobe.com/fr/enterprise/using/manage-users-individually.html)
- [Gérer les utilisateurs | Chargement CSV en bloc](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)
- [Gérer les utilisateurs du répertoire](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html)
- [Affectation d’utilisateurs à des profils de produit (pour les entreprises et les institutions)](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#assign-users)
- [Attribuer des licences aux utilisateurs des équipes](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)
- [Modèle de stockage d’entreprise](https://helpx.adobe.com/enterprise/kb/business-storage-model-introduction.html)