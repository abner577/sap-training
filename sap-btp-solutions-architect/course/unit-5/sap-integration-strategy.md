## Describing SAPs Integration Strategy
- SAP Integration isnt just about connecting 2 systems its the discipline of designing how business processes and governance work and communicate across an enterprise landscape.

A solution architect needs to answer questions like:
- How do SAP and non-SAP systems exchange data, which systems own a specific business transactions, should this comm, be API-based, event driven, file-based?

- The target model is an Integration Center of Excellence or CoE. A Coe is the operation model that defines reusuable patterns for approved APIs, integration standards, security rules, monitoring practices, etc.

### The 5 main architecture principles to keep in mind:
| Imperative | Plain meaning |
|---|---|
| The platform matters | Use a common integration platform instead of scattered custom tools. |
| Agility and scalability | Build repeatable integration patterns that can evolve as systems change. |
| Citizen integrator | Some simpler integrations should be possible for business-oriented users with guided tools. |
| Strong governance | Control access, credentials, encryption, change management, and standards. |
| Reporting and analytics | Monitor integration behavior, failures, performance, and trends. |

---

### Sap Integration Suite
- Integration Suite is the central BTP service family for integration. Its job is to connect applications and data between diff applications. 

SAPs Integration Suite is surronded by 4 main ideas:

1. Predefined Integration Content --> SAP provides reusuable APIs, event, and integration flows so teams dont need to start from 0
2. Open integration --> SAP systems can integrate with non-SAP systems using normal REST apis and connectors.
3. Holistic integration --> Integration includes many diff types of integration and comm. Not just one style of connection
4. AI-assisted integration --> AI can help with mapping, testing, anomaly detection, and reducing manual integration effort.

---

| Tool | Main responsibility |
|---|---|
| Cloud Integration Automation Service | Guided setup and technical configuration |
| SAP Cloud Integration | Runtime execution of integration flows |
| SAP Cloud Connector | Secure tunnel/access path from BTP to selected on-premise systems |
| SAP Cloud ALM / Focused Run / Solution Manager | Monitoring and operations |

---

### Monitoring Toolchain
- The final section: Reporting and analytics is important because business failures are to be taken seriously. This lesson compare three SAP monitoring/operations tools:

| Tool | Best mental model |
|---|---|
| SAP Solution Manager | Traditional ALM and monitoring, especially strong in on-premise and hybrid SAP landscapes. |
| SAP Focused Run | High-volume, advanced monitoring for large and complex landscapes. |
| SAP Cloud ALM | Cloud-native ALM and operations tool, especially relevant for cloud-centric and hybrid SAP landscapes. |

---

## SAP Integration Suite
- The previous lesson mainly explained why enterprises need a integration strategy, this lesson focuses on the SAP tools that support that strategy and explains what each one does. 

**Core capabilities of SAP Integration Suite**
| Capability | Practical purpose |
|---|---|
| Cloud Integration | Build and run integration flows, or iFlows, that move and transform messages between systems. |
| API Management | Expose, secure, monitor, govern, and publish APIs. |
| Open Connectors | Connect more easily to many non-SAP SaaS applications through prebuilt connectors and unified APIs. |
| Integration Assessment | Help architects choose the right integration approach using SAP’s Integration Solution Advisory Methodology. |
| Migration Assessment | Analyze old SAP PI/PO scenarios and estimate migration effort to SAP Integration Suite. |
| Integration Advisor | Help design message structures and mappings, especially for B2B/A2A scenarios, using SAP knowledge and machine learning. |
| Event Mesh / Advanced Event Mesh | Support event-driven architecture, where systems react to business events asynchronously. |
| SAP Application Interface Framework | Helps monitor and correct interface messages from within S/4HANA, especially for business users. |


**1. Cloud Integration**
- This is the heart of many Integration Suite scenarios, it uses what we call **iFlows**. An iFlow describes:
- Who sends the message, who receives the message, how the message is transformed, how routing decisions happen, whether encryption ot security steps are applied, how errors are handled. 

- An important concepts are adapters which decide which communication protocols Cloud will use when implementng these integrations such as:
- REST, SOAP, ODATA, SFTP, etc.

- The adapter decides how Cloud integration talks to a system. The iFlow decides what happens to the message once it is inside the integration process. 

**2. API Management**
- API Management governs access to APIs, it helps with API security, auth and autho, rate limiting, monitoring API usage, etc.

**3. Open connectors**
- Open connectors help connect to third-party SaaS systems. The key value that this brings is normalization. Instead of every developer learning the unique API style of each SaaS product, Open Connectors provides prebuilt connectors and a more consistent API pattern. 

**4. Integration and Migration Assesment**
| Tool | Question it answers |
|---|---|
| Integration Assessment | “For this new integration scenario, what integration style and technology should we use?” |
| Migration Assessment | “For this old integration, how hard will it be to move it to SAP Integration Suite?” |

**5. Integration Advisor**
- Integration Advisor is mainly about reducing the pain of message definitions and mappings. Some important terms to know are:

| Term | Meaning |
|---|---|
| Type system | A standard message family, such as IDoc, ASC X12, EDIFACT, etc. |
| MIG | Message Implementation Guideline. Defines the customized message structure needed for a scenario. |
| MAG | Mapping Guideline. Defines how one message structure maps to another. |

- In simpel terms, Integration Advisor helps you define what the message should look like and how fields should map between systems.

**6. Event Mesh**
- This section introduces event-driven architecutre. We know that this means that we dont just answer to an API call instead we respond to an event such as a sales order being created or a payment being received (like Kafka for ex.)

- SAP Event Mesh is the more standard BTP event broker. 