## Exploring SAP BTP Commercial Models and Estimating Costs
- This lession is about how an SAP BTP Solution Architect thinks about cost before recommending an architecture.

The architect asks himself the question: "For this business use case, which BTP services do we need, how predictable is the usage, and which commericla model gives the company the right balance of fleixbility and cost?"

### Diff types of commercial models

**Commercial Models**
- A commercial model is the way a company pays for and is allowed to consume SAP BTP services. 

1. Trial Account
- Not meant for production, limited usage and restraints.

2. Free Tier
- Selected BTP services have a free service plan inside an enterprise account. That matters because an enterprise account is closer to the real production structure. In many cases, you can test a service on a free plan and later move to a paid plan.

3. Pay-As-You-Go
- A consumption-based model with low commitment.
- The company pays based on what it actually uses. Useful when the company is still experimenting and doesnt yet know which services it will use long-term. Good for things like POCs.

4. Consumption-Based Agreements: CPEA / SAP BTPEA
- These are also consumoption-based, but with more enterprise commitment. The company commits to cloud credits, as services are consumed, usage is deducted from that balance. 

5. Subscription
- This is more fixed, The company subscribes to specific BTP services at a fixed cost for a contract period. This can be commercially favorable, but it is less flexible because the company is committing to specific services.

### Cost Estimation
- The architect shouldnt estimate cost by randomly picking services. The proper flow is:

1. Understand the business use case.
2. Identify the required BTP capabilities.
3. Create or review the solution diagram.
4. Identify the actual BTP services needed.
5. Build a software bill of materials.
6. Estimate usage for each service.
7. Use the SAP Discovery Center estimator.

- A software bill of materials (SBOM) is basically the list of technical componenets required for the solution.

SBOM might include things like:
- SAP Build Code for development
- Cloud Foundry Runtime for hosting
- SAP HANA Cloud for persistence
- etc.