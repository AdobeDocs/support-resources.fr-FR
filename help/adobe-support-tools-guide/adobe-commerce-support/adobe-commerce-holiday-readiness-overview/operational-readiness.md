---
title: Préparation opérationnelle
description: Recommandations relatives à la préparation opérationnelle pour aider les commerçants Adobe Commerce à préparer leurs environnements aux événements à trafic élevé tels que la saison des fêtes.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bcd8874c-7b93-5596-bdaa-22660e84df14
    internal-label: Deploy
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 938d2364-5176-55ec-80f1-9415253e5e51
    internal-label: Site Management
  - id: b48dbafb-4193-5648-b9d9-bf96e9c9a411
    internal-label: Backend Development
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: c89c0345d0e483463ab44195c2d5c0cb18d1d4c5
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%
---

# Préparation opérationnelle

Cette section fournit des recommandations techniques pour la préparation des environnements Adobe Commerce (Commerce sur infrastructure cloud et sur site) pour les événements à trafic élevé tels que la saison des fêtes.

## Application de tous les correctifs de sécurité et de performances {#apply-all-security-and-performance-patches}

Effectuez toutes les mises à jour avant le gel du code pour éviter les perturbations du déploiement.

## Exécuter les contrôles d’intégrité avant les fêtes {#run-pre-holiday-health-checks}

Testez les sauvegardes, l’intégrité du cron et les scripts de préchauffage du cache pour garantir le bon fonctionnement en cas de forte charge.

## Définir des playbooks de surveillance {#establish-monitoring-playbooks}

Documentez les seuils d’alerte, les étapes d’escalade et les points de contact pour une réponse 24h/24, 7j/7 pendant le pic.

## Plans de restauration de documents {#document-rollback-plans}

Conservez les stratégies de restauration versionnées pour récupérer rapidement les anomalies de déploiement.

