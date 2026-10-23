# Learning Path 2 — Syllabus-aligned module and unit index

**Primary reference:** [AZ-900 Badge Links Reference](../AZ-900-BADGE-LINKS-REFERENCE.md)

This index follows the unit titles and order in the Badge Links reference. The files currently present in the repository do **not yet fully match that syllabus**. Where a lesson is absent or the existing lesson only partially matches, this index says so rather than pretending that the unit is complete.

The module and unit numbering here follows the supplied Badge Links notes. Microsoft Learn's current learning path may have updated titles or a different unit count; the reference document flags entries that need verification.

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
| 6 | Describe AI, machine learning, and IoT/Edge services in Azure | [New dedicated lesson](module-2/unit-6-ai-machine-learning-iot-edge.md) |
| 7 | Describe application hosting options | [Aligned lesson](module-2/unit-7.md), expanded beyond App Service |

The former Unit 7 lesson on Virtual Machine Scale Sets and Availability Sets has been preserved as [supplementary content](supplementary/virtual-machine-scale-sets-and-availability-sets.md). The old `unit-6.md` path is now a pointer to the canonical Virtual Desktop Unit 3 lesson, to reduce confusion from the previous numbering.

## Module 3 — Describe Azure networking services

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | **Missing dedicated introduction** |
| 2 | Create, configure, and manage users | **Placement/title needs verification**; this appears under networking in the supplied notes but may belong to another topic |
| 3 | Describe Azure virtual private networks | [VNet and subnet lesson](module-3/unit-1.md) is relevant but needs remapping and title review |
| 4 | Describe Azure ExpressRoute | [Covered in the combined DNS/VPN/ExpressRoute lesson](module-3/unit-2.md); create a dedicated unit or split the lesson |
| 5 | Describe Azure DNS | [Covered in the combined DNS/VPN/ExpressRoute lesson](module-3/unit-2.md); create a dedicated unit or split the lesson |

The existing [Public and Private Endpoints lesson](module-3/unit-3.md) is useful for current AZ-900 scope, but it is not one of the five units in the Badge Links reference. Keep it as supplementary content or map it to a verified current objective without changing the reference list.

## Module 4 — Describe Azure storage services

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | **Missing dedicated introduction** |
| 2 | Describe Azure storage accounts | Covered within [the combined storage lesson](module-4/unit-1.md); split into its own lesson |
| 3 | Describe Azure storage redundancy | Covered within [the combined storage lesson](module-4/unit-1.md); split into its own lesson |
| 4 | Describe Azure storage services | Covered within [the combined storage lesson](module-4/unit-1.md); split into its own lesson |
| 5 | Identify Azure data migration options | Covered within [the combined storage lesson](module-4/unit-1.md); split into its own lesson |
| 6 | Identify Azure file movement options | Covered within [the combined storage lesson](module-4/unit-1.md); split into its own lesson |

## Module 5 — Describe Azure identity, access, and security

| Unit | Reference title | Current lesson / status |
|---|---|---|
| 1 | Introduction | **Missing dedicated introduction** |
| 2 | Describe Azure directory services | Partially covered in [current identity lesson](module-5/unit-1.md); split and relabel |
| 3 | Describe Azure authentication methods | Partially covered in [current identity lesson](module-5/unit-1.md); split and relabel |
| 4 | Describe Azure external identities | Partially covered in [current identity lesson](module-5/unit-1.md); split and relabel |
| 5 | Describe Azure conditional access | Partially covered in [current identity lesson](module-5/unit-1.md); split and relabel |
| 6 | Describe Azure role-based access control | Partially covered in [current identity lesson](module-5/unit-1.md); split and relabel |
| 7 | Describe Zero Trust model | Covered in [current security lesson](module-5/unit-2.md); split and relabel |
| 8 | Describe defense-in-depth | Covered in [current security lesson](module-5/unit-2.md); split and relabel |
| 9 | Describe encryption and key management in Azure | Covered in [current security lesson](module-5/unit-2.md); split and relabel |
| 10 | Describe Microsoft Defender for Cloud | Covered in [current security lesson](module-5/unit-2.md); split and relabel |

## Correction plan

1. Preserve the Badge Links reference as the syllabus structure.
2. Split combined lessons where a reference unit needs its own lesson.
3. Move and relabel existing lessons only when their content matches the target unit.
4. Preserve useful extra AZ-900 topics as supplementary lessons rather than replacing reference units.
5. Verify the questionable “Create, configure, and manage users” entry against current Microsoft Learn before assigning it to a module.
6. Audit all lesson content against the [official AZ-900 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900), which is the authority for current exam objectives.

**Current status:** Module 2 has now been aligned to the reference order for Virtual Desktop (Unit 3), Containers (Unit 4), AI/ML/IoT/Edge (Unit 6), and application hosting (Unit 7). The VM Scale Sets and Availability Sets material is preserved as supplementary content. Other modules still need the same careful unit-by-unit split and alignment; do not treat this path as fully reconciled yet.
