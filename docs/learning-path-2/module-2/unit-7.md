# Learning Path 2 — Module 2, Unit 7: Azure App Service

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Describe application hosting options

## Learning objectives

By the end of this unit, you should be able to:

- Explain what Azure App Service is used for.
- Recognize the difference between App Service and Azure Virtual Machines.
- Explain the purpose of an App Service plan at a high level.
- Identify scenarios where App Service is a suitable hosting option.

## 1. What is Azure App Service?

Azure App Service is a managed platform for hosting web applications, REST APIs, and mobile back ends. It is a platform-as-a-service (PaaS) offering: Azure manages much of the underlying hosting infrastructure so developers can focus more on their application.

Imagine Holy Trinity Boys Senior School wants an online portal for announcements, learning resources, and timetables. If you build the portal with Node.js or Python, App Service can host it so students and staff can access it over the internet.

App Service supports popular application stacks such as .NET, Java, Node.js, Python, and PHP. It can also run supported custom containers.

## 2. Why use App Service?

App Service is useful when you want to deploy a web application or API without managing a full virtual machine.

Depending on the configuration and pricing tier, it offers capabilities such as:

- Managed hosting and platform maintenance.
- Scaling to handle changes in demand.
- Custom domain and TLS/SSL certificate support.
- Deployment integrations and staging options.
- Monitoring and diagnostic features.

These features do not remove the need to secure your application, configure access, manage secrets, or monitor costs. You still own your application and its configuration.

## 3. App Service versus Azure Virtual Machines

### Azure Virtual Machines

A VM gives you a virtual computer. You have more control over the guest operating system and installed software, but you also take on more responsibility for operating-system configuration, updates, and the hosting environment.

### Azure App Service

With App Service, you deploy your web application to a managed hosting platform. Azure handles much of the underlying infrastructure and platform maintenance.

| Consideration | Azure Virtual Machines | Azure App Service |
|---|---|---|
| Infrastructure management | You manage more of the VM and OS | Azure manages more of the hosting platform |
| Guest OS control | Greater control | More limited |
| Typical use | Custom environments, OS-level control, varied workloads | Web applications, REST APIs, and mobile back ends |
| Operations | More hands-on management | Less infrastructure management |

**Rule of thumb:** If you need detailed operating-system control, consider a VM. If you mainly need to host a web application or API and want Azure to manage more of the platform, consider App Service.

## 4. What is an App Service plan?

An **App Service plan** defines the compute resources, operating system, region, and pricing tier used to run App Service apps. Your app runs within a plan; the plan determines the capacity available to it.

Think of a plan as the hosting capacity allocated for your applications. Several apps can share the same plan and its compute resources. That can be useful, but apps sharing a plan can also compete for those resources.

Changing the plan's tier or capacity can affect cost and performance. Always choose a plan based on the workload's needs and check current Azure pricing before deploying a real service.

## 5. A simple school-portal scenario

Suppose a school launches a portal before examination results are released. Traffic may be much higher than usual.

App Service can help the school scale the hosting capacity according to the selected plan and configuration. Developers can also use deployment workflows and staging options to test an update before making it live, where the selected tier supports those features.

Remember: App Service hosts the application. The school may still need a separate database, identity solution, storage, and monitoring services.

## 6. App Service versus container services

We have already met Azure Container Instances, Azure Container Apps, and Azure Kubernetes Service (AKS).

- **App Service:** Managed hosting for web apps and APIs; supports several language stacks and custom containers.
- **Azure Container Instances:** A straightforward way to run containers without managing VMs, often for simpler isolated workloads.
- **Azure Container Apps:** A managed platform for containerized applications, APIs, jobs, and microservices.
- **AKS:** Managed Kubernetes for workloads that need Kubernetes orchestration and its greater flexibility.

These services overlap in some capabilities, so select based on the application's architecture and the amount of operational control needed.

## 7. Application hosting options: compare the main choices

Azure App Service is one option, not the whole application-hosting picture. For AZ-900, recognize the broad choices and the trade-offs between control and management effort.

| Hosting option | What it is useful for | Main trade-off |
|---|---|---|
| Azure Virtual Machines | Running an operating system and software that you configure | Most control, but you manage more of the operating system and maintenance |
| Azure App Service | Hosting web apps and APIs on a managed platform | Less infrastructure management than a VM; platform constraints apply |
| Azure Functions | Running event-driven code in response to triggers | Useful for short tasks and event processing rather than managing a full server |
| Containers | Packaging an application and its dependencies for consistent deployment | Requires container images and an appropriate container hosting service |
| Azure Static Web Apps | Hosting static front ends and supported web app workflows | Best suited to static content and supported web application patterns |

A school portal might use App Service for its web application, a database service for records, Functions for event-triggered tasks, or containers when its deployment needs that packaging model. A VM may be preferable when the application requires operating-system-level control.

**Exam reminder:** App Service, Functions, containers, and virtual machines are not identical. Select the hosting model that fits the workload and the amount of infrastructure management the team wants to handle.

## 8. Knowledge check

### Question 1

A school wants to host a Node.js web portal and prefers not to manage the underlying virtual machine. Which service is a strong fit?

- A. Azure App Service
- B. Azure Resource Groups
- C. Azure Availability Zones

**Answer: A.** App Service is a managed platform for web applications and APIs.

### Question 2

Which statement best describes an App Service plan?

- A. It is a place to store container images.
- B. It defines the compute resources and pricing tier used to run App Service apps.
- C. It is a separate physical Azure region.

**Answer: B.** The plan defines the hosting resources and pricing tier for the apps that run in it.

### Question 3

A workload needs extensive control over the guest operating system and installed software. Which option is generally more suitable?

- A. Azure Virtual Machines
- B. Azure App Service
- C. Azure Container Registry

**Answer: A.** A VM offers more guest OS control than the managed App Service platform.

### Question 4

True or false: Using App Service means the developer no longer needs to secure the application or monitor its costs.

**Answer: False.** Azure manages much of the hosting platform, but customers remain responsible for their application, configuration, access, data, and cost management.

## 9. Key takeaways

- Azure App Service is a managed PaaS offering for web applications, REST APIs, and mobile back ends.
- It supports popular stacks including .NET, Java, Node.js, Python, and PHP, as well as supported custom containers.
- Compared with a VM, App Service reduces the amount of underlying infrastructure you need to manage.
- An App Service plan defines the compute resources and pricing tier used to run apps.
- App Service does not eliminate the need to secure your application, manage configuration, and monitor spending.
- VMs are generally more suitable when you need greater guest OS control.

## 9. Official Microsoft Learn references

- [Azure App Service overview](https://learn.microsoft.com/en-us/azure/app-service/app-service-web-overview)
- [Azure App Service plans](https://learn.microsoft.com/en-us/azure/app-service/overview-hosting-plans)
- [Get started with Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/getting-started)
- [Choose how to host applications on Azure](https://learn.microsoft.com/en-us/azure/developer/intro/hosting-apps-on-azure)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
