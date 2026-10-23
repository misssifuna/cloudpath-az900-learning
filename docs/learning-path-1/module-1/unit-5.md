# Module 1 · Unit 5: Describe the consumption-based model

**Learning path:** Introduction to Cloud Infrastructure: Describe cloud concepts  
**Purpose:** Explain how cloud usage and costs are measured and charged.  
**Estimated time:** 7–9 minutes

> **Scope note:** This unit explains the consumption-based model and introduces the Azure organization hierarchy so the billing idea has a place to live. Management groups, subscriptions, resource groups, and detailed cost-management tools are explored further in later Azure architecture and governance lessons.

## 5.1 Return to the school

Imagine the school has moved its student-record system from its own on-premises server to cloud services.

With the old on-premises approach, the school might buy a server and pay for it upfront, then pay separately for electricity, support, and upgrades. The equipment cost is not necessarily tied directly to how many student records are viewed each day.

With cloud services, the school may instead pay according to the resources it uses and the pricing terms of the services it selects.

For example, its bill might be affected by:
- How long a virtual machine runs.
- How much data is stored and for how long.
- How much data is transferred out of a cloud service.
- Which service tier or performance level is selected.
- Whether the service has a fixed charge, a usage-based charge, or both.

The exact billing unit depends on the resource and its pricing arrangement.

## 5.2 What is the consumption-based model?

The **consumption-based model** means that charges are based on the amount of a cloud service or resource consumed, according to its pricing rules.

A simple mental model is:

**Amount charged = measured usage × applicable rate**, plus any other applicable charges, discounts, or taxes.

This is a simplified model, not a complete formula for every Azure service. Some services charge per second or hour, some per operation or unit of data, and others have fixed or tier-based pricing.

The important idea is that cloud usage can be measured, and that measurement can influence the bill.

## 5.3 Compare the two approaches

```text
SCHOOL-OWNED SERVER                         CLOUD SERVICE
┌────────────────────────┐                 ┌────────────────────────┐
│ Buy equipment upfront  │                 │ Choose a cloud service │
│                        │                 │                        │
│ Pay for power, support │                 │ Usage may be measured  │
│ and maintenance        │                 │ against pricing rules  │
│                        │                 │                        │
│ Upgrade when needed    │                 │ Adjust supported       │
│                        │                 │ resources as needed    │
└────────────────────────┘                 └────────────────────────┘
```

Cloud services can reduce the need to buy physical equipment upfront, but they are **not automatically cheaper**. Leaving resources running, choosing oversized resources, storing large amounts of data, or transferring lots of data can increase costs. The customer needs to monitor usage and choose suitable resources.

## 5.4 A simple usage example

Suppose a school uses a cloud virtual machine for an application. To keep the example simple, imagine the service charges a hypothetical **KSh 10 per running hour**.

| Running time | Illustrative charge |
|---|---:|
| 1 hour | KSh 10 |
| 10 hours | KSh 100 |
| 100 hours | KSh 1,000 |

These numbers are invented only to explain the arithmetic. They are **not actual Azure prices**. Real Azure prices depend on region, resource type, configuration, currency, agreements, and current rates. A virtual machine may also incur charges for associated disks, networking, or other resources. Stopping a virtual machine does not necessarily stop every associated charge.

## 5.5 How Azure organizes what you use

When working in Azure, you will see a hierarchy that helps organize resources and manage access, policy, and billing scopes.

```text
Microsoft Entra tenant / organization
             │
             ▼
      Management group
             │
             ▼
        Subscription  ◄──── Common billing and management scope
             │
             ▼
        Resource group
             │
       ┌─────┴─────┐
       ▼           ▼
   Resource      Resource
  (virtual       (storage
   machine)      account)
```

This is a simplified view. A tenant can have multiple management groups and subscriptions; subscriptions can contain multiple resource groups; resource groups contain resources. A subscription can also exist under the tenant without being placed in a management group other than the tenant's root management group.

### The parts of the hierarchy

**Management group**
- Organizes multiple subscriptions.
- Lets an organization apply supported governance settings, such as Azure Policy and role assignments, across subscriptions.
- Is not itself the virtual machine or database consuming compute or storage.

**Subscription**
- A boundary used to organize access, policies, quotas, and resource deployment.
- Commonly a key scope for tracking usage and charges.
- An organization can use separate subscriptions for different environments, teams, or workloads.
- The exact invoice and payment arrangement depends on the customer's Azure agreement and billing account.

**Resource group**
- A logical container for related Azure resources.
- Helps organize, deploy, monitor, and manage related resources together.
- Is not normally a separate billable service by itself; charges come from the resources and services in it.
- Resources in a resource group do not have to be in the same region, although the resource group has a location for its metadata.

**Resource**
- An individual Azure item you create or use, such as a virtual machine, storage account, database, or virtual network.
- Resources and their usage are what commonly generate the underlying charges.

## 5.6 Simulated Azure portal view

This is a **teaching simulation**, not a screenshot or live Azure account.

```text
┌─────────────────────────────────────────────────────────────┐
│ Microsoft Azure                                      Search │
├──────────────────┬──────────────────────────────────────────┤
│ Home             │ Resource groups                          │
│                  │                                          │
│ Management       │ Subscription: School-Production           │
│ groups           │                                          │
│ Subscriptions    │ ┌──────────────────────────────────────┐ │
│ Resource groups  │ │ rg-student-records                   │ │
│ All resources    │ │                                      │ │
│ Cost Management  │ │  vm-student-app       Virtual machine│ │
│                  │ │  ststudentfiles       Storage account│ │
│                  │ │  vnet-school          Virtual network│ │
│                  │ └──────────────────────────────────────┘ │
└──────────────────┴──────────────────────────────────────────┘
```

Read the simulated view from the top down:

1. **Subscription:** the subscription named `School-Production` groups this workload within an Azure subscription.
2. **Resource group:** `rg-student-records` groups related resources.
3. **Resources:** the virtual machine, storage account, and virtual network are individual Azure resources.
4. **Cost view:** Cost Management can help review charges at supported scopes, such as a billing account, subscription, resource group, or resource, depending on permissions and the available billing setup.

The names are illustrative. They do not represent a real Azure account.

## 5.7 Where does the bill come from?

Think of the school creating three resources:

```text
Subscription: School-Production
          │
          ▼
Resource group: rg-student-records
          │
          ├── Virtual machine ──► compute / running-time charges
          │
          ├── Storage account ──► capacity / operations / transfer
          │
          └── Virtual network ──► some networking features may incur charges
```

Not every resource is charged in the same way. Some features may have no direct charge, while associated services or data transfer can cost money. Always check the pricing details for the specific resource.

**Remember the distinction:**
- Management groups organize subscriptions.
- Subscriptions organize resources and are a common scope for reviewing usage and charges.
- Resource groups organize related resources.
- Individual resources and their usage generally generate the underlying service charges.

A subscription is not the same thing as a single resource, and a resource group is not a separate bill that automatically adds a fee just for existing.

## 5.8 Check your understanding

**Question 1.** What does the consumption-based model mean?

A. Every cloud service is always free.  
B. Charges can be based on measured usage according to the service's pricing rules.  
C. Customers must buy all physical servers upfront.

**Correct answer: B.** Cloud usage can be measured and billed according to applicable pricing rules.

**Question 2.** Which Azure item is the logical container for related resources?

A. Resource group.  
B. Keyboard.  
C. Internet browser.

**Correct answer: A.** Resource groups help organize related Azure resources.

**Question 3.** What is a management group mainly used for?

A. Storing a school's student records directly.  
B. Organizing subscriptions and applying governance across them.  
C. Measuring the electricity used by an on-premises server.

**Correct answer: B.** Management groups organize subscriptions for governance and management.

**Question 4.** Which item commonly generates the underlying Azure service charge?

A. A resource being used, such as a virtual machine or storage service.  
B. The name of a resource group by itself.  
C. A diagram of the subscription hierarchy.

**Correct answer: A.** Charges usually come from resources and their usage, not from the resource group's name.

**Question 5.** If a virtual machine is stopped, does that guarantee that the total cost becomes zero?

**Suggested answer:** No. Compute charges may stop or change depending on the VM state and billing rules, but associated storage, networking, reserved capacity, or other services may continue to incur charges.

**Question 6.** Why should a customer monitor cloud usage?

**Suggested answer:** To understand where charges come from, detect unexpected usage, adjust resources to match needs, and avoid unnecessary spending.

## 5.9 Practical lab: Explore an Azure subscription and follow the costs

**Mission:** Act as the school's junior cloud administrator. Identify the subscription available to your account, create a resource group, deploy a small resource only if you understand its possible charges, inspect cost information, and clean up what you created.

**Important cost and billing reality:** Azure account offers vary. A new account may receive an eligible free offer and a default subscription, but this is not guaranteed for every account. Some offers require payment details. Creating resources can incur charges, and the Cost Analysis view may take time to show usage. A bill or invoice may not be available immediately, particularly if no charge has accrued. Never create a costly resource just to force a bill. If this is a class exercise, follow your instructor's approved sandbox or subscription instructions.

### Before you start: safety checklist

- Use an account and subscription you are authorised to use.
- Check the offer, remaining credit, free-service limits, currency, and billing terms shown for your account.
- Do not enter a payment method unless you understand the terms and have permission to do so.
- Do not create a virtual machine for this exercise unless your instructor has approved it and you know how to stop and delete it.
- Set a budget or cost alert if the available subscription supports it; an alert is not necessarily a hard spending limit.
- Record the resource names you create so you can remove them afterwards.

### Step A — Sign in and identify your subscription

1. Open the [Azure portal](https://portal.azure.com/) and sign in. If you do not have an account, use Microsoft's official Azure account sign-up process and carefully review eligibility, payment, and offer terms before continuing.
2. In the portal search bar, search for **Subscriptions** and open it.
3. Look for the subscription available to your account. A new account may show a subscription such as **Azure subscription 1**, but names and offers vary.
4. Open the subscription and note its **subscription name**, **subscription ID** (do not share it publicly), **status**, and **offer or billing information** visible to you.
5. If the subscription list is empty or access is denied, stop and ask the instructor/account administrator to assign an approved subscription. Do not create another account to bypass access controls.

**Checkpoint:** Can you explain what a subscription is and why it matters for resource access and cost tracking?

### Step B — Create a resource group

A resource group is a logical container for related resources. Creating one alone is generally not the same as deploying a billable compute resource, although always follow the portal's current guidance.

1. In the portal, search for **Resource groups**.
2. Select **Create**.
3. Choose the subscription you identified in Step A.
4. Choose a region for the resource group's metadata.
5. Use a clear lab name, for example `rg-az900-school-lab`.
6. Review the settings and create the resource group.
7. Open it and confirm the subscription and region.

**Checkpoint:** The resource group belongs to a subscription, but it is not itself the virtual machine, database, or storage service that may generate usage charges.

### Step C — Understand the resource-creation screen before deploying anything

1. In the portal search bar, search for **Storage accounts** and open the creation page, but do not select **Review + create** until you have reviewed all settings and possible costs.
2. Observe the fields such as subscription, resource group, region, performance, redundancy, and other configuration options.
3. Notice how the selected subscription and resource group determine where the resource is organised.
4. Review the pricing and free-tier eligibility using the [Azure pricing page](https://azure.microsoft.com/pricing/) or the official pricing calculator before deploying.
5. If you do not have an instructor-approved subscription or are unsure about charges, **stop at the review screen**. You can complete the remainder using the simulated exercise below without deploying a resource.

If your instructor has approved deployment, create only the agreed low-cost resource, avoid uploading personal or school data, and record the creation time and configuration. Pricing and free allowances change; do not assume a resource is free merely because the portal offers a free tier.

### Step D — Inspect cost information

1. Search for **Cost Management + Billing** in the portal.
2. Open **Cost Management** or **Cost analysis**, if available for your account and permissions.
3. Select the relevant billing scope or subscription.
4. Review the available date range, cost amount, service/resource breakdown, and any forecast or budget information shown.
5. If no usage is visible yet, do not assume the service is broken. Usage data can take time to appear, and an account with no billable usage may show zero or no cost records.
6. If your account has an invoice, open the invoice area and inspect the available billing period, totals, and line items. Do not publish or share personal billing details.

**Important:** Cost analysis is not the same as a final invoice. An invoice is issued according to your billing agreement and billing period. You may not receive one immediately at the end of this lab.

### Step E — Clean up the lab

1. If you deployed a resource, first inspect it and confirm that you do not need anything stored in it.
2. Delete the lab resource(s) you created, following your instructor's instructions.
3. Verify that the resources have been deleted.
4. Delete `rg-az900-school-lab` only after confirming it contains no resources you need. Deleting a resource group deletes its contained resources.
5. Recheck Cost Management later to see whether any usage charges were recorded. Deleting resources prevents future use of those resources but does not erase charges already incurred.

### If you cannot create an Azure account or do not have an active subscription

Complete this no-cost conceptual simulation instead. These are sample values, not live Azure prices or a real bill.

| Simulated item | Usage | Example rate | Example cost |
|---|---:|---:|---:|
| Virtual machine compute | 3 hours | KSh 10/hour | KSh 30 |
| Storage | 5 GB-month | KSh 2/GB-month | KSh 10 |
| Data transfer | 2 GB | KSh 3/GB | KSh 6 |
| **Illustrative total** | | | **KSh 46** |

These hypothetical rates are only for arithmetic practice. Actual Azure prices depend on service, region, configuration, agreement, and current pricing. Taxes, discounts, credits, and other charges are not included.

### Practical questions to submit

Answer these in your project notes or submission:

1. What subscription was visible in your account? If you had no subscription, what prevented access?
2. What is the difference between a subscription and a resource group?
3. Which subscription did you select when creating the lab resource group?
4. Which settings on the resource-creation screen could affect cost?
5. Did Cost Analysis show any usage? Explain why the amount may be zero, delayed, or unavailable.
6. Is Cost Analysis the same as an invoice? Explain the difference.
7. What resource(s) did you create and delete? If you did not deploy anything, explain why stopping at the review screen was the safer choice.
8. Using the hypothetical table above, calculate the total and explain which usage generated each charge.

**Evidence to capture (hide personal identifiers):** a screenshot of the subscription list or subscription overview; the lab resource group and its resources (if any); and the Cost Analysis or simulated cost table. Hide subscription IDs, tenant IDs, email addresses, payment details, and other sensitive information before submitting.

### Success criteria

You have completed the exercise when you can identify a subscription, explain its relationship to resource groups and resources, identify where Azure cost information is reviewed, distinguish cost analysis from an invoice, and confirm that any lab resources have been cleaned up. A real invoice is not required if the billing period has not closed or no billable usage occurred.


## Key takeaway

The consumption-based model connects cloud usage with cost. Azure provides a hierarchy—management groups, subscriptions, resource groups, and resources—to organize workloads and manage them. Understand which resource is being used, how it is priced, and the scope at which you review its costs.

### What comes next?

Later Azure management and governance lessons go deeper into the pricing calculator, Cost Management, tags, budgets, Azure Policy, and ways to control spending.

---
**Study note:** The rates in the arithmetic example are hypothetical. Check current Microsoft Azure pricing for real cost estimates. These are original learning questions, not copied exam questions.
