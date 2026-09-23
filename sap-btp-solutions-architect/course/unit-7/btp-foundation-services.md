## SAP BTP Foundation Services
First we will explore exactly what is meant by Foundation Services:
- Foundation services are the essentual capabilities that support the entire platform. They provide the security and stabilitiy for all other SAP BTPO setvices and custom applications to run. 

For example before you BTP can custom applications made with BTP can work safely and correctly, it needs essential things like: auth, autho, connectivity, logging, alerting

- All these capabilities are provided through SAP BTP Foundation Services. They are the shared platform services that make BTP applications and other BTP services secure and reliable. 

---

- So the main point of this lesson is that Foundation services help everything else run properly by answering questions like:

- How do users log in?
- How does a cloud app reach an on-premise ERP?
- Where are logs stored?
- How do I schedule background jobs?
- How do I store files?
- How do I monitor usage?
- How do I manage compliance and retention?

- And Foundation Services cut across the rest of BTP these essential services are found throughout all the different sections of BTP. They are called "foundation" beacuse many solution depend on them, even when they arent the main business feature. 

- The lesson groups foundation services into these categories:
| Category | What It Means |
|---|---|
| Runtimes and lifecycle | Run apps, manage deployment, logs, jobs, transports |
| Security and compliance | Identity, login, authorization, audit, retention |
| Persistency | Store data, files, cache, or application state |
| Connectivity | Securely connect BTP apps to SAP/non-SAP, cloud/on-prem systems |
| Administration and operations | Monitor, alert, track usage, operate the platform |


**1. Runtimes And Application Lifecycle**
This area incldues things that help applications run and be managed. This lesson adds some exmaples like:
- SAP Cloud Logging Service (pretty straightforward)
- SAP Job Scheduling Service --> Runs background jobs on a schedule, this can include recurring jobs, one-time jobs and retry handling. 

**2. Security & Compliance**
- This section focuses on SAP Cloud Identity Service (CIS) --> Is a bundle of identity-related services --> It helsps secure SAP BTP itself and applications built on BTP. 

**3, Identity Authentication Service (IAS)**
- IAS is the front door it handles:

| Function | Meaning |
|---|---|
| Login | User proves identity |
| SSO | User logs in once and accesses multiple apps |
| MFA | Second factor for stronger security |
| Federation | Connects to corporate identity providers like Microsoft Entra ID/Azure AD or Okta |
| Branding | Company-specific login screen |

**4. Administration & Operations**
- This lesson highlights two key services:

1. SAP Alert Notification Service --> Sends alerts when important events/failures happen
2. SAP Usage Data Management Service --> Tracks usage for reporting, planning, billing, auditing. 