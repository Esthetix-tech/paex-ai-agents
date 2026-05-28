---
name: Risk Level Map
title: PAEX-AI Risk Level Map
description: Defines Low, Medium, High and Critical risk classifications for routing, hooks, evidence, approval and execution boundaries.
layer: agent-registry
context_layer: Repository Governance
pace_layer: Repository Governance / Risk Classification
risk_level: high
status: active
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - file_activation
  - risk_policy_change
  - risk_level_downgrade_exception
  - critical_risk_exception
  - blocked_risk_override_request
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
requires_worm: true
worm_scope:
  - file_activation
  - risk_policy_change
  - risk_level_downgrade_exception
  - critical_risk_exception
  - blocked_risk_override_request
requires_guardian_review: true
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - downgrade_risk_because_agent_is_capable
  - treat_critical_work_as_autonomous_execution
  - allow_high_risk_without_hooks
  - classify_unknown_risk_as_low
  - lower_trigger_minimum_risk_without_evidence
allowed_actions:
  - define_risk_classification
  - identify_risk_escalation_triggers
  - require_upward_classification_when_unclear
  - validate_risk_level_alignment
  - document_risk_downgrade_conditions
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - duplicate_frontmatter_key_check
  - risk_trigger_alignment_check
  - required_hooks_check
  - ci_validation_result
  - guardian_review_record
  - human_approval_record
rollback_required: true
canary_required: false
related_files:
  - ../../../AGENTS.md
  - ../../../README.md
  - ../../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - ../agent-router/agent-router.md
  - ../secondary-hooks-map/secondary-hooks-map.md
  - ../frontmatter-schema/frontmatter-schema.md
  - ../registry-maintenance-policy/registry-maintenance-policy.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
  - ../../governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../governance/worm-event-schema/worm-event-schema.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
exemption_reason: risk_classification_policy_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

# Risk Level Map｜PAEX-AI Risk Level Map

## 1. Purpose

This file defines how Codex classifies task, file and Agent risk levels.

Core rule:

> When risk is unclear, classify upward.

Plain-language interpretation:

> 不確定風險時，不要低估。寧可先升級審查，也不要讓風險裸奔。

---

## 2. Risk Levels

| Risk Level | Meaning | Default Action |
|---|---|---|
| Low | Reversible, local, non-sensitive, non-production work | Proceed with basic self-check |
| Medium | Normal operational or repository work with limited impact | Proceed with validation and review note |
| High | Sensitive, external, production-adjacent, financial, legal, brand, data or permission impact | Require Guardian note, WORM consideration, rollback, hooks |
| Critical | Irreversible, legally / financially material, production destructive, security incident, ledger/payment/identity root impact | Do not autonomously execute; prepare decision package and escalate |
| Blocked | Unsafe, unlawful, contradictory, unreviewed, quarantined or missing required authority | Block execution |
| TBD | Risk cannot be determined with available evidence | HOLD until classified |

---

## 3. Low Risk

Low-risk tasks are reversible, local, non-sensitive, non-production, unlikely to affect customers, partners, finance, brand, legal, privacy or security, and unlikely to alter authority, permissions or routing.

Examples: formatting, typo correction, internal note cleanup, README formatting, non-critical naming cleanup, local scripts without external effect, non-production prototype scaffolding, harmless documentation restructuring.

Required controls: basic self-check and clear summary.

Allowed Router Decision: `PROCEED`.

---

## 4. Medium Risk

Medium-risk tasks have real operational value but limited blast radius.

Examples: normal feature work, internal workflow update, non-critical UI change, non-sensitive automation, minor schema update without production impact, minor Agent frontmatter update, internal dashboard formatting, low-risk report generation, new draft template with no active routing authority.

Required controls: validation or test note, assumptions stated, review need flagged, no unauthorized scope expansion.

Allowed Router Decisions: `PROCEED`, `HOLD`.

---

## 5. High Risk

High-risk tasks may affect money, identity, permission, customer trust, public brand, legal / compliance, production infrastructure, sensitive data, external partners or automated external actions.

Examples: payment-adjacent logic, refund logic, ledger-adjacent reporting, booking / cancellation logic, coupon or pricing logic, PII handling, permission change, public brand content, partner-impacting rules, automated publishing, paid media budget changes, MCP tool exposure, production write action, healthcare / legal / financial / tax / compliance content, data pipeline affecting management reporting, high-risk Agent permission expansion, L2 Core architecture change, SoMatch / SHINES application logic being added to ESTRIX Core.

Required controls: Guardian-style review note, WORM-style event note or WORM decision, rollback plan, counter-metrics, Canary / controlled rollout recommendation where applicable, unresolved-risk disclosure and explicit approval where applicable.

Allowed Router Decisions: `HOLD`, `ESCALATE`, `PROCEED`. `PROCEED` is allowed only when required hooks and evidence exist.

---

## 6. Critical Risk

Critical-risk tasks are irreversible, materially consequential or capable of causing severe financial, legal, security, operational, reputational or customer harm.

Examples: core ledger mutation, payment settlement change, destructive production database action, irreversible legal or financial action, Kill Switch release, high-risk Human Override, broad permission escalation, account freeze, partner termination, public crisis statement, large-scale automated campaign spend, production IoT control logic, customer-impacting outage recovery decision, identity trust root change, Agent Registry permission model change, new external business model activation, Guardian Veto override.

Required controls: no autonomous execution, decision package, evidence list, Guardian Review, WORM requirement, rollback / kill-switch plan, explicit human approval, escalation path and unresolved-risk disclosure.

Allowed Router Decisions: `HOLD`, `BLOCK`, `ESCALATE`.

Critical work should be treated like a locked door, not a speed bump.

---

## 7. Blocked and TBD

Use `blocked` when the task violates law or platform safety, requests unsafe credential exposure, bypasses required approval, conflicts with governance boundaries, tries to restore quarantined file without review, attempts destructive production action without approval, asks Mission to self-approve high-risk work, asks Guardian to execute production work, or suppresses WORM / audit / review record.

Use `tbd` when available evidence is insufficient to determine risk. TBD always returns HOLD until classified.

---

## 8. Risk Escalation Triggers

| Trigger | Minimum Risk |
|---|---|
| Payment, refund, settlement, ledger | High / Critical |
| Production database migration | High / Critical |
| Destructive DB operation | Critical |
| PII, KYC, medical, legal, HR, sensitive data | High |
| Public brand statement | High |
| Public crisis statement | Critical |
| Automated external publishing | High |
| Large-scale ad spend | Critical |
| MCP tool exposure | High |
| Permission escalation | High / Critical |
| Identity root / trust registry change | Critical |
| Agent permission model change | Critical |
| Quarantined file restoration | High |
| Guardian Veto override | Critical |
| Human Override | High / Critical |
| Kill Switch release | Critical |
| Legal / financial commitment | Critical |
| Healthcare / legal / financial advice boundary | High / Critical |
| L2 Core architecture change | High |
| SoMatch / SHINES logic being added to ESTRIX Core | High |
| ESTRIX described as beauty-only or SoMatch-only | High |
| New external business model | Critical |
| Registry routing authority change | High / Critical |

## 8.1 Capability-Based Downgrade Ban

Codex must not reduce risk level because an Agent, tool, model, reviewer or workflow is highly capable, trusted, specialized, frequently used or previously successful.

Risk classification must be based on:

- impact scope;
- reversibility;
- production exposure;
- data sensitivity;
- financial / legal / security consequence;
- customer / partner / public impact;
- permission boundary;
- required hooks;
- available evidence;
- rollback capability.

If capability is high but consequence is high, the task remains High or Critical.

## 8.2 Minimum Risk Floor Rule

If a task matches a trigger in the Risk Escalation Triggers table, Codex must not classify it below the listed minimum risk unless all downgrade conditions are documented.

A valid downgrade requires:

- reduced blast radius;
- no production impact;
- no sensitive data exposure;
- no irreversible action;
- required hooks attached;
- evidence of reversibility;
- clear rollback path;
- human / Guardian review when applicable.

If downgrade evidence is missing, return HOLD.

---

## 9. Risk Downgrade Rule

Codex must not downgrade risk because an Agent is skilled, specialized, trusted, frequently used or previously successful.

Risk may be downgraded only when blast radius is reduced, data sensitivity is reduced, production impact is removed, irreversible action is removed, required hooks are attached, human approval boundary is preserved, evidence shows the task is reversible and contained, public / partner / customer impact is eliminated, or sensitive data is masked, removed or de-identified.

Plain-language interpretation:

> 能力強不代表風險低。風險只會因為影響範圍變小、資料變安全、行為可回滾、審查已掛載而降低。

---

## 10. Risk Level vs Required Output

| Risk | Final Response |
|---|---|
| Low | Compact response allowed |
| Medium | Full response template recommended |
| High | Full template + hooks + WORM + Guardian + rollback |
| Critical | Full template + escalation package; no autonomous execution |
| Blocked | BLOCK reason + safe alternative |
| TBD | HOLD format with required clarification |

---

## 11. Final Rule

> Capability does not reduce risk. A powerful Agent may be capable of doing something that it is not authorized to do.
