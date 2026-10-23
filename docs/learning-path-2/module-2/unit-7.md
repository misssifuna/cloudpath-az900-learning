# Unit 7: Azure Virtual Machine Scale Sets and Availability Sets

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 2:** Describe Azure compute services  
**Unit:** Virtual Machine Scale Sets and availability sets

## Learning objectives

By the end of this unit, you should be able to:

- Explain what Azure Virtual Machine Scale Sets do.
- Distinguish horizontal scaling from vertical scaling.
- Explain the purpose of availability sets.
- Define fault domains and update domains.
- Compare scale sets, availability sets, and availability zones.

## 1. What are Azure Virtual Machine Scale Sets?

Azure Virtual Machine Scale Sets (VMSS) let you create and manage a group of virtual machines. You can configure the VMs to be load-balanced and set up scaling so that the number of instances increases or decreases in response to demand or a schedule.

Imagine a school portal normally needs two VMs. When admissions open and traffic increases, the system can scale out to five VM instances. When traffic falls, it can scale back down. Scaling policies, application health, and load balancing need to be configured appropriately; a scale set alone does not guarantee that an application is always available.

## 2. Horizontal scaling versus vertical scaling

### Horizontal scaling: scale out and scale in

Horizontal scaling changes the number of VM instances.

- **Scale out:** Add instances to handle more work.
- **Scale in:** Remove instances when fewer are needed.

Scale sets are useful for managing groups of VMs and can support autoscaling.

### Vertical scaling: scale up and scale down

Vertical scaling changes the capacity of an individual VM, for example by selecting a VM size with more CPU or memory.

**Memory tip:** Horizontal means changing the number of machines. Vertical means changing the capacity of a machine.

## 3. What is an availability set?

An Azure availability set is a logical grouping of VMs designed to reduce the chance that a single hardware failure or planned maintenance event will affect every VM in the group at once.

Azure distributes VMs across fault domains and update domains.

### Fault domain

A fault domain is a group of infrastructure components that share a common source of failure, such as power or networking. Separating VMs across fault domains helps reduce the impact of a shared hardware or infrastructure failure.

### Update domain

An update domain groups VMs for planned maintenance. Separating VMs across update domains helps avoid restarting every VM in the set at the same time during platform maintenance.

For example, if a school portal uses two VMs in an availability set, the arrangement can help reduce the chance that both are affected by the same hardware failure or planned maintenance event.

An availability set is not a backup and does not guarantee that an application can never go down.

## 4. Availability sets versus availability zones versus scale sets

These Azure features have different primary purposes.

| Feature | Main purpose |
|---|---|
| Virtual Machine Scale Sets | Manage a group of VMs; can scale the number of instances |
| Availability Sets | Spread VMs across fault and update domains to reduce correlated failures |
| Availability Zones | Use separate physical locations within a supported Azure region to improve resilience to datacentre-level failures |

Availability zones generally provide stronger isolation from datacentre-level failures than availability sets. Scale sets can also be deployed across supported availability zones, combining scaling with zone-level resilience.

The correct design depends on the workload, supported region and VM configuration, cost, and required availability. Running multiple VMs does not automatically make an application resilient: networking, data replication, health checks, and application design also matter.

## 5. Knowledge check

### Question 1

A student portal experiences heavy traffic during admissions. The team wants the number of VM instances to increase automatically. Which Azure feature is a strong fit?

- A. Virtual Machine Scale Sets
- B. Azure Resource Groups
- C. Azure Container Registry

**Answer: A.** Scale sets manage groups of VMs and can scale the number of instances.

### Question 2

What does horizontal scaling mean?

- A. Increasing the memory of one VM only.
- B. Adding more VM instances or removing instances as demand changes.
- C. Moving a resource to another resource group.

**Answer: B.** Horizontal scaling changes the number of instances.

### Question 3

What is the main purpose of an availability set?

- A. To store application backups.
- B. To distribute VMs across fault and update domains to reduce correlated failures.
- C. To automatically translate code into containers.

**Answer: B.** Availability sets help reduce the chance that one failure or maintenance event affects all grouped VMs.

### Question 4

What is a fault domain?

- A. A group of infrastructure components that share a potential failure source.
- B. A pricing tier for App Service.
- C. A kind of user account.

**Answer: A.** Fault domains help isolate VMs from shared infrastructure failure sources.

### Question 5

Which feature uses physically separate locations within a supported Azure region to help protect against datacentre-level failures?

- A. Availability sets
- B. Availability zones
- C. Resource groups

**Answer: B.** Availability zones are separate physical locations within a region.

## 6. Key takeaways

- Virtual Machine Scale Sets manage groups of VMs and can scale the number of instances.
- Horizontal scaling changes the number of instances; vertical scaling changes the capacity of an individual VM.
- Availability sets spread VMs across fault and update domains.
- Fault domains help isolate shared infrastructure failures.
- Update domains help separate planned maintenance.
- Availability zones use separate physical locations within a supported region and generally provide stronger datacentre-level isolation than availability sets.
- These features reduce specific risks but do not replace application-level resilience, backup, monitoring, or disaster recovery planning.

## 7. Official Microsoft Learn references

- [Virtual Machine Scale Sets documentation](https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/)
- [Availability options for Azure Virtual Machines](https://learn.microsoft.com/en-us/azure/virtual-machines/availability)
- [Availability sets overview](https://learn.microsoft.com/en-us/azure/virtual-machines/availability-set-overview)
- [Introduction to Virtual Machine Scale Sets](https://learn.microsoft.com/en-us/training/modules/intro-to-azure-virtual-machine-scale-sets/)

---

**Unofficial study resource:** This is original AZ-900 preparation material, not an official Microsoft exam question set or a guarantee of exam coverage.
