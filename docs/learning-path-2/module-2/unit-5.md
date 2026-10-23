# Learning Path 2 — Module 2, Unit 5: Azure Functions

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Azure Functions

## Learning objectives

By the end of this unit, you should be able to:

- Explain what Azure Functions does.
- Describe serverless computing in simple terms.
- Recognize triggers and bindings.
- Identify scenarios where Azure Functions is useful.
- Distinguish Azure Functions from Azure App Service and Virtual Machines.

## 1. What is Azure Functions?

Azure Functions is a serverless compute service that runs code in response to events or schedules. It is a platform-as-a-service offering: Azure manages much of the infrastructure, allowing developers to focus on their code.

Imagine Holy Trinity Boys Senior School has an online application portal. When a new application is submitted, the school wants to run a small piece of code to validate the information or notify the admissions team. An Azure Function can run in response to that event.

A function can also run on a schedule, such as generating a daily report at midnight.

## 2. Three important concepts

### Trigger: what starts the function?

A trigger defines the event that causes a function to run. Examples include:

- An HTTP request to an endpoint.
- A timer reaching a scheduled time.
- A file being added or changed in storage.
- A message arriving in a queue.
- A supported database or event source reporting a change.

### Function: what code runs?

The function contains the instructions for the task. For example, it could validate a submission, transform data, process a message, or prepare a notification.

### Binding: how can it connect to other services?

Bindings provide a declarative way to connect a function to supported inputs and outputs. They can reduce the amount of integration code you need to write. A trigger starts the function; an input or output binding can help the function read or write data.

## 3. What does serverless mean?

**Serverless does not mean there are no servers.** The servers still exist in Azure's infrastructure. It means you do not need to manage the underlying servers in the same way you would with a virtual machine.

Depending on the hosting plan, Azure Functions can scale compute resources according to demand. Pricing also depends on the plan: some options charge based on consumption, while others have different pricing arrangements. Serverless does not automatically mean free.

## 4. Common Azure Functions scenarios

| Scenario | Example task |
|---|---|
| File upload | Process or validate a newly uploaded document |
| Scheduled task | Generate a report every night |
| Queue message | Process a message from an application |
| HTTP request | Run code that responds to a web request |
| Data change | React when supported data changes |
| Event stream | Process incoming event or device data |

Azure Functions can also be used to build APIs and connect cloud services. The right design depends on execution duration, reliability, security, and workload requirements.

## 5. Azure Functions versus other compute services

### Azure Virtual Machines

A VM gives you a virtual computer and substantial control over its guest operating system. You manage more of the environment.

### Azure App Service

App Service is a managed hosting platform for web applications, REST APIs, and mobile back ends. It is often a good fit when you want to deploy a complete web application without managing the underlying VM.

### Azure Functions

Functions is particularly useful for code that responds to events or schedules. It can handle tasks, process messages, and expose HTTP-triggered endpoints without requiring you to manage a full server environment.

| Service | Remember it for |
|---|---|
| Azure Virtual Machines | More control over the virtual computer and guest OS |
| Azure App Service | Managed hosting for web apps and APIs |
| Azure Functions | Event-driven or scheduled code |

These services can be combined in one solution; they are not always mutually exclusive choices.

## 6. Knowledge check

### Question 1

A school wants code to run automatically when a new file is uploaded to supported Azure storage. Which service is a strong fit?

- A. Azure Functions
- B. Azure Resource Groups
- C. Azure Availability Zones

**Answer: A.** Azure Functions can respond to supported storage events.

### Question 2

In Azure Functions, what does a trigger do?

- A. Defines the event that starts the function.
- B. Stores container images.
- C. Creates a physical Azure datacentre.

**Answer: A.** A trigger causes a function to run when its configured event occurs.

### Question 3

What does serverless mean?

- A. There are no physical servers anywhere.
- B. The cloud provider manages much of the underlying infrastructure for you.
- C. Your code runs without any computing resources.

**Answer: B.** Servers still exist; the provider manages much of the infrastructure.

### Question 4

Which option is especially suitable for a scheduled task or event-driven processing?

- A. Azure Functions
- B. Azure Management Groups
- C. Azure Container Registry

**Answer: A.** Functions can execute code in response to events or schedules.

## 7. Key takeaways

- Azure Functions runs code in response to events or schedules.
- A trigger defines what starts a function.
- Bindings help connect functions with supported inputs and outputs.
- Serverless does not mean there are no servers or that the service is always free.
- Azure Functions is especially useful for event-driven processing, scheduled tasks, and HTTP-triggered code.
- App Service is a strong fit for managed web application hosting, while VMs offer greater guest operating-system control.
- The hosting plan affects scaling, available resources, and cost.

## 8. Official Microsoft Learn references

- [Azure Functions documentation](https://learn.microsoft.com/en-us/azure/azure-functions/)
- [What is Azure Functions?](https://learn.microsoft.com/en-us/azure/azure-functions/functions-overview)
- [Azure Functions scenarios](https://learn.microsoft.com/en-us/azure/azure-functions/functions-scenarios)
- [Azure Functions best practices](https://learn.microsoft.com/en-us/azure/azure-functions/functions-best-practices)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
