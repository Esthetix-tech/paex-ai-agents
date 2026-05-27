---
name: WORM Event Schema
title: PACE-AI WORM Event Schema
description: Immutable governance event schema for recording high-risk decisions, Guardian vetoes, Human Overrides, Kill Switch actions, Canary releases, funding events, agent changes and audit-critical governance actions.
layer: governance
pace_layer: Global Governance / Platform Audit
risk_level: critical
status: stable
owner: Sovereign Governance Office
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.0
related_files:
  - governance/core-governance-protocols.md
  - governance/guardian-review-coordinator.md
  - governance/human-override-accountability.md
  - governance/kill-switch-governor.md
  - governance/canary-release-governor.md
  - governance/agent-drift-review.md
  - governance/production-readiness-gate.md
  - sovereign/principle-0-charter.md
  - sovereign/sovereign-agent.md
  - sovereign/cross-domain-war-room-playbook.md
  - agent-registry/risk-level-map.md
---

# PACE-AI WORM Event Schema

## 1. Purpose

This file defines the canonical WORM Event Schema for PACE-AI Enterprise Governance OS.

WORM means:

> Write Once, Read Many.

In PACE-AI, WORM is not a normal system log.  
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

WORM is the truth ledger of PACE-AI.

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

In the PACE model:

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