# AI Profitability Partner Playbook

## Purpose

This playbook helps practitioners run a structured AI Profitability conversation with a partner or customer.

Use it when the conversation sounds like:

- “AI is getting too expensive.”
- “How do we know this investment is worth it?”
- “The pilot works. Should we scale it?”
- “Which architecture or model is economically better?”
- “How do we justify this AI feature?”
- “What should we measure before investing further?”

The objective is **not** to prove that AI is profitable.

The objective is to help the partner reach an **evidence-backed next action**.

Use the supporting assets for different purposes:

```text
Partner Playbook
→ how to reason through and facilitate the conversation

Scenario TEMPLATE.md
→ how the method translates to a specific partner or workload

Engagement Canvas
→ what to capture and leave behind from the engagement
```

---

# The conversation

Use five questions:

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

Do not force every engagement through the same metrics.

> **Standardize the questions. Adapt the answers to the workload and business model.**

---

# Before the conversation

Try to establish four things before going deep:

1. **Why now?**  
   Rising cost, new investment, pilot-to-production, architecture choice, margin concern, ROI question, or another trigger.

2. **Who owns the decision?**  
   Engineering, product, FinOps, business leadership, customer, or multiple stakeholders.

3. **What evidence already exists?**  
   Cost, runtime telemetry, evaluations, workload metrics, business KPIs, financial assumptions.

4. **What decision needs to be made?**  
   Prove, optimize, scale, sustain, restructure, pause, or retire.

Start with the decision—not a product demonstration.

---

# 1. WORK

> **What work are we trying to accomplish?**

Define the job before discussing AI consumption.

## Ask

- What business or customer problem are we solving?
- What is the meaningful unit of work?
- What does successful completion look like?
- What makes the work acceptable?
- What happens when the work fails or requires rework?
- Why is AI being introduced?

Examples of units of work might include:

```text
one resolved support issue
one accepted engineering task
one completed workflow
one reviewed document
one successful customer task
one generated design accepted for use
```

## Watch for

### Starting with the technology

Avoid beginning with:

> “We are using GPT-X with retrieval and three agents.”

Redirect toward:

> “What work is that system supposed to accomplish?”

### Counting activity as success

Generated output is not automatically **Accepted Work**.

Accepted Work means the AI-assisted work satisfies the acceptance criteria required for the job being performed.

## Exit condition

You should be able to complete:

> **One successful unit of work is ________, and we accept it when ________.**

If you cannot, do not move into detailed unit economics yet.

---

# 2. MEASURE

> **What did the work consume, and how much Accepted Work did it produce?**

Measure the complete relevant system—not only model usage.

Relevant evidence may include:

```text
tokens / model calls
tools / retrieval
compute / cloud infrastructure
latency / retries
human review / rework
other economically material services
```

## Useful measures

Depending on the workload:

```text
Accepted Work rate
=
Accepted units / attempted units
```

```text
Cost per Accepted Work
=
Relevant cost / Accepted units
```

```text
AI work waste
=
Resource-consuming activity that did not produce Accepted Work
```

These are patterns, not mandatory universal KPIs.

## Preserve evidence provenance

Keep important evidence types separate:

```text
MEASURED
Direct measurement or billing evidence

OBSERVED
Activity or outcomes actually observed

ALLOCATED
Measured cost assigned using an explicit rule

MODELED
Estimated using assumptions

UNKNOWN
Evidence not currently available
```

For example:

```text
Azure AI Search resource cost
        +
observed workload search activity
        +
explicit allocation rule
        ↓
attributed workload Search cost
```

Do not describe allocated cost as directly measured at a finer grain than the underlying evidence supports.

## Watch for

- optimizing tokens before defining Accepted Work,
- comparing systems only on cost per interaction,
- excluding failed work from the economics,
- treating allocated cost as directly measured,
- ignoring human review or rework where economically material.

## Exit condition

You should understand:

> **What the work costs at a defensible grain, how much Accepted Work is produced, and where the largest uncertainty or waste exists.**

---

# 3. OUTCOME

> **What changed because Accepted Work occurred?**

Accepted Work proves that the intended work was completed.

It does not yet prove business value.

## Ask

- What downstream outcome should this work influence?
- Is that outcome measured?
- What baseline are we comparing against?
- Where does the evidence live?
- Could something else explain the change?

Examples:

```text
support case resolved
escalation avoided
engineering cycle time reduced
workflow completed
manual effort reduced
conversion increased
defect avoided
customer task completed
```

Keep these distinctions explicit:

```text
Accepted Work
≠ business outcome

Observed outcome
≠ incremental outcome
```

### Modeled outcome
Expected based on assumptions.

### Observed outcome
Actually occurred.

### Incremental outcome
Evidence supports that the AI changed the outcome relative to an appropriate baseline or counterfactual.

If the evidence is missing, record it as **Unknown** and turn the gap into a measurement plan.

## Exit condition

You should know either:

> **what business outcome changed**

or:

> **what evidence is still needed to determine whether it changed.**

---

# 4. VALUE

> **What was the change worth, and how credible is the claim?**

Value the outcome only after defining the work and outcome.

Potential mechanisms include:

```text
revenue gained
cost avoided
capacity released
margin improved
risk reduced
cycle time shortened
customer value created
```

Basic reasoning may look like:

```text
Economic benefit
-
Relevant cost
=
Net Economic Value
```

For expansion decisions:

```text
Additional expected value
-
Additional required cost
=
Incremental / next-dollar economics
```

## Test two different things

### Evidence confidence

> **How strongly is the value claim supported?**

Consider measurement quality, baseline quality, attribution, completeness of cost, and observed versus modeled inputs.

### Value resilience

> **How sensitive is the conclusion to assumptions?**

Test the assumptions most capable of changing the decision.

A resilient model is not necessarily well proven.

Strong evidence does not necessarily mean attractive economics.

## Watch for

- modeled ROI presented as realized value,
- revenue presented without relevant costs,
- productivity translated directly into dollars without a realization mechanism,
- sensitivity analysis presented as causal evidence,
- historical average economics used when the decision concerns the next dollar.

## Exit condition

You should understand:

```text
What value is supported
What remains modeled
Which assumptions matter most
What remains unknown
How resilient the conclusion is
```

---

# 5. ACTION

> **What should we do next?**

Do not end with a dashboard or ROI number.

End with a decision.

Possible actions:

```text
PROVE
OPTIMIZE
RESTRUCTURE
SCALE
SUSTAIN
PAUSE
RETIRE
```

| What the evidence suggests | Likely next action |
|---|---|
| Promising economics, weak business evidence | **PROVE** |
| Valuable work, inefficient execution | **OPTIMIZE** |
| Architecture or business model prevents sustainable economics | **RESTRUCTURE** |
| Strong evidence and attractive next-dollar economics | **SCALE** |
| Healthy economics, no immediate expansion need | **SUSTAIN** |
| Material unresolved risk or temporary constraint | **PAUSE** |
| Investment is no longer justified | **RETIRE** |

These are decision patterns, not automatic rules.

## Every action needs a reassessment trigger

Examples:

```text
Scale
→ reassess after workload doubles

Optimize
→ reassess after architecture change

Prove
→ reassess when outcome evidence is available

Restructure
→ reassess after the new operating model is tested
```

That turns AI Profitability into an operating loop rather than a one-time ROI exercise.

Record the engagement output, evidence gaps, owners, and reassessment trigger in the **Engagement Canvas**.

---

# Different entry points are okay

The five questions provide structure without requiring every conversation to begin in the same place.

### “Our AI bill is too high.”

Start with:

```text
WORK → MEASURE
```

Then ask whether optimization preserves Accepted Work.

### “How do we prove ROI?”

Start with:

```text
WORK → OUTCOME → VALUE
```

Then inspect whether Accepted Work and incrementality are established.

### “Should we scale our pilot?”

Start with:

```text
VALUE → EVIDENCE → ACTION
```

Then work backward to unresolved assumptions.

### “Which architecture should we choose?”

Compare alternatives using:

```text
Cost
+
Accepted Work
+
quality / reliability
+
business outcome
```

not cost alone.

---

# Partner-type translation

The playbook stays constant.

The economic interpretation changes.

### SI

Typical lens:

> **How do we help the customer prove and improve the economics of an AI investment?**

### SDC

Typical lens:

> **Can we deliver this AI capability with sustainable provider economics and meaningful customer value?**

Do not create separate methodologies for each partner type.

Use the **Scenario Profiles** and `scenarios/TEMPLATE.md` to translate the common method into the specific unit of work, acceptance criteria, cost boundary, business outcome, value mechanism, and decision context.

---

# Common conversation traps

Avoid shortcuts such as:

```text
“Tokens went down, therefore economics improved.”

“Quality scores are high, therefore the project has ROI.”

“The KPI improved after launch, therefore AI caused it.”

“The model shows 5× value, therefore we should scale.”

“The service costs $X per month, therefore each request costs $X/N.”
```

Instead ask:

```text
What work improved?
How much Accepted Work resulted?
What changed downstream?
What evidence supports attribution?
Which costs are measured versus allocated?
What remains modeled or unknown?
What decision does the evidence support today?
```

---

# When to bring in Microsoft capabilities

Do not begin with products.

Begin with the economic problem, then map evidence gaps to capabilities.

Examples:

```text
Need better cloud cost / allocation evidence
→ FinOps capabilities

Need runtime or evaluation evidence
→ Foundry / observability / application tooling

Need coding-workflow evidence
→ development lifecycle / coding-agent telemetry

Need business outcome evidence
→ partner or customer operational systems
```

The platform supports the profitability motion; it does not define it.

---

# How to close the conversation

A strong close sounds like:

> **“Based on what we know today, the primary constraint is ________. The evidence supports ________ as the next action. Before the next investment decision, we need to learn ________.”**

Then capture the agreed result in the **Engagement Canvas**:

- decision,
- evidence supporting it,
- evidence gaps,
- owner,
- next action,
- reassessment trigger.

---

# Practitioner check

Before considering the conversation complete, confirm that:

- [ ] We started with the work, not the AI.
- [ ] The unit of work is clear and Accepted Work has explicit criteria.
- [ ] Relevant costs are identified and have defensible provenance.
- [ ] Measured, allocated, modeled, and unknown costs are distinguished.
- [ ] A downstream business outcome is defined.
- [ ] Observed and incremental outcomes are not conflated.
- [ ] Value claims show their evidence status and expose assumptions.
- [ ] A specific next action is identified.
- [ ] A reassessment trigger or evidence gap is captured.

If something is missing, that is useful information.

It tells you what needs to be proven next.
