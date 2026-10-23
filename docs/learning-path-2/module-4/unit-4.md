# Learning Path 2 — Module 4, Unit 4: Describe Azure storage services

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure storage services  
**Learning goal:** Compare the main Azure Storage services and recognize Blob access tiers for different access patterns.

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

## Quick knowledge check

**Which service is best suited to storing website images and PDFs as unstructured objects?**

**Answer:** Azure Blob Storage.

## Official learning resource

[Describe Azure storage services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)
