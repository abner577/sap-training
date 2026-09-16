## Describing Application Development and Automation Services
This lesson is about how SAP BTP supports building applications and automating business processes. This unit will zoom into one major BTP capability area: Application development and automation. So this includes things like:

- Building new apps around SAP systems, extending SAP systems without heavily modifying them, automating workflows and repetitive tasks.

Once again this follows the clean core philosophy and explains why SAP has shifted toward it and the historical sturggles that companies have had when heavily customizing SAP.

### SAP S/4HANA Cloud Extensibility Model
- This lesson introduces 3 main extension approaches

| Extension Type | Where It Runs | Who Usually Uses It | Best For |
|---|---|---|---|
| Key user extensibility | Inside S/4HANA | Business/key users | Simple fields, UI changes, rules, forms |
| Developer extensibility | Inside S/4HANA | ABAP developers | More advanced logic close to the ERP |
| Side-by-side extensibility | On SAP BTP | Developers/architects | External apps, complex extensions, integrations, workflows |

Side-by-side extensions means the custom application runs beside the ERP, usually on SAP BTP. It then comm. with S/4 through relreased APIs, events, or integration services. 

Example:
A retailer wants a custom returns portal.

S/4HANA owns:
- Sales orders
- Customer records
- Inventory postings
- Refund accounting
(i.e. all the data)

BTP owns:
- The customs return UI and all the features such as approval workflow, photo upload, and customer notis.

The portal calls S/4HANA APIs when it needs official sales order or return data (i.e. data).

Why this is better than putting everything in S/4HANA:
- The customer-facing portal can evolve independently.
- The ERP core stays cleaner.
- Upgrades are less risky.

### Clean Core Level Concept
- It uses levels A-D

| Level | Meaning | Risk |
|---|---|---|
| Level A | Uses released, stable public interfaces and ABAP Cloud | Lowest risk |
| Level B | Uses some unreleased but SAP-classified stable APIs | Still preferred/acceptable |
| Level C | Uses unreleased APIs needed for legacy scenarios, with changelog awareness | Higher risk |
| Level D | Uses non-recommended objects or techniques | Highest risk |

- Clean core isnt just about public cloud as well, these principles still matter for private cloud and on-premise landscapes. 

### BTP tools
The main tools are:

**1. SAP Build Apps** --> Low-code --> Used for UI app development
- Lets users build apps visually with drag and drop componenets, connect to backend systems and write application logic without writing much code. 
*But this is deprecated as the standalone product as SAPs direction is the unified SAP Build offering, so SAP Build is the broaderd unified platform.*

**2. SAP Build Code** --> Pro code --> Use dfor full-stack dev and extension development
- For devs, supports code-based dev especially for building extensions and applications on SAP BTP. Includes things like AI assistance, API access, CI/CD support. 

- Often built using Java or Node.js

**3. ABAP Development Tools for Eclipse** --> Pro-code but specifically for ABAP --> Used for ABAP-based development
- For ABAP developers, key programming model here is RAP, the ABAP RESTful Application Programming Model. RAP is used to build modern ABAP-based services/APIs.

**4. SAP Build Process Automation** --> Low-code/no-code automation --> Workflows, approvals, document processing
- For automating workflows and tasks.

**5. SAP Build as a Unified Portfolio (Combines 1, 2, 4)**
It includes:
- SAP Build Apps for low-code app development
- SAP Build Process Automation for workflows and automation
- SAP Build Work Zone for business sites and entry points
- SAP Build Code for pro-code development

- The important direction is "fusion team development" --> Which means that business people and technical people work together.

---
Question about compilers and runtime enviornments:
- The compiler itself doesnt automatically ccome bundled as part of the runtime environment.

**- A compiler** translates your source code into machine code or bytecode before the program runs
**- Runtime Environment** = The software system that supports and manages your program while it is actively executing, handling tasks like memroy allocation, garbage collection, and thread management.

Now there are two types of languages really: Ahead-of-Time (AOT) & Just-In-Time (JIT) languages when it comes to the subject of compiling:
1. AOT compiled Languages
- Use a standalone compiler like GCC to turn code directly into native machine instructions.

2. JIT compiled Languages
- Languages like Java or C# use a compiler to turn source code --> bytecode first. --> Then the runtime like a JRE/JVM contains a JIT compiler inside it to translate that intermediate code into machine code right as it runs. In these specific cases the runtime does include a specialized compiler component.
---

## Runtime environments and programming models
- This lesson tackles the question: "If you build an application or extension on SAP BTP, where does it run, and what programming model do you use to build it?"

### Runtime Environments
- SAP BTP mainly gives three runtime options:

**1. Cloud Foundry** --> General cloud-native business apps and extensions
- It supports multiple programming languages through buildpacks. A buildpack is basically the mecahnism that detects your app type and prepares it to run. Cloud Foundry gives devs built-in platform features like:

- Routing, Load balancing, deployement, scaling, containerization, etc.

- We typically use this when we are building a normal web app, side-by-side extension, for more like typical business applications.

**2. Kyma** --> Containerized, Kubernetes-based, microservice/event-driven apps
Use Kyma when:
- You are building highly scalable microservices.
- You need Kubernetes flexibility.
- You need event-driven architecture.
- You need service mesh capabilities.

A service mesh helps manage communication between many microservices. It can handle routing, security, observability, and traffic behavior between services.

**3. ABAP Environment**--> ABAP-based cloud apps and extensions
SAP BTP ABAP Environment is a cloud-based ABAP runtime.
This is important because ABAP is not only for traditional on-premise ERP customization. SAP also supports modern cloud ABAP through ABAP Cloud and RAP.

*Question about whats the diff, what makes microservices/event-driven apps better to be containerized instead of normal? I thought basically all apps were containerized and use docker? Isnt this what you upload to cloud providers and stuff? Do cloud providers use this stuff in the backend to scale up and down?*

### Programming Models
- A programming model is the recommended way developers structure and build applications. The lesson focuses on two:

1. CAP --> Cloud Foundry / Kyma 
2. RAP --> ABAP Environment --> Modern ABAP / ABAP CLOUD

#### CAP: Cloud Application Programming Model
- CAP is SAPs framework for building cloud-native business applicaitons. It helps devs build enterprise apps faster by providing patterns and libraries for common tasks instead of manually coding everything from scratch. CAP gives a structured way to define:

- Data models, services, queries, relationships, APIs, etc.

#### RAP: ABAP RESTful Application Programming Model
- RAP is SAPs modern ABAP programming model, very similar to what CAP is and what it provides but just in the ABAP world.

### SAP Fiori
- Is the UI/UX design system for SAP applications. It focuses on clean/simple UI and role-based experience (i.e. users see what is relevant to their job.)

- Fiori apps are commonly built using SAPUI5, which is SAPs Javascript UI framework, and then often consume OData services from CAP, RAP, or S/4HANA

- So CAP/RAP often provide the backend and Fiori is the frontend. 

#### How backend and frontend comm.
A full-stack SAP application might look like this:
User
-> SAP Fiori UI
-> OData API
-> CAP or RAP backend
-> SAP HANA Cloud / S/4HANA / other systems

### Mobile Applications
- In SAPs mobile ecosystem there are 3 important concepts:

| Mobile Component | What It Is |
|---|---|
| SAP Mobile Services | Backend platform for mobile apps |
| SAP Mobile Start | End-user mobile entry app |
| SAP Mobile Cards | Small card-based business content/actions |

**SAP Mobile Services**
- This runs on SAP BTP, its not the app users install. Its the backend platform developers/admins use to support movile apps. It provides:

- Secure backend connectivity
- Authentication and SSO
- Offline access
- Push notifications
- Monitoring and analytics

**SAP Mobile Start**
- Is the user-facing mobile app. It gives users a central mobile entry point for SAP work.

**SAP Mobile Cards**
- They are small, focused pieces of business information. They are like micro-apps or wallet-style cards. A card might show:

- A workflow task, a purchase order approval, a sales order summary, etc.

- So they are quick buisness information and simple actions without opening a full app.

### Mobile Development Options
| Tool | Best For |
|---|---|
| SAP Mobile Development Kit | Cross-platform enterprise apps with faster development |
| SAP BTP SDK for iOS | Native iOS apps |
| SAP BTP SDK for Android | Native Android apps |