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