# Module 1 · Unit 1: Introduction to Microsoft Azure Fundamentals

**Learning path:** Introduction to Cloud Infrastructure: Describe cloud concepts  
**Status:** Draft for learner review  
**Teaching approach:** Start with a familiar situation, explain the need, then introduce the technical words.

## Scenario: A school wants reliable student records

Imagine a school wants to keep an organised record of every student: names, admission numbers, classes, attendance, results and contact details.

At first, staff might keep paper files or separate spreadsheets on individual computers. That can work for a small amount of information, but problems appear as the school grows:

- Different offices may keep different copies, so information becomes inconsistent.
- Finding a record can take time.
- Staff may need to visit the office or computer where a file is stored.
- Backups and access permissions can be difficult to manage consistently.

The school therefore considers keeping the records in one central system that authorised staff can access from their own computers.

## What is a server, and why use one?

A **server is a computer that provides something to other computers**. It might store shared files, run the student-record application, or manage a database.

For example, the school's server could hold the central student database. The admissions office and teachers would use their computers to access the system, according to their permissions.

The point is not that every school needs a dedicated server just to keep student records. A server is one possible way to provide a shared system; a school might instead use a hosted service or another setup.

## What are computing resources?

**Computing resources are the equipment and capacity needed to run digital systems.** In our school example, that can include:

- **Processing power:** the ability to carry out the instructions in the student-record system.
- **Memory:** working space the system uses while it is running.
- **Storage:** space where student records and files are kept.
- **Networking:** the connections that let staff computers communicate with the server.

Think of these as the computer's working capacity, short-term workspace, filing space and communication links.

## What are computing services?

A **computing service is something useful made available using computing resources**.

In the school example:
- The server's processing power, memory and storage are resources.
- A student-record application that lets staff register learners and view results is a service.
- A shared file area where staff keep school documents is another service.

The school needs the useful outcome—such as recording a student's results—not necessarily to own every machine that makes it possible.

## Why might running its own server become difficult?

If the school owns and operates the server, it or its IT provider must plan for:

- **Upfront cost:** buying suitable equipment and setting it up can require significant initial spending.
- **Growth:** if more students, records or users put pressure on the system, the school may need to upgrade or add equipment.
- **Maintenance:** hardware can fail; equipment needs power, a safe location, updates and technical support.
- **Backups and recovery:** the school needs a plan for restoring records if equipment fails or data is lost.
- **Security:** the school must control access and protect the equipment and information, with help from its IT provider where applicable.

This arrangement can still make sense in some situations. The difficulty is that the school must plan and pay for the capacity and responsibilities it manages.

## Where cloud computing enters the picture

Instead of buying and operating all the underlying physical equipment, the school could use a provider's computing resources over a network, usually the internet.

The provider operates the physical data-centre equipment. The school uses the services it needs and remains responsible for the parts it controls, such as deciding who should access student records.

That is the basic idea behind **cloud computing**: using computing resources and services supplied over a network, rather than having to own and manage all the underlying physical infrastructure yourself.

Cloud services do not make costs, security or maintenance disappear. They change which tasks the provider handles and which remain with the school. The details depend on the service chosen.

## Key idea

The school wants a dependable way to store, process and share information. A server is one way to provide the computing resources behind that system. Cloud computing offers another way: the school can use resources operated by a provider instead of managing all the physical equipment itself.

## Check your understanding

1. In this scenario, what is the difference between the server's storage and the student-record application?
2. Why might the school need more computing resources as the number of students and users grows?
3. If the school uses a cloud provider, does that mean the school has no security responsibilities? Explain briefly.

## Content notes

- This is an introductory explanation, not a claim that all schools run their own servers.
- The school example will be reused across later units to explain shared responsibility, cloud models, scalability and consumption-based costs.
- Keep the language simple; introduce formal Azure terminology only after the idea is understood.
