# Learning Path 2 — Module 4, Unit 1: Azure Storage Services

## Learning goals

By the end of this lesson, you should be able to:
- Compare Azure Blob Storage, Azure Files, Azure Table Storage, and Azure Queue Storage.
- Explain what a storage account does.
- Distinguish Blob Storage access tiers.
- Explain the purpose of storage redundancy.
- Recognize common tools for moving files and migrating data.

## 1. The four main Azure Storage services

Imagine a school in Saboti moving some of its operations to Azure. It needs to store student documents, share files among staff, and protect its information if hardware fails.

### Azure Blob Storage

Blob Storage stores large amounts of unstructured data, such as photos, videos, PDFs, backups, and website images.

**School example:** storing scanned certificates and images for a school website.

### Azure Files

Azure Files provides managed file shares that multiple clients can access using supported file-sharing protocols.

**School example:** a shared folder for teachers' lesson plans and administrative documents.

### Azure Table Storage

Table Storage stores structured, non-relational data as entities with properties.

**School example:** a simple collection of student-related records organized by keys and fields. It is not the same as a traditional relational SQL database.

### Azure Queue Storage

Queue Storage stores messages that allow different parts of an application to communicate asynchronously.

**School example:** queuing requests to generate student report PDFs so the system can process them in the background.

**Memory trick:** Blob = objects, Files = shared folders, Table = non-relational records, Queue = messages.

## 2. What is a storage account?

A **storage account** is the top-level Azure resource that provides a namespace and configuration for supported Azure Storage services. It is where important settings such as redundancy and certain network options are configured.

Think of it as the managed storage facility within which you create the storage resources your application needs. Different storage account types support different services and performance features, so check the supported options when designing a solution.

## 3. Blob access tiers: how often do you need the data?

Blob Storage offers access tiers to help balance storage costs against access costs and retrieval time.

- **Hot:** data accessed frequently.
- **Cool:** data accessed infrequently, but still expected to be available without the long delay associated with archive rehydration.
- **Cold:** data accessed very infrequently, with a longer minimum recommended retention period than cool.
- **Archive:** long-term data that is rarely accessed and can tolerate hours of retrieval delay when rehydration is required.

In general, cooler tiers reduce storage costs but have higher access or transaction costs. Archive has the lowest storage cost among these tiers but the highest access costs and can take hours to retrieve. Minimum retention and early deletion charges may apply, and not every redundancy option supports archive.

**School example:**
- Current school website images might suit Hot.
- Older documents that may be needed occasionally could suit Cool or Cold, depending on access needs.
- Historical records kept for long-term retention and rarely accessed might suit Archive if the retrieval delay is acceptable and policy requirements allow it.

Do not choose a tier based only on the age of a file. Consider access frequency, retrieval latency, retention, and total cost.

## 4. Redundancy: what if hardware or a location fails?

Azure Storage keeps copies of data according to the redundancy option selected for the storage account. Redundancy improves durability and can improve availability, but it is not a substitute for every form of backup or recovery planning.

| Option | Meaning | General use |
|---|---|---|
| LRS — Locally redundant storage | Multiple copies within a single physical location in the primary region | Lower-cost protection against local hardware failures |
| ZRS — Zone-redundant storage | Synchronous copies across separate availability zones in one region | Protection against a zone failure |
| GRS — Geo-redundant storage | LRS in the primary region plus asynchronous replication to a secondary region | Additional protection against a regional disaster |
| GZRS — Geo-zone-redundant storage | ZRS in the primary region plus asynchronous replication to a secondary region | Zone resilience plus geographic disaster protection |

Read-access variants (RA-GRS and RA-GZRS) can provide read access to the secondary region. Replication and failover behavior vary; geo-replication is generally asynchronous, so the latest writes might not have reached the secondary region when an outage occurs. An account failover may be required to restore write availability after a primary-region outage.

Availability of redundancy options depends on the storage service, account type, and region. Archive tier has restrictions on supported redundancy options.

**Memory trick:**
- **L**RS = Local
- **Z**RS = Zones
- **G**RS = Geography
- **GZ**RS = Zones in the primary region plus Geography

## 5. Storage, backup, and redundancy are not identical

Redundancy helps protect data against certain infrastructure failures. It does not necessarily protect against accidental deletion, unwanted edits, compromised credentials, or every application-level problem.

A robust plan may also need backups, soft delete, versioning, access controls, and tested recovery procedures, depending on the service and requirements.

## 6. Moving files and migrating data

Know the purpose of these tools for AZ-900:

- **AzCopy:** command-line utility for copying data to, from, or between supported Azure Storage locations.
- **Azure Storage Explorer:** graphical application for working with Azure Storage data.
- **Azure File Sync:** synchronizes Windows Server file shares with Azure Files, helping organizations retain local file-server access while using a cloud file share.
- **Azure Migrate:** helps assess and migrate workloads to Azure; it is a broader migration service, not simply a file-copy command.
- **Azure Data Box:** physical appliance-based transfer option for moving large volumes of data when transferring over the network is impractical.

Choose the tool based on what is being moved, the source and destination, volume, available bandwidth, and whether you need synchronization or migration assessment.

## Quick knowledge check

1. A school needs to store photos and PDF documents for a website. Which service is the best fit?
   - A. Azure Queue Storage
   - B. Azure Blob Storage
   - C. Azure VPN Gateway

2. Teachers need a shared file folder accessible from multiple clients. Which service fits best?
   - A. Azure Files
   - B. Azure Table Storage
   - C. Azure DNS

3. Which Blob access tier is intended for data rarely accessed and where hours of retrieval delay can be acceptable?
   - A. Hot
   - B. Archive
   - C. Cool

4. Which redundancy option copies data across separate availability zones within one region?
   - A. LRS
   - B. ZRS
   - C. GRS

5. Which tool is a graphical application for managing Azure Storage data?
   - A. Azure Storage Explorer
   - B. Azure Data Box
   - C. Azure VPN Gateway

### Answers and explanations

1. **B — Azure Blob Storage.** It is designed for unstructured object data such as images, PDFs, and backups.
2. **A — Azure Files.** It provides managed file shares.
3. **B — Archive.** Archive is for rarely accessed data and may require hours to rehydrate.
4. **B — ZRS.** Zone-redundant storage replicates data across availability zones in the primary region.
5. **A — Azure Storage Explorer.** It provides a graphical interface for working with Azure Storage.

## Key takeaway

**Choose storage by data type, access pattern, and resilience needs.** Blob stores objects, Files provides file shares, Table stores non-relational entities, and Queue stores messages. Tiers manage access-cost trade-offs; redundancy helps protect against infrastructure failures.

## Official Microsoft Learn references

- [Describe Azure storage services — AZ-900 learning module](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)
- [Storage account overview](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview)
- [Blob access tiers](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview/)
- [Azure Storage redundancy](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy)
- [Azure storage migration and file movement options](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)

These are original study notes for AZ-900 preparation, not official exam questions or a substitute for the current Microsoft Learn study guide.
