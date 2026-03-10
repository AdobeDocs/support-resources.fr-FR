---
title: Avis de fin de prise en charge de MySQL et conseils de compatibilité des bases de données pour Adobe Commerce
description: Cet article fournit des informations sur les délais de fin de prise en charge de MySQL et des conseils de compatibilité de base de données pour les versions d’Adobe Commerce prises en charge.
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Avis de fin de prise en charge de MySQL et conseils de compatibilité des bases de données pour Adobe Commerce

Cet article fournit des informations importantes sur la fin de prise en charge de MySQL (EOS) et la compatibilité des bases de données pour les versions d’Adobe Commerce prises en charge.
Adobe recommande vivement aux commerçants de consulter cette annonce et de prendre des mesures pour préserver la stabilité de la plateforme et se conformer aux exigences de prise en charge.
Pour en savoir plus, consultez les [Conditions préalables à la mise à niveau pour MariaDB](https://experienceleague.adobe.com/fr/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) et [Configuration requise](https://experienceleague.adobe.com/fr/docs/commerce-operations/installation-guide/system-requirements).

## Fin de prise en charge de MySQL 8.0 (EOS)

MySQL 8.0 arrive à la fin de la prise en charge (EOS) le 30 avril 2026.
Passée cette date, les versions d’Adobe Commerce ci-après ne prendront plus en charge ni ne conserveront la compatibilité avec les versions de MySQL publiées après MySQL 8.0 :

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe ne validera pas et ne fournira pas de prise en charge des versions majeures MySQL plus récentes sur ces versions d’Adobe Commerce.

## Action requise pour les clients On-premise

Il est vivement conseillé aux installations sur site Adobe Commerce exécutant les versions suivantes de migrer leurs serveurs de base de données vers une version MariaDB compatible :

* 2,4,5
* 2,4,6
* 2,4,7

MariaDB est entièrement pris en charge pour ces versions et est désormais la plateforme de base de données recommandée.

* 2,4,5
* 2,4,6
* 2,4,7

Nous vous recommandons vivement de migrer vos serveurs de base de données vers une version MariaDB compatible.
MariaDB est entièrement pris en charge pour ces versions d’Adobe Commerce et est la plateforme de base de données recommandée.

## Prise en charge de MySQL dans Adobe Commerce 2.4.8 et 2.4.9

Adobe Commerce 2.4.8 et 2.4.9 sont les dernières versions d’Adobe Commerce à prendre en charge MySQL.

Pour ces versions :
* MySQL 8.4 est la version finale de MySQL prise en charge par Adobe Commerce.
* Aucune version de MySQL publiée après la version 8.4 ne sera certifiée ou prise en charge dans Adobe Commerce.

## Orientation future : MariaDB comme plateforme de base de données par défaut

À l’avenir, Adobe Commerce continuera à prendre en charge MariaDB en tant que plateforme de base de données par défaut et recommandée.

Adobe recommande vivement aux clients ci-dessous de commencer à planifier leur migration vers MariaDB afin de maintenir la compatibilité à long terme et l’alignement de la prise en charge :
* Tous les clients sur site Adobe Commerce 2.4.8 et 2.4.9
* Les clients exécutant des versions antérieures d’Adobe Commerce prises en charge
