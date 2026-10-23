# Learning Path 2 — Module 3, Unit 4: Describe Azure ExpressRoute

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure networking services  
**Learning goal:** Explain the purpose of ExpressRoute and distinguish private connectivity from a VPN connection over the internet.

## 3. Azure ExpressRoute: private connectivity

**Azure ExpressRoute** extends an on-premises network into the Microsoft cloud through a private connection facilitated by a connectivity provider. Its traffic does not traverse the public internet.

Organizations may consider ExpressRoute when they require private connectivity, high-capacity data transfer, or predictable network performance for important workloads. It generally involves additional cost and provider setup compared with a VPN.

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
**What is a key distinction of ExpressRoute?**

**Answer:** It provides private connectivity to Microsoft cloud services through a connectivity provider rather than relying on a VPN tunnel over the public internet.

## Official learning resource
[Describe Azure networking services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-networking/)
