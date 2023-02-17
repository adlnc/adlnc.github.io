---
title: "Kubernetes"
date: 2023-01-22T17:40:57Z
draft: false
tags: ["tech", "kubernetes", "concepts"]
categories: ["posts", "tech", "kubernetes"]

---

## Kubernetes

Kubernetes est un système de gestion de cluster de containers open-source largement utilisé pour automatiser le déploiement, la mise à l'échelle et la gestion des applications containerisées. Il a été initialement développé par Google et est maintenant maintenu par la Cloud Native Computing Foundation.

Kubernetes gère des clusters de nœuds, où chaque nœud est un ordinateur ou un serveur qui exécute les containers. Kubernetes utilise un ensemble de concepts tels que les pods, les services, les déploiements et les ingress pour décrire et gérer les applications dans le cluster.

Les pods sont les unités de base de déploiement dans Kubernetes. Ils regroupent un ou plusieurs containers qui partagent le même espace de noms et les mêmes ressources, telles que les ports réseau et le stockage. Les services sont utilisés pour créer une interface stable pour accéder aux pods dans le cluster, en masquant les détails de déploiement des pods individuels. Les déploiements décrivent comment les pods doivent être déployés et gérés à l'aide de stratégies telles que la mise à l'échelle horizontale et la mise à jour en direct. Les ingress sont utilisés pour gérer l'accès aux applications depuis l'extérieur du cluster.

Kubernetes permet également de gérer la configuration et les secrets de l'application, ainsi que les ressources système telles que les volumes de stockage et les réseaux. Il prend en charge la découverte de service pour aider les applications à se découvrir mutuellement, ainsi que les plugins d'authentification et d'autorisation pour gérer les accès aux ressources dans le cluster.

En résumé, Kubernetes est un outil clé pour la gestion de l'infrastructure des applications basées sur des containers. Il offre une abondance de fonctionnalités pour aider les équipes de développement et d'opérations à déployer, gérer et maintenir des applications de manière fiable et scalable.

    +------------------+      +------------------+      +------------------+
    |                  |      |                  |      |                  |
    |      Node        |      |       Node       |      |       Node       | 
    |                  |      |                  |      |                  |
    +------------------+      +------------------+      +------------------+
             |                          |                        |  
             |                          |                        |   
             |                          |                        |    
    +------------------+      +------------------+      +------------------+
    |                  |      |                  |      |                  |
    |   Kubelet        |      |   Kubelet        |      |   Kubelet        |
    |                  |      |                  |      |                  |
    +------------------+      +------------------+      +------------------+
             |                          |                        |  
             |                          |                        |   
             |                          |                        |  
    +------------------+      +------------------+      +------------------+
    |                  |      |                  |      |                  |
    |   Container      |      |   Container      |      |   Container      |
    |    Runtime       |      |    Runtime       |      |    Runtime       |
    +------------------+      +------------------+      +------------------+

Ce schéma montre un cluster de Kubernetes avec trois nœuds. Chaque nœud est un ordinateur qui exécute un logiciel appelé "Kubelet", qui gère les conteneurs sur ce nœud. Les containers sont exécutés par un runtime de conteneur, tel que Docker.

Le cœur de Kubernetes est un contrôleur de cluster appelé "API server" qui expose une API pour décrire les déploiements de l'application, les services, les volumes de stockage, etc. Les informations sont stockées dans une base de données distribuée appelée etcd. Les autres composants de Kubernetes, tels que le planificateur et le contrôleur, utilisent ces informations pour décider comment déployer les applications et gérer les erreurs.
