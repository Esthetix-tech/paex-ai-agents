---
name: Agent Router
title: PAEX-AI Agent Router
description: Routing rules for matching tasks to C-A-E-P agents, Business Architecture Context Stack layers, risk levels and mandatory secondary hooks.
layer: agent-registry
context_layer: Repository Governance
pace_layer: Repository Governance / Routing
risk_level: high
status: active_candidate
owner: Agent Repository Steward
review_required: true
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-candidate-patch-03
requires_worm: true
worm_scope:
  - activation
  - router_policy_change
  - high_or_critical_routing_exception_review
  - forbidden_action_policy_change_request
  - quarantine_restore_review
requires_guardian_review: true
human_approval_required: true
human_approval_scope:
  - file_activation
  - router_policy_change
  - high_or_critical_routing_exception_review
  - forbidden_action_policy_change_request
  - quarantine_restore_review
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - route_before_classification
  - route_high_or_critical_without_required_hooks
  - route_quarantined_files_as_active
  - allow_mission_self_approval_for_high_or_critical_work
  - allow_guardian_hidden_production_execution
  - allow_sovereign_direct_irreversible_execution
rollback_required: true
canary_required: false
related_files:
  - ../risk-level-map/risk-level-map.md
  - ../secondary-hooks-map/secondary-hooks-map.md
  - ../frontmatter-schema/frontmatter-schema.md
  - ../registry-maintenance-policy/registry-maintenance-policy.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
  - ../../governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
---

# Agent Router｜PAEX-AI Agent Router

## 1. Purpose

This file defines how Codex routes tasks inside the PAEX-AI `agents/` repository.

Core rule:

> Route before execution. Classify before routing. Hook before high-risk action.

Plain-language interpretation:

> 先判斷層級，再決定誰做，再決定誰審。不要看到有人會做，就直接派給他。

This router prevents capable-but-unauthorized execution, high-risk work without Guardian hooks, application-specific logic contaminating ESTRIX Core, and quarantined files becoming active routing targets.

## 1.1 Scope and Non-Scope

This router applies to:
- task-to-agent routing;
- Business Architecture Context Stack classification;
- C-A-E-P layer routing;
- risk-level routing;
- secondary hook attachment;
- candidate file validation;
- quarantine routing;
- repository governance routing.

This router does not:
- execute tasks directly;
- approve High or Critical work;
- replace Guardian Review;
- replace Sovereign decision packages;
- replace K / CEO final decision;
- replace CI test results;
- replace legal, security, privacy, finance or compliance sign-off.
---

## 2. Router Inputs

Before routing, Codex must identify the user request, Business Architecture Context Layer, C-A-E-P governance layer, risk level, capability domain, required hooks, evidence, human approval need, affected files/systems, candidate file if known, routing status, tool permission boundary and whether the work is reusable, application-specific or one-time.

---

## 3. Business Architecture Pre-Classification

| Layer | Use When |
|---|---|
| L0｜K Command | Company-level authority, portfolio, ownership, final decision, non-delegable action |
| L1｜Esthetix Arsenal | Esthetix positioning, governance OS, AI / SaaS / Agent infrastructure strategy |
| L2｜ESTRIX Core | Reusable core engine modules, shared data, workflow, permission, audit, CRM, booking, billing |
| L3｜Application / Use Case | Specific brand, vertical, use case, SoMatch, SHINES, service packaging |
| L4｜Engagement / Project | One-time task, client, campaign, sprint, report, version, project delivery |

If unclear, return HOLD using the standardized HOLD format.

---

## 4. C-A-E-P Routing Map

| Governance Layer | Route To | May Do | Must Not Do |
|---|---|---|---|
| C｜Core Strategy | `agents/core/` | strategy, roadmap, portfolio, decision package, revenue intelligence | irreversible execution |
| A｜Mission | `agents/mission/` | execution, delivery, operations, campaigns, engineering tasks | self-approve High / Critical work |
| E｜Guardian | `agents/guardian/` | review, verify, audit, veto, enforce standards | hidden production execution |
| P｜Platform | `agents/platform/` | reusable infrastructure, tooling, registry, data pipeline, SRE, design system | final business authorization |
| Sovereign | `agents/sovereign/` | arbitration package, Principle 0, Kill Switch package, Human Override package | direct irreversible execution |
| Governance | `agents/governance/` | define protocol | execute normal business work |
| Registry | `agents/agent-registry/` | define routing/schema/risk metadata | execute work |
| Shared | `agents/shared/` | provide reusable templates | act as routing target |
| Quarantine | `agents/_quarantine/` | isolate unsafe files | active routing |

---

## 5. Routing Decision Values

Codex must use one of:

```text
PROCEED
HOLD
BLOCK
ESCALATE
```

Use `PROCEED` when risk is controlled and required hooks exist.
Use `HOLD` when more evidence, approval, classification, registry sync, file repair or review is needed.
Use `BLOCK` when action violates governance, law, platform safety, security, privacy, quarantine or non-negotiable boundaries.
Use `ESCALATE` when Sovereign, K / CEO or an authorized human decision is required.

## Router Decision Matrix

| Condition | Router Decision |
|---|---|
| Classification clear, risk controlled, hooks satisfied, candidate file valid | PROCEED |
| Layer unclear, evidence missing, hooks missing, frontmatter mismatch, review pending | HOLD |
| Law / security / privacy / platform safety violated, forbidden action requested, quarantined file routed as active | BLOCK |
| Critical risk, irreversible decision, Sovereign boundary, K / CEO decision required | ESCALATE |

---

## 6. Mandatory Routing Algorithm

```text
1. Parse task.
2. Identify affected business entity.
3. Classify Business Architecture Layer: L0 / L1 / L2 / L3 / L4.
4. Classify PACE layer: C / A / E / P / Sovereign / Governance / Registry / Shared / Quarantine.
5. Classify risk level: Low / Medium / High / Critical / Blocked / TBD.
6. Identify capability domain.
7. Identify candidate Agent / file if applicable.
8. Check risk-level-map.md.
9. Check secondary-hooks-map.md.
10. Check frontmatter-schema.md for candidate files.
11. Verify file path and layer consistency.
12. Verify routing_enabled status.
13. Verify registry_enabled status where applicable.
14. Verify tool_permissions are safe.
15. Verify candidate is not quarantined.
16. Verify required hooks are attached.
17. Verify evidence and review requirements.
18. Verify human approval requirement.
19. Choose Router Decision.
20. Output routing note or proceed.
```

Routing must answer: Who can do this? Who may do this? Who must review this? What evidence is required? What must be logged? What must not be automated?

## Frontmatter Routing Gate

Before routing to any candidate file, verify:

- `routing_enabled` is true for executable Agent targets;
- `registry_enabled` is not mistaken as execution permission;
- `tool_permissions` match task risk;
- `risk_level` is equal to or higher than task risk;
- `layer`, `context_layer` and file path are consistent;
- `status` is not `draft`, `deprecated`, `quarantined` or `disabled`;
- required hooks are declared for Medium+ tasks;
- forbidden_actions do not conflict with requested task.

If any gate fails:
- return HOLD for repairable mismatch;
- return BLOCK for non-negotiable violation;
- return ESCALATE for high-risk authority conflict.

---

## 7. Business Architecture Routing Rules

### 7.1 L2 Core Protection

Route reusable ESTRIX engine capabilities to L2 / Core-related files. If a request involves reusable CRM, booking, billing, dashboard, permission, audit, notification, task management, Agent workflow, workflow automation, shared schema or reusable state machine, default to `L2｜ESTRIX Core Engine Layer`.

Do not implement inside SoMatch / SHINES unless explicitly approved.

### 7.2 L3 Application Protection

Route brand-specific or use-case-specific work to L3, such as SoMatch offer names, SHINES beauty consultation flow, medspa-specific workflow, franchise-specific SOP, application-level brand voice or application-specific onboarding scripts.

### 7.3 L4 Engagement Protection

Route one-time work to L4, such as one campaign, one monthly report, one sprint, one MVP draft, one client onboarding checklist or one version delivery task.

### 7.4 Core Contamination HOLD

Return HOLD if Codex cannot determine whether something is ESTRIX Core capability, SoMatch Application packaging, SHINES workflow, L4 one-time project or Esthetix-wide governance rule.

---

## 8. Layer Routing Rules

Route to Guardian for review, veto, compliance, quality gate, security, audit, evidence, production readiness, brand risk, legal / tax / privacy, model risk, finance / ledger / payment, accessibility / human factors or risk assessment.

Route to Mission for implementation, content creation, engineering delivery, marketing execution, sales execution, support operations, project delivery, product discovery, design production, data extraction task or customer service task.

Route to Platform for reusable infrastructure, including SRE, data pipeline, document automation, PromptOps, MCP tooling, design system, reporting distribution, identity graph, workflow architecture, knowledge system, meeting operating system or localization / terminology system.

Route to Core Strategy for market entry, product management, portfolio management, revenue intelligence, deal strategy, account strategy, financial forecasting, investment research, executive coordination, long-term roadmap, resource allocation analysis or decision packaging.

Route to Sovereign for Principle 0 conflict, cross-domain arbitration, Kill Switch package, Human Override package, irreversible company-level decision, Guardian Veto override, public crisis decision, broad permission escalation, business model activation or company-level authority conflict.

---

## 9. Quarantine Routing Rules

Route to `_quarantine` when there is missing frontmatter, content mismatch, wrong layer, unsafe permission, duplicate responsibility, unclear risk level, pending human review, unclear routing target, Guardian purity issue, Sovereign boundary issue, Core contamination, Application redefinition or Engagement overreach.

Quarantined files must have:

```yaml
routing_enabled: false
status: quarantined
tool_permissions: none
```

No quarantined file may be referenced as an active routing target.

---

## 10. Required Routing Output

For Medium+ tasks:

```text
Router Decision:
Business Context Layer:
PACE Layer:
Risk Level:
Primary Agent / File:
Secondary Hooks:
Evidence Required:
Human Approval Needed:
Notes:
```

For HOLD:

```text
Router Decision: HOLD

Proposed Layer:
Reason for Uncertainty:
Assumptions:
Required Clarification:
Safest Temporary Classification:
Execution Status:
Risk Note:
Next Recommended Action:
```

For BLOCK:

```text
Router Decision: BLOCK

Blocked Action:
Reason:
Policy / Boundary Violated:
Risk Level:
Safe Alternative:
Required Human / Guardian Review:
```

For ESCALATE:

```text
Router Decision: ESCALATE

Escalation Target:
Reason:
Decision Needed:
Evidence Needed:
Required Hooks:
Temporary Safe Action:
```

For Low-risk tasks, Codex may output compact routing:

Router Decision:
Business Context Layer:
PACE Layer:
Risk Level:
Primary Agent / File:
Notes:

For Low-risk documentation-only tasks, routing output may be omitted when the action is local, reversible and does not affect registry, routing, permissions, risk level or Business Architecture boundaries.

---

## 11. Router Integrity Checks

Before marking a routing file active, verify:

- [ ] `risk-level-map.md` exists.
- [ ] `secondary-hooks-map.md` exists.
- [ ] `frontmatter-schema.md` exists.
- [ ] `quarantine-policy.md` exists.
- [ ] PR / CI checklist exists.
- [ ] Routing decisions use only `PROCEED`, `HOLD`, `BLOCK`, `ESCALATE`.
- [ ] HOLD output follows standardized format.
- [ ] BLOCK output follows standardized format.
- [ ] ESCALATE output follows standardized format.
- [ ] Shared files are non-routable.
- [ ] Quarantined files are non-routable.
- [ ] High / Critical tasks require hooks.
- [ ] Business Architecture Context Stack is represented.
- [ ] ESTRIX Core contamination can return HOLD.
- [ ] Guardian hidden execution can return BLOCK.
- [ ] Sovereign direct irreversible execution can return BLOCK or ESCALATE.

---

## 12. Routing Examples

| Scenario | Business Layer | PACE Layer | Risk | Router Decision |
|---|---|---|---|---|
| Fix typo in README | Repository | Shared / Governance | Low | PROCEED |
| Add SoMatch wording to offering catalog | L3 | A / Mission or Application Context | Medium | PROCEED / HOLD |
| Add SoMatch service wording into ESTRIX Core | L2 / L3 conflict | P / E review | High | HOLD |
| Change payment retry logic | L2 | A + E hooks | Critical | ESCALATE |
| Restore quarantined Guardian file | Repository | E + Registry | High | HOLD / ESCALATE |
| Public crisis statement | L0 | Sovereign + Guardian | Critical | ESCALATE |
| Mission Agent claims final approval | Repository | A boundary violation | High | BLOCK |

---

## 12.1 Human Approval Boundary

Human approval is required for:
- activating this router as active baseline;
- changing router decision logic;
- requesting a formal policy change for a forbidden action boundary;
- reviewing a High / Critical routing exception request before any execution;
- restoring quarantined files;
- changing routing behavior for Sovereign, Guardian or Production Write actions.

Human approval does not automatically authorize forbidden actions.

If a requested action conflicts with `forbidden_actions`, the router must return `BLOCK` unless the governing policy is formally amended, reviewed, versioned and recorded.

High / Critical work must not proceed without required hooks. A missing-hook exception is not allowed as a case-by-case shortcut. It requires formal router policy amendment, governance review, WORM record and human approval.

## 13. Final Rule

> The router does not ask only “who can do this?” The router asks “who may do this, who must review it, what must be logged, and what must never be automated?”
