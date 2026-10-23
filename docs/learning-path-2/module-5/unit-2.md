# Learning Path 2 — Module 5, Unit 2: Describe Azure directory services

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Describe Microsoft Entra ID and recognize Microsoft Entra Domain Services as a related directory capability.

## 1. Why identity matters in the cloud

Cloud resources can be reached from many places and devices. A firewall alone cannot tell whether the person signing in is a teacher, a school administrator, a GeekHub developer, or an attacker using stolen credentials.

Identity security helps answer two key questions:

1. **Who are you?**
2. **What are you allowed to do?**

Imagine Holy Trinity Boys Senior School stores student documents in Azure. Staff need to sign in, but not every staff member should be able to read payroll records or change the school's cloud configuration. Identity and access controls help make those distinctions.

## 2. Microsoft Entra ID

**Microsoft Entra ID** (formerly Azure Active Directory, or Azure AD) is Microsoft's cloud identity and access management service. It helps manage identities and control access to applications and resources.

An identity can represent a person, a group, or an application/workload that needs to access something.

Typical uses include:
- Signing in to Microsoft cloud services and integrated applications.
- Managing users and groups.
- Supporting SSO and MFA.
- Applying Conditional Access policies.
- Helping administrators control access to cloud resources.

**Important distinction:** Microsoft Entra ID is not the same thing as an Azure subscription. Entra ID handles identity and sign-in; an Azure subscription is a billing and resource-management boundary. Access to Azure resources can be assigned to identities through Azure RBAC.

## Microsoft Entra ID and Microsoft Entra Domain Services

**Microsoft Entra ID** is Microsoft's cloud identity and access management service. It supports identities, sign-in, application access, and identity-related security controls for cloud and connected resources.

**Microsoft Entra Domain Services** provides managed domain services such as domain join, LDAP, Kerberos, and NTLM for compatible workloads. It can help applications that depend on traditional domain capabilities without requiring an organization to manage domain controllers itself.

Do not treat these services as identical: Entra ID is the cloud identity service; Entra Domain Services supplies selected managed domain capabilities for workloads that need them.

## Quick knowledge check

**Which service is the primary cloud identity and access management service?**

**Answer:** Microsoft Entra ID.

## Official learning resource

[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
