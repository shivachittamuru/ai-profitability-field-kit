# AI Profitability Field Kit

AI adoption increasingly raises a practical business question:

> **Can we demonstrate that the economic value created by AI justifies the resources invested in it?**

The AI Profitability Field Kit helps Microsoft practitioners and partners connect AI investment to **Accepted Work, business outcomes, economic value, evidence, and action**.

The goal is to make AI profitability conversations **simple, confident, repeatable, and adaptable** across partner types and AI use cases.

---

## A simple way to frame the conversation

The field kit starts with the work, not the technology:

```text
WORK
What work are we trying to accomplish?

        ↓

MEASURE
What did it consume, and how much Accepted Work did it produce?

        ↓

OUTCOME
What changed?

        ↓

VALUE
What was that change worth, and how credible is the claim?

        ↓

ACTION
What should we do next?
```

**Accepted Work** means AI-assisted work that meets the acceptance criteria required for the job being performed.

AI activity becomes economically meaningful only when it produces work that is actually acceptable for its intended purpose.

---

## Start here

### New to the approach?
→ [AI Profitability POV](docs/pov/ai-profitability-pov.md)

Understand the core perspective and principles.

### Running a partner conversation?
→ [Partner Playbook](docs/playbook/partner-playbook.md)

Use a repeatable structure to move from the partner's business question to an evidence-backed next action.

### Looking for your scenario?
→ [Scenario Profiles](docs/scenarios/)

See how the approach translates across SI, services, SDC/ISV, agentic, software-development, optimization, and other scenarios.

### Running a working session?
→ [AI Profitability Engagement Canvas](docs/canvas/engagement-canvas.md)

Capture the work, consumption, Accepted Work, outcome, value, evidence, and next action.

### Preparing a presentation?
→ [Slide Library](slides/)

Select reusable modules for different audiences and conversations.

### Looking for worked examples?
→ [Reference Examples](examples/)

Examples demonstrate the approach; they do not define it.

### Have feedback or a field learning?
→ [Validation and Field Learnings](validation/)

Capture what worked, what was unclear, and what should change.

---

## How the methods fit together

The field kit combines two complementary disciplines.

### Token-to-Value

**Token-to-Value is the measurement discipline.**

It helps connect AI consumption to Accepted Work, business outcomes, and economic value while preserving the distinction between what is measured, attributed, modeled, and unknown.

It answers questions such as:

- What AI resources are being consumed?
- What does that consumption cost?
- How much Accepted Work is being produced?
- What does one accepted unit of work cost?
- What outcomes and value might that work support?

### Value-to-Action

**Value-to-Action is the broader decision discipline.**

It begins with the work and business decision, incorporates measurement evidence, evaluates outcomes and economic value, tests the strength of the evidence, and determines what action is justified.

Token-to-Value therefore **plugs into Value-to-Action** rather than handing off to it at a single stage.

---

## Core vs. Examples

The repository intentionally separates the reusable field capability from specific implementations.

```text
CORE
│
├── POV
├── Partner Playbook
├── Engagement Canvas
├── Scenario Profiles
└── Evidence / Decision Guidance
        │
        ▼
EXAMPLES
│
├── Reference workloads
├── Enterprise scenarios
└── Future partner cases
```

> **The core is scenario-independent. Examples are applications of the core, not representations of every enterprise AI workload.**

---

## What the field kit provides

The field kit provides:

- a common AI Profitability point of view,
- a repeatable partner conversation,
- a measurement discipline for connecting consumption to Accepted Work,
- scenario-specific translations of the common approach,
- explicit treatment of evidence and uncertainty,
- and a path from AI economics to an investment decision.

The reasoning remains consistent while each workload defines its own:

```text
work to be accomplished
unit of work
acceptance criteria
business outcome
value mechanism
relevant costs
evidence requirements
decision criteria
```

---

## Evidence discipline

The field kit keeps important evidence boundaries visible:

- **Measured** — directly measured evidence
- **Observed** — activity or outcomes actually observed
- **Allocated** — measured cost distributed using an explicit rule
- **Modeled** — estimated using assumptions
- **Incremental** — change supported relative to a baseline or counterfactual
- **Realized** — economic value sufficiently supported by observed evidence
- **Unknown** — evidence is not currently available

For example:

```text
Observed resource use
        +
Explicit allocation rule
        =
Attributed workload cost
```

And:

```text
AI activity ≠ Accepted Work
Accepted Work ≠ business outcome
Observed outcome ≠ incremental outcome
Modeled value ≠ realized value
```

---

## Who this is for

The field kit is intended for practitioners and partners involved in AI economics and investment decisions, including:

- Partner Solution Architects
- AI architects and engineers
- Application developers
- FinOps practitioners
- System Integrators / services partners
- Software Development Companies / ISVs
- Technical and business leaders

The questions may differ by audience. The underlying reasoning remains consistent.

---

## Repository structure

```text
ai-profitability-field-kit/
│
├── README.md
├── docs/
│   ├── pov/
│   ├── playbook/
│   ├── scenarios/
│   ├── canvas/
│   └── facilitator/
├── slides/
├── examples/
└── validation/
```

---

## Current maturity

**Status: V0.1 — internal draft**

Initial work focuses on:

1. AI Profitability POV
2. Partner Playbook
3. SI / SDC scenario translations
4. Engagement Canvas
5. Modular field assets

The field kit will be refined through internal enablement and selective partner application.

---

## How we will know this works

Practitioners should eventually be able to:

1. **Understand** the AI Profitability perspective.
2. **Apply** it to a new partner or workload.
3. **Deliver** the conversation independently.
4. **Act** on an evidence-backed next step.
5. **Improve** the approach through field feedback.

> **The goal is not simply to create content. It is to create a repeatable organizational capability for helping partners make better AI investment decisions.**

---

## Working hypotheses

The field kit is currently being developed and validated. Claims about broad applicability, practitioner adoption, partner impact, or improved investment decisions should be treated as hypotheses until supported by field evidence.