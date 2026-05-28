---
name: Quarantine Policy
title: PAEX-AI Quarantine Policy
description: Defines when Agent files must be isolated, how they are reviewed, and how they may be restored into the active repository.
layer: _quarantine
context_layer: Repository Governance
pace_layer: Repository Governance / Quarantine Policy
risk_level: high
status: active
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - policy_activation
  - quarantine_restore_policy_change
  - medium_high_or_critical_restore_exception
  - tool_permission_restoration
  - active_reference_exception
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
requires_worm: true
worm_scope:
  - policy_activation
  - quarantine_restore_review
  - medium_high_or_critical_restore_exception
  - active_reference_exception
  - tool_permission_restoration
requires_guardian_review: true
secondary_hooks:
  - quarantine-review
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - route_quarantined_files_as_active
  - restore_medium_high_or_critical_without_review
  - hide_quarantine_reason
  - reference_quarantined_file_as_active_target
  - grant_tool_permissions_before_restoration
allowed_actions:
  - define_quarantine_policy
  - identify_quarantine_conditions
  - validate_restoration_requirements
  - block_active_routing_for_quarantined_files
  - require_review_for_medium_high_or_critical_restore
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - duplicate_frontmatter_key_check
  - quarantine_reason_record
  - restoration_review_record
  - ci_validation_result
  - guardian_review_record
  - human_approval_record
rollback_required: true
canary_required: false
related_files:
  - ../../../AGENTS.md
  - ../../../README.md
  - ../../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - ../../agent-registry/frontmatter-schema/frontmatter-schema.md
  - ../../agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
  - ../../agent-registry/agent-router/agent-router.md
  - ../../agent-registry/risk-level-map/risk-level-map.md
  - ../../agent-registry/secondary-hooks-map/secondary-hooks-map.md
  - ../../governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../governance/worm-event-schema/worm-event-schema.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
exemption_reason: quarantine_policy_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

# Quarantine Policy｜PAEX-AI Quarantine Policy

## 1. Purpose

This policy defines how unsafe, ambiguous, incomplete, duplicated or mismatched Agent files are isolated and restored.

Core rule:

> If a file cannot be safely trusted, it must not be routed.

Plain-language interpretation:

> 不確定能不能用的 Agent，不要硬上線。先隔離，再審查，再恢復。

---

## 2. Quarantine Folder

Quarantined files belong under:

```text
agents/_quarantine/
```

Recommended subfolders:

```text
_quarantine/
├─ content-mismatch/
├─ duplicate-responsibility/
├─ missing-frontmatter/
├─ pending-human-review/
├─ unclear-risk-level/
├─ unsafe-permission/
├─ wrong-layer/
└─ quarantine-policy/
```
The quarantine policy file itself is a governance policy stored inside the `_quarantine/quarantine-policy/` folder. It is not a quarantined Agent record and may use `status: active_candidate`, `registry_enabled: true` and `tool_permissions: metadata_only` when approved.
---

## 3. When to Quarantine

| Reason | Example |
|---|---|
| Missing frontmatter | No YAML metadata |
| Wrong layer | Mission file placed under Guardian |
| Content mismatch | File name says invoice manager but content is investment researcher |
| Duplicate responsibility | Two Agents claim same owner/routing scope |
| Unclear risk level | Risk cannot be determined |
| Unsafe permission | Critical Agent has production write without review |
| Pending human review | Business owner / Guardian has not approved |
| Unclear routing target | Router cannot determine safe route |
| Guardian purity issue | Guardian acts as hidden executor |
| Sovereign boundary issue | Sovereign claims irreversible execution |
| Core contamination | SoMatch / SHINES-only logic appears in ESTRIX Core |
| Application redefinition | L3 file tries to redefine ESTRIX boundary |
| Engagement overreach | L4 deliverable changes company-level architecture |
| Active reference conflict | A quarantined file is still referenced as active |
| Frontmatter-content conflict | Metadata grants authority not supported by content |

---

## 4. Quarantine Frontmatter

Quarantined files should use:

```yaml
---
name:
title:
description:
layer: _quarantine
context_layer: Repository Governance
pace_layer: Quarantine
risk_level: blocked
status: quarantined
owner: Agent Repository Steward
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: none
routing_enabled: false
registry_enabled: false
version:
quarantine_reason:
original_path:
proposed_path:
required_review:
related_files:
---
```

---

## 5. Quarantine Decision

Codex may recommend quarantine when evidence supports it. Codex may move low-risk files to quarantine if the task explicitly asks for repository cleanup and the reason is mechanical. Codex must not restore Medium / High / Critical quarantined files without required review.

Quarantine is a safety state, not a punishment.

---

## 6. Active Reference Ban

Quarantined files must not be referenced by active registry, router, agent-index, capability-map, responsibility matrix or production routing rules unless the reference explicitly marks them as quarantined.

FAIL if a quarantined file is listed as active, has `routing_enabled: true`, has tool permissions beyond `none`, is used as active execution target, or is required for v1.4 activation.

Plain-language interpretation:

> 關進禁閉室的人，不能還掛在值勤表上。

---

## 7. Restoration Requirements

A quarantined file may be restored only when the quarantine reason is resolved, frontmatter is corrected, path matches layer, risk level is assigned, tool permissions are safe, routing status is correct, duplicate responsibility is resolved, required Guardian review is complete, required owner is identified, registry is updated, WORM-style note is created for High / Critical restoration, human approval is recorded if Medium risk or above, active reference conflicts are removed, related files are updated, and PR / CI validation passes or returns approved HOLD resolution.

---

## 8. Restoration Review Matrix

| Risk Level | Codex Autofix | Human Review | Guardian Review | WORM |
|---|---:|---:|---:|---:|
| Low | Allowed for metadata/format | Optional | No | No |
| Medium | Limited | Required | Conditional | Optional |
| High | Not autonomous | Required | Required | Required |
| Critical | Not autonomous | Required | Required | Required |
| Blocked | Not allowed | Required | Required | Required |

Medium restoration requires WORM when it affects routing, permissions, registry entries, active references or tool permission restoration.

---

## 9. Quarantine Record Template

```markdown
# Quarantine Record

## File

- Original Path:
- Current Quarantine Path:
- Proposed Path:
- Date:
- Owner:

## Reason

- Quarantine Reason:
- Evidence:
- Risk Level:
- Affected Registry:
- Affected Routing:

## Required Repair

- Frontmatter:
- Layer:
- Risk Level:
- Tool Permissions:
- Hooks:
- Owner:
- Review:
- Related Files:
- Registry Update:

## Restoration Decision

- Restore Allowed:
- Required Approval:
- Required Guardian:
- WORM Needed:
- Router Decision:
- Notes:
```

---

## 10. BLOCK and HOLD Conditions

Return `BLOCK` when someone tries to route to quarantined file as active, restore file without required review, use unsafe production permissions, violate law/security/platform safety, bypass WORM / Guardian / human approval, claim authority inconsistent with its layer, remove quarantine reason without resolving it, hide quarantined status through path rename, or reference quarantined file as active routing target.

Return `HOLD` when quarantine reason is unclear, proposed active path is unclear, risk level is TBD, owner is missing, required review is missing but repairable, file may be duplicate but evidence is incomplete, content mismatch requires human interpretation, active reference may exist but requires registry scan, or restoration target is disputed.

---

## 11. Quarantine Restore PR Requirements

A restore PR must include:

```text
Restored File:
Original Path:
Quarantine Path:
Proposed Active Path:
Reason for Quarantine:
Evidence of Repair:
Risk Level:
Required Hooks:
Guardian Review:
Human Approval:
Registry Updated:
Router Decision:
Unresolved Risks:
```

Medium+ restore PRs require human review. High / Critical restore PRs require Guardian Review and WORM-style record.

---

## 12. Final Rule

> Quarantine is not deletion. Quarantine is a safety buffer that prevents uncertain files from becoming active authority.
