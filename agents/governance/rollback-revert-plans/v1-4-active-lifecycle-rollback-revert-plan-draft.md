---
name: v1-4-active-lifecycle-rollback-revert-plan-draft
title: PAEX-AI Agents Repository v1.4 Active Lifecycle Rollback Revert Plan Draft
description: Rollback and revert plan draft for PAEX-AI agents repository v1.4 active lifecycle promotion, pending explicit approval.
layer: governance
context_layer: Repository Governance
pace_layer: Repository Governance / Rollback Revert Plan
risk_level: high
status: draft
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - lifecycle_promotion_rollback
  - v1_4_active_lifecycle_promotion
  - governance_baseline_activation
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-active-lifecycle-rollback-revert-plan-draft
requires_worm: true
worm_scope:
  - lifecycle_promotion_rollback
  - v1_4_active_lifecycle_promotion
  - governance_baseline_activation
requires_guardian_review: true
secondary_hooks:
  - governance-review
  - registry-maintenance-review
  - ci-validation-review
forbidden_actions:
  - treat_rollback_plan_draft_as_activation_approval
  - execute_revert_without_human_review
  - mark_repository_active_from_rollback_plan_draft
  - expand_routing_authority
  - expand_tool_permissions
  - lower_risk_level
  - bypass_worm_for_rollback
allowed_actions:
  - prepare_rollback_revert_plan_draft
  - identify_revert_conditions
  - document_safe_recovery_path
  - record_required_rollback_evidence
  - define_human_review_gates
evidence_required:
  - post_merge_validation_pass_on_origin_main
  - validated_commit_sha
  - formal_guardian_approval
  - final_worm_activation_record
  - explicit_k_ceo_approval
  - final_validation_result
  - rollback_validation_result
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
  - ../worm-event-schema/worm-event-schema.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
  - ../v1-4-lock-candidate-readiness-record/v1-4-lock-candidate-readiness-record.md
  - ../guardian-review-approvals/v1-4-active-activation-guardian-review-approval-draft.md
  - ../worm-activation-records/v1-4-active-final-worm-activation-record-draft.md
  - ../k-ceo-approval-memos/v1-4-active-activation-k-ceo-approval-memo-draft.md
  - ../lifecycle-promotion-records/v1-4-active-formal-activation-decision-record-draft.md
  - ../lifecycle-promotion-checklists/v1-4-active-lifecycle-promotion-checklist-draft.md
  - ../active-status-change-plans/v1-4-active-status-change-plan-draft.md
  - ../final-validation-checklists/v1-4-active-final-validation-checklist-draft.md
exemption_reason: rollback_revert_plan_draft_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_rollback_plan
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-28
---

# PAEX-AI Agents Repository v1.4 Active Lifecycle Rollback Revert Plan Draft

## Plan State

current state: v1.4-lock-candidate-ready

target state: active, pending approval

not active yet

This rollback / revert plan is a draft. It does not authorize automatic activation.

## Evidence Source

Evidence source: POST_MERGE_VALIDATION_PASS on origin/main.

validated commit: 4c29364bc5920c33fe431d6acac80ef68aacb8cd

## Rollback Boundary

Active activation requires formal Guardian approval, final WORM activation record, explicit K / CEO approval and final validation.

Rollback or revert action after lifecycle promotion must also preserve:

- no routing authority expansion;
- no tool permission expansion;
- no risk level reduction;
- WORM evidence for High / Critical lifecycle changes;
- human review for rollback execution.

## Revert Triggers

Use this plan if any of the following occurs after an approved lifecycle promotion:

- final validation fails after status change;
- related_files paths break;
- routing safety changes unexpectedly;
- tool permission safety changes unexpectedly;
- risk level is lowered without approval;
- Sovereign index becomes routable;
- activation approval evidence is incomplete or disputed;
- active status is applied outside the approved scope.

## Draft Recovery Path

1. Pause further lifecycle promotion actions.
2. Preserve evidence and validation output.
3. Open a rollback review note.
4. Revert only the approved lifecycle status change scope.
5. Restore `v1.4-lock-candidate-ready` state if active promotion is invalid.
6. Run validation after revert.
7. Record WORM evidence for the rollback.
8. Require human review before closing the rollback.

## Router Decision

PROCEED for lifecycle promotion package review.

HOLD for active activation.
