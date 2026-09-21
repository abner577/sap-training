## Exploring Data and Analytics Services
- The main point of this lesson is that SAP BTPs dat and analytics services help companies turn scattered data into buisness-meaningful insights. It isnt just about storing the data its about organizing it and making it usable for decisions.

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
- MD is the stable business data used across processes. THe problem is that many applications need the same master data. SAP Master Data Integration gelps applications share master data through a pattern. Instead of every application mapping directly to every other application. They communicate through a common model, the SAP One Domain Model

4. SAP Analytics Cloud (SAC)
- Is where users consume and interact with data through analytics and dashboards. 
- It has analytics applications, planning capabilities, and data analyzing capabilitites. 

- Its the front-end experience for analyzing, planning, and explaining business data. 