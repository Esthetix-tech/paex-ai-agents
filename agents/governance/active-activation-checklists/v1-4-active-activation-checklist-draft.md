---
name: v1-4-active-activation-checklist-draft
title: PAEX-AI Agents Repository v1.4 Active Activation Checklist Draft
description: Active activation checklist draft for PAEX-AI agents repository v1.4, pending explicit approval and final validation.
layer: governance
context_layer: Repository Governance
pace_layer: Repository Governance / Activation Checklist
risk_level: high
status: draft
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - active_activation_checklist
  - v1_4_active_activation
  - governance_baseline_approval
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-active-activation-checklist-draft
requires_worm: true
worm_scope:
  - active_activation_checklist
  - v1_4_active_activation
  - governance_baseline_approval
requires_guardian_review: true
secondary_hooks:
  - governance-review
  - registry-maintenance-review
  - ci-validation-review
forbidden_actions:
  - treat_checklist_draft_as_activation
  - mark_repository_active_from_checklist_draft
  - mark_baseline_files_active_from_checklist_draft
  - expand_routing_authority
  - expand_tool_permissions
  - lower_risk_level
  - bypass_formal_guardian_review_approval
  - bypass_final_worm_activation_record
  - bypass_k_ceo_or_delegated_approval
allowed_actions:
  - document_activation_checklist_items
  - summarize_validation_evidence
  - identify_activation_gates
  - record_pending_approval_status
  - prepare_final_validation_requirements
evidence_required:
  - post_merge_validation_pass_on_origin_main
  - validated_commit_sha
  - formal_guardian_review_approval
  - final_worm_activation_record
  - k_ceo_or_delegated_approval_memo
  - final_activation_validation_result
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
  - ../guardian-review-records/v1-4-lock-candidate-guardian-review-record.md
  - ../worm-activation-records/v1-4-lock-candidate-worm-activation-record.md
  - ../guardian-review-approvals/v1-4-active-activation-guardian-review-approval-draft.md
  - ../worm-activation-records/v1-4-active-final-worm-activation-record-draft.md
  - ../k-ceo-approval-memos/v1-4-active-activation-k-ceo-approval-memo-draft.md
exemption_reason: active_activation_checklist_draft_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_activation_checklist
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-28
---

# PAEX-AI Agents Repository v1.4 Active Activation Checklist Draft

## Checklist State

current state: v1.4-lock-candidate-ready

target state: active, pending approval

not active yet

This checklist is a draft. It does not mark the repository as active and does not authorize automatic activation.

## Evidence Source

Evidence source: POST_MERGE_VALIDATION_PASS on origin/main.

validated commit: 8828e046fbe62c9bc0df4ca01ce60c175cac0c5a

## Activation Gate Checklist

- [ ] Confirm 12-file governance baseline exists.
- [ ] Confirm readiness record exists and remains lock-candidate-ready only.
- [ ] Confirm Guardian Review Record draft remains draft and is not formal approval.
- [ ] Confirm WORM Activation Record draft remains draft and is not final immutable activation record.
- [ ] Confirm formal Guardian Review approval is explicitly recorded.
- [ ] Confirm final WORM activation record is explicitly finalized and sealed.
- [ ] Confirm K / CEO or delegated approval is explicitly recorded.
- [ ] Confirm active activation requires explicit K / CEO or delegated approval.
- [ ] Confirm no automatic activation.
- [ ] Confirm no repository or baseline file is active before approval.
- [ ] Confirm no routing authority expansion.
- [ ] Confirm no tool permission expansion.
- [ ] Confirm no risk level reduction.
- [ ] Confirm Sovereign index remains non-routable.
- [ ] Run final validation immediately before activation.

## Non-Activation Boundary

Until every checklist item is completed and approved:

- repository state remains `v1.4-lock-candidate-ready`;
- target state remains `active, pending approval`;
- not active yet;
- active activation remains blocked from execution;
- no automatic activation is allowed.

## Required Approval Evidence

Active activation requires explicit K / CEO or delegated approval.

Required evidence:

- formal Guardian Review approval;
- final WORM activation record;
- K / CEO or delegated approval memo;
- final validation result;
- approved activation scope;
- approved activation timestamp.

## Router Decision

PROCEED for approval package review.

HOLD for active activation.
