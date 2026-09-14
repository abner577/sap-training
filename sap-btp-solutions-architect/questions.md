## Questions

1. *Is it specifically for integrating with existing SAP services like BRIM? Or for just connecting diff parts of our buisness (i.e. diff apps) together? Is the integration suite specifically for this or are there other parts for Integration that arent Integration Suite?*

2. *So is it like you build a custom app and through Integraiton Suite it enables comm. between that app and other SAP systems? Or can we also enable communicate between our already existing apps & external apps and SAP systems? Also enable communication between our already apps between each other, is this another aspect another part that isnt integration suite?*

*3. Difference between SAP BTP and S/4HANA what is BTP`s role?*

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

---
---

## Difference between BTP and S/4HANA
- S/4HANA is primarly the business system where core ERP processes and data live. BTP is the broader technology platform you use around systems like S/4HANA to extend them, integrate them with other systems, and use additionaly servie.

- BTP is often used with S/4HANA

### S/4HANA already has many of these capabilities
- SAP does offer many of the things that BTP offers, so naturally it begs the question, why use BTP at all? 
- Well when you are using these services and doing things inside S/4HANA such as writing ABAP-based extensions, adding fields, reacting to business events, etc.

- SAP generally calls this on-stack extensibility -> Meaning that your customization is living very close to the ERP itself. 

Imagine this scenario:
A company uses:
- S/4HANA for procurement and inventory, Salesforce for customer relationships, a custom supplier portal etc.

- Now the company wants a new application where: "Create a supplier portal where suppliers can see purchase orders from S/4HANA, upload documents, receive shipment information, and communicate with our procurement department."

- Now technically we may be able to put parts of this inside S/4HANA but architecturally it probably doesnt make sense. Instead we do some sort of architecture like:

            Suppliers
                │
                ▼
            Supplier Portal
            on BTP
                │
                │
                │           
                ▼           
            Integration   
                Suite
                │
    ┌───────────┼───────────┐
    ▼           ▼           ▼
    S/4HANA     Shipping    Other APIs


## Clean core philosophy
- Keep the ERP core as standard and upgrade-friendly as practical, and put loosely coupled extensions outside it when that makes architectural sense. SAP explicitly distinguishes on-stack extensions in S/4HANA from side-by-side extensions on BTP. Side-by-side applications run independently and communicate with S/4HANA through released APIs and events.

- Where the main point that we need to understand is that BTP provides the external application and technology around that core business system.

And its a big part of the "clean core" philosophy that SAP is pushing. Hisorically ccompanies would heavily customize their SAP ERP systems where we have many customizaton and cusom code. But the problem is that it creates tecnical debts because once SAP releases an upgrade you no longer know if all your customization will still work. 