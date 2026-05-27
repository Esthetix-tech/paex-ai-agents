---
name: PR CI Validation Checklist
title: PAEX-AI PR / CI Validation Checklist
description: Pull request and CI validation checklist for AGENTS.md v1.4 readiness, covering frontmatter, routing, risk, hooks, quarantine and Business Architecture Context Stack rules.
layer: governance
context_layer: Repository Governance
pace_layer: Repository Governance / PR CI Validation
risk_level: high
status: active_candidate
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - file_activation
  - checklist_policy_change
  - v1_4_activation
  - required_check_downgrade
  - required_check_exception
  - dry_run_bypass
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-candidate-patch-03
requires_worm: true
worm_scope:
  - checklist_activation
  - checklist_policy_change
  - v1_4_activation
  - required_check_exception
  - failed_required_check_override
  - dry_run_result_record
requires_guardian_review: true
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - approve_v1_4_without_companion_files
  - ignore_high_or_critical_missing_hooks
  - route_quarantined_files_as_active
  - treat_warning_as_pass_for_required_checks
  - mark_active_without_dry_run
rollback_required: true
canary_required: false
related_files:
  - ../../agent-registry/frontmatter-schema/frontmatter-schema.md
  - ../../agent-registry/agent-router/agent-router.md
  - ../../agent-registry/risk-level-map/risk-level-map.md
  - ../../agent-registry/secondary-hooks-map/secondary-hooks-map.md
  - ../../agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
  - ../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
exemption_reason: metadata_checklist_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_metadata_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

# PR / CI Validation Checklist｜PAEX-AI v1.4 Readiness

## 1. Purpose

This checklist defines required pull request and CI checks before AGENTS.md may be upgraded from v1.3.2 Stable Governance Draft to v1.4 Active Repository Governance Baseline.

Core rule:

> v1.4 is not only a better document. v1.4 must be mechanically enforceable.

Plain-language interpretation:

> v1.3.2 是治理憲法草案定稿。v1.4 必須開始有警察、法院、稽核表與自動檢查。

---

## 2. PR Validation Summary

Every PR touching `agents/` should be checked for frontmatter validity, folder-layer consistency, risk-level consistency, routing eligibility, secondary hooks, Guardian purity, Mission execution boundary, Platform infrastructure boundary, Sovereign execution boundary, shared / quarantine non-routing rules, Business Architecture Context Stack contamination, ESTRIX Core contamination, Use Case promotion opportunities, related file dependency integrity, registry synchronization and version lifecycle discipline.

---

## 3. Required CI Checks

| Check ID | Check Name | Required For | Failure Result |
|---|---|---|---|
| CI-001 | Frontmatter Exists | all governed `.md` files | FAIL |
| CI-002 | Required Fields Present | all governed `.md` files | FAIL |
| CI-003 | Enum Values Valid | all governed `.md` files | FAIL |
| CI-004 | Path Matches Layer | all Agent / context files | FAIL |
| CI-005 | Risk Level Present | all governed files | FAIL |
| CI-006 | High / Critical Hooks Present | High / Critical files | FAIL |
| CI-007 | Routing Enabled Validity | all files | FAIL |
| CI-008 | Shared Non-Routing Rule | `shared/` files | FAIL |
| CI-009 | Quarantine Non-Routing Rule | `_quarantine/` files | FAIL |
| CI-010 | Guardian Purity Check | `guardian/` files | HOLD / FAIL |
| CI-011 | Mission No Self-Approval | `mission/` files | FAIL |
| CI-012 | Sovereign No Direct Execution | `sovereign/` files | FAIL |
| CI-013 | Registry Files Not Execution Agents | `agent-registry/` files | FAIL |
| CI-014 | L2 Core Contamination Check | `20_estrix_core/` + core engine files | HOLD |
| CI-015 | L3 Does Not Redefine ESTRIX | `30_applications/` | HOLD |
| CI-016 | L4 Does Not Redefine Architecture | `40_engagements/` | HOLD |
| CI-017 | Quarantine Restore Review | quarantine restore PRs | FAIL |
| CI-018 | Related Files Exist | files with `related_files` | WARNING / FAIL |
| CI-019 | Duplicate Responsibility Scan | new Agent files | HOLD |
| CI-020 | Version Updated | modified governance files | WARNING |
| CI-021 | Context Layer Present | L0–L4 / governance context files | FAIL |
| CI-022 | Tool Permissions Valid | all governed files | FAIL |
| CI-023 | Status Lifecycle Valid | all governed files | FAIL |
| CI-024 | High / Critical Forbidden Actions Present | High / Critical files | FAIL |
| CI-025 | Human Approval Rule Valid | Critical / irreversible files | FAIL |
| CI-026 | Registry Index Updated | new / moved / renamed Agent files | HOLD / FAIL |
| CI-027 | Companion Governance Files Synchronized | v1.4 governance files | FAIL |
| CI-028 | Exempt File Rule Applied | non-governed assets | WARNING / FAIL |
| CI-029 | Duplicate Frontmatter Keys | all governed `.md` files | FAIL |

---

## 4. Frontmatter Checklist

For every governed file:

```text
[ ] Frontmatter exists.
[ ] name exists.
[ ] title exists.
[ ] description exists.
[ ] layer exists.
[ ] context_layer exists where required.
[ ] pace_layer exists.
[ ] risk_level exists.
[ ] status exists.
[ ] owner exists.
[ ] review_required exists.
[ ] human_approval_required exists.
[ ] codex_autofix_allowed exists.
[ ] tool_permissions exists.
[ ] routing_enabled exists.
[ ] registry_enabled exists.
[ ] version exists.
[ ] related_files is present or intentionally omitted.
```

For High / Critical files:

```text
[ ] requires_worm is defined.
[ ] requires_guardian_review is defined.
[ ] requires_human_approval is defined or explicitly justified.
[ ] secondary_hooks are listed.
[ ] forbidden_actions are listed.
[ ] rollback_required is defined where applicable.
[ ] canary_required is defined where applicable.
```

---

## 5. Path and Layer Checklist

```text
[ ] files under agents/core use C / Core Strategy or valid context layer.
[ ] files under agents/mission use A / Mission.
[ ] files under agents/guardian use E / Guardian.
[ ] files under agents/platform use P / Platform.
[ ] files under agents/sovereign use Sovereign.
[ ] files under agents/governance are protocols, not execution agents.
[ ] files under agents/agent-registry are metadata/routing/schema files.
[ ] files under agents/shared are not routing targets.
[ ] files under agents/_quarantine are not routing targets.
[ ] L0 files are command context only.
[ ] L1 files are Esthetix Arsenal context only.
[ ] L2 files are ESTRIX Core context only.
[ ] L3 files are Application / Use Case context only.
[ ] L4 files are Engagement / Project context only.
```

---

## 6. Risk / Hook Checklist

```text
[ ] Risk level is not lower than domain trigger minimum.
[ ] Payment / ledger / refund / settlement has Finance / Ledger hooks.
[ ] Public brand content has Brand / Compliance hooks.
[ ] PII has Privacy / Data Boundary hooks.
[ ] MCP tool exposure has Security / Tool Permission hooks.
[ ] Production write action has Production Readiness + WORM.
[ ] Guardian Veto override has Sovereign + Human Approval.
[ ] Kill Switch release has Kill Switch Governor + Sovereign.
[ ] Human Override has accountability record + WORM.
[ ] Quarantine restore has Quarantine Policy + Registry Maintenance review.
[ ] ESTRIX Core module change has Core Steward / Architecture review.
[ ] Critical irreversible work has explicit human approval.
```

---

## 7. Business Architecture Context Stack Checklist

For Esthetix / ESTRIX / SHINES / SoMatch changes:

```text
[ ] Task classified into L0 / L1 / L2 / L3 / L4.
[ ] Esthetix is not described as SoMatch.
[ ] Esthetix is not reduced to SHINES technical department.
[ ] ESTRIX is not described as SHINES-only.
[ ] ESTRIX is not described as SoMatch-only.
[ ] ESTRIX is not described as beauty-only.
[ ] SoMatch is described as SHINES external service brand powered by ESTRIX.
[ ] SHINES validates ESTRIX but does not define full ESTRIX boundary.
[ ] Reusable capability is placed in L2.
[ ] Brand-specific packaging is placed in L3.
[ ] One-time delivery is placed in L4.
```

---

## 8. Core Contamination Checklist

For changes to ESTRIX Core:

```text
[ ] Capability is reusable across two or more current/future Use Cases.
[ ] Logic is independent from brand voice.
[ ] Data model is useful outside current application.
[ ] Duplication outside Core would create inconsistency.
[ ] Feature is engine behavior, not service packaging.
[ ] No SoMatch-only wording is added to Core.
[ ] No SHINES-only process detail is added to Core.
[ ] No temporary campaign assumption is added to Core.
[ ] No client-specific artifact is added to Core.
```

If any item fails, return `HOLD` and propose split into L2 / L3 / L4.

---

## 9. Boundary Checklists

Guardian files must primarily review, verify, audit, veto or enforce. They must not directly execute production work, approve their own execution or overlap with Mission without explanation.

Mission files must execute delivery or operational work. They must not claim final approval for High / Critical tasks, bypass Guardian Review or claim veto authority.

Platform files must provide reusable infrastructure. They must not be written as final business decision-makers.

Sovereign files must prepare decision packages and must not execute irreversible action.

Quarantined files must have `routing_enabled: false`, `status: quarantined`, `tool_permissions: none`, a recorded reason, original path, proposed path if known and restore evidence.

---

## 10. Related Files Validation Rule

FAIL when related files point to required governance files and the path is broken, when active / active_candidate files have broken required related paths, or when related files point to quarantined files as active dependency.

WARNING when related files are optional references, intentionally omitted for Low-risk files, draft/template files, or planned dependencies marked `TBD`.

---

## 11. CI vs Human Review Boundary

Mechanical CI may automatically FAIL missing frontmatter, invalid enum, wrong path-layer mapping, `routing_enabled` violation, quarantine active routing, missing required hooks, broken required related files and shared file routing target violations.

Mechanical CI should return HOLD for Guardian purity ambiguity, duplicate responsibility, Core contamination suspicion, L3 redefining ESTRIX, L4 architecture overreach, unclear business context layer or unclear risk classification.

Human / Guardian review is required when CI detects semantic ambiguity, risk is High or Critical, file changes routing authority, file affects registry/hooks/quarantine/v1.4 activation baseline or file changes Core / Application / Engagement boundary.

---

## 12. PR Review Comment Template

```text
PAEX-AI PR Review

Risk Level:
Business Context Layer:
C-A-E-P Mapping:
Files Touched:
Frontmatter Check:
Path / Layer Check:
Required Hooks:
Guardian Review Needed:
WORM Needed:
Canary / Rollback Needed:
Quarantine Impact:
Core Contamination Risk:
Use Case Promotion Opportunity:
Router Decision:
Unresolved Risks:
Reviewer:
```

---

## 13. v1.4 Activation Checklist

AGENTS.md may be upgraded to v1.4 Active Repository Governance Baseline only when:

```text
[ ] frontmatter-schema.md exists and is approved.
[ ] agent-router.md exists and is approved.
[ ] secondary-hooks-map.md exists and is approved.
[ ] risk-level-map.md exists and is approved.
[ ] quarantine-policy.md exists and is approved.
[ ] PR / CI validation checklist exists and is approved.
[ ] Repository files have been checked against required frontmatter.
[ ] High / Critical files have required hooks.
[ ] Shared and quarantine folders are non-routable.
[ ] Business Architecture Context Stack files are in place.
[ ] ESTRIX Core contamination rules are enforceable.
[ ] K / CEO approves v1.4 activation.
```

---

## 14. Final v1.4 Gate

Before marking this checklist as `active / v1.4`, verify:

```text
[ ] This checklist itself passes frontmatter-schema.md.
[ ] agent-router.md uses the strengthened v1.4 routing algorithm.
[ ] risk-level-map.md includes upward classification and no capability-based downgrade.
[ ] secondary-hooks-map.md covers all High / Critical triggers in AGENTS.md.
[ ] quarantine-policy.md blocks active references to quarantined files.
[ ] CI distinguishes mechanical FAIL from semantic HOLD.
[ ] Business Architecture Context Stack checks are represented in CI.
[ ] ESTRIX Core contamination checks are represented in CI.
[ ] At least one dry run has been performed against sample good / bad files.
[ ] K / CEO approves v1.4 activation.
```

---

## 15. Dry Run Test Cases

| Test Case | Expected Result |
|---|---|
| Missing frontmatter Agent | FAIL |
| Shared file with `routing_enabled: true` | FAIL |
| Quarantined file referenced as active | FAIL |
| Mission Agent claims final approval | FAIL |
| Guardian Agent claims production execution | HOLD / FAIL |
| Critical file missing WORM | FAIL |
| SoMatch wording added to ESTRIX Core | HOLD |
| L4 engagement tries to redefine ESTRIX | HOLD |
| Payment logic without Finance / Ledger hooks | FAIL / ESCALATE |
| Clean Low-risk documentation update | PROCEED |
| Broken required `related_files` path | FAIL |
| Duplicate frontmatter keys | FAIL |

---

## 16. Final Rule

> A governance document becomes a governance system only when it can be checked, routed, blocked, escalated and audited.
