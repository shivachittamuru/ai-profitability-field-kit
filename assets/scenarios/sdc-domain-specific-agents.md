# SDC — Domain-Specific Agentic Workflow

## Scenario

A Software Development Company (SDC) is building an AI-powered product capability that completes a **multi-step domain workflow** using models, tools, retrieval, APIs, and potentially multiple agents.

Examples might include:

- financial research and analysis,
- claims processing,
- engineering or CAD automation,
- legal or compliance workflows,
- healthcare administration,
- enterprise research,
- document-heavy knowledge work,
- domain-specific planning and execution.

The profitability question is not simply:

> **How much does the agentic workflow cost to run?**

It is:

> **Can the SDC reliably deliver valuable end-to-end customer outcomes while keeping the workflow economically sustainable at scale?**

---

## WORK

**Work to be accomplished**

Complete a meaningful domain workflow from request to an acceptable business result.

**Possible unit of work**

> One successfully completed domain workflow.

The unit should represent something the customer actually values, not an internal agent step.

---

## ACCEPTED WORK

Individual model responses, tool calls, subagent outputs, or completed orchestration steps should not automatically count as Accepted Work.

A workflow counts only when the **end-to-end result** satisfies the required domain, quality, and control criteria.

For example:

```text
workflow completed
+
required domain checks pass
+
output quality acceptable
+
required controls satisfied
+
acceptable human intervention / rework
=
Accepted Work
```

Intermediate steps may still be useful for diagnosis and optimization, but the economic unit should remain the completed customer workflow.

---

## MEASURE

**What did the workflow consume, and how much Accepted Work did it produce?**

Relevant evidence may include:

```text
model / token usage
agent and subagent calls
tool / API calls
retrieval / search
workflow steps
retries / loops
compute and application infrastructure
storage / networking
observability
third-party services
human review / intervention
failed or abandoned workflows
```

Useful measures may include:

```text
Accepted Work rate

Cost per Accepted Workflow

Cost-to-serve by workflow / customer / tier

Human intervention per Accepted Workflow

Retries / tool calls per Accepted Workflow

Failure / abandonment rate

End-to-end latency
```

Because agentic workflows may use shared or capacity-based services, cost attribution should remain explicit:

```text
measured resource cost
+
observed workflow usage
+
explicit allocation rule
=
attributed workflow cost
```

Do not represent allocated workflow cost as directly measured per-run cost unless the underlying billing data supports that grain.

---

## OUTCOME

**What changed?**

Potential customer outcomes may include:

- workflow completed faster,
- manual steps eliminated,
- specialist effort reduced,
- decision cycle shortened,
- throughput increased,
- errors or rework reduced,
- previously unavailable capability enabled,
- higher consistency or service quality.

Potential SDC outcomes may include:

- greater feature adoption,
- increased usage,
- retention or expansion,
- higher willingness to pay,
- new revenue,
- lower support burden.

Keep the chain explicit:

```text
Agent activity
≠ Accepted Workflow
≠ Customer Outcome
≠ Incremental Outcome
```

A technically successful workflow does not automatically prove that the customer is receiving incremental business value.

---

## VALUE

**Whose economics matter?**

Both usually matter:

```text
Customer Value
+
Provider Economics
```

### Customer value

Potential mechanisms include:

```text
less manual effort
        ↓
faster / cheaper workflow completion
        ↓
customer economic value
```

or:

```text
higher workflow quality / capability
        ↓
better downstream decision or operation
        ↓
customer economic value
```

### Provider economics

The SDC must also understand:

```text
price / revenue
-
AI + tool + infrastructure cost
-
human support / intervention
-
other relevant cost-to-serve
=
provider economics
```

A workflow can create high customer value while still being expensive for the provider to operate.

Likewise, strong provider margins do not compensate for weak customer value.

---

## EVIDENCE TO ASK FOR

Relevant evidence may include:

- agent / workflow telemetry,
- model and tool usage,
- workflow traces,
- quality or domain evaluations,
- completion and failure evidence,
- human intervention or review data,
- cloud / FinOps cost evidence,
- customer workflow metrics,
- product usage and adoption data,
- pricing / entitlement data,
- revenue, retention, or expansion data,
- baseline or comparison workflow performance.

Missing evidence should be treated as **Unknown**, not silently assumed.

---

## ACTION

This scenario may support decisions such as:

**PROVE / OPTIMIZE / RESTRUCTURE / SCALE / SUSTAIN / PAUSE**

Typical patterns:

| Situation | Possible action |
|---|---|
| Workflow works technically, but customer outcome is unclear | **PROVE** |
| High retries, tool usage, latency, or intervention drive cost | **OPTIMIZE** |
| Orchestration or workflow design prevents sustainable economics | **RESTRUCTURE** |
| Strong customer outcomes and healthy provider economics | **SCALE** |
| Economics are healthy at the current scope | **SUSTAIN** |
| Persistent weak outcomes or unsustainable economics | **PAUSE** |

These are decision patterns, not automatic rules.

---

## Practitioner takeaway

For this scenario, the economic chain is:

```text
Customer Workflow
        ↓
Models + Agents + Tools + Infrastructure + Human Support
        ↓
Accepted Workflow
        ↓
Customer Outcome
        ↓
Customer Value
        ↓
Provider Economics
        ↓
PROVE / OPTIMIZE / RESTRUCTURE / SCALE / ...
```

The key question is:

> **Are we converting complex agent activity into reliable customer workflows that create enough value to justify the cost-to-serve?**