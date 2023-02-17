---
title: "Kubernetes"
date: 2023-01-22T17:40:57Z
draft: false
tags: ["tech", "kubernetes", "concepts"]
categories: ["posts", "tech", "kubernetes"]

---

## Kubernetes

Kubernetes is a widely used open-source container cluster management system for automating the deployment, scaling, and management of containerized applications. Initially developed by Google, it is now maintained by the Cloud Native Computing Foundation.

Kubernetes manages clusters of nodes, where each node is a computer or server that runs containers. Kubernetes uses a set of concepts such as pods, services, deployments, and ingresses to describe and manage applications in the cluster.

Pods are the basic units of deployment in Kubernetes. They group one or more containers that share the same namespace and resources, such as network ports and storage. Services are used to create a stable interface for accessing pods in the cluster, hiding the details of individual pod deployment. Deployments describe how pods should be deployed and managed using strategies such as horizontal scaling and live updates. Ingresses are used to manage access to the applications from outside the cluster.

Kubernetes also manages application configuration and secrets, as well as system resources such as storage volumes and networks. It supports service discovery to help applications find each other, as well as authentication and authorization plugins to manage access to resources in the cluster.

In summary, Kubernetes is a key tool for managing infrastructure for container-based applications. It provides a wealth of features to help development and operations teams deploy, manage, and maintain applications in a reliable and scalable manner.

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

> This diagram shows a Kubernetes cluster with three nodes. Each node is a computer that runs a software called "Kubelet", which manages the containers on that node. The containers are run by a container runtime, such as Docker.

The core of Kubernetes is a cluster controller called "API server" which exposes an API for describing the application deployments, services, storage volumes, etc. The information is stored in a distributed database called etcd. Other Kubernetes components, such as the scheduler and the controller, use this information to decide how to deploy the applications and handle errors.
