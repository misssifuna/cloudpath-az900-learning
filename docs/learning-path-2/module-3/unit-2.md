# Learning Path 2 — Module 3, Unit 2: Azure DNS, VPN Gateway, and ExpressRoute

## Learning goals

By the end of this lesson, you should be able to:
- Explain what DNS does and what Azure DNS provides.
- Distinguish Azure public DNS from Azure Private DNS at a basic level.
- Explain how Azure VPN Gateway supports encrypted connectivity.
- Distinguish site-to-site and point-to-site VPN connections.
- Compare VPN Gateway with ExpressRoute.

## 1. Azure DNS: finding services by name

Imagine a school has a portal at a memorable domain name. People use names more easily than numerical IP addresses. The Domain Name System (DNS) resolves a domain name to the records needed to locate a service.

**Azure DNS** lets organizations host and manage DNS domains and records using Azure infrastructure. It provides DNS hosting and resolution; it does not itself host your website or supply the network path to it.

Azure DNS capabilities include:

- **Azure Public DNS:** hosts DNS zones for publicly resolvable domain names.
- **Azure Private DNS:** manages and resolves DNS names for private resources in virtual networks.
- **Azure DNS Private Resolver:** enables DNS queries between Azure and on-premises environments without requiring you to deploy your own DNS server virtual machines for that purpose.

**Remember:** DNS resolves names; it is not the website itself.

## 2. Azure VPN Gateway: an encrypted connection

A school may keep some systems in its physical office while hosting other services in Azure. Its office network needs a secure way to connect to its Azure virtual network.

**Azure VPN Gateway** establishes VPN connections that use encryption over the public internet. It can connect on-premises networks to Azure VNets and can support connections between VNets.

Two common connection types:

- **Site-to-site VPN:** connects an on-premises network to an Azure VNet.
- **Point-to-site VPN:** connects an individual device, such as an authorized employee's laptop, to an Azure VNet.

A VPN can be a cost-effective way to provide encrypted connectivity. However, VPN traffic still traverses the public internet. Encryption protects the traffic; it does not mean the public internet is no longer involved.

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

## 5. Putting the services together

For a school modernizing its IT:

- **Azure DNS** manages domain-name resolution for the portal.
- An IT administrator can use a **point-to-site VPN** to connect an authorized laptop to the Azure network.
- The school could evaluate **ExpressRoute** if it later needs a private provider-facilitated connection from its campus network to Azure.

These services solve different problems: name resolution, encrypted connectivity, and private connectivity.

## Quick knowledge check

1. Which service manages DNS zones and records in Azure?
   - A. Azure DNS
   - B. Azure VPN Gateway
   - C. ExpressRoute

2. An IT administrator needs to connect an individual laptop securely to an Azure VNet. Which VPN connection type fits?
   - A. Site-to-site
   - B. Point-to-site
   - C. ExpressRoute

3. Which statement about a typical Azure VPN Gateway connection is correct?
   - A. It uses an encrypted VPN connection over the public internet.
   - B. Its traffic never traverses the public internet.
   - C. It translates every domain name into a website.

4. An organization requires a private connection to Microsoft cloud that does not traverse the public internet. Which service is the best match?
   - A. Azure DNS
   - B. VPN Gateway
   - C. ExpressRoute

### Answers and explanations

1. **A — Azure DNS.** It hosts and manages DNS zones and records.
2. **B — Point-to-site.** This connects an individual device to an Azure VNet.
3. **A — Encrypted VPN over the public internet.** Encryption does not remove the public internet from the route.
4. **C — ExpressRoute.** It provides private connectivity through a connectivity provider, without traffic traversing the public internet.

## Key takeaway

**Azure DNS = names; VPN Gateway = encrypted VPN connectivity over the internet; ExpressRoute = private connectivity that does not traverse the public internet.**

## Official Microsoft Learn references

- [Azure DNS documentation](https://learn.microsoft.com/en-us/azure/dns/)
- [Azure networking services overview](https://learn.microsoft.com/en-us/azure/networking/fundamentals/networking-overview)
- [Compare VPN Gateway and ExpressRoute](https://learn.microsoft.com/en-us/azure/networking/hybrid-connectivity/hybrid-connectivity)
- [Describe Azure networking services — AZ-900 learning module](https://learn.microsoft.com/en-us/training/modules/describe-azure-networking-services/)

These are original study notes for AZ-900 preparation, not official exam questions or a substitute for the current Microsoft Learn study guide.
