---
name: Governance Protocols Index
title: PAEX-AI Sovereign Governance Protocols Index
description: Sovereign-level index for core governance protocols, activation orders, decision playbooks, escalation controls and company-level routing logic used by PAEX-AI Enterprise Governance OS.
layer: sovereign
pace_layer: C-Level / Global Governance
risk_level: high
status: stable
owner: Sovereign Governance Office
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: true
registry_enabled: true
version: v1.0
related_files:
  - governance/core-governance-protocols.md
  - governance/worm-event-schema.md
  - governance/canary-release-governor.md
  - governance/guardian-review-coordinator.md
  - governance/human-override-accountability.md
  - governance/kill-switch-governor.md
  - governance/agent-drift-review.md
  - governance/production-readiness-gate.md
  - governance/controlled-production-activation-order.md
  - governance/stable-controlled-activation-order.md
  - sovereign/principle-0-charter.md
  - sovereign/sovereign-agent.md
  - sovereign/sovereign-decision-playbook.md
  - sovereign/cross-domain-war-room-playbook.md
  - sovereign/controlled-production-activation-order.md
  - sovereign/stable-controlled-activation-order.md
  - agent-registry/registry-maintenance-policy.md
  - agent-registry/risk-level-map.md
  - agent-registry/layer-map.md
  - _quarantine/quarantine-policy.md
---

# PAEX-AI Sovereign Governance Protocols Index

## 1. Purpose

This file defines how the `sovereign/` layer references, summarizes and routes to the major governance protocols used by PAEX-AI Enterprise Governance OS.

It is the sovereign-level command index for:

- core governance laws;
- executive decision protocols;
- Principle 0 interpretation;
- controlled production activation;
- War Room escalation;
- Kill Switch decisions;
- Human Override accountability;
- Guardian Review routing;
- WORM audit requirements;
- Canary release constraints;
- Agent Drift calibration;
- production readiness gates;
- repository registry and quarantine governance.

This file does not replace the detailed operating standards under `agents/governance/`.

Instead, it tells humans, Codex, Sovereign Agent and orchestration tools which governance protocol should be consulted before acting.

Core rule:

> Governance owns the operating law. Sovereign applies that law to company-level decisions.

The purpose of this index is to prevent PAEX-AI from making high-risk decisions by intuition, convenience or routing guesswork.

When a decision touches company-wide interest, this index should help answer:

- Which protocol governs this situation?
- Which file is the master standard?
- Which file is only an executive summary or routing reference?
- Should this go to Guardian Review?
- Should this go to Sovereign Decision?
- Should this enter War Room?
- Does this require WORM?
- Does this require Human Override?
- Does this require Kill Switch review?
- Can Codex safely assist, or must a human / Guardian / Sovereign reviewer intervene?

---

## 2. Sovereign Positioning

This file belongs to the `sovereign/` layer.

Its function is not to execute frontline work.

Its function is to provide company-level governance navigation.

In the PAEX model:

| Layer | Governance Meaning |
|---|---|
| `core/` | Strategic planning, executive analysis, finance, market strategy and portfolio-level thinking. |
| `mission/` | Task execution, value creation, production work and operational delivery. |
| `guardian/` | Professional review, risk detection, compliance, safety, evidence review and veto authority. |
| `platform/` | Infrastructure, tools, registry, workflow, data, WORM, Oracle and shared operating support. |
| `governance/` | Master operating protocols and enforceable governance standards. |
| `sovereign/` | Highest-level company decision framing, Principle 0, escalation, activation orders and War Room control. |
| `agent-registry/` | Repository-level routing, responsibility, capability, risk and layer mapping. |
| `_quarantine/` | Temporary containment for unsafe, unclear, incomplete or mis-layered files. |

The `sovereign/` layer should not become a duplicate of `governance/`.

It should function as the executive command layer that points to the correct governance law and applies it to company-level decision contexts.

---

## 3. Master File Rule

`agents/governance/core-governance-protocols.md` is the master protocol file for core governance operations.

If a similarly named file exists under `agents/sovereign/`, it should act only as one of the following:

- a sovereign charter summary;
- an executive-facing reference;
- a routing entry;
- a decision index;
- a high-level activation statement;
- a cross-protocol navigation layer.

It must not diverge from the governance master.

If there is a conflict between a governance file and a sovereign file:

1. The governance file controls operating detail.
2. The sovereign file controls executive framing and escalation routing.
3. If the conflict affects High / Critical workflows, create or reference a WORM Event.
4. Route the conflict to Guardian Review and Sovereign Decision Playbook.
5. Update this index after resolution.

Core rule:

> One law, many views. Governance is the law; Sovereign is the command interpretation.

---

## 4. Protocol Index

| Protocol / Artifact | Master or Reference File | Sovereign Use |
|---|---|---|
| Principle 0 | `sovereign/principle-0-charter.md` | Supreme decision criterion for company-wide interest. |
| Sovereign Agent | `sovereign/sovereign-agent.md` | Cross-domain synthesis, escalation framing and executive recommendation. |
| Sovereign Decision Playbook | `sovereign/sovereign-decision-playbook.md` | Structured decision package for company-level judgment. |
| Cross-Domain War Room | `sovereign/cross-domain-war-room-playbook.md` | Critical cross-domain incident coordination and executive crisis cockpit. |
| Core Governance Protocols | `governance/core-governance-protocols.md` | Master law for WORM, Canary, Override, Kill Switch, Guardian Review, Drift Review and Production Readiness. |
| WORM Audit | `governance/worm-event-schema.md` | Immutable truth ledger and audit evidence standard. |
| Canary Release | `governance/canary-release-governor.md` | Controlled release, blast radius, Soak Time, Counter-Metrics and abort criteria. |
| Guardian Review | `governance/guardian-review-coordinator.md` | Professional review, evidence requirements, Veto coordination and appeal path. |
| Human Override | `governance/human-override-accountability.md` | Responsibility signature for human exceptions and AI / Guardian override. |
| Kill Switch | `governance/kill-switch-governor.md` | Stop, degrade, freeze, rollback, quarantine, release and recovery authority. |
| Agent Drift Review | `governance/agent-drift-review.md` | Recurring calibration of Agent behavior, prompt alignment, tool use and policy fit. |
| Production Readiness Gate | `governance/production-readiness-gate.md` | Final pre-production governance gate. |
| Controlled Production Activation | `sovereign/controlled-production-activation-order.md` and `governance/controlled-production-activation-order.md` | Sovereign authorization and governance operating standard for real production entry. |
| Stable Controlled Activation | `sovereign/stable-controlled-activation-order.md` and `governance/stable-controlled-activation-order.md` | 30-day observation and stable transition criteria. |
| Registry Governance | `agent-registry/registry-maintenance-policy.md` | Registry consistency, routing safety, responsibility mapping and capability control. |
| Frontmatter Schema | `agent-registry/frontmatter-schema.md` | Required metadata contract for all formal Agent and governance files. |
| Risk Level Map | `agent-registry/risk-level-map.md` | Risk classification logic and execution boundary. |
| Layer Map | `agent-registry/layer-map.md` | Repository layer rules and PAEX placement logic. |
| Quarantine Policy | `_quarantine/quarantine-policy.md` | Unsafe file containment, review, repair and restoration rules. |
| Quarantine README | `_quarantine/README.md` | Repository-level explanation of quarantine categories and Codex boundaries. |

---

## 5. Routing Guidance

Use this section when deciding which file should answer a question.

### 5.1 Use Sovereign Files When the Question Is Company-Level

Route to `sovereign/` when the question is:

- Should the company proceed?
- Does this violate Principle 0?
- Is this a company-wide risk?
- Should this become a War Room?
- Should funding freeze or unlock?
- Should a Kill Switch trigger or remain active?
- Can a Kill Switch be released?
- Can Controlled Production Activation proceed?
- Can Stable Controlled Activation proceed?
- Which governance protocol applies at the executive level?
- How should conflicting Guardian positions be summarized?
- What decision package should be presented to human leadership?

Typical sovereign routing targets:

| Situation | Route To |
|---|---|
| Company-wide risk judgment | `sovereign/sovereign-decision-playbook.md` |
| Principle 0 interpretation | `sovereign/principle-0-charter.md` |
| Cross-domain incident | `sovereign/cross-domain-war-room-playbook.md` |
| Production entry decision | `sovereign/controlled-production-activation-order.md` |
| Stable transition decision | `sovereign/stable-controlled-activation-order.md` |
| Cross-protocol navigation | `sovereign/governance-protocols-index.md` |
| Sovereign Agent role boundary | `sovereign/sovereign-agent.md` |

---

### 5.2 Use Governance Files When the Question Is an Operating Rule

Route to `governance/` when the question is:

- What is the exact operating rule?
- What fields are required?
- What workflow must be followed?
- What evidence is mandatory?
- What triggers WORM?
- What triggers Canary?
- What triggers Kill Switch?
- What allows or blocks Human Override?
- What is the Guardian Review output format?
- What conditions trigger abort, hold, release or escalation?
- What is required before production activation?

Typical governance routing targets:

| Situation | Route To |
|---|---|
| General governance law | `governance/core-governance-protocols.md` |
| Immutable audit event | `governance/worm-event-schema.md` |
| Controlled release | `governance/canary-release-governor.md` |
| Guardian decision | `governance/guardian-review-coordinator.md` |
| Human override | `governance/human-override-accountability.md` |
| Stop / rollback / release | `governance/kill-switch-governor.md` |
| Agent behavior drift | `governance/agent-drift-review.md` |
| Production readiness | `governance/production-readiness-gate.md` |

---

### 5.3 Use Agent Registry Files When the Question Is About Repository Routing

Route to `agent-registry/` when the question is:

- Which agent owns this capability?
- Which file should receive this task?
- Which layer does this file belong to?
- Is the file production-ready?
- What risk level applies?
- Which Guardian hook is required?
- Which capability tags are available?
- Is routing enabled?
- Is registry activation enabled?
- Does this file duplicate another responsibility?

Typical registry routing targets:

| Situation | Route To |
|---|---|
| Agent list | `agent-registry/agent-index.md` |
| Ownership | `agent-registry/agent-responsibility-matrix.md` |
| Task routing | `agent-registry/agent-router.md` |
| Capabilities | `agent-registry/capability-map.md` |
| Layer placement | `agent-registry/layer-map.md` |
| Risk classification | `agent-registry/risk-level-map.md` |
| Secondary reviewers / hooks | `agent-registry/secondary-hooks-map.md` |
| Metadata requirements | `agent-registry/frontmatter-schema.md` |
| Registry repair rules | `agent-registry/registry-maintenance-policy.md` |

---

### 5.4 Use Quarantine Files When the Question Is About Unsafe or Ambiguous Files

Route to `_quarantine/` when the question is:

- Why is this file unsafe?
- Why was this file removed from routing?
- What is missing before restoration?
- Is the layer wrong?
- Is the risk level unclear?
- Does this file imply unsafe permissions?
- Does this file duplicate another responsibility?
- Can Codex move, repair or restore it?
- What review is required before restoration?

Typical quarantine routing targets:

| Situation | Route To |
|---|---|
| General quarantine rules | `_quarantine/quarantine-policy.md` |
| Quarantine explanation | `_quarantine/README.md` |
| Content mismatch | `_quarantine/content-mismatch/content-mismatch.md` |
| Duplicate responsibility | `_quarantine/duplicate-responsibility/duplicate-responsibility.md` |
| Missing frontmatter | `_quarantine/missing-frontmatter/missing-frontmatter.md` |
| Unclear risk level | `_quarantine/unclear-risk-level/unclear-risk-level.md` |
| Unsafe permission | `_quarantine/unsafe-permission/unsafe-permission.md` |
| Wrong layer | `_quarantine/wrong-layer/wrong-layer.md` |
| Human decision required | `_quarantine/pending-human-review/pending-human-review.md` |

---

## 6. Sovereign Decision Routing Matrix

Use the following matrix to determine whether a situation should remain in normal workflow, go to Guardian Review, move to Sovereign Decision, or escalate to War Room.

| Condition | Required Route |
|---|---|
| Low-risk drafting or summarization | Mission / Core / Platform according to router. |
| Medium-risk external or cross-team action | Guardian Review. |
| High-risk funding, brand, security, IoT, Ledger-adjacent or claims workflow | Guardian Review + WORM + Canary / relevant governance protocol. |
| Human wants to override Guardian / AI warning | Human Override Accountability + WORM + Sovereign visibility if High+. |
| Workflow cannot be audited | WORM Event Schema / block until audit restored. |
| High-risk rollout needs testing | Canary Release Governor. |
| Risk must be stopped, degraded, frozen or rolled back | Kill Switch Governor. |
| Agent behavior appears misaligned | Agent Drift Review. |
| Production launch or major activation | Production Readiness Gate + Controlled Production Activation Order. |
| Company-wide interest conflict | Principle 0 Charter + Sovereign Decision Playbook. |
| Cross-domain incident or Critical exposure | Cross-Domain War Room Playbook. |
| File is unsafe, unclear or mis-layered | Quarantine Policy. |
| Registry routing is inconsistent | Registry Maintenance Policy. |

Routing rule:

> When local routing and company-wide risk conflict, route upward.

---

## 7. Conflict Resolution

If two files appear to conflict, apply the following sequence.

```text
Conflict Detected
→ Identify whether each file is Governance, Sovereign, Registry, Mission, Guardian, Platform or Quarantine
→ Check Master File Rule
→ Compare frontmatter, status, risk level and owner
→ Determine whether conflict affects routing, authority, permissions or High / Critical workflow
→ If High / Critical, create or reference WORM Event
→ Route to Guardian Review if operating rule is unclear
→ Route to Sovereign Decision Playbook if company-level judgment is required
→ Update this index after resolution
