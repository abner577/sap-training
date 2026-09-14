# What are the major parts of BTP?
- There are usually 5 big capability areas

### 1. Application Development and Automation
- This answers: "How do we build something new?" --> Supposed SAP gives you 95% of what your company needs, but your company needs a custom application for the remaining 5% --> We can use BTP to build that application

For example:
Custom Customer Dispute Portal
            │
            ▼
        SAP BTP
            │
          APIs
            │
            ▼
      SAP BRIM / FI-CA

- The user interacts with your custom app, the app calls SAP APIs behind the scenes. 

#### Clean core philosophy
- SAP encourages to avoid dumping huge amounts of custom code directly inside the ERP core.

OLD APPROACH

S/4HANA
 ├── SAP code
 ├── custom code
 ├── more custom code
 ├── modifications
 ├── company-specific logic
 └── even more modifications

 NEW APPROACH
    BTP
Custom extensions
    │
    │ APIs/events
    ▼
S/4HANA
relatively clean

- BTP solution architect material describes BTP as a platform for extending, integrating, and analyzing processes without disrupting the core ERP system.

---

### 2. Integration
- This answers: "How do all our systems communicate?" --> One of the biggest BTP offerings here is SAP Integration Suite.

So image your existing architecture has a bunch of different componenets such as:
- Salesforce, Telecom network, custom portal, bank info, etc.

- Now there lies the question how can we connect/combined this information, and that is what Integration Suite does.

SAP BRIM
   │
   │
   ▼
Integration Suite
   │
   ├──────── Salesforce
   │
   ├──────── Bank
   │
   ├──────── Telecom network
   │
   └──────── Custom billing portal


*Is it specifically for integrating with existing SAP services like BRIM? Or for just connecting diff parts of our buisness (i.e. diff apps) together? Is the integration suite specifically for this or are there other parts for Integration that arent Integration Suite?*

---

### 3. Data & Analytics
- This answers: "How do we collect, organize, understand, and analyze all the company's data?"

- Imagine a company wants one dashboard containing:
Subscriber data       → CRM
Billing data          → BRIM
Payment data          → FI-CA
Network usage         → Telecom systems
Marketing data        → Salesforce
Financial data        → S/4HANA

- BTP-related data technologies can help companies bring data together, model it, analyze it, and expose useful information.

It includes technologies such as:
- SAP HANA Cloud, SAP Analytics Cloud.

---

### 4. Artificial Intelligence
- THis answers: "How do we add AI to business processes"

- BTP provides AI capabilities intended specifically for SAP scenarios, including building AI apps and agents that can connect to business processes and SAP data.

Where technologies like the following are included:
- SAP AI Core and Joule

---

### 5. Foundation Services
- These are the things that make everything above manageable. 

It answers questions like:
- Who is allowed to access this application?
- Where is the app running?
- How do we authenticate users?
- How do we monitor it?
- How do we store credentials?
- How do we manage permissions?
- How do we deploy it?

This includes areas such as:
- identity, authorization, security, connectivity, monitoring, lifecycle management

SAP describes these core capabilities as providing things such as application lifecycle management, security, interoperability, and administration/operations.