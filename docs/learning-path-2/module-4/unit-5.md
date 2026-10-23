# Learning Path 2 — Module 4, Unit 5: Identify Azure data migration options

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure storage services  
**Learning goal:** Recognize the roles of Azure Migrate and Azure Data Box in moving workloads or large volumes of data to Azure.

## 1. Migration is more than copying a file

Organizations may need to move servers, applications, databases, or large collections of data from existing systems to Azure. The right approach depends on what is being moved, its size, network capacity, downtime constraints, and the target service.

## 2. Azure Migrate

**Azure Migrate** helps organizations assess and plan migration of workloads to Azure. It can support discovery and assessment of existing environments and coordinate migration journeys for supported workloads.

**Example:** A school or business has an older server running an application. Before moving it, the team needs to understand its configuration, dependencies, and readiness for Azure. Azure Migrate is the category of tool to investigate for this workload-migration task.

## 3. Azure Data Box

**Azure Data Box** provides a physical-device-based option for transferring large volumes of data to or from Azure when moving the data over the network would be impractical. The device is shipped, loaded with data, returned, and processed through the service workflow.

**Example:** An organization has many terabytes of archived files but limited internet bandwidth. A physical transfer appliance may be more practical than uploading all data over the available connection.

## 4. Choose based on the job

- Assessing and migrating existing workloads: consider Azure Migrate.
- Transferring very large data volumes with constrained network bandwidth: consider Azure Data Box.
- Copying a smaller set of files to storage: tools such as AzCopy or Azure Storage Explorer may be more appropriate; these are covered in Unit 6.

## Quick knowledge check

**Which option is specifically associated with physical transfer of very large data volumes when network transfer is impractical?**

**Answer:** Azure Data Box.

## Key takeaway

Azure Migrate helps assess and plan workload migration; Azure Data Box supports physical transfer of large data volumes. They are not simply interchangeable file-copy tools.

## Official learning resource

[Describe Azure storage services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)
