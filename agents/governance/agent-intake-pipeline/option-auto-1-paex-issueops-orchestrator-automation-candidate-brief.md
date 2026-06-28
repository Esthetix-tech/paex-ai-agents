---
title: "Option AUTO-1｜PAEX IssueOps Orchestrator Automation Candidate Brief"
status: "candidate_brief"
mode: "documentary_only"
risk_level: "high"
business_context_layer: "Enterprise Governance / Repository Governance / Automation Governance"
caep_mapping: "G｜Governance"
worm_required: false
worm_required_scope: "future_automation_implementation_activation_workflow_creation_authority_or_production_use_only"
canonical: false
automation_implementation: false
automation_activation: false
workflow_created: false
github_actions_enabled: false
codex_automation_enabled: false
issueops_commands_enabled: false
pr_auto_merge_enabled: false
approval_authority: false
execution_authority: false
activation_authority: false
production_authority: false
created_from_baseline: "0b2985912ebb1e8c42b76b0ab5d8b7428da9a6f5"
safe_managed_total_expected: 53
physical_agents_md_count_before_expected: 145
physical_agents_md_count_after_expected_if_merged: 146
sovereign_index_expected: "routing_enabled: false"
---

# Option AUTO-1｜PAEX IssueOps Orchestrator Automation Candidate Brief

## 1. Document Status

This is a documentary-only, candidate-only automation governance brief. It is an automation governance design candidate only.

This brief is not workflow implementation, not GitHub Actions creation, not Codex automation activation, not IssueOps command activation, not PR auto-merge enablement, not formal approval evidence, not a WORM record, not production authority, and not final go/no-go.

This brief does not create, enable, implement, activate, approve, canonicalize, operationalize, or authorize any workflow, IssueOps command, Codex automation, GitHub App, token, secret, webhook, merge automation, formal approval evidence, WORM record, schema mutation, deployment, runtime automation, lifecycle state, production authority, or final decision. All substantive actions remain HOLD.

## 2. Current Manual Relay Problem

The current workflow is manual relay:

- 小艾 produces prompts and next-step governance directions.
- K manually copies prompts to Codex.
- Codex executes and returns results.
- K manually copies results back to 小艾.
- 小艾 reviews the results and creates next instructions.
- K manually posts to Codex or GitHub again.

The bottlenecks are:

- K becomes a manual API / relay between 小艾, Codex, GitHub PRs, and GitHub.
- The review-repair-merge cycle is slow.
- Context can be lost when material is copied across surfaces.
- Formatting errors can enter prompts, PR comments, or evidence blocks.
- Repeated prompt generation consumes human attention.
- Tier 2 PR-linked evidence and post-merge validation can be delayed.
- The manual relay pattern is difficult to scale.

## 3. Automation Goal

The desired future direction is that GitHub may become the task center and audit trail.

Candidate future flow:

K creates a GitHub issue or PR comment -> GitHub IssueOps command or label -> GitHub Actions validates authorization and scope -> Codex task is prepared or triggered only where separately authorized -> branch / PR / review / repair / Tier 2 / merge / post-merge validation may be orchestrated -> K remains the final authorization authority for high-risk gates.

This is candidate-only. It does not establish GitHub as the operational task center, does not create GitHub Actions workflows, does not activate IssueOps commands, and does not authorize automated Codex execution.

## 4. Candidate Architecture

Candidate components:

| Candidate Component | Candidate Role | Current Status |
|---|---|---|
| GitHub Issue | Task intake candidate. | HOLD / not implemented. |
| GitHub PR comment | Candidate command interface. | HOLD / not enabled. |
| Labels | Candidate state markers. | HOLD / not established. |
| GitHub Actions | Candidate orchestrator, guard, validator, and evidence poster. | HOLD / workflow not created. |
| Codex | Candidate repository task executor only when separately authorized. | HOLD / no automation activation. |
| 小艾 | Strategy, prompt, and governance logic designer candidate role. | HOLD / no runtime integration. |
| K | Authorization and risk decision authority. | Existing human authority; not automated. |
| PR timeline | Candidate audit trail input. | HOLD / not formal evidence by itself. |

This architecture is not adopted, not canonical, not active, and not operational.

## 5. Candidate IssueOps Commands

| Candidate Command | Candidate Purpose | Possible Trigger Location | Required Authorization Candidate | Allowed Output Candidate | Prohibited Action | Failure Mode | Current Status |
|---|---|---|---|---|---|---|---|
| `/paex audit` | Start read-only audit candidate. | Issue or PR comment. | K-scoped or low-risk declared scope. | Audit report or HOLD. | File mutation or approval. | HOLD if scope unclear. | HOLD / not implemented / not enabled. |
| `/paex prepare` | Prepare candidate plan or brief. | Issue comment. | Explicit documentary-only authorization. | Candidate brief draft/PR candidate. | Workflow creation or activation. | HOLD if protected scope unclear. | HOLD / not implemented / not enabled. |
| `/paex create` | Create authorized documentary artifact candidate. | Issue command. | Exact file path and scope authorization. | Branch/PR candidate. | Existing file mutation unless scoped. | HOLD if path mismatch. | HOLD / not implemented / not enabled. |
| `/paex review` | Run PR scope / wording / boundary review candidate. | PR comment. | PR number and expected commit. | Review comment/report candidate. | Merge or approval. | HOLD if head SHA mismatch. | HOLD / not implemented / not enabled. |
| `/paex repair` | Perform targeted repair candidate. | PR comment. | Exact file and repair scope. | Repair commit/PR update candidate. | Broad refactor. | HOLD if more than scoped file changes. | HOLD / not implemented / not enabled. |
| `/paex tier2` | Post Tier 2 PR-linked evidence candidate. | PR comment. | Passed review and no duplicate comment. | PR-linked evidence comment candidate. | Formal approval evidence. | HOLD if GitHub write fails. | HOLD / not implemented / not enabled. |
| `/paex merge` | Merge after K authorization candidate. | PR comment or issue. | Explicit K authorization and exact head SHA. | Merge plus validation candidate. | Auto-merge without K authorization. | HOLD if base/head mismatch. | HOLD / not implemented / not enabled. |
| `/paex postmerge` | Run post-merge validation candidate. | PR comment or workflow event. | Merged PR reference. | Validation report candidate. | New mutation or WORM record. | HOLD if validation fails. | HOLD / not implemented / not enabled. |
| `/paex status` | Summarize state candidate. | Issue or PR comment. | Read-only scope. | Status report. | Authority creation. | HOLD if repo state cannot be verified. | HOLD / not implemented / not enabled. |

No command listed above is executable, deployed, active, enabled, or authorized by this brief.

## 6. Candidate Workflow Names

| Candidate Workflow Name | Candidate Purpose | Possible Trigger | Required Guardrails | Prohibited Action | Current Status |
|---|---|---|---|---|---|
| `paex-orchestrator.yml` | Candidate top-level IssueOps router. | Issue comment / label. | Actor, scope, branch, protected-file, and authorization checks. | Self-authorization or production deployment. | HOLD / not created / not enabled. |
| `paex-pr-guard.yml` | Candidate PR protected-scope guard. | Pull request event. | Diff, count, Sovereign index, WORM schema, formal evidence checks. | Approving or merging PR. | HOLD / not created / not enabled. |
| `paex-tier2-comment.yml` | Candidate Tier 2 comment poster. | Manual dispatch or guarded PR comment. | Prior review PASS, exact head SHA, duplicate-comment check. | Formal approval evidence creation. | HOLD / not created / not enabled. |
| `paex-merge-gate.yml` | Candidate K-authorized merge gate. | Explicit K authorization command. | Exact head SHA lock, PR status, protected-scope checks. | Merge without K authorization. | HOLD / not created / not enabled. |
| `paex-postmerge-validation.yml` | Candidate post-merge validator. | PR merged event. | File, count, protected-scope, WORM, Sovereign, and branch checks. | Creating new authority or WORM record. | HOLD / not created / not enabled. |

No workflow file is created by this brief. No workflow exists, is active, or is enabled by this brief.

## 7. Automation Level Model

| Level | Description | Capability | Risk | Allowed Scope | Prohibited Scope | Current PAEX Status | Promotion Criteria |
|---|---|---|---|---|---|---|---|
| Level 0｜Manual Relay | K manually relays prompts/results. | Manual control and review. | Slow, error-prone, hard to scale. | Current manual operation. | Automated execution. | Current baseline. | Clear repeated pattern and candidate design. |
| Level 1｜Template-based Relay | Reusable prompt/report templates assist K. | Less formatting drift. | Still manual and context-fragile. | Documentary templates. | Workflow activation. | Partially present / moving toward Level 2 candidate design. | Stable templates and boundaries. |
| Level 2｜IssueOps Semi-automation | GitHub comments/labels may trigger guarded tasks. | Guarded orchestration candidate. | Unauthorized command and evidence confusion risk. | Low-risk or separately authorized tasks. | Auto-merge, WORM, production, schema, authority creation without K. | Not implemented. | Separate implementation plan, tests, and K authorization. |
| Level 3｜PAEX-Orchestrator Full-flow Automation | Multi-step PR/review/repair/merge orchestration candidate. | Higher automation with gates. | High governance and security risk. | Only after Level 2 stability. | Autonomous high-risk authority. | Not implemented. | Low-risk pilots pass and fail-closed controls mature. |
| Level 4｜Production-grade Autonomous Governance OS | Production-grade governed autonomy. | Operational automation. | Critical risk. | Future production-grade scope only. | Replacing K, Guardian, WORM, or legal authority. | Not implemented. | Formal production readiness, WORM, security, and K authorization. |

Current PAEX status is Level 0 / Level 1 moving toward Level 2 candidate design. Level 2 and Level 3 are not implemented.

## 8. Task Automation Classification Matrix

| Task Type | Candidate Automation Level | Requires K Authorization? | Requires WORM Assessment? | May Auto-run? | May Auto-merge? | Prohibited Interpretation | Current Router State |
|---|---|---|---|---|---|---|---|
| Read-only audit | Level 1-2 candidate. | Depends on scope; yes for High governance audit. | Usually no unless authority/evidence mutation. | Candidate-only after authorization. | No. | Audit is not approval. | HOLD for automation. |
| Documentary-only candidate brief | Level 1-2 candidate. | Yes when High governance. | Usually no for document itself. | Candidate-only after exact scope. | No. | Brief is not model establishment. | HOLD for automation. |
| Targeted repair | Level 2 candidate. | Yes, exact scope required. | Depends on touched scope. | Candidate-only after exact file authorization. | No. | Repair is not broad refactor. | HOLD for automation. |
| PR review | Level 2 candidate. | Yes for High governance. | Usually no unless evidence/authority mutation. | Candidate read-only. | No. | Review is not approval authority. | HOLD for automation. |
| Guardian Review summary | Level 2 candidate. | Yes. | Depends on risk and evidence path. | Candidate-only. | No. | Guardian summary is not final approval. | HOLD for automation. |
| Tier 2 PR-linked evidence comment | Level 2 candidate. | Yes and prior gates required. | Usually no for comment itself; future evidence path may require WORM. | Candidate-only when separately authorized. | No. | PR comment is not formal approval evidence. | HOLD for automation. |
| Post-merge validation | Level 2 candidate. | Yes if High governance PR. | Usually no unless authority/evidence mutation. | Candidate-only. | No. | Validation is not production authority. | HOLD for automation. |
| Merge after K authorization | Level 2-3 candidate. | Yes, exact head SHA required. | Depends on PR scope. | No autonomous high-risk merge. | Only after explicit K authorization candidate. | Merge is not go-live. | HOLD for automation. |
| Schema mutation | Level 2-3 candidate guard only. | Yes. | Yes where canonical schema/WORM touched. | No. | No. | Guard is not approval. | HOLD. |
| WORM record creation | Level 3+ future candidate. | Yes. | Yes. | No. | No. | Automation is not WORM authority. | HOLD. |
| Formal approval evidence creation | Level 3+ future candidate. | Yes. | Yes where applicable. | No. | No. | Comment is not formal evidence. | HOLD. |
| Sovereign routing enablement | Level 3+ future candidate guard only. | Yes. | Yes. | No. | No. | Routing enablement is not implied by labels. | HOLD. |
| Agent activation | Level 3+ future candidate guard only. | Yes. | Yes where High/Critical. | No. | No. | Safe-managed count is not activation. | HOLD. |
| Production deployment | Level 4 future candidate. | Yes. | Yes where production/authority. | No. | No. | Deployment is not authorized by this brief. | HOLD. |
| Final go/no-go | Level 4 future candidate evidence support only. | Yes, non-delegable. | Yes. | No. | No. | Automation cannot decide go/no-go. | HOLD. |

## 9. K Authorization Boundary

K remains the high-risk authorization authority. K authorization must be explicit, scope-bounded, and tied to repository evidence.

Future automation must verify K authorization in GitHub evidence. Merge authorization must be tied to an exact head SHA. Authorization must not be inferred from discussion, labels, branch names, comments by non-authorized actors, Codex output, or GitHub Actions output.

K authorization must not be created by Codex, GitHub Actions, IssueOps commands, labels, or PR comments that do not explicitly carry authorized K scope.

## 10. Codex Execution Boundary

Codex may be a candidate executor only when separately authorized. Codex cannot self-authorize, cannot create approval authority, cannot create production authority, and cannot treat prompt completion as implementation approval.

Codex cannot create WORM records unless separately authorized through a future WORM-required path. Codex cannot convert a candidate brief into a canonical convention or runtime automation.

## 11. GitHub Actions Boundary

GitHub Actions may be a future guard, validator, and commenter candidate. GitHub Actions must not create formal approval evidence, must not create WORM records, must not authorize production, must not enable Sovereign routing, and must not self-modify workflows unless separately scoped.

Workflow creation remains HOLD. This brief creates no workflow files and enables no GitHub Actions automation.

## 12. Tier 2 PR-linked Evidence Boundary

Tier 2 PR comment is PR-linked evidence only. It is not formal approval evidence, not approval authority, not production authority, and not K / CEO / Sovereign substitute authority.

Automation may later post Tier 2 PR-linked evidence only if separately authorized and all gates pass. That future action remains HOLD.

## 13. Guardian Review Boundary

Guardian Review is a review gate only. It is not approval authority, not final decision, not go/no-go, not formal approval evidence, and not production authority.

Future automation may assist with Guardian Review summaries only as separately authorized evidence support. It must not convert Guardian Review into automatic approval.

## 14. PR Merge Boundary

PR merge is repository integration only. It is not approval, not model establishment, not production authority, and not formal go-live.

Future merge automation must require explicit K authorization and exact head SHA match. Any mismatch must default to HOLD.

## 15. Count Model Boundary

If this PR is merged, physical `agents/**/*.md` count may increase from `145` to `146`.

`146` is documentary Markdown count only.

`146` is not:

- safe-managed count
- agent-like count
- activation denominator
- approval
- authorization
- workflow implementation
- automation activation
- WORM record
- formal evidence
- canonical convention
- model establishment
- lifecycle state
- production authority

The safe-managed total remains `53`.

`183` remains NOT OBSERVED unless directly verified from repository evidence.

## 16. WORM REQUIRED Boundary

Future actions remain WORM REQUIRED where applicable, including:

- automation implementation affecting formal evidence
- automation activation affecting governance execution
- workflow creation if controlling WORM / approval / production evidence
- formal approval evidence creation
- WORM record creation
- canonical schema mutation
- evidence validation model establishment
- production authority creation
- final go/no-go
- Sovereign / authority boundary mutation

This brief itself is documentary-only and WORM NOT REQUIRED.

## 17. Production Go-live Boundary

This brief does not create production deployment, runtime automation, operations readiness, final go/no-go, or production authority.

Future production use remains HOLD and requires separately scoped development, testing, security, deployment, evidence, WORM, authority, and K authorization gates.

## 18. Security / Abuse / Over-automation Risks

Candidate risks include:

- prompt injection via issue comments
- unauthorized command execution
- label spoofing
- actor identity ambiguity
- stale head SHA merge
- workflow self-modification
- secret leakage
- token misuse
- PR comment as false approval
- accidental protected scope modification
- Codex self-escalation
- auto-merge abuse
- evidence spoofing
- WORM boundary bypass

Candidate mitigations include actor allowlists, explicit K authorization checks, exact head SHA locks, protected-scope diff guards, fail-closed workflow behavior, no workflow self-modification, least-privilege tokens, duplicate evidence checks, WORM-required boundary checks, and human review gates.

These mitigations are candidate-only and are not implemented by this brief.

## 19. Failure Mode / HOLD Policy

Automation must fail closed.

Candidate failure rules:

- if authorization missing -> HOLD
- if head SHA mismatch -> HOLD
- if protected scope touched -> HOLD
- if count model mismatch -> HOLD
- if Sovereign index changed unexpectedly -> HOLD
- if WORM schema touched -> HOLD
- if formal evidence touched -> HOLD
- if workflow modified unexpectedly -> HOLD
- if GitHub write action fails -> HOLD
- if command actor cannot be verified -> HOLD

## 20. Candidate Roadmap

| Stage | Candidate Purpose | Current Status |
|---|---|---|
| AUTO-1 | Candidate brief. | This document only. |
| AUTO-2 | Read-only IssueOps command design brief. | HOLD pending separate authorization. |
| AUTO-3 | PR guard candidate implementation plan. | HOLD pending separate authorization. |
| AUTO-4 | Tier 2 comment automation candidate implementation plan. | HOLD pending separate authorization. |
| AUTO-5 | K-authorized merge gate candidate implementation plan. | HOLD pending separate authorization. |
| AUTO-6 | Level 2 MVP implementation, if separately authorized. | HOLD pending separate authorization. |
| AUTO-7 | Level 2 validation on 3-5 low-risk PRs. | HOLD pending separate authorization. |
| AUTO-8 | Level 3 candidate brief only after Level 2 stability. | HOLD pending separate authorization. |

All stages remain HOLD unless separately authorized.

## 21. Level 3 Promotion Criteria

Level 3 may be considered only when:

- AUTO-1 is merged and validated.
- Level 2 MVP is implemented and tested.
- PR guard automatically blocks protected scope violations.
- Count model check is automated.
- Safe-managed total check is automated.
- Sovereign index check is automated.
- Tier 2 comment automation is stable.
- K authorization is machine-verifiable via GitHub comment / label.
- Exact head SHA lock is verified.
- Post-merge validation is automated.
- Failure mode defaults to HOLD.
- 3-5 low-risk PRs pass without major governance boundary failure.

These criteria are not met by this brief.

## 22. Non-decisions

This brief makes no decision and creates no establishment or activation for:

- GitHub Actions workflow creation
- workflow file modification
- automation implementation
- automation activation
- Codex automation activation
- IssueOps command activation
- PR auto-merge
- Guardian automatic approval
- Tier 2 automatic approval
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
- backend implementation
- evidence validation model
- canonical convention
- schema mutation
- README.md / AGENTS.md modification
- registry modification
- agent file modification
- `pace-ai` to `PAEX-GOS` rename
- repo-wide text replacement

## 23. Rename Boundary

No `pace-ai` to `PAEX-GOS` rename is executed. No repo-wide text replacement is executed. Historical references are not silently rewritten.

Future rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 24. Router Decision

PROCEED only for documentary-only Option AUTO-1 automation candidate brief PR creation.

HOLD for GitHub Actions workflow creation, workflow file modification, automation implementation, automation activation, Codex automation activation, GitHub App installation, GitHub token creation, secret creation, API key creation, webhook creation, IssueOps command activation, PR auto-merge enablement, automatic Codex execution authorization, automatic Guardian approval, automatic Tier 2 approval, formal approval evidence creation, WORM record creation, production deployment, runtime automation enablement, agent activation, safe-managed production use, Sovereign routing enablement, execution authorization, activation authorization, risk acceptance, lifecycle state, production authority, final go/no-go, backend implementation, evidence validation model establishment, canonical convention establishment, schema mutation, README.md / AGENTS.md modification, registry modification, agent file modification, `pace-ai` to `PAEX-GOS` rename, and repo-wide text replacement.
