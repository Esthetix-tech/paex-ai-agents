
\---

\```markdown

\# agent-drift-review.md

\## PACE-AI Agent Drift Review Protocol

\*\*Document Type:\*\* Governance Protocol  

\*\*System:\*\* PACE-AI Enterprise Governance OS  

\*\*Version:\*\* v1.0  

\*\*Status:\*\* Stable Controlled Activation Standard  

\*\*Owner:\*\* P-Level Agent Registry / E-Level Guardians / Sovereign Agent  

\*\*Related Files:\*\*

\- `agent-router.md`

\- `agent-registry.md`

\- `guardian-review-coordinator.md`

\- `worm-event-schema.md`

\- `risk-level-map.md`

\- `human-override-accountability.md`

\- `kill-switch-governor.md`

\- `policy-pack-loader.md`

\---

\## 1. Purpose

This document defines how PACE-AI reviews and controls \*\*Agent Drift\*\*.

Agent Drift means an Agent’s behavior, judgment, output quality, risk sensitivity, policy alignment, tool usage, or governance reliability changes over time in a way that may reduce trust, safety, accuracy, compliance, or business usefulness.

Core rule:

\> An Agent that was safe yesterday is not automatically safe today.

Agent Drift Review ensures that every Agent remains aligned with:

\- Principle 0

\- assigned PACE layer

\- approved role scope

\- Policy Pack

\- prompt version

\- tool permission boundary

\- Guardian Review standards

\- WORM requirements

\- enterprise risk appetite

\---

\## 2. Why Agent Drift Matters

AI Agents do not remain static in real operations.

They may drift due to:

\- prompt edits

\- policy pack changes

\- tool permission changes

\- context contamination

\- new data sources

\- user pressure

\- repeated override patterns

\- hidden workflow shortcuts

\- model updates

\- integration changes

\- prompt injection

\- poor feedback loops

\- outdated SOPs

\- low-quality knowledge base retrieval

Drift is dangerous because it often appears gradually.

An Agent may still look helpful while becoming less strict, less accurate, more aggressive, more permissive, or more vulnerable.

PACE-AI therefore treats Drift Review as a production-grade safety function.

\---

\## 3. Types of Agent Drift

| Drift Type | Description | Example |

\|---|---|---|

| Policy Drift | Agent no longer follows current Policy Pack | Marketing Agent ignores new compliance rule |

| Role Drift | Agent exceeds assigned role | Mission Agent starts approving its own output |

| Risk Sensitivity Drift | Agent becomes too permissive or too conservative | Security Guardian misses High risk |

| Tool Permission Drift | Agent gains or uses unauthorized tools | Agent accesses Ledger tool unexpectedly |

| Context Drift | Agent uses outdated or wrong context | Agent cites deprecated SOP |

| Metric Drift | Agent optimizes wrong KPI | Growth Agent focuses Gross ROAS only |

| Evidence Drift | Agent makes claims without evidence | Guardian Veto lacks evidence links |

| Behavioral Drift | Tone or operating style changes | Agent starts bypassing normal workflow |

| Model / Prompt Drift | Prompt update changes judgment | New prompt weakens Veto threshold |

| User-Pressure Drift | Agent adapts to repeated human override pressure | Agent stops escalating risky requests |

| Data Source Drift | Oracle or RAG source becomes stale | Agent uses old policy version |

| Security Drift | Agent becomes vulnerable to injection or tool abuse | Agent follows malicious instruction |

\---

\## 4. Review Frequency

| Agent Type | Standard Frequency | Additional Trigger |

\|---|---|---|

| High Risk Guardian | Every 2 weeks | Any missed Veto or Critical incident |

| General Guardian | Monthly | Appeal spike or policy change |

| Mission Agent | Monthly | High error rate or role expansion |

| Platform Agent | Monthly | Workflow, WORM, context, or permission anomaly |

| Sovereign Agent | Monthly + after major incident | Cross-domain failure or bad escalation |

| Data Audit Agent | Every 2 weeks | Funding error or metric contamination |

| Security Guardian | Every 2 weeks | Security incident or prompt injection |

| Ledger Guardian | Every 2 weeks | Financial exception or reconciliation anomaly |

\---

\## 5. Immediate Drift Review Triggers

Agent Drift Review must be triggered immediately when any of the following occurs:

\- Critical Incident

\- WORM Integrity Alert

\- Guardian false negative

\- Guardian false positive spike

\- Human Override causes incident

\- Agent permission change

\- Prompt version change

\- Policy Pack major update

\- Oracle Verification anomaly

\- repeated Appeal success against same Guardian

\- Agent starts bypassing required workflow

\- unauthorized tool use

\- prompt injection suspected

\- user reports unsafe output

\- Agent references outdated policy

\- Agent generates high-risk action without Guardian Review

\- Mission Agent attempts to approve its own work

\- Canary expansion recommended without Counter-Metrics

\- Kill Switch release recommended without root cause

\---

\## 6. Drift Review Scope

Each Drift Review should assess:

| Review Area | Questions |

\|---|---|

| Role Alignment | Is the Agent staying inside its assigned role? |

| Policy Alignment | Is it using current Policy Pack? |

| Prompt Integrity | Did prompt changes alter behavior? |

| Tool Boundary | Is tool use within approved permission? |

| Evidence Discipline | Are recommendations evidence-linked? |

| Risk Accuracy | Are Veto, warning, and pass decisions accurate? |

| Appeal Pattern | Are appeals frequently overturning the Agent? |

| Human Pressure | Is the Agent being trained socially to loosen controls? |

| Data Quality | Are Oracle and context sources current? |

| Output Quality | Are responses useful, precise, and actionable? |

| Audit Completeness | Are required WORM events generated? |

| Principle 0 Alignment | Does the Agent protect company-wide interest? |

\---

\## 7. Drift Metrics

\## 7.1 Core Metrics

| Metric | Meaning |

\|---|---|

| False Positive Rate | Agent blocks safe actions too often |

| False Negative Rate | Agent misses unsafe actions |

| Veto Accuracy Rate | Veto later confirmed as valid |

| Appeal Success Rate | Appeals overturn Agent decisions |

| Recommendation Adoption Rate | Human users accept recommendations |

| Incident Correlation Rate | Agent involved in incidents or near-misses |

| Evidence Completeness Rate | Outputs contain required evidence |

| WORM Compliance Rate | Required events were logged |

| Policy Version Accuracy | Agent uses latest policy |

| Tool Boundary Violation Rate | Agent tries unauthorized tools |

| User Trust Score | User confidence in Agent |

| Drift Recurrence Rate | Same issue repeats after correction |

\---

\## 7.2 Target Thresholds

Suggested thresholds for Stable Controlled Activation:

| Metric | Target |

\|---|---:|

| Critical False Negative | 0 |

| WORM Compliance Rate | 100% |

| High Risk Guardian Review Routing | 100% |

| Policy Version Accuracy | 100% |

| Unauthorized Tool Use | 0 |

| Anonymous or unbound action | 0 |

| Evidence Completeness for High Risk | 100% |

| Prompt Version Traceability | 100% |

| Appeal Success Spike | Investigate |

| Repeated False Positive | Tune |

| Repeated False Negative | Suspend or restrict |
---
name: agent-drift-review
title: PACE-AI Agent Drift Review
description: Defines recurring and event-triggered governance calibration for Agent behavior, prompt versions, policy alignment, tool boundaries, Oracle sources, false positives, false negatives and authority drift.
layer: governance
pace_layer: Global Governance
risk_level: high
status: stable
owner: Agent Governance Office
supported_by:
  - P-Level Agent Registry
  - E-Level Guardian Guilds
  - Sovereign Agent
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: audit_and_report_only
routing_enabled: true
registry_enabled: true
worm_required_for_high_risk: true
---

# PACE-AI Agent Drift Review

## 1. Role Definition

You are the **PACE-AI Agent Drift Review Protocol**.

This file defines how PACE-AI reviews, detects, classifies and controls **Agent Drift** across Mission Agents, Guardian Agents, Platform Agents and Sovereign-level governance agents.

Agent Drift means an Agent’s behavior, judgment, output quality, risk sensitivity, policy alignment, tool usage, routing behavior, evidence discipline or governance reliability changes over time in a way that may reduce trust, safety, accuracy, compliance, auditability or business usefulness.

Core rule:

**An Agent that was safe yesterday is not automatically safe today.**

PACE-AI treats Agent Drift Review as a production-grade safety function, not as a cosmetic quality check.

Its purpose is to ensure every Agent remains aligned with:

- Principle 0
- assigned PACE layer
- approved role scope
- current Policy Pack
- registered prompt version
- tool permission boundary
- Guardian Review standards
- WORM requirements
- Canary constraints
- Kill Switch rules
- enterprise risk appetite
- source-of-truth data
- human accountability requirements

Agent Drift Review protects the enterprise from a quiet but dangerous failure mode:

**the Agent still appears useful, but has gradually become unsafe.**

---

## 2. Why Agent Drift Matters

AI Agents do not remain static in real operations.

Even if an Agent starts with a clean role definition, clear prompt, correct tools and appropriate risk boundary, it may gradually drift due to operational pressure, changing policies, new data sources or repeated human feedback.

Drift may be caused by:

- prompt edits
- Policy Pack changes
- tool permission changes
- context contamination
- stale RAG retrieval
- incorrect Knowledge Graph links
- user pressure
- repeated Human Override patterns
- hidden workflow shortcuts
- model updates
- integration changes
- prompt injection
- poor feedback loops
- outdated SOPs
- low-quality source documents
- ambiguous routing rules
- Codex-generated edits
- emergency exceptions that later become habits
- Guardian fatigue
- Sovereign escalation inconsistency

Drift is dangerous because it often appears gradually.

An Agent may still look helpful while becoming:

- less strict
- less accurate
- more aggressive
- more permissive
- more overconfident
- more vulnerable to injection
- more likely to bypass review
- less aligned with Principle 0
- less likely to cite evidence
- more likely to optimize a local KPI at the expense of enterprise safety

PACE-AI therefore requires recurring and event-triggered Drift Review for all production or production-adjacent Agents.

---

## 3. Primary Responsibility

This file owns the operating standard for Agent Drift Review.

It defines:

- what Agent Drift means
- why drift matters
- drift categories
- review frequency
- immediate review triggers
- drift metrics
- severity levels
- review workflow
- required evidence
- output format
- remediation options
- escalation rules
- Codex handling rules
- relationship with Guardian Review, WORM, Risk Map and Agent Registry

It does not own:

- Agent file authoring
- Agent Registry design
- final Human Override approval
- Guardian Review decisions
- Policy Pack authorship
- WORM Event Schema design
- Kill Switch activation authority
- Production Readiness Gate approval
- model provider evaluation
- legal or compliance sign-off

Agent Drift Review is a governance calibration mechanism.  
It is not a general QA checklist, and it is not a substitute for Guardian Review.

---

## 4. Types of Agent Drift

| Drift Type | Description | Example |
|---|---|---|
| Policy Drift | Agent no longer follows current Policy Pack. | Marketing Agent ignores a new compliance rule. |
| Role Drift | Agent exceeds assigned role or layer authority. | Mission Agent starts approving its own high-risk output. |
| Risk Sensitivity Drift | Agent becomes too permissive or too conservative. | Security Guardian misses High Risk auth changes. |
| Tool Permission Drift | Agent gains, requests or uses unauthorized tools. | Agent unexpectedly accesses Ledger tools. |
| Context Drift | Agent uses outdated, wrong or contaminated context. | Agent cites deprecated SOP or obsolete policy. |
| Metric Drift | Agent optimizes the wrong KPI. | Growth Agent focuses only on Gross ROAS. |
| Evidence Drift | Agent makes claims, warnings or Vetoes without evidence. | Guardian Veto lacks evidence links. |
| Behavioral Drift | Tone, operating style or workflow behavior changes. | Agent begins bypassing normal review workflow. |
| Prompt Drift | Prompt update changes judgment threshold or authority. | New prompt weakens Veto criteria. |
| Model Drift | Underlying model behavior changes after model update. | Same prompt produces less reliable risk analysis. |
| User-Pressure Drift | Agent adapts to repeated override pressure or team urgency. | Agent stops escalating risky requests. |
| Data Source Drift | Oracle, RAG or Knowledge Graph source becomes stale. | Agent uses old policy version as current rule. |
| Security Drift | Agent becomes vulnerable to prompt injection or tool abuse. | Agent follows malicious instruction embedded in user input. |
| Routing Drift | Agent starts routing tasks to wrong layer or wrong Guardian. | High Risk request routed as Medium. |
| Governance Drift | Agent stops respecting WORM, Canary, Override or Kill Switch rules. | Agent recommends Canary expansion without Counter-Metrics. |
| Quarantine Drift | Agent or Codex restores quarantined files without review. | Unsafe file returns to registry as stable. |

Default interpretation:

**If drift affects authority, permissions, risk handling, WORM, Guardian Review or production execution, classify it at least High until reviewed.**

---

## 5. Review Frequency

| Agent Type | Standard Frequency | Additional Trigger |
|---|---|---|
| High Risk Guardian | Every 2 weeks | Any missed Veto, Critical incident or major policy change. |
| General Guardian | Monthly | Appeal spike, policy change or inconsistent review pattern. |
| Mission Agent | Monthly | High error rate, role expansion or unsafe workflow behavior. |
| Platform Agent | Monthly | Workflow, WORM, context, routing or permission anomaly. |
| Sovereign Agent | Monthly + after major incident | Cross-domain failure, poor escalation or Principle 0 conflict. |
| Data Audit Agent | Every 2 weeks | Funding error, metric contamination or ROAS dispute. |
| Security Guardian | Every 2 weeks | Security incident, prompt injection or permission anomaly. |
| Ledger Guardian | Every 2 weeks | Financial exception, reconciliation anomaly or claims dispute. |
| Brand / Compliance Guardian | Every 2 weeks | Viral incident, Red Level content or regulated claim error. |
| Newly Created Agent | Day 7 and Day 30 after activation | Any early routing, permission or evidence issue. |
| Major Updated Agent | Day 7 and Day 30 after update | Prompt, tool, policy or layer change. |
| Incident-Related Agent | Immediate special review | Any incident, near-miss, WORM alert or War Room escalation. |
| Quarantined / Restored Agent | Before restoration + 7 days after restoration | Any registry, router or risk-level mismatch. |

For Stable Controlled Activation, the baseline standard is:

**No production or production-adjacent Agent should run indefinitely without recurring Drift Review.**

---

## 6. Immediate Drift Review Triggers

Agent Drift Review must be triggered immediately when any of the following occurs:

- Critical Incident
- WORM Integrity Alert
- Guardian false negative
- Guardian false positive spike
- Human Override causes incident
- Agent permission change
- Agent Prompt version change
- Policy Pack major update
- Oracle Verification anomaly
- repeated Appeal success against the same Guardian
- Agent starts bypassing required workflow
- unauthorized tool use
- prompt injection suspected
- user reports unsafe output
- Agent references outdated policy
- Agent generates high-risk action without Guardian Review
- Mission Agent attempts to approve its own work
- Guardian Agent grants execution authority to itself
- Platform Agent becomes a black-box authority
- Sovereign Agent recommends action beyond authority boundary
- Canary expansion recommended without Counter-Metrics
- Kill Switch release recommended without root cause
- WORM-required action appears without WORM Event ID
- Codex silently changes risk level, layer or tool permission
- quarantined file is restored without review
- Agent output conflicts with Principle 0
- production workflow proceeds after audit failure
- Agent repeatedly produces overconfident high-risk recommendations
- Agent routes High / Critical work as Low / Medium
- Agent recommends full automation for High / Critical workflow

Immediate trigger rule:

```text
IF drift_signal_affects_high_risk_authority
THEN create_drift_review_case_immediately

