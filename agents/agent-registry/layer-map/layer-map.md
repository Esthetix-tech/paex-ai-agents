---
name: layer-map
title: Layer Map
description: Support draft only registry layer map for preparing non-canonical layer review material without overriding Context Stack, layer policy, routing, activation or registry policy authority.
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
  - override_canonical_context_stack
  - modify_layer_classification_authority
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

For layer-map specifically, this file must not override the canonical Context Stack or layer policy and must not modify layer classification authority. Any canonical layer authority requires separate governance PR, Guardian Review and human approval.

\# PACE-AI Layer Map

\## C-A-E-P Governance Layer Classification Standard

\*\*Document Type:\*\* Agent Registry Layer Map  

\*\*System:\*\* PACE-AI Enterprise Governance OS  

\*\*Version:\*\* v1.0  

\*\*Status:\*\* Draft for Codex Agent Engine Configuration  

\*\*Owner:\*\* Esthetix / PACE-AI Governance Layer  

\*\*Primary Purpose:\*\* Define how every AI Agent is classified into the PACE-AI C-A-E-P governance layers.

\---

\## 1. Document Purpose

This document defines the official \*\*C-A-E-P layer classification standard\*\* for PACE-AI.

PACE-AI is not a collection of AI tools.  

It is an enterprise-grade intelligent governance operating system.

Every Agent must be assigned to one primary governance layer:

| Layer | Name | Core Identity |

\|---|---|---|

| C | Core Strategy | Strategic judgment and resource decision support |

| A | Agile Squads | Mission execution and value creation |

| E | Expertise Guilds | Expert review, red-line control, and veto |

| P | Platform | Shared infrastructure, data, workflow, audit, and knowledge systems |

This file answers one question:

\> Where does an Agent live inside the PACE-AI operating model?

Secondary review, risk, evidence, WORM, Canary, or industry policy dependencies are defined separately in:

\```text

/agents/agent-registry/secondary-hooks-map.md
第2頁/共62頁

```

