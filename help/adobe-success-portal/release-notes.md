---
title: Notes de mise à jour du portail Adobe Success
description: Les dernières informations de mise à jour pour [!DNL Adobe Success portal].
feature: Release Notes
exl-id: be268e05-8298-4f21-8f2f-f66c52d76fe3
source-git-commit: 2894190b3171228e9c14a7cdef5bb2d92b97a6ec
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 83%

---

# Notes de mise à jour d’[!DNL Adobe Success portal]

Ces notes de mise à jour contiennent des mises à jour d’[!DNL Adobe Success portal] et comprennent les éléments suivants :

![Nouveau](../adobe-success-portal/assets/new.svg) - Nouvelles fonctionnalités
![Correctif](../adobe-success-portal/assets/fix.svg) - Correctifs et améliorations
![Bug](../adobe-success-portal/assets/bug.svg) - Problèmes connus

## 4,0

_1 novembre 2025_

![Corriger](../adobe-success-portal/assets/fix.svg) Optimisation de l’ordre de conversation dans la page des détails de l’incident pour faire défiler automatiquement le message le plus récent.

![Correction](../adobe-success-portal/assets/fix.svg) Mise à jour des détails de la casse. Lors de son ouverture dans un nouvel onglet à l’aide de **Ctrl+Clic** / **Commande+Clic**, le bouton Précédent est correctement désactivé pour éviter les erreurs de navigation.

![Bogue](../adobe-success-portal/assets/bug.svg) Correction d’un problème en raison duquel des détails incorrects de statut, de région ou de fuseau horaire s’affichaient pour les alertes **[!UICONTROL Statut d’Adobe]** dans **[!UICONTROL Assistance et informations]**.

![bug](../adobe-success-portal/assets/bug.svg) résolution des problèmes d’affichage avec les **[!UICONTROL accélérateurs]** et **[!UICONTROL activités]** liés aux **[!UICONTROL partenaires stratégiques]**.

## 3.0

_9 octobre 2025_

![Nouveau](../adobe-success-portal/assets/new.svg) Ajout d’une vue Calendrier au module **[!UICONTROL Plan d’action]** pour visualiser les chronologies des **[!UICONTROL accélérateurs]** et **[!UICONTROL activités]** liés aux **[!UICONTROL objectifs commerciaux clés]** (KBO).
* Accédez au calendrier à partir de la page des KBO du plan d’action ou des pages de détails **[!UICONTROL KBO]**/**[!UICONTROL Accélérateur]**/**[!UICONTROL Activité]** (uniquement si elles sont liées à un KBO).
* Basculez entre la vue Liste (par défaut) et la vue Calendrier.
* Le calendrier affiche des sections réductibles pour chaque KBO :
   * Bleu pour les **[!UICONTROL accélérateurs]**
   * Vert pour les **[!UICONTROL activités]**
* Chaque **[!UICONTROL accélérateur]**/ **[!UICONTROL activité]** affiche le nom, le statut et les dates de début/fin (au format *Mois XX*, *AAAA*).
* Cliquez sur une carte d’événement pour ouvrir une page contenant les détails de l’événement. Cliquer sur le bouton Précédent vous ramène au .
* Les événements ont un code couleur : bleu pour les **[!UICONTROL accélérateurs]**, vert pour les **[!UICONTROL activités]**. Faites défiler verticalement les KBO et horizontalement, par semaine ou par mois.
* Les infobulles affichent les noms complets lorsque le texte est tronqué et la chronologie reste visible lors du défilement.
* La vue par défaut est celle de la semaine en cours ; les flèches de navigation permettent de passer d’une semaine à l’autre.
* La vue Mois fournit une chronologie claire des travaux en cours et prévus.

![Correction](../adobe-success-portal/assets/fix.svg) Amélioration des pages **[!UICONTROL Objectifs commerciaux clés]** et **[!UICONTROL Activités]** dans le **[!UICONTROL Plan d’action]** afin d’afficher des infobulles sur les dates d’achèvement, ce qui améliore la visibilité de la chronologie.

![Correctif](../adobe-success-portal/assets/fix.svg) Recherche ajoutée dans les filtres sur **[!UICONTROL Plan d’action]** et **[!UICONTROL Suivi des résultats]** pour une navigation plus rapide.


![Correctif](../adobe-success-portal/assets/fix.svg) Ajout d’infobulles à chaque résultat afin d’obtenir rapidement le contexte.

![Correctif](../adobe-success-portal/assets/fix.svg) Ajout de la marque Adobe aux fichiers PDF téléchargés à partir des résultats et des cas.

![Correctif](../adobe-success-portal/assets/fix.svg) Affichage de tous les **[!UICONTROL partenaires stratégiques]** associés à un compte, avec des indicateurs pour les contacts principaux.

![Correctif](../adobe-success-portal/assets/fix.svg) Correction d’un problème en raison duquel les fuseaux horaires dans **[!UICONTROL Alertes et statut Adobe]** ne reflétaient pas correctement le profil de l’utilisateur connecté.

![Correctif](../adobe-success-portal/assets/fix.svg) Correction d’un problème en raison duquel les filtres **[!UICONTROL Alertes et statut Adobe]** ne fonctionnaient pas ensemble comme prévu.

![Correctif](../adobe-success-portal/assets/fix.svg) Correction d’un problème en raison duquel le tri des pages **[!UICONTROL Cas d’utilisation]** sur les Détails KBO et **[!UICONTROL Suivi des résultats]** était incohérent.

![Correction](../adobe-success-portal/assets/fix.svg) Correction d’un problème en raison duquel l’infobulle de la page de liste des cas n’affichait pas le nom complet du cas lorsque vous passiez la souris sur le titre d’un cas.

![Correctif](../adobe-success-portal/assets/fix.svg) Correction d’un problème en raison duquel l’icône de flèche arrière s’affichait incorrectement dans le navigateur Safari.

## 2.0

_11 septembre 2025_

![Nouveau](../adobe-success-portal/assets/new.svg) Ajout des champs suivants à la page **[!UICONTROL Détails des activités]** :

* **[!UICONTROL Priorité]** : indique le niveau de priorité d’une activité. Les valeurs disponibles sont *Urgent*, *Élevée*, *Normale*, *Faible* et *Aucune*. Si la valeur est *Aucune*, le champ **[!UICONTROL Priorité]** n’est pas visible dans l’UI du portail.
* **[!UICONTROL Propriétaire Adobe]** : affiche la personne propriétaire Adobe désignée pour l’activité.
* **[!UICONTROL Propriétaire chez le client ou la cliente]** : affiche la personne propriétaire chez le client ou la cliente.
* **[!UICONTROL Étapes suivantes]** : affiche les actions suivantes capturées pour l’activité.
* **[!UICONTROL Solutions Adobe]** : indique les solutions Adobe liées à l’activité.

![Correctif](../adobe-success-portal/assets/fix.svg) Amélioration des pages **[!UICONTROL Objectifs commerciaux principaux]** et **[!UICONTROL Activités]** dans le **[!UICONTROL Plan d’action]** afin d’afficher les dates d’achèvement de chaque accélérateur et activité, ce qui améliore la visibilité des chronologies.

![Correctif](../adobe-success-portal/assets/fix.svg) Amélioration de l’affichage des **[!UICONTROL Cas d’utilisation]** sur la page **[!UICONTROL Détails KBO]** afin d’assurer une conception plus épurée, une meilleure convivialité et une navigation cohérente.

![Correction](../adobe-success-portal/assets/fix.svg) Correction du problème en raison duquel une action **Ctrl+Clic** (ou **Commande+Clic** sur Mac) sur les liens des cas n’ouvraient pas le lien dans un nouvel onglet.
