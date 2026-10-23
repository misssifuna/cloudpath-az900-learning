# Learning Path 3 — Module 3, Unit 4: Describe Azure Resource Manager and ARM templates

**Module:** Describe features and tools for managing and deploying Azure resources  
**Learning goal:** Explain the role of Azure Resource Manager and recognize infrastructure as code and ARM templates.

## 4. Azure Resource Manager (ARM)

Azure Resource Manager is Azure's deployment and management service. It provides a consistent management layer for creating, updating, and deleting resources.

When you manage resources through the Azure portal, CLI, PowerShell, or an ARM template, those tools can use Azure Resource Manager to carry out the management operation.

Think of ARM as the management layer coordinating Azure resource operations—not a virtual machine or a storage service.

## 5. Infrastructure as code (IaC) and ARM templates

**Infrastructure as code (IaC)** means describing infrastructure in files so that it can be reviewed, version-controlled, reused, and deployed consistently.

An **ARM template** is a JSON file that declares the Azure resources and configuration you want. Rather than manually creating each resource every time, you define the desired resources in the template and deploy it.

Benefits include:
- **Consistency:** repeat deployments with the same defined configuration.
- **Automation:** use templates in deployment workflows.
- **Version control:** store and review infrastructure definitions in Git.
- **Reusability:** share or adapt templates for multiple environments.

**Declarative vs. imperative:**
- Declarative: state *what* the desired end state should contain.
- Imperative: specify *how* to perform the steps in sequence.

ARM templates are declarative. Bicep is another Azure IaC language that provides a more concise syntax and is converted into ARM deployment representations.

**Example:** GeekHub needs a test and production environment with similar network and storage resources. An IaC template can define the intended setup so it can be deployed more consistently, with environment-specific parameters where needed.

## Quick knowledge check
**What is a benefit of infrastructure as code?**

**Answer:** It makes deployments repeatable and reviewable by defining infrastructure in files rather than relying only on manual steps.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
