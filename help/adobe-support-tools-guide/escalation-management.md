---
title: Gestion des remontées d’informations
description: La gestion des remontées d’informations fournit des options en libre-service dans l’assistance Experience League pour afficher les résumés des cas, demander des rappels, planifier des sessions de dépannage, mettre à jour l’urgence des cas et gérer les remontées d’informations d’assistance.
source-git-commit: d41e987c8778849311922d1b9438c2c74fb60138
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 1%

---

# Gestion des remontées d’informations

La **gestion des remontées d’informations** est une fonctionnalité en libre-service de l’assistance d’Adobe Experience League. Il permet aux clients d’agir directement sur les cas d’assistance, offre une visibilité sur les cas en temps réel par le biais de résumés générés par l’IA et propose des options d’escalade structurées pour prendre en charge une résolution plus rapide des problèmes critiques.

## Récapitulatif du cas

La fonctionnalité **[!UICONTROL Résumé du cas]** fournit un aperçu généré par l’IA d’un cas d’assistance. Il résume les commentaires, les actions et les interactions à ce jour afin que vous puissiez consulter le dernier statut sans lire l’historique complet du dossier.

Pour accéder au **[!UICONTROL Résumé du cas]**, procédez comme suit :

1. Accédez à **[!UICONTROL Mes cas]** dans l’assistance d’Adobe Experience League.
2. Recherchez le dossier que vous souhaitez examiner dans la liste des cas.
3. Dans la colonne **[!UICONTROL Synthèse des cas]**, cliquez sur **Synthèse des cas**.

![Résumé du cas](/help/adobe-support-tools-guide/assets/case-summary.png)

Le panneau Résumé du cas s’ouvre et affiche le résumé généré par l’IA avec les informations suivantes :

- Produit Adobe pour lequel le dossier est soumis
- Nombre de jours pendant lesquels le dossier a été ouvert
- **État actuel** - Énoncé concis de l&#39;état d&#39;avancement actuel du dossier
- **Prochaines étapes** - Un aperçu des actions entreprises par l’équipe d’assistance ou d’ingénierie et des étapes suivantes.
- **Résumé** - Détails sur le problème, y compris la description du problème et l’impact commercial
- **Principales mises à jour** - Une liste chronologique des mesures et mises à jour importantes pour le cas à ce jour.

>[!NOTE]
>
>L&#39;indicateur d&#39;état du dossier affiche l&#39;état actuel du dossier. Si le dossier est ouvert, il indique le nombre de jours pendant lesquels il l&#39;a été (par exemple, **Ouvert depuis 6 jours**). Si le litige est clos, l&#39;écran indique **[!UICONTROL Clôturé]**.

![Résumé de cas AI](/help/adobe-support-tools-guide/assets/ai-case-summary.png)

## Obtenir de l’aide

La fonctionnalité **[!UICONTROL Obtenir de l’aide]** permet aux clients d’appeler et de gérer les remontées d’assistance directement depuis la liste de cas, sans contacter l’assistance par e-mail ou par téléphone. En fonction de la priorité de cas, l’assistance d’Adobe Experience League affiche les options d’escalade en libre-service pertinentes.

Pour accéder à **[!UICONTROL Obtenir de l’aide]**, procédez comme suit :

1. Accédez à **[!UICONTROL Mes cas]** dans l’assistance d’Adobe Experience League.
1. Recherchez le dossier que vous souhaitez escalader dans la liste des dossiers.
1. Dans la colonne **[!UICONTROL Aide supplémentaire]**, cliquez sur **[!UICONTROL Obtenir de l&#39;aide]** pour le dossier.

   >[!NOTE]
   >
   >L&#39;option **[!UICONTROL Obtenir de l&#39;aide]** n&#39;est disponible que pour les dossiers ouverts et n&#39;apparaît pas pour les dossiers fermés.

1. Examinez le panneau de réaffectation. Il affiche le produit sélectionné, la priorité de cas, l’ID de cas et les options d’escalade disponibles. Les options disponibles peuvent inclure :

   - [!UICONTROL Demander un appel immédiat]
   - [!UICONTROL Demander un appel planifié]
   - [!UICONTROL Modification de l&#39;urgence du problème]
   - [!UICONTROL J&#39;ai un problème qui n&#39;est pas répertorié]

![Obtenir de l’aide](/help/adobe-support-tools-guide/assets/get-help.png)

### Demander un appel immédiat

L’option **[!UICONTROL Demander un appel immédiat]** est disponible pour les cas **P1-Critique**. Utilisez cette option pour demander un rappel immédiat par téléphone à un ingénieur du support technique.

>[!NOTE]
>
>Vous ne pouvez demander qu’un seul rappel à la fois. Vous pouvez demander un autre rappel une fois le premier appel terminé.

>[!NOTE]
>
>Cette option est disponible pour tous les produits, à l’exception de Adobe Experience Platform (AEP), [!DNL Commerce] et [!DNL GenStudio].

Pour demander un rappel immédiat, procédez comme suit :

1. Dans le panneau **[!UICONTROL Obtenir de l’aide]**, sélectionnez **[!UICONTROL Demander un appel immédiat]**, puis cliquez sur **[!UICONTROL Continuer]**.
1. Le formulaire de demande de rappel s’affiche, prérempli avec le produit, la priorité et l’ID de cas sélectionnés. Renseignez les champs obligatoires du formulaire.
   - Saisissez le numéro de téléphone à appeler.
   - Saisissez une brève description du problème ou la raison de la demande de rappel (jusqu’à 1 000 caractères).
1. Cliquez sur **[!UICONTROL Demander le rappel]** pour soumettre la demande, ou cliquez sur **[!UICONTROL Précédent]** pour revenir à l’écran précédent.

Une fois la demande soumise, l’écran de confirmation s’affiche :

- &#x200B;
- Numéro de téléphone
- Produit
- Identifiant du cas
- Titre du dossier
- Priorité

Un ingénieur du support technique vous contacte dès qu’il est disponible. Cliquez sur **[!UICONTROL Fermer]** pour ignorer la confirmation.

### Demander un appel planifié

L’option **[!UICONTROL Demander un appel planifié]** est disponible pour les cas **P2-Urgent** et **P3-Important**. Utilisez cette option pour planifier une réunion web de partage d’écran avec un ingénieur du support technique à une date et une heure qui vous conviennent.

>[!NOTE]
>
>Vous ne pouvez planifier qu’un seul appel à la fois. Une fois la réunion en cours terminée, vous pouvez planifier un autre appel.

>[!NOTE]
>
>Cette option est disponible pour tous les produits, à l’exception de Adobe Experience Platform (AEP), [!DNL Commerce] et [!DNL GenStudio].

Pour demander un appel planifié, procédez comme suit :

1. Dans le panneau **[!UICONTROL Obtenir de l’aide]**, sélectionnez **[!UICONTROL Demander un appel planifié]**, puis cliquez sur **[!UICONTROL Continuer]**.
1. Un formulaire de planification s’affiche, prérempli avec le produit, la priorité et l’ID de cas sélectionnés. Renseignez les champs obligatoires du formulaire.
   - **[!UICONTROL De quoi voulez-vous discuter ?]** : fournissez une brève description pour aider l’ingénieur d’assistance à se préparer (jusqu’à 1 000 caractères).
   - **[!UICONTROL Sélectionner une date]** : permet de sélectionner une date dans le calendrier.
   - **[!UICONTROL Sélectionner un intervalle de temps]** : sélectionnez une heure disponible pour la date choisie.
1. Cochez la case accusé de réception pour confirmer que le contenu personnel ou sensible est fermé avant le partage d’écran.
1. Cliquez sur **[!UICONTROL Planifier l’appel]** pour confirmer la réservation, ou cliquez sur **[!UICONTROL Précédent]** pour revenir à l’écran précédent.

Une fois la réunion programmée, l&#39;écran de confirmation s&#39;affiche :

- Adobe ID
- Lien de la réunion
- Date de la réunion
- Heure de la réunion
- Fuseau horaire
- Priorité
- Identifiant du cas
- Produit
- Ingénieur d’assistance
- Titre du dossier

Un ingénieur du support technique est disponible pour vous aider par partage d’écran au moment prévu. L&#39;invitation à la réunion comprend un lien Microsoft Teams pour rejoindre la réunion. Sélectionnez **[!UICONTROL Fermer]** pour ignorer la confirmation.

### Modification de l&#39;urgence de l&#39;événement

L&#39;option **[!UICONTROL Changement dans l&#39;urgence de l&#39;événement]** est disponible pour les cas **P3-Important** et **P4-Mineur**. Utilisez cette option pour modifier la priorité de casse jusqu&#39;à **P2-Urgent**.

>[!NOTE]
>
>Vous pouvez modifier la priorité de **P4-Mineur** en **P3-Important** ou de **P3-Important** en **P2-Urgent** une fois dans 24 heures.

Pour modifier l’urgence d’un problème, procédez comme suit :

1. Dans le panneau **[!UICONTROL Obtenir de l’aide]**, sélectionnez **[!UICONTROL Modifier l’urgence du problème]**.
1. Un champ de texte intégré s’affiche. Sur le terrain, décrivez clairement ce qui a changé ou pourquoi la question nécessite maintenant une attention immédiate.
1. Cliquez sur **[!UICONTROL Mettre à jour l&#39;urgence de l&#39;événement]** pour soumettre la demande, ou sur **[!UICONTROL Annuler]** pour quitter sans apporter de modifications.

   Une fois la demande soumise, l’écran de confirmation s’affiche :

   - Produit sélectionné
   - Priorité
   - Identifiant du cas

1. Cliquez sur **[!UICONTROL Revenir au formulaire]** pour revenir au dossier.

### J&#39;ai un problème non répertorié

L’option **[!UICONTROL J’ai un problème non répertorié]** est disponible pour toutes les priorités de cas et permet l’escalade lorsque d’autres options disponibles ne répondent pas au problème. Cette option garantit que le dossier reçoit l’attention directe d’un ingénieur de l’assistance.

Suivez les étapes ci-dessous pour signaler les problèmes qui ne sont pas répertoriés :

1. Dans le panneau **[!UICONTROL Obtenir de l’aide]**, sélectionnez **[!UICONTROL Je rencontre un problème non répertorié]**. Deux champs intégrés s’affichent.
1. Renseignez les champs intégrés :
   - **[!UICONTROL Pourquoi voulez-vous escalader cette affaire ?]**
   - **[!UICONTROL Nous pouvons mieux vous aider avec des informations détaillées.]**
1. Dans la liste déroulante, sélectionnez un motif de réaffectation :
   - [!UICONTROL Délai de résolution]
   - [!UICONTROL La résolution n’a pas répondu aux attentes]
   - [!UICONTROL Compétences en communication agent]
   - [!UICONTROL Connaissances techniques de l’agent]
1. Dans le champ de texte libre, fournissez un contexte supplémentaire sur la réaffectation.
1. Cliquez sur **[!UICONTROL Escaler le cas]** pour envoyer l’escalade, ou cliquez sur **[!UICONTROL Annuler]** pour quitter sans envoyer.

   Une fois la réaffectation envoyée, l’écran de confirmation s’affiche :

   - Produit sélectionné
   - Priorité
   - Identifiant du cas

1. Cliquez sur **[!UICONTROL Revenir au formulaire]** pour revenir au dossier.
