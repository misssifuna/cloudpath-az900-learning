# Learning Path 2 — Module 4, Unit 3: Describe Azure storage redundancy

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure storage services  
**Learning goal:** Compare common Azure Storage redundancy options and understand why redundancy is not the same as backup.

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



## 6. Moving files and migrating data

Know the purpose of these tools for AZ-900:

- **AzCopy:** command-line utility for copying data to, from, or between supported Azure Storage locations.
- **Azure Storage Explorer:** graphical application for working with Azure Storage data.
- **Azure File Sync:** synchronizes Windows Server file shares with Azure Files, helping organizations retain local file-server access while using a cloud file share.
- **Azure Migrate:** helps assess and migrate workloads to Azure; it is a broader migration service, not simply a file-copy command.
- **Azure Data Box:** physical appliance-based transfer option for moving large volumes of data when transferring over the network is impractical.

Choose the tool based on what is being moved, the source and destination, volume, available bandwidth, and whether you need synchronization or migration assessment.

## 5. Storage, backup, and redundancy are not identical

Redundancy helps protect data against certain infrastructure failures. It does not necessarily protect against accidental deletion, unwanted edits, compromised credentials, or every application-level problem.

A robust plan may also need backups, soft delete, versioning, access controls, and tested recovery procedures, depending on the service and requirements.

## Quick knowledge check
Which redundancy option copies data across availability zones within the primary region?

**Answer:** ZRS.

## Official learning resource
[Describe Azure storage services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)
