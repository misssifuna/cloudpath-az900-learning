# Learning Path 2 — Module 1, Unit 5: Describe Azure management infrastructure

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module 1:** Describe the core architectural components of Azure  
**Unit:** Describe Azure management infrastructure

## Learning objectives

By the end of this unit, you should be able to:

- Explain what an Azure resource is.
- Distinguish resource groups, subscriptions, and management groups.
- Describe the hierarchy used to organise and govern Azure resources.
- Choose a sensible scope for organising a simple Azure deployment.

## 1. From physical infrastructure to management infrastructure

In Unit 4, we explored where Azure runs: datacentres, regions, and availability zones. Now we move from **where Azure resources run** to **how you organise and manage them**.

Imagine GeekHub Solutions is helping a school deploy a website, a database, and file storage in Azure. The school needs a way to keep related items together, manage access, apply rules, and understand costs. Azure's management hierarchy helps with that.

## 2. Azure resources

A **resource** is an individual item you create and manage in Azure. Examples include:

- A virtual machine (a computer hosted in Azure).
- A virtual network (networking for Azure resources).
- A storage account (a place to store data).
- A database or web app.

Think of each resource as one managed component of a solution. Resources have settings and properties, and many have a location, such as an Azure region.

## 3. Resource groups

A **resource group** is a container for resources that are managed together. For example, a school's website might have its web app, database, and supporting resources placed in a resource group called `school-website-prod`.

Resource groups are useful for organising related resources, controlling access, applying certain management operations, and reviewing costs.

Important details:

- Every resource belongs to a resource group.
- A resource group stores metadata about the resources it contains.
- A resource group has a location for its metadata; the resources inside it can be in different regions.
- A resource can belong to only one resource group at a time.
- Deleting a resource group deletes the resources within it, so this action must be treated carefully.

**Practical rule:** Group resources that share a lifecycle or are managed together. Do not assume that a resource group is a physical building or a data centre.

## 4. Azure subscriptions

An **Azure subscription** is a logical management and billing boundary for Azure resources. It is also an important scope for access control and policies.

A subscription helps an organisation separate workloads, environments, teams, or budgets. For example, GeekHub might use separate subscriptions for development and production if its governance and billing needs justify that arrangement.

Remember:

- Resources are created within a subscription.
- A subscription can contain multiple resource groups.
- A subscription is associated with a billing arrangement, but the exact invoice and payment setup depends on the account and offer.
- A subscription is not the same thing as a Microsoft account or a physical Azure region.

A person signs in using an identity, then uses permissions to access subscriptions and the resources within them.

## 5. Management groups

A **management group** is a level above subscriptions. Organisations can use management groups to organise multiple subscriptions and apply governance, such as Azure Policy or access controls, at a broader scope.

For example, a company might have a management group called `Production` containing several production subscriptions. A policy assigned at that management-group scope can be inherited by the subscriptions and supported resources beneath it.

Not every small project needs a complicated management-group structure. It becomes more useful as an organisation grows and needs consistent rules across many subscriptions.

## 6. Learn the hierarchy

The common hierarchy from broadest to most specific is:

1. **Management groups** — organise subscriptions.
2. **Subscriptions** — organise and govern resource usage and billing.
3. **Resource groups** — group related resources for management.
4. **Resources** — the individual services and components.

A simplified view:

```text
Management group
├── Subscription: Production
│   ├── Resource group: School-Website
│   │   ├── Web app
│   │   ├── Database
│   │   └── Storage account
│   └── Resource group: School-Analytics
│       └── Analytics resources
└── Subscription: Development
    └── Resource group: Website-Test
        └── Test web app
```

The hierarchy is logical, not a map of physical locations. For instance, resources in one resource group may be deployed to different Azure regions if the resource types and design allow it.

## 7. A school example

Suppose a school wants a public website and a separate environment for testing changes.

- **Resources:** the website app, database, and storage.
- **Resource group:** keeps the production website components together.
- **Subscription:** provides a boundary for managing access, usage, and billing; the school could separate production and development into different subscriptions.
- **Management group:** could group the school's subscriptions if it has several and needs common policies.

The right structure depends on the organisation's scale, security needs, and operating model. This is an example design, not a requirement that every school must use multiple subscriptions.

## 8. Knowledge check

Choose an answer before checking the explanation.

### Question 1
Which Azure component is designed to group related resources that are managed together?

- A. Availability zone
- B. Resource group
- C. Azure region
- D. Management group

**Answer: B — Resource group.** A resource group is a logical container for related Azure resources.

### Question 2
A large organisation wants to apply governance across several Azure subscriptions. Which scope is designed to sit above subscriptions?

- A. Resource
- B. Resource group
- C. Management group
- D. Availability zone

**Answer: C — Management group.** Management groups help organise subscriptions and apply governance across them.

### Question 3
Which statement about a resource group is correct?

- A. It is a physical datacentre.
- B. Every resource group must contain resources from only one physical datacentre.
- C. Its metadata has a location, but its resources can be in different regions.
- D. It is the identity used to sign in to Azure.

**Answer: C.** A resource group's metadata location does not require all its resources to be deployed in that same region.

### Question 4
Put these scopes in order from broadest to most specific:

**Management group → Subscription → Resource group → Resource**

This order is the key hierarchy to remember for AZ-900.

## 9. Key takeaways

- **Resource:** an individual Azure service or component.
- **Resource group:** a container for resources managed together.
- **Subscription:** a boundary for organising resource usage, access, and billing.
- **Management group:** a way to organise and govern multiple subscriptions.
- The hierarchy is **management groups → subscriptions → resource groups → resources**.
- These are logical management scopes, not physical infrastructure locations.

## 10. Official Microsoft Learn references

- [Organize your Azure resources](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-setup-guide/organize-resources)
- [Azure management groups](https://learn.microsoft.com/en-us/azure/governance/management-groups/overview)
- [Azure Resource Manager overview](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)

---

**Unofficial study resource:** This lesson is original study material for AZ-900 preparation. It is not an official Microsoft exam question set or a guarantee of exam coverage.
