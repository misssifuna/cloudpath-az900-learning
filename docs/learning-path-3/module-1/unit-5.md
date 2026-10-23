# Learning Path 3 — Module 1, Unit 5: Describe the purpose of tags

**Module:** Describe cost management in Azure  
**Learning goal:** Explain how resource tags help categorize Azure resources and support cost reporting.

## 5. Resource tags

An Azure **tag** is a name-value pair attached to a supported resource to add organizational metadata.

Examples:

| Tag name (key) | Tag value | Why it helps |
|---|---|---|
| Environment | Development | Separate test from production costs |
| Department | IT | Identify the team responsible |
| Project | SchoolWebsite | Group project-related resources |
| Owner | GeekHub | Help identify who should review a resource |

Tags can help filter and group costs in Cost Analysis and support governance processes.

### Important limitations

- Tags are metadata; they do not themselves grant or deny access.
- Tags are not a replacement for resource groups, subscriptions, or RBAC.
- Not every resource or charge supports tags in the same way.
- Tag-based cost reporting applies according to the service's support and usage-data rules; don't assume every historic charge is retagged automatically.
- **Never put passwords, access tokens, personal information, or other secrets in tags.** Tags can appear in reports, logs, templates, and other outputs.

## Quick knowledge check
**Can a tag itself reduce a resource's cost?**

**Answer:** No. Tags add metadata for organization and reporting; optimization decisions may reduce costs.

## Official learning resource
[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
