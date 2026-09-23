## Exploring AI Capabilities Across SAP BTP
- This lesson is showing that AI in SAP BTP isnt only Joule, AI also appears inside multiple BTP capability areas. This lesson connects SAP AI strategy back to the BTP pillars you already studied. 

**Mental Model**
SAP BTP
|
|-- Application Development and Automation
|     |-- Joule for Developers
|     |-- SAP Build AI capabilities
|     |-- ABAP AI capabilities
|
|-- Data and Analytics
|     |-- SAP Analytics Cloud smart features
|     |-- Just Ask + Joule
|     |-- HANA Cloud Vector Engine
|
|-- Integration
      |-- Integration Advisor
      |-- GenAI-based iFlow generation


- The main idea is that SAP BTP AI isnt just one isolated componenet, it appears in different places depending on the Job.

- A developer uses it to generate code and tets, a business analyst uses it t find insights, etc.

### Application Developmennt and Automation AI
- This section focuses on *Joule for Developers*. This means that there are AI capabilities are built into SAP development tools, across SAP Build. For example for SAP Build Apps which is the low-code platform it can generate pages and sample data, and for SAP Build Code it can generate unit tests and elements. 


### Data and Analytics AI
- This section focuses mainly on SAP Analytics Cloud (SAC) --> SAC uses AI for augmented analytics --> Meaning that AI helps business users analyze data and find patterns and provide better analytics.

SAC AI can do things like -->

1. Automatically analyze data and find key influencers and patterns
2. Let business users create predictive models without code and user forcasting to helps with budgets and future proejcts, etc.


### RAG and HANA Cloud Vector Engine
- RAG means the AI retrieves relevant information first, then uses that information to generate the answer. 

Step by step:
1. User asks a question.
2. The question is converted into a searchable representation.
3. The system retrieves relevant enterprise data or documents.
4. The retrieved context is passed to the AI model.
5. The model generates an answer based on that context.

- SAP HANA Cloud Vector Engine supports use cases like RAG and semantic search --> The key concept in this is **vector embedding**. What a vector embedding is just a numerical representation of meaning for a word.

### Integration AI Capabilities 
- This section connects AI to SAP Integration Suite. The lesson focuses on two main AI-related integration capabilities.

1. Integration Advisor --> Helps define and map structures intelligently
2. GenAI iFlow generation --> Creates draft integration flows from natural language prompts

**Integration Advisor:**
Integration Advisor helps with one of the hardest parts of integration: mapping data between systems.

Example problem:

One system says --> customer_ID. Another says --> cust_num. Another says --> clientIdentifier

- A basic tool may not know these are related. Integration Advisor can use semantic understanding and learned patterns to suggest mappings.

**GenAI-Based iFlow Generation**
- An iFlow defines how data moves from one system to another, it defines things like the source system, rules for changing formats and mapping fields, defines the target system, and error handling.

- With iFlow generation a developer can describes what they need from an iFlow and then the AI can generate a draft iFlow with all this.

---

## AI Foundation
- This lesson explains AI Foundation. So it really explores the platform capabilities that SAP provides so companies can build and operate AI. So AI Foundation is the technical foundation on SAP BTP that supports AI development. 

- AI Foundation is the layer of BTP that makes enterprise AI usable, and connected to business sytems. 

**Main AI Foundation Components**
1. Unified AI Portal
- Central entry point for AI Foundation tools and services. Its like the front door for accessing AI capabilities on BTP. Should use skills for specific smaller problems and a whole other custom AI agent for complex goals that have many workflows.

2. Joule Studio
- Low-code/no-code env for extending Joule with skills and agents.
- This is where we extend the base Joule copilot --> So we can add skills and agents to Joule. 

3. Generative AI Hub
- Access and point for diff LLMs. Is the central place for accessing and using LLMs.

4. SAP AI Core / AI Launchpad
- Lifecycle, training, and operations capabilities

5. SAP Knowledge Graph
- Grounds AI in relationships among business objects. For example:

Customer
  placed
Sales Order
  contains
Product
  sourced from
Supplier
  affected by
Shipping Delay

Or better seen like:

Customer places sales Order --> Sales Order contains products --> Products are sourced from Supplier

- And then SAP Foundation Model is presented as helping AI work better with SAP business data, especially structure business data from enterprise systems. 

6. SAP Foundation Model
- Helps AI work with SAP business data and structured enterprise context.