# The actual BTP environment
- Eventually we will log into something called the SAP BTP Cockpit, we can think of it like as a control center. A companys BTP landscape could be organized roughly like:

Company
│
└── GLOBAL ACCOUNT
      │
      ├── Subaccount: Development
      │       │
      │       ├── Applications
      │       ├── Services
      │       └── Runtime
      │
      ├── Subaccount: Testing
      │
      │
      └── Subaccount: Production

- A global-account is the top-level account representing the organizations BTP resources, inside of it are subaccounts.
- Subaccounts are where applications are deployed, services are used, subscriptions are managed, etc. Each subaccount also belongs to a specific gepgraphic region. 

---

## Cloud Foundry & Kyma
- These are runtime environments where application can actually run.

#### Cloud Foundry
- A managed platform for deploying applications written in various languages
SAP BTP
   ↓
Cloud Foundry
   ↓
Your running Java application

#### Kyma
- Kyma is based on kubernetes, so if a company wants a more container-oriented architeccture. 



