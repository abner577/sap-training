# SAP BTP Solution Architect Review Notes

## Unit 1: Architecture Context

Main lesson: SAP Reference Business Architecture helps an architect move from a business need to a possible SAP solution design without starting from a blank page.

The basic flow is:

Business need -> business capability -> business process -> solution capability -> solution component -> architecture/integration/data flow

Important distinctions:

| Concept | Plain Meaning |
|---|---|
| Business capability | What the business must be able to do |
| Business process | How the business does it step by step |
| Solution capability | What the software must be able to support |
| Solution component | The actual SAP product, service, or component that provides the capability |

SAP Reference Business Architecture is SAP's reusable map of how companies commonly work and which SAP solutions often support that work. It does not automatically choose the solution for you, but it gives the architect a strong starting point.

High-level solution architecture is the broad map. It shows which SAP products and capabilities are usually involved for a business area.

Detailed solution architecture goes deeper. It shows:

- which SAP components are involved
- which process steps happen in which component
- how systems connect
- what data moves between systems

Solution value flow connects business value to software behavior. It shows how SAP solutions support a business outcome, such as receiving an order, confirming it, delivering the product, invoicing, and collecting payment.

Solution process flow is more detailed than the value flow. It shows the actual sequence of system-supported steps.

Simple mental model:

Reference Business Architecture explains what the business needs to do. Reference Solution Architecture explains how SAP software can support it.

## Unit 2: SAP BTP Basics, Resources, and Cost

Main lesson: SAP BTP is not one giant application. It is a cloud platform and set of services that companies use to build, extend, integrate, automate, analyze, and add AI around SAP and non-SAP systems.

The main architecture idea is clean core:

S/4HANA should stay focused on core business transactions. BTP is often used around it for extensions, integrations, automation, analytics, and AI so the ERP core does not become overloaded with custom code.

Why clean core matters:

- Heavy ERP customization creates technical debt.
- Upgrades become harder because custom changes may break.
- Keeping extensions on BTP makes changes easier to manage.
- Architects should decide what belongs in S/4HANA and what belongs outside on BTP.

Major BTP areas:

| Area | What It Is Used For |
|---|---|
| Application development | Build custom apps and extensions |
| Automation | Automate workflows, approvals, and repetitive tasks |
| Integration | Connect SAP and non-SAP systems |
| Data and analytics | Store, model, analyze, and report on data |
| AI | Add AI capabilities, model access, and AI lifecycle support |
| Foundation services | Handle security, identity, connectivity, monitoring, and platform basics |

Common services mentioned:

| Need | Example Services |
|---|---|
| Low-code/no-code apps | SAP Build Apps |
| Pro-code development | SAP Build Code |
| User entry point/workspace | SAP Build Work Zone |
| Workflow and task automation | SAP Build Process Automation |
| Data and analytics | SAP HANA Cloud, SAP Business Data Cloud |
| AI lifecycle and model access | SAP AI Core, SAP AI Launchpad, Generative AI Hub |

BTP account model:

| Concept | Plain Meaning |
|---|---|
| Global account | The top-level account that represents the commercial agreement with SAP |
| Directory | Optional grouping for subaccounts |
| Subaccount | Where applications, services, entitlements, subscriptions, and environments are managed |
| Region | The geographic location where apps or data are hosted |
| Environment | The runtime inside a subaccount, such as Cloud Foundry, Kyma, or ABAP environment |

Subaccounts can be organized by region, environment, business unit, or lifecycle stage such as dev, test, and prod.

Basic cost models:

- Trial account: used for learning and experimentation.
- Free tier: try certain services with free usage limits.
- Pay-as-you-go: consume services and pay based on usage.
- Consumption-based agreement: commit to a pool of cloud credits and consume eligible services.
- Subscription: pay for a specific service or product subscription.

Useful SAP resources:

| Resource | What It Helps With |
|---|---|
| SAP BTP Guidance Framework | Choose architecture approaches and technology options |
| SAP Discovery Center | Explore BTP services, missions, and use cases |
| SAP Business Accelerator Hub | Find APIs, events, integrations, and reusable business content |
| SAP Architecture Center / Reference Architecture | Find proven patterns and blueprints |
| SAP BTP Solution Diagrams | Communicate architecture visually |

Simple mental model:

S/4HANA owns the core business records and transactions. BTP gives architects the surrounding tools to extend, connect, automate, analyze, and innovate without stuffing every custom idea into the ERP core.

## Unit 3: Application Development and Automation

Main lesson: This unit is about how BTP helps companies build apps, extend SAP systems, and automate business work without putting every custom change inside S/4HANA.

Main use cases:

- Build new apps around SAP and non-SAP systems.
- Extend SAP systems while keeping the core cleaner.
- Automate workflows, approvals, document handling, and repetitive tasks.

SAP Build portfolio:

| Tool | What It Is Used For |
|---|---|
| SAP Build Apps | Low-code app development with visual UI building and backend connections |
| SAP Build Process Automation | Low-code/no-code workflows, approvals, automation, and document processing |
| SAP Build Work Zone | Business sites, workspaces, and user entry points |
| SAP Build Code | Pro-code development for developers building full-stack apps and extensions |

Other development tools:

| Tool | What It Is Used For |
|---|---|
| ABAP Development Tools for Eclipse | Pro-code ABAP development |
| SAP Fiori | SAP's UI/UX design system for business apps |

Runtime environments:

| Runtime | When It Fits |
|---|---|
| Cloud Foundry | General cloud-native business apps and extensions |
| Kyma | Kubernetes-based, containerized, microservice, or event-driven apps |
| ABAP environment | ABAP-based cloud development and extensions |

Programming models:

| Model | Plain Meaning |
|---|---|
| CAP | SAP's Cloud Application Programming Model for building cloud-native business apps, often with Node.js or Java |
| RAP | ABAP RESTful Application Programming Model for building modern ABAP services and apps |

CAP helps developers define data models, services, relationships, queries, and business logic in a structured way instead of building everything from scratch.

Mobile services:

| Service | What It Is Used For |
|---|---|
| SAP Mobile Services | Backend platform services for mobile apps |
| SAP Mobile Start | End-user mobile entry point for SAP work |
| SAP Mobile Cards | Small card-based business actions and information |

Running an app also needs support services:

- Identity and user access so the right users can log in and do the right things.
- Logging and observability so teams can see what the app is doing and troubleshoot issues.
- CI/CD to build, test, and deploy applications.
- SAP Cloud Transport Management to move deployable content between environments such as dev, test, and prod with control and governance.

Simple mental model:

Unit 3 is about building and running the custom side of the architecture. S/4HANA keeps the core business process stable, while BTP gives teams the tools to create apps, automate work, choose the right runtime, and operate what they build.
