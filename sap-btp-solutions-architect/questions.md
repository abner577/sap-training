## Questions

1. *Is it specifically for integrating with existing SAP services like BRIM? Or for just connecting diff parts of our buisness (i.e. diff apps) together? Is the integration suite specifically for this or are there other parts for Integration that arent Integration Suite?*

2. *So is it like you build a custom app and through Integraiton Suite it enables comm. between that app and other SAP systems? Or can we also enable communicate between our already existing apps & external apps and SAP systems? Also enable communication between our already apps between each other, is this another aspect another part that isnt integration suite?*

## Answers
- BTP is a platform full of separetly consumable services, runtimes, tools, and capabilities. You dont automatically use all of them. An architect chooses the pieces needed for a particular solution.

For example:
- Companies may use BTP much differently while one may use it primarily for integration and analytics another might use it alot for application development.

- Additionally, application development supports multiple languages not just ABAP. --> You write normal application code. BTP is providing the cloud environment where that application runs and the services around it.

- SAP also has Business Application Studio, which is essentially a cloud-based professional development environment. We cna think of it as a somewhat SAP-oriented cloud IDE with tools for building, and connecting to SAP systems. 

#### Integration Suite understanding
- Integration Suite isnt limited to connecting application that were created on BTP. It can connect:

SAP application → SAP application
SAP application → non-SAP application
non-SAP application → SAP application
even non-SAP → non-SAP
cloud → cloud
cloud → on-premises
on-premises → cloud

- So one of its core jobs are enabling communication between already-existing external apps and SAP systems. 

---

Just because you need communication between things in and out of the SAP landscape doesnt necessarily mean you need Integration Suite. --> Integration Suite becomes particular valuable when you need things like:
- Transformation, orchestration, monitoring, API governance, etc.

### How does BTP provides its services and functionality?
- For example we know that BTP gives functionality that provides monitoring, securtiy, AI, etc. --> The main way that it provides these funtionalities is by giving you a service that you can pick which in turn provides this for you.

- So we can think of the BTP platform as a giant catalog:
                 SAP BTP
       ┌──────────────────────────┐
       │ Application runtimes     │
       │ Databases                │
       │ Integration              │
       │ Authentication           │
       │ Logging                  │
       │ Monitoring               │
       │ Analytics                │
       │ AI                       │
       │ Automation               │
       │ API management           │
       │ Event messaging          │
       │ Connectivity             │
       │ Development tools        │
       └──────────────────────────┘

- Then the solutions architect would say: "For this particular solution, which of these do we need?"

