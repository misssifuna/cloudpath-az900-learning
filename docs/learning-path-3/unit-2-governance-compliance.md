# Learning Path 3 — Unit 2: Azure Governance and Compliance

**Topic:** Azure management and governance  
**Estimated study time:** 15–20 minutes

## Learning objectives

By the end of this lesson, you should be able to:

- Explain why organizations use governance and compliance tools.
- Describe Microsoft Purview, Azure Policy, resource locks, and the Service Trust Portal.
- Distinguish Azure Policy from Azure RBAC.
- Distinguish resource locks from permissions.
- Apply these ideas to a school or small business Azure environment.

## 1. Governance and compliance: why do they matter?

Imagine GeekHub manages Azure resources for several schools. Each school may have rules about where data is stored, which resources can be created, how resources are tagged, and which important resources must not be accidentally deleted.

**Governance** means setting and applying rules so resources are managed consistently and responsibly.

**Compliance** means meeting applicable requirements, such as internal policies, contractual commitments, or relevant legal and regulatory obligations.

Azure provides tools to help organizations implement and monitor controls. A tool can support compliance, but using it does not automatically make an organization compliant with every law or standard.

## 2. Microsoft Purview

**Microsoft Purview** provides data governance and compliance capabilities. Depending on the services and configuration in use, it can help organizations discover and understand data, classify it, and manage data-related risks and compliance requirements.

Example: a school wants to understand where sensitive student information is stored and how it is governed. Purview capabilities can help the organization discover and classify data across supported environments.

Remember the broad purpose: **data governance and compliance**. Purview is not the same as Azure RBAC, which assigns permissions to Azure resources.

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

## 4. Azure Policy vs. Azure RBAC

This is an important distinction.

| Tool | Main question | Example |
|---|---|---|
| **Azure Policy** | Does the resource or action comply with organizational rules? | Prevent a storage account from being created in an unapproved region. |
| **Azure RBAC** | Which identity can perform which actions on which resources? | Allow a developer to manage resources in one resource group. |

A user might have permission to create a resource through RBAC, but Azure Policy can still deny the deployment if it violates an assigned policy. They complement each other; neither replaces the other.

## 5. Azure resource locks

A **resource lock** helps protect Azure resources from accidental deletion or modification. Locks can be applied at supported scopes such as a subscription, resource group, or resource. A lock at a parent scope can affect resources underneath it.

Two main lock types:

- **CanNotDelete (Delete lock):** users can read and modify the resource, but cannot delete it while the lock remains in effect.
- **ReadOnly (Read-only lock):** users can read the resource but cannot update or delete it through the covered Azure Resource Manager control-plane operations.

### Example

The school website is critical during exam registration. A CanNotDelete lock on its resource group can help prevent someone from accidentally deleting the website resources.

### Important limitations

- A lock does not grant permissions. Azure RBAC still determines who has access.
- Locks override otherwise sufficient permissions for covered management operations.
- A lock is not a backup and does not guarantee that data cannot be deleted through every data-plane operation.
- ReadOnly locks can interfere with legitimate operations, so apply them carefully and test expected workflows.
- A lock can be removed by an appropriately authorized identity. Protecting access to lock management remains important.

## 6. Service Trust Portal

The **Microsoft Service Trust Portal** provides information and resources about Microsoft's security, privacy, and compliance practices for its cloud services. Depending on access and the resource, it can provide compliance documentation, audit reports, and related trust materials.

Example: an organization evaluating Microsoft cloud services may consult the portal to review Microsoft's published compliance documentation as part of its own risk and procurement process.

The portal provides evidence and documentation; it does not automatically certify that a customer's specific Azure deployment is compliant.

## 7. Put the tools together

For a school's Azure environment:

1. **Microsoft Purview** can help discover, classify, and govern supported data.
2. **Azure Policy** checks resources against deployment and configuration standards.
3. **Azure RBAC** determines who can create, update, or manage resources.
4. **Resource locks** help prevent accidental deletion or modification of important resources.
5. **Service Trust Portal** provides Microsoft's published trust and compliance documentation.

Governance is most effective when rules, permissions, monitoring, documentation, and human processes work together.

## 8. Knowledge check

Try answering before looking at the answer key.

1. An organization wants to prevent resources from being deployed outside approved Azure regions. Which tool is best suited to enforce this rule?
2. Which tool determines whether a developer has permission to update a virtual machine?
3. A critical resource should remain editable but must not be accidentally deleted. Which lock type fits?
4. What does an Azure Policy initiative contain?
5. Where can an organization review Microsoft's published cloud compliance and trust documentation?
6. Does having a resource lock mean the resource is backed up?

### Answer key

1. **Azure Policy**, with an appropriate allowed-locations policy and assignment.
2. **Azure RBAC.**
3. **CanNotDelete (Delete lock).**
4. **A group of related policy definitions.**
5. **Microsoft Service Trust Portal.**
6. **No.** A lock is not a backup; backup and recovery must be planned separately.

## Key takeaways

- Governance sets and applies organizational rules; compliance concerns meeting applicable requirements.
- Microsoft Purview supports data governance and compliance capabilities.
- Azure Policy audits or enforces resource rules.
- Azure RBAC assigns permissions to identities at defined scopes.
- Resource locks help protect resources against covered accidental deletion or modification operations.
- The Service Trust Portal provides Microsoft's published security, privacy, and compliance documentation.
- These tools support governance but do not, by themselves, guarantee complete compliance or security.

## Official Microsoft Learn resources

- [Describe features and tools for governance and compliance in Azure](https://learn.microsoft.com/en-us/training/modules/describe-features-tools-azure-for-governance-compliance/)
- [Azure Policy overview](https://learn.microsoft.com/en-us/azure/governance/policy/overview)
- [Lock Azure resources](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/lock-resources)
- [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/)
- [AZ-900 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
