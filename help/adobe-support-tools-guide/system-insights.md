---
title: Informations système
description: La fonction System Insights identifie de manière proactive les problèmes potentiels dans les environnements Adobe Commerce. L’examen des informations lors de la création du dossier réduit le temps de résolution, permet d’éviter les pannes et prend en charge un déploiement stable et sécurisé.
hide: true
hold: true
source-git-commit: d72c704d44f675d40c9c5b0ce2132957d5129df9
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 1%

---

# Informations système

La fonction Informations système fournit des résultats proactifs qui permettent d’identifier les problèmes potentiels en termes de performances, de sécurité et de fonctionnalités dans une configuration de produit Adobe. Ces informations font apparaître des risques tels qu’une dégradation des performances, des vulnérabilités de sécurité ou des configurations incorrectes basées sur des données de télémétrie collectées à partir d’outils d’observabilité, notamment les API, New Relic et [!DNL Splunk].

Les informations système s’affichent pendant le processus de création du dossier et permettent d’accélérer le diagnostic et la résolution.

## Création des informations système

Les équipes d’Adobe analysent en permanence les problèmes d’assistance courants et les tendances émergentes. Sur la base de ces résultats, Adobe ajoute des vérifications automatisées au système.

Ces contrôles analysent la configuration du produit afin de détecter des problèmes tels que des configurations incorrectes, des tâches bloquées ou des conditions susceptibles d’entraîner des problèmes fonctionnels ou des pannes système.

Lorsqu’un contrôle identifie une valeur ou un état en dehors de la plage de sécurité définie par les équipes produit et support d’Adobe, le système l’affiche en tant qu’Insight système.

## Importance des informations système

En examinant régulièrement les informations sur le système, vous pouvez identifier les problèmes rapidement, avant qu’ils n’affectent la stabilité du système ou l’expérience client. Cette approche proactive :

- Améliore la fiabilité de la plateforme
- Réduction des temps d’arrêt
- Permet de maintenir les bonnes pratiques recommandées par Adobe

## Disponibilité et portée

Actuellement, les informations système sont disponibles pour Adobe Commerce uniquement. Ces informations s’affichent pendant le processus de création de dossier sur la prise en charge d’Experience League et sont également disponibles via l’outil [SWAT (Site-Wide Analysis Tool)](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/site-wide-analysis-tool/intro).

>[ !Nnote]
>
>Les informations système affichent des données pour les environnements de production uniquement.

## Accès aux informations système

Les informations système s’affichent tout au long du workflow de création de dossier. Lorsque les détails du problème sont saisis, le panneau **[!UICONTROL Informations système]** s’affiche dans la partie droite de l’écran, sous la section Recommandations optimisées par l’IA. Pour en savoir plus sur les recommandations optimisées par l’IA, voir [Remplissez le ticket d’assistance](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket) dans l’article Expérience de l’assistance clientèle d’Adobe .

Le panneau affiche une liste déroulante des informations dont la portée est définie sur l’instance de projet spécifique. La définition de la portée est basée sur les informations saisies dans le champ **[!UICONTROL URL du projet]**. Saisissez l’**[!UICONTROL URL du projet]** avec précision pour vous assurer que les informations reflètent l’environnement correct.

Une fois le panneau chargé, il affiche une liste déroulante des cartes insight marquées pour votre environnement. Chaque carte insight comprend :

- Un titre qui résume le problème
- Brève description de l’insight

![Accéder aux ressources d’assistance](/help/adobe-support-tools-guide/assets/access-support-resources.png)

Pour afficher les détails complets d’insight, sélectionnez une carte insight dans la liste. La vue détaillée fournit les informations suivantes :

- Nom d’Insight
- Produit Adobe sur lequel est marqué l’insight
- Type d’Insight, classé comme suit :
   - [!UICONTROL fonctionnalité]
   - [!UICONTROL Performances]
   - [!UICONTROL Sécurité]
- [!UICONTROL Niveau de risque] indiquant la gravité
- [!UICONTROL Dernière exécution de vérification] indique à quel moment le résultat a été détecté.
- [!UICONTROL Insight Source], fourni par l’outil SWAT (Site-Wide Analysis Tool)
- Une explication détaillée du problème et de son impact potentiel, ainsi que des étapes exploitables pour enquêter et résoudre le problème. La vue détaillée explique également les causes typiques de ce type de problème et inclut des liens vers la documentation Adobe pertinente à titre de référence supplémentaire.

![Cliquez sur Carte de dossier](/help/adobe-support-tools-guide/assets/click-case-card.png)

Passez en revue toutes les informations du panneau avant de continuer, car insight peut directement résoudre le problème rencontré.

## Action sur une insight

Après avoir révisé une insight, choisissez l’une des actions suivantes.

### Poursuivre la création du dossier

Si le problème persiste ou nécessite une assistance supplémentaire, sélectionnez **[!UICONTROL Continuer la création du dossier]**. Le système conserve toutes les informations de dossier saisies précédemment.

### Marquer le problème comme résolu

Si insight résout le problème et qu’un dossier d’assistance n’est plus nécessaire, sélectionnez **[!UICONTROL Problème résolu]**.

Lorsque cette option est sélectionnée :

- Une boîte de dialogue de confirmation s’affiche.
- La boîte de dialogue indique que toutes les données de dossier saisies seront définitivement effacées.

![Action sur une insight](/help/adobe-support-tools-guide/assets/issue-resolved.png)

Sélectionnez **[!UICONTROL Terminé]** pour confirmer et revenir à la page **[!UICONTROL Mes dossiers]**. Sélectionnez **[!UICONTROL Annuler]** pour revenir à la vue détaillée d’insight.

![Effacer le formulaire de dossier](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## Envoi de commentaires sur une insight

Au bas de chaque vue détaillée d’insight, vous pouvez indiquer si l’insight vous a été utile. Ces commentaires aident Adobe à améliorer en permanence la pertinence et la précision des informations système.

![Fournir des commentaires](/help/adobe-support-tools-guide/assets/submit-feedback.png)

Pour fournir un retour d’informations :

1. Ouvrez une vue détaillée d’insight.
2. Faites défiler jusqu’au bas du panneau.
3. Recherchez l’invite **[!UICONTROL Cela a-t-il été utile ? Envoyer des commentaires.]**
4. Sélectionnez l’une des options suivantes :
   - **Pouce vers le haut** icône si insight a été utile
   - **Pouces vers le bas** icône si insight n’a pas été utile
5. (Facultatif) Saisissez des commentaires supplémentaires.
6. Sélectionnez **[!UICONTROL Envoyer]** pour envoyer vos commentaires, ou **[!UICONTROL Ignorer]** pour fermer la section des commentaires sans procéder à l’envoi.
