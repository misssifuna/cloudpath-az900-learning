# Learning Path 3 — Module 3, Unit 2: Describe tools for interacting with Azure

**Module:** Describe features and tools for managing and deploying Azure resources  
**Learning goal:** Distinguish the Azure portal, Cloud Shell, Azure CLI, and Azure PowerShell.

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

## Quick knowledge check
**Which option provides a browser-based graphical interface for managing Azure?**

**Answer:** The Azure portal.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
