# Learning Path 2 — Module 4, Unit 6: Identify Azure file movement options

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure storage services  
**Learning goal:** Identify common tools for copying, exploring, and synchronizing data with Azure Storage.

## 1. AzCopy

**AzCopy** is a command-line utility for copying data to, from, or between supported Azure Storage locations. It is useful when you want scripted or repeatable data-transfer operations.

## 2. Azure Storage Explorer

**Azure Storage Explorer** is a graphical application for working with Azure Storage data. It helps users browse and manage supported storage resources without relying exclusively on command-line commands.

## 3. Azure File Sync

**Azure File Sync** synchronizes Windows Server file shares with Azure Files. It can help an organization keep frequently used files available on a local file server while using an Azure file share as part of its storage arrangement.

## 4. Quick comparison

| Tool | Main purpose |
|---|---|
| AzCopy | Command-line copying of supported storage data |
| Azure Storage Explorer | Graphical access to and management of Azure Storage data |
| Azure File Sync | Synchronization between Windows Server file shares and Azure Files |
| Azure Migrate | Assessing and migrating workloads; see Unit 5 |
| Azure Data Box | Physical transfer of very large data volumes; see Unit 5 |

## Quick knowledge check

**Which tool provides a graphical interface for working with Azure Storage?**

**Answer:** Azure Storage Explorer.

## Key takeaway

Choose a file-movement tool based on whether you need command-line copying, a graphical interface, or ongoing file synchronization. For workload migration or very large physical transfers, consider the distinct options covered in Unit 5.

## Official learning resource

[Describe Azure storage services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)
