# Scenario Stress Test v0.1

## Purpose

This exercise tests whether the AI Profitability core can describe materially different partner scenarios without becoming either too generic or too customized.

Round 1 uses three contrasting scenarios:

1. **SI / Services — Customer Support Agent**
2. **SI / Services — AI-Assisted Software Modernization**
3. **SDC / ISV — Embedded AI Product / Copilot**

The goal is not to prove the framework works.

The goal is to identify:

- what stays stable,
- what changes,
- where the framework strains,
- and whether the core methodology needs adjustment before scenario profiles are published.

---

# Core stress-test contract

Each scenario must answer the same questions:

```text
SCENARIO
Who is the partner and what are they trying to do?

WORK
What work are we trying to accomplish?

UNIT OF WORK
What is one economically meaningful unit?

ACCEPTED WORK
What must be true before the work counts?

CONSUMPTION
What resources materially contribute to cost?

OUTCOME
What downstream change matters?

VALUE
How does that outcome create economic value?

EVIDENCE
What can be measured?
What is observed, allocated, modeled, incremental, realized, or unknown?

ACTION
What decision might this analysis support?

STRAIN
Where does the framework become awkward or incomplete?
```

---

# Scenario 1 — SI / Services: Customer Support Agent

## Scenario

A systems integrator is helping an enterprise deploy an AI-assisted customer support agent.

The partner needs to help the customer determine whether the agent should remain a pilot, be optimized, or scale into broader production use.

---

## WORK

> **What work are we trying to accomplish?**

Resolve customer issues accurately and efficiently while preserving required service quality and controls.

---

## UNIT OF WORK

A reasonable unit is:

> **One customer support issue handled.**

Depending on the workflow, that may include classification, retrieval, response generation, tool execution, escalation, or case closure.

---

## ACCEPTED WORK

One support interaction counts as Accepted Work when it satisfies the agreed acceptance criteria.

For example:

```text
correct resolution
+
grounded / policy-compliant response
+
required customer or system action completed
+
no unnecessary human correction
```

A generated answer alone is not Accepted Work.

---

## CONSUMPTION

Potentially relevant resources include:

```text
model tokens / calls
retrieval / search
tool calls
agent orchestration
application compute
observability
storage
networking
human review
human escalation / rework
```

Some costs may be interaction-linked.

Others may exist at resource, capacity, workload, daily, or monthly grain and require allocation.

---

## OUTCOME

Possible downstream outcomes include:

```text
issue resolved
first-contact resolution improved
escalation avoided
average handling time reduced
customer wait time reduced
support capacity increased
customer satisfaction preserved or improved
```

Accepted Work and business outcome remain distinct.

A technically correct response may still fail to resolve the customer's issue.

---

## VALUE

Potential economic value may come from:

```text
lower human handling cost
avoided escalation cost
additional support capacity
reduced backlog
higher retention / satisfaction
recovered revenue opportunities
```

The appropriate mechanism depends on the customer's operating model.

---

## EVIDENCE

Likely evidence sources:

```text
AI runtime telemetry
evaluation / quality scores
CRM / case-management systems
contact-center metrics
labor-cost assumptions
FinOps / cloud cost evidence
```

Example evidence states:

```text
Model usage           → MEASURED / OBSERVED
Shared Search cost    → MEASURED + ALLOCATED
Accepted Work         → OBSERVED
Resolved case         → OBSERVED
Avoided escalation    → may require baseline / INCREMENTAL evidence
Economic benefit      → MODELED initially, potentially REALIZED later
```

---

## ACTION

This analysis could support:

```text
PROVE
if technical work is strong but business outcomes are not established

OPTIMIZE
if Accepted Work is valuable but execution cost is inefficient

SCALE
if outcome evidence and next-dollar economics are strong

RESTRUCTURE
if escalation, workflow, or architecture design prevents viable economics
```

---

## Where the framework strains

This scenario fits the framework relatively naturally.

The main challenge is **causal attribution**.

For example:

```text
resolution rate improved
```

does not automatically mean:

```text
AI caused the improvement
```

Support operations may change simultaneously through staffing, routing, policy, seasonality, or process changes.

### Round 1 observation

The distinction:

```text
Accepted Work
→ Business Outcome
→ Incremental Outcome
```

is essential and appears useful.

No core change required yet.

---

# Scenario 2 — SI / Services: AI-Assisted Software Modernization

## Scenario

A systems integrator is using coding agents to help modernize a customer's legacy application estate.

The customer wants to know whether AI-assisted development actually improves delivery economics rather than simply increasing developer activity.

---

## WORK

> **What work are we trying to accomplish?**

Deliver accepted modernization work safely, correctly, and faster than the relevant baseline.

Examples might include:

```text
framework migration
language modernization
dependency upgrades
test generation
API migration
legacy module replacement
```

---

## UNIT OF WORK

This is already more difficult than Scenario 1.

Potential units include:

```text
engineering task
story
module
migration unit
pull request
accepted code change
```

An individual prompt or coding-agent session is not economically meaningful enough.

A reasonable initial unit is:

> **One accepted engineering task or migration unit.**

---

## ACCEPTED WORK

Work should count only when the engineering acceptance criteria are satisfied.

For example:

```text
implementation completed
+
build succeeds
+
required tests pass
+
security / static checks pass
+
human review accepts the change
```

Depending on the scenario, production validation may also be required.

This is a strong test of the Accepted Work abstraction because many AI actions may happen before one unit of accepted work exists.

---

## CONSUMPTION

Potential cost and effort include:

```text
coding-agent tokens / calls
repo search
tool execution
test runs
build / CI compute
developer prompts
developer review
human rework
failed patch cycles
cloud development environments
supporting infrastructure
```

Importantly, the denominator should not be:

```text
cost per prompt
```

if the real economic unit is an accepted engineering task.

---

## OUTCOME

Potential downstream outcomes include:

```text
migration throughput increased
engineering cycle time reduced
developer effort reduced
backlog completed faster
defect rate maintained or improved
release accelerated
modernization program completed earlier
```

Accepted code is not itself necessarily the final business outcome.

---

## VALUE

Potential economic mechanisms include:

```text
developer capacity released
reduced delivery cost
shorter modernization timeline
earlier decommissioning of legacy systems
earlier realization of modernization benefits
reduced defect / maintenance burden
```

The value mechanism may therefore span much longer time horizons than the AI work itself.

---

## EVIDENCE

Likely sources:

```text
coding-agent telemetry
Git / PR history
CI/CD systems
work-item tracking
developer time / effort data
defect systems
program milestones
financial assumptions
```

Example:

```text
Token usage                 → MEASURED / OBSERVED
Agent edits / test attempts → OBSERVED
Accepted engineering task   → OBSERVED
Developer hours saved       → often MODELED initially
Cycle-time change           → OBSERVED
Incremental cycle-time gain → requires baseline / comparison
Program economic value      → likely MODELED before REALIZED
```

---

## ACTION

Potential actions include:

```text
OPTIMIZE
if AI creates accepted work but wastes too much developer / compute effort

PROVE
if productivity claims rely mainly on assumptions

SCALE
if accepted-work throughput and delivery economics remain strong across more teams

RESTRUCTURE
if workflow design causes excessive review, churn, or low acceptance
```

---

## Where the framework strains

This scenario exposes several important issues.

### 1. Work is hierarchical

There may be:

```text
AI action
↓
code edit
↓
accepted implementation increment
↓
engineering task
↓
epic / modernization milestone
```

Which level should be the economic unit?

The answer may depend on the investment decision.

This suggests:

> **Unit of work may need to be decision-relative rather than universally fixed.**

### 2. Human effort is part of the production system

The AI is not independently producing the final unit.

The workflow may look like:

```text
AI work
+
developer work
+
CI / tests
+
review
=
Accepted Work
```

That means AI profitability cannot always be interpreted as:

```text
AI cost → output value
```

It may need to reason about a **human + AI production system**.

### 3. “Time saved” is easy to overstate

If a developer completes something faster, the economic value depends on what happens to the released capacity.

```text
time saved
≠ automatically cost saved
```

The capacity might enable more delivery rather than reduce expense.

### Round 1 observation

The core still appears useful, but this scenario suggests two possible principles:

```text
1. Choose the unit of work based on the decision being made.

2. Measure the economics of the human + AI system when human effort is materially required.
```

These may belong in the Playbook eventually.

Do not update the core yet; test Scenario 3 first.

---

# Scenario 3 — SDC / ISV: Embedded AI Product / Copilot

## Scenario

A software company is adding an AI copilot or agentic capability to its existing product.

The company needs to determine whether the capability creates enough customer value while maintaining sustainable product economics.

---

## WORK

> **What work are we trying to help the customer accomplish?**

Examples might include:

```text
create a report
analyze a dataset
generate a design
complete a workflow
draft content
resolve a domain task
automate part of a professional workflow
```

The starting point is still the customer's work—not “we added AI.”

---

## UNIT OF WORK

Potential units might include:

```text
successful user task
completed workflow
accepted artifact
resolved domain problem
```

A useful generic form is:

> **One successfully completed customer task.**

---

## ACCEPTED WORK

The customer's task counts when it meets the product's acceptance criteria.

For example:

```text
task completed
+
output quality acceptable
+
required controls satisfied
+
customer does not need substantial rework
```

Depending on the product, acceptance may be inferred from user behavior or explicitly evaluated.

---

## CONSUMPTION

Provider-side economics may include:

```text
model inference
retrieval / search
agent tools
application compute
storage
observability
networking
third-party services
support
human review if applicable
```

These costs may vary substantially by customer, feature, model, or workflow.

---

## OUTCOME

There are potentially two classes of outcomes.

### Customer outcome

```text
task completed faster
workflow automated
decision improved
manual effort reduced
new capability enabled
```

### Provider outcome

```text
feature adoption
retention
upsell
higher willingness to pay
new revenue
usage growth
```

This is our first major structural tension.

---

## VALUE

There are clearly **two economic perspectives**.

### Customer economics

> Is the AI capability valuable enough for the customer to use or pay for?

Conceptually:

```text
Customer benefit
-
customer price / effort / risk
=
Customer Net Value
```

### Provider economics

> Can the software company deliver the capability sustainably?

Conceptually:

```text
AI-related revenue / economic contribution
-
cost to serve
=
Provider Economics
```

A feature can have:

```text
high customer value
+
poor provider economics
```

or:

```text
strong provider margin
+
weak customer value
```

Neither is a sustainable long-term outcome.

---

## EVIDENCE

Potential sources:

```text
product telemetry
AI runtime telemetry
FinOps / infrastructure cost
feature usage
task completion
customer research
pricing / entitlement data
renewal / retention
revenue
support data
```

Example:

```text
Inference usage           → MEASURED / OBSERVED
Shared infrastructure     → MEASURED + ALLOCATED
Accepted Work             → OBSERVED
Customer time saved       → potentially MODELED
Feature adoption          → OBSERVED
Incremental retention     → difficult; needs causal evidence
Revenue                   → OBSERVED
Feature-level margin      → measured + allocated + modeled depending on pricing
```

---

## ACTION

Possible decisions:

```text
OPTIMIZE
change model / architecture / routing to improve cost-to-Accepted-Work

RESTRUCTURE
change packaging, pricing, limits, entitlement, or architecture

PROVE
collect stronger customer-value evidence

SCALE
expand availability when customer value and provider economics both support it

SUSTAIN
maintain as a strategic or retention capability

PAUSE / RETIRE
when value or economics remain structurally unattractive
```

---

## Where the framework strains

This is the strongest stress point so far.

The current generic term:

```text
Economic Value
```

may hide two materially different questions:

```text
CUSTOMER VALUE
Does the user/customer receive enough economic value?

PROVIDER ECONOMICS
Can the partner deliver that value sustainably?
```

For an SI, there may even be a third lens:

```text
DELIVERY ECONOMICS
Can the partner deliver the engagement efficiently and profitably?
```

This suggests that **“Who receives the value?”** may need to become an explicit part of the methodology.

---

# Round 1 cross-scenario comparison

| Dimension | Support Agent | Software Modernization | Embedded AI Product |
|---|---|---|---|
| Partner | SI | SI | SDC / ISV |
| Work | Resolve support issue | Complete modernization work | Help user complete product task |
| Unit of work | Support case | Engineering task / migration unit | Customer task / workflow |
| Accepted Work | Correct resolution | Accepted implementation | Accepted customer task |
| Human contribution | Medium | High | Low–variable |
| Cost grain challenge | Shared infra | AI + developer + CI | Shared infra + per-user variability |
| Outcome | Service performance | Delivery performance | Customer + product outcomes |
| Value | Operating economics | Delivery/program economics | Customer value + provider economics |
| Main evidence challenge | Causality | Baseline + human effort | Attribution + two-sided economics |
| Likely action | Prove/Optimize/Scale | Prove/Optimize/Scale | Optimize/Restructure/Scale |

---

# What stayed stable

The following concepts survived all three scenarios:

```text
Start with WORK

Define an economically meaningful UNIT OF WORK

Define ACCEPTED WORK explicitly

Measure relevant CONSUMPTION

Keep ACCEPTED WORK separate from OUTCOME

Connect OUTCOME to VALUE

Make EVIDENCE status visible

End with an ACTION
```

This is encouraging.

The five-question field language remains meaningful:

```text
WORK
MEASURE
OUTCOME
VALUE
ACTION
```

No scenario required a fundamentally different methodology.

---

# What changed

The scenario-specific semantics changed significantly:

```text
unit of work
acceptance criteria
human contribution
cost attribution
business outcome
value mechanism
time horizon
evidence source
decision threshold
```

This supports the current design principle:

> **Standardize the reasoning and evidence discipline. Customize the workload and business semantics deliberately.**

---

# Where the framework genuinely strained

Round 1 surfaced three important questions.

## 1. Should the unit of work be decision-relative?

In complex engineering workflows, several valid units may exist.

```text
interaction
task
story
module
program milestone
```

The correct unit may depend on the decision.

**Provisional principle:**

> Choose the unit of work at the level where the investment decision becomes economically meaningful.

---

## 2. Should we explicitly model the human + AI production system?

For many enterprise workloads:

```text
AI + Human + Tools + Infrastructure → Accepted Work
```

AI cost alone may therefore be an incomplete denominator.

**Provisional principle:**

> Include materially required human effort and supporting resources when assessing the economics of Accepted Work.

---

## 3. Do we need separate value perspectives?

The ISV scenario strongly suggests yes.

```text
Customer Value
        +
Provider Economics
```

For services partners:

```text
Customer Value
        +
Delivery Economics
```

A sustainable AI investment may require more than one perspective to work.

**Provisional hypothesis:**

> AI Profitability should explicitly identify whose economics are being evaluated.

This should be tested again in Round 2 before modifying the core POV.

---

# Round 1 verdict

## Does the framework pass?

**Provisionally, yes.**

The common contract remained meaningful across:

```text
operational automation
engineering productivity
product economics
```

The test did not require replacing the five core questions.

However, it surfaced three refinements worth testing further:

1. **Decision-relative unit of work**
2. **Human + AI system economics**
3. **Explicit value beneficiary / economic perspective**

These should remain hypotheses until Round 2 tests them against:

```text
AI FinOps / optimization
Domain-specific agentic workflow
Usage-based agentic SaaS
```

---

# No core changes yet

Do not update the POV or Playbook based only on Round 1.

Round 2 should determine whether these are:

```text
universal principles
scenario-specific guidance
or unnecessary complexity
```

Only then should mature findings move into the field-facing assets.