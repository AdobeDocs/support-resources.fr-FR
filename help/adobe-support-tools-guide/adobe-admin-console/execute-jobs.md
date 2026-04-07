---
title: Exécution des traitements en attente
description: Découvrez comment exécuter des tâches en attente dans Adobe Admin Console pour vous assurer que toutes les modifications sont appliquées à votre organisation.
exl-id: 18549d19-7985-4a45-8894-e69836ddb23c
source-git-commit: 9085108231aaa46d8417d346686c211ea48f6b81
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Exécution des traitements en attente

Cette fonctionnalité s’applique aux organisations d’entreprise qui utilisent le [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) .

- Les modifications apportées à la [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) sont effectuées en deux phases :

   1. **Phase de modification** : apportez des modifications aux organisations ou affectez des produits.
   2. **Phase d’exécution** : vérifiez et exécutez les modifications en attente pour qu’elles prennent effet.

- Pour vous assurer que toutes les modifications apportées à la [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) sont implémentées et prennent effet, sélectionnez l’onglet **[!UICONTROL Exécution de la tâche]** et continuez à exécuter les modifications en attente.

  Connectez-vous à l’[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) .

## Persistance et visibilité des modifications

### Modifier la persistance

- Vous pouvez vous déconnecter et revenir ultérieurement sans perdre les modifications en attente.
- Modifications non exécutées :
   - Sont jetés après 30 jours.
   - Elles sont effacées lorsque la session se termine, par exemple lorsque l’onglet ou la fenêtre du navigateur est fermé.

&#x200B;> [!NOTE]
>
> Exécutez rapidement les modifications importantes pour vous assurer qu’elles sont appliquées correctement.

### Plusieurs administrateurs et conflits

- Deux administrateurs travaillant dans la même organisation :
   - Ne pas voir les modifications non exécutées les unes des autres.
   - Voir les modifications uniquement après :
      - l’exécution, et
      - Actualisation de l’affichage ou nouvelle connexion.
- Les modifications non exécutées peuvent entrer en conflit avec les modifications déjà exécutées.

### Gestion des conflits

Des conflits sont signalés :
- Au moment de l’exécution, ou
- Lorsque les données sont actualisées (par exemple, après s’être déconnecté et reconnecté).

## Exécution des modifications en attente

En tant qu’administrateur global, vous pouvez vérifier et exécuter les modifications en attente à partir de l’onglet **[!UICONTROL Exécution de la tâche]**.

### Étapes d’exécution des modifications

1. Connectez-vous à l’[!DNL Global Admin Console] .
2. Sélectionnez l’onglet **[!UICONTROL Exécution de la tâche]** dans le panneau de navigation de gauche.
3. Passez en revue les modifications en attente.
4. Sélectionnez **[!UICONTROL Envoyer les modifications]** pour les exécuter.

Après avoir envoyé le traitement :

- Le traitement entre dans la file d’attente d’exécution.
- Le statut est **[!UICONTROL En attente]** pendant l’exécution de la tâche.
- Adobe recommande de n’exécuter qu’une seule tâche à la fois pour plus de prévisibilité et de facilité de dépannage.

&#x200B;> [!IMPORTANT]
>
> Si une erreur se produit lors de l’exécution, toutes les modifications qui n’ont pas été appliquées avec succès doivent être saisies et envoyées à nouveau.

### Allocations de longue durée

Si l’affectation d’un produit dure plus de 12 heures :
- Le traitement est marqué comme **[!UICONTROL Échec]**.
- Les tâches en attente suivantes de ce traitement ne sont pas exécutées.

![tâches en attente](assets/pending-jobs.png)

## Annuler un traitement en cours

Vous pouvez annuler une tâche en cours d’exécution à partir de l’onglet **[!UICONTROL Exécution de la tâche]**.

### Procédure d’annulation d’un traitement en cours

1. Connectez-vous à l’[!DNL Global Admin Console] .
2. Sélectionnez **[!UICONTROL Exécution du traitement]**.
3. Sélectionnez **[!UICONTROL Annuler le traitement en cours]**.

### Comportement d’annulation

1. Le traitement est arrêté à la fin de l’étape en cours.
2. Le travail ne s’arrête pas au milieu d’une étape.
3. Certaines étapes peuvent prendre quelques minutes ou heures.
4. Pendant ce temps, le travail peut rester dans un état **[!UICONTROL Annulation]**.

&#x200B;> [!NOTE]
>
> Planifiez les annulations en sachant que l’achèvement de l’étape en cours peut considérablement retarder l’arrêt du traitement.

## Afficher l’historique des tâches

- Pour afficher les traitements exécutés au cours des 30 derniers jours :

   1. Connectez-vous à l’[!DNL Global Admin Console] .
   2. Sélectionnez **[!UICONTROL Exécution du traitement]**.
   3. Faites défiler jusqu’au bas de la page.
   4. Sélectionnez **[!UICONTROL Tâches récentes]**.

- Les tâches récentes s’affichent :
   - Commandes **job** envoyées.
   - **Erreurs** et **avertissements** associés à l’exécution.

&#x200B;> [!NOTE]
>
> Les renommations ou suppressions suivantes d’objets associés **n’affectent pas** la manière dont les commandes s’affichent dans l’historique des tâches. L’historique reflète l’État au moment de la soumission.
