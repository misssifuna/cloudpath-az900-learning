# Module 1 · Unit 3: Describe the shared responsibility model

**Learning path:** Introduction to Cloud Infrastructure: Describe cloud concepts  
**Purpose:** Explain how cloud responsibilities are divided between the provider and customer.  
**Estimated time:** 5–7 minutes

## 3.1 Return to the school's student-record system

In Unit 2, we compared a school operating its own physical server with using a cloud provider.

Now imagine the school chooses a cloud service for its student records. The provider runs the underlying infrastructure, but the school still decides who should access the records and how staff use the system.

Who is responsible for keeping the whole arrangement secure?

The answer is that responsibility is **shared**. The cloud provider and the customer each have duties. The exact division depends on which cloud service the school chooses.

## 3.2 What is the shared responsibility model?

The **shared responsibility model** describes how security and management responsibilities are divided between a cloud provider and its customer.

The provider is responsible for some parts of the cloud service. The customer is responsible for other parts. Some responsibilities can involve both parties, each handling different aspects.

Moving to the cloud does not transfer every responsibility to the provider.

## 3.3 What does the cloud provider manage?

For a typical cloud service, the provider manages the physical infrastructure that supports the service. Depending on the service, this can include:

- Physical data-centre buildings and facilities.
- Physical servers and storage equipment.
- Physical networking equipment.
- The physical security of the provider's data centres.
- Other underlying layers included in the provider's service agreement.

For example, if the school uses a cloud-hosted service, it normally does not need to enter the provider's data centre to repair a failed physical server. The provider manages that physical infrastructure.

## 3.4 What does the school still manage?

The school remains responsible for the tasks assigned to it. These commonly include:

- Deciding which staff members should have accounts and access.
- Protecting passwords and authentication methods.
- Assigning appropriate permissions to users.
- Handling student information carefully.
- Configuring the parts of the service the school controls.
- Following relevant laws, policies, and the school's own procedures.

For example, the cloud provider cannot automatically know that a particular teacher has changed roles and should no longer have access to certain records. The school must manage user access appropriately.

## 3.5 The responsibility changes with the service type

Consider three broad ways the school could use technology. These are simplified examples; the precise responsibilities depend on the service and its configuration.

| Service approach | Provider generally manages | Customer generally manages |
|---|---|---|
| **On-premises server** | Only the work explicitly contracted to an external IT provider, if any | Most of the physical equipment and software responsibilities, plus users and data |
| **Infrastructure as a Service (IaaS)** | Physical data centre, physical servers, storage, networking, and virtualization layer | Operating system configuration and updates, applications, data, identities, and access |
| **Platform as a Service (PaaS)** | Physical infrastructure and more of the platform, such as the operating environment managed by the service | Applications, data, identities, access, and customer-controlled settings |
| **Software as a Service (SaaS)** | Most of the application platform and underlying infrastructure | Users, access, data handling, and customer-controlled settings |

The important pattern is that the provider generally manages more of the underlying technology as you move from IaaS to PaaS to SaaS. The customer still has responsibilities, especially around identities, access, and data.

## 3.6 A simple way to remember it

Imagine the school rents a secure digital record service.

- The provider is responsible for operating and protecting the infrastructure that it supplies.
- The school is responsible for using the service properly, including managing staff access and protecting the information it controls.
- Both must fulfil their own responsibilities for the overall arrangement to be secure.

Neither party can assume the other is handling every task.

## 3.7 Check your understanding

**Question 1.** What does the shared responsibility model describe?

A. The school and provider share one password.  
B. How responsibilities are divided between the cloud provider and customer.  
C. A rule that the provider is responsible for everything.

**Correct answer: B.** Each party has responsibilities, and the division depends on the service.

**Question 2.** In a typical cloud service, who is responsible for the physical security of the provider's data centre?

A. The cloud provider.  
B. Every student at the school.  
C. The school receptionist.

**Correct answer: A.** The provider manages the physical facilities it operates.

**Question 3.** The school needs to remove a staff member's access after that person leaves. Who should manage the school's user access?

A. The school, using the access controls available in the service.  
B. The provider must know automatically whenever staff leave.  
C. No one; cloud services remove access needs.

**Correct answer: A.** The school is responsible for managing its users and permissions.

**Question 4.** Which statement is generally true when moving from IaaS to PaaS to SaaS?

A. The customer always manages every layer.  
B. The provider generally manages more of the underlying technology.  
C. The customer no longer has any responsibilities.

**Correct answer: B.** More of the technology stack is managed by the provider as the service becomes more managed.

**Question 5.** Does using a cloud provider mean the school no longer needs to protect student information?

**Suggested answer:** No. The provider manages certain infrastructure and service responsibilities, but the school must still manage its own access, data handling, and other customer responsibilities.

## Key takeaway

The shared responsibility model helps clarify who must manage and protect each part of a cloud arrangement. The provider manages the parts of the service it supplies; the customer remains accountable for the responsibilities it controls. Always consider the specific service rather than assuming that all cloud services divide responsibilities in exactly the same way.

---
**Study note:** These are original learning questions, not copied exam questions. Use Microsoft's published AZ-900 learning objectives as the authority for exam scope.
