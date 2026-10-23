# Unit 3: Azure containers

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Azure containers

## Learning objectives

By the end of this unit, you should be able to:

- Explain what containers are and why developers use them.
- Distinguish a container image from a running container.
- Compare containers with virtual machines at a high level.
- Recognize Azure Container Instances, Azure Container Apps, Azure Kubernetes Service, and Azure Container Registry.

## 1. What is a container?

A **container** is an isolated environment for running an application. It packages the application and its dependencies so it can run consistently across compatible environments.

Imagine GeekHub develops a student portal. It works on one developer's laptop but fails in another environment because a dependency or configuration differs. Packaging the application and its dependencies into a container image helps reduce that problem.

Containers still need a suitable host and runtime, and they still require good security and resource management.

## 2. Containers versus virtual machines

A virtual machine typically runs its own guest operating system on virtualized hardware. A container typically shares the host operating system's kernel through a container runtime while keeping the application environment isolated.

This often makes containers lighter and faster to start than full VMs. However, containers are not simply tiny virtual machines: they have a different isolation model, and their security depends on configuration and the hosting platform.

Use a VM when you need substantial control over a guest operating system. Consider containers when you want to package and deploy applications consistently, especially when an application is designed for containerization.

## 3. Three important container terms

### Container image

A **container image** is the packaged template used to create a container. It contains the application and the components it needs, such as libraries and runtime dependencies.

### Container

A **container** is a running instance created from an image. One image can be used to create multiple container instances.

### Container registry

A **container registry** stores and manages container images. **Azure Container Registry (ACR)** is Azure's managed registry service. Teams can store images there and deploy them to supported Azure container services.

A simple flow is:

1. Build an application and package it as a container image.
2. Store the image in a registry.
3. Deploy the image to a service that can run containers.
4. Monitor and update the running application as needed.

## 4. Azure services for containers

Azure has several services for running containers. Their capabilities and management models differ.

### Azure Container Instances (ACI)

ACI provides a straightforward way to run containers in Azure without provisioning and managing VMs. It can be useful for simple container workloads, tasks, and jobs that don't need a full orchestration platform.

### Azure Container Apps

Azure Container Apps is a managed platform for containerized applications, APIs, background jobs, and microservices. It provides features such as scaling and application-level capabilities without requiring you to manage Kubernetes directly.

### Azure Kubernetes Service (AKS)

AKS is Azure's managed Kubernetes service. Kubernetes orchestrates containers across a cluster and helps manage deployment, scaling, and operations. AKS offers considerable flexibility, but teams need more knowledge of Kubernetes and cluster operations.

### Azure Container Registry (ACR)

ACR stores and manages container images. It is a registry, not the service that runs your container workload.

## 5. Choose the right concept

- Need a straightforward way to run a container without managing VMs? Consider **Azure Container Instances**.
- Need a managed platform for container apps, APIs, jobs, or microservices? Consider **Azure Container Apps**.
- Need Kubernetes orchestration and its greater level of control? Consider **Azure Kubernetes Service**.
- Need a private place to store container images? Consider **Azure Container Registry**.

The best option depends on the workload, scaling and networking requirements, and how much operational complexity the team can manage.

## 6. Knowledge check

### Question 1
What is a container image?

- A. A template used to create a running container.
- B. A physical Azure datacentre.
- C. An Azure subscription.

**Answer: A.** An image packages the application and its dependencies and is used to create containers.

### Question 2
Which service stores and manages container images?

- A. Azure Container Registry.
- B. Azure Availability Zones.
- C. Azure Resource Groups.

**Answer: A.** Azure Container Registry is Azure's managed container-image registry.

### Question 3
A team wants to run containers without managing VMs and doesn't need a full orchestration platform. Which option is a reasonable starting point?

- A. Azure Container Instances.
- B. Azure Management Groups.
- C. Azure Virtual Network Manager.

**Answer: A.** ACI is designed for straightforward container execution without provisioning VMs.

### Question 4
Which service provides managed Kubernetes in Azure?

- A. Azure Container Registry.
- B. Azure Kubernetes Service.
- C. Azure Container Instances.

**Answer: B.** AKS is Azure's managed Kubernetes service.

## 7. Key takeaways

- Containers package applications and their dependencies for consistent deployment.
- A container image is the template; a container is a running instance of that image.
- Containers typically share the host operating system's kernel, while a VM usually runs its own guest operating system.
- Azure Container Instances runs containers without requiring you to manage VMs.
- Azure Container Apps is a managed platform for containerized apps, jobs, and microservices.
- AKS provides managed Kubernetes orchestration.
- Azure Container Registry stores and manages container images.

## 8. Official Microsoft Learn references

- [Azure Container Instances overview](https://learn.microsoft.com/en-us/azure/container-instances/container-instances-overview)
- [Azure Container Apps overview](https://learn.microsoft.com/en-us/azure/container-apps/overview)
- [Azure Kubernetes Service documentation](https://learn.microsoft.com/en-us/azure/aks/)
- [Azure Container Registry documentation](https://learn.microsoft.com/en-us/azure/container-registry/)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
