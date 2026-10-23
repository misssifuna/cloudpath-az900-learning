# Learning Path 3 — Module 1, Unit 6: Describe cost optimization options in Azure

**Module:** Describe cost management in Azure  
**Learning goal:** Recognize common ways to reduce waste and align resource choices with workload needs.

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

## Quick knowledge check
**What is one sensible cost-optimization practice?**

**Answer:** Right-size resources, remove unused resources, choose suitable storage tiers, or use pricing options that match predictable workloads.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
