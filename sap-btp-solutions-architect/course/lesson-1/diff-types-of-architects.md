## Lesson 1: Enterprise IT Arhictecture
- An Enterprise IT Architecture is the city plan for a companys technology. Its a strategic blueprint that aligns an organizations IT assets hardware, software, data, and networks—with its business goals.

- This is the single most important benefit. EA translates business strategy (e.g., "We want to expand into European markets" or "We need to improve customer self-service") into a concrete technology roadmap.

### Advantages of using an Enterprise Architecture
1. Promote Growth
- All about staying in tune and up to date with latest tech trends to stay competitive. From Monoliths to Microservices, Cloud transformation, IoT Architectures

2. Ensure Compliance
- Data Compliance and Governance standards

3. Reducing Complexity 
- Post merger integration, integration architectures

### Enterprise Architecture Frameworks
1. Zachmann
- John Zachmann published his work A Framework for Information Systems Architecture. It was notived that a architecture of IT componenets within an enterprise was needed with the following objectives:

- Start meaningful dialogues between all stakeholders within the information system.
- Create concrete added value through architectural representations.
- Evaluate operational tools and/or methods in relation to each other.
- Optimization of dominant approaches to the development of IT applications.

2. The Open Group Architectural Framework (TOGAF)
- A method for designing, implementing, controlling, and managing the development of an organization using controlled phase

---

## Lesson 2: Diff types of architects
*Enterprise Architects vs. Solution Architects*

- An Enterprise Architect is like a City Planner. They don't design individual buildings. Instead, they look at the entire city and plan its overall structure. Their goal is the long-term health and coherence of the entire city.

- A Solution Architect is like a Building Architect. They are given a specific plot of land within the city (a business problem) and must design a functional, safe, and effective building (a technology solution) on that plot. They must follow the city planner's zoning laws and connect to the existing utility and transportation grids.

### Comparison Table: Enterprise Architect vs. Solution Architect

| Feature | Enterprise Architect (EA) | Solution Architect (SA) |
|---|---|---|
| **Primary Focus** | **Strategic:** “What” and “Why” | **Tactical:** “How” |
| **Scope** | **Enterprise-wide:** The entire organization, its goals, processes, and technology landscape. | **Project/Solution-specific:** A single business problem, application, or system integration. |
| **Time Horizon** | **Long-term:** 3-10 year roadmaps. Focused on the future state of the organization. | **Mid-term:** The lifecycle of a specific project, usually months to 1-2 years. |
| **Key Question** | “How can technology enable our long-term business strategy?” | “How do we build a technical solution to solve this specific business problem?” |
| **Stakeholders** | C-level executives such as CIO, CTO, and CEO; business unit leaders. | Project managers, business analysts, development teams, and infrastructure engineers. |

---

## Lesson 3: SAP Enterprise Architecture Framework Tools
- The set of tools which can be used by enterprise architects in performign their tasks. Some of these tools are:

### 1. SAP Signavio: The "Why & What"
- This tool is a "GPSfor Business Processes". It tells an organization why and what to build by revealing how the business actually runs, where the pain points are, and what the ideal future state looks like. 

Imagine and architect gets a request like this: "We need an app to approve invoices faster." This is how SAP Signavio can help:

- **Process Mining:** SAP Signavio connects directly to systems like SAP Cloud ERP and analyzes event logs. It produces a visual, data-backed map of how a process (e.g., Order-to-Cash) actually runs, not how people think it runs.

- The Value: An organization can pinpoint the exact bottleneck. Is the invoice approval slow because of a specific user, a missing data field, or a system integration failure? This data justifies the business case for your BTP project and ensures you're aiming at the real target.

**Process Modeling (BPMN):** It provides a collaborative environment to design the "to-be" process. Business analysts and process owners can map out the ideal future state using a standard notation.

### 2. SAP LeanIX: The "Where & How"
- Once SAP Signavio tells you what to build, SAP LeanIX tells you where it fits in the existing maze of technology.

**Application Portfolio Management (APM):** SAP LeanIX acts as a definitive catalog of every application in your landscape (SAP, non-SAP, on-prem, cloud, custom).

The Value: Before an organization builds a new SAP BTP app, they can instantly check: Do we already have a tool that does this? What applications will my new SAP BTP app need to integrate with?

Technology & Risk Management: It maps the underlying technologies (e.g., Java versions, Node.js runtimes, database types) and their lifecycles.

The Value: Organizations can make informed decisions about the technology stack for their SAP BTP solution (e.g., CAP vs. RAP, Cloud Foundry vs. Kyma)

### 3. SAP Cloud ALM
- Provides architects a central entry point to manage SAP landscapes (cloud, on-premise and hybrid) with content-driven guided implementation and highly automated operations

### 4. SAP Build
- SAP Build (a part of SAP BTP) is a suite of low-code and pro-code tools designed to accelerate application development and automation. SAP Build can be used when architectural designs require custom applications or extensions to applications to be built.

---

## Lesson 4: Understanding SAP Reference Business Architecture
Covers:
- SAP Reference Architecture Content Framework
- Business Capability & Business Process Model
- Solution Capability & Solution Process Model 

- SAP Reference Business Architecutre is basically SAPs prebuild map of how a company works and which SAP solutions can support that work. It helps architects avoid starting from a blank page. 

We can think of it in 3 connected maps:
| Layer | Simple Meaning | Example |
|---|---|---|
| Business Capability Model | What the business must be able to do | Manage customer orders |
| Business Process Model | How the business does it step by step | Receive order, check inventory, ship goods, invoice customer |
| Solution Architecture | Which systems/software support it | SAP S/4HANA Sales, SAP BTP Integration Suite, SAP Build Process Automation |

### SAP Reference Architecture Content Framework
Lets break this phrase down:

- SAP --> The vendor providing the solution
- Reference --> A reusuable starting point
- Architecture --> A structured view of business
- Content --> The actual maps and diagrams
- Framework --> The organizing structure

SAP Reference Architeture Content Framework = SAPs reusuable library of business and solution maps that helps architects connect business needs to SAP solution. Its not like an application so to say its more like an architecture guidebook and mapping systems.

### Business Capability Model
- A business capability = Something the organization must be able to do to create value. For example such as: Manage inventory, manage customer orders, etc. 
A business capability is about what, not how. For example if we have a business capability to manage customer order, that doesnt yet say whether the order comes from a website, mobile app, or call center --> It just states the business need. It only covers the "what" not the "how"