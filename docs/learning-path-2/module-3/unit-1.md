# Learning Path 2 — Module 3, Unit 1: Azure Virtual Networks and Subnets

## Learning goals

By the end of this lesson, you should be able to:
- Explain what an Azure virtual network (VNet) does.
- Distinguish a VNet from a subnet.
- Explain private and public IP addresses at a basic level.
- Recognize why address ranges should not overlap when networks need to connect.
- Explain how network security groups (NSGs) help control traffic.

## 1. Why does Azure need networks?

Imagine GeekHub builds a school portal in Azure. The portal may have a web front end, application logic, and a database. These components need to communicate, but the school should not expose every component to the public internet.

A network gives resources a way to communicate and gives administrators a place to plan and control that communication.

## 2. What is an Azure virtual network (VNet)?

An **Azure virtual network (VNet)** is a logically isolated private network in Azure. Think of it as the school's private digital campus.

A VNet:
- provides a network space for supported Azure resources to communicate;
- has an IP address space that you choose;
- can be divided into subnets;
- can be connected to other networks when needed.

Resources in the same VNet can generally communicate using private IP addresses, subject to their configuration and security rules. Separate VNets are isolated by default; you need an explicit connection, such as VNet peering or a VPN, for them to communicate privately.

**Remember:** a VNet is a software-defined network, not one physical cable or one physical data centre.

## 3. What is a subnet?

A **subnet** is a smaller range of IP addresses inside a VNet. Subnets help organize resources by purpose and make it easier to apply network rules.

For our school portal, the network might be arranged like this:

```text
School-Portal-VNet
├── Web subnet       → web-facing components
├── App subnet       → application logic
└── Data subnet      → database-related components
```

This is a conceptual example, not a deployment blueprint. The exact Azure services and subnet requirements depend on the design.

The important distinction:
- **VNet:** the whole private network.
- **Subnet:** one segment within that network.

Subnets do not automatically block all traffic from one another. If you need to restrict communication, configure appropriate controls such as network security groups.

## 4. IP addresses: private versus public

An **IP address** identifies a network interface so that traffic can be directed to it.

- **Private IP address:** used for communication within a private network or connected networks. It is not directly reachable from the public internet just because it exists.
- **Public IP address:** can provide an internet-reachable address when associated with a supported Azure resource and configured appropriately. A public IP does not mean every port or service is automatically open; security and service configuration still matter.

A public-facing website might accept internet traffic through a public endpoint, while its database is reachable only through private networking.

## 5. Address spaces and overlap

When you create a VNet, you choose an address space. Subnets receive smaller address ranges from that space.

For example, imagine a VNet using the private range `10.20.0.0/16`, with separate smaller ranges for web, app, and data subnets. The exact CIDR notation is beyond what you need to calculate for this introductory AZ-900 lesson.

**Key rule:** subnets inside the same VNet must use non-overlapping address ranges. When connecting VNets or connecting Azure to an on-premises network, plan non-overlapping ranges so that routing can distinguish the networks correctly.

## 6. Network security groups (NSGs)

A **network security group (NSG)** contains rules that allow or deny network traffic. It can be associated with a subnet or a network interface.

Think of an NSG as a set of digital access rules:
- allow web traffic to the web tier when required;
- allow the application tier to reach the database on the required port;
- block traffic that should not be permitted.

An NSG is not the same thing as a VNet or subnet. The VNet provides the network, the subnet organizes the address space, and the NSG filters traffic. Good security depends on configuring rules appropriately.

## 7. VNet peering: connecting virtual networks

**VNet peering** privately connects two Azure virtual networks, including VNets in different Azure regions. Traffic can travel over Microsoft's backbone network.

Peering does **not** merge the two VNets into one. It creates a connection between them. Peering is not automatically transitive: if VNet A peers with VNet B, and VNet B peers with VNet C, that alone does not mean A can communicate with C through B.

## Exam-ready comparison

| Term | Meaning |
|---|---|
| Virtual network (VNet) | An isolated private network in Azure |
| Subnet | A smaller IP address range within a VNet |
| Private IP | An address for private network communication |
| Public IP | An address that can support internet-facing connectivity when configured |
| NSG | Rules that allow or deny network traffic |
| VNet peering | A private connection between two VNets |

## Quick knowledge check

Try answering before looking at the explanations.

1. A school wants to separate its web tier and database tier into different network segments. What should it create inside its VNet?
   - A. Two subscriptions
   - B. Two subnets
   - C. Two availability zones

2. What is the main purpose of a VNet?
   - A. To provide a logically isolated network for Azure resources
   - B. To automatically back up every database
   - C. To replace all identity and access controls

3. A team needs to control which network traffic can reach a subnet. Which service is most directly relevant?
   - A. Azure Cost Management
   - B. Network security group (NSG)
   - C. Azure Advisor

4. Two VNets are peered. Does that mean they have become one VNet, or that peering is automatically transitive to every other connected VNet?
   - A. Yes, both are true
   - B. No; peering connects the VNets but does not merge them and is not automatically transitive

### Answers and explanations

1. **B — Two subnets.** Subnets divide a VNet's address space into smaller segments for organization and traffic-control planning.
2. **A — A logically isolated network.** A VNet provides private network connectivity for supported resources.
3. **B — NSG.** NSGs use rules to allow or deny traffic to and from subnets or network interfaces.
4. **B — No.** Peering creates a private connection between the two VNets. It does not merge them, and peering through an intermediate VNet is not automatically transitive.

## Key takeaway

**VNet = the private network; subnet = a segment within it; NSG = traffic rules; peering = a private connection between VNets.**

## Official Microsoft Learn references

- [Virtual networks and virtual machines in Azure](https://learn.microsoft.com/en-us/azure/virtual-network/network-overview)
- [Azure virtual networks and subnets](https://learn.microsoft.com/en-us/azure/networking/design-guide/vnets-subnets)
- [Plan Azure virtual networks](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-nsg)

These notes are an original study aid for AZ-900 preparation, not official exam questions or a substitute for the current Microsoft Learn study guide.
