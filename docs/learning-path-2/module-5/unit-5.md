# Learning Path 2 — Module 5, Unit 5: Describe Azure conditional access

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Explain how Conditional Access evaluates sign-in context and applies access decisions.

## 7. Conditional Access

**Microsoft Entra Conditional Access** uses signals about a sign-in to decide whether access should be allowed, blocked, or allowed only after additional requirements are met.

Policies can consider signals such as:
- Which user or group is signing in.
- Which application or resource is being accessed.
- Location or sign-in risk, where supported and configured.
- Device state or compliance, where supported and configured.

**Example:** A school might require administrators to complete MFA before accessing Azure management tools. A policy could also block certain sign-ins or require a compliant device, depending on the organization's configuration and licensing.

Think of Conditional Access as an **if-this-sign-in-context, then-apply-these-access-controls** system. It is not simply a list of users and passwords.

## Quick knowledge check
**Is Conditional Access the same as assigning permissions to a resource?**

**Answer:** No. Conditional Access evaluates access conditions at sign-in; Azure RBAC grants resource permissions.

## Official learning resource
[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
