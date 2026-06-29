---
title: "AUTO-8｜Head SHA Lock Format Candidate Brief"
status: "candidate_brief"
mode: "documentary_only"
risk_level: "high"
business_context_layer: "Enterprise Governance / Repository Governance / Automation Governance / Head SHA Lock Review"
caep_mapping: "G｜Governance"
worm_required: false
worm_required_scope: "future_canonical_head_sha_lock_model_head_sha_verifier_git_verifier_pr_guard_implementation_workflow_creation_validation_script_automation_activation_authority_or_production_use_only"
canonical: false
head_sha_lock_format_canonical: false
head_sha_verifier_created: false
git_verifier_created: false
git_commit_verification_model_created: false
machine_verifiable_head_sha_lock_model_created: false
cryptographic_verification_model_created: false
actor_verification_model_created: false
identity_model_created: false
signature_model_created: false
authentication_model_created: false
formal_approval_evidence_created: false
worm_record_created: false
machine_readable_head_sha_lock_file_created: false
machine_readable_enforcement_file_created: false
runtime_config_created: false
pr_guard_input_file_created: false
pr_guard_implemented: false
pr_guard_enabled: false
pr_guard_executable: false
pr_guard_checks_enabled: false
pr_guard_script_created: false
validation_script_created: false
validation_logic_executable: false
workflow_created: false
github_actions_enabled: false
issueops_commands_enabled: false
command_parser_implemented: false
automation_implementation: false
automation_activation: false
codex_automation_enabled: false
pr_auto_merge_enabled: false
approval_authority: false
execution_authority: false
activation_authority: false
production_authority: false
level_2_implemented: false
level_3_ready: false
k_authorization_replaced: false
created_from_baseline: "16c52446f00ff03241d2d35686dd87a351f5513a"
auto_1_reference: "agents/governance/agent-intake-pipeline/option-auto-1-paex-issueops-orchestrator-automation-candidate-brief.md"
auto_2_reference: "agents/governance/agent-intake-pipeline/auto-2-read-only-issueops-command-design-candidate-brief.md"
auto_3_reference: "agents/governance/agent-intake-pipeline/auto-3-pr-guard-candidate-implementation-plan-validation-design-brief.md"
auto_5_reference: "agents/governance/agent-intake-pipeline/auto-5-protected-scope-path-inventory-candidate-brief.md"
auto_6_reference: "agents/governance/agent-intake-pipeline/auto-6-forbidden-wording-dictionary-candidate-brief.md"
auto_7_reference: "agents/governance/agent-intake-pipeline/auto-7-k-authorization-evidence-format-candidate-brief.md"
safe_managed_total_expected: 53
physical_agents_md_count_before_expected: 151
physical_agents_md_count_after_expected_if_merged: 152
sovereign_index_expected: "routing_enabled: false"
---

# AUTO-8｜Head SHA Lock Format Candidate Brief

## 1. Document Status

This document is documentary-only.

This document is candidate-only.

This document is a head SHA lock format candidate brief only.

This document is not a canonical head SHA lock model.

This document is not a head SHA verifier.

This document is not a Git verifier.

This document is not a Git commit verification model.

This document is not a cryptographic proof model.

This document is not an actor verification model.

This document is not an identity model.

This document is not a signature model.

This document is not an authentication model.

This document is not formal approval evidence.

This document is not a WORM record.

This document is not a machine-readable head SHA lock file.

This document is not runtime config.

This document is not a PR Guard input file.

This document is not PR Guard implementation.

This document is not PR Guard activation.

This document is not PR Guard check enablement.

This document is not validation script creation.

This document is not GitHub Actions workflow creation.

This document is not automation implementation.

This document is not automation activation.

This document is not IssueOps command activation.

This document is not command parser implementation.

This document is not Codex automation activation.

This document is not PR auto-merge enablement.

This document is not production authority.

This document is not Level 2 implementation.

This document is not Level 3 readiness.

This document is not final go/no-go.

## 2. AUTO-1 / AUTO-2 / AUTO-3 / AUTO-4 / AUTO-5 / AUTO-6 / AUTO-7 Baseline

AUTO-1 established candidate IssueOps Orchestrator architecture.

AUTO-2 defined future `/paex` command semantics.

AUTO-3 designed the future PR Guard check matrix.

AUTO-4 returned PARTIAL READY / BLOCKED because machine-ready prerequisites remained incomplete.

AUTO-5 created candidate protected scope path inventory.

AUTO-6 created candidate forbidden wording dictionary.

AUTO-7 created candidate K authorization evidence format.

AUTO-5 helps answer "where a change occurred."

AUTO-6 helps answer "whether wording may imply unauthorized governance state."

AUTO-7 helps answer "whether K authorization evidence is sufficiently scoped and reviewable."

AUTO-8 helps answer "whether the authorized, reviewed, Tier 2 evidenced, and merged PR head commit is the same reviewed commit."

AUTO-8 does not implement PR Guard.

AUTO-8 does not create canonical head SHA lock model.

AUTO-8 does not create head SHA verifier.

AUTO-8 does not create WORM record.

AUTO-8 does not modify AUTO-1 / AUTO-2 / AUTO-3 / AUTO-5 / AUTO-6 / AUTO-7 artifacts.

Current baseline:

- latest main expected: `16c52446f00ff03241d2d35686dd87a351f5513a`
- physical `agents/**/*.md` before AUTO-8: `151`
- expected after merge if accepted: `152`
- safe-managed total: `53`
- Sovereign index: `routing_enabled: false`
- `183`: NOT OBSERVED unless directly verified

## 3. Why Head SHA Lock Format Is Needed

Future review must avoid reviewing one commit and merging another.

K authorization should identify the expected PR head commit when merge or targeted action depends on a reviewed PR state.

Guardian Review, Tier 2 evidence, and merge authorization should ideally refer to the same PR head commit.

A PR can receive new commits after review, after Tier 2 comment, or after K merge authorization.

Head mismatch can create wrong-head risk.

New commits after authorization can create stale-head risk.

Force-push can create review continuity risk.

Base main can move without the PR head changing, creating base drift review risk.

Merge commit is not the same as PR head commit.

Post-merge validation should confirm merged history includes the authorized PR head commit.

AUTO-8 remains candidate-only until separately reviewed and canonicalized if ever authorized.

## 4. Head SHA Lock Format Purpose

The purpose of AUTO-8 is to collect candidate head SHA lock fields.

It defines authorized PR head binding candidate.

It defines reviewed head commit candidate.

It defines Tier 2 evidence head commit candidate.

It defines K merge authorization expected head commit candidate.

It defines current PR head at merge time candidate.

It defines base main commit reference candidate.

It defines merge commit interpretation candidate.

It defines stale-head and wrong-head risk categories.

It defines force-push risk category.

It defines base drift risk category.

It defines post-merge validation candidate.

It defines head-in-merged-history check candidate.

It supports future reviewer discipline.

It supports future PR Guard head SHA review design only as a later step.

This document is not canonical.

This document is not approved.

This document is not machine-verifiable.

This document is not executable.

This document is not runtime config.

This document is not a PR Guard input file.

This document is not final head SHA lock model.

## 5. Minimum Candidate Head SHA Lock Fields

| Field | Candidate Requirement | Purpose | Example Candidate Wording | Missing Field Risk | False Positive Risk | False Negative Risk | Reviewer Interpretation | Current Router State |
|---|---|---|---|---|---|---|---|---|
| target PR number | Identify the PR being reviewed | Prevent wrong-PR action | `Target PR: #128` | Authorization may bind to wrong PR | Harmless PR reference blocked | Wrong PR merged | Compare requested PR and current PR | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| target branch | Identify the PR branch | Prevent wrong branch action | `Target branch: intake/example` | Branch ambiguity | Branch discussion blocked | Wrong branch head accepted | Compare branch name to PR metadata | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| base main commit | Record reviewed base context | Track base drift | `Expected base main commit: abc123...` | Base drift invisible | Base drift over-blocked | Risk-sensitive drift missed | Distinguish base drift from head drift | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| reviewed head commit | Record review target | Bind review to commit | `Reviewed head commit: abc123...` | Review target unclear | Example SHA treated as target | Different commit accepted | Check review evidence context | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| authorized head commit | Record authorized target | Bind K authorization to commit | `Authorized head commit: abc123...` | Authorization target unclear | Commit mention treated as authorization | Head change missed | K authorization remains separate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| Tier 2 evidence head commit | Record Tier 2 target | Bind PR-linked evidence to commit | `Target head commit: abc123...` | Evidence target unclear | Evidence comment over-trusted | Evidence for different head accepted | Tier 2 is review evidence only | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| merge authorization expected head commit | Record merge-specific expected head | Prevent stale merge | `Expected head commit: abc123...` | Merge may use stale authorization | Missing optional wording over-blocked | New head merged without review | Compare K merge instruction to PR head | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| current PR head at merge time | Observe current PR head | Detect head drift before merge | `Current PR head: abc123...` | Latest head not checked | Network metadata issue blocks review | New commit accepted | Compare immediately before merge | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| merge commit | Record integration commit | Distinguish merge commit from PR head | `Merge commit: def456...` | Merge commit confused with head | Normal merge commit treated as failure | Wrong merge history missed | Merge commit may differ from PR head | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| merged history includes authorized head commit | Confirm reviewed commit entered main | Prevent wrong-head integration | `merged history includes abc123...` | Head-in-history not checked | Normal history shape over-blocked | Authorized head absent from main | Check history conceptually or with later tooling | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| stale-head risk | Identify new commits after evidence | Trigger re-check candidate | `new commit after review requires HOLD` | Stale authorization accepted | New harmless commit blocked | Material change missed | Compare evidence time and head commit | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| wrong-head risk | Identify mismatch among reviewed, evidenced, authorized, current heads | Prevent wrong commit merge | `head mismatch requires HOLD` | Mismatch not flagged | Typo treated as mismatch | Wrong commit accepted | Resolve exact commit values | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| force-push risk | Identify history rewrite risk | Preserve review continuity | `force-push after review requires re-review candidate` | Continuity risk missed | Force-push mention over-blocked | Rewritten code accepted | Check PR event context where available | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| base drift risk | Identify base movement without head change | Preserve context review | `base changed; assess risk-sensitive context` | Base drift ignored | Any base movement blocked | Context-sensitive risk missed | Distinguish base drift from head drift | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| re-review trigger candidate | Define when review should repeat | Avoid stale review | `head mismatch triggers re-review candidate` | Review not repeated | Minor metadata triggers review | Material change missed | Human reviewer decides | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| re-authorization trigger candidate | Define when K authorization should repeat | Avoid stale authorization | `new head requires new K authorization candidate` | Authorization reused wrongly | Harmless new evidence over-blocked | New code merged under old authorization | K remains human decision owner | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| permitted action | Define allowed action | Prevent scope upgrade | `merge PR #128 only` | Action boundary unclear | Narrow action blocked | Implementation hidden in merge | Check requested action text | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| prohibited actions | Define actions remaining HOLD | Preserve non-authority boundary | `do not create workflow` | Scope creep | Boundary language over-blocked | Prohibited action missed | Compare diff to prohibitions | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| documentary-only / candidate-only boundary | Preserve artifact class | Prevent authority creation | `documentary-only / candidate-only` | Document treated as authority | Candidate doc blocked as implementation | Authority wording missed | Review wording context | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| protected scope boundary | Preserve forbidden path boundaries | Prevent protected mutations | `no protected scope modified` | Protected mutation missed | Reference blocked as mutation | Hidden protected file touched | Compare changed files and evidence | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| post-merge validation requirements | Define post-action checks | Ensure integration evidence | `verify main count and head-in-history` | Completion without verification | Excessive check blocks docs | Post-merge issue missed | Match checks to authorized action | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| reviewer interpretation note | Preserve human judgment | Avoid automatic hash equals authorization logic | `hash match is evidence, not authorization` | Reviewer over-trusts metadata | Manual interpretation over-blocked | Authorization replacement missed | Read context and K authorization separately | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| current router state | State HOLD status for implementation | Prevent runtime use | `HOLD FOR IMPLEMENTATION` | Candidate fields treated as runtime | Candidate table blocked as config | Runtime use implied | Keep as documentary-only | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |

## 6. Head SHA Lock Pattern Categories

| Pattern Category | Candidate Description | Example Candidate Pattern | Risk | Review Concern | Candidate Router Action | Current Router State |
|---|---|---|---|---|---|---|
| clear authorized head match | Reviewed, Tier 2, K authorization, and current PR head match | all references use `abc123...` | Lower wrong-head risk | Still not K replacement | PROCEED candidate for scoped action review | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| clear head mismatch | Current PR head differs from reviewed head | review `abc123...`, current `def456...` | Wrong-head merge | Re-review likely needed | HOLD candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| stale head after new commit | PR receives new commit after review or K authorization | authorized `abc123...`, new head `def456...` | Stale authorization | New commit may be unreviewed | HOLD / re-review candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| force-push after review | PR branch is rewritten after evidence | old head disappears | Review continuity risk | Diff may not match evidence | HOLD / re-review candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| base main drift without head change | main advances while PR head stays same | base `aaa...` to `bbb...` | Context drift | May or may not affect risk | REVIEW candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| merge commit differs from PR head but history includes authorized head | Standard merge commit creates new commit | merge `def...`, head `abc...`, history includes `abc...` | Misread normal merge | Merge commit difference is normal | PROCEED candidate if other checks pass | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| merge commit exists but authorized head not found in merged history | Merge result lacks authorized head | merge `def...`, no `abc...` ancestor | Wrong integration | History mismatch | HOLD candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| Guardian Review head differs from Tier 2 evidence head | Review and evidence target different commits | review `abc...`, Tier 2 `def...` | Evidence mismatch | Which commit was validated | HOLD / reconcile candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| Tier 2 evidence head differs from K merge authorization head | Evidence and K target differ | Tier 2 `abc...`, K `def...` | Stale or wrong evidence | Merge may exceed evidence | HOLD candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| K merge authorization missing expected head commit | K instruction lacks head SHA | PR number only | Ambiguous scope | May be acceptable only with explicit human clarification | HOLD / clarification candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| K merge authorization references wrong PR head | K target does not match PR metadata | K `abc...`, PR current `def...` | Wrong-head action | Must not silently upgrade | HOLD candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| post-merge validation missing head-in-history check | Merge done without ancestry check | no head-in-history evidence | Wrong integration may pass | Completion evidence incomplete | HOLD / follow-up validation candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| ambiguous commit reference | SHA wording unclear or partial | `abc` | Ambiguity | May match multiple commits | HOLD / require full SHA candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| abbreviated SHA ambiguity | Short SHA used where full lock needed | `abc1234` | Collision or confusion | Human may over-trust abbreviation | HOLD / expand candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| wrong branch head reference | Branch name does not match PR branch | target branch differs | Wrong branch | PR metadata conflict | HOLD candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |
| wrong PR reference | PR number does not match action target | review PR #128, merge PR #129 | Wrong PR action | Evidence mismatch | HOLD candidate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-VERIFIABLE / HOLD FOR IMPLEMENTATION |

## 7. PR Head Commit vs Merge Commit

PR head commit is the reviewed commit at the tip of the PR branch.

Merge commit is created when PR is merged by standard merge commit.

Merge commit may differ from PR head commit.

This difference is normal under merge-commit strategy.

The key post-merge question is whether merged history includes the authorized PR head commit.

This is candidate reviewer guidance only and not executable validation logic.

## 8. Authorized Head vs Reviewed Head vs Tier 2 Head

Reviewed head commit is the commit examined during read-only or Guardian review.

Guardian Review head commit is the commit referenced by the Guardian review gate.

Tier 2 evidence head commit is the commit referenced by the PR-linked Tier 2 evidence comment.

K authorization expected head commit is the commit K explicitly identifies for a merge or targeted action when head binding is required.

Current PR head at merge time is the live PR branch tip immediately before merge.

These should ideally align for merge authorization.

Mismatch should be treated as a HOLD candidate condition or re-review / re-authorization candidate trigger.

This brief does not create automatic enforcement.

## 9. Base Main Commit / Base Drift Candidate

Base main commit is useful context but not identical to PR head commit.

Base main may change while PR head remains unchanged.

Base drift does not automatically invalidate authorization, but may create reviewer interpretation risk.

Base drift may require re-check if risk-sensitive context changed.

This is candidate guidance only and not machine-enforced.

## 10. Stale Head / Wrong Head / Force-push Risks

Stale head risk occurs when a new commit is added after review, Tier 2 evidence, or K authorization.

Wrong head risk occurs when reviewed head, evidenced head, authorized head, and current PR head do not match.

Force-push after review can rewrite the review continuity trail.

Ambiguous or abbreviated commit reference can make a head lock unclear.

Missing expected head commit in K authorization can make the authorized scope ambiguous.

Missing head-in-history check after merge can hide whether the authorized head reached main.

These are review risks, not executable checks.

## 11. Post-merge Validation Candidate

Candidate post-merge validation should check latest main commit.

Candidate post-merge validation should check merge commit hash.

Candidate post-merge validation should check PR head commit included in merged history.

Candidate post-merge validation should check authorized head commit included in merged history.

Candidate post-merge validation should check only expected files changed.

Candidate post-merge validation should check no protected scope modified.

Candidate post-merge validation should check no WORM / formal evidence / production / authority boundary created.

Candidate post-merge validation should check physical count model remains accurate.

Candidate post-merge validation should check safe-managed total remains unchanged.

Candidate post-merge validation should check Sovereign routing remains false.

Candidate post-merge validation should check `183` remains NOT OBSERVED unless directly verified.

Candidate post-merge validation should check rename boundary remains clean.

No script or workflow is created by this brief.

## 12. K Authorization Boundary

K authorization remains human and separate.

Head SHA lock format cannot create K authorization.

Head SHA lock format cannot replace K authorization.

Commit hash alone cannot replace K authorization.

PR metadata cannot replace K authorization.

Labels alone cannot replace K authorization.

PR body cannot replace K authorization.

Guardian Review cannot replace K authorization.

Tier 2 comment cannot replace K authorization.

Codex output cannot replace K authorization.

Automation cannot replace K authorization.

Path inventory cannot replace K authorization.

Forbidden wording dictionary cannot replace K authorization.

Authorization evidence format cannot replace K authorization.

## 13. Guardian Review / Tier 2 Boundary

Guardian Review is a review gate only.

Guardian Review does not create K authorization.

Tier 2 PR-linked evidence is PR-linked evidence only.

Tier 2 PR-linked evidence is not formal approval evidence.

Tier 2 PR-linked evidence does not create merge authorization.

Tier 2 PR-linked evidence does not create WORM record.

Tier 2 PR-linked evidence does not create production authority.

Tier 2 PR-linked evidence does not replace K authorization.

Tier 2 evidence head commit may be used as candidate review context only.

## 14. Machine-verification Boundary

AUTO-8 does not create head SHA verifier.

AUTO-8 does not create Git verifier.

AUTO-8 does not create Git commit verification model.

AUTO-8 does not create machine-verifiable head SHA lock model.

AUTO-8 does not create cryptographic proof model.

AUTO-8 does not create actor verification model.

AUTO-8 does not create identity model.

AUTO-8 does not create signature model.

AUTO-8 does not create authentication model.

AUTO-8 does not create machine-readable head SHA registry.

AUTO-8 does not create machine-readable enforcement file.

Future machine-checking head SHA lock remains HOLD and WORM REQUIRED where applicable.

## 15. Formal Approval Evidence / WORM Boundary

AUTO-8 is documentary-only and WORM NOT REQUIRED.

AUTO-8 does not create formal approval evidence.

AUTO-8 does not create WORM record.

Future formal approval evidence creation remains HOLD and WORM REQUIRED where applicable.

Future WORM record creation remains HOLD and WORM REQUIRED where applicable.

Future evidence validation model remains HOLD and WORM REQUIRED where applicable.

Future canonical head SHA lock model remains HOLD and WORM REQUIRED where applicable.

## 16. Implementation / Activation / Production Boundary

AUTO-8 does not implement PR Guard.

AUTO-8 does not create scripts.

AUTO-8 does not create validation logic.

AUTO-8 does not create workflow.

AUTO-8 does not activate automation.

AUTO-8 does not activate IssueOps.

AUTO-8 does not implement command parser.

AUTO-8 does not enable Codex automation.

AUTO-8 does not enable PR auto-merge.

AUTO-8 does not create production deployment.

AUTO-8 does not create runtime automation.

AUTO-8 does not create production authority.

AUTO-8 does not create final go/no-go.

## 17. Level 2 / Level 3 Boundary

AUTO-8 supports future PR Guard / Level 2 preparation only.

AUTO-8 does not implement Level 2.

AUTO-8 does not activate IssueOps.

AUTO-8 does not qualify the system for Level 3.

Level 3 remains HOLD until Level 2 MVP is separately authorized, implemented, tested, and passes 3-5 low-risk PR validation cycles.

## 18. Count Model

If this PR is merged, physical `agents/**/*.md` count may increase from `151` to `152`.

`152` is documentary Markdown count only.

152 is documentary Markdown count only.

`152` is not:

- safe-managed count
- agent-like count
- activation denominator
- approval
- authorization
- formal approval evidence
- WORM record
- head SHA verifier
- Git commit verification model
- cryptographic proof model
- identity model
- signature model
- actor verification model
- PR Guard implementation
- validation implementation
- workflow implementation
- automation activation
- canonical convention
- model establishment
- lifecycle state
- production authority
- canonical path registry
- canonical wording dictionary
- canonical authorization evidence model
- canonical head SHA lock model

safe-managed total remains `53`.

safe-managed total remains 53.

`183` remains NOT OBSERVED unless directly verified from repository evidence.

183 remains NOT OBSERVED unless directly verified from repository evidence.

## 19. Rename / Repo-wide Replacement Boundary

No `pace-ai` to `PAEX-GOS` rename is executed.

No repo-wide text replacement is executed.

Historical references are not silently rewritten.

Future rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 20. False Positive / False Negative Risks

False positive risks include treating normal merge commit difference as wrong-head failure.

False positive risks include rejecting a valid merge because merge commit differs from PR head.

False positive risks include rejecting a PR because base main changed even though PR head stayed the same.

False positive risks include treating an example SHA as an actual authorization target.

False positive risks include treating a candidate head SHA rule as canonical enforcement.

False negative risks include accepting a PR after new commits were pushed post-review.

False negative risks include accepting stale K authorization after head changed.

False negative risks include accepting Tier 2 evidence for a different head.

False negative risks include accepting abbreviated SHA ambiguity.

False negative risks include failing to check that merged history includes authorized head.

False negative risks include accepting wrong branch head reference.

False negative risks include accepting wrong PR reference.

## 21. Future Reviewer Interpretation Rules

Candidate reviewer rules include verifying target PR number.

Candidate reviewer rules include verifying target branch.

Candidate reviewer rules include verifying reviewed head commit.

Candidate reviewer rules include verifying Tier 2 evidence head commit.

Candidate reviewer rules include verifying K merge authorization expected head commit.

Candidate reviewer rules include verifying current PR head at merge time.

Candidate reviewer rules include verifying whether new commits were pushed after review / Tier 2 / K authorization.

Candidate reviewer rules include verifying whether force-push changed review continuity.

Candidate reviewer rules include distinguishing PR head commit from merge commit.

Candidate reviewer rules include verifying merged history includes authorized PR head commit after merge.

Candidate reviewer rules include distinguishing base drift from head drift.

Candidate reviewer rules include distinguishing candidate guidance from machine enforcement.

Candidate reviewer rules include distinguishing K authorization from Guardian Review.

Candidate reviewer rules include distinguishing K authorization from Tier 2 PR-linked evidence.

Candidate reviewer rules include distinguishing K authorization from Codex output.

Candidate reviewer rules include distinguishing K authorization from automation output.

These rules are candidate-only and not machine-enforced.

## 22. Future PR Guard Usage Candidate

This brief could inform a future PR Guard design by describing head SHA lock fields as review inputs.

Future PR Guard may use head SHA lock fields as review inputs only after separate authorization.

This brief does not create any executable head SHA check.

This brief does not create a machine-readable head SHA schema.

This brief does not create a runtime config.

This brief does not create a PR Guard input file.

Future implementation remains HOLD.

## 23. WORM REQUIRED Future Action Boundary

Future canonical head SHA lock model establishment remains WORM REQUIRED where applicable.

Future head SHA verifier establishment remains WORM REQUIRED where applicable.

Future Git verifier establishment remains WORM REQUIRED where applicable.

Future machine-verifiable head SHA lock model establishment remains WORM REQUIRED where applicable.

Future Git commit verification model establishment remains WORM REQUIRED where applicable.

Future cryptographic proof model establishment remains WORM REQUIRED where applicable.

Future actor verification model establishment remains WORM REQUIRED where applicable.

Future identity / signature / authentication model establishment remains WORM REQUIRED where applicable.

Future evidence validation model establishment remains WORM REQUIRED where applicable.

Future PR Guard implementation affecting head SHA review remains WORM REQUIRED where applicable.

Future validation script creation controlling head SHA evidence workflows remains WORM REQUIRED where applicable.

Future workflow creation affecting authorization / approval / WORM evidence remains WORM REQUIRED where applicable.

Future command parser implementation controlling authorization-bearing issue comments remains WORM REQUIRED where applicable.

Future automation activation remains WORM REQUIRED where applicable.

Future formal approval evidence creation remains WORM REQUIRED where applicable.

Future WORM record creation remains WORM REQUIRED where applicable.

Future production authority creation remains WORM REQUIRED where applicable.

Future final go/no-go remains WORM REQUIRED where applicable.

Future Sovereign / authority boundary mutation remains WORM REQUIRED where applicable.

This brief itself is documentary-only and WORM NOT REQUIRED.

## 24. Non-decisions

No decision, establishment, or activation is made for:

- canonical head SHA lock model
- head SHA verifier
- Git verifier
- Git commit verification model
- machine-verifiable head SHA lock model
- cryptographic proof model
- actor verification model
- identity model
- signature model
- authentication model
- machine-readable head SHA registry
- machine-readable enforcement file
- runtime config
- PR Guard input file
- PR Guard implementation
- PR Guard activation
- PR Guard check enablement
- guard script creation
- validation script creation
- executable validation logic
- GitHub Actions workflow creation
- workflow file modification
- automation implementation
- automation activation
- IssueOps command activation
- command parser implementation
- Codex automation activation
- PR auto-merge
- automatic Guardian approval
- automatic Tier 2 approval
- formal approval evidence
- WORM record
- production deployment
- runtime automation
- agent activation
- safe-managed production use
- Sovereign routing
- execution authorization
- activation authorization
- risk acceptance
- lifecycle state
- production authority
- final go/no-go
- Level 2 implementation
- Level 3 readiness
- backend implementation
- evidence validation model
- canonical convention
- schema mutation
- README.md / AGENTS.md modification
- registry modification
- agent file modification
- existing AUTO-1 modification
- existing AUTO-2 modification
- existing AUTO-3 modification
- existing AUTO-5 modification
- existing AUTO-6 modification
- existing AUTO-7 modification
- `pace-ai` to `PAEX-GOS` rename
- repo-wide text replacement

## 25. Router Decision

PROCEED only for documentary-only AUTO-8 Head SHA Lock Format Candidate Brief PR creation.

HOLD for canonical head SHA lock model, head SHA verifier, Git verifier, Git commit verification model, machine-verifiable head SHA lock model, cryptographic proof model, actor verification model, identity model, signature model, authentication model, machine-readable head SHA file, machine-readable enforcement file, runtime config, PR Guard input file, PR Guard implementation, PR Guard activation, PR Guard check enablement, guard script creation, validation script creation, executable validation logic, GitHub Actions workflow creation, workflow file modification, automation implementation, automation activation, IssueOps command activation, command parser implementation, Codex automation activation, GitHub App installation, GitHub token creation, secret creation, API key creation, webhook creation, PR auto-merge enablement, automatic Codex execution authorization, automatic Guardian approval, automatic Tier 2 approval, formal approval evidence creation, WORM record creation, production deployment, runtime automation enablement, agent activation, safe-managed production use, Sovereign routing enablement, execution authorization, activation authorization, risk acceptance, lifecycle state, production authority, final go/no-go, Level 2 implementation, Level 3 readiness, backend implementation, evidence validation model establishment, canonical convention establishment, schema mutation, README.md / AGENTS.md modification, registry modification, agent file modification, existing AUTO-1 artifact modification, existing AUTO-2 artifact modification, existing AUTO-3 artifact modification, existing AUTO-5 artifact modification, existing AUTO-6 artifact modification, existing AUTO-7 artifact modification, `pace-ai` to `PAEX-GOS` rename, and repo-wide text replacement.

## 26. Head SHA Discovery Rules

When identifying candidate head SHA lock patterns, use repository governance context only.

Do not claim the format is complete.

Do not claim the format is canonical.

Do not treat candidate fields as machine-verifiable.

Do not create machine-readable head SHA lock files.

Do not create JSON / YAML / config / schema output.

Mark examples as examples only.

Include valid, invalid, stale, ambiguous, force-push, base drift, and post-merge candidate patterns.

Emphasize human reviewer interpretation.

Avoid automatic "commit hash exists equals merge allowed" logic.

Preserve K authorization as separate and non-replaceable.

Preserve Guardian Review and Tier 2 PR-linked evidence as non-authorization review gates.
