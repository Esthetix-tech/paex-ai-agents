# Guardian Review PR Comment Standard Note

## Positioning

This is a documentary-only PR comment standard note.

This note operationalizes Tier 2 evidence from the Guardian Review Evidence Format Policy Note.
This note does not create PR comments.
This note does not modify prior PR evidence.
This note does not create GitHub-native review objects.
This note does not mutate formal approval evidence.
This note does not mutate audit evidence.
This note does not mutate WORM records.
This note does not mutate the Sovereign index.
This note does not enter Phase 5.
This note does not activate agents.
This note does not authorize routing/tool expansion.
This note does not increase safe-managed count.
This note does not treat Guardian Review comments as K / CEO / Sovereign substitute.

## Policy Baseline

- Guardian Review Evidence Format Policy Note exists.
- Tier 1: GitHub-native approving review.
- Tier 2: PR comment containing Guardian Review PASS.
- Tier 3: Codex PR review transcript + post-merge validation reference.
- Tier 4: Closure note / validation note referencing Guardian Review PASS.
- Tier 3 remains acceptable short-term for completed documentary track.
- Tier 2 is recommended as medium-term default for new High governance documentation PRs.
- Tier 1 remains optional unless repository governance explicitly adopts it.

## Tier 2 Adoption Standard

- Tier 2 PR comment should be used for new High governance documentation PRs.
- Tier 2 PR comment is recommended before merge once Guardian Review gate is evaluated.
- Tier 2 PR comment supplements Codex transcript and post-merge validation reference.
- Tier 2 PR comment does not replace GitHub-native approving review if Tier 1 is explicitly required.
- Tier 2 PR comment is not K / CEO / Sovereign substitute authority.

## PR Categories Requiring Tier 2

Tier 2 PR comment evidence should be used for:

- High governance documentation PRs
- Guardian-adjacent documentation PRs
- Sovereign-boundary-adjacent documentation PRs
- registry / intake pipeline governance PRs
- evidence-format / review-format governance PRs
- Phase boundary / readiness / closure documentation PRs
- Any PR where Guardian Review gate is marked REQUIRED

## Minimum PR Comment Fields

Tier 2 Guardian Review PR comments should include:

- PR number / title
- base / compare branch
- head commit
- Risk Level
- Business Context Layer
- C-A-E-P Mapping
- Guardian Review Requirement
- Guardian Review Result
- WORM Assessment
- Files Accepted
- Files Need Repair
- Files Should Hold
- Files Should Quarantine
- Merge Recommendation
- Count Recommendation
- No-authority boundary
- Router Decision
- Reviewer identity / source, if available
- Timestamp, if available

## PR Comment Template Guidance

The following Markdown template is guidance only. It is not approval authority by itself, must reflect the actual PR review result, must not fabricate reviewer identity or timestamp, and must not be used to bypass Guardian Review.

```md
Guardian Review PR Comment

- PR number / title:
- base / compare branch:
- head commit:
- Risk Level:
- Business Context Layer:
- C-A-E-P Mapping:
- Guardian Review Requirement:
- Guardian Review Result:
- WORM Assessment:
- Files Accepted:
- Files Need Repair:
- Files Should Hold:
- Files Should Quarantine:
- Merge Recommendation:
- Count Recommendation:
- No-authority boundary:
- Router Decision:
- Reviewer identity / source, if available:
- Timestamp, if available:
```

## Relationship With Tier 1 / Tier 3 / Tier 4

- Tier 2 bridges Codex transcript and PR-linked evidence.
- Tier 2 does not replace Tier 1 if Tier 1 is required.
- Tier 3 remains acceptable for already completed documentary governance track.
- Tier 4 remains supporting evidence and should not alone replace Tier 1-3.

## No Retroactive Mutation Boundary

This PR comment standard note explicitly prohibits:

- adding comments to prior PRs without separate scope
- modifying prior PR metadata
- creating retrospective GitHub-native reviews
- rewriting prior Guardian Review claims
- mutating formal approval evidence
- mutating audit evidence
- mutating WORM records
- treating this standard as retroactive approval authority

## No-Authority Boundary

This PR comment standard note explicitly prohibits:

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
- treating PR comment as approval authority by itself

## Count Model

- PR comment standard note count increase: 0
- PR comment adoption count increase: 0
- current safe-managed total remains: 53
- PR comment standard does not authorize activation
- PR comment standard does not authorize Phase 5

## Guardian / WORM Summary

- Guardian Review required for standard note PR: true
- Guardian Review required because this is High governance PR comment standard documentation
- WORM Assessment: NOT REQUIRED
- WORM only required if future work mutates formal approval evidence, audit evidence, WORM records, lifecycle, Sovereign index, authority boundary, runtime, or production authority
- Guardian Review comment is not K / CEO / Sovereign substitute

## Required Controls

allowed_actions:

- record_guardian_review_pr_comment_standard
- operationalize_tier_2_evidence_format
- record_minimum_pr_comment_fields
- preserve_no_retroactive_mutation_boundary
- preserve_no_authority_boundary
- record_count_model
- recommend_future_pr_linked_evidence

evidence_required:

- guardian_review_evidence_format_policy_note_reference
- evidence_hierarchy_reference
- tier_2_pr_comment_standard_reference
- no_authority_boundary_statement
- future_scope_boundary_statement

forbidden_actions:

- mutate_prior_pr_reviews_during_standard_note
- create_pr_comments_during_standard_note
- create_github_native_review_without_scope
- mutate_formal_approval_evidence
- mutate_audit_evidence
- mutate_worm_records
- mutate_sovereign_index
- treat_guardian_review_comment_as_k_ceo_substitute
- treat_guardian_review_comment_as_sovereign_substitute
- activate_agent
- enter_phase_5
- expand_routing_authority
- expand_tool_permissions
- increase_safe_managed_count

## Risks / Blockers

- Tier 2 may overcomplicate workflow if over-applied.
- PR comment formatting may still vary if users ignore template.
- Retroactive evidence mutation risk remains.
- PR comment may be misread as approval authority.
- Guardian Review comment may be misread as K / CEO / Sovereign substitute.
- Auditability may remain weaker than Tier 1 if GitHub-native approving review is not adopted.
- WORM contamination risk if immutable evidence is touched.

## Router Decision

- PROCEED for documentary-only Guardian Review PR Comment Standard Note
- HOLD for retroactive PR evidence mutation
- HOLD for GitHub-native review creation until explicitly scoped
- HOLD for PR comment creation until separately scoped
- HOLD for Phase 5
- HOLD for activation
- HOLD for routing/tool expansion
- HOLD for authority expansion
- HOLD for count increase beyond 53
