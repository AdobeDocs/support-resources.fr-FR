---
title: Notes de mise à jour du nouveau formulaire de cas EXL
description: Dernières informations de mise à jour pour le formulaire de dossier EXL.
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 8%

---


# Notes de mise à jour du nouveau formulaire de cas EXL

La nouvelle expérience de création de dossier introduit un formulaire actualisé conçu pour rationaliser la résolution des problèmes et comprend les éléments suivants :

![Nouveau](../adobe-support-tools-guide/assets/new.svg) - Nouvelles fonctionnalités
![Correctif](../adobe-support-tools-guide/assets/fix.svg) - Correctifs et améliorations
![Bug](../adobe-support-tools-guide/assets/bug.svg) - Problèmes connus

## Version 1.0 - Formulaire de création de dossier amélioré

*vendredi 15 janvier 2026*

![Nouveau](../adobe-support-tools-guide/assets/new.svg) Le formulaire de dossier est organisé en un flux guidé, ce qui permet aux utilisateurs et aux utilisatrices de comprendre les informations requises à chaque étape :

- [!UICONTROL Sélection de produits]
- [!UICONTROL Détails de l&#39;événement]
- [!UICONTROL Informations système]
- [!UICONTROL Impact]
- [!UICONTROL Coordonnées]
- [!UICONTROL Vérifier et envoyer]

![Nouveau](../adobe-support-tools-guide/assets/new.svg) Ajoutée **Nouvelle [!UICONTROL Procédure de reproduction] Champ** pour capturer des détails exploitables et accélérer la résolution des problèmes.

![Nouveau](../adobe-support-tools-guide/assets/new.svg) Ajout de **champs supplémentaires [!UICONTROL Contexte d’environnement]** pour les produits autorisés afin de capturer des détails importants :

- **Marketo**
   - ID Munchkin
- **Adobe Target**
   - Nom de l’activité
   - URL du site (nom de propriété des balises) / journal HAR ou Assurance
- **Adobe Analytics**
   - RSID
   - URL du site (nom de la propriété des balises) / journal HAR ou Assurance / cURL / journal de débogage
   - Lien court de Workspace
- **Adobe Journey Optimizer (AJO)**
   - ID de parcours ou URL de Parcours
   - Exemple de profil
- **Real-Time Customer Data Platform (RTCDP)**
   - Identifiant du composant affecté (identifiant de destination, identifiant de profil, identifiant d’audience, identifiant de jeu de données ou identifiant de flux de données)
   - Fichier HAR/Journaux Assurance
- **Customer Journey Analytics (CJA)**
   - projet Workspace
   - Nom de la propriété des balises


![Nouveau](../adobe-support-tools-guide/assets/new.svg) Ajout d’un **Panneau de recommandations[!UICONTROL  piloté par l’IA]** pour afficher des conseils utiles sans interrompre le flux de création de dossier.

![Nouveau](../adobe-support-tools-guide/assets/new.svg) Ajout d’une étape [!UICONTROL Résumé de la révision] pour fournir une vue consolidée de toutes les informations saisies et permettre aux utilisateurs de :

- Consulter les détails du dossier à un seul endroit
- Revenez aux étapes précédentes pour apporter des modifications
- Revenir au résumé sans perdre la progression

![Correction](../adobe-support-tools-guide/assets/fix.svg) le champ de description de cas renommé devient *[!UICONTROL « Veuillez décrire le problème »]* pour plus de clarté.

![Corriger](../adobe-support-tools-guide/assets/fix.svg) Ajout d’un astérisque (*) comme indicateurs de champ obligatoires pour garantir l’exhaustivité et réduire les erreurs d’envoi.
