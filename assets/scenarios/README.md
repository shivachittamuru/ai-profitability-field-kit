# Scenario Profiles

Scenario Profiles show how the common AI Profitability approach translates across different partner types and AI workloads.

The core questions remain stable:

```text
WORK → MEASURE → OUTCOME → VALUE → ACTION
```

What changes by scenario are the:

```text
unit of work
acceptance criteria
cost boundary
human contribution
business outcome
value mechanism
evidence sources
decision context
```

> **Standardize the reasoning. Customize the business semantics.**

Use the matrix below for a quick comparison, then open an individual scenario when you need more detail.

---

# Scenario Matrix

| Partner / Scenario | WORK | ACCEPTED WORK | MEASURE | OUTCOME | VALUE LENS | Typical ACTION |
|---|---|---|---|---|---|---|
| **SI — Customer Support Agent** | Resolve customer issues accurately and efficiently | Issue resolved correctly, grounded, compliant, with acceptable rework/escalation | AI + tool + infrastructure cost, human review/rework, cost per Accepted Work | Resolution, FCR, handling time, escalation, capacity | Customer operating economics | **PROVE / OPTIMIZE / SCALE** |
| **SI — AI-Assisted Software Modernization** | Complete modernization work safely and faster | Engineering task passes build, tests, review, security, and acceptance criteria | Coding-agent usage + developer effort + CI/test/rework cost | Throughput, cycle time, defects, program velocity | Customer delivery / program economics | **PROVE / OPTIMIZE / SCALE** |
| **SI — AI FinOps / Architecture Optimization** | Improve AI workload economics without harming required quality | Architecture or configuration change produces verified efficiency improvement while preserving acceptance criteria | Before/after cloud cost, utilization, AI usage, Accepted Work, quality | Lower cost per Accepted Work, reduced waste, improved capacity | Customer workload economics | **OPTIMIZE / RESTRUCTURE / SUSTAIN** |
| **SDC — Embedded AI Copilot** | Help product users complete valuable tasks | Customer task completed with acceptable quality, controls, and rework | AI cost per Accepted Work, shared infrastructure, feature usage | Task success, adoption, engagement, retention, willingness to pay | **Customer value + provider economics** | **PROVE / OPTIMIZE / RESTRUCTURE / SCALE** |
| **SDC — Domain-Specific Agentic Workflow** | Complete a multi-step domain workflow reliably | End-to-end workflow meets domain, quality, and control requirements | Model/tool/subagent activity, infrastructure, retries, human intervention | Workflow completion, cycle time, automation, quality | Customer process value + provider cost-to-serve | **PROVE / OPTIMIZE / SCALE** |
| **SDC — Usage-Based Agentic SaaS** | Deliver repeatable AI-powered customer outcomes at scale | Customer workflow successfully completes to agreed criteria | Cost per Accepted Work by customer/feature/tier, utilization, shared cost | Usage, retention, expansion, successful customer outcomes | **Customer value + revenue + gross-margin/unit economics** | **OPTIMIZE / RESTRUCTURE / SCALE / SUSTAIN** |

---

# Available Scenario Profiles

## SI 

- [Customer Support Agent](si-customer-support-agent.md)
- [AI-assisted Software Modernization](si-software-modernization.md)

More SI scenarios will be added as they are validated.

## SDC

- [Embedded AI Copilot](sdc-embedded-ai-copilot.md)
- [Domain-Specific Agentic Workflow](sdc-domain-specific-agents.md)

More SDC scenarios will be added as they are validated.

---

# What stays common

Across scenarios:

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

---

# What deliberately changes

Each scenario may define its own:

```text
unit of work
acceptance criteria
cost attribution
human involvement
business outcome
value mechanism
evidence sources
decision thresholds
```

This is intentional.

The field kit provides a common reasoning model without forcing unrelated workloads into identical metrics.

---

# Current learnings

Three findings are carrying forward so far:

### 1. Accepted Work generalizes well

A support resolution, accepted code change, completed domain workflow, and successful customer task are different forms of work, but each needs an explicit acceptance boundary before AI activity becomes economically meaningful.

### 2. Measure the production system, not only the model

Relevant economics may include AI, cloud infrastructure, tools, human review, rework, and other supporting resources.

### 3. Be explicit about whose economics matter

For an SI engagement, customer economics may dominate.

For an SDC, both **customer value** and **provider economics** may need to work for the AI capability to be sustainable.

---

# How to use these profiles

Use a Scenario Profile when you need to quickly answer:

- What does **Accepted Work** mean here?
- What should we measure?
- Which business outcomes matter?
- Where could economic value come from?
- What evidence should we ask for?
- What decisions could the analysis support?

For the general conversation method, use the [AI Profitability Partner Playbook](../playbook/partner-playbook.md).