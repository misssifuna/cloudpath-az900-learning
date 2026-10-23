# Unit 2: Azure Virtual Machines

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Azure Virtual Machines

## Learning objectives

By the end of this unit, you should be able to:

- Explain what an Azure virtual machine (VM) is.
- Identify common VM configuration choices.
- Understand the shared responsibilities of Microsoft and the customer.
- Recognize when a VM is a suitable compute option.
- Distinguish a VM from a physical computer and from managed application hosting.

## 1. What is a virtual machine?

A **virtual machine (VM)** is a software-based computer that runs on a physical host. It behaves much like a computer: it has processor capacity, memory, storage, networking, an operating system, and applications.

Virtualization allows a physical host to support multiple virtual machines. Each VM can run its own operating system and workloads, isolated according to the virtualization platform and configuration.

An **Azure Virtual Machine** is a VM hosted on Azure infrastructure. Microsoft manages the physical datacentres and host infrastructure; the customer manages much of the guest operating system, applications, and configuration.

## 2. Imagine a school portal

A school wants to run an application that needs a particular operating system and custom software configuration. It could create an Azure VM, install the required software, configure networking, and deploy the application.

This offers flexibility, but it also means the school or its service provider must plan for operating-system updates, security configuration, monitoring, backups, and application maintenance.

## 3. What do you configure when creating a VM?

Common choices include:

- **Image:** the starting template for the operating system, such as a supported Windows or Linux image.
- **Size:** the VM's virtual CPU, memory, and other capacity characteristics.
- **Disks:** storage for the operating system and application data.
- **Networking:** connectivity settings, such as a virtual network and network interface.
- **Region and availability options:** where the VM is deployed and what supported resilience options are configured.
- **Access and security:** identities, credentials or keys, firewall/network rules, and other protections.

The best configuration depends on the workload. A small test application generally does not need the same capacity as a busy production system.

## 4. Who manages what?

Azure follows a shared-responsibility approach. For a typical infrastructure-as-a-service (IaaS) VM:

**Microsoft manages** the physical datacentre, physical servers, and underlying host infrastructure.

**The customer manages** the guest operating system and its updates, installed applications, data, and many security and network configuration decisions. Exact responsibilities depend on the service and configuration.

A key exam point: choosing a VM does **not** mean Microsoft manages every part of the operating system for you.

## 5. When should you choose a VM?

A VM can be a good fit when you need:

- Substantial control over the operating system.
- Compatibility with software that requires a particular environment.
- Custom system configuration or software installation.
- A migration path for an existing server-based application.

A VM may not be the simplest choice for a straightforward website if a managed service such as Azure App Service already meets the requirements. With a VM, more operational work remains with you.

## 6. VM costs and operation

VM costs depend on factors such as the chosen size, region, operating system licensing, disks, networking, and how long resources are used. Some associated resources may continue to incur charges even when a VM is stopped. In particular, **stopping a VM from inside its operating system is not necessarily the same as stopping (deallocating) it in Azure**.

Check the VM's state and pricing details rather than assuming that a powered-off guest operating system means all charges have stopped.

## 7. Knowledge check

### Question 1
What is an Azure VM?

- A. A physical laptop shipped to the customer.
- B. A software-based computer hosted on Azure infrastructure.
- C. A container image only.

**Answer: B.** A VM is a virtual computer hosted on Azure's underlying physical infrastructure.

### Question 2
For a typical Azure VM, who is responsible for managing the guest operating system and its updates?

- A. Microsoft in every case.
- B. The customer, as part of the shared-responsibility model.
- C. The physical datacentre's power system.

**Answer: B.** With a typical IaaS VM, the customer manages much of the guest operating system and installed software.

### Question 3
A school must install custom software that requires specific operating-system access. Which option may be suitable?

- A. Azure Virtual Machines.
- B. Azure management groups.
- C. An availability zone by itself.

**Answer: A.** VMs offer substantial control over the operating system and environment.

### Question 4
Which statement about VM costs is safest?

- A. Every charge always stops when the guest OS is shut down.
- B. Costs depend on the VM and associated resources; stopping and deallocating are different states.
- C. All VM sizes cost the same.

**Answer: B.** Review the VM state and associated resources to understand potential charges.

## 8. Key takeaways

- A VM is a virtual computer with compute, memory, storage, networking, and an operating system.
- Azure hosts the VM on Microsoft's physical infrastructure.
- Customers retain responsibility for much of the guest OS, applications, data, and configuration.
- VM size, image, disks, networking, region, and security settings affect the deployment.
- VMs offer control but usually require more maintenance than managed application-hosting services.
- VM and associated-resource costs depend on configuration and state.

## 9. Official Microsoft Learn references

- [Virtual machines in Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/overview)
- [Azure shared responsibility in the cloud](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
