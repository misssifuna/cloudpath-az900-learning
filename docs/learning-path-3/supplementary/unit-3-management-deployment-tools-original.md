# Azure Fundamentals — Learning Path 3, Unit 3
## Azure management and deployment tools

**Exam alignment:** AZ-900 — Describe features and tools for managing and deploying Azure resources.

## Learning objectives

By the end of this lesson, you should be able to:
- Distinguish the Azure portal, Azure Cloud Shell, Azure CLI, and Azure PowerShell.
- Explain Azure Resource Manager (ARM).
- Explain infrastructure as code (IaC) and ARM templates.
- Recognize the purpose of Azure Arc.

## 1. Azure portal

The Azure portal is a web-based graphical user interface (GUI). You sign in through a browser and use menus, forms, dashboards, and resource pages to create and manage resources.

**Example:** A school administrator opens the portal to inspect a storage account or review a virtual machine's settings.

**Remember:** The portal is a way to interact with Azure; it is not the only way.

## 2. Azure Cloud Shell

Cloud Shell is a browser-accessible shell for administering Azure. It can run either:
- **Bash**, commonly used with Azure CLI.
- **PowerShell**, commonly used with Azure PowerShell.

It reduces the need to install command-line tools on your own computer. It is available from the Azure portal and uses an authenticated Azure session.

**Example:** You are using a computer where you cannot install software. You can open Cloud Shell in the browser and run an Azure command.

Cloud Shell is the environment. Azure CLI and Azure PowerShell are command-line tools you can use within it.

## 3. Azure CLI and Azure PowerShell

Both can manage Azure resources and can be used for automation, but they use different command styles.

### Azure CLI
Azure CLI commands commonly begin with `az`.

Example command to list resource groups:
```bash
az group list --output table
```

### Azure PowerShell
Azure PowerShell uses PowerShell cmdlets, commonly named with a verb-noun pattern such as `Get-AzResource`.

Example command to list resources:
```powershell
Get-AzResource
```

These are illustrative read/list commands. They require an appropriate authenticated Azure session and permissions. Creating real Azure resources may incur charges.

**Exam distinction:** Azure CLI uses the `az` command style; Azure PowerShell uses PowerShell cmdlets. Either can automate administration.

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

## 6. Azure Arc

Azure Arc helps extend Azure management and governance capabilities to resources that may be outside Azure, including supported on-premises and multicloud servers and Kubernetes environments.

**Example:** A school has a server in its own computer room and also uses Azure resources. Azure Arc can help bring supported non-Azure infrastructure into Azure management and governance.

**Remember:** Azure Arc is about managing supported resources across environments; it does not mean every resource is physically moved into Azure.

## Quick comparison

| Tool or concept | Main purpose |
|---|---|
| Azure portal | Graphical, browser-based management |
| Azure Cloud Shell | Browser-based shell environment |
| Azure CLI | Command-line management using `az` commands |
| Azure PowerShell | Command-line management using PowerShell cmdlets |
| Azure Resource Manager | Azure's management and deployment layer |
| ARM template | Declarative JSON definition of Azure resources |
| Infrastructure as code | Manage infrastructure definitions as code |
| Azure Arc | Extend Azure management to supported resources outside Azure |

## Knowledge check

Try answering before checking the answers.

1. You want to manage Azure resources using a graphical interface in a browser. Which tool should you use?
2. Which tool uses commands that commonly begin with `az`?
3. What is the difference between Cloud Shell and Azure CLI?
4. What is Azure Resource Manager responsible for?
5. A team wants to deploy a consistent set of resources repeatedly from a version-controlled file. Which concept and tool fit best?
6. What problem does Azure Arc help address?

### Answers

1. Azure portal.
2. Azure CLI.
3. Cloud Shell is the shell environment; Azure CLI is a command-line tool that can run in it.
4. It provides Azure's management and deployment layer for resource operations.
5. Infrastructure as code (IaC), using an ARM template or another suitable IaC language such as Bicep.
6. Managing supported infrastructure across Azure, on-premises, and multicloud environments.

## Official Microsoft learning resources

- [AZ-900 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
- [Describe features and tools for managing and deploying Azure resources](https://learn.microsoft.com/en-us/training/modules/describe-features-tools-manage-deploy-azure-resources/)
- [Azure Resource Manager templates overview](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/overview)
- [Azure Resource Manager documentation](https://learn.microsoft.com/en-us/azure/azure-resource-manager/)

## Completion checklist

- [ ] I can distinguish the portal, Cloud Shell, CLI, and PowerShell.
- [ ] I can explain ARM and ARM templates.
- [ ] I understand why IaC supports consistent, repeatable deployments.
- [ ] I can describe the purpose of Azure Arc.
- [ ] I can answer the knowledge-check questions without looking.
