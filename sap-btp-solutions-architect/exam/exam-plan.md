# SAP Certified Professional - Solution Architect - SAP BTP Prep

## Certification Goal

Target certification: SAP Certified Professional - Solution Architect - SAP BTP.

The goal is to demonstrate professional-level ability to translate business requirements into an end-to-end SAP solution blueprint using SAP BTP and related SAP ecosystem capabilities. The emphasis is not memorizing service names in isolation, but explaining architecture decisions, responsibility boundaries, integration choices, governance, extensibility, data, AI, operations, and trade-offs.

## How Codex Should Help

Use this repo as the continuity anchor if a new chat starts. The learner has completed the "Becoming an SAP BTP Solution Architect" course and is moving into certification preparation.

Codex should help by:

- Correcting misconceptions objectively.
- Asking the learner to justify architecture choices, not just recognize terms.
- Connecting answers to SAP BTP, S/4HANA, Integration Suite, SAP Build, data and analytics, AI, foundation services, cost, operations, and governance.
- Verifying current SAP facts from official SAP sources when names, exam rules, service availability, or certification details matter.

Codex should not claim generated questions are real exam questions.

- A solution architect should start with the business outcome, then map capabilities, products, integrations, data ownership, security, cost, and operations.

## Main Review Map

### Unit 1: Architecture Context

- Enterprise architecture aligns business strategy, processes, applications, data, and technology.
- Solution architecture designs a specific solution inside the enterprise architecture guardrails.
- SAP Signavio helps understand and model business processes.
- SAP LeanIX helps understand application landscapes, dependencies, lifecycles, and portfolio rationalization.
- SAP Cloud ALM supports implementation and operations lifecycle management.
- SAP Reference Architecture helps map business capabilities, business processes, solution capabilities, solution components, value flows, process flows, component diagrams, and data flows.

Key distinction: business capability is what the business must do; business process is how it does it; solution capability is what software must support; solution component is the actual product or service.

### Unit 2: BTP Basics, Account Model, Resources, Cost

- Global account represents the commercial/contractual top-level account.
- Directories optionally organize subaccounts.
- Subaccounts are where services, applications, subscriptions, entitlements, quotas, and runtime environments are managed.
- Regions matter for latency, availability, data residency, and supported service availability.
- Environments include Cloud Foundry, Kyma, and ABAP environment.
- Entitlement means the right to use a service or plan; quota means the allowed amount.
- Some services are consumed as subscriptions; others as service instances with bindings or service keys.
- Trial, Free Tier, Pay-As-You-Go, CPEA/BTPEA, and subscriptions have different cost/flexibility trade-offs.
- Discovery Center, SAP BTP Guidance Framework, SAP Business Accelerator Hub, SAP Architecture Center, and SAP Trust Center are official architecture resources.

Exam instinct: do not guess service choices; use guidance, reference architectures, API catalogs, trust/compliance information, and cost estimation.

### Unit 3: App Development, Automation, Extensibility

- Key-user extensibility: simple in-app S/4HANA adaptations by business/key users.
- Developer extensibility: ABAP-based extensions close to S/4HANA using released cloud-ready approaches.
- Side-by-side extensibility: apps or services on BTP communicating with S/4HANA through released APIs/events.
- CAP is SAP's cloud application programming model, commonly for Node.js/Java business apps on BTP.
- RAP is SAP's ABAP RESTful Application Programming Model for modern ABAP services and applications.
- SAP Fiori is the SAP UX design system; SAPUI5 is a common UI technology.
- SAP Build includes Build Apps, Build Process Automation, Build Work Zone, and Build Code.
- Cloud Foundry is suitable for many business applications and extensions.
- Kyma is Kubernetes-based and fits containerized, microservice, event-driven, and service-mesh needs.
- ABAP environment fits cloud ABAP development.
- CI/CD, Transport Management, Cloud Logging, Work Zone, and SAP Start help deliver and operate solutions.

Exam instinct: decide extension placement by business requirement, ownership, clean core, lifecycle, integration, and user audience.

### Unit 4: Data and Analytics

- DAAM starts with business outcome, current state, data ownership, use cases, and governance before choosing tools.
- SAP HANA Cloud is a managed database service.
- SAP Datasphere supports business data fabric, semantic modeling, integration, virtualization, cataloging, and analytical modeling.
- SAP Analytics Cloud is the analytics, planning, dashboarding, and analysis front end.
- SAP Master Data Integration helps share master data through common models.
- SAP MDG governs and improves master data quality.
- SAP Business Data Cloud packages governed data products, Datasphere, Analytics Cloud, Databricks, AI, and business data fabric concepts.

Key distinction: HANA Cloud is not the same as Datasphere; SAC is not the same as Datasphere; BDC is a broader business-data offering, not merely a dashboard tool.

### Unit 5: Integration

- Integration strategy includes process integration, API-led integration, event-driven integration, data integration, B2B integration, monitoring, security, and governance.
- Integration Suite is a BTP service family for integration, not only "connect app A to app B."
- Cloud Integration runs iFlows for message processing, mapping, routing, protocol handling, and error handling.
- API Management exposes, secures, monitors, publishes, and governs APIs.
- Open Connectors simplify integration with many third-party SaaS applications.
- Event Mesh and Advanced Event Mesh support asynchronous event-driven architecture.
- Integration Advisor helps define message implementation guidelines and mapping guidelines.
- Integration Assessment applies ISA-M decision logic.
- Migration Assessment supports PI/PO migration analysis.
- SAP Cloud Connector provides secure connectivity from BTP to selected on-premise systems.
- SAP Cloud ALM, Focused Run, and Solution Manager support monitoring/operations in different landscape contexts.

Exam instinct: first identify integration domain, style, pattern, source/target ownership, latency, volume, security, monitoring, and governance. Then choose the tool.

### Unit 6: AI

- SAP Business AI means AI grounded in business context and embedded across SAP scenarios.
- Joule is SAP's generative AI copilot experience.
- Joule Agents are more goal-oriented and agentic, capable of multi-step work.
- Embedded AI is AI already built into SAP applications.
- AI Foundation on BTP supports building, extending, governing, and operating AI.
- Generative AI Hub provides access and governance for models.
- SAP AI Core and SAP AI Launchpad support AI lifecycle and operations.
- Joule Studio extends Joule with skills and agents.
- HANA Cloud Vector Engine supports vector search and RAG-style use cases.
- SAP Knowledge Graph helps ground AI in business object relationships.

Exam instinct: separate user-facing copilot, embedded app AI, developer/AI lifecycle services, model access/governance, and data grounding.

### Unit 7: Foundation Services

- Foundation services support security, identity, connectivity, persistence, operations, lifecycle, logging, jobs, alerts, usage tracking, and administration.
- Cloud Identity Services include identity-related capabilities such as authentication, SSO, MFA, federation, and identity lifecycle support.
- IAS is the authentication/front-door component.
- Authorization decides what authenticated users can do.
- Platform users administer/develop/operate BTP; business users consume applications and services.
- Cloud Connector helps BTP reach selected on-premise resources securely.
- Cloud Logging, Job Scheduling, Alert Notification, and Usage Data Management are supporting services architects should account for.

Exam instinct: foundation services are often hidden in scenarios but required for a complete architecture.

## Distinctions To Keep Sharp

- BTP is not the system of record for every business process; S/4HANA often owns core ERP transactions.
- Integration Suite is not needed for every simple API call, but it becomes valuable for orchestration, transformation, monitoring, governance, reusable content, and hybrid integration.
- Event-driven integration is not the same as synchronous API calls.
- API Management governs APIs; Cloud Integration processes messages/iFlows.
- Datasphere models and exposes business data; SAC consumes and analyzes it.
- HANA Cloud can store application/analytical data, but it is not automatically the complete analytics architecture.
- Joule is not the same thing as all SAP AI.
- Clean core does not mean "never customize"; it means use cloud-ready, upgrade-friendly, released extension approaches.