# Unit 1: Introduction to Azure compute

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Introduction

## Learning objectives

By the end of this unit, you should be able to:

- Explain what compute means in cloud computing.
- Recognize that Azure offers several ways to run applications and code.
- Compare the broad trade-off between control and management effort.
- Identify the kinds of workloads that will be explored in this module.

## 1. What is compute?

In cloud computing, **compute** is the processing power used to run programs, applications, and workloads. It includes the computing resources that execute instructions, process data, and respond to requests.

Imagine GeekHub Solutions is helping a school launch a student portal. The portal must run application code, respond when parents visit the site, and process form submissions. The school needs a compute option to run that work.

## 2. Different workloads need different compute options

Azure offers different ways to run applications and code. The right choice depends on what you're building, how much control you need, and how much infrastructure you want to manage.

### Azure Virtual Machines

A virtual machine (VM) is a software-defined computer running on Azure infrastructure. You choose a supported operating system and configure the software you need. You have significant control, but you are also responsible for much of the operating system maintenance, updates, security configuration, and application setup.

**Example:** A school needs a legacy application that requires a specific operating system configuration.

### Azure App Service

Azure App Service is a managed platform for hosting web applications, APIs, and related workloads. You deploy your application while Azure manages much of the underlying hosting infrastructure.

**Example:** GeekHub wants to host a school website or web API without maintaining a full virtual machine.

### Azure Functions

Azure Functions runs code in response to triggers, such as an HTTP request, a timer, or an event from another service. It is commonly used for event-driven tasks and serverless computing.

**Example:** When a student submits a form, a function validates the submission and sends it for further processing.

### Containers and container services

A container packages an application and its dependencies into an isolated unit. Azure offers services to run containers, from simple container instances to more comprehensive orchestration platforms.

**Example:** A development team wants to package an application consistently so it can run across supported environments.

## 3. The main trade-off: control versus management

A useful starting point is to ask: **How much of the underlying environment do I want to manage myself?**

- **Virtual machines:** more control over the operating system and environment, but more maintenance responsibility.
- **Managed application hosting:** less infrastructure management; you focus more on application code and configuration.
- **Serverless functions:** Azure manages much of the infrastructure, and your code runs in response to events. The level of management and scaling behaviour depends on the service and plan you choose.
- **Containers:** package applications consistently; how much infrastructure you manage depends on the Azure container service you select.

No option is automatically best for every workload. Choose according to the application's requirements, operational skills, cost, and scaling needs.

## 4. Knowledge check

### Question 1
What does compute refer to in cloud computing?

- A. Only the physical buildings that house servers.
- B. Processing resources used to run programs and workloads.
- C. Only the files stored in a database.

**Answer: B.** Compute is the processing capability used to execute code and run workloads.

### Question 2
A school wants to deploy a web application but does not want to maintain a full virtual machine. Which option is a strong starting point?

- A. Azure App Service.
- B. An availability zone.
- C. A management group.

**Answer: A.** App Service is a managed platform for web applications and APIs.

### Question 3
A form submission should trigger a small piece of code to validate the data. Which service is designed for event-driven code?

- A. Azure Functions.
- B. Azure Resource Manager management groups.
- C. An Azure region.

**Answer: A.** Azure Functions can execute code in response to supported triggers.

## 5. Key takeaways

- Compute is the processing capability used to run applications and code.
- Azure Virtual Machines offer substantial control but require more operating-system management.
- Azure App Service provides managed hosting for web applications and APIs.
- Azure Functions is useful for event-driven code.
- Containers package applications and their dependencies; the chosen container service determines how much infrastructure management is required.
- Choose compute based on workload needs and the balance between control and management effort.

## 6. Official Microsoft Learn reference

- [Choose an Azure compute service — Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
