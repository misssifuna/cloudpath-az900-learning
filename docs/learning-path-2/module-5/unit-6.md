# Learning Path 2 — Module 5, Unit 6: Describe Azure role-based access control

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Explain how Azure RBAC assigns roles to identities at a scope.

## 8. Azure role-based access control (Azure RBAC)

**Azure RBAC** manages who can perform which actions on Azure resources. A role assignment generally connects:

- **Security principal:** the user, group, service principal, or managed identity receiving access.
- **Role definition:** the permitted actions.
- **Scope:** where the permissions apply.

Azure RBAC scopes can include a management group, subscription, resource group, or individual resource. Permissions assigned at a broader scope can flow down to contained scopes.

Common built-in roles include:

- **Owner:** can manage resources and assign access.
- **Contributor:** can manage resources but cannot grant other users access through Azure RBAC.
- **Reader:** can view resources but not make changes to them.

The exact permissions depend on the role definition and scope. Use the **principle of least privilege**: give people only the access they need to perform their tasks, at the narrowest practical scope.

**Example:** A developer who deploys the school's website might need Contributor access to one app's resource group, but not Owner access to the whole subscription.

### Don't confuse Entra roles and Azure RBAC

- **Microsoft Entra roles** manage identity-directory tasks, such as managing users.
- **Azure RBAC roles** manage access to Azure resources, such as a storage account or virtual machine.

They solve related but different permission problems.

## Quick knowledge check
**What does Azure RBAC control?**

**Answer:** Which actions an identity can perform on Azure resources at a given scope.

## Official learning resource
[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
