---
title: Kubernetes Rearing
date: 2024-01-01T14:13:14.674Z
extra:
  featured: true
  link: https://k8s.haxx.ninja/
  image: /media/k8s.webp
description: As a contributor to the inception of Kubernetes, we played a pivotal role in revolutionizing container orchestration and cloud-native computing. From the early days of conceptualization to the project's maturation into a cornerstone of modern infrastructure, our efforts were driven by a relentless pursuit of innovation and excellence. Beyond shaping Kubernetes' core architecture and functionality, we dedicated ourselves to ensuring its success.  Through rigorous code reviews, architecture reviews, vulnerability assessments, and the implementation of best practices, we helped fortify Kubernetes against potential exploits, empowering organizations to deploy and manage their applications with confidence in multi-cloud environments. Our journey with Kubernetes is not just about technological advancement; it's a testament to the power of collaboration, perseverance, and the relentless pursuit of excellence in shaping the future of cloud computing.
taxonomies:
  tags:
  - KubernetesInnovation
  - CloudNative
  - ContainerOrchestration
  - Infrastructure
  - Security
  - DevOps
  - OpenSource
  - CloudComputing
  - SoftwareEngineering
  - TechnologyLeadership
---
Hardening a scheduling application server that was never intended to be hardened (wrapped by private R&D security IP not made publicly available) is always a challenge.  Especially in light of everything else one must consider and engineer around;

* Cluster Architecture
* Containers
* Workloads
* Services, Load Balancing, and Networking
* Storage
* Configuration
* Policies
* Scheduling, Preemption and Eviction
* Cluster Administration
* Extending Kubernetes

Which is why it is worthwhile to view my lecture on the project that became Kubernetes.  Design decisions were made of that era's philosophy.  Hence this walkthrough to right the sins that were made.