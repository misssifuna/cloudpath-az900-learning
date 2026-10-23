# Learning Path 2 — Module 5, Unit 3: Describe Azure authentication methods

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Distinguish authentication from authorization and recognize single sign-on, multifactor authentication, and passwordless authentication.

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

## Quick knowledge check

**What does authentication establish?**

**Answer:** It verifies who is signing in. Authorization determines what that identity is allowed to do.

## Official learning resource

[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
