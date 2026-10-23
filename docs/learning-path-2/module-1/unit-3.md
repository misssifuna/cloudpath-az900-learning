# Learning Path 2 — Module 1, Unit 3: Get started with Azure accounts

## Learning goal

Understand the difference between a Microsoft sign-in identity, an Azure account arrangement, and an Azure subscription.

## 1. Start with a real-life example

Imagine Holy Trinity Boys Senior School in Saboti wants to host its website on Azure. Before the school can create cloud resources, someone needs to sign in, have the right permissions, and use an Azure subscription.

A simplified picture is:

1. **Identity / sign-in account:** Who are you?
2. **Azure subscription:** Which subscription provides the scope for resource access and billing?
3. **Azure resources:** Which cloud services are created, such as a website, storage account, or database?

This is a simplified picture: the permissions assigned to the signed-in identity also determine which resources it can manage.

## 2. Understand the three terms

### A. Microsoft account

A Microsoft account is a personal sign-in identity used for Microsoft services. A person might use an Outlook.com address or another email address registered as a Microsoft account.

An email address alone does not tell you whether the identity is a personal Microsoft account or a work/school account.

### B. Azure account

“Azure account” is commonly used to describe the account arrangement that gives a user or organization access to Azure. It is associated with a sign-in identity and, depending on how Azure is set up, billing and subscription arrangements.

You might sign in with a personal Microsoft account or an organizational work/school identity.

### C. Azure subscription

An Azure subscription is a logical boundary used to organize Azure resources and manage access and billing.

For example, a school could use one subscription for its website and another for a separate project, if its administrative needs justify that arrangement.

## 3. How they fit together

- A **sign-in identity** helps establish who is trying to access Azure.
- An **Azure subscription** provides a scope for resource management, access control, and billing.
- **Azure resources** are the services you create and use inside a subscription, such as virtual machines, web apps, and storage accounts.

One identity can have access to multiple subscriptions, depending on its permissions. A subscription is not the same thing as a Microsoft account.

## 4. Free account and billing awareness

Microsoft offers Azure account options that may include free services or credits for eligible new customers. Offers and eligibility can change, so always read the current terms before signing up.

Important safety habits:

- Check which subscription is selected before creating a resource.
- Review pricing and estimated costs before deploying billable services.
- Understand that free offers may have limits, eligibility rules, or expiration dates.
- Remove resources you no longer need, and verify that they have actually been deleted.
- Never share passwords or secret authentication codes.

## 5. School example

Suppose a school administrator signs in and can see two subscriptions: **School Website** and **Digital Learning Project**.

If the administrator creates a web app under **Digital Learning Project**, the resource belongs to that selected subscription. Costs and access are managed within the relevant Azure arrangements and permissions.

The identity used to sign in does not itself become the website; it is the identity used to access and manage the Azure environment.

## 6. Original knowledge check

**Question 1:** Which statement best describes an Azure subscription?

A. It is the same thing as an email address.  
B. It provides a scope for organizing Azure resources, managing access, and billing.  
C. It is a physical datacenter.

**Answer: B.**

**Question 2:** Can one sign-in identity have access to more than one Azure subscription?

A. Yes, if the appropriate access has been granted.  
B. No, every identity is permanently limited to one subscription.  
C. Only if every subscription has the same name.

**Answer: A.**

**Question 3:** What should you check before creating a potentially billable Azure resource?

A. Only the color of the Azure portal.  
B. The selected subscription, permissions, and expected costs.  
C. Whether the resource name is short.

**Answer: B.**

## Key takeaways

- A personal Microsoft account and a work/school account are different kinds of sign-in identities.
- An Azure account arrangement gives access to Azure and is associated with identity and subscription/billing setup.
- An Azure subscription is a management and billing boundary for Azure resources.
- One identity may access multiple subscriptions when authorized.
- Always check the selected subscription and expected costs before creating resources.

## Official learning resource

Microsoft Learn: [Describe the core architectural components of Azure](https://learn.microsoft.com/en-us/training/modules/describe-core-architectural-components-of-azure/)

CloudPath AZ-900 Learning Companion is an independent study aid and is not affiliated with or endorsed by Microsoft.
