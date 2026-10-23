# Learning Path 3 — Module 1, Unit 4: Describe Microsoft Cost Management

**Module:** Describe cost management in Azure  
**Learning goal:** Explain how Microsoft Cost Management helps analyze and manage actual Azure spending.

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

## Quick knowledge check
**What is the difference between a cost estimate and cost analysis?**

**Answer:** An estimate models planned usage; cost analysis helps review recorded costs and usage.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
