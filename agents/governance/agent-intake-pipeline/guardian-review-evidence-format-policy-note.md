# Guardian Review Evidence Format Policy Note

## Positioning

This is a documentary-only evidence format policy note.

This note defines acceptable Guardian Review evidence formats for governance workflow clarity.
This note does not retroactively modify prior PR evidence.
This note does not create GitHub-native review objects.
This note does not mutate formal approval evidence.
This note does not mutate audit evidence.
This note does not mutate WORM records.
This note does not mutate the Sovereign index.
This note does not enter Phase 5.
This note does not activate agents.
This note does not authorize routing/tool expansion.
This note does not increase safe-managed count.
This note does not treat Guardian Review as K / CEO / Sovereign substitute.

## Problem Statement

- Current workflow may record Guardian Review PASS through Codex PR review transcript and post-merge validation.
- GitHub-native PR metadata may show reviews: [].
- This creates evidence format ambiguity during governance audit.
- The ambiguity is about evidence preservation format, not necessarily review failure.
- Accepted evidence forms and hierarchy should be defined before retroactive correction or stronger future enforcement.

## Validated Baseline

- validated_ref: origin/main
- validated_commit: fdfaa0efd941dbd83ea9285e25ced7ad7db69ee4
- current_safe_managed_total: 53
- phase_5_execution: HOLD
- phase_5_artifact_mutation: HOLD
- activation: HOLD
- routing_tool_expansion: HOLD
- authority_expansion: HOLD
- count_increase_beyond_53: HOLD
- sovereign_index_routing_enabled: false

## Accepted Evidence Formats

### A. Codex PR Review Transcript in Conversation / Task Log

- use: short-term acceptable evidence for documentary governance workflow
- strength: medium
- requirement: must be traceable to PR number, branch, commit, review result, Guardian Review result, WORM assessment, and router decision

### B. PR Comment Containing Guardian Review Result

- use: recommended medium-term default for High governance documentation
- strength: high
- requirement: should include Guardian Review Requirement, Guardian Review Result, WORM Assessment, Count Recommendation, Router Decision

### C. GitHub-Native Approving Review

- use: strongest platform-native signal
- strength: very high
- requirement: only mandatory if repository governance explicitly adopts GitHub-native approving review requirement
- caution: must not be self-approval by unauthorized executor

### D. Documentary Closing Note Referencing Guardian Review PASS

- use: supporting evidence and closure summary
- strength: medium-high
- limitation: should not alone replace original review evidence if Tier 1-3 evidence is absent

### E. Repository Policy File Defining Evidence Hierarchy

- use: governing standard
- strength: high
- requirement: itself requires Guardian Review before merge

## Evidence Hierarchy

### Tier 1: GitHub-Native Approving Review

- highest auditability
- required only if repository governance explicitly adopts it or if future high-critical workflow requires platform-native gate

### Tier 2: PR Comment Containing Guardian Review PASS

- recommended medium-term default for High governance documentation
- improves PR-linked preservation without requiring native approving review

### Tier 3: Codex PR Review Transcript + Post-Merge Validation Reference

- acceptable short-term baseline for current documentary governance track
- may need Tier 2 or Tier 1 upgrade if audit policy requires platform-native or PR-linked evidence

### Tier 4: Closure Note / Validation Note Referencing Guardian Review PASS

- supporting evidence
- should not alone replace Tier 1-3 original review evidence

## Policy Direction

- Short-term: accept Codex PR review transcript + post-merge validation reference as sufficient for current documentary governance track.
- Medium-term: require PR comment or closure / validation note reference for High governance documentation.
- Long-term: require GitHub-native approving review only if repository governance explicitly adopts that standard.
- Avoid retroactive mutation of prior PRs unless separately scoped.
- Future policy changes must not be treated as K / CEO / Sovereign substitute authority.

## No Retroactive Mutation Boundary

This evidence format policy note explicitly prohibits:

- modifying prior PR metadata
- creating retroactive GitHub-native review objects
- rewriting prior Guardian Review claims
- mutating formal approval evidence
- mutating audit evidence
- mutating WORM records
- treating policy note as retroactive approval authority
- treating Guardian Review as K / CEO / Sovereign substitute

## No-Authority Boundary

This evidence format policy note explicitly prohibits:

- Phase 5 entry
- activation
- routing/tool expansion
- production/runtime authority
- authority expansion
- safe-managed count increase beyond 53
- Sovereign index mutation
- formal approval evidence mutation
- audit evidence mutation
- WORM mutation
- K / CEO substitute authority
- Sovereign substitute authority

## Count Model

- policy note count increase: 0
- evidence format policy count increase: 0
- current safe-managed total remains: 53
- policy note does not authorize activation
- policy note does not authorize Phase 5

## Guardian / WORM Summary

- Guardian Review required for policy note PR: true
- Guardian Review required because this is High governance evidence policy documentation
- WORM Assessment: NOT REQUIRED
- WORM only required if future work mutates formal approval evidence, audit evidence, WORM records, lifecycle, Sovereign index, authority boundary, runtime, or production authority
- prior Guardian PASS is not K / CEO / Sovereign substitute

## Required Controls

allowed_actions:

- record_guardian_review_evidence_policy
- record_evidence_format_gap
- record_accepted_evidence_formats
- record_evidence_hierarchy
- preserve_no_retroactive_mutation_boundary
- preserve_no_authority_boundary
- record_count_model
- recommend_future_pr_linked_evidence

evidence_required:

- pr_81_post_merge_validation_reference
- guardian_review_gate_statement
- github_review_metadata_statement
- no_authority_boundary_statement
- future_scope_boundary_statement

forbidden_actions:

- mutate_prior_pr_reviews_during_policy_note
- create_github_native_review_without_scope
- mutate_formal_approval_evidence
- mutate_audit_evidence
- mutate_worm_records
- mutate_sovereign_index
- treat_guardian_review_as_k_ceo_substitute
- treat_guardian_review_as_sovereign_substitute
- activate_agent
- enter_phase_5
- expand_routing_authority
- expand_tool_permissions
- increase_safe_managed_count

## Risks / Blockers

- ambiguity between external Codex transcript and GitHub-native review object
- retroactive evidence mutation risk
- risk of treating Guardian Review as K / CEO substitute
- risk of overcomplicating workflow if Tier 1 is required prematurely
- risk of insufficient audit trail if evidence is not preserved in PR-linked form
- WORM contamination risk if immutable evidence is touched

## Router Decision

- PROCEED for documentary-only Guardian Review Evidence Format Policy Note
- HOLD for retroactive PR evidence mutation
- HOLD for GitHub-native review creation until policy exists or user explicitly scopes it
- HOLD for Phase 5
- HOLD for activation
- HOLD for routing/tool expansion
- HOLD for authority expansion
- HOLD for count increase beyond 53
