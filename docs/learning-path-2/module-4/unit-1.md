# Learning Path 2 — Module 4, Unit 1: Introduction to Azure storage services

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure storage services  
**Learning goal:** Understand what Azure Storage is used for and preview the storage topics in this module.

## Welcome

Applications need places to keep files, records, messages, and other data. Azure provides managed storage services, but there is no single storage option that is best for every kind of information.

Imagine a school portal. It may need to store scanned certificates and website images, provide shared folders for staff, keep structured records, queue background work, and protect important data if infrastructure fails. Azure Storage services address different parts of those needs.

## What this module covers

1. **Storage accounts:** the Azure resource that provides a namespace and configuration for supported storage services.
2. **Storage redundancy:** how copies of data are maintained to help protect against particular hardware, zone, or regional failures.
3. **Storage services:** Blob Storage, Azure Files, Table Storage, and Queue Storage, plus access tiers for blob data.
4. **Data migration:** services and appliances that help move workloads or large volumes of data to Azure.
5. **File movement:** tools for copying, browsing, or synchronizing files and storage data.

## A simple way to choose

Start by asking: What kind of data is it? How often will it be accessed? Who needs to use it? How quickly must it be available after a failure? How much data must be moved, and how much network bandwidth is available?

These questions help narrow the choices before comparing cost and configuration details.

## Quick knowledge check

**Why isn't one storage service automatically the best choice for every workload?**

**Answer:** Different services are designed for different data types and access patterns, such as objects, shared files, non-relational entities, or messages.

## Key takeaway

Azure storage decisions involve both the service that holds the data and the way that data is accessed, protected, and moved.

## Official learning resource

[Describe Azure storage services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/)
