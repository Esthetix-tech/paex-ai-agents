---
name: agent-responsibility-matrix
title: Agent Responsibility Matrix
description: Support draft only registry responsibility matrix for preparing non-canonical responsibility review material without binding assignment, owner authority, reviewer authority, routing, activation or registry policy authority.
layer: agent-registry
context_layer: Repository Governance
pace_layer: Agent Registry / Support Draft Intake
risk_level: high
status: active_candidate
owner: Agent Repository Steward
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.0
related_files: []
requires_guardian_review: true
requires_worm: false
rollback_required: false
canary_required: false
exemption_reason: registry_support_draft_only_no_canonical_authority
exemption_review_required: true
forbidden_actions:
  - activate_agent_during_intake
  - expand_routing_authority_without_review
  - expand_tool_permissions_without_review
  - modify_canonical_registry_policy_without_review
  - modify_agent_router_without_review
  - modify_frontmatter_schema_without_review
  - modify_risk_level_map_without_review
  - modify_secondary_hooks_without_review
  - assign_binding_responsibility_without_review
  - declare_canonical_source_of_truth_without_approval
  - mark_agent_active_without_lifecycle_promotion
  - grant_tool_permission_without_review
  - override_registry_maintenance_policy
  - treat_support_draft_as_canonical_policy
  - make_router_decision_without_authority
  - make_risk_level_decision_without_authority
  - create_binding_agent_ownership_without_review
  - designate_formal_owner_without_review
  - designate_reviewer_authority_without_review
allowed_actions:
  - draft_registry_support_index
  - summarize_existing_agent_metadata
  - prepare_non_canonical_mapping
  - identify_registry_gaps
  - prepare_review_notes
  - recommend_hold_or_escalation
  - prepare_human_review_materials
evidence_required:
  - source_files_reviewed
  - frontmatter_snapshot
  - mapping_assumptions
  - canonical_policy_references
  - non_canonical_boundary_statement
  - review_findings
  - human_review_required_for_canonical_use
---

## Governance Intake Boundary

This Phase 3B-1 intake file is support draft only, non-canonical, no authority expansion, a metadata support reference and a human-review material preparer.

It is not canonical registry policy, router decision authority, schema authority, risk-level decision authority, secondary hooks authority, routing authority, tool permission mapping authority, activation authority, binding responsibility assignment authority or registry source of truth.

It must not act as a canonical source of truth, make router decisions, define schema authority, make risk-level decisions, map or grant tool permissions, activate agents, create binding responsibility assignment or override existing canonical registry files.

For agent-responsibility-matrix specifically, this file must not form binding responsibility assignment and must not designate formal owner or reviewer authority. Any binding ownership or reviewer assignment requires separate governance PR, Guardian Review and human approval.

## Recent Governance References

This registry support draft should be read together with the latest governance records:

- Phase 5 Partial Summary Closing Note.
- Phase 5-2 Scope Discovery Closing Note.
- Registry Consistency Read-only Validation Closing Note.
- Phase 4E HOLD / Exclusion Register.

Current count and intake boundaries:

- Prior registry support count reference: `48`.
- Current authoritative safe-managed files total: `53`.
- Authority source: Safe-managed Count Reconciliation Note, 183 Agents Master Inventory Summary, and Phase 4E Final Closure Summary.
- Inventory boundary: `183` remains a governance import target / target inventory concept; `183` physical agent files are not observed on `origin/main`.
- No-authority boundary: this registry support count reconciliation does not activate agents, does not authorize routing/tool expansion, does not enter Phase 5, does not increase safe-managed count, does not grant production/runtime authority, and does not mutate the Sovereign index or formal/audit evidence.
- Phase 5-2 introduced no safe-managed count increase.
- Read-only validation, planning notes, documentary notes and closing notes do not increase the operational safe-managed count.
- HOLD files must not enter a general repair batch.
- Registry support draft cross-references do not grant activation, routing, tool expansion, runtime, production, publication, customer-facing, approval, Guardian, K / CEO, Sovereign or repair authority.

\# PACE-AI Agent Responsibility Matrix

\## Responsibility Boundaries for 183 Intelligent Agents

\*\*Document Type:\*\* Agent Governance Responsibility Matrix  

\*\*System:\*\* PACE-AI Enterprise Governance OS  

\*\*Version:\*\* v1.0  

\*\*Status:\*\* Draft for Codex Agent Engine Configuration  

\*\*Owner:\*\* Esthetix / PACE-AI Governance Layer  

\*\*Primary Purpose:\*\* Define what each Agent category can do, cannot do, who reviews it, and which governance controls must be attached.

\---

\## 1. Document Purpose

This document defines responsibility boundaries for AI Agents imported into PACE-AI.

The purpose is to ensure every Agent has:

\- A clear mission

\- A primary governance layer

\- Defined authority boundaries

\- Explicit prohibited actions

\- Required Guardian checks

\- WORM conditions

\- Canary conditions

\- Counter-Metrics conditions

\- Conflict resolution rules

\- Knowledge assetization obligations

This matrix prevents Agent sprawl, role confusion, duplicated authority, hidden automation, and untraceable decision-making.

Core rule:

\> An Agent without a responsibility boundary is not an enterprise asset.  

\> It is a governance risk.

\---

\## 2. Responsibility Design Principles

\## 2.1 One Primary Layer

Every Agent must have one primary layer:

| Layer | Primary Identity |

\|---|---|

| C | Strategic decision support |

| A | Mission execution |

| E | Expert review and veto |

| P | Shared platform and infrastructure |

An Agent may have secondary hooks, but it must have only one primary home.

Example:

\```text

Primary: A / Mission

Secondary: E-brand-compliance, P-campaign-data
第2頁/共62頁

```

