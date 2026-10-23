# Learning Path 2 — Module 3, Unit 3: Describe Azure virtual private networks

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure networking services  
**Learning goal:** Explain how Azure VPN Gateway provides encrypted connectivity between Azure and other networks.

## 2. Azure VPN Gateway: an encrypted connection

A school may keep some systems in its physical office while hosting other services in Azure. Its office network needs a secure way to connect to its Azure virtual network.

**Azure VPN Gateway** establishes VPN connections that use encryption over the public internet. It can connect on-premises networks to Azure VNets and can support connections between VNets.

Two common connection types:

- **Site-to-site VPN:** connects an on-premises network to an Azure VNet.
- **Point-to-site VPN:** connects an individual device, such as an authorized employee's laptop, to an Azure VNet.

A VPN can be a cost-effective way to provide encrypted connectivity. However, VPN traffic still traverses the public internet. Encryption protects the traffic; it does not mean the public internet is no longer involved.

## 4. VPN Gateway versus ExpressRoute

| Feature | VPN Gateway | ExpressRoute |
|---|---|---|
| Connection | Encrypted VPN over the public internet | Private provider-facilitated connection |
| Does traffic traverse the public internet? | Yes | No |
| Typical consideration | Cost-effective encrypted connectivity | Private connectivity for demanding workloads |
| Setup | Often quicker | Provider circuit may take longer |
| Example | A school securely connects its office to Azure | A large institution privately connects its data centre to Azure |

### AZ-900 exam tip

- If a scenario emphasizes an **encrypted connection over the public internet**, consider **VPN Gateway**.
- If it emphasizes a **private connection that does not traverse the public internet**, consider **ExpressRoute**.

Choose based on the stated requirements; neither service is automatically the best choice for every organization.

## Quick knowledge check
**What does a VPN connection typically use to protect traffic over an untrusted network?**

**Answer:** Encryption through a VPN tunnel.

## Official learning resource
[Describe Azure networking services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-networking/)
