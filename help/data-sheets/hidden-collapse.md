---
title: Bogue de réduction de sections
description: Sections réductibles UGP-13446 non rendues, peut-être en raison d'onglets de page incorporés
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# Sections réductibles

<http://jira.corp.adobe.com/browse/UGP-13446> Sections réductibles UGP-13446 non rendues, peut-être en raison d&#39;onglets de page incorporés

## Exemples

La première avec les onglets de page, la seconde sans

### Option 2 : avec onglets de page

+++ Installation manuelle du correctif pour 6.5.18.0 - 6.5.22.0

**Étape 1 : télécharger et extraire le package de correctif**

- Téléchargez le [correctif pour 6.5.18.0 - 6.5.22](https://www.adobe.com) à partir du portail de distribution de logiciels Adobe
- Extraire localement

**Étape 2 : Accédez au dossier de version approprié**

- En fonction de la version du pack de services installée sur votre environnement, accédez au dossier correspondant.

  Exemple pour le pack de services 20, le dossier est :

  ```
  <extracted-hotfix>/SP20/
  ```

**Étape 3 : Rechercher le répertoire de déploiement**

- Sur votre serveur AEM Forms on JEE, accédez à :

  ```
  [AEM installation directory]/deploy
  ```

  Exemple : `adobe/adobe-experience-manager-forms/deploy`



**Étape 4 : mettre à jour et remplacer les fichiers EAR**

>[!BEGINTABS]

>[!TAB JBoss]

1. Ouvrez `adobe-core-jboss.ear` et remplacez `adminui.war` par .

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. Dans le `adobe-core-jboss.ear` , accédez au dossier `lib/` et remplacez `adobe-uisupport.jar` par :

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Sauve l&#39;oreille. Assurez-vous que les modifications sont correctement enregistrées.


1. Remplacer `adobe-edcserver-jboss.ear` par

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. Remplacer `adobe-forms-jboss.ear` par

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. Ouvrez `adobe-core-weblogic.ear` et remplacez `adminui.war` par .

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. Dans le `adobe-core-weblogic.ear`, remplacez `adobe-uisupport.jar` par :

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Sauve l&#39;oreille. Assurez-vous que les modifications sont correctement enregistrées.


1. Remplacer `adobe-edcserver-weblogic.ear` par

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. Remplacer `adobe-forms-weblogic.ear` par

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB  WebSphere ]

1. Ouvrez `adobe-core-websphere.ear` et remplacez `adminui.war` par .

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. Dans le `adobe-core-websphere.ear`, remplacez `adobe-uisupport.jar` par :

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Sauve l&#39;oreille. Assurez-vous que les modifications sont correctement enregistrées.


1. Remplacer `adobe-edcserver-websphere.ear` par

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. Remplacer `adobe-forms-websphere.ear` par

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   Par exemple : `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**Étape 5 : mettre à jour le fichier `adobe-rightsmanagement-<appserver>-dsc.jar`avec**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Par exemple : `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Étape 6 : configuration supplémentaire pour Document Security sur WebSphere et WebLogic** :

Si vous utilisez Document Security (anciennement Rights Management), définissez la propriété système Java suivante (argument JVM) avant de démarrer le serveur AEM Forms :

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Étape 7 : réexécutez Configuration Manager**

- Lancez Configuration Manager pour redéployer le fichier EAR mis à jour et appliquer le correctif

+++

### Option 2 : sans onglets de page

+++ Installation manuelle du correctif pour 6.5.18.0 - 6.5.22.0

**Étape 1 : télécharger et extraire le package de correctif**

- Téléchargez le [correctif pour 6.5.18.0 - 6.5.22](https://www.adobe.com) à partir du portail de distribution de logiciels Adobe
- Extraire localement

**Étape 2 : Accédez au dossier de version approprié**

- En fonction de la version du pack de services installée sur votre environnement, accédez au dossier correspondant.

  Exemple pour le pack de services 20, le dossier est :

  ```
  <extracted-hotfix>/SP20/
  ```

**Étape 3 : Rechercher le répertoire de déploiement**

- Sur votre serveur AEM Forms on JEE, accédez à :

  ```
  [AEM installation directory]/deploy
  ```

  Exemple : `adobe/adobe-experience-manager-forms/deploy`



**Étape 4 : mettre à jour et remplacer les fichiers EAR**

Onglets de page supprimés

**Étape 5 : mettre à jour le fichier `adobe-rightsmanagement-<appserver>-dsc.jar`avec**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Par exemple : `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Étape 6 : configuration supplémentaire pour Document Security sur WebSphere et WebLogic** :

Si vous utilisez Document Security (anciennement Rights Management), définissez la propriété système Java suivante (argument JVM) avant de démarrer le serveur AEM Forms :

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Étape 7 : réexécutez Configuration Manager**

- Lancez Configuration Manager pour redéployer le fichier EAR mis à jour et appliquer le correctif

+++

Ailette
