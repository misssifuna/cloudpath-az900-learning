# Module 1 · Unit 4: Define cloud models

**Learning path:** Introduction to Cloud Infrastructure: Describe cloud concepts  
**Purpose:** Explain public, private, and hybrid cloud models.  
**Estimated time:** 5–7 minutes

## 4.1 Return to the school’s technology choices

Imagine the school has a student-record system. In Unit 2, we compared a server located on the school premises with using cloud services. In Unit 3, we learned that responsibilities are divided between the cloud provider and the customer.

Now consider a different question: **Who can use the cloud infrastructure, and how is it made available?**

Cloud deployment models help answer that question. The three core models in this lesson are public cloud, private cloud, and hybrid cloud.

## 4.2 Public cloud

In a **public cloud**, cloud services are provided by a third-party provider over a network. The provider's infrastructure supports services for multiple customers, with logical separation and access controls designed to keep each customer's resources and data separate.

Imagine the school subscribes to a student-management service hosted by a cloud provider. The school uses the service without owning the physical servers in the provider's data centre.

Key points:
- The provider owns or operates the underlying cloud infrastructure.
- Infrastructure is made available to multiple customers.
- Customers use and configure the services they subscribe to.
- Public cloud does **not** mean that every customer's data is publicly visible.

Examples of public cloud providers include Microsoft Azure, Amazon Web Services (AWS), and Google Cloud.

## 4.3 Private cloud

A **private cloud** is a cloud environment dedicated to a single organization. It may be hosted in the organization's own data centre or by a third-party provider.

Imagine a large education organization operates a private cloud environment dedicated to its own schools and departments. The environment is not shared as a cloud infrastructure environment with unrelated customers, though it may still use external support or hosting.

Key points:
- The environment is dedicated to one organization.
- The organization may have more control over how the environment is configured.
- It still requires management, security, and funding.
- Private cloud does not automatically mean that the organization operates everything itself or that it is always more secure.

A server sitting in a school computer room is **not automatically a private cloud**. It is simply an on-premises server unless it is part of a cloud environment that provides cloud-like capabilities.

## 4.4 Hybrid cloud

A **hybrid cloud** combines a private cloud with public cloud services, allowing data or applications to work across the two environments as needed.

Imagine the education organization keeps a particular system in its dedicated private environment but uses public cloud services for a website or to handle additional demand during a busy enrolment period. If those environments are integrated to work together, the organization is using a hybrid cloud approach.

Key points:
- It combines private and public cloud environments.
- It can let an organization keep some workloads in one environment while using services in another.
- It requires planning for integration, security, access, and data movement.
- Simply having one unrelated on-premises server and one public cloud account does not necessarily create a meaningful hybrid cloud; the environments need to be connected or integrated as part of the solution.

## 4.5 Compare the three models

| Model | Who can use the environment? | Simple description |
|---|---|---|
| **Public cloud** | Multiple customers use services on provider infrastructure, with separation between their resources | Provider-operated cloud services used by many customers |
| **Private cloud** | One organization has a dedicated cloud environment | Cloud environment dedicated to one organization |
| **Hybrid cloud** | One organization integrates private and public cloud environments | A connected combination of private and public cloud |

## 4.6 How should an organization choose?

The right model depends on its needs, not on one model being universally best.

- Consider a **public cloud** when the organization wants to use provider-operated services and scale resources as needed.
- Consider a **private cloud** when the organization needs a dedicated environment and has reasons and resources to support it.
- Consider a **hybrid cloud** when some workloads need to remain in a private environment while other workloads benefit from public cloud services.

Organizations should also consider cost, security requirements, compliance, existing systems, staff skills, and the work required to connect and manage environments.

## 4.7 Check your understanding

**Question 1.** A school subscribes to a service hosted on Microsoft Azure, using infrastructure that supports many customers with appropriate separation. Which model is this?

A. Public cloud.  
B. Private cloud.  
C. On-premises only.

**Correct answer: A.** Public cloud services are provided on provider-operated infrastructure used by multiple customers.

**Question 2.** What best describes a private cloud?

A. Any computer that is password-protected.  
B. A cloud environment dedicated to one organization.  
C. A public website that anyone can visit.

**Correct answer: B.** A private cloud is dedicated to one organization. A single on-premises server alone is not automatically a private cloud.

**Question 3.** An organization integrates its dedicated private cloud with services in a public cloud. Which model does this describe?

A. Public cloud only.  
B. Private cloud only.  
C. Hybrid cloud.

**Correct answer: C.** Hybrid cloud combines integrated private and public cloud environments.

**Question 4.** Does “public cloud” mean all customer data is publicly accessible?

A. Yes, all data is visible to everyone.  
B. No, customers' resources and data are logically separated and access is controlled.  
C. Yes, but only during business hours.

**Correct answer: B.** Public describes the service model, not public access to customer data.

**Question 5.** A school has one on-premises server and an unrelated cloud subscription. Is that automatically a hybrid cloud?

**Suggested answer:** No. Hybrid cloud generally involves private and public cloud environments that are integrated to work together. A standalone on-premises server is not automatically a private cloud.

## Key takeaway

Public cloud services are provided on infrastructure used by multiple customers; a private cloud is dedicated to one organization; and a hybrid cloud integrates private and public cloud environments. Choose the model based on requirements and trade-offs, not assumptions.

---
**Study note:** These are original learning questions, not copied exam questions. Use Microsoft's published AZ-900 learning objectives as the authority for exam scope.
