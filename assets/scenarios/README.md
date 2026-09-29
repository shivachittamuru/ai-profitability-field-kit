# Scenario Profiles

These profiles show how the common AI Profitability reasoning model translates across different partner types and workloads.

The core questions remain stable:

WORK → MEASURE → OUTCOME → VALUE → ACTION

What changes by scenario are the unit of work, acceptance criteria, cost boundary, business outcome, value mechanism, evidence sources, and decision context.

Start with the matrix below, then open an individual scenario only if you need more detail.

# AI Profitability Scenario Matrix

The same five questions apply across partner types:

```text
WORK → MEASURE → OUTCOME → VALUE → ACTION
```

What changes is the **unit of work, acceptance criteria, value mechanism, and decision context**.

| Partner / Scenario | WORK | ACCEPTED WORK | MEASURE | OUTCOME | VALUE LENS | Typical ACTION |
|---|---|---|---|---|---|---|
| **SI — Customer Support Agent** | Resolve customer issues accurately and efficiently | Issue resolved correctly, grounded, compliant, with acceptable rework/escalation | AI + tool + infrastructure cost, human review/rework, cost per Accepted Work | Resolution, FCR, handling time, escalation, capacity | Customer operating economics | **PROVE / OPTIMIZE / SCALE** |
| **SI — AI-Assisted Software Modernization** | Complete modernization work safely and faster | Engineering task passes build, tests, review, security and acceptance criteria | Coding-agent usage + developer effort + CI/test/rework cost | Throughput, cycle time, defects, program velocity | Customer delivery/program economics | **PROVE / OPTIMIZE / SCALE** |
| **SI — AI FinOps / Architecture Optimization** | Improve the economics of an AI workload without harming required quality | Architecture/configuration change produces verified cost or efficiency improvement while preserving acceptance criteria | Before/after cloud cost, utilization, AI usage, Accepted Work, quality | Lower cost per Accepted Work, reduced waste, improved capacity | Customer workload economics | **OPTIMIZE / RESTRUCTURE / SUSTAIN** |
| **SDC / ISV — Embedded AI Copilot** | Help product users complete valuable tasks | Customer task completed with acceptable quality, controls and rework | AI cost per Accepted Work, shared infrastructure, feature usage | Task success, adoption, engagement, retention, willingness to pay | **Customer value + provider economics** | **PROVE / OPTIMIZE / RESTRUCTURE / SCALE** |
| **SDC / ISV — Domain-Specific Agentic Workflow** | Complete a multi-step domain workflow reliably | End-to-end workflow meets domain, quality and control requirements | Model/tool/subagent activity, infrastructure, retries, human intervention | Workflow completion, cycle time, automation, quality | Customer process value + provider cost-to-serve | **PROVE / OPTIMIZE / SCALE** |
| **SDC / ISV — Usage-Based Agentic SaaS** | Deliver repeatable AI-powered customer outcomes at scale | Billable/customer workflow successfully completes to agreed criteria | Cost per Accepted Work by customer/feature/tier, utilization, shared cost | Usage, retention, expansion, successful customer outcomes | **Customer value + revenue + gross-margin/unit economics** | **OPTIMIZE / RESTRUCTURE / SCALE / SUSTAIN** |

---

## What stays common

Across all six scenarios:

```text
Start with the WORK
        ↓
Define ACCEPTED WORK
        ↓
Measure the resources required to produce it
        ↓
Observe the downstream OUTCOME
        ↓
Translate that outcome into VALUE
        ↓
Use the evidence to choose an ACTION
```

## What deliberately changes

Each scenario defines its own:

```text
unit of work
acceptance criteria
cost boundary
human contribution
business outcome
value mechanism
evidence sources
decision thresholds
```

> **Standardize the reasoning. Customize the business semantics.**

---

## Three findings worth carrying forward

**1. Accepted Work generalizes well.**  
A support resolution, accepted code change, completed domain workflow, and successful customer task are very different—but all need an explicit acceptance boundary before AI activity becomes economically meaningful.

**2. Measure the production system, not only the model.**  
Depending on the scenario, relevant economics may include AI, cloud infrastructure, tools, human review, rework, and other supporting costs.

**3. Be explicit about whose economics matter.**  
For an SI engagement, customer economics may dominate. For an ISV, both **customer value** and **provider economics** may need to work for the investment to be sustainable.