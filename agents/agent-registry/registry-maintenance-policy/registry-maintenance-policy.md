---
name: registry-maintenance-policy
title: PAEX-AI Agent Registry Maintenance Policy
description: Defines how the agent registry, router, responsibility matrix, capability map, layer map, risk map and secondary hooks are maintained, reviewed, repaired and audited.
layer: agent-registry
pace_layer: Repository Governance / Registry Maintenance
risk_level: high
owner: Agent Repository Steward
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
related_files:
  - ../../../AGENTS.md
  - ../../../README.md
  - ../../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - ../agent-router/agent-router.md
  - ../risk-level-map/risk-level-map.md
  - ../secondary-hooks-map/secondary-hooks-map.md
  - ../frontmatter-schema/frontmatter-schema.md
  - ../../governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../governance/worm-event-schema/worm-event-schema.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
context_layer: Repository Governance
status: active
requires_worm: true
requires_guardian_review: true
requires_human_approval: true
human_approval_scope:
  - file_activation
  - registry_policy_change
  - registry_index_change
  - routing_authority_change
  - high_or_critical_registry_exception
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - modify_registry_authority_without_review
  - activate_agent_without_frontmatter_validation
  - bypass_router_for_registry_updates
  - restore_quarantined_file_without_required_review
worm_scope:
  - file_activation
  - registry_policy_change
  - registry_index_change
  - routing_authority_change
  - high_or_critical_registry_exception
  - registry_restore_or_quarantine_reference_change
allowed_actions:
  - repair_registry_metadata
  - propose_registry_synchronization
  - validate_related_files_paths
  - detect_duplicate_responsibility
  - propose_quarantine_for_unsafe_registry_entries
  - require_guardian_review_for_registry_authority_change
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - duplicate_frontmatter_key_check
  - registry_index_consistency_check
  - router_consistency_check
  - guardian_review_record
  - ci_validation_result
  - worm_activation_record
  - human_approval_record
rollback_required: true
canary_required: false
exemption_reason: registry_policy_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

# PAEX-AI Agent Registry Maintenance Policy

## 0. Activation and Authority Boundary

Registry authority changes, routing authority changes, High / Critical registry exceptions and quarantine restoration impacts require human approval.

Codex may repair formatting and path metadata.

Codex must not expand authority, routing, status, risk level, tool permissions or lifecycle state without required review.

## 1. Purpose

This file defines how the `agents/agent-registry/` layer is maintained, reviewed, repaired and audited.

The Agent Registry is the dispatch brain of the `agents/` repository.

It tells Codex, human operators, orchestration tools and future automation layers:

- which Agents exist;
- where each Agent lives;
- what each Agent owns;
- what each Agent must not own;
- what each Agent can safely do;
- what risk level each Agent carries;
- which files may be routed;
- which files are only governance references;
- which Guardian or governance protocol must be attached;
- which files are quarantined, deprecated or retired.

Core rule:

> The registry must reflect operational truth. If the registry lies, the router becomes dangerous.

This policy exists to prevent repository drift from becoming governance failure.

A wrong registry entry can cause:

- the wrong Agent to receive a task;
- a Mission Agent to self-review High Risk work;
- a quarantined file to be treated as active;
- a draft file to receive production routing;
- a High Risk workflow to bypass Guardian Review;
- a Critical workflow to appear automatable;
- a duplicate Agent to create unclear ownership;
- Codex to repair metadata while accidentally expanding authority.

Therefore, registry maintenance is not clerical cleanup.

It is authority control.

---

## 2. Governance Positioning

The Agent Registry belongs to the `agent-registry` repository layer and functions as a Platform / Repository Governance control surface.

It is not itself a Mission Agent.

It does not execute frontline work.

It does not approve business decisions.

It does not override Guardian or Sovereign governance.

Its job is to ensure that routing, responsibility, capability, risk and layer placement remain accurate.

In PAEX-AI terms:

| Registry Function | Governance Meaning |
|---|---|
| Agent index | Identity control |
| Responsibility matrix | Ownership control |
| Router | Dispatch control |
| Capability map | Capability visibility |
| Layer map | Authority boundary control |
| Risk-level map | Risk classification control |
| Secondary hooks map | Companion review and escalation control |
| Frontmatter schema | Metadata contract |
| Maintenance policy | Registry governance law |

The registry must be maintained as a source of truth.  
If the registry and the actual file content conflict, the conflict must be resolved before production routing.

---

## 3. Controlled Registry Files

This policy governs the following files.

| File | Function | Governance Risk |
|---|---|---|
| `agent-index.md` | Canonical list of active, draft, active_candidate, deprecated, disabled, blocked, template and quarantined Agents / artifacts. | If wrong, the system may believe nonexistent or unsafe capabilities are available. |
| `agent-responsibility-matrix.md` | Defines primary ownership, non-ownership, escalation paths and final decision boundaries. | If wrong, accountability becomes blurred. |
| `agent-router.md` | Defines task-to-Agent routing logic. | If wrong, tasks may go to unsafe or unauthorized Agents. |
| `capability-map.md` | Maps capability tags to Agents and support files. | If wrong, capabilities may be overstated or duplicated. |
| `layer-map.md` | Defines PAEX / C-A-E-P layer placement and boundary rules. | If wrong, Agents may operate at the wrong authority layer. |
| `risk-level-map.md` | Defines risk classification standards and Agent-level risk mapping. | If wrong, High / Critical workflows may be under-controlled. |
| `secondary-hooks-map.md` | Defines companion reviewers, fallback Agents and mandatory governance hooks. | If wrong, workflows may bypass Guardian, WORM, Canary or Kill Switch controls. |
| `frontmatter-schema.md` | Defines the required metadata contract for formal files. | If wrong, the registry loses identity and authority consistency. |
| `registry-maintenance-policy.md` | Defines this maintenance policy. | If weakened, the entire registry can drift. |

These files should be treated as controlled governance artifacts.

Codex may propose repairs, but should not silently rewrite their authority model.

---

## 4. Maintenance Principles

## 4.1 Single Source of Registry Truth

No Agent or governance artifact should be considered production-ready unless it is represented consistently across the required registry surfaces.

For an active routable Agent, the following must agree:

- YAML frontmatter;
- file path;
- `agent-index.md`;
- `agent-responsibility-matrix.md`;
- `agent-router.md`;
- `capability-map.md`;
- `layer-map.md`;
- `risk-level-map.md`;
- `secondary-hooks-map.md`, if applicable.

If these disagree, the registry is not safe.

Example:

```text
File says:
risk_level: high

risk-level-map says:
medium

router routes it as:
low-risk automation

Result:
Registry conflict. Must be repaired before routing.
```
---

## 4.2 Registry Update Workflow

Registry updates must follow a controlled workflow.

Required sequence:

1. Identify the affected file.
2. Validate frontmatter against `frontmatter-schema.md`.
3. Confirm file path and `layer` alignment.
4. Confirm `risk_level` against `risk-level-map.md`.
5. Confirm mandatory hooks against `secondary-hooks-map.md`.
6. Confirm routing eligibility against `agent-router.md`.
7. Check whether the file is active, active_candidate, draft, deprecated, disabled, blocked, template or quarantined.
8. Validate `related_files` paths.
9. Update registry surfaces only when the change is consistent.
10. Record evidence for High / Critical registry changes.

Registry updates must not silently change authority.

A registry update that changes routing authority, tool permission, lifecycle status, risk level, Guardian requirement, quarantine status or High / Critical hooks requires review.

---

## 4.3 Codex Autofix Boundary

Codex may autofix:

- typo-level metadata errors;
- Markdown formatting;
- obvious path formatting mistakes;
- broken optional reference paths when the correct path is mechanically clear;
- missing `context_layer` when the file location and role make it obvious;
- harmless title or capitalization cleanup;
- `routing_enabled: false` for registry, governance, shared or quarantine files when required by policy;
- `registry_enabled: true` for registry files when required by policy.

Codex must not autofix without required review:

- risk level change;
- layer change;
- status promotion to `active`;
- routing authority expansion;
- tool permission escalation;
- Guardian / Mission / Platform / Sovereign role conversion;
- High / Critical required hook removal;
- WORM removal;
- human approval removal;
- quarantine restoration;
- registry authority change;
- routing policy change;
- production-write permission;
- application-to-core promotion;
- L4-to-L2 promotion;
- any change that increases blast radius.

Plain-language rule:

> Codex may tighten loose screws.  
> Codex must not redesign the machine without review.

---

## 4.4 Related Files Validation

`related_files` must be valid relative paths from the current file location unless the file is root-level.

Validation rules:

- FAIL when a required governance dependency path is broken.
- FAIL when a registry file points to an outdated flat path while the actual repository uses nested paths.
- FAIL when an active or active_candidate file depends on a quarantined file as an active routing target.
- HOLD when the path base is ambiguous.
- WARNING when an optional reference is missing and explicitly marked as `TBD`.
- WARNING when a Low-risk draft references a planned file that is not yet created.

Root-level governance files must use repository-root relative paths.

Nested governance files must use paths relative to their own file location.

---

## 4.5 Duplicate Responsibility Handling

Duplicate responsibility exists when two or more Agents or governance files claim the same primary ownership, routing authority, final approval boundary or execution scope without a clear hierarchy.

Return HOLD when:

- duplicate ownership is suspected but evidence is incomplete;
- two Agents appear to cover the same capability;
- responsibility overlap may be intentional but is not documented;
- escalation ownership is unclear.

Return BLOCK when:

- duplicate authority allows High / Critical work to bypass review;
- a Mission Agent claims Guardian authority;
- a Guardian Agent also claims production execution authority;
- two files define conflicting routing rules for the same task;
- duplicate registry entries create unsafe active routing.

Required resolution:

- identify the primary owner;
- identify secondary or support owners;
- define escalation path;
- update agent-index, responsibility matrix and router;
- quarantine unsafe duplicate files if necessary.

---

## 4.6 Quarantine and Restoration Relationship

Registry maintenance must respect quarantine policy.

A quarantined file must not be:

- routed as active;
- listed as active in agent-index;
- used as an active execution target;
- granted tool permissions;
- restored without required review;
- referenced as a required active dependency.

A quarantined file may be restored only when:

- quarantine reason is resolved;
- frontmatter is corrected;
- path-layer mapping is valid;
- risk level is assigned;
- tool permissions are safe;
- routing status is correct;
- duplicate responsibility is resolved;
- Guardian review is completed when required;
- human approval is recorded for Medium+ restoration;
- WORM record exists for High / Critical restoration;
- registry files are updated;
- PR / CI validation passes.

---

## 5. HOLD and BLOCK Conditions

Return HOLD when:

- registry and file content conflict;
- risk level is unclear;
- layer mapping is unclear;
- routing eligibility is unclear;
- related_files path base is ambiguous;
- duplicate responsibility may exist;
- High / Critical hooks are incomplete but repairable;
- required review is missing but can be obtained;
- active file references may include quarantined files but require scan;
- registry surfaces are out of sync.

Return BLOCK when:

- a quarantined file is routed as active;
- High / Critical work is routed without mandatory hooks;
- registry authority is modified without review;
- tool permissions are escalated without approval;
- Mission self-approves High / Critical work;
- Guardian executes production work;
- Sovereign directly executes irreversible action;
- frontmatter grants authority contradicted by governance;
- required WORM, Guardian Review or human approval is bypassed.

---

## 6. Registry Maintenance PR Requirements

A registry maintenance PR must include:

```text
Registry Maintenance PR

Files Changed:
Registry Surfaces Affected:
Reason for Change:
Risk Level:
Business Context Layer:
Frontmatter Validation:
Related Files Check:
Duplicate Responsibility Check:
Router Impact:
Capability Map Impact:
Risk Map Impact:
Secondary Hooks Impact:
Quarantine Impact:
Guardian Review Needed:
WORM Needed:
Human Approval Needed:
Tests / CI:
Unresolved Risks:
Reviewer:
```

High / Critical registry PRs must include:

- Guardian Review record;
- WORM-style event record;
- rollback plan;
- human approval record where required;
- evidence that routing authority did not expand silently.

---

## 7. Final Rule

> Registry maintenance is not file cleanup.  
> Registry maintenance is authority maintenance.  
> If the registry is wrong, the router is unsafe.  
> > If the router is unsafe, Codex must stop, hold or escalate.

---
