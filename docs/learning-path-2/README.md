# Learning Path 2 — Syllabus-aligned module and unit index

**Primary reference:** [AZ-900 Badge Links Reference](../AZ-900-BADGE-LINKS-REFERENCE.md)

This index follows the unit order in the Badge Links reference and links to dedicated lesson files for all five modules. The combined notes have been split, with original versions preserved under supplementary content. The supplied notes contain one verified title discrepancy in networking Unit 2, documented in the source reference and reflected here.

The module and unit numbering follows the intended CloudPath sequence. Current Microsoft Learn remains authoritative for exam scope and technical accuracy.

## Module 1 — Describe the core architectural components of Azure

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | [Current lesson](module-1/unit-1.md) |
| 2 | What is Microsoft Azure | [Current lesson](module-1/unit-2.md) |
| 3 | Get started with Azure accounts | [Current lesson](module-1/unit-3.md) |
| 4 | Describe Azure physical infrastructure | [Current lesson](module-1/unit-4.md) |
| 5 | Describe Azure management infrastructure | [Current lesson](module-1/unit-5.md) |

**Status:** 5 reference units have corresponding files. Confirm each lesson's details against the reference before marking every objective fully covered.

## Module 2 — Describe Azure compute services

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | [Current lesson](module-2/unit-1.md) |
| 2 | Describe Azure virtual machines | [Current lesson](module-2/unit-2.md) |
| 3 | Describe Azure virtual desktop | [Aligned lesson](module-2/unit-3.md) |
| 4 | Describe Azure containers | [Aligned lesson](module-2/unit-4.md) |
| 5 | Describe Azure functions | [Existing lesson](module-2/unit-5.md) |
| 6 | Describe AI, machine learning, and IoT/Edge services in Azure | [Dedicated lesson](module-2/unit-6.md) |
| 7 | Describe application hosting options | [Aligned lesson](module-2/unit-7.md), expanded beyond App Service |

The former Unit 7 lesson on Virtual Machine Scale Sets and Availability Sets has been preserved as [supplementary content](supplementary/virtual-machine-scale-sets-and-availability-sets.md). The old `unit-6.md` path is now a pointer to the canonical Virtual Desktop Unit 3 lesson, to reduce confusion from the previous numbering.

## Module 3 — Describe Azure networking services

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | [Dedicated introduction](module-3/unit-1.md) |
| 2 | Create, configure, and manage users | **Source discrepancy:** CloudPath uses [Describe Azure virtual networking](module-3/unit-2.md), matching current Microsoft Learn. See the [reference note](../AZ-900-BADGE-LINKS-REFERENCE.md). |
| 3 | Describe Azure virtual private networks | [Dedicated VPN lesson](module-3/unit-3.md) |
| 4 | Describe Azure ExpressRoute | [Dedicated lesson](module-3/unit-4.md) |
| 5 | Describe Azure DNS | [Dedicated lesson](module-3/unit-5.md) |

The existing Public and Private Endpoints topic has been preserved as [supplementary content](supplementary/public-private-endpoints.md).

## Module 4 — Describe Azure storage services

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | [Dedicated introduction](module-4/unit-1.md) |
| 2 | Describe Azure storage accounts | [Dedicated lesson](module-4/unit-2.md) |
| 3 | Describe Azure storage redundancy | [Dedicated lesson](module-4/unit-3.md) |
| 4 | Describe Azure storage services | [Dedicated lesson](module-4/unit-4.md) |
| 5 | Identify Azure data migration options | [Dedicated lesson](module-4/unit-5.md) |
| 6 | Identify Azure file movement options | [Dedicated lesson](module-4/unit-6.md) |

## Module 5 — Describe Azure identity, access, and security

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | [Dedicated introduction](module-5/unit-1.md) |
| 2 | Describe Azure directory services | [Dedicated lesson](module-5/unit-2.md) |
| 3 | Describe Azure authentication methods | [Dedicated lesson](module-5/unit-3.md) |
| 4 | Describe Azure external identities | [Dedicated lesson](module-5/unit-4.md) |
| 5 | Describe Azure conditional access | [Dedicated lesson](module-5/unit-5.md) |
| 6 | Describe Azure role-based access control | [Dedicated lesson](module-5/unit-6.md) |
| 7 | Describe Zero Trust model | [Dedicated lesson](module-5/unit-7.md) |
| 8 | Describe defense-in-depth | [Dedicated lesson](module-5/unit-8.md) |
| 9 | Describe encryption and key management in Azure | [Dedicated lesson](module-5/unit-9.md) |
| 10 | Describe Microsoft Defender for Cloud | [Dedicated lesson](module-5/unit-10.md) |

The combined original storage, identity, security, and networking notes have been preserved in `supplementary/` before splitting. Public/private endpoints and VM Scale Sets/Availability Sets are also preserved as supplementary lessons.

## Reconciliation notes

- Combined lessons were split into dedicated unit files, and original combined notes were preserved under supplementary content.
- Virtual Machine Scale Sets and Availability Sets, plus Public/Private Endpoints, remain available as supplementary AZ-900 topics rather than replacing reference units.
- The supplied networking Unit 2 title was checked against current Microsoft Learn; CloudPath uses “Describe Azure virtual networking” and records the discrepancy in the source reference.
- Continue auditing the technical content of every lesson against the [official AZ-900 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900) before marking all objectives fully verified.

**Current status:** All five modules now have reference-aligned unit files or dedicated pointers. The compute sequence has a dedicated AI/ML/IoT/Edge lesson; networking, storage, and identity/security combined notes have been split into dedicated units. The suspicious networking title was checked against current Microsoft Learn and documented as a source discrepancy. Original combined lessons and extra AZ-900 topics are preserved in `supplementary/`. Continue the content audit before marking every objective complete.
