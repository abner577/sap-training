## Lesson 4: Understanding SAP Reference Business Architecture
Covers:
- SAP Reference Architecture Content Framework
- Business Capability & Business Process Model
- Solution Capability & Solution Process Model 

- SAP Reference Business Architecutre is basically SAPs prebuild map of how a company works and which SAP solutions can support that work. It helps architects avoid starting from a blank page. 

We can think of it in 3 connected maps:
| Layer | Simple Meaning | Example |
|---|---|---|
| Business Capability Model | What the business must be able to do | Manage customer orders |
| Business Process Model | How the business does it step by step | Receive order, check inventory, ship goods, invoice customer |
| Solution Architecture | Which systems/software support it | SAP S/4HANA Sales, SAP BTP Integration Suite, SAP Build Process Automation |

### SAP Reference Architecture Content Framework
Lets break this phrase down:

- SAP --> The vendor providing the solution
- Reference --> A reusuable starting point
- Architecture --> A structured view of business
- Content --> The actual maps and diagrams
- Framework --> The organizing structure

SAP Reference Architeture Content Framework = SAPs reusuable library of business and solution maps that helps architects connect business needs to SAP solution. Its not like an application so to say its more like an architecture guidebook and mapping systems.

### Business Capability Model
- A business capability = Something the organization must be able to do to create value. For example such as: Manage inventory, manage customer orders, etc. 
A business capability is about what, not how. For example if we have a business capability to manage customer order, that doesnt yet say whether the order comes from a website, mobile app, or call center --> It just states the business need. It only covers the "what" not the "how"

#### Business Domain and Hierarchy
Business Domain
  -> Business Area
    -> Business Capability

Example:
Customer
  -> Sales
    -> Manage customer orders

- The point is organization, SAP is saying: "Lets not throw 500 business capabilities into a random list lets group them logically." This is what it referes to that the Business Capability Model is organized by: Business Domain --> Business Area --> Business Capabilitiy. 

### Business 