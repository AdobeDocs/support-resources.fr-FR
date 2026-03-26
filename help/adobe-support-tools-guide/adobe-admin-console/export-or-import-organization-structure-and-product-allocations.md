---
title: Exporter ou importer la structure de l'organisation et les allocations de produits
description: Découvrez comment les administrateurs globaux exportent et importent les données de hiérarchie d’organisation et d’attribution de produits dans Global Admin Console à l’aide de JSON, CSV ou XLSX. S’applique à l’entreprise.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 3220086a-4603-465f-a3e3-194193ca10ba
source-git-commit: d29553542d3e6ea7e12fbf4c1bd1e5f6600d42b0
workflow-type: tm+mt
source-wordcount: '4425'
ht-degree: 3%

---

# Exporter ou importer la structure de l&#39;organisation et les allocations de produits

**S’applique à :** Entreprise

Découvrez comment les administrateurs globaux peuvent rationaliser la gestion de l’organisation et des produits grâce aux fonctionnalités d’exportation et d’importation de Global Admin Console.

Accédez à l’onglet **[!UICONTROL Organisations]** dans le [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) pour exporter ou importer la structure de l’organisation. Accédez à l’onglet **[!UICONTROL Affectation de produit]** pour consulter les données d’affectation. Utilisez l’icône **[!UICONTROL Plus d’options]** **⋮** pour sélectionner exporter ou importer. [Connectez-vous au Global Admin Console](https://global-admin-console.adobe.com).

## Exporter la structure de l&#39;organisation

En tant qu&#39;[administrateur global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), vous pouvez exporter la hiérarchie de l&#39;organisation. Vous pouvez télécharger une représentation JSON, CSV ou XLSX de l’ensemble de la hiérarchie de l’organisation ou d’un sous-ensemble de celle-ci. Vous pouvez ensuite utiliser ces données à des fins d’analyse ou de modification.

Le format d’exportation choisi a un impact sur la structure des données exportées :

- Format CSV : permet d’exporter un seul type de données à la fois. Lors de l’exportation de profils de produit au format CSV, les profils et les ressources sont combinés en un seul tableau. Il existe plusieurs entrées pour le profil de produit, une pour chaque ressource.
- Format XLSX : les résultats de chaque organisation sont affichés sur une feuille séparée. Les enregistrements sont connectés entre les différents types d&#39;objets par un identifiant de référence. Dans certains cas, il peut y avoir plusieurs lignes pour un objet particulier (par exemple, des objets Ressource lorsqu’un ensemble de valeurs est associé à une ressource donnée).
- Format JSON : le plus flexible. Il peut tirer parti des relations structurelles entre les objets exportés (par exemple, les produits d’une organisation apparaissent directement dans l’élément d’organisation). Les mêmes champs sont exportés dans les trois formats, mais certaines valeurs sont redondantes au format JSON.

### Étapes d’exportation

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/). Dans l’onglet **[!UICONTROL Organisations]**, utilisez le sélecteur d’organisation pour sélectionner la hiérarchie d’organisations à exporter. Les données de toutes les organisations de la hiérarchie sont exportées.
2. Sélectionnez l’icône **[!UICONTROL Plus d’options]** ⋮ et choisissez **[!UICONTROL Exporter]**.

   ![Exporter la structure organisationnelle](./assets/export-org-structure.png)

3. Dans la boîte de dialogue **[!UICONTROL Exporter]**, sélectionnez les éléments à exporter et un format dans lequel exporter les données.

   Boîte de dialogue d’exportation Admin Console ![](./assets/export-12.png)

4. Sélectionnez **[!UICONTROL Exporter]**. La génération du fichier d’exportation peut prendre plusieurs minutes. Une fois l’opération terminée, pour télécharger le rapport, accédez à **&#x200B;**&#x200B;> **[!UICONTROL Insights]** > **[!UICONTROL Export Reports]**.

>[!NOTE]
>
>Les fichiers JSON sont exportés au format zip. Vous pouvez les ouvrir à l’aide d’un utilitaire zip ou des fonctionnalités zip du système d’exploitation.

Après avoir téléchargé le fichier, vous pouvez manipuler les données, puis les importer à nouveau. Les mises à jour importées apparaissent dans Global Admin Console comme si vous aviez modifié manuellement les données.

## Importer la structure de l’organisation

En tant qu’[administrateur global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), vous pouvez importer des données potentiellement modifiées. Une fois chargées, les nouvelles données sont comparées aux données actuelles et toutes les modifications sont appliquées à la hiérarchie de l’organisation. Toutes les opérations d&#39;import sont effectuées sur la copie mise à jour de la hiérarchie de l&#39;organisation. Si des modifications sont en attente, elles seront ajoutées en plus des modifications en attente dans la hiérarchie.

### Étapes d’importation

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com). Dans l’onglet **[!UICONTROL Organisations]**, utilisez le sélecteur d’organisation pour sélectionner la hiérarchie d’organisations dans laquelle vous souhaitez effectuer l’importation.
2. Sélectionnez l’icône **[!UICONTROL Plus d’options]** **⋮** et sélectionnez **[!UICONTROL Importer]**. Selon la taille et la complexité du fichier d’importation, le traitement peut prendre de quelques secondes à plusieurs minutes.
3. Sélectionnez **[!UICONTROL Sélectionner un fichier]**, puis choisissez un fichier JSON, CSV ou XLSX à charger. Pour les fichiers CSV, un seul détail d’organisation peut être importé à la fois et cela ne prend pas en charge l’importation de produits. Les modifications importées semblent avoir été modifiées manuellement.
4. Sélectionnez **[!UICONTROL Fermer]**.
5. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]**. Sélectionnez ensuite **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html). Avant d’exécuter les modifications, les actions en attente sont affichées de la même manière que lorsque des modifications sont effectuées manuellement dans le Global Admin Console.

## Export et import de schémas

Lors de l’importation de données à l’aide d’un fichier CSV, les champs peuvent apparaître dans n’importe quel ordre, mais doivent toujours correspondre à leur ligne d’en-tête.

Lors de l’import de données, vous devez spécifier une opération pour chaque élément. L’opération peut être l’une des suivantes :

- Mise à jour : indique une modification.
- Créer : indique la création d’un objet (organisation, groupe d’utilisateurs ou administrateur, par exemple).
- Supprimer : indique la suppression d’un objet (par exemple, organisation, groupe d’utilisateurs ou administrateur).

Les enregistrements d’entrée sans champ d’opération ou vide sont ignorés.

### Organisations

<table>
  <tr>
    <th>Nom du champ</th>
    <th>Description</th>
    <th>Remarques</th>
  </tr>

<tr>
    <td>identifiant</td>
    <td>
      Identifiant de l’organisation.<br><br>
      Lors de l’ajout d’une nouvelle organisation, cela peut être vide ou défini sur un identifiant d’espace réservé, par exemple, .
      new_org_1. L’identifiant d’espace réservé est utilisé lorsque d’autres entrées importées doivent faire référence
      à cette organisation. Après la création, un ID d’organisation réel sera attribué et remplacera tous les
      utilise l’id d’organisation de l’espace réservé.
    </td>
    <td>Peut être défini sur une valeur temporaire lorsque operation=create</td>
  </tr>

<tr>
    <td>nom</td>
    <td>
      Nom simple de l’organisation. Longueur minimale 4, max 100.
      Les noms peuvent contenir jusqu’à 3 octets de caractères UTF-8.
      Les caractères à 4 octets ne sont pas pris en charge.
    </td>
    <td>
      Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement
    </td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>Code pays ou région</td>
    <td>
      Doit être défini lorsque operation=create, peut être mis à jour lorsque operation=update
    </td>
  </tr>

<tr>
    <td>type</td>
    <td>Type d'organisme</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      ID de l’organisation parent. Vide pour l’organisation racine.
      Lors de la mise à jour, des restrictions importantes s’appliquent, notamment le fait que le nouveau parent soit dans la même hiérarchie et
      disposer des produits présents dans l’organisation.
    </td>
    <td>
      Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement
    </td>
  </tr>

<tr>
    <td>adminCount</td>
    <td>Nombre d’administrateurs</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>domainCount</td>
    <td>Nombre de domaines</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Nombre d’utilisateurs</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>userGroupCount</td>
    <td>Nombre de groupes d’utilisateurs</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>administrateurs</td>
    <td>Ensemble d’objets admin représentant les administrateurs de cette organisation.</td>
    <td rowspan="6">
      Peut être manquant s’il n’est pas sélectionné pour l’exportation. Il s’affiche dans un onglet distinct dans les fichiers XLSX.
    </td>
  </tr>

<tr>
    <td>domaines</td>
    <td>Ensemble d’objets domaine représentant des domaines dans cette organisation.</td>
  </tr>

<tr>
    <td>produits</td>
    <td>Ensemble d’objets produit représentant des produits dans cette organisation.</td>
  </tr>

<tr>
    <td>productProfiles</td>
    <td>Ensemble d’objets de profil de produit représentant les profils de produit dans cette organisation.</td>
  </tr>

<tr>
    <td>userGroups</td>
    <td>Ensemble d’objets de groupe d’utilisateurs représentant des groupes d’utilisateurs dans cette organisation.</td>
  </tr>

<tr>
    <td>orgPolicies</td>
    <td>Structure représentant les politiques et leurs valeurs</td>
  </tr>

<tr>
    <td>opération</td>
    <td>
      Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données.
    </td>
    <td>Toujours vide à l'export.</td>
  </tr>
</table>


**Conditions d’importation requises :**

- Pour la mise à jour ou la suppression, orgId doit faire référence à une organisation existante dans votre hiérarchie.
- Si vous créez une organisation, vous pouvez laisser le champ orgId vide ou le définir sur un identifiant unique que vous pouvez créer (par exemple new-1 ou new-2). Ceci fournit un identifiant qui peut être utilisé pour faire référence à l’organisation à créer.
- Le code pays doit être valide.
- L’ID d’organisation pour l’opération *Mise à jour* et *Suppression* doit déjà être présent dans la hiérarchie de l’organisation.
- orgId marqué comme *Supprimer* ne doit pas être sélectionné en tant que parentOrgId pour les organisations avec une opération *Mettre à jour* ou *Créer*.
- Les organisations enfants au même niveau et du même parent ne doivent pas avoir les mêmes orgNames.
- Pour créer une organisation ou mettre à jour le nom d&#39;une organisation, le nom de l&#39;organisation ne doit pas correspondre au nom d&#39;un enfant existant du même parent.

### Administrateurs

<table>
  <tr>
    <th>Nom du champ</th>
    <th>Description</th>
    <th>Utilisation</th>
  </tr>

<tr>
    <td>orgId</td>
    <td>Référence à l’organisation dans laquelle réside l’administrateur.</td>
    <td>Utilisé comme référence pour rechercher des objets contenant ou associés.</td>
  </tr>

<tr>
    <td>Prénom</td>
    <td>
     Prénom de l’utilisateur administrateur.
Le prénom et le nom des utilisateurs d’Adobe ID peuvent être remplacés par une valeur fournie par l’utilisateur lorsque celui-ci accepte l’invitation.
    </td>
    <td rowspan="4">
      Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement
    </td>
  </tr>

<tr>
    <td>Nom</td>
    <td>Nom de l’utilisateur administrateur</td>
  </tr>

<tr>
    <td>E-mail</td>
    <td>Adresse e-mail de l’utilisateur administrateur. Il s’agit d’une clé primaire pour l’utilisateur et elle doit être unique.</td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>
Code de pays ou de région où opère l’utilisateur. S’applique uniquement aux types d’ID Federated et Enterprise.
    </td>
  </tr>

<tr>
    <td>userType</td>
    <td>Adobe ID, Enterprise ID ou Federated ID.</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>ADMINISTRATEUR GLOBAL, OBSERVATEUR GLOBAL, ADMINISTRATEUR SYSTÈME, ADMINISTRATEUR DU GROUPE D’UTILISATEURS, ADMINISTRATEUR DE PRODUIT, ADMINISTRATEUR DE PROFIL DE PRODUIT, ADMINISTRATEUR DE DÉPLOIEMENT ET STORAGE_ADMIN.</td>
    <td rowspan="5">Peut être défini lorsque operation=Create</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>ID de groupe du groupe dont cet utilisateur est administrateur. Pertinent uniquement pour les administrateurs de groupe d’utilisateurs et de profil de produit.</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>ID de licence de produit du produit dont cet utilisateur est administrateur. Pertinent pour les administrateurs de produit uniquement.</td>

</tr>

<tr>
    <td>domain</td>
    <td>Nom de domaine de l’utilisateur s’il n’utilise pas le domaine d’e-mail</td>

</tr>

<tr>
    <td>userName</td>
    <td>Nom d’utilisateur de l’utilisateur si l’adresse e-mail n’est pas utilisée</td>
  </tr>

<tr>
    <td>opération</td>
    <td>Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données.</td>
    <td></td>
  </tr>
</table>


**Conditions d’importation requises :**

- orgId, email, adminType et userType doivent contenir des valeurs valides.
- countryCode doit être valide.
- Si l’utilisateur existe déjà et est en cours de mise à jour, userType doit correspondre à l’utilisateur.
- Recherchez les adresses e-mail en double dans l’organisation.

### Profils de produit

Les exportations et importations de profils de produit se composent de deux parties : les détails du profil de produit et un ensemble de ressources associées au profil de produit. Ces ressources identifient les services qui peuvent être configurés, généralement simplement pour les activer ou les désactiver.

- Les objets de ressource sont imbriqués dans le profil de produit au format JSON.
- Lors de l’utilisation de CSV ou XLSX avec des profils de produit, les profils et les ressources sont combinés en un seul tableau. Il y aura plusieurs entrées pour le profil de produit, une pour chaque ressource.
- Le champ sélectionné dans la ressource contrôle si le service est activé.
- Lors de l’importation de profils de produit, une opération Créer ou Mettre à jour doit être effectuée sur le profil de produit lui-même et sur tout objet de ressource à mettre à jour ou à créer.


<table>
  <tr>
    <th>Nom du champ</th>
    <th>Description</th>
    <th>Utilisation</th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      Identifiant du profil produit
La valeur d’espace réservé peut être utilisée lors de la création afin que d’autres objets puissent référencer le nouveau profil.
    </td>
    <td>Peut être défini sur une valeur temporaire lorsque operation=create</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     Nom du profil de produit. Il ne peut pas s’agir d’un doublon d’autres profils de produit ou groupes d’utilisateurs de la même organisation.
    </td>
    <td rowspan="2">
   Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>Description textuelle du profil de produit</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>Référence de l’ID de licence au produit</td>
    <td rowspan="2"> Utilisé comme référence pour rechercher l’objet contenant ou associé
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
Organisation contenant le groupe d’utilisateurs
    </td>
  </tr>

<tr>
    <td>notifications</td>
    <td>True ou false pour indiquer si une notification par e-mail doit être envoyée aux utilisateurs lorsqu’ils sont ajoutés ou supprimés de ce profil de produit</td>
    <td>Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement</td>
  </tr>

<tr>
    <td>ressources</td>
    <td> Tableau des ressources associées à ce profil de produit.
Le champ Ressources est uniquement présent pour le format JSON. Pour les formats CSV et XLSX, les ressources sont représentées par les champs supplémentaires suivants : resourceName, resourceId, resourceDescription, icon, selected, quota, resourceType. Pour plus d’informations sur ces champs, consultez la section intitulée Produits et ressources.
Si le profil de produit comporte plusieurs ressources, plusieurs lignes sont présentes, une pour chaque ressource. Les autres champs auront les mêmes valeurs pour chaque ressource. </td>
    <td></td>
  </tr>

<tr>
    <td>opération</td>
    <td>Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données.</td>  
    <td></td>
  </tr>
</table>



**Conditions d’importation requises :**

- productProfileId, licenseId et orgId doivent avoir des valeurs valides.
- Lors de la création d’un profil de produit, productProfileName doit être un nom valide et ne doit pas dupliquer un autre nom de profil de produit ou nom de groupe d’utilisateurs dans la même organisation.
- Le champ de quota doit avoir une valeur valide pour le type d&#39;unité. Il est numérique ou illimité lorsque resourceType=QUOTA ou vide dans les autres cas.
- Le champ de notification doit être « true » ou « false ».
- Pour les importations CSV et XLSX, validez productProfileId ; toutes ses entrées doivent avoir les mêmes orgId, licenseId et productProfileName.
- Validez le productProfileName en double dans le fichier d’entrée et l’organisation.
- Les profils à mettre à jour et à supprimer doivent être présents dans l’organisation.
- Les ressources à mettre à jour et à supprimer (désactiver) doivent être présentes dans le profil.
- Pour que les profils soient créés, vérifiez les points suivants :
   - L’orgId doit être une nouvelle organisation ou une organisation existante.
   - L’ID de licence doit être un nouveau produit ou un produit existant.
   - Validez les ressources pour le profil.

### Ressources dans les profils de produit

<table>
  <tr>
    <th>Nom du champ</th>
    <th>Description</th>
    <th>Utilisation</th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>Nom de la ressource</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>Identifiant de la ressource</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>Description textuelle de la ressource</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>icon</td>
    <td>URL vers l’image pour la ressource</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>sélectionné</td>
    <td>
      Pour une entrée de configuration, si la fonction est activée.
      Ce champ est présent uniquement dans JSON.
    </td>
    <td rowspan="2">
      Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement.
    </td>
  </tr>

<tr>
    <td>quota</td>
    <td>
      Quantité de ressource principale qui peut être distribuée aux utilisateurs via ce profil de produit.
      Ce champ est présent uniquement dans JSON.
    </td>
  </tr>


<tr>
    <td>resourceType</td>
    <td>
      Si présent, la valeur est SERVICE. Elle indique que cette ressource représente un service qui peut être
      activé ou désactivé en fonction de la valeur du champ sélectionné.
      Ce champ est présent uniquement dans JSON.
    </td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>opération</td>
    <td>
      Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données.
    </td>
    <td></td>
  </tr>
</table>


**Conditions d’importation requises :**

- Le champ Opération des ressources est ignoré lorsque des opérations sont définies pour le profil de produits auquel elles appartiennent, à savoir *Supprimer* ou *Créer*.
- Aucune ressource ne doit être marquée pour suppression ; il s’agit d’une opération non valide.
- Pour que les profils de produit soient créés, le nombre de ressources doit correspondre au nombre de ressources du profil de produit source.
- Pour les ressources avec l’opération *Mise à jour*, la ressource doit être présente dans le profil de produit.

### Groupes d’utilisateurs

<table>
  <tr>
    <th>Nom du champ</th>
    <th>Description</th>
    <th>Utilisation</th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
      Identifiant du groupe d’utilisateurs. La valeur d’espace réservé peut être utilisée lors de la création afin que :
      d’autres objets peuvent référencer le nouveau groupe d’utilisateurs.
    </td>
    <td>Peut être défini sur une valeur temporaire lorsque operation=create</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td>Nom du groupe d’utilisateurs</td>
    <td rowspan="2">
      Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement.
    </td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>Description textuelle du groupe d’utilisateurs</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Nombre d’utilisateurs dans le groupe d’utilisateurs</td>
    <td>Lecture seule</td>
  </tr>

<tr>
    <td>profils</td>
    <td>
      Tableau des identifiants de profil de produit auxquels le groupe d’utilisateurs est associé.
      XLSX a une ligne par valeur avec les mêmes valeurs pour les autres champs.
    </td>
    <td>
      Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement.
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>Organisation contenant le groupe d’utilisateurs</td>
    <td>Utilisé comme référence pour rechercher l’objet contenant ou associé</td>
  </tr>

<tr>
    <td>opération</td>
    <td>
      Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données.
    </td>
    <td></td>
  </tr>
</table>

**Conditions d’importation requises :**

- orgId doit faire référence à une organisation existante ou en cours de création dans le même import.
- userGroupId doit faire référence à un groupe existant pour la mise à jour ou la suppression, et peut être un ID que vous définissez pour de nouveaux groupes d’utilisateurs.
- Pour la mise à jour ou la création, userGroupName ne doit pas être vide et ne doit pas dupliquer un autre nom de groupe d’utilisateurs ou de profil de produit dans la même organisation.
- Assurez-vous que userGroupName n’est pas dupliqué dans le fichier d’entrée et dans l’organisation.
- Les groupes d’utilisateurs à mettre à jour et à supprimer doivent être présents dans l’organisation.
- Le profil à supprimer du groupe d’utilisateurs doit être présent dans le groupe d’utilisateurs . Les opérations de mise à jour ne peuvent pas être effectuées sur le profil d’un groupe d’utilisateurs.
- Pour que des groupes d’utilisateurs soient créés, vérifiez les points suivants :
   - L’orgId doit être une nouvelle organisation ou une organisation existante.
   - L’ID de licence, le cas échéant, doit être un nouveau produit ou un produit existant.
   - productProfileId doit être un nouveau profil de produit ou un profil de produit existant.

### Domaines

Les informations sur les domaines fournissent des informations en lecture seule sur les domaines disponibles dans chaque organisation. Ces données ne sont pas modifiables.


| Nom du champ | Description | Utilisation |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | Référence à l’organisation dans laquelle ce domaine est répertorié | Utilisé comme référence pour rechercher des objets contenant ou associés. |
| domainName | Nom du domaine (par exemple, adobe.com). | Lecture seule |
| directoryName | Nom du répertoire dans lequel le domaine est listé | Lecture seule |
| directoryType | L’un des formats suivants : Federated ID ou Enterprise ID. | Lecture seule |
| domainStatus | L’UNE DES OPTIONS ACTIVE, RÉSERVÉE, NON RÉCLAMÉE, RÉCLAMÉE, VALIDÉE, RETIRÉE ET EXPIRÉE. | Lecture seule |


### Produits et ressources {#products-and-resources}

Dans les fichiers XLSX, il existe deux feuilles : une pour les produits et une pour les ressources. Dans JSON, les objets de ressource sont imbriqués dans l’objet de produit.

**Produits**


| Nom du champ | Description | Utilisation |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | Identifiant identifiant le produit. Chaque produit possède un ID de licence unique dans l’organisation dans laquelle il est répertorié. Lors de l’ajout d’un nouveau produit, cela peut être vide ou utiliser un identifiant d’espace réservé (par exemple, new_product_1). Après la création, un ID de licence réel est attribué et remplace tous les utilisateurs de l’ID de licence de l’espace réservé. | Peut être défini sur une valeur temporaire lorsque operation=create |
| productName | Nom du produit | Lecture seule |
| productDescription | Description textuelle du produit | Lecture seule |
| allowOverallocation | Valeur booléenne indiquant si la suraffectation de cette instance de produit est autorisée. La suraffectation fait référence à la possibilité d&#39;accorder plus de quantité à une organisation enfant que ce qui vous a été accordé. | Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement |
| icon | URL de l’icône de produit | Lecture seule |
| sourceLicenseId | ID de licence de l&#39;instance de produit dans l&#39;organisation à partir de laquelle ce produit a été alloué. La valeur est nulle si cette instance n’est pas un produit alloué, mais un produit acheté. | Peut être défini lorsque operation=Create |
| productId | Identifiant du produit. | Lecture seule |
| orgId | Identifiant de l’organisation contenant cette instance de produit | Utilisé comme référence pour rechercher l’objet contenant ou associé |
| redistribuable | Valeur booléenne indiquant si ce produit dispose de ressources pouvant être accordées aux organisations enfants. | Lecture seule |
| ressources | Objet contenant un ensemble d’objets de ressource représentant les ressources et les paramètres de ce produit |                                                                               |
| opération | Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données. |                                                                               |


**Conditions d’importation requises :**

- Pour créer, licenseId doit être un identifiant unique que vous créez.
- Pour la mise à jour, licenseId doit être l&#39;identifiant d&#39;un produit existant dans l&#39;organisation spécifiée.
- orgId doit faire référence à une organisation existante ou en cours de création dans la même opération d’importation.
- Pour créer, sourceLicenseId doit faire référence à un produit existant ou à l&#39;ID que vous avez défini pour un produit en cours de création au cours de la même opération d&#39;importation.
- licenseId et sourceLicenseId ne doivent pas être identiques pour les produits avec l&#39;opération *Create*.
- Validez les organisations de produits. L’organisation doit être nouvelle ou doit déjà être présente dans la hiérarchie de l’organisation.
- Pour les opérations *Mise à jour* et *Suppression*, le produit doit déjà être présent dans la hiérarchie de l’organisation.
- Le licenseId marqué comme *Delete* ne doit pas être utilisé comme sourceLicenseId des produits avec les opérations *Create* et *Update*.
- Pour les produits avec l’opération *Create*, vérifiez que le sourceLicenseId doit être présent dans l’organisation parent.

**Ressources pour les produits**

Les objets de ressource peuvent apparaître dans les produits et dans les profils de produit.


| Nom du champ | Description | Utilisation |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | Nom de la ressource | Lecture seule |
| resourceId | Identifiant de la ressource | Lecture seule |
| resourceDescription | Description textuelle de la ressource | Lecture seule |
| icon | URL vers l’image pour la ressource | Lecture seule |
| productName | Nom du produit dont fait partie cette ressource. | Lecture seule |
| licenseId | Identifiant de licence (instance de produit) du produit dont fait partie cette ressource. | Utilisé comme référence pour rechercher l’objet contenant ou associé |
| grantedQuantity | Quantité accordée de cette ressource : quantité de ressources dont dispose cette organisation pour être utilisée localement ou allouée à des organisations enfants. | Peut être défini ou mis à jour lorsque operation=create ou operation=update, respectivement |
| unité | Nom de l’unité de quantité de la subvention. | Lecture seule |
| currentQuantity | Quantité actuellement utilisable dans cette organisation. Il s&#39;agit de la quantité accordée moins les ressources allouées aux organisations enfants. Il s’agit de la valeur affichée dans Admin Console pour ce produit/cette ressource. | Lecture seule |
| provisionedQuantity | Quantité effectivement approvisionnée : peut être inférieure à grant ou current, peut être inférieure à currentQuantity si une limitation est en place. | Lecture seule |
| opération | Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données. |                                                                               |


**Conditions d’importation requises :**

Le champ Opération des ressources est ignoré lorsque des opérations sont définies pour le produit auquel elles appartiennent, à savoir *Supprimer* ou *Créer*.
- Aucune ressource ne doit être marquée pour suppression ; il s’agit d’une opération non valide.
- Pour les produits à créer, le nombre de ressources doit correspondre au nombre de ressources du produit source.
- Pour les ressources avec l’opération *Mise à jour*, la ressource doit être présente dans le produit.

## Importer et exporter des données d’allocation de produit

En tant qu’[administrateur global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), vous pouvez exporter les données d’attribution de produit sous la forme d’un fichier JSON ou CSV. Vous pouvez ensuite manipuler ces données et les charger à nouveau pour importer les modifications. Lorsque les données potentiellement modifiées sont chargées, les nouvelles données sont comparées aux données actuelles et toutes les modifications sont appliquées aux données d’attribution de produit. Vous pouvez ensuite vérifier et envoyer les modifications en attente pour qu’elles prennent effet.

## Exporter le modèle d’allocation de produit

Pour exporter le modèle d’attribution de produit, procédez comme suit :

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/) et accédez à l’onglet **[!UICONTROL Attribution du produit]**.
2. Sélectionnez l’icône **[!UICONTROL Plus d’options]** ⋮, puis sélectionnez **[!UICONTROL Exporter au format CSV]** ou **[!UICONTROL Exporter au format JSON]**. Votre fichier est téléchargé. [En savoir plus](#export-and-import-formats-for-product-allocation) sur les formats d’exportation.

## Importer le modèle d’allocation de produit

Vous pouvez exporter des données, les modifier, puis importer le fichier modifié. Pour importer le modèle d&#39;allocation de produit, procédez comme suit :

1. Connectez-vous à [&#128279;](https://global-admin-console.adobe.com/) et accédez à l’onglet **[!UICONTROL Attribution du produit]**.
2. Sélectionnez l’icône **[!UICONTROL Plus d’options]** ⋮ et sélectionnez **[!UICONTROL Importer]**.
3. Sélectionnez un fichier JSON ou CSV à charger.
4. Sélectionnez **[!UICONTROL Vérifier les modifications en attente]**. Après avoir examiné les modifications, sélectionnez **[!UICONTROL Envoyer les modifications]** pour les [exécuter](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Formats d’exportation et d’importation pour l’affectation de produits

Les formats d&#39;export et d&#39;import sont les mêmes. Lors de l’importation au format CSV, les champs peuvent apparaître dans n’importe quel ordre, mais ils doivent correspondre à la ligne d’en-tête. Lors de l’importation au format JSON, les champs peuvent apparaître dans n’importe quel ordre.

Vous devez spécifier l&#39;opération lors de l&#39;import des données d&#39;allocation de produit. L’opération peut être l’une des suivantes :

- Mise à jour : indique une modification (modification des valeurs grantedQuantity et allowOverAllocation).
- Créer : indique d’ajouter une ressource produit à l’organisation spécifiée.
- Supprimer : indique la suppression du produit.

Si aucune opération n’est fournie, aucune modification ne se produit lors de l’importation des données de cette ligne au format CSV ou de cet objet au format JSON.

Dans le fichier exporté, il existe une ligne ou un enregistrement pour chaque ressource de produit. Certains produits ont plus d’une ressource.

Si un produit comporte plusieurs ressources, les opérations de mise à jour peuvent s&#39;appliquer à des ressources indépendantes, une opération de suppression supprime le produit, y compris toutes les ressources d&#39;une organisation, et une opération de création nécessite un enregistrement pour chacune des ressources du fichier d&#39;importation afin que la quantité appropriée de chacune d&#39;elles puisse être spécifiée. Le champ allowOverAllocation est à l&#39;échelle du produit et peu importe dans quelle ressource se trouve une mise à jour de ce champ.

### Description des en-têtes


| Nom du champ | Description | Utilisation |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| productName | Nom du produit. | Lecture seule |
| licenseId | ID d’un produit (unique à un produit dans une organisation). Lors de l’ajout d’un nouveau produit, cela peut être vide ou défini sur un identifiant d’espace réservé (par exemple, new_product_1). L’identifiant d’espace réservé est utilisé dans les cas où d’autres entrées importées doivent faire référence à ce produit. Après la création, un ID de licence réel sera attribué et remplacera tous les utilisateurs de l’ID de licence de l’espace réservé. | Peut être défini lorsque operation=Create |
| sourceLicenseId | ID du produit parent. Il est vide ou nul s’il s’agit d’un achat au lieu d’une affectation. | Peut être défini lorsque operation=Create |
| productId | Identifiant qui identifie cette classe de produits. Cet ID est partagé entre les produits du même type et diffère de l’ID de licence qui identifie une instance de ce produit. | Lecture seule |
| resourceName | Nom de cette ressource produit. Par exemple, les licences utilisateur. | Lecture seule |
| resourceId | Identifiant qui identifie cette ressource de produit. | Peut être défini lorsque operation=Create |
| orgPathName | Chemin d’accès de l’organisation dans laquelle se trouve cette ressource de produit. Segments séparés par « / ». | Lecture seule |
| orgName | Nom simple de l’organisation contenant cette ressource de produit. Il s’agit du dernier segment de orgPathName. | Lecture seule |
| orgId | ID d&#39;organisation de l&#39;organisation contenant cette ressource de produit. | Peut être défini lorsque operation=Create |
| grantedQuantity | Nombre d&#39;unités de quantité de ressource accordées à cette organisation par son parent ou montant acheté si cette entrée de ressource de produit représente un achat. Ce champ peut être mis à jour, sauf pour les produits achetés ou les allocations racines que l&#39;administrateur global n&#39;est pas autorisé à modifier. | Peut être mis à jour lorsque operation=Update ou operation=Create |
| unité | Nom de l’unité de ressource. Par exemple, Utilisateurs. | Lecture seule |
| totalAllocations | Somme des subventions accordées aux organisations enfants de cette organisation pour cette ressource de produit. Cette valeur comprend les subventions directes aux enfants immédiats ainsi que les suraffectations de ces organisations. Par exemple, si cette organisation a accordé à un enfant 10 et que celui-ci lui a ensuite attribué son enfant 25, le totalAllocations serait de 25 : les 10 accordées à l’enfant plus un excédent de 15 pour cet enfant. | Lecture seule |
| grantOverage | Montant de l&#39;excédent de totalAllocations sur le totalQuantity accordé. Si totalAllocations ne dépasse pas grantedQuantity, cette valeur est nulle ou nulle. | Lecture seule |
| localLicensedQuantity | Montant de cette ressource allouée à cette organisation restant à utiliser après déduction de la quantité allouée aux enfants. Il s’agit du montant affiché comme disponible dans Admin Console. Cette valeur peut être nulle, mais elle n’est jamais négative, même si cette organisation a suraffecté des ressources à ses enfants. | Lecture seule |
| localUsage | Nombre d&#39;unités de la ressource utilisée dans cette organisation. Par exemple, la délégation d’une licence utilisateur à un utilisateur est comptabilisée comme 1 unité d’utilisation. | Lecture seule |
| totalUsage | Nombre d&#39;unités de la ressource utilisée par cette organisation et tous les enfants. Cela indique l’utilisation de cette ressource dans la partie de la hiérarchie d’organisation enracinée par cette organisation. | Lecture seule |
| useOverage | Montant de l&#39;utilisation totale sur la subvention de l&#39;organisation (l&#39;organisation et les enfants ont utilisé plus de la ressource que disponible). Cette valeur affiche une valeur différente de zéro lorsque totalUsage dépasse localLicensedQuantity. | Lecture seule |
| allowOverAllocation | Indique si l&#39;utilisateur est autorisé à accorder davantage de ressources aux enfants même s&#39;il n&#39;en a plus à accorder (autorisé à accorder malgré le dépassement de la subvention). Cette valeur s’applique à toutes les ressources de ce produit. Si une tentative est effectuée pour mettre à jour allowOverallocation pour plusieurs ressources du même produit à différentes valeurs, le résultat est aléatoire. | Peut être mis à jour lorsque operation=Update |
| isPurchasedProduct | true si le produit est un produit acheté (non alloué par le parent). Cela équivaut à une valeur vide pour sourceLicenseId. | Lecture seule |
| redistribuable | true si le produit peut être alloué à des enfants, false signifie que le produit n’est disponible que dans l’organisation dans laquelle il est affiché et que les ressources ne peuvent pas être allouées à une autre organisation. | Lecture seule |
| opération | Valeur parmi vide, Créer, Mettre à jour ou Supprimer. Action à effectuer lors de l’importation des données. |                                                          |


**Exigences d’importation**

**Validation des données**

- Le champ opération doit comporter une opération valide.
- Les données d’importation de produit doivent comporter des propriétés et des valeurs pour les champs obligatoires.
- Les propriétés des données d’importation de produit doivent être du type correct.
- Le champ Politique de produit (sur-affectation) ne doit pas être fourni pour différentes ressources.
- Le champ grantedQuantity :
   - Ne peut pas être modifié en *illimité* s’il n’est pas déjà *illimité*.
   - Doit être un entier non négatif ou la valeur de chaîne *illimitée.*

**Autorisation/validation accessible**

- L&#39;organisation associée aux données d&#39;importation doit exister. Si vous effectuez une mise à jour, vérifiez que le produit et la ressource associés aux données d’importation existent réellement.

**Ajouter la validation du produit**

- SourceLicenseId doit exister.
- L&#39;organisation associée au nouveau produit doit exister.
- Le produit en cours de création ne doit pas exister (produit avec le même ID de licence).
- Les ressources associées à un produit en cours de création doivent avoir un productId correspondant à ce produit.
