# CloudPath curriculum reconciliation status

**Repository:** [misssifuna/cloudpath-az900-learning](https://github.com/misssifuna/cloudpath-az900-learning)  
**Syllabus reference:** [AZ-900 Badge Links Reference](AZ-900-BADGE-LINKS-REFERENCE.md)  
**Exam-scope authority:** [Current Microsoft AZ-900 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)

## Agreed structure

- 3 learning paths
- 12 modules
- Learning Path 1, Module 1 intentionally uses **5 app units**, combining the overlapping introductory entries that remain separate in the source reference.
- The AI, machine learning, and IoT/Edge lesson has now been authored for Learning Path 2, Module 2, Unit 6.

## Current unit tally

Counting each listed syllabus unit as one, except for the intentional consolidation in Learning Path 1, Module 1:

| Learning path | Module unit counts used by CloudPath | Total |
|---|---:|---:|
| Path 1 — Describe cloud concepts | 5 + 6 + 4 | 15 |
| Path 2 — Describe Azure architecture and services | 5 + 7 + 5 + 6 + 10 | 33 |
| Path 3 — Describe Azure management and governance | 6 + 5 + 4 + 4 | 19 |
| **Calculated total** | **15 + 33 + 19** | **67** |

**Count discrepancy to resolve:** The intended project total was recalled as **61 or 62 units**, but the current Badge Links module lists produce **67 app units** after the known five-unit consolidation. That leaves a difference of **5–6 units**. No additional units have been silently removed to force the total to match. Before changing the curriculum count, identify which entries are intended to be merged, excluded, or treated as non-lesson navigation items.

## Work completed in this reconciliation

- Added module indexes for Learning Paths 1, 2, and 3.
- Added Learning Path 1 Module 2 and Module 3 lessons, which were not present as separate Markdown lesson files in the repository.
- Reordered compute lessons so Virtual Desktop is Unit 3, Containers Unit 4, AI/ML/IoT/Edge Unit 6, and application hosting Unit 7.
- Preserved Virtual Machine Scale Sets and Availability Sets as supplementary content rather than letting them replace application hosting.
- Split the combined storage lesson into six units and preserved the original combined lesson.
- Split the combined identity/security lessons into the ten reference-aligned units and preserved the original combined lessons.
- Split the combined networking notes into dedicated units and preserved the original combined notes.
- Split Learning Path 3's four combined lessons into dedicated unit files and preserved the original files under the learning-path-3 supplementary folder.
- Preserved public/private endpoints as supplementary AZ-900 material.
- Verified the questionable networking Unit 2 title against current Microsoft Learn. The supplied notes say “Create, configure, and manage users”; the current networking module says “Describe Azure virtual networking.” The source discrepancy is documented in the Badge Links reference and the CloudPath networking index.
- Preserved the source reference's original six entries for Learning Path 1, Module 1, while documenting the intentional five-unit app consolidation.

## Still required before calling the curriculum fully verified

1. Reconcile the **61/62 versus 67** unit-count discrepancy with the intended app counting convention.
2. Review each split lesson for accuracy and ensure the extraction has not left duplicated or missing material.
3. Markdown links in the root README, all three learning-path indexes, and this status document have been checked; no broken internal links were found. The app/prototype curriculum data still needs to be compared with these canonical Markdown indexes.
4. Recheck service names and exam coverage against the current Microsoft Learn study guide before release.

The unit indexes describe the intended learner-facing sequence. This status file deliberately does not claim that every lesson has completed a technical review.
