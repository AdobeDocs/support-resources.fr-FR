---
title: 'Gestion des résultats dans le  [!DNL Adobe Success] '
description: Ce guide explique comment accéder aux résultats du portail, les interpréter et agir sur ceux [!DNL Adobe Success] ci pour vous aider à gérer de manière proactive les risques liés aux performances, à la sécurité et aux fonctionnalités des produits.
source-git-commit: 435931272f25caa6997a16d371aafcf70cf9facd
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Gestion des résultats dans le portail [!DNL Adobe Success]

Ce guide explique comment accéder aux résultats du portail [!DNL Adobe Success], les interpréter et agir sur ceux-ci pour vous aider à gérer de manière proactive les risques liés aux performances, à la sécurité et aux fonctionnalités des produits.

La page du portail [!DNL Adobe Success] **[!UICONTROL Résultats]** affiche les problèmes ou les risques détectés dans votre instance de produit Adobe. Les résultats incluent des problèmes de performances, de sécurité et de fonctionnalité, ainsi que leur statut et leur niveau de risque. La surveillance de cette page vous permet de résoudre les problèmes rapidement, avant qu’ils n’affectent vos environnements.

**Quels sont les résultats ?**

Les résultats sont des alertes d’informations d’assistance affichées sur le portail [!DNL Adobe Success]. Ils mettent en évidence les problèmes potentiels liés à la configuration de votre produit Adobe, tels que des ralentissements des performances, des risques de sécurité ou des configurations incorrectes. Ces alertes sont basées sur des données de télémétrie collectées à partir d’outils tels que les API, les [!DNL New Relic] et les [!DNL Splunk].

**Comment les résultats sont-ils créés ?**

Les équipes d’Adobe étudient régulièrement les problèmes et les tendances d’assistance les plus courants. En fonction des informations obtenues, ils ajoutent de nouvelles vérifications au système. Une fois par jour, le portail [!DNL Adobe Success] analyse les données des produits pour détecter les problèmes, tels que les configurations incorrectes, les tâches bloquées ou tout ce qui peut entraîner une panne du système. Si un contrôle détecte un élément en dehors de la plage de sécurité (telle que définie par les équipes produit et support d’Adobe), il s’affiche sous la forme d’un résultat.

**Pourquoi les résultats sont-ils importants**

En examinant régulièrement les résultats, vous pouvez détecter les problèmes le plus tôt possible, avant qu’ils n’affectent votre système ou vos clients. Cette approche proactive améliore la stabilité du système, réduit les temps d’arrêt et prend en charge les bonnes pratiques.

**Comment corriger les résultats**

Chaque résultat comprend des recommandations et des instructions claires sur la façon de résoudre le problème, ainsi que des liens vers la documentation pertinente, le cas échéant. Partagez ces résultats avec votre service informatique, votre équipe d’ingénierie ou votre partenaire Adobe, et travaillez ensemble pour y remédier. La résolution précoce de ces problèmes permet d’éviter les problèmes plus importants et de garantir le bon fonctionnement de votre système.


## Accéder aux résultats

Pour afficher des informations sur un produit :

1. Accédez à **[!UICONTROL Assistance et informations]**.
1. Sélectionnez la fiche produit correspondante. Sélectionnez l’onglet **[!UICONTROL Résultats]**.

   ![asp-support-inisghts-results](../../assets/asp-support-inisghts-findings.png)


1. Une liste de tous les résultats du produit sélectionné s’affiche.

   ![adobe-success-portal-results](../../assets/adobe-success-portal-findings.png)

1. À partir de là, vous pouvez :

   ![adobe-success-portal-download](../../assets/adobe-success-portal-download.png)

   * Rechercher des entrées spécifiques.
   * Exportez la liste des résultats en sélectionnant **[!UICONTROL Télécharger les résultats]**. Pour exporter un rapport correspondant à un résultat, cochez la case en regard du résultat correspondant dans la colonne **[!UICONTROL Nom du résultat]**. Si vous ne sélectionnez pas de résultat, le PDF contient par défaut la liste de tous les résultats.
   * Voir les détails d’un résultat, y compris une résolution recommandée en sélectionnant un résultat sous **[!UICONTROL Nom du résultat]**. La page Détails de la recherche affiche la recherche sélectionnée avec un contexte supplémentaire et une recommandation. Pour afficher ce rapport, sélectionnez la flèche de téléchargement.


     ![résultats-détails](../../assets/findings-details.png)


## Résultats des actions

Suivez ces étapes pour vérifier si chaque résultat est toujours applicable ou peut être ignoré.

>[!NOTE] :
>
>Les vérifications standard sont exécutées sur vos instances. Si les vérifications ne détectent pas le problème dans votre instance, le statut indique **[!UICONTROL Non détecté]**.

1. Accédez à **[!UICONTROL Assistance et informations]**.
1. Sélectionnez la fiche produit correspondante.
1. Ouvrez l’onglet **[!UICONTROL Résultats]**. Tous les résultats du produit sélectionné s’affichent.
1. Sélectionnez une entrée sous **[!UICONTROL Nom de la recherche]**. Sur la page Détails des résultats de recherche, vous pouvez :
   * Sélectionnez **[!UICONTROL Valider]** pour vérifier si le problème est toujours présent (le bouton **[!UICONTROL Valider]** est conçu pour confirmer que le problème a été résolu) :

   ![adobe-success-portal-validate](../../assets/adobe-success-portal-validate.png)


   * Si le problème est toujours présent, le message suivant s’affiche : *[!UICONTROL Validation terminée. Recherche toujours détectée]*. Utilisez les informations et la recommandation de la page Détails des résultats pour rechercher et résoudre ces problèmes.
   * Si le problème n’est plus présent, le message suivant s’affiche : *[!UICONTROL Validation terminée. Détection de l’élément]*. Lorsque le résultat n&#39;est plus détecté, il est grisé et passe à l&#39;état **[!UICONTROL Non détecté]**. Les résultats avec le statut **[!UICONTROL Non détecté]** se trouvent au bas de la liste des résultats.
   * Si le problème ne s’applique pas ou ne vous concerne pas, vous pouvez le rejeter en sélectionnant le **[!UICONTROL Rejeter]**. Lorsque le résultat est ignoré, le résultat est grisé et le statut passe à **[!UICONTROL Ignoré]**.  Les résultats avec le statut **[!UICONTROL Rejeté]** se trouvent au bas de la liste des résultats.

## Présentation des résultats

* **[!UICONTROL Recherche de nom]** - Sélectionnez pour obtenir des informations détaillées et les étapes de résolution recommandées.
* **[!UICONTROL Type]** - Catégorisé comme *Fonctionnalité*, *Performances* et *Sécurité*.
* **[!UICONTROL Niveau de risque]** - Indicateur de gravité, avec indicateurs visuels.
* **[!UICONTROL Statut]** - Le statut actuel du résultat (par exemple, *Détecté*, *Non détecté*, *Ignoré*).
* **[!UICONTROL Vérification de la dernière exécution]** - Horodatage de la dernière vérification qui a mis à jour la recherche.


## Bonnes pratiques

La page **[!UICONTROL Résultats]** répertorie les recommandations avec les niveaux de risque suivants : **[!UICONTROL Élevé]**, **[!UICONTROL Élevé]** et **[!UICONTROL Medium]**. **[!UICONTROL Élevé]** est critique, **[!UICONTROL Élevé]** est urgent et **[!UICONTROL Medium]** n’est pas critique. Pour maintenir l’intégrité et les performances du site :

* Traiter rapidement les constatations **[!UICONTROL à haut risque]**, car elles posent des menaces critiques.
* Résolvez rapidement les problèmes de **[!UICONTROL risque élevé]** afin d’éviter toute escalade.
* Surveillez régulièrement les résultats des tests de risque de **[!UICONTROL Medium]** et agissez selon vos besoins.




