## Lesson 1: Describing SAP BTP Basics
Main ideas:
- SAP BTP is a cloud platform/portfolio of services, NOT one giant application.
- It helsp companies build, extend, integrate, automate, analyze and add AI around SAP and non-SAP systems
- S/4HANA remains the core business system for many official business transactions
- BTP often sits around the ERP to keep the core cleaner
- The five big BTP areas are: application development, automation, integration, data/analyics, and AI.
- Integration Suite helps connect SAP systems, non-SAP systems, cloud systems, and on-premise systems.

- The main thing that we should takeaway is that BTP is the platform layer that helps enterprises change faster without constantly damaging or over-customizing their core systems. 

**- Technical debt** = short-term technical decisions that make future change slower, riskier, and more expensive. 

- Also the business reason beind clean core is technical debt.

Example:
A company customizes S/4HANA heavily for every special business request. At first, that feels fast. But later, upgrades become painful, integrations become fragile, and every new feature requires untangling old custom code.
That is why BTP matters. It gives companies a place to extend, integrate, and innovate without putting all custom logic directly inside the ERP core.

#### Specific-level details:
1. Application Development:
- SAP Build Work Zone: business sites/workspaces
- SAP Build Apps: low-code/no-code apps
- SAP Build Code: pro-code development using ABAP Cloud and CAP

2. Automation:
- SAP Build Process Automation: workflows and automation

3. Data & Analytics
- SAP HANA Cloud: database as a service and persistence
- SAP Business Data Cloud: harmonized business data foundation
- SAP Master Data Governance: consistent master data

4. AI
- AI Services: ready-to-use AI capabilities
- SAP AI Core and SAP AI Launchpad: AI lifecycle/development tools
- Generative AI Hub: access and management for generative AI use cases

---

## SAP BTP Account Model Setup
**1. GlobalAccount:** A representation of your contractual agreement with SAP. Dont actually build anything on this level, you administer form here.

**2. Subaccounts:** Hold together your applications, services, and subscriptions and allow you to organize and structure your global account. The actual work is done on this level.

**3. Region:** Represents a geographical location where application, data, or services are hosted. Third-party cloud providers usually, operate the infrastructure layer of the regions, whereas SAP operates the platform layer. 

**4. Directory:** Optional grouping for subaccounts

**5. Environment:** Runtime inside a subaccount, such as Cloud Foundry, Kyma, etc.

Example:

Global Account
  -> Directory: Americas
    -> Subaccount: Sales Dev
    -> Subaccount: Sales Prod
  -> Directory: Europe
    -> Subaccount: Operations Dev
    -> Subaccount: Operations Prod

Check out this picture for an actual example of a SAP BTP Account Model setup:
![SAP BTP Account Model Example](sap-btp-solutions-architect\docs\sap-btp-account-model.png)
![SAP BTP Account Model Example-1](sap-btp-solutions-architect\docs\development-env-account-model.png)

- So we can also simulate normal SWE development enviornments with subaccounts, such as having one subaccount for DEV, TEST, and PROD.

### Common Patterns to set up accounts:
| Pattern | When It Helps |
|---|---|
| By environment: Dev/Test/Prod | Basic software lifecycle separation |
| By region: Americas/Europe/APAC | Regional governance, data residency, local teams |
| By business function: Sales/Ops/Finance | Department ownership and cost tracking |
| By project | Project isolation and separate development work |
| By division plus lifecycle | Large enterprises with many teams and products |

---

#### SAP BTP Cockpit
- The cockpit is the central tool for operations including adminstration and development.

#### Additional SAP BTP Terminology
**- Entitlement:** Means you are allowed to use a specific SAP BTP service or service plan.
**- Quote:** A quote means how much of it you are allowed to use.

**- Service =** SAP HANA Cloud
**- Service plan =** Free plan, standard plan, pro plan


**Subscription vs Service Instance**
- Some BTP services are conumsed through a subscription. For example the admin subscribes once, and users access the service through a shared URL.
- Other services are consumed through service instance, for example a SAP HANA Cloud datbaase instance --> Its a technical resouce that an app can bind to.

**Service Keys and Bindings**
- If an application needs to use a service instance, it needs connection details and credentials. This is where service keys and bindings come in.

Create service instance
  -> create service key or binding
    -> application receives credentials/configuration
      -> application consumes the service

- This explains how an app actually uses BTP services, it isnt magic, the app gets bound to a service instance. 

---

## Summary
Global account = what the company bought

Directory = how the company organizes teams or areas

Subaccount = where actual project work happens

Environment = where applications run

Service entitlement/quota = what the subaccount is allowed to use

Subscription or service instance = how the service is actually consumed

Application = the thing you build that uses those services