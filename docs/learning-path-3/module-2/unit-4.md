# Learning Path 3 — Module 2, Unit 4: Describe the purpose of resource locks

**Module:** Describe features and tools in Azure for governance and compliance  
**Learning goal:** Explain how resource locks help prevent accidental deletion or modification.

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

## Quick knowledge check
**What is the main purpose of a resource lock?**

**Answer:** To help prevent accidental deletion or modification of a protected resource; it is not a substitute for access control or backup.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
