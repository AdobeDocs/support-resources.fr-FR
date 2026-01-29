---
title: FAQ sur l’abandon de la prise en charge du logiciel Adobe Commerce
description: Le FAQ suivant est destiné à aider les commerçants, les développeurs et les partenaires à comprendre les implications de la date de fin de prise en charge (EOS) publiée par Adobe Commerce pour les versions affectées d’Adobe Commerce.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
source-git-commit: 267c52f4c769bed8910ace25c604c2d6c84b6302
workflow-type: tm+mt
source-wordcount: '1733'
ht-degree: 0%

---

# FAQ sur l’abandon de la prise en charge du logiciel Adobe Commerce

Le FAQ suivant est destiné à aider les commerçants, les développeurs et les partenaires à comprendre les implications de la date de fin de prise en charge (EOS) publiée par Adobe Commerce pour les versions affectées d’Adobe Commerce.

## Dispositions générales

### Où puis-je trouver les dates de prise en charge logicielle pour toutes les versions d’Adobe Commerce ?

La politique relative au cycle de vie des logiciels Adobe Commerce et les dates de prise en charge des logiciels sont présentées dans la [politique relative au cycle de vie des logiciels Adobe Commerce](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf). Nous publions également les dates de fin de prise en charge (EOS) sur notre [page de documentation destinée aux développeurs](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/versions).

### Que signifie le fait qu’Adobe cesse la prise en charge d’une version du logiciel Adobe Commerce ?

Lorsqu’Adobe met fin à la prise en charge d’une version de son logiciel Adobe Commerce, les éléments suivants sont attendus :

* Adobe Commerce n’apporte plus de modifications au produit pour cette version (y compris des modifications fonctionnelles, de qualité, de sécurité et de conformité PCI).
* Les demandes d’extraction de la communauté ne seront plus acceptées ni fusionnées pour la version EOS. Les extensions de Commerce Marketplace qui ne sont compatibles qu’avec des versions d’Adobe Commerce non prises en charge seront supprimées.
* La documentation en ligne des versions non prises en charge sera supprimée (par exemple, les documents destinés aux développeurs).
* Les tickets d’assistance envoyés après la fin de la prise en charge d’une version d’Adobe Commerce ne seront pas résolus (vous trouverez plus de détails sur l’assistance technique ci-dessous).

### Quelles sont les implications pour les commerçants qui utilisent un logiciel Adobe Commerce non pris en charge ?

Nous vous recommandons vivement d’utiliser uniquement un logiciel pris en charge.

Si vous décidez de continuer à utiliser des logiciels dont la prise en charge a pris fin, vous ne recevrez plus de mises à jour de produits importantes ni d’assistance technique, qui inclut souvent les dernières mises à jour de sécurité. L’utilisation de logiciels non pris en charge peut avoir un impact sur les domaines suivants :

**Offrir des expériences d’achat sécurisées :**

* Vous devrez consacrer des ressources à l’évaluation et faire appel à des fournisseurs tiers pour fournir une assistance en matière de sécurité, des correctifs et des mises à jour.
* Une fois qu’une version du logiciel Adobe Commerce n’est plus prise en charge, elle n’est plus compatible [PCI](https://www.pcisecuritystandards.org/pci_security/maintaining_payment_security). Si cela se produit, vous risquez d’être passible d’amendes, de la suppression de la capacité de traitement des cartes de crédit ou d’autres sanctions en conséquence.
* Comme la plupart des exploits ont tendance à cibler des installations qui ne sont pas à jour avec les dernières mises à jour de sécurité, nous recommandons toujours aux commerçants de garder leurs logiciels à jour et d&#39;installer les mises à jour de sécurité dès qu&#39;elles sont disponibles. Il appartient au commerçant de protéger sa boutique en ligne par des mesures de protection et des contrôles de sécurité adéquats pour protéger son site Web et les données personnelles de ses clients. L’une des meilleures façons d’y parvenir est d’installer les derniers correctifs, correctifs et mises à jour logicielles et de surveiller en permanence votre site et votre console d’administration à la recherche d’activités inhabituelles.

**Fonctionnement efficace**

* À mesure que les versions non prises en charge des logiciels Adobe Commerce vieillissent, le nombre de développeurs et de partenaires disponibles est en diminution. Ils sont en mesure de fournir une prise en charge des versions obsolètes lorsqu’ils orientent leurs opérations vers des technologies plus récentes. Généralement, il en résulte que la quantité et la qualité des talents pour la maintenance logicielle diminuent, tandis que le coût de maintenance du logiciel augmente.
* Pour les logiciels Adobe Commerce non pris en charge, les technologies périphériques et les dépendances peuvent également atteindre leur propre fin de cycle de vie (par exemple, PHP, MYSQL, REDIS, SOLR). Il est donc de plus en plus difficile de gérer et de maintenir un site sécurisé et conforme.
* Les développeurs d’extensions se concentrent également sur les technologies les plus récentes et les plateformes compatibles. Par conséquent, ils peuvent ne pas continuer à gérer les extensions pour les versions d’Adobe Commerce non prises en charge.
* L’utilisation de versions non prises en charge des logiciels Adobe Commerce entraîne souvent une augmentation des dépenses et des ressources liées à la maintenance d’une ancienne plateforme, au lieu de les consacrer à l’innovation et à la croissance continues de l’entreprise.

**Croissance agressive**

* Adobe continue d’investir dans de nouvelles technologies et fonctionnalités. En gardant vos logiciels à jour, vous êtes en mesure de tirer parti des nouvelles technologies et capacités qui peuvent aider votre entreprise à fonctionner de manière plus stratégique et à croître encore plus rapidement.

### Quels sont quelques exemples de la façon dont les commerçants peuvent tirer profit des nouvelles technologies en se tenant à jour avec leur logiciel Adobe Commerce ?

Vous pouvez tirer de nombreux avantages de rester à jour sur votre logiciel Adobe Commerce :

* En plus de maintenir votre plateforme à jour avec les dernières protections de sécurité, y compris la conformité PCI, la mise à niveau vers une version prise en charge peut apporter des améliorations en termes de performances et d&#39;évolutivité, vous donnant ainsi accès aux dernières innovations.
* Adobe Commerce 2.4.4, sortie le 12 avril 2022, marque une nouvelle étape en termes de fonctionnalités, de performances et de protection pour le commerce. Il jette les bases des prochaines années d’aide à l’innovation d’Adobe pour la résilience des entreprises commerciales. Basée sur la dernière version de PHP 8.1, la dernière version permet aux commerçants de préparer leurs activités de commerce numérique avec :
   * Accès plus rapide aux fonctionnalités innovantes fournies sous forme de services SaaS, telles que les recommandations de produits, les services de paye et la recherche en direct
   * Maintenance et mises à niveau plus simples et plus rentables
   * Flexibilité continue pour personnaliser et répondre aux besoins spécifiques de l’entreprise
   * Amélioration significative des performances et de l’évolutivité
   * Amélioration de l’expérience des développeurs et des outils de surveillance de l’intégrité des plateformes

### Que dois-je faire pour éviter les problèmes de fin de prise en charge du logiciel ?

Votre plateforme commerciale est un système d’entreprise important pour votre entreprise. Le maintien à jour et à jour est un investissement permanent essentiel dans l’entreprise. Les dernières mises à jour technologiques et de sécurité pour votre vitrine numérique sont importantes à plusieurs niveaux et peuvent aider à améliorer les innovations et la croissance.

Le passage à la dernière version du logiciel Adobe Commerce peut demander du temps et des ressources pour s’exécuter correctement. Il est recommandé de planifier votre projet aussi longtemps avant la date de fin de prise en charge que possible afin de vous assurer de disposer du temps et des ressources nécessaires pour atteindre vos objectifs stratégiques dans les délais impartis et le budget alloué. Pour vous aider à effectuer votre prochaine mise à niveau, Adobe a publié le Guide de mise à niveau vers la version [2.4](https://experienceleague.adobe.com/docs/commerce-operations/assets/adobe-commerce-2-4-upgrade-guide.pdf?lang=fr) qui comprend les bonnes pratiques et les étapes techniques à suivre, ainsi que les outils et ressources à utiliser lors de l’exécution de votre mise à niveau.

Il est également important de réserver les ressources du développeur et des partenaires le plus tôt possible. Le temps et les ressources du partenaire sont souvent réservés bien avant la date de fin de prise en charge, ce qui entraîne une diminution significative des ressources pour aider les projets de migration. Il est recommandé d’avoir un plan glissant sur trois ans dont vous discutez au moins une fois par an et de vous assurer que l’année suivante est planifiée et budgétée. Utilisez le calendrier des versions d’[Adobe](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/planning/schedule) pour suivre les dates de publication.

### Puis-je faire appel à un fournisseur tiers pour l’assistance logicielle lorsque l’assistance Adobe Commerce cessera ?

Oui, vous pouvez rechercher des sociétés de sécurité, des développeurs ou des partenaires qui fourniront une prise en charge pour les versions d’Adobe Commerce non prises en charge. Il vous incombe d&#39;évaluer ces fournisseurs, de recertifier la conformité si nécessaire, et d&#39;identifier et de résoudre les menaces de sécurité continues qui peuvent avoir un impact sur votre entreprise et vos clients.

### Je dispose d’une licence pour Adobe Commerce qui s’étend au-delà de la date de fin de prise en charge indiquée pour cette version. Adobe continuera-t-il à fournir la prise en charge logicielle de ma version non prise en charge pendant toute la durée de vie de ma licence si je choisis de ne pas passer à une version prise en charge ?

La licence Adobe Commerce vous donne le droit d’accéder aux versions d’Adobe Commerce généralement disponibles et de les utiliser, y compris l’accès et l’utilisation de versions non prises en charge. Que votre version du logiciel soit prise en charge ou non, vous devez continuer à tenir à jour vos droits de licence actuels pour continuer à accéder au logiciel Adobe Commerce et à l’utiliser. Cela se termine à la fin de votre contrat Adobe Commerce.

Une licence Adobe Commerce ne fournit pas de prise en charge logicielle pour les versions qui ont atteint et dépassé leur date de fin de prise en charge. Si vous continuez à utiliser des logiciels non pris en charge, vous devrez gérer et payer vos propres correctifs de sécurité et une nouvelle certification de conformité PCI, et vous devrez probablement assumer des risques et des responsabilités supplémentaires en matière de sécurité.

### Une version du logiciel « s’arrête-t-elle » lorsqu’elle atteint et dépasse sa date de fin de prise en charge ?

Non, le logiciel Adobe Commerce ne s’arrête pas une fois la date de fin de prise en charge atteinte ou dépassée. Votre licence reste valide même pour les logiciels Adobe Commerce non pris en charge tant que votre compte est en règle, mais vous serez responsable de la re-certification de conformité PCI et ne pourrez plus déposer de tickets d&#39;assistance. Plus important encore, vous ne recevrez plus de correctifs de sécurité qui aident à protéger votre vitrine numérique.

### Puis-je continuer à utiliser le logiciel Adobe Commerce après l’expiration de ma licence ?

Une fois votre licence Adobe Commerce arrivée à expiration, vous devez cesser d’utiliser le logiciel Adobe Commerce et supprimer toutes les versions de ce logiciel. Tant que votre compte est en règle, la licence Adobe Commerce vous donne le droit d’accéder aux versions d’Adobe Commerce généralement disponibles et de les utiliser.

## Provisions techniques

### Les tickets d’assistance ouverts AVANT la date de fin de prise en charge d’une version de logiciel continueront-ils à être résolus même après la fin de la date de prise en charge ?

Oui, les tickets d’assistance ouverts avant la date de fin d’assistance d’une version de logiciel continueront à être traités et résolus même si la date de fin d’assistance de cette version de logiciel est dépassée. Cependant, la résolution des tickets d’assistance peut dépendre de l’utilisation ou non de composants hors de contrôle d’Adobe Commerce (c’est-à-dire PHP, jQuery, etc.) qui ont expiré ou atteint la fin de la prise en charge. Dans ces cas, le ticket d’assistance peut être résolu en vous demandant d’effectuer la mise à niveau vers la version la plus récente.

### Si j’ouvre un ticket pour une version de logiciel pour laquelle la prise en charge du logiciel prend bientôt fin, Adobe donnera-t-il la priorité à ces tickets afin qu’ils soient résolus avant la date de fin de la prise en charge ?

Non, Adobe ne redéfinit pas la priorité des tickets d’assistance en fonction de la date de fin de prise en charge de ces versions logicielles. Les tickets d’assistance sont traités en fonction d’algorithmes internes dérivés de la raison du contact, de l’environnement et de l’impact commercial du ticket.

### Pour les tickets d’assistance ouverts AVANT la date de fin de l’assistance, existe-t-il une alerte pour rappeler aux commerçants la fin prochaine de l’assistance ?

Non, il n’existe aucune alerte de rappel informant les utilisateurs et utilisatrices de tickets d’assistance des dates de fin d’assistance à venir. Il est de la responsabilité de l’ouvrez-ticket de connaître les dates de fin de prise en charge de la version d’Adobe Commerce sur laquelle il se trouve, qui se trouvent dans notre politique [Cycle de vie du logiciel Adobe Commerce](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf).

### Si un ticket d’assistance pour une version de logiciel est ouvert APRÈS la date de fin de prise en charge de cette version, le problème sera-t-il toujours résolu ?

Non, Adobe Commerce ne fonctionnera pas pour résoudre les tickets d’assistance qui ont été ouverts après la date de fin de prise en charge de cette version du logiciel.
