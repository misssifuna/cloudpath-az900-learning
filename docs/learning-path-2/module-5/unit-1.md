# Learning Path 2 — Module 5, Unit 1: Azure Identity, Authentication, and Authorization

**Learning Path 2 — Azure architecture and services**  
**Module 5 — Identity, access, and security**  
**Estimated study time:** 15–20 minutes

## Learning objectives

By the end of this lesson, you should be able to:

- Explain what Microsoft Entra ID does.
- Distinguish authentication from authorization.
- Describe single sign-on (SSO), multifactor authentication (MFA), and passwordless sign-in.
- Explain the purpose of Conditional Access.
- Describe Azure role-based access control (Azure RBAC) and least privilege.

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

## 3. Authentication vs. authorization

These terms sound similar but answer different questions.

| Term | Question answered | Example |
|---|---|---|
| **Authentication** | Who are you? | A teacher signs in using an account and verifies their identity. |
| **Authorization** | What are you allowed to access or change? | The teacher can view class materials but cannot change Azure network settings. |

A successful sign-in does **not** automatically mean a person can access every resource. Authentication verifies identity; authorization checks permissions.

## 4. Single sign-on (SSO)

**Single sign-on** lets a user authenticate once and then access multiple supported applications without having to sign in separately to each one, subject to the organization's security policies.

**Example:** A school staff member signs in and can then open several connected school applications.

SSO can reduce password fatigue and make access easier to manage. It does not mean that every application is automatically accessible, nor does it remove the need for authorization.

## 5. Multifactor authentication (MFA)

**MFA** requires two or more different types of proof to verify identity. Common factor categories are:

- **Something you know:** a password or PIN.
- **Something you have:** a registered phone, security key, or authenticator device.
- **Something you are:** a biometric such as a fingerprint or face match.

A password plus an additional verification step is a common MFA pattern. Two passwords are still both knowledge factors, so they are not two different factor types.

**Why it matters:** If an attacker steals a password, MFA can make it harder to sign in using that password alone. MFA reduces risk, but users still need to watch for phishing and never approve unexpected prompts.

## 6. Passwordless authentication

Passwordless methods let a user sign in without typing a conventional account password. Depending on the configuration, methods can include passkeys, FIDO2 security keys, or Windows Hello for Business.

Passwordless does not mean “no security.” The method still needs to verify the user, often using a device-bound credential, a PIN, or biometrics.

## 7. Conditional Access

**Microsoft Entra Conditional Access** uses signals about a sign-in to decide whether access should be allowed, blocked, or allowed only after additional requirements are met.

Policies can consider signals such as:
- Which user or group is signing in.
- Which application or resource is being accessed.
- Location or sign-in risk, where supported and configured.
- Device state or compliance, where supported and configured.

**Example:** A school might require administrators to complete MFA before accessing Azure management tools. A policy could also block certain sign-ins or require a compliant device, depending on the organization's configuration and licensing.

Think of Conditional Access as an **if-this-sign-in-context, then-apply-these-access-controls** system. It is not simply a list of users and passwords.

## 8. Azure role-based access control (Azure RBAC)

**Azure RBAC** manages who can perform which actions on Azure resources. A role assignment generally connects:

- **Security principal:** the user, group, service principal, or managed identity receiving access.
- **Role definition:** the permitted actions.
- **Scope:** where the permissions apply.

Azure RBAC scopes can include a management group, subscription, resource group, or individual resource. Permissions assigned at a broader scope can flow down to contained scopes.

Common built-in roles include:

- **Owner:** can manage resources and assign access.
- **Contributor:** can manage resources but cannot grant other users access through Azure RBAC.
- **Reader:** can view resources but not make changes to them.

The exact permissions depend on the role definition and scope. Use the **principle of least privilege**: give people only the access they need to perform their tasks, at the narrowest practical scope.

**Example:** A developer who deploys the school's website might need Contributor access to one app's resource group, but not Owner access to the whole subscription.

### Don't confuse Entra roles and Azure RBAC

- **Microsoft Entra roles** manage identity-directory tasks, such as managing users.
- **Azure RBAC roles** manage access to Azure resources, such as a storage account or virtual machine.

They solve related but different permission problems.

## 9. External identities and guest access

Organizations sometimes need to collaborate with people outside their organization—for example, an external auditor or a contractor. Microsoft Entra external identity capabilities can support that collaboration.

External access should be deliberately scoped. Invite only the people who need access, grant minimum permissions, and review access when the work ends.

## 10. Zero Trust and least privilege

The **Zero Trust** approach is commonly summarized as **verify explicitly, use least privilege, and assume breach**.

In practical terms:
- Do not trust a request only because it comes from inside an office network.
- Verify identity and evaluate relevant context.
- Limit permissions and privileged access.
- Monitor activity and plan for the possibility that a credential or device is compromised.

MFA, Conditional Access, RBAC, and access reviews can support this approach. No single control guarantees complete security.

## 11. Quick comparison

| Feature | Main purpose |
|---|---|
| Microsoft Entra ID | Manage identities and sign-in/access capabilities |
| Authentication | Verify who is signing in |
| Authorization | Determine permitted actions and resources |
| SSO | Make access to multiple supported apps easier after sign-in |
| MFA | Require multiple types of verification |
| Conditional Access | Apply access decisions based on sign-in signals and policy |
| Azure RBAC | Assign permissions for Azure resources at defined scopes |
| Zero Trust | Security approach that verifies explicitly and limits implicit trust |

## 12. Knowledge check

Try to answer before looking at the answer key.

1. A teacher signs in with a password and then confirms a prompt in an authenticator app. Which control is this?
2. A teacher can sign in successfully but cannot change the school's virtual network. Is this an authentication or authorization issue?
3. The IT administrator wants school administrators to use MFA when managing Azure. Which Microsoft Entra capability can apply that requirement based on sign-in conditions?
4. A developer only needs to manage resources in one project resource group. What access principle should guide the assignment, and what scope is likely more appropriate than the whole subscription?
5. Which is primarily for managing Azure resource permissions: Microsoft Entra ID alone, or Azure RBAC?

### Answer key

1. **MFA**, because the user provides more than one type of verification.
2. **Authorization**; sign-in succeeded, but the requested action is not permitted.
3. **Conditional Access**, configured to require MFA for the relevant users and resources.
4. **Least privilege**; grant the minimum suitable role at the project resource group scope, if that covers the required work.
5. **Azure RBAC** assigns roles for Azure resource actions and scopes. Microsoft Entra ID provides identity and access capabilities that work alongside it.

## Key takeaways

- Authentication asks **who are you?** Authorization asks **what can you do?**
- Microsoft Entra ID provides cloud identity and sign-in capabilities.
- SSO improves convenience; MFA adds verification; passwordless uses alternatives to conventional passwords.
- Conditional Access evaluates sign-in signals against policy.
- Azure RBAC grants resource permissions at a scope; least privilege limits unnecessary access.
- Zero Trust means verifying explicitly rather than trusting automatically.

## Official Microsoft Learn resources

- [AZ-900 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
- [Describe Azure identity, access, and security](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
- [Microsoft Entra Conditional Access documentation](https://learn.microsoft.com/en-us/entra/identity/conditional-access/)
