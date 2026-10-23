# Learning Path 2 — Module 5, Unit 8: Describe defense-in-depth

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure identity, access, and security  
**Learning goal:** Explain why security controls are layered across different parts of a system.

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

## Quick knowledge check
**Why use defense in depth?**

**Answer:** Multiple layers reduce reliance on any single control; if one fails, other controls may still limit harm.

## Official learning resource
[Describe Azure identity, access, and security — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/)
