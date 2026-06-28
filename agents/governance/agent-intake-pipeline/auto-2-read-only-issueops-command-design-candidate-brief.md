---
title: "AUTO-2｜Read-only IssueOps Command Design Candidate Brief"
status: "candidate_brief"
mode: "documentary_only"
risk_level: "high"
business_context_layer: "Enterprise Governance / Repository Governance / Automation Governance / IssueOps Command Governance"
caep_mapping: "G｜Governance"
worm_required: false
worm_required_scope: "future_command_activation_parser_implementation_workflow_creation_automation_activation_authority_or_production_use_only"
canonical: false
issueops_commands_implemented: false
issueops_commands_enabled: false
issueops_commands_executable: false
command_parser_implemented: false
automation_implementation: false
automation_activation: false
workflow_created: false
github_actions_enabled: false
codex_automation_enabled: false
pr_auto_merge_enabled: false
approval_authority: false
execution_authority: false
activation_authority: false
production_authority: false
created_from_baseline: "2f846ccd6de80881316018776dcced6ae24cf539"
auto_1_reference: "agents/governance/agent-intake-pipeline/option-auto-1-paex-issueops-orchestrator-automation-candidate-brief.md"
safe_managed_total_expected: 53
physical_agents_md_count_before_expected: 146
physical_agents_md_count_after_expected_if_merged: 147
sovereign_index_expected: "routing_enabled: false"
---

# AUTO-2｜Read-only IssueOps Command Design Candidate Brief

## 1. Document Status

This document is documentary-only, candidate-only, and a command design brief only.

This document is not IssueOps command activation, not command parser implementation, not GitHub Actions workflow creation, not automation implementation, not automation activation, not Codex automation activation, not PR auto-merge enablement, not formal approval evidence, not a WORM record, not production authority, and not final go/no-go.

All command activation, parser implementation, workflow creation, automation activation, authority, production, formal approval evidence, WORM, and go-live actions remain HOLD.

## 2. AUTO-1 Baseline and AUTO-2 Scope

AUTO-1 established a candidate governance architecture for IssueOps Orchestrator design. AUTO-1 did not implement workflows, did not implement commands, did not activate IssueOps, and did not enable automation.

AUTO-2 narrows the next design layer to future `/paex` command semantics. AUTO-2 still does not implement, enable, deploy, or activate `/paex` commands. AUTO-2 does not modify the AUTO-1 artifact.

Current baseline:

- latest main expected: `2f846ccd6de80881316018776dcced6ae24cf539`
- physical `agents/**/*.md` before AUTO-2: `146`
- expected physical `agents/**/*.md` after merge if accepted: `147`
- safe-managed total: `53`
- Sovereign index: `routing_enabled: false`

These baseline values are repository-count context only. They do not create command authority, activation authority, production authority, formal approval evidence, or WORM evidence.

## 3. Future /paex Command Set Design Purpose

Future candidate `/paex` commands may reduce K's manual relay burden by using GitHub Issue comments, PR comments, and labels as task input. GitHub labels may become candidate state markers, and the GitHub PR timeline may remain an audit trail input.

The design purpose is to preserve K authorization for high-risk gates, preserve WORM / authority / production boundaries, and support future Level 2 IssueOps semi-automation only after separate implementation authorization.

This purpose statement is candidate-only. It does not activate Level 2, does not create command execution, and does not establish an IssueOps operating convention.

## 4. Candidate Command List

Every command listed below is NOT IMPLEMENTED, NOT ENABLED, NOT EXECUTABLE, and HOLD until separately authorized.

| Command | Candidate purpose | Possible trigger surface | Candidate actor requirement | Required authorization candidate | Exact head SHA requirement | Allowed output | Prohibited action | Expected audit trail | Failure mode | HOLD condition | WORM impact | Current router state |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `/paex audit` | Read-only repository, PR, or governance audit candidate. | GitHub issue or PR comment. | Verified allowed actor candidate. | Scope-specific authorization where risk requires. | Required when tied to PR state. | Audit summary, repository state report, gap analysis, blocker matrix. | File mutation, commit, PR creation, merge, WORM record, approval evidence, production authority. | Issue / PR comment thread. | HOLD. | Scope unclear, protected data risk, actor not verified. | Usually not WORM required for read-only report; future evidence mutation may require WORM. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex prepare` | Task packet or Codex-ready prompt candidate. | GitHub issue comment. | Verified allowed actor candidate. | Documentary / preparation scope authorization. | Optional unless tied to PR state. | Task packet, prompt draft, scope checklist, authorization checklist. | Automatic Codex execution, branch creation, PR creation, file modification, workflow creation, authority creation. | Issue comment thread. | HOLD. | Ambiguous scope, missing risk classification, missing K authorization where required. | Usually no WORM for draft packet; future authority evidence may require WORM. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex create` | Task creation request candidate. | GitHub issue comment. | Verified allowed actor candidate. | Exact file / branch / scope authorization. | Required when PR-linked or branch-linked. | Candidate branch / PR creation request, task plan, proposed file scope. | Automatic Codex execution authorization, unapproved file modification, protected scope mutation, workflow creation, WORM record creation, formal approval evidence creation, production deployment. | Issue / PR thread plus future branch record if separately authorized. | HOLD. | Scope mismatch, protected scope risk, no explicit authorization. | Future file mutation may not be WORM by itself; authority or evidence mutation remains WORM REQUIRED where applicable. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex review` | Read-only PR review candidate. | PR comment. | Verified allowed actor candidate. | PR number, expected commit, and review scope authorization. | Required. | Review summary, PASS / HOLD recommendation, protected scope analysis, wording risk analysis. | Guardian approval authority, formal approval evidence, merge, file modification, production authority. | PR timeline. | HOLD. | Head SHA mismatch, diff unavailable, protected scope ambiguity. | Review comment usually not WORM required; future authority evidence remains WORM REQUIRED where applicable. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex repair` | Targeted repair candidate if separately authorized. | PR comment. | Verified allowed actor candidate. | Exact file and repair scope authorization. | Required. | Targeted repair proposal, limited repair task packet, future branch repair scope. | Self-authorized repair, broad rewrite, protected scope modification, workflow modification, schema mutation, WORM record creation, production authority. | PR timeline plus future commit if separately authorized. | HOLD. | Repair scope mismatch, protected file touched, stale head SHA. | Repair may require WORM if authority, schema, or formal evidence is affected. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex tier2` | Tier 2 PR-linked evidence comment candidate. | PR comment. | Verified allowed actor candidate. | Prior review gates PASS and separate Tier 2 authorization. | Required. | PR-linked evidence comment, review evidence summary. | Formal approval evidence, approval authority, Guardian approval, K / CEO / Sovereign substitute authority, WORM record, final go/no-go, production authority. | PR timeline comment. | HOLD. | Review not PASS, duplicate evidence, write failure, head SHA mismatch. | Comment itself may be WORM not required; future formal evidence remains WORM REQUIRED. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex merge` | K-authorized merge candidate. | PR comment. | Verified K or authorized K-scope actor candidate. | Explicit K authorization. | Required. | Merge plus post-merge validation candidate if separately implemented. | Auto-merge without K, merge on stale head SHA, merge with protected scope failure, merge as approval, merge as production authority, merge as go/no-go. | PR timeline and merge commit. | HOLD. | Missing K authorization, head mismatch, protected scope fail, count fail, WORM boundary fail. | Merge of documentary files may be WORM not required; authority/evidence/schema actions remain WORM REQUIRED. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex postmerge` | Post-merge validation candidate. | PR comment or merge event. | Verified allowed actor candidate. | Merged PR reference and validation scope authorization. | Required for referenced PR head. | Latest main HEAD, merged commit validation, file diff validation, count model validation, protected scope validation, authority boundary validation. | Creating WORM record, creating formal approval evidence, production deployment, production authority, lifecycle state mutation. | PR timeline and validation report. | HOLD. | Main mismatch, diff check fail, protected scope fail, count mismatch. | Validation report usually not WORM required; future authority evidence remains WORM REQUIRED. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex status` | State reporting candidate. | GitHub issue or PR comment. | Verified allowed actor candidate. | Read-only status scope authorization. | Required when reporting PR-specific state. | PR state, branch state, count state, gate state, HOLD / PROCEED recommendation. | Lifecycle state creation, production state creation, risk acceptance, authority creation, final go/no-go. | Issue / PR comment. | HOLD. | State cannot be verified, actor not verified, ambiguity detected. | Usually not WORM required; future authority state remains WORM REQUIRED. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |

## 5. Candidate Command Schema

Future candidate command fields may include:

- command name
- target issue / PR
- target branch
- expected head SHA
- expected base SHA
- risk level
- task type
- authorization evidence URL
- Tier 2 evidence URL
- allowed files
- prohibited scopes
- WORM impact
- output mode
- failure mode
- router state

This is only future schema design. It does not implement parser logic, does not create config files, does not create JSON schema files, and does not create YAML workflow files.

## 6. Command-by-command Matrix

| Command | Candidate Purpose | Trigger Surface | Actor Requirement | K Authorization Required? | Exact Head SHA Required? | Allowed Output | Prohibited Action | WORM Impact | Failure Mode | Current Router State |
|---|---|---|---|---|---|---|---|---|---|---|
| `/paex audit` | Read-only audit. | Issue / PR comment. | Verified allowed actor. | Depends on risk. | Yes for PR-linked audit. | Audit summary / blocker matrix. | Mutation, merge, WORM record, approval evidence. | Future evidence mutation may be WORM REQUIRED. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex prepare` | Prepare task packet. | Issue comment. | Verified allowed actor. | Yes for High governance scope. | Optional unless PR-linked. | Prompt draft / checklist. | Execution, branch, PR, file mutation. | Future authority evidence may be WORM REQUIRED. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex create` | Request creation scope. | Issue comment. | Verified allowed actor. | Yes. | Yes when branch / PR-linked. | Proposed file scope / task plan. | Automatic execution, protected scope mutation. | Depends on future file / evidence scope. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex review` | Read-only PR review. | PR comment. | Verified allowed actor. | Yes for High PR. | Yes. | PASS / HOLD recommendation. | Approval authority, merge, file mutation. | Future authority evidence remains WORM REQUIRED. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex repair` | Targeted repair scope. | PR comment. | Verified allowed actor. | Yes. | Yes. | Repair proposal / limited task packet. | Self-authorized repair, broad rewrite. | WORM REQUIRED where authority/schema/evidence affected. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex tier2` | PR-linked evidence comment. | PR comment. | Verified allowed actor. | Yes. | Yes. | PR-linked evidence comment. | Formal approval evidence, WORM record, authority. | Future formal evidence remains WORM REQUIRED. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex merge` | K-authorized merge. | PR comment. | Verified K authorization source. | Yes, explicit. | Yes. | Merge / validation candidate. | Auto-merge without K, stale-head merge. | Depends on PR and authority scope. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex postmerge` | Post-merge validation. | PR comment / future event. | Verified allowed actor. | Yes for High governance PR. | Yes for referenced PR. | Validation report. | WORM record, formal evidence, production authority. | Future authority evidence remains WORM REQUIRED. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| `/paex status` | State report. | Issue / PR comment. | Verified allowed actor. | Depends on scope. | Yes for PR-specific state. | Status report / recommendation. | Lifecycle state, production state, final go/no-go. | Usually no WORM unless authority state created. | HOLD. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |

## 7. /paex audit Boundary

`/paex audit` is a future candidate command for read-only audit tasks only.

Allowed future candidate outputs include audit summary, repository state report, gap analysis, and blocker matrix.

Prohibited actions include file modification, commit, PR creation, merge, WORM record creation, approval evidence creation, and production authority creation.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 8. /paex prepare Boundary

`/paex prepare` is a future candidate command for generating task packets or Codex-ready prompts.

Allowed future candidate outputs include task packet, prompt draft, scope checklist, and authorization checklist.

Prohibited actions include automatic Codex execution, branch creation, PR creation, file modification, workflow creation, and authority creation.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 9. /paex create Boundary

`/paex create` is a future candidate command that may eventually request task creation, but not automatic execution unless separately authorized.

Allowed future candidate outputs include candidate branch / PR creation request, task plan, and proposed file scope.

Prohibited actions include automatic Codex execution authorization, unapproved file modification, protected scope mutation, workflow creation, WORM record creation, formal approval evidence creation, and production deployment.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 10. /paex review Boundary

`/paex review` is a future candidate command for read-only PR review.

Allowed future candidate outputs include review summary, PASS / HOLD recommendation, protected scope analysis, and wording risk analysis.

Prohibited actions include Guardian approval authority, formal approval evidence, merge, file modification, and production authority.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 11. /paex repair Boundary

`/paex repair` is a future candidate command for targeted repair only if separately authorized.

Allowed future candidate outputs include targeted repair proposal, limited repair task packet, and future branch repair scope.

Prohibited actions include self-authorized repair, broad rewrite, protected scope modification, workflow modification, schema mutation, WORM record creation, and production authority.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 12. /paex tier2 Boundary

`/paex tier2` is a future candidate command for Tier 2 PR-linked evidence comment creation only after all required gates pass and only if separately authorized.

Allowed future candidate outputs include PR-linked evidence comment and review evidence summary.

Prohibited actions include formal approval evidence, approval authority, Guardian approval, K / CEO / Sovereign substitute authority, WORM record, final go/no-go, and production authority.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 13. /paex merge Boundary

`/paex merge` is a future candidate command for K-authorized merge only.

Required future safeguards include explicit K authorization, exact head SHA lock, required review gates PASS, protected scope PASS, count model PASS, Sovereign boundary PASS, WORM boundary PASS, and failure closed to HOLD.

Prohibited actions include auto-merge without K, merge on stale head SHA, merge with protected scope failure, merge as approval, merge as production authority, and merge as go/no-go.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 14. /paex postmerge Boundary

`/paex postmerge` is a future candidate command for post-merge validation.

Allowed future candidate outputs include latest main HEAD, merged commit validation, file diff validation, count model validation, protected scope validation, and authority boundary validation.

Prohibited actions include creating WORM record, creating formal approval evidence, production deployment, production authority, and lifecycle state mutation.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 15. /paex status Boundary

`/paex status` is a future candidate command for reporting state only.

Allowed future candidate outputs include PR state, branch state, count state, gate state, and HOLD / PROCEED recommendation.

Prohibited actions include lifecycle state creation, production state creation, risk acceptance, authority creation, and final go/no-go.

Current state: NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 16. Actor Verification Boundary

Future candidate actor verification must address GitHub username verification, K authorization distinguishability from non-K comments, label spoofing prevention, issue comment author checks, PR comment author checks, bot comment boundaries, stale authorization expiry, and head SHA re-check.

Commands from unauthorized actors must HOLD.

This brief does not implement actor verification.

## 17. K Authorization Boundary

K remains the high-risk authorization authority. K authorization must be explicit and tied to scope and head SHA where applicable.

K authorization cannot be inferred from discussion, cannot be created by Codex, cannot be created by GitHub Actions, cannot be replaced by labels alone, and cannot be replaced by Tier 2 comments.

## 18. Codex Execution Boundary

This command design does not authorize Codex execution. `/paex create` does not automatically authorize Codex execution.

Codex cannot self-authorize, cannot create approval authority, cannot create production authority, and cannot create WORM records.

Future Codex execution must remain separately scoped and separately authorized.

## 19. GitHub Actions Boundary

This command design does not create workflows, does not implement a command parser, and does not activate GitHub Actions.

Future GitHub Actions may only be guard / validator / commenter if separately authorized. GitHub Actions must not create formal approval evidence, must not create WORM records, and must not authorize production.

Workflow creation remains HOLD.

## 20. Guardian / Tier 2 Boundary

`/paex review` is not Guardian approval authority. `/paex tier2` is not formal approval evidence.

Guardian Review remains review gate only. Tier 2 PR-linked evidence remains PR-linked evidence only.

Neither replaces K authorization, creates production authority, or creates final go/no-go.

## 21. WORM REQUIRED Boundary

Future actions remain WORM REQUIRED where applicable, including:

- command activation affecting formal governance execution
- command parser implementation controlling evidence workflows
- workflow creation affecting approval / WORM / production evidence
- formal approval evidence creation
- WORM record creation
- canonical schema mutation
- evidence validation model establishment
- production authority creation
- final go/no-go
- Sovereign / authority boundary mutation

This brief itself is documentary-only and WORM NOT REQUIRED.

## 22. Production Go-live Boundary

This brief does not create production deployment, runtime automation, operations readiness, final go/no-go, or production authority.

Future production use remains HOLD and requires separately scoped development, testing, security, deployment, evidence, WORM, authority, and K authorization gates.

## 23. Failure Mode / HOLD Policy

Future commands must fail closed.

Candidate failure rules:

- unauthorized actor -> HOLD
- missing K authorization -> HOLD
- head SHA mismatch -> HOLD
- target PR mismatch -> HOLD
- protected scope touched -> HOLD
- count model mismatch -> HOLD
- safe-managed total mismatch -> HOLD
- Sovereign index changed unexpectedly -> HOLD
- WORM schema touched -> HOLD
- formal approval evidence touched -> HOLD
- workflow modified unexpectedly -> HOLD
- GitHub write action fails -> HOLD
- command parser ambiguity -> HOLD
- suspected prompt injection -> HOLD
- label spoofing risk -> HOLD

No future command may work around a HOLD condition or self-escalate authority.

## 24. Security / Abuse Risks

Candidate risks include:

- prompt injection through issue comments
- malicious command text
- unauthorized actor commands
- label spoofing
- stale head SHA merge
- fake K authorization
- bot identity confusion
- token / secret leakage
- workflow self-modification
- command parser ambiguity
- accidental protected scope mutation
- PR comment as false approval
- Codex self-escalation
- Tier 2 evidence spoofing
- WORM boundary bypass
- production authority spoofing

Candidate mitigations include actor allowlists, explicit K authorization evidence checks, exact head SHA locks, protected-scope diff guards, parser ambiguity rejection, command allowlists, no workflow self-modification, least-privilege tokens, duplicate evidence checks, WORM-required boundary checks, and human review gates.

These mitigations are candidate-only and are not implemented by this brief.

## 25. Count Model Boundary

If this PR is merged, physical `agents/**/*.md` count may increase from `146` to `147`.

`147` is documentary Markdown count only.

`147` is not:

- safe-managed count
- agent-like count
- activation denominator
- approval
- authorization
- command implementation
- command activation
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

## 26. Relationship to Level 2 and Level 3

AUTO-2 supports future Level 2 design. AUTO-2 does not implement Level 2, does not activate IssueOps, and does not qualify the system for Level 3.

Level 3 remains HOLD until a Level 2 MVP is implemented, tested, and passes 3-5 low-risk PR validation cycles without major governance boundary failure.

## 27. Non-decisions

This brief makes no decision and creates no establishment or activation for:

- `/paex` command activation
- command parser implementation
- GitHub Actions workflow creation
- workflow file modification
- automation implementation
- automation activation
- Codex automation activation
- IssueOps command execution
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
- existing AUTO-1 modification
- `pace-ai` to `PAEX-GOS` rename
- repo-wide text replacement

## 28. Rename Boundary

No `pace-ai` to `PAEX-GOS` rename is executed. No repo-wide text replacement is executed. Historical references are not silently rewritten.

Future rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 29. Router Decision

PROCEED only for documentary-only AUTO-2 IssueOps command design candidate brief PR creation.

HOLD for IssueOps command activation, command parser implementation, GitHub Actions workflow creation, workflow file modification, automation implementation, automation activation, Codex automation activation, GitHub App installation, GitHub token creation, secret creation, API key creation, webhook creation, PR auto-merge enablement, automatic Codex execution authorization, automatic Guardian approval, automatic Tier 2 approval, formal approval evidence creation, WORM record creation, production deployment, runtime automation enablement, agent activation, safe-managed production use, Sovereign routing enablement, execution authorization, activation authorization, risk acceptance, lifecycle state, production authority, final go/no-go, backend implementation, evidence validation model establishment, canonical convention establishment, schema mutation, README.md / AGENTS.md modification, registry modification, agent file modification, existing AUTO-1 artifact modification, `pace-ai` to `PAEX-GOS` rename, and repo-wide text replacement.
