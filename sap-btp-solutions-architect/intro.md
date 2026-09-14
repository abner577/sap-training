## What is SAP BTP
- It is the technology platform that sits around your core business sytems and gives you tools to connect them, extend them, build new application, automatite processes and etc.

## Where does SAP BTP fits into the SAP world?
- So we can think about it like the main product/thing that performs the main SAP goal which is to connect diff parts of your business (i.e. diff applications) and then provides extra stuff on top of that.

Imagine a company has:
Salesforce
    │
SAP S/4HANA ───── SAP BRIM
    │                 │
SuccessFactors        │
    │                 │
External banking APIs │
    │                 │
Custom applications   │

- A company asks the questions: "How do all of these systems talk to each other? How do I automate a process that crosses 3 systems? How do I combine data from multiple systems for analytics"

Therefore the architecture starts looking more like this:
                 USERS
                   │
                   ▼
       ┌────────────────────────┐
       │        SAP BTP         │
       │                        │
       │  Apps / Extensions     │
       │  Integration           │
       │  Automation            │
       │  Data / Analytics      │
       │  AI                    │
       │  Security / Identity   │
       └────────────────────────┘
          │       │       │
          ▼       ▼       ▼

      S/4HANA    BRIM   Salesforce
          │               │
          ▼               ▼
       Other SAP       Non-SAP
        systems         systems

- S/4HANA = system that run the business
- BTP = A platform you can use to connect, extend, autoamte, analyze and innovate around these systems.

## Is SAP BTP a cloud platform?
- SAP operates the BTP platform layer, while the underlying infrastructure usually comes from one of the big cloud providers. So behind the scenes they are still using the cloud providers and we are accessing their resources through BTP.

- We can roughly think of BTP as sitting mostly like PaaS --> We arent really worrying about: "What physical server is this running on?"

- Instead we are saying: "I need a database, I need a runtime, I need auth, etc."

---

## What exactly is a Solution Architect?
- A software developers often thinks like: "How do I build this component?"

- A solution architect thinks like: "What combination of systems, technologies, integrations and design choices should we use to solve the enter business problem". They operate at a higher level making planning documents and making the system design and high-level decisions. 

A solution architect basically designs the blueprint --> They dont need to manually do the work such as hand-build out the APIs --> But they need to understand these underlying technical systems well enough to decide things like:
- Where should everything go? How should everything connect? Is it scalable? How much will it cost? etc.


## So what exactly is an SAP BTP Solution Architect?
- An SAP BTP Solution Architect gets a business problem and figures out: "How should we use SAP BTP and the surronding landscape to solve it?"


## Concrete Example:
- Lets say that you are working for a telecom company that uses SAP BRIM and they already have things like:

- Network usage, Convergent Mediation, Charging, CI, FI-CA,

Now this company says we want:
- We want customers to open our mobile application, see unusually high charges, request an explanation, dispute the charge, and have AI categorize the dispute before sending it to the appropriate billing team.

- This cant just be solved with BRIM, we now need a full solution so a Solutions Architect may come up with the architecture in order to solve this problem and that may look something like:

                      MOBILE APP
                          │
                          ▼
                   Custom API/App
                     on SAP BTP
                          │
           ┌──────────────┼─────────────┐
           │              │             │
           ▼              ▼             ▼
     Authentication      AI        Automation
           │              │             │
           └──────────────┼─────────────┘
                          │
                          ▼
                 Integration Suite
                          │
            ┌─────────────┼──────────────┐
            ▼             ▼              ▼
          FI-CA      Convergent      CRM / Other
                     Invoicing         Systems


- And we can note that BTP is now doing several jobs:

1. Application Development
- It gave the team the ability to build their custom solution and host it.

2. Integration
- Enables communication of all this with other SAP systems?

*So is it like you build a custom app and through Integraiton Suite it enables comm. between that app and other SAP systems? Or can we also enable communicate between our already existing apps & external apps and SAP systems? Also enable communication between our already apps between each other, is this another aspect another part that isnt integration suite?*

---

## Summary
- Dont think of BTP as one giant application like S/4HANA. Its closer to a collection of services and development capabilities under a common platform.

For example:
SAP BTP
│
├── Build something
│     └── Application development
│
├── Connect something
│     └── Integration Suite
│
├── Automate something
│     └── SAP Build / automation
│
├── Analyze something
│     └── Data & analytics
│
├── Make something intelligent
│     └── AI
│
└── Operate all of it safely
      └── Security / identity / monitoring / platform services