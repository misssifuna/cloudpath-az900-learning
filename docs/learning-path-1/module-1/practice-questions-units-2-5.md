# Module 1 — Unit Practice Questions

These are original learning questions, not copied from the AZ-900 exam. Try each question before reading its explanation.

## Unit 2 — Introduction to cloud computing
### Q2.1 — Knowledge check
**Which statement best defines cloud computing?**
- A. Connecting a computer to Wi-Fi
- B. Using computing services delivered over a network, usually the internet
- C. Keeping all data on a physical server in the school office

**Answer: B.** Cloud computing delivers computing services over a network. Wi-Fi is a connection method, not cloud computing itself.

### Q2.2 — Scenario
**The school buys a physical server, installs it in its office, and asks its IT technician to maintain it. What is this?**
- A. On-premises infrastructure
- B. Public cloud
- C. Hybrid cloud automatically

**Answer: A.** The server is located on the school's premises. It is not automatically a cloud environment.

### Q2.3 — Apply the concept
**The school wants to use a provider's database service rather than operate its own database server. What cloud idea does this illustrate?**

**Suggested answer:** Using a computing service supplied by a cloud provider instead of owning and operating all the underlying physical infrastructure.

## Unit 3 — Shared responsibility model
### Q3.1 — Knowledge check
**Who is generally responsible for the physical security of the cloud provider's data centre?**
- A. The cloud provider
- B. Every customer individually
- C. The school librarian

**Answer: A.** The provider manages the physical facilities it operates.

### Q3.2 — Scenario
**A teacher leaves the school, but their account still has access to student records. Which responsibility needs attention?**
- A. The school's user and access management
- B. The provider's building maintenance
- C. The public cloud deployment model

**Answer: A.** The school must manage user access and permissions appropriate to its service.

### Q3.3 — Compare
**As you move from IaaS to PaaS to SaaS, what generally happens to provider responsibilities?**
- A. They disappear
- B. The provider manages more of the underlying technology stack
- C. The customer becomes responsible for the data centre

**Answer: B.** More underlying layers are managed by the provider in more fully managed service types.

## Unit 4 — Cloud models
### Q4.1 — Knowledge check
**A school uses a provider's cloud infrastructure that serves multiple customers with appropriate data separation. Which model is this?**
- A. Public cloud
- B. Private cloud
- C. On-premises only

**Answer: A.** Public cloud supports multiple customers; it does not mean their data is publicly accessible.

### Q4.2 — Scenario
**An education organization operates a cloud environment dedicated to its own organization. Which model fits?**
- A. Public cloud
- B. Private cloud
- C. Hybrid cloud in every case

**Answer: B.** A private cloud environment is dedicated to one organization.

### Q4.3 — Scenario
**An organization integrates a private cloud with public cloud services so workloads can use both. What is this?**
- A. Hybrid cloud
- B. Private cloud only
- C. An on-premises server by itself

**Answer: A.** Hybrid cloud integrates private and public cloud environments.

## Unit 5 — Consumption model and Azure hierarchy
### Q5.1 — Knowledge check
**What does the consumption-based model mean?**
- A. All cloud services are free
- B. Charges may depend on measured usage and service pricing rules
- C. Customers must buy physical servers upfront

**Answer: B.** Usage is measured and billed according to the specific service's pricing rules.

### Q5.2 — Match the hierarchy
Match each Azure concept to its main purpose:
- **Management group:** organizes subscriptions and supports governance.
- **Subscription:** organizes resource deployment and provides a common management/cost scope.
- **Resource group:** groups related resources.
- **Resource:** an individual item such as a virtual machine or storage account.

### Q5.3 — Scenario
**The school groups a virtual machine and storage account in a resource group. What is the group?**
- A. A resource group
- B. A management group
- C. An invoice

**Answer: A.** A resource group is a logical container for related resources.

### Q5.4 — Cost reasoning
A practice scenario uses hypothetical prices:
- Virtual machine: 3 hours × KSh 10/hour = KSh 30
- Storage: 5 GB-month × KSh 2/GB-month = KSh 10
- Data transfer: 2 GB × KSh 3/GB = KSh 6

**What is the total illustrative cost?**
- A. KSh 40
- B. KSh 46
- C. KSh 56

**Answer: B.** KSh 30 + KSh 10 + KSh 6 = KSh 46. These are invented rates for arithmetic practice, not actual Azure prices.

### Q5.5 — Troubleshooting
**The learner opens Cost Analysis immediately after creating a resource, but no cost is shown. Does this prove Azure is broken?**

**Suggested answer:** No. Usage data may take time to appear, there may not yet be billable usage, or the learner may lack the required permissions or billing scope. Check the scope, permissions, date range, and later usage data.

### Q5.6 — Safety and cleanup
**After a lab, the learner deletes a virtual machine but leaves its disk and other resources behind. Is the environment guaranteed to have zero cost?**

**Answer: No.** Associated resources may continue to incur charges. Review and remove unneeded lab resources. Deletion does not erase charges already accrued.

## Suggested scoring
Award one point for each multiple-choice question and up to two points for open-ended or matching questions. For incorrect answers, revisit the related unit and flashcard rather than memorizing the answer letter.
