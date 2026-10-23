# Learning Path 2 — Module 5, Unit 2: Zero Trust, Defense in Depth, Encryption, and Defender for Cloud

**Learning Path 2 — Azure architecture and services**  
**Module 5 — Identity, access, and security**  
**Estimated study time:** 15–20 minutes

## Learning objectives

By the end of this lesson, you should be able to:

- Explain the Zero Trust security model.
- Describe defense in depth and why security controls are layered.
- Explain encryption at rest and in transit.
- Describe the purpose of Azure Key Vault.
- Explain what Microsoft Defender for Cloud helps organizations do.

## 1. Start with the security problem

Imagine GeekHub Solutions hosts a school website and stores documents in Azure. The site could face several risks: stolen passwords, an exposed network port, a misconfigured storage account, or a compromised application.

No single security measure can prevent every possible attack. Strong cloud security combines multiple controls, checks configuration continuously, and plans how to detect and respond when something goes wrong.

## 2. Zero Trust

Zero Trust is a security approach built around three central principles:

1. **Verify explicitly:** authenticate and evaluate relevant signals instead of trusting a request automatically.
2. **Use least privilege:** grant only the access needed, for only as long as needed where practical.
3. **Assume breach:** design systems to limit damage and support detection and recovery if an attacker gets in.

### Example

An administrator is working from the school office. A traditional “inside the office network means trusted” approach may grant broad access automatically. A Zero Trust approach still verifies the administrator's identity, checks relevant sign-in context, and applies appropriate permissions.

**Remember:** Zero Trust does not mean “trust nobody under any circumstances.” It means don't grant implicit trust simply because of location, device, or network.

## 3. Defense in depth

**Defense in depth** means using multiple layers of security so that if one control fails, other controls can still reduce the chance or impact of an attack.

A school website might use:

- **Identity layer:** MFA and least-privilege access.
- **Network layer:** network security groups and firewall rules.
- **Compute/application layer:** secure configuration, updates, and application protections.
- **Data layer:** access controls, backups, and encryption.
- **Monitoring layer:** logging, alerts, and security investigation.

For example, MFA cannot stop every attack. But if an attacker obtains a password, MFA may block the sign-in; network restrictions may reduce exposure; and monitoring may help identify suspicious activity.

Defense in depth is not the same as installing five copies of one tool. The layers should address different risks and complement one another.

## 4. Encryption: protecting information

Encryption transforms readable data into a form that cannot be understood without the appropriate cryptographic key.

### Encryption at rest

Protects stored data, such as files in a storage account or data on a disk. If the underlying storage media is accessed without authorization, encryption helps prevent the stored contents from being read directly.

### Encryption in transit

Protects data while it travels between systems, such as between a browser and a website. HTTPS uses TLS to protect the connection.

| Type | When it protects data | Example |
|---|---|---|
| Encryption at rest | While stored | School documents in Azure Storage |
| Encryption in transit | While moving across a connection | A teacher opens the school website over HTTPS |

Encryption is important, but it does not replace access control. An authorized user or compromised application may still access data after it has been decrypted for legitimate use.

## 5. Keys, secrets, and certificates

These terms are related but different:

- **Cryptographic key:** used by cryptographic operations, such as encrypting or decrypting data or creating/verifying signatures.
- **Secret:** sensitive information such as an API key, password, or connection string.
- **Certificate:** a digital credential that associates an identity with a public key and is commonly used with TLS.

Avoid placing credentials directly in source code or committing them to GitHub. If a secret is exposed, remove the exposure and rotate or revoke the credential as appropriate; deleting the visible line alone may not remove it from the repository's history.

## 6. Azure Key Vault

**Azure Key Vault** helps securely store and control access to secrets, cryptographic keys, and certificates.

For example, a GeekHub application may need a database connection secret. Rather than hard-coding that secret into the application source, the application can retrieve it from a suitably configured vault using an appropriate identity and permissions.

Good practices include:
- Restricting access using least privilege.
- Controlling network access where appropriate.
- Monitoring access and configuration.
- Rotating credentials and keys according to the organization's needs.
- Protecting recovery settings against accidental or malicious deletion.

Key Vault is not a general-purpose database for all application content. Its purpose is to protect and manage sensitive keys, secrets, and certificates.

## 7. Microsoft Defender for Cloud

**Microsoft Defender for Cloud** helps organizations improve their cloud security posture and protect workloads. It can provide security recommendations, help assess configurations against security standards, and offer threat-protection capabilities depending on enabled plans and supported resources.

Two useful ideas:

- **Security posture management:** find and prioritize weaknesses, such as insecure configurations.
- **Threat protection:** detect suspicious activity and threats affecting supported workloads.

Think of it as a security adviser and protection service for supported cloud resources—not a guarantee that an environment is completely secure.

A school administrator might use its recommendations to identify an exposed management port or a storage configuration that needs attention. Available features and costs depend on the selected plan and resource configuration.

## 8. Put the controls together

Consider this scenario: a school stores student documents in Azure Storage and runs a website.

1. Microsoft Entra ID helps authenticate staff.
2. Conditional Access can require MFA under configured conditions.
3. Azure RBAC limits which staff and applications can access the storage account.
4. Network controls restrict unnecessary connectivity.
5. Encryption helps protect stored data and data moving over secure connections.
6. Key Vault helps protect application secrets and cryptographic keys.
7. Defender for Cloud can help surface security recommendations and supported threat signals.
8. Logs, alerts, backup, and recovery procedures help the team investigate and respond to incidents.

No one control solves everything. The goal is to reduce the likelihood of compromise, limit damage, and improve detection and recovery.

## 9. Knowledge check

Try to answer before looking at the answer key.

1. Which Zero Trust principle means granting only the permissions required for a task?
2. A website uses MFA, network restrictions, encryption, and monitoring. What security approach does this illustrate?
3. A file is stored on a disk and protected using encryption. Is this encryption at rest or in transit?
4. Where should an application team consider storing API secrets instead of hard-coding them in source code?
5. What is a core purpose of Microsoft Defender for Cloud?

### Answer key

1. **Least privilege.**
2. **Defense in depth**, because several complementary security layers are in place.
3. **Encryption at rest.**
4. **Azure Key Vault**, with access configured for the application identity and appropriate permissions.
5. **Improving security posture and helping protect supported cloud workloads**, including security recommendations and threat-protection capabilities depending on configuration and plans.

## Key takeaways

- Zero Trust means verify explicitly, use least privilege, and assume breach.
- Defense in depth layers different security controls to reduce the chance or impact of an attack.
- Encryption at rest protects stored data; encryption in transit protects data while it moves.
- Azure Key Vault helps manage secrets, keys, and certificates securely.
- Microsoft Defender for Cloud helps assess cloud security posture and protect supported workloads.
- Security is a combination of prevention, detection, response, and recovery.

## Official Microsoft Learn resources

- [AZ-900 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
- [Describe Azure identity, access, and security](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
- [Azure security fundamentals](https://learn.microsoft.com/en-us/azure/security/fundamentals/)
- [Describe core infrastructure security services in Azure](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/)
- [Describe security management capabilities in Azure](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/)
