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

The objective is to help the partner reach an evidence-backed next action.

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

Standardize the questions. Adapt the answers to the workload and business model.

---

# Before the conversation

You do not need complete economics before starting.

Try to understand four things:

1. **Why the conversation is happening now**

   - rising cost,
   - new AI investment,
   - pilot-to-production decision,
   - architecture choice,
   - margin concern,
   - customer ROI question,
   - or another decision.

2. **Who owns the decision**

   - engineering,
   - product,
   - FinOps,
   - business leadership,
   - customer,
   - or multiple stakeholders.

3. **What evidence already exists**

   - cloud cost,
   - runtime telemetry,
   - evaluations,
   - workload metrics,
   - business KPIs,
   - financial assumptions.

4. **What decision needs to be made**

   - prove,
   - optimize,
   - scale,
   - sustain,
   - restructure,
   - pause,
   - or retire.

Start with the decision—not a product demonstration.

---

# 1. WORK

> **What work are we trying to accomplish?**

The goal is to define the job before discussing AI consumption.

## Ask

- What business or customer problem are we solving?
- What work is being performed today?
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

## Capture

```text
Work to be accomplished:
Unit of work:
Current baseline:
Acceptance criteria:
Decision being considered:
```

## Watch for

### Starting with the technology

Avoid:

> “We are using GPT-X with retrieval and three agents.”

Redirect toward:

> “What work is that system supposed to accomplish?”

### Counting output as success

Generated output is not automatically Accepted Work.

Define the acceptance criteria first.

## Exit condition

You should be able to complete this sentence:

> **One successful unit of work is \_\_\_\_\_\_\_\_, and we accept it when \_\_\_\_\_\_\_\_.**

If you cannot, do not move into detailed unit economics yet.

---

# 2. MEASURE

> **What did the work consume, and how much Accepted Work did it produce?**

This is where Token-to-Value provides the measurement discipline.

## Ask

### Consumption

- What AI resources are consumed?
- What supporting cloud services are involved?
- What human effort is required?
- What retry, rework, or failure activity exists?
- Which costs are dedicated versus shared?

Relevant signals might include:

```text
tokens
model calls
tool calls
retrieval
compute
cloud infrastructure
latency
retries
human review
human rework
```

### Accepted Work

- How many work attempts occurred?
- How many met the acceptance criteria?
- How is acceptance verified?
- What failures still consumed resources?
- Is quality consistent enough for economic comparison?

## Useful measures

Depending on the workload:

```text
Total relevant cost

Accepted Work rate
=
Accepted units / attempted units

Cost per Accepted Work
=
Relevant cost / Accepted units

AI work waste
=
Resource-consuming activity that did not produce Accepted Work
```

These are patterns, not mandatory universal KPIs.

## Preserve cost provenance

Always distinguish:

```text
MEASURED
Direct billing / usage evidence

OBSERVED
Runtime activity actually observed

ALLOCATED
Shared measured cost assigned using an explicit rule

MODELED
Cost estimated from pricing or assumptions

UNKNOWN
Not currently available
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

Do not describe the result as measured per-request cost if Azure did not bill it at that grain.

## Watch for

- optimizing tokens before defining Accepted Work,
- comparing systems only on cost per interaction,
- excluding failed work from the denominator,
- treating allocated cost as directly measured cost,
- ignoring human review or rework where economically material.

## Exit condition

You should understand:

> **What the work costs at a defensible grain, how much Accepted Work is produced, and where the largest uncertainty or waste exists.**

---

# 3. OUTCOME

> **What changed because Accepted Work occurred?**

Accepted Work proves that the AI performed the intended work.

It does not yet prove business value.

## Ask

- What downstream outcome should this work influence?
- Is that outcome currently measured?
- Where does the evidence live?
- What baseline are we comparing against?
- How long after the AI work should the outcome occur?
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

## Classify the evidence

### Modeled outcome

Expected based on assumptions.

### Observed outcome

Actually occurred after the AI work.

### Incremental outcome

Evidence supports that the AI changed the outcome relative to an appropriate baseline or counterfactual.

Keep these separate.

```text
Accepted Work
≠ observed outcome

Observed outcome
≠ incremental outcome
```

## When business evidence is missing

Do not invent a value.

Record:

```text
Outcome evidence: UNKNOWN
```

Then turn the gap into a measurement plan:

- what event must be captured,
- from which system,
- with what identifier,
- over what period,
- against what baseline.

## Exit condition

You should know either:

> **what business outcome changed**

or:

> **exactly what evidence is missing to determine whether it changed.**

Both are useful outcomes from the conversation.

---

# 4. VALUE

> **What was the change worth, and how credible is the claim?**

Only value the outcome after defining the work and outcome.

## Ask

- How does the outcome create economic benefit?
- Is the benefit revenue, contribution, cost avoided, capacity, margin, risk, or something else?
- What additional costs are required to produce it?
- Is the value modeled, observed, incremental, or realized?
- What assumptions drive the conclusion?
- How easily does the economic case break?

## Basic reasoning

Depending on the use case:

```text
Economic benefit
-
Relevant customer cost
=
Net Economic Value
```

For an expansion decision:

```text
Additional expected value
-
Additional required cost
=
Incremental / next-dollar economics
```

Avoid relying only on historical average economics when the decision is about additional investment.

## Test two different things

### Evidence confidence

> How strongly is the value claim supported?

Consider:

- measurement quality,
- baseline quality,
- attribution,
- completeness of costs,
- observed versus modeled inputs.

### Value resilience

> How sensitive is the conclusion to assumptions?

Test important assumptions such as:

- workload volume,
- success rate,
- conversion,
- labor value,
- margins,
- AI cost,
- human review,
- model choice.

These are different questions.

A resilient model is not necessarily well proven.

Strong evidence does not necessarily mean attractive economics.

## Watch for

- modeled ROI presented as realized ROI,
- revenue presented without relevant costs,
- productivity translated directly into dollars without a mechanism,
- sensitivity analysis presented as causal evidence,
- ignoring next-dollar economics.

## Exit condition

You should be able to state:

```text
What value we can support:
What value is still modeled:
What assumptions matter most:
What remains unknown:
How resilient the conclusion appears:
```

---

# 5. ACTION

> **What should we do next?**

Do not end the conversation with a dashboard or ROI number.

End with a decision.

Possible actions:

```text
SCALE
SUSTAIN
OPTIMIZE
PROVE
RESTRUCTURE
PAUSE
RETIRE
```

Use the primary constraint to guide the action.

| What the evidence suggests                               | Likely next action |
| -------------------------------------------------------- | ------------------ |
| Promising economics, weak business evidence              | **PROVE**          |
| Valuable work, inefficient execution                     | **OPTIMIZE**       |
| Economics depend on a flawed architecture/business model | **RESTRUCTURE**    |
| Strong evidence and attractive next-dollar economics     | **SCALE**          |
| Healthy economics, no immediate expansion need           | **SUSTAIN**        |
| Material unresolved risk or temporary constraint         | **PAUSE**          |
| Evidence indicates the investment is no longer justified | **RETIRE**         |

These are decision patterns, not automatic rules.

Context and mandatory business or technical controls still apply.

## Every action needs a reassessment trigger

Examples:

```text
Scale
→ reassess after workload doubles

Optimize
→ reassess after architecture change

Prove
→ reassess when pilot outcome evidence is available

Restructure
→ reassess after new operating model is tested
```

This turns AI Profitability into an operating loop rather than a one-time ROI exercise.

---

# The conversation should produce one page

A successful engagement does not need a large report.

At minimum, leave with:

```text
AI PROFITABILITY SNAPSHOT

WORK
What are we trying to accomplish?

ACCEPTED WORK
What counts as successfully completed work?

COST / CONSUMPTION
What do we know, allocate, model, or not know?

OUTCOME
What changed?

VALUE
What can we reasonably claim?

EVIDENCE
What is measured / observed / allocated /
modeled / incremental / realized / unknown?

ACTION
What should happen next?

REASSESS
What evidence or event changes the decision?
```

This becomes the input to the Engagement Canvas.

---

# Different entry points are okay

Partners may enter the conversation at different places.

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

The five questions provide structure without requiring every conversation to begin at the same point.

---

# Partner-type translation

The playbook stays constant.

The economic interpretation changes.

### SI / Services Partner

Common question:

> How do we help the customer prove and improve the economics of an AI investment?

Typical emphasis:

```text
customer baseline
delivery economics
business outcomes
architecture optimization
evidence plan
customer investment decision
```

### SDC / ISV

Common question:

> Can we deliver this AI capability with sustainable product economics and meaningful customer value?

Typical emphasis:

```text
cost per Accepted Work
feature / customer economics
gross-margin impact
model and architecture choices
pricing / packaging
usage growth
next-dollar product investment
```

Detailed translations belong in the Scenario Profiles rather than this playbook.

---

# Common conversation traps

Avoid these shortcuts:

```text
“Tokens went down, therefore economics improved.”

“Quality scores are high, therefore the project has ROI.”

“The business KPI improved after launch, therefore AI caused it.”

“The model shows 5× value, therefore we should scale.”

“We cannot measure it yet, therefore the value is zero.”

“The service costs $X per month, therefore each request costs $X/N.”
```

Replace them with:

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

Begin with the economic problem.

Then map the evidence gaps to capabilities.

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

> **“Based on what we know today, the primary constraint is \_\_\_\_\_\_\_\_. The evidence supports \_\_\_\_\_\_\_\_ as the next action. Before the next investment decision, we need to learn \_\_\_\_\_\_\_\_.”**

That is more useful than ending with a generic ROI estimate.

---

# Practitioner checklist

Before considering the conversation complete, confirm:

- [ ] We started with the work, not the AI.
- [ ] The unit of work is clear.
- [ ] Accepted Work has explicit criteria.
- [ ] Relevant costs are identified.
- [ ] Measured, allocated, modeled, and unknown costs are distinguished.
- [ ] A downstream business outcome is defined.
- [ ] Observed and incremental outcomes are not conflated.
- [ ] Value claims show their evidence status.
- [ ] Important assumptions and resilience are understood.
- [ ] A specific next action is identified.
- [ ] A reassessment trigger or evidence gap is captured.

If several of these are missing, that is not failure.

It tells you what needs to be proven next.
