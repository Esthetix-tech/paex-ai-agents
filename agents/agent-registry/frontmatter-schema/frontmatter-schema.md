---
name: Frontmatter Schema
title: PAEX-AI Agent Frontmatter Schema
description: Mechanical validation schema for Agent, governance, registry, context, shared and quarantine files inside the PAEX-AI agents repository.
layer: agent-registry
context_layer: Repository Governance
pace_layer: Repository Governance / Metadata Schema
risk_level: high
status: active_candidate
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - file_activation
  - schema_policy_change
  - high_or_critical_field_exemption
  - permission_field_change
  - layer_mapping_change
  - quarantine_restore_schema_change
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
requires_worm: false
requires_guardian_review: true
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - grant_authority_by_metadata_only
  - allow_missing_required_fields_for_active_files
  - route_files_with_layer_path_conflict
  - autofix_permission_escalation_without_review
  - restore_quarantined_files_without_required_review
allowed_actions:
  - define_frontmatter_schema
  - validate_governance_metadata
  - identify_required_field_gaps
  - classify_schema_exemptions
  - support_ci_frontmatter_checks
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - duplicate_frontmatter_key_check
  - enum_value_validation
  - path_layer_alignment_check
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
  - ../risk-level-map/risk-level-map.md
  - ../secondary-hooks-map/secondary-hooks-map.md
  - ../registry-maintenance-policy/registry-maintenance-policy.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
  - ../../governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../governance/worm-event-schema/worm-event-schema.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
exemption_reason: metadata_schema_only_no_production_execution
exemption_scope:
  - worm_not_required_for_read_only_schema_definition
  - canary_not_required_for_non_release_metadata_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

# Frontmatter Schema｜PAEX-AI Agent Frontmatter Schema

## 1. Purpose｜目的

This file defines the required frontmatter metadata standard for all governed files in the `agents/` repository.

Frontmatter is the identity card, permission boundary, lifecycle tag, routing hint and audit metadata for every Agent, governance protocol, registry file, Business Architecture Context Stack file, shared asset and quarantined file.

Core rule:

> A file without clear frontmatter cannot be safely routed, trusted, activated, reviewed, restored or promoted.

Plain-language interpretation:

> Frontmatter 是 Agent 的身分證、權限卡與風險標籤。身分證不清楚，就不能上戰場。

---

## 2. Scope｜適用範圍

This schema applies to Agent role specification files, governance protocol files, registry files, Business Architecture Context Stack files, Application / Use Case context files, Engagement / Project files, shared templates, quarantine policy files, quarantined records, PR / CI validation checklists and repository-level governance documents.

Pure static assets may be exempted only when the exemption is explicitly documented. Exempt files must not be routed as Agent targets.

---

## 3. Required Fields｜必要欄位

Every governed `.md` file should include the following frontmatter fields unless explicitly exempted.

```yaml
---
name:
title:
description:
layer:
context_layer:
pace_layer:
risk_level:
status:
owner:
review_required:
human_approval_required:
codex_autofix_allowed:
tool_permissions:
routing_enabled:
registry_enabled:
version:
related_files:
---
```

| Field | Required | Type | Allowed / Expected Values | Purpose |
|---|---:|---|---|---|
| `name` | Yes | string | short canonical name | Machine-readable identity |
| `title` | Yes | string | human-readable title | Executive-readable title |
| `description` | Yes | string | one sentence | Defines what this file governs or performs |
| `layer` | Yes | enum/string | `L0`, `L1`, `L2`, `L3`, `L4`, `core`, `mission`, `guardian`, `platform`, `sovereign`, `governance`, `agent-registry`, `shared`, `_quarantine` | Primary repository or context layer |
| `context_layer` | Conditional | string | Business Architecture layer or repository governance context | Required for L0–L4 and recommended for governance / registry |
| `pace_layer` | Yes | string | `C / Core Strategy`, `A / Mission`, `E / Guardian`, `P / Platform`, `Sovereign`, `Repository Governance`, `Business Architecture / ...` | PACE governance identity |
| `risk_level` | Yes | enum | `low`, `medium`, `high`, `critical`, `blocked`, `tbd` | Risk classification |
| `status` | Yes | enum | draft, active_candidate, active, deprecated, disabled, blocked, quarantined, template | Lifecycle status |
| `owner` | Yes | string | responsible owner | Accountability |
| `review_required` | Yes | boolean | `true` / `false` | Whether review is required before activation |
| `human_approval_required` | Yes | boolean | `true` / `false` | Whether human approval is required before execution or activation |
| `codex_autofix_allowed` | Yes | enum | `none`, `limited`, `safe_metadata_only`, `safe_docs_only`, `allowed` | Whether Codex may modify automatically |
| `tool_permissions` | Yes | enum/string | `none`, `metadata_only`, `read_only`, `draft_only`, `review_only`, `limited_write`, `execution_limited`, `production_write_blocked` | Tool/action boundary |
| `routing_enabled` | Yes | boolean | `true` / `false` | Whether file can be routed as execution target |
| `registry_enabled` | Yes | boolean | `true` / `false` | Whether file participates in registry logic |
| `version` | Yes | string | semantic or governance version | Version tracking |
| `related_files` | Recommended | list | relative paths | Traceable governance dependencies |

## Status Routing Rules

| Status | Routing Allowed |
|---|---:|
| draft | No |
| active_candidate | No, unless explicitly used for review |
| active | Yes, if routing_enabled is true |
| deprecated | No |
| disabled | No |
| blocked | No |
| quarantined | No |
| template | No |

---

### Human Approval Field Relationship

`human_approval_required` is the general activation / execution approval flag.

`requires_human_approval` is the High / Critical governance control flag.

For High / Critical files, both should be aligned unless an explicit exemption is documented.

## 4. High-Risk / Critical Required Fields

If `risk_level` is `high` or `critical`, the following fields should be added unless an explicit exemption is documented.

```yaml
requires_worm: true
requires_guardian_review: true
requires_human_approval: true
secondary_hooks:
  - ...
forbidden_actions:
  - ...
allowed_actions:
  - ...
evidence_required:
  - ...
rollback_required: true
canary_required: true
```
If a High-risk or Critical file uses an exemption from a normally required control, it must include an explicit exemption record.

```yaml
exemption_reason: metadata_schema_only_no_production_execution
exemption_scope:
  - worm_not_required_for_read_only_schema_definition
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date:
```

```text
For High / Critical files, if `requires_worm`, `requires_guardian_review`, `requires_human_approval`, `rollback_required`, or `canary_required` is set to `false` against the normal requirement, an exemption record is required.
```

High-risk governance documents may set `requires_worm: false` only when they do not execute production actions, but they must still define review, forbidden actions and activation controls.

---

## 5. Layer-Specific Defaults

### 5.1 Registry Files

```yaml
layer: agent-registry
context_layer: Repository Governance
pace_layer: Repository Governance / ...
routing_enabled: false
registry_enabled: true
tool_permissions: metadata_only
codex_autofix_allowed: limited
```

Registry files define rules. They are not execution agents.

### 5.2 Governance Files

```yaml
layer: governance
context_layer: Repository Governance
pace_layer: Governance Protocol / ...
routing_enabled: false
registry_enabled: true
tool_permissions: review_only
```

Governance files define protocols and gates. They are not normal task executors.

### 5.3 Guardian Files

```yaml
layer: guardian
pace_layer: E / Guardian
routing_enabled: true
tool_permissions: review_only
requires_guardian_review: false
guardian_review_trigger:
  - high_or_critical_risk
  - sensitive_domain
  - production_write
  - public_brand_content
  - financial_or_legal_impact
```

Guardian agents review, audit, verify, veto and enforce standards. They must not become hidden executors.

### 5.4 Mission Files

```yaml
layer: mission
pace_layer: A / Mission
routing_enabled: true
tool_permissions: limited_write
requires_guardian_review: false
guardian_review_trigger:
  - high_or_critical_risk
  - required_by_secondary_hooks
  - external_brand_content
  - production_write
  - financial_legal_security_or_privacy_risk
```

Mission agents execute work but must not self-approve High / Critical actions.

### 5.5 Platform Files

```yaml
layer: platform
pace_layer: P / Platform
routing_enabled: true
tool_permissions: limited_write
requires_guardian_review: false
guardian_review_trigger:
  - production_infrastructure_change
  - security_or_data_boundary_change
  - automation_or_tool_exposure
  - required_by_secondary_hooks
```

Platform agents provide reusable infrastructure, not final business authorization.

### 5.6 Core Strategy Files

```yaml
layer: core
pace_layer: C / Core Strategy
routing_enabled: true
tool_permissions: draft_only
requires_human_approval: false
human_approval_trigger:
  - irreversible_company_level_action
  - budget_or_resource_commitment
  - public_positioning_change
  - business_model_activation
  - legal_financial_or_governance_commitment
```

Core Strategy agents may recommend or prepare decision packages. They must not execute irreversible company-level actions.

### 5.7 Sovereign Files

```yaml
layer: sovereign
pace_layer: Sovereign
routing_enabled: false
tool_permissions: review_only
requires_human_approval: true
```

Sovereign prepares arbitration and activation packages. It does not directly execute irreversible action.

### 5.8 Shared Files

```yaml
layer: shared
pace_layer: Shared Reference
routing_enabled: false
registry_enabled: false
tool_permissions: metadata_only
```

Shared files are reusable assets, not routing targets.

### 5.9 Quarantine Files

```yaml
layer: _quarantine
pace_layer: Quarantine
risk_level: blocked
status: quarantined
routing_enabled: false
registry_enabled: false
tool_permissions: none
```

Quarantined files must not be routed until restored through quarantine policy.

---

## 6. Business Architecture Context Files

For L0–L4 Business Architecture files, use:

```yaml
layer: L0 | L1 | L2 | L3 | L4
context_layer: K Command Layer | Esthetix Arsenal Layer | ESTRIX Core Engine Layer | Application / Use Case Layer | Engagement / Project Layer
pace_layer: Business Architecture / ...
routing_enabled: false
registry_enabled: false
tool_permissions: metadata_only
```

These files guide context classification. They are not execution agents.

---

## 7. Validation Rules

Codex and CI should validate the following rules:

1. Required frontmatter fields exist.
2. Required fields are not empty unless explicitly allowed.
3. Duplicate frontmatter keys do not exist.
4. Enum values are valid.
5. File path matches `layer`.
6. `pace_layer` matches the file role and repository path.
7. `routing_enabled` is valid for the file type and status.
8. `registry_enabled` is valid for registry and non-registry files.
9. `tool_permissions` are compatible with the file layer and risk level.
10. High / Critical files include required hooks or an explicit exemption record.
11. Guardian files do not have unsafe execution permissions.
12. Mission files do not claim veto or final approval authority.
13. Sovereign files do not claim direct irreversible execution authority.
14. Shared files are not routable.
15. Quarantined files are not routable.
16. Active files do not depend on quarantined files as active routing targets.
17. L2 files do not contain application-only brand logic.
18. L3 files do not redefine ESTRIX Core.
19. L4 files do not redefine Esthetix, ESTRIX or application boundaries.
20. Frontmatter content does not contradict the file body.

Duplicate frontmatter keys must fail CI because duplicated metadata may create inconsistent routing, lifecycle, permission or risk interpretation.
---

## 8. Related Files Validation

FAIL when `related_files` points to required governance files and the path is broken, when it points to core registry files such as `agent-router.md`, `risk-level-map.md`, `secondary-hooks-map.md`, `frontmatter-schema.md`, or `quarantine-policy.md` and the path is broken, or when an active file depends on a quarantined file as active routing target.

WARNING when `related_files` points to optional reference material, the file is Low risk, or the file is draft/template and the missing dependency is explicitly marked `TBD`.

---

## 9. HOLD Conditions

Return `HOLD` if frontmatter is missing, required fields are empty, path and layer conflict, risk level is unclear, high-risk hooks are missing, a Mission agent claims Guardian authority, a Guardian agent has production execution permission, a shared file is routable, a quarantined file is referenced as active, ESTRIX Core is polluted by SoMatch / SHINES brand-specific logic, or file content contradicts frontmatter.

Required HOLD format:

```text
Router Decision: HOLD

File:
Issue:
Proposed Fix:
Required Owner:
Required Review:
Can Codex autofix:
Risk Note:
Next Action:
```

---

## 10. Autofix Rules

Codex may autofix formatting, typo-level metadata corrections, title capitalization, obvious missing `related_files`, `version` formatting, `routing_enabled: false` for shared and registry files, `registry_enabled: true` for registry files, and harmless Markdown cleanup.

Codex must not autofix without review: risk level changes, layer changes, tool permission escalation, Guardian / Mission role conversion, Sovereign boundary changes, High / Critical `forbidden_actions`, human approval requirements, production-write permissions, quarantined file restoration, ESTRIX Core promotion, application-to-core boundary changes, or registry authority changes.

---

## 11. Mechanical CI vs Semantic Review Boundary

Mechanical CI may automatically FAIL missing frontmatter, invalid enum values, wrong path-layer mapping, `routing_enabled` violation, quarantined file active routing, missing required hooks, broken required `related_files`, and shared files used as routing targets.

Mechanical CI should return HOLD for semantic review when Guardian purity, duplicate responsibility, Core contamination, L3 redefinition, L4 overreach, business context layer, or risk classification is ambiguous.

Human / Guardian review is required when CI detects semantic ambiguity, risk is High or Critical, file changes routing authority, file affects registry/hooks/quarantine/v1.4 activation baseline, or file changes Core / Application / Engagement boundary.

---

## 12. Final Rule

> Frontmatter does not create authority. Frontmatter declares authority that must be consistent with file content, path, registry rules and governance policy.

If frontmatter says “allowed” but governance says “blocked,” governance wins.
