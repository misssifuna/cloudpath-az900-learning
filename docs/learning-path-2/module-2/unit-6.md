# Learning Path 2 — Module 2, Unit 6: Azure Virtual Desktop

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Azure Virtual Desktop

## Learning objectives

By the end of this unit, you should be able to:

- Explain the purpose of Azure Virtual Desktop (AVD).
- Distinguish Azure Virtual Desktop from an individual virtual machine.
- Recognize host pools, session hosts, and RemoteApp.
- Understand personal and pooled desktop options at a high level.

## 1. What is Azure Virtual Desktop?

Azure Virtual Desktop is a desktop and application virtualization service that runs on Azure. It lets users remotely access a Windows desktop experience or individual published applications from supported devices and clients.

Imagine GeekHub has a remote team member who needs a managed Windows desktop with approved business applications. Instead of relying entirely on the person's physical computer, the organization can provide a hosted desktop environment that the person accesses remotely.

The desktop environment runs on Azure-hosted infrastructure, while the user connects from their own device. This is different from simply opening a website or using a browser-based SaaS application: AVD delivers a remote desktop experience or specific remote applications.

## 2. Key Azure Virtual Desktop terms

### Host pool

A host pool is a group of session-host virtual machines that provides desktops or applications to users.

### Session host

A session host is a virtual machine where a user's remote desktop or application session runs.

### RemoteApp

RemoteApp lets an organization publish individual applications rather than providing the entire desktop to every user.

### Workspace and application group

At a high level, application groups define the desktops or applications users can access, and a workspace is the logical place where those published resources are presented to users.

## 3. Personal versus pooled desktops

### Personal desktop

A user is assigned a dedicated desktop environment. This can be useful when a person needs a more individually owned desktop experience.

### Pooled desktop

Multiple users share a pool of session-host resources, with sessions assigned according to the pool's configuration. Pooling can improve resource utilization when users do not all need dedicated VMs.

The best choice depends on user needs, application requirements, performance, management, and cost.

## 4. Azure Virtual Desktop versus Azure Virtual Machines

Azure Virtual Machines provide virtual computers for many kinds of workloads, such as hosting websites, databases, or custom software.

Azure Virtual Desktop is a service for delivering remote Windows desktops and applications. It uses session-host virtual machines, but also provides the service components that manage desktop access and delivery.

| Azure Virtual Machines | Azure Virtual Desktop |
|---|---|
| Provides virtual computers for many workload types | Delivers remote desktops and applications |
| A VM can host a website, database, or other workload | Session-host VMs run users' desktop or application sessions |
| You manage the VM's operating environment | Azure manages much of the desktop-delivery infrastructure, but you still manage session hosts, images, access, and configuration |

**Important:** Azure Virtual Desktop uses virtual machines, but an individual VM is not the same as a complete virtual desktop service.

## 5. When is Azure Virtual Desktop useful?

Possible scenarios include:

- Providing remote staff with access to a managed Windows desktop.
- Delivering business applications to users on different supported devices.
- Supporting temporary or distributed workforces.
- Using pooled desktops when a dedicated VM for every user is unnecessary.
- Publishing selected applications without providing a full desktop.

AVD is not automatically the cheapest or simplest choice for every user. Organizations need to consider licensing, session-host compute, storage, networking, security, and ongoing administration.

## 6. Knowledge check

### Question 1

What is the primary purpose of Azure Virtual Desktop?

- A. To deliver remote Windows desktops and applications.
- B. To store container images.
- C. To manage Azure subscriptions only.

**Answer: A.** AVD is a desktop and application virtualization service.

### Question 2

In Azure Virtual Desktop, what is a session host?

- A. A physical Azure region.
- B. A virtual machine where users' remote desktop or application sessions run.
- C. A container registry.

**Answer: B.** Session hosts run the desktop or application sessions.

### Question 3

What is RemoteApp used for?

- A. Publishing individual applications remotely.
- B. Creating an Azure subscription.
- C. Replicating a datacentre.

**Answer: A.** RemoteApp can deliver individual applications rather than a complete desktop.

### Question 4

True or false: Azure Virtual Desktop and an individual Azure virtual machine mean exactly the same thing.

**Answer: False.** AVD is a service for delivering remote desktops and applications, and it uses VMs as session hosts.

### Question 5

What is one potential advantage of pooled desktops?

- A. Every user must have a separate physical computer.
- B. Multiple users can share a pool of session-host resources, potentially improving resource utilization.
- C. No licensing or compute costs apply.

**Answer: B.** Pooling can improve resource utilization, though costs and licensing still apply.

## 7. Key takeaways

- Azure Virtual Desktop delivers remote Windows desktops and applications.
- A host pool groups session hosts.
- A session host is a VM where a user's remote session runs.
- RemoteApp can publish individual applications rather than a full desktop.
- Personal desktops provide dedicated environments; pooled desktops share host resources.
- AVD is more than a VM: it is the service for delivering and managing desktop and application access.
- Organizations still need to plan access, security, licensing, session-host resources, and costs.

## 8. Official Microsoft Learn references

- [What is Azure Virtual Desktop?](https://learn.microsoft.com/en-us/azure/virtual-desktop/overview)
- [Azure Virtual Desktop documentation](https://learn.microsoft.com/en-us/azure/virtual-desktop/)
- [Azure Virtual Desktop terminology](https://learn.microsoft.com/en-us/azure/virtual-desktop/environment-setup)
- [Windows multi-session FAQ](https://learn.microsoft.com/en-us/azure/virtual-desktop/windows-multisession-faq)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
