# Learning Path 3 — Unit 1: Azure Cost Management, Pricing, and Tags

**Topic:** Azure management and governance  
**Estimated study time:** 15–20 minutes

> Roadmap note: this lesson begins the management-and-governance section of CloudPath. The official Microsoft Learn path groups cost management, governance/compliance, and Azure management tools in this learning path.

## Learning objectives

By the end, you should be able to:

- Identify factors that influence Azure costs.
- Explain what the Azure Pricing Calculator estimates.
- Explain how Microsoft Cost Management helps track and control spending.
- Describe Azure budgets and alerts.
- Explain how resource tags help organize and analyze costs.
- Recognize common cost-optimization options.

## 1. Why cloud costs need active management

Cloud computing makes it possible to provision resources quickly. That convenience can create surprises if resources are left running, oversized, or deployed in ways that cost more than expected.

Imagine GeekHub hosts a school website in Azure. Its costs might include the app hosting plan, database, storage, backups, networking, monitoring, and data transfer. A resource can keep incurring charges even when nobody is actively visiting the website.

**Key idea:** cloud resources are not automatically free just because they are easy to create. Understand the pricing model, estimate before deployment, monitor usage, and remove resources you no longer need.

## 2. What affects Azure costs?

Common cost factors include:

- **Resource type and size:** a larger VM or higher-capacity service generally costs more than a smaller configuration.
- **Consumption and running time:** compute charges may depend on time running, requests, transactions, or other measured usage.
- **Storage amount and operations:** how much data is stored, the access tier, and the number or type of operations can affect costs.
- **Region:** pricing can vary by Azure region.
- **Service tier and features:** premium performance, extra capacity, or optional security and monitoring features may add cost.
- **Networking and data transfer:** some data transfer and networking services can incur charges.
- **Licensing and purchasing model:** eligible licenses, commitments, and discounts can change the effective price.
- **Resiliency and backup choices:** replication, additional instances, and backup retention can increase cost while improving availability or recovery.

Don't memorize a single price as universal. Prices and service options can change, and actual cost depends on configuration, region, usage, agreement, and discounts.

## 3. Azure Pricing Calculator

The **Azure Pricing Calculator** is used to estimate expected Azure service costs before deployment.

Typical workflow:
1. Choose the services you plan to use.
2. Configure options such as region, tier, size, and estimated usage.
3. Review the estimated costs.
4. Compare alternative designs and adjust the estimate.

**Example:** compare two possible hosting plans for a school's website before selecting one.

The calculator is an estimate, not a guarantee of the final invoice. Estimates depend on the assumptions you enter and may not capture every tax, negotiated discount, variable usage, or ancillary charge.

Open the [Azure Pricing Calculator](https://azure.microsoft.com/pricing/calculator/).

## 4. Microsoft Cost Management

**Microsoft Cost Management** helps analyze, monitor, and optimize Microsoft Cloud costs. Its capabilities include:

- **Cost Analysis:** explore spending by subscription, resource group, service, time period, and other available dimensions.
- **Budgets:** set a target amount for a defined scope and period.
- **Alerts:** notify relevant people when a configured budget threshold or other supported condition is reached.
- **Exports:** make cost and usage data available for further analysis.
- **Optimization recommendations:** help identify possible savings.

### Budget vs. alert vs. hard spending limit

These concepts are not interchangeable:

- A **budget** tracks spending against a target.
- An **alert** notifies you when a configured condition is met.
- A budget does **not automatically cap spending or shut down all resources**. Any automated response requires a separately configured action or process, and not every action is appropriate for every workload.

**Example:** GeekHub sets a monthly budget for a test environment and configures notifications at selected thresholds. The team receives a warning and reviews usage. It must still decide which resources to resize or stop.

## 5. Resource tags

An Azure **tag** is a name-value pair attached to a supported resource to add organizational metadata.

Examples:

| Tag name (key) | Tag value | Why it helps |
|---|---|---|
| Environment | Development | Separate test from production costs |
| Department | IT | Identify the team responsible |
| Project | SchoolWebsite | Group project-related resources |
| Owner | GeekHub | Help identify who should review a resource |

Tags can help filter and group costs in Cost Analysis and support governance processes.

### Important limitations

- Tags are metadata; they do not themselves grant or deny access.
- Tags are not a replacement for resource groups, subscriptions, or RBAC.
- Not every resource or charge supports tags in the same way.
- Tag-based cost reporting applies according to the service's support and usage-data rules; don't assume every historic charge is retagged automatically.
- **Never put passwords, access tokens, personal information, or other secrets in tags.** Tags can appear in reports, logs, templates, and other outputs.

## 6. Cost-optimization options

Microsoft Learn highlights several options. Their availability and suitability depend on workload and terms.

- **Right-size resources:** choose a configuration that meets performance needs without unnecessary capacity.
- **Shut down or remove idle resources:** check whether the resource still needs to run. Be aware that stopping a VM and deallocating it can have different billing implications; associated disks and other resources may still cost money.
- **Reservations:** commit to eligible resource usage for a defined term in exchange for discounted pricing. Best when usage is predictable and the commitment fits your needs.
- **Savings plans:** commit to a specified amount of eligible compute spend over a term for discounted rates on qualifying usage. Check which services and regions qualify.
- **Spot pricing:** use eligible spare Azure capacity at a discounted price, while accepting that workloads can be evicted when Azure needs the capacity. It suits interruptible jobs, not workloads requiring uninterrupted availability.
- **Select appropriate storage tiers:** align access patterns and retention needs with the right storage tier while accounting for access and retrieval charges.
- **Review and monitor regularly:** compare actual costs with estimates and investigate unexpected changes.

**Exam clue:** if a workload is interruptible and needs lower-cost spare compute capacity, think **Spot**. If usage is predictable and an organization is willing to commit for a term, evaluate **Reservations** or **Savings plans**, depending on the service and pricing model.

## 7. Put it together: a school website example

Suppose a school runs a website, database, and document storage in Azure.

1. Before deployment, use the Pricing Calculator to estimate the planned configuration.
2. Apply tags such as `Project=SchoolWebsite`, `Environment=Production`, and `Owner=IT`.
3. Use Cost Analysis to review the actual spending after resources are running and usage data is available.
4. Create a budget and configure alerts to notify the responsible team.
5. Investigate unexpected increases, check for idle resources, and consider right-sizing.
6. Only choose commitments or Spot pricing when the workload and terms suit them.

This creates a loop: **estimate → deploy thoughtfully → tag → monitor → optimize**.

## 8. Knowledge check

Try answering before looking at the answer key.

1. Which tool estimates the cost of planned Azure services before you deploy them?
2. Does creating an Azure budget automatically stop resources when spending reaches the budget amount?
3. What is the purpose of a tag such as `Environment=Development`?
4. Which option may suit a batch job that can be interrupted: Spot pricing or a workload that must run continuously without interruption?
5. What should you consider before committing to a Reservation or savings plan?

### Answer key

1. **Azure Pricing Calculator.**
2. **No.** Budgets and alerts help monitor and notify; stopping resources requires separately configured action or intervention.
3. **To add metadata that helps organize, identify, filter, and analyze resources and their costs.**
4. **Spot pricing**, if the job can tolerate eviction and interruption.
5. Whether usage is predictable, eligible, and likely to continue for the commitment term; compare expected savings against flexibility and other conditions.

## Key takeaways

- Azure cost depends on service configuration, usage, region, tier, networking, and purchasing terms.
- Use the Pricing Calculator to estimate before deploying.
- Use Cost Management to analyze actual spending, budgets, alerts, and exports.
- Budgets track a target; they are not automatic hard spending caps.
- Tags add useful metadata and can help group costs, but do not control permissions.
- Right-sizing, removing idle resources, Reservations, savings plans, and Spot pricing serve different scenarios.

## Official Microsoft Learn resources

- [Describe cost management in Azure](https://learn.microsoft.com/en-us/training/modules/describe-cost-management-azure/)
- [Plan to manage Azure costs](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/plan-manage-costs)
- [Microsoft Cost Management documentation](https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/)
- [Group and allocate costs using tags](https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/group-filter)
- [AZ-900 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
