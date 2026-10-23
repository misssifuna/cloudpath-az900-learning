# Learning Path 2 — Module 5, Unit 9: Describe encryption and key management in Azure

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Explain encryption at rest and in transit, and recognize the purpose of keys, secrets, certificates, and Azure Key Vault.

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

## Quick knowledge check
**What is the purpose of encryption?**

**Answer:** It makes data unreadable without the appropriate decryption capability, helping protect data at rest or in transit.

## Official learning resource
[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
