---
title: Limiter l’accès au produit par les adresses IP
description: Utilisez l’accès basé sur les adresses IP pour contrôler l’accès des utilisateurs et utilisatrices aux produits Adobe et restreindre l’utilisation aux plages d’adresses IP publiques approuvées.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---


# Limiter l’accès au produit par les adresses IP

S’applique à l’entreprise.

Utilisez l’accès basé sur les adresses IP pour contrôler l’accès de vos utilisateurs et utilisatrices aux produits Adobe et empêcher toute utilisation non autorisée d’adresses IP publiques non répertoriées.

Accédez à [](https://adminconsole.adobe.com/settings/identity) pour ajouter des adresses IP publiques de confiance au **accès basé sur les adresses IP** place sur la liste autorisée pour une utilisation sécurisée des applications et services Adobe.

## Avantages de l’accès basé sur IP

Le contrôle d’accès basé sur l’adresse IP utilise une adresse IP placée sur la liste autorisée pour limiter l’utilisation des produits Adobe à partir d’adresses IP publiques aléatoires. L’accès basé sur les adresses IP s’applique à tous les répertoires et produits associés de votre Adobe Admin Console.

Vous pouvez ajouter des adresses IP publiques de confiance à la liste **Adresses IP autorisées** pour empêcher les utilisateurs de :

- Accès aux produits à partir d’adresses IP publiques qui se trouvent en dehors des plages d’adresses IP autorisées
- Connexion à Adobe [profils utilisateur](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html) à partir d’adresses IP publiques en dehors des plages d’adresses IP autorisées
- Changement de profils utilisateur sur les applications web en dehors des plages d’adresses IP autorisées

  ![Exporter la structure organisationnelle](./assets/ip-based-access.avif)

## Activer l’accès basé sur les adresses IP

### Considérations importantes

>[!Iconsidérations importantes]
>
>- Les administrateurs doivent commencer par ajouter leur propre adresse IP publique, puis uniquement ajouter d’autres plages d’adresses IP. Dans le cas contraire, une erreur peut se produire.
>- L’accès basé sur les adresses IP ne s’applique pas aux adresses IP privées.

Vous pouvez ajouter jusqu’à 150 plages d’adresses IP publiques différentes au format CIDR uniquement.

Pour activer l’accès basé sur les adresses IP dans votre Adobe Admin Console, procédez comme suit :

1. Accédez à la section **[!UICONTROL Paramètres ](https://adminconsole.adobe.com/settings/identity)**.
2. Sélectionnez et développez **[!UICONTROL Confidentialité et sécurité]** dans le menu de sélection, puis sélectionnez **[!UICONTROL Paramètres d’authentification]**.
3. Dans la section **[!UICONTROL Accès basé sur IP]**, cliquez sur le bouton **[!UICONTROL Ajouter une adresse IP]**.
4. Dans la fenêtre **[!UICONTROL Ajouter une adresse IP]** :
   - Saisissez les adresses IP publiques ou le bloc CIDR à ajouter à votre place sur la liste autorisée.
   - Utilisez une virgule pour séparer plusieurs adresses IP.
   - Sélectionnez **[!UICONTROL Enregistrer]**.

   Actuellement, nous ne prenons en charge que le format IPv4. Voici quelques exemples :
   - Adresse IP v4 : 1.3.4.6
   - Adresse de sous-réseau IP v4 : 1.2.0.0/24

Vos adresses IP sont ajoutées en quelques minutes. Les utilisateurs associés verront la restriction la prochaine fois qu’ils tenteront de se connecter ou de changer de profil en dehors des adresses IP publiques autorisées. Nous vous recommandons d’informer vos utilisateurs à l’avance de cette modification.

Vous pouvez modifier ou supprimer n’importe quelle adresse IP répertoriée en sélectionnant les options de modification ou de suppression en regard de chaque entrée.

>[!NOTE]
>
>- Lorsque l’accès par IP est activé, **aucune déconnexion forcée n’est effectuée**. Les utilisateurs ne sont affectés que lorsqu’ils tentent de sélectionner le profil restreint lors de la connexion ou du changement de profil sur le web.
>- Si vous utilisez une passerelle web sécurisée, assurez-vous que tout le trafic y est acheminé. Affichez la [liste des domaines autorisés](https://helpx.adobe.com/enterprise/kb/network-endpoints.html) pour que les applications et services Adobe fonctionnent correctement.
>- Si vous êtes exclu d’Admin Console parce que vous avez saisi une adresse IP non valide, contactez l’[Assistance clientèle d’Adobe](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html).

## Rejoignez la conversation

Pour collaborer, poser des questions et discuter avec d’autres administrateurs, visitez notre [Communauté des entreprises et des équipes](https://www.adobe.com/go/entcom).
