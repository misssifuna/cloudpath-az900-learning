# Learning Path 3 — Module 2, Unit 3: Describe the purpose of Azure Policy

**Module:** Describe features and tools in Azure for governance and compliance  
**Learning goal:** Explain how Azure Policy evaluates and enforces organizational rules for Azure resources.

## 3. Azure Policy

**Azure Policy** evaluates resources against organizational rules and can audit or enforce compliance.

Examples of policies:
- Allow resources to be deployed only in approved Azure regions.
- Require a specific tag, such as `Owner`.
- Audit whether resources send diagnostic logs to a designated workspace.
- Restrict deployment of resource types that the organization has not approved.

A policy can have different effects. For example, it may audit a resource, deny a non-compliant deployment, or modify/deploy configuration where the policy and permissions support it.

### Policy definitions, initiatives, and assignments

- **Policy definition:** describes a rule and its evaluation behavior.
- **Initiative (policy set):** groups related policy definitions toward a broader goal.
- **Assignment:** applies a policy or initiative to a scope, such as a management group, subscription, or resource group.

### Example

A school wants new production resources to use approved regions and include an Environment tag. Administrators can assign appropriate policies to the relevant subscription or resource group. Depending on the policy effect, Azure can audit non-compliance or block certain deployments.

## Quick knowledge check
**What can Azure Policy do?**

**Answer:** Audit or enforce resource configuration requirements, such as allowed locations or required tags.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
