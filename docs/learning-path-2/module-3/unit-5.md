# Learning Path 2 — Module 3, Unit 5: Describe Azure DNS

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure networking services  
**Learning goal:** Explain how Azure DNS hosts DNS domains and supports name resolution.

## 1. Azure DNS: finding services by name

Imagine a school has a portal at a memorable domain name. People use names more easily than numerical IP addresses. The Domain Name System (DNS) resolves a domain name to the records needed to locate a service.

**Azure DNS** lets organizations host and manage DNS domains and records using Azure infrastructure. It provides DNS hosting and resolution; it does not itself host your website or supply the network path to it.

Azure DNS capabilities include:

- **Azure Public DNS:** hosts DNS zones for publicly resolvable domain names.
- **Azure Private DNS:** manages and resolves DNS names for private resources in virtual networks.
- **Azure DNS Private Resolver:** enables DNS queries between Azure and on-premises environments without requiring you to deploy your own DNS server virtual machines for that purpose.

**Remember:** DNS resolves names; it is not the website itself.

## Quick knowledge check
**What does DNS do?**

**Answer:** It translates domain names into the records or addresses clients use to locate services.

## Official learning resource
[Describe Azure networking services — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-networking/)
