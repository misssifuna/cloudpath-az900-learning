# Learning Path 2 — Module 3, Unit 3: Public and Private Endpoints

## Learning goals

By the end of this lesson, you should be able to:
- Define a public endpoint and a private endpoint.
- Explain how Azure Private Link and private endpoints support private access to Azure services.
- Distinguish private endpoints from virtual network service endpoints.
- Identify the security misconception that a private endpoint automatically disables public access.

## 1. What is an endpoint?

An **endpoint** is a point through which a client or network connects to a service. For AZ-900, focus on the difference between a public endpoint and a private endpoint.

Imagine a school portal stores documents in Azure Storage. The school must decide how the application and authorized users will connect to that storage.

## 2. Public endpoints

A **public endpoint** uses a publicly reachable address for access to a service. Depending on the service and its configuration, clients may connect over the internet.

Public access does not necessarily mean that everybody is allowed to use the resource. Authentication, authorization, firewalls, and other network controls can still restrict access.

**Example:** a public website must be reachable by students on different networks. Its web endpoint is designed for public access, while sensitive backend services can remain private.

## 3. Private endpoints

An **Azure private endpoint** is a network interface with a private IP address in your virtual network. It connects privately to a specific Azure service resource using Azure Private Link.

For example, a school can create a private endpoint for its Azure Storage account. The application can connect to the storage resource using a private address rather than needing to reach that resource through its public endpoint.

Benefits include:
- private connectivity from a virtual network to supported Azure services;
- traffic to the service staying on the Microsoft network rather than traversing the public internet;
- access to a specific resource instance, which helps limit unintended access to other resources.

A private endpoint is not a replacement for identity permissions. The application and user still need the required authorization.

**Important security point:** creating a private endpoint does not, by itself, automatically disable public network access to the target resource. If the requirement is to permit access only through private paths, configure the target service's public network access and other access controls accordingly, then test the intended connections.

## 4. Private endpoint versus service endpoint

These terms sound similar but are different.

| Feature | Private endpoint | Virtual network service endpoint |
|---|---|---|
| What it provides | A private IP address in your VNet for a specific service resource | Extends VNet identity to a supported Azure service |
| Private IP for the service connection | Yes | No |
| Traffic path | Microsoft network; avoids the public internet for that private connection | Microsoft network backbone |
| Resource scope | Maps to a specific resource instance | Service access is controlled using supported virtual-network rules |
| Main memory aid | Private IP to a specific resource | VNet identity to a supported service |

For the AZ-900 level, remember that **a private endpoint provides a private IP address**. A service endpoint does not create a private IP address for the Azure service.

## 5. A practical school example

A school uses:
- a public website so students can find general information;
- an Azure Storage account for sensitive internal documents;
- a private endpoint so the application's VNet can connect privately to that storage account;
- identity permissions and service network settings to restrict who can access the documents.

This is a layered approach: private connectivity helps control the network path, while identity and access controls determine who is authorized.

## Quick knowledge check

1. What does an Azure private endpoint provide?
   - A. A private IP address in a VNet that connects to a specific supported service resource
   - B. A public website
   - C. An automatic backup of the service

2. Which statement is true about a public endpoint?
   - A. It always means everyone has permission to access the data.
   - B. It can provide public network connectivity, while authentication and network controls still restrict access.
   - C. It can only be reached from one Azure subnet.

3. Does creating a private endpoint automatically disable public network access to the target service?
   - A. Yes, always
   - B. No; configure the target service's public network access and other controls separately as needed.

4. Which statement distinguishes a private endpoint from a service endpoint?
   - A. Both always assign a private IP address to the service.
   - B. A private endpoint provides a private IP in the VNet; a service endpoint extends VNet identity to a supported service.
   - C. A service endpoint is a VPN connection to an office.

### Answers and explanations

1. **A.** A private endpoint is a network interface with a private IP in the VNet, associated with a supported service resource through Private Link.
2. **B.** Public network reachability does not mean unrestricted authorization.
3. **B.** Public network access settings and other controls must be configured deliberately.
4. **B.** Private endpoints provide private IP connectivity; service endpoints work differently and do not assign a private IP address to the service.

## Key takeaway

**Public endpoint = public network path; private endpoint = private IP connectivity to a specific supported resource.** Neither endpoint removes the need for appropriate identity, authorization, and network security configuration.

## Official Microsoft Learn references

- [AZ-900 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
- [Azure network foundation services overview](https://learn.microsoft.com/en-us/azure/networking/foundations/network-foundations-overview)
- [What is a private endpoint?](https://learn.microsoft.com/en-us/azure/private-link/private-endpoint-overview)
- [Private access to Azure PaaS services](https://learn.microsoft.com/en-us/azure/networking/design-guide/private-platform-as-a-service)

These are original study notes for AZ-900 preparation, not official exam questions or a substitute for the current Microsoft Learn study guide.
