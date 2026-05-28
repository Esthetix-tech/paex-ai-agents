---
name: WORM Event Schema
title: PAEX-AI WORM Event Schema
description: Immutable governance event schema for recording high-risk decisions, Guardian vetoes, Human Overrides, Kill Switch actions, Canary releases, funding events, agent changes and audit-critical governance actions.
layer: governance
context_layer: Repository Governance
pace_layer: Repository Governance / WORM Event Schema
risk_level: critical
status: active
owner: Sovereign Governance Office
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - file_activation
  - worm_schema_policy_change
  - audit_event_schema_change
  - critical_governance_event_change
  - high_or_critical_worm_exception
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
requires_worm: true
worm_scope:
  - file_activation
  - worm_schema_policy_change
  - audit_event_schema_change
  - critical_governance_event_change
  - high_or_critical_worm_exception
requires_guardian_review: true
secondary_hooks:
  - governance-review
  - registry-maintenance-review
  - ci-validation-review
forbidden_actions:
  - edit_worm_event_after_creation
  - suppress_worm_for_high_or_critical_action
  - bypass_guardian_review_for_critical_event_schema
  - weaken_audit_event_attribution
  - route_worm_schema_as_execution_agent
allowed_actions:
  - define_worm_event_schema
  - validate_audit_event_metadata
  - require_evidence_for_high_or_critical_actions
  - support_governance_event_review
  - reference_canonical_registry_controls
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - duplicate_frontmatter_key_check
  - markdown_structure_check
  - guardian_review_record
  - worm_activation_record
  - ci_validation_result
  - human_approval_record
rollback_required: true
canary_required: false
related_files:
  - ../../../AGENTS.md
  - ../../../README.md
  - ../../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - ../../agent-registry/frontmatter-schema/frontmatter-schema.md
  - ../../agent-registry/agent-router/agent-router.md
  - ../../agent-registry/risk-level-map/risk-level-map.md
  - ../../agent-registry/secondary-hooks-map/secondary-hooks-map.md
  - ../../agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
  - ../pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
exemption_reason: critical_schema_reference_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_schema_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

# PAEX-AI WORM Event Schema

## 1. Purpose

This file defines the canonical WORM Event Schema for PAEX-AI Enterprise Governance OS.

WORM means:

> Write Once, Read Many.

In PAEX-AI, WORM is not a normal system log.  
It is the immutable governance record layer for high-risk authority, professional vetoes, human overrides, funding decisions, Kill Switch actions, Canary releases, agent permission changes, policy changes, incident decisions and production-critical governance events.

Core rule:

> If a high-risk decision cannot be recorded, attributed, evidenced and audited, it must not proceed.

WORM exists to make governance visible, durable and reviewable.

It answers:

- Who acted?
- What was changed?
- Why was the decision made?
- Which policy applied?
- What evidence was reviewed?
- Which risks were known?
- Which controls were attached?
- Was there a Guardian Veto?
- Was there a Human Override?
- Was Canary required?
- Was Kill Switch available?
- Can this decision survive audit, appeal and postmortem review?

WORM is the truth ledger of PAEX-AI.

---

## 2. Governance Positioning

WORM belongs to the `governance/` layer.

Its function is to provide the mandatory event schema for audit-critical governance actions across:

- Sovereign decisions.
- Guardian reviews.
- Human Overrides.
- Kill Switch actions.
- Canary releases.
- Funding unlock / freeze decisions.
- Ledger-adjacent changes.
- Agent permission changes.
- Policy Pack changes.
- Production activation decisions.
- Cross-domain War Room incidents.
- Quarantine restoration of High / Critical artifacts.

In the PAEX model:

| Layer | Relationship to WORM |
|---|---|
| C-Level / Sovereign | Uses WORM to preserve strategic accountability. |
| A-Level / Mission | Must generate WORM events when requesting or executing high-risk work. |
| E-Level / Guardian | Must record vetoes, warnings, review outcomes and escalations. |
| P-Level / Platform | Provides WORM infrastructure, hash chain, storage, indexing and retrieval. |
| Governance | Defines the required schema, event rules and failure behavior. |

WORM must not be controlled by any Mission Agent that benefits from the event outcome.

---

## 3. Core Principles

### 3.1 Append-only

A WORM event must never be edited, overwritten, deleted, reordered or silently corrected after creation.

If additional information is required, create a new linked event.

Allowed follow-up event types include:

- `EVENT_CORRECTION_SUBMITTED`
- `SUPPLEMENTAL_EVIDENCE_ADDED`
- `APPEAL_SUBMITTED`
- `APPEAL_DECISION`
- `POSTMORTEM_ADDED`
- `ROOT_CAUSE_CONFIRMED`
- `CONTROL_MEASURE_UPDATED`

Original events remain intact.

---

### 3.2 Tamper-evident

WORM must make unauthorized modification detectable.

Each event should include:

- `previous_hash`
- `record_hash`
- `merkle_batch_id`
- `merkle_root`
- trusted timestamp
- actor identity
- source system
- policy version
- evidence links

If the hash chain breaks, create:

```text
WORM_INTEGRITY_ALERT
```
