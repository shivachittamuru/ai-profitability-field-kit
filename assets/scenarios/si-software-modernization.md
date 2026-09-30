# SI — AI-Assisted Software Modernization

## Scenario

A System Integrator is helping a customer modernize an existing software estate using coding agents or other AI-assisted development capabilities.

Examples may include:

- application migration,
- framework or language upgrades,
- cloud modernization,
- API modernization,
- refactoring,
- test generation,
- legacy-code transformation.

The profitability question is not simply:

> **How much does the coding agent cost?**

It is:

> **Is AI helping the customer complete accepted modernization work faster or more economically without degrading quality, security, or maintainability?**

---

## WORK

**Work to be accomplished**

Complete modernization tasks safely and efficiently.

**Possible unit of work**

> One accepted modernization task, story, module, or migration increment.

The unit should align to something the engineering organization already recognizes as completed work.

---

## ACCEPTED WORK

AI-generated code or a completed agent run should not automatically count as Accepted Work.

A modernization unit may count only when it satisfies the customer's required engineering controls.

For example:

```text
implementation completed
+
build succeeds
+
required tests pass
+
security / quality checks pass
+
human review accepted
+
acceptance criteria satisfied
=
Accepted Work
```

The exact criteria will vary by engineering organization and workload.

---

## MEASURE

**What did the work consume, and how much Accepted Work did it produce?**

Relevant evidence may include:

```text
coding-agent / model usage
tokens
repo searches / file reads
tool and shell calls
code edits
build / test attempts
CI/CD usage
developer review
developer rework
cloud / development infrastructure
```

Useful measures may include:

```text
Accepted Work rate

AI cost per Accepted Work

Total delivery cost per Accepted Work

Developer effort per Accepted Work

Rework per Accepted Work

Build / test attempts per Accepted Work

Cycle time per Accepted Work
```

Failed attempts still consume resources and should remain visible.

Relevant cost should not be limited to inference when developer review, rework, CI, or supporting infrastructure are economically material.

---

## OUTCOME

**What changed?**

Potential customer outcomes may include:

- faster modernization throughput,
- shorter engineering cycle time,
- reduced manual transformation effort,
- lower rework,
- fewer migration defects,
- increased test coverage,
- faster completion of modernization milestones,
- additional engineering capacity.

Keep the evidence chain explicit:

```text
Generated code
≠ Accepted Work
≠ Business Outcome
≠ Incremental Outcome
```

For example, an AI-assisted team may complete more tasks, but the improvement relative to the prior delivery process still needs to be established.

---

## VALUE

**Whose economics matter?**

The primary lens is usually the customer's **delivery and program economics**.

Potential value mechanisms include:

```text
shorter cycle time
        ↓
more modernization work completed
        ↓
earlier program completion / capacity released
        ↓
economic value
```

or:

```text
less developer effort / rework
        ↓
lower delivery effort per accepted task
        ↓
lower modernization cost or additional capacity
```

Other potential value may come from:

- faster retirement of legacy systems,
- earlier cloud migration benefits,
- reduced maintenance burden,
- reduced technical debt,
- lower defect remediation,
- accelerated product delivery.

Avoid automatically converting developer hours saved into financial savings unless there is a credible mechanism for capturing the benefit.

---

## EVIDENCE TO ASK FOR

Relevant evidence may include:

- coding-agent runtime and usage telemetry,
- source-control activity,
- build and test results,
- CI/CD data,
- static analysis and security checks,
- pull-request or review evidence,
- engineering work-item data,
- developer effort or rework data,
- baseline delivery metrics,
- program cost and milestone data.

Missing evidence should be treated as **Unknown**, not silently assumed.

---

## ACTION

This scenario may support decisions such as:

**PROVE / OPTIMIZE / RESTRUCTURE / SCALE / SUSTAIN**

Typical patterns:

| Situation | Possible action |
|---|---|
| Agent produces code, but accepted delivery improvement is unclear | **PROVE** |
| Accepted Work is strong, but retries/rework or model cost are high | **OPTIMIZE** |
| Workflow or engineering process prevents AI from creating useful progress | **RESTRUCTURE** |
| Accepted Work and delivery outcomes improve with attractive next-dollar economics | **SCALE** |
| Economics are healthy at the current scope | **SUSTAIN** |

These are decision patterns, not automatic rules.

---

## Practitioner takeaway

For this scenario, the economic chain is:

```text
Modernization Task
        ↓
AI + Developer + Engineering Systems
        ↓
Accepted Engineering Work
        ↓
Delivery / Program Outcome
        ↓
Customer Economic Value
        ↓
PROVE / OPTIMIZE / RESTRUCTURE / SCALE / ...
```

The key question is:

> **Are we converting AI-assisted development into accepted modernization work that improves the customer's delivery economics—not simply generating code faster?**