# DecisionThread

DecisionThread is an AI-augmented wealth-advisory workbench that keeps client opportunity, product decisions, portfolio consequences, and execution context connected.

Built primarily for **bank wealth advisors and relationship managers (RMs)**.

[Case Study](https://yucheng-chang-yc.github.io/decisionthread/) · [Live Demo](https://yucheng-chang-yc.github.io/decisionthread/demo/)

## What works

- **Opportunity radar:** surfaces clients who may need attention based on events, cash, maturities, allocation, and bank signals.
- **Client context:** keeps holdings, objectives, events, and the reason to engage visible in one workflow.
- **AI-assisted meeting context:** scripted conversation signals can update meeting preparation and advisor attention without overwriting governed financial facts.
- **PIW-governed commercial product prioritisation:** combines the eligible product universe with client relevance, portfolio context, and explicit bank priorities.
- **Proposal and whole-portfolio consequence:** turns product, amount, account, and funding source into a proposed portfolio so trade-offs are visible before action.
- **Heterogeneous product treatment:** uses evidence suited to each product family rather than forcing funds, structured products, deposits, and insurance into one analytical model.
- **Execution handoff:** carries proposal identity, rationale, and decision state toward downstream suitability and transaction review.

## Key design decisions

- Treat commercial intent as a legitimate, visible input—but never as a route around client eligibility.
- Use PIW as a governed boundary, not as a complete personalisation model.
- Let AI interpret and update context while authoritative financial state and calculations remain deterministic.
- Judge a recommendation by its whole-portfolio effect, including adverse trade-offs, rather than by isolated product fit.
- Separate advisor-facing product language from the analytical treatment required by each product type.
- Preserve decision context across system boundaries instead of implying autonomous advice or execution.

## Prototype scope

This repository is a functional interaction and decision-architecture prototype, not a production banking system.

- Client and product data are synthetic.
- The AI runtime and conversational inputs are scripted or simulated.
- Enterprise data, suitability, order-management, and other downstream integrations are simulated at their handoff boundaries.
- The prototype demonstrates workflows and decision logic; it does not report measured production, client, or commercial outcomes.

## Repository structure

```text
.
|-- index.html                 # Case study
|-- demo/
|   `-- index.html             # Interactive prototype
|-- assets/
|   |-- screenshots/           # Product evidence
|   `-- clips/                 # Reserved for captured clips
|-- tools/
|   `-- capture-demo.mjs       # Demo screenshot capture
|-- .gitignore
`-- README.md
```

## Run locally

No build step is required. Open [index.html](index.html) for the case study and [demo/index.html](demo/index.html) for the live prototype in a modern browser.

Capture helpers can be run with Node.js:

```powershell
node tools/capture-demo.mjs
```

`capture-demo.mjs` is included.

## Evidence screenshots

- [Advisor workspace and opportunity radar](assets/screenshots/01_workspace_clean.png)
- [AI context update](assets/screenshots/02_ai_context_update.png)
- [AI-assisted meeting preparation](assets/screenshots/02b_ai_meeting_prep.png)
- [Governed product decision](assets/screenshots/03_governed_product_decision.png)
- [Whole-portfolio consequence](assets/screenshots/04_portfolio_consequence.png)
- [Execution handoff](assets/screenshots/05_execution_handoff.png)
- [Product campaign routing](assets/screenshots/06_product_campaign.png)
