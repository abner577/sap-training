## Describing SAPs AI Strategy
- This lesson introduces SAPs AI strategy, where SAP is promoting their SAP Business AI. SAP Business AI means an AI that understand business context, works inside SAP-managed systems, and helps users act more effectively.

**The three big SAP AI Building Blocks**
| Concept | What It Is | Architect Mental Model |
|---|---|---|
| **Joule & Joule Agents** | SAP’s generative AI copilot and agent layer | The user-facing AI assistant that can answer, recommend, and sometimes act |
| **Embedded AI** | AI built directly into SAP applications | AI inside the business process, often without the user prompting it |
| **AI Foundation on SAP BTP** | Technical services and platform capabilities for AI | The foundation used to build, extend, govern, and consume AI capabilities |

The distinction is important:
- If for example an employee asks to show some overdue charges, that is closer to Joule as an **assistive AI**

- Then if an AI agent finds the overdue receivables, checks the historys and triggers next steps, this is closer to **agentic AI.**

- Then if SuccessFactors automatically recommends training paths during onboarding, that is **embedded AI.**

---

## Exploring Joule and Joule Agents
- This lesson explains how SAPs AI strategy becomes visible to users through Joule and becomes more action-oriented through Joule Agents. 

- Joule helps users ask, understand, navigate, and perform tasks using natural language. Joule Agents go further by planning and executing multi-step work toward a business goal.

- Joule is SAPs generative AI copilot, its embedded across a bunch of SAP products. Its value comes from being connected to a business context. That means that Joule can understand the context of different things like:

1. The User Role
- Joule understands that you are a sales manager or a developer and gets specific help for that

2. Company data
- Joule can understand SAP system data

3. Business process
- Joule understands workflows like onboards or purchase orders. 

**Joules capabilities:**
- So since Joule is a copilot it can do many things, it can help you navigate somehwere in your SAP system, it can give you information like the status of an order, it can be transactional so it can help you execute something like creating an order, it can also explain a concept to you like a normal chatbot would. All while being grounded in business context and having business information.

### Joule vs Joule Agents
- Joule by itself is mostly a copilot. It helps users ask questions, navigate, generate content, summarize information, and perform certain tasks.
- Joule Agents is closer to Agentic AI. Meaning that AI can pursue a goal by planning steps, selecting tools, executing actions, and adapting if needed.

**Comparison Table**
| Joule | Joule Agents |
|---|---|
| Copilot | Goal-oriented agent |
| Responds to user prompts | Can plan multi-step tasks |
| Helps retrieve, summarize, navigate, transact | Can coordinate work across systems |
| More assistive | More autonomous |
| Usually one interaction at a time | Can manage a broader workflow |
