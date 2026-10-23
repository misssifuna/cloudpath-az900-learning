# Learning Path 2 — Module 5, Unit 3: Describe Azure authentication methods

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Distinguish authentication from authorization and recognize SSO, MFA, and passwordless authentication.

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

## Quick knowledge check
**What does authentication establish?**

**Answer:** It verifies who is signing in. Authorization determines what that identity is allowed to do.

## Official learning resource
[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
