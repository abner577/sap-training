## Exploring Data and Analytics Services
- The main point of this lesson is that SAP BTPs data and analytics services help companies turn scattered data into buisness-meaningful insights. It isnt just about storing the data its about organizing it and making it usable for decisions.

- In a real organization data about different aspects of your company will be stored in different places such as Ariba or SuccessFactors right so the problem is how we organize and get all this data connected while still remaining secure.

### Core concepts/terminology
1. Data warehouse
- A data warehouse is a structured, repository for reporting and business intelligence. Think things like finance reports, dashboards, sales performance, operational KPIs. The data is usually cleaned and transformed before being loaded.

2. Data lake
- A data lake stores raw or semi-raw data, including structured, semi-structured, and unstructed data. 

3. Data fabric
- A data fabric is a architecture layer that connects, manages, and exposes data across different systems. Meant to provide a unified way to access enterprise data.

4. Data mesh
- Instead of one central data team owning everything, business domains own their own data products. For example, sales owns sales-order data, HR owns workforce data, and so on.

5. Data product
- Its a reusuable and trustworthy data asset. It isnt just the raw data table, it includes the data, transformation logic, metadata, ownership and access rules.

---

### The main SAP Tools around this:
| Tool | What It Is | Main Role |
|---|---|---|
| **SAP HANA Cloud** | Cloud database-as-a-service | Stores and processes application or analytical data |
| **SAP Datasphere** | Business data fabric and data warehouse service | Integrates, models, virtualizes, catalogs, and exposes business data |
| **SAP Master Data Integration** | Master data replication hub | Helps SAP apps share consistent master data |
| **SAP Master Data Governance, cloud edition** | Master data governance application/service | Cleanses, governs, consolidates, and improves master data quality |
| **SAP Analytics Cloud** | Analytics, planning, BI, and predictive SaaS | Builds dashboards, stories, planning models, and analysis experiences |


**1. SAP HANA Cloud**
- Its the database layer, its a managed cloud database service that can support workloads. Can just think about it like a normal db.

**2. SAP Datasphere**
- It helps data professionals access and distribute data from SAP and non-SAP systems while preserving business context. Datasphere is about making data usable as meaningful business objects and analytical models.

*Semantically = Relating to the meaning or words, language, or other symbols*

Capabilities:
- Connect to SAP and non-SAP data sources, model data semantically, so consumers understand business meaning (i.e. becomes business-friendly and ready for consumption.)

**3. SAP Master Data Integration and SAP MDG**
- MD is the stable business data used across processes. THe problem is that many applications need the same master data. SAP Master Data Integration helps applications share master data through a pattern. Instead of every application mapping directly to every other application. They communicate through a common model, the SAP One Domain Model

4. SAP Analytics Cloud (SAC)
- Is where users consume and interact with data through analytics and dashboards. 
- It has analytics applications, planning capabilities, and data analyzing capabilitites. 

- Its the front-end experience for analyzing, planning, and explaining business data. \

---

## Exploring SAP Business Data Cloud (BDC)
The main point of this lesson is: 
- SAP Business Data Cloud is SAPs newer, higher-level data and analytics offering that brings together data products, Datasphere, Analytics Cloud, Databricks, and AI into a managed business data fabric. 

- Last lesson introduced different parts of this capability of BTP such as: data fabric, data products, SAP Datasphere AP Analytics Cloud, SAP HANA Cloud, MDG, and so on. This lesson is saying: SAP Business Data Cloud packages several of those ideas into one product.

- The role of SAP Business Data Cloud is not to simply be another dashboarding tool, its a platform intended to give companies a trusted, business-aware data foundation.

**The main problems BDC solves**
Many companies have data spread across:
- SAP systems, non-SAP systems, cloud data lakes, on-premises database, etc. 

- The main aching point isnt just that the data is scattered, the bigger problem is that the data often lacks a shared business meaning. For example, diff teams may define diff terms like performance and revenue differently. --> These diff teams then pull data from diff places like S/4HANA, spreadsheets, etc.

- BDC tries to solve this by creating a more unififed governed and semantically rich data foundatio.

### Layered Mental Model
| Layer | Plain Meaning |
|---|---|
| **Source Systems Layer** | Where the original data lives |
| **Data Products Layer** | Curated, governed, API-accessible business data assets |
| **Business Data Fabric Layer** | Tools that model, analyze, engineer, govern, and use the data |
| **Intelligent Applications Layer** | Managed AI-powered business apps built on top of curated data |