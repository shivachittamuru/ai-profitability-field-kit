# SI — Customer Support Agent

## Scenario

A System Integrator is helping a customer design, deploy, or scale an AI-assisted customer-support solution.

The profitability question is not simply:

> **How much does the agent cost?**

It is:

> **Is the customer converting AI investment into accepted support work and economically valuable service outcomes?**

---

## WORK

**What work are we trying to accomplish?**

Resolve customer issues accurately and efficiently while maintaining the required service quality, policy, and customer experience.

**Possible unit of work**

> One customer issue handled.

---

## ACCEPTED WORK

The AI activity should count as Accepted Work only when the support task meets the customer's acceptance criteria.

For example:

```text
correct resolution
+
grounded / policy-compliant response
+
required action completed
+
acceptable human intervention / rework
```

A generated response alone is not Accepted Work.

---

## MEASURE

**What did it consume, and how much Accepted Work did it produce?**

Relevant evidence may include:

```text
model / token usage
retrieval and search
tool calls
application infrastructure
observability
human review
escalation / rework
```

Useful measures may include:

```text
Accepted Work rate

Cost per Accepted Work

Human intervention per Accepted Work

Failed / wasted AI work
```

Cloud costs should preserve their provenance:

```text
measured cost
+
explicit allocation where required
=
attributed workload cost
```

Do not represent capacity-based or shared costs as directly measured per-interaction costs.

---

## OUTCOME

**What changed?**

Potential customer outcomes include:

- issue resolution,
- first-contact resolution,
- escalation rate,
- average handling time,
- wait time,
- support capacity,
- customer satisfaction.

Keep the evidence chain explicit:

```text
Accepted Work
≠ Business Outcome
≠ Incremental Outcome
```

For example, a resolved case may be observed while the improvement relative to the previous support process is still unknown.

---

## VALUE

**What was the outcome worth?**

Potential value mechanisms include:

- lower human handling or escalation cost,
- additional support capacity,
- reduced backlog,
- improved customer retention or experience,
- revenue protected or recovered.

The appropriate value mechanism depends on the customer's operating model.

Avoid automatically converting “minutes saved” into financial savings unless there is a credible mechanism for realizing that value.

---

## EVIDENCE TO ASK FOR

A practitioner might look for:

```text
AI runtime telemetry
quality / evaluation evidence
case-management or CRM data
contact-center metrics
human review / escalation data
cloud / FinOps cost evidence
business assumptions or financial data
baseline performance
```

Missing evidence should be labeled **Unknown**, not silently assumed.

---

## ACTION

The conversation should end with an evidence-backed next step.

Typical patterns:

| Situation | Possible action |
|---|---|
| Strong technical performance, weak business evidence | **PROVE** |
| Valuable Accepted Work, but high execution cost or rework | **OPTIMIZE** |
| Strong outcome evidence and attractive next-dollar economics | **SCALE** |
| Workflow or architecture prevents viable economics | **RESTRUCTURE** |
| Healthy economics with no immediate expansion need | **SUSTAIN** |

These are decision patterns, not automatic rules.

---

## Practitioner takeaway

For this scenario, the economic chain is:

```text
Customer Issue
      ↓
AI + Human + Supporting Services
      ↓
Accepted Support Work
      ↓
Customer / Service Outcome
      ↓
Customer Economic Value
      ↓
PROVE / OPTIMIZE / SCALE / ...
```

The key question is:

> **Are we improving the economics of resolving customer problems—not merely reducing the cost of AI calls?**