# SDC — Embedded AI Copilot

## Scenario

A Software Development Company (SDC) is adding an AI copilot or agentic capability to its software product.

The profitability question is not simply:

> **How much does the AI feature cost to run?**

It is:

> **Does the capability create enough customer value while remaining economically sustainable for the SDC?**

---

## WORK

**What work are we helping the customer accomplish?**

Examples might include:

- generating a report,
- analyzing data,
- creating content,
- completing a workflow,
- making a recommendation,
- automating part of a professional task.

**Possible unit of work**

> One successfully completed customer task.

---

## ACCEPTED WORK

AI activity should count as Accepted Work only when the customer task meets the product's acceptance criteria.

For example:

```text
task completed
+
output quality acceptable
+
required controls satisfied
+
acceptable customer rework
```

A model response or feature invocation alone is not Accepted Work.

---

## MEASURE

**What did it consume, and how much Accepted Work did it produce?**

Relevant evidence may include:

```text
model / token usage
retrieval and search
tool or agent calls
application infrastructure
storage / networking
observability
third-party services
human support or review
```

Useful measures may include:

```text
Accepted Work rate

Cost per Accepted Work

Cost-to-serve by feature / customer / tier

Failed or wasted AI work
```

Shared infrastructure costs should preserve their provenance:

```text
measured provider cost
+
explicit allocation rule
=
attributed feature / customer cost
```

Do not treat allocated cost as directly measured per-user or per-task cost.

---

## OUTCOME

**What changed?**

There may be two kinds of outcomes.

### Customer outcomes

Examples:

- task completed faster,
- manual effort reduced,
- workflow automated,
- quality improved,
- new capability enabled.

### SDC outcomes

Examples:

- feature adoption,
- engagement,
- retention,
- expansion,
- willingness to pay,
- new revenue.

Keep these distinct.

Customer value does not automatically imply provider value.

---

## VALUE

**What was the outcome worth?**

For an SDC, there are usually two economic lenses.

### Customer value

> Is the capability valuable enough for the customer to use, adopt, or pay for?

Potential mechanisms include:

- time saved,
- reduced manual effort,
- better decisions,
- higher productivity,
- new business capability.

### Provider economics

> Can the SDC deliver the capability sustainably?

Relevant considerations may include:

```text
revenue / price
-
AI and infrastructure cost
-
other relevant cost-to-serve
=
provider economics
```

A capability can have:

```text
high customer value
+
poor provider economics
```

or:

```text
healthy provider margin
+
weak customer value
```

Neither is a strong long-term position.

---

## EVIDENCE TO ASK FOR

A practitioner might look for:

```text
AI runtime telemetry
feature / product usage
Accepted Work evidence
customer task-success evidence
cloud / FinOps cost evidence
pricing / packaging data
revenue or entitlement data
retention / expansion data
support burden
customer research or feedback
```

Missing evidence should be labeled **Unknown**, not silently assumed.

---

## ACTION

The conversation should end with an evidence-backed next step.

| Situation | Possible action |
|---|---|
| Strong customer interest, weak proof of value | **PROVE** |
| Valuable capability, but high cost-to-serve | **OPTIMIZE** |
| Economics depend on pricing, packaging, or architecture | **RESTRUCTURE** |
| Strong customer value and healthy provider economics | **SCALE** |
| Healthy economics with no immediate expansion need | **SUSTAIN** |
| Persistent weak customer value or unsustainable economics | **PAUSE / RETIRE** |

These are decision patterns, not automatic rules.

---

## Practitioner takeaway

For this scenario, the economic chain is:

```text
Customer Task
      ↓
AI + Product + Supporting Services
      ↓
Accepted Work
      ↓
Customer Outcome
      ↓
Customer Value
      ↓
Adoption / Revenue / Retention
      ↓
Provider Economics
      ↓
PROVE / OPTIMIZE / RESTRUCTURE / SCALE / ...
```

The key question is:

> **Are we creating enough customer value while delivering the capability with sustainable product economics?**