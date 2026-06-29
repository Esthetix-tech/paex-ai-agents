---
title: "AUTO-3｜PR Guard Candidate Implementation Plan / Validation Design Brief"
status: "candidate_brief"
mode: "documentary_only"
risk_level: "high"
business_context_layer: "Enterprise Governance / Repository Governance / Automation Governance / PR Guard Governance"
caep_mapping: "G｜Governance"
worm_required: false
worm_required_scope: "future_pr_guard_implementation_validation_script_workflow_creation_automation_activation_authority_or_production_use_only"
canonical: false
pr_guard_implemented: false
pr_guard_enabled: false
pr_guard_executable: false
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
created_from_baseline: "a125abe2e17c8e651e46cf511445073a1bdc6a7f"
auto_1_reference: "agents/governance/agent-intake-pipeline/option-auto-1-paex-issueops-orchestrator-automation-candidate-brief.md"
auto_2_reference: "agents/governance/agent-intake-pipeline/auto-2-read-only-issueops-command-design-candidate-brief.md"
safe_managed_total_expected: 53
physical_agents_md_count_before_expected: 147
physical_agents_md_count_after_expected_if_merged: 148
sovereign_index_expected: "routing_enabled: false"
---

# AUTO-3｜PR Guard Candidate Implementation Plan / Validation Design Brief

## 1. Document Status

This document is documentary-only, candidate-only, and a PR Guard planning / validation design brief only.

AUTO-3 is documentary-only. AUTO-3 is candidate-only.

This document is not PR Guard implementation, not PR Guard activation, not validation script creation, not GitHub Actions workflow creation, not automation implementation, not automation activation, not IssueOps command activation, not command parser implementation, not Codex automation activation, not PR auto-merge enablement, not formal approval evidence, not a WORM record, not production authority, and not final go/no-go.

PR Guard remains NOT IMPLEMENTED. PR Guard checks remain NOT ENABLED. PR Guard checks remain NOT EXECUTABLE. PR Guard script remains NOT CREATED. Validation script remains NOT CREATED. GitHub Actions implementation remains HOLD. Command parser implementation remains HOLD. IssueOps command activation remains HOLD. Codex automation activation remains HOLD. PR auto-merge remains HOLD. Workflow creation remains HOLD. Production deployment remains HOLD. Execution / activation / production authority remains HOLD. Final go/no-go remains HOLD.

## 2. AUTO-1 / AUTO-2 Baseline and AUTO-3 Scope

AUTO-1 established candidate IssueOps Orchestrator architecture. AUTO-2 defined future `/paex` command semantics. Neither AUTO-1 nor AUTO-2 implemented workflows, commands, parsers, scripts, or automation.

AUTO-3 designs the candidate PR Guard validation matrix needed before Level 2 IssueOps semi-automation. AUTO-3 does not implement PR Guard and does not modify AUTO-1 or AUTO-2 artifacts.

Existing AUTO-1 artifact remains unmodified. Existing AUTO-2 artifact remains unmodified.

Current baseline:

- latest main expected: `a125abe2e17c8e651e46cf511445073a1bdc6a7f`
- physical `agents/**/*.md` before AUTO-3: `147`
- expected physical `agents/**/*.md` after merge if accepted: `148`
- safe-managed total: `53`
- Sovereign index: `routing_enabled: false`

These baseline values are repository-count context only. They do not create PR Guard authority, automation authority, formal approval evidence, WORM evidence, production authority, or go/no-go.

## 3. Why PR Guard Must Precede Level 2

Level 2 IssueOps semi-automation must not proceed before PR Guard design because automation increases velocity and risk. Future `/paex create`, `/paex review`, `/paex merge`, and `/paex postmerge` flows require guardrails before any implementation can be considered.

Protected scope violations must be machine-detectable, count model errors must be caught, WORM / formal approval / production authority wording must be blocked or routed to HOLD, workflow or automation activation must be detected, and failure must close to HOLD. K authorization and exact head SHA verification must remain central.

This section is candidate rationale only. It does not implement PR Guard.

## 4. PR Guard Candidate Purpose

PR Guard is a future candidate safety layer for:

- PR diff validation
- protected scope validation
- count model validation
- Sovereign boundary validation
- WORM boundary validation
- workflow / script / config mutation detection
- command activation detection
- automation implementation detection
- forbidden authority wording detection
- Level 2 / Level 3 misinterpretation prevention
- rename boundary validation
- failure-closed HOLD routing

PR Guard is not approval authority, not formal approval evidence, not Guardian Review, not Tier 2 approval, not K authorization, not production authority, and not go/no-go.

## 5. Candidate Check Categories

Future PR Guard check categories may include:

- file addition / modification / deletion diff check
- protected scope check
- `.github/workflows` mutation check
- scripts / validation scripts check
- configs / schemas check
- secrets / tokens / API keys / webhooks check
- `README.md` / `AGENTS.md` check
- registry files check
- agent files check
- Sovereign index check
- WORM schema check
- WORM records check
- formal approval evidence check
- audit evidence check
- existing AUTO artifacts check
- safe-managed total check
- physical `agents/**/*.md` count check
- forbidden authority wording scan
- command activation wording scan
- command parser implementation wording scan
- automation implementation wording scan
- workflow creation wording scan
- production readiness wording scan
- Level 2 / Level 3 boundary scan
- rename boundary scan
- failure-closed HOLD policy check

Every check remains future candidate design only. No check is implemented, enabled, executable, active, deployed, or canonical by this brief.

## 6. Candidate Check Matrix

| Check Name | Candidate Purpose | Input Evidence | PASS Condition | HOLD Condition | Failure Severity | K Authorization Dependency | WORM Impact | Protected Scope Impact | Output Evidence | Current Router State |
|---|---|---|---|---|---|---|---|---|---|---|
| File diff check | Identify added, modified, deleted, binary, generated, config, and executable files. | PR diff. | Only scoped files changed. | Unexpected add / modify / delete. | High. | Required for exceptions. | WORM where authority/evidence affected. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Protected scope check | Detect protected scope changes. | PR file list and paths. | No protected scope touched unless separately scoped. | Protected scope touched. | High. | Required for protected changes. | WORM where applicable. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Workflow mutation check | Detect `.github/workflows` add/modify. | PR diff paths. | No workflow changes. | Workflow added/modified. | High. | Required for workflow changes. | WORM where approval/WORM/production evidence affected. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Scripts / validation scripts check | Detect executable script creation or mutation. | PR diff paths and extensions. | No scripts unless scoped. | Script or validation script added/modified unexpectedly. | High. | Required for scripts. | WORM where evidence workflow controlled. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Configs / schemas check | Detect config, JSON schema, YAML schema, and deployment config changes. | PR diff paths and extensions. | No config/schema changes unless scoped. | Unexpected config/schema change. | High. | Required for config/schema scope. | WORM for canonical schema mutation. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Secrets / tokens / webhooks check | Detect secret-bearing or integration artifacts. | PR diff paths and content indicators. | No secrets, tokens, API keys, or webhooks. | Secret or webhook artifact appears. | Critical. | Required plus security review. | WORM likely where authority/security affected. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| README / AGENTS check | Detect repository instruction or top-level doc mutation. | PR diff paths. | No `README.md` or `AGENTS.md` changes unless scoped. | Root instruction/documentation changed unexpectedly. | High. | Required for instruction changes. | WORM for high-risk governance changes. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Registry / agent files check | Detect registry and agent file changes. | PR diff paths. | No registry/agent changes unless scoped. | Registry or agent file touched unexpectedly. | High. | Required. | WORM where authority/activation affected. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Sovereign index check | Ensure Sovereign routing boundary remains unchanged. | Sovereign index file. | `routing_enabled: false` unless separately authorized. | Unexpected Sovereign change. | Critical. | Explicit K authorization required. | WORM REQUIRED where boundary mutated. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| WORM schema / record check | Detect WORM schema, record, or draft changes. | PR diff paths. | No WORM schema/record changes unless scoped. | WORM schema touched or record created. | Critical. | Required. | WORM REQUIRED for future applicable actions. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Formal approval / audit evidence check | Detect formal approval evidence or audit evidence mutation. | PR diff paths and wording. | No formal approval evidence created; audit evidence unchanged unless scoped. | Evidence path touched unexpectedly. | Critical. | Required. | WORM REQUIRED for formal evidence. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Existing AUTO artifacts check | Ensure AUTO-1/AUTO-2 are not silently modified. | PR diff paths. | Existing AUTO artifacts unchanged unless scoped. | AUTO-1/AUTO-2 touched unexpectedly. | High. | Required. | Depends on scope. | Direct. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Safe-managed total check | Verify safe-managed total evidence. | Safe-managed source file. | Total remains `53` unless separately authorized. | Mismatch or unauthorized change. | High. | Required for changes. | WORM where activation/authority affected. | Count boundary. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Physical Markdown count check | Calculate physical `agents/**/*.md` count. | Repository file tree. | Expected count matches PR scope. | Count mismatch. | Medium/High. | Required for count-affecting PRs. | Usually not WORM by itself. | Count boundary. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Forbidden authority wording scan | Detect risky authority claims. | Added/modified text. | Terms appear only in negative, candidate, future, prohibited, non-decision, risk, or HOLD context. | Authority implied. | High/Critical. | Required for authority claims. | WORM where authority/evidence affected. | Semantic. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Command / parser activation scan | Detect IssueOps command or parser activation claims. | Added/modified text and file paths. | No activation/implementation implied. | Command/parser activation implied. | High. | Required. | WORM where formal governance execution affected. | Semantic. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Workflow / automation implementation scan | Detect automation implementation or activation. | PR diff and wording. | No implementation/activation implied. | Automation implied or files created. | High/Critical. | Required. | WORM where evidence/production affected. | Direct/semantic. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Production readiness scan | Detect production/go-live claims. | Added/modified text. | No production authority/readiness/go-live created. | Production state implied. | Critical. | Explicit K authorization required. | WORM REQUIRED where applicable. | Semantic. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Level 2 / Level 3 boundary scan | Prevent Level 2/3 misinterpretation. | Added/modified text. | Candidate-only design boundary preserved. | Level 2 implementation or Level 3 readiness implied. | High. | Required for promotion. | WORM where authority/activation affected. | Semantic. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Rename boundary scan | Detect `pace-ai` to `PAEX-GOS` or repo-wide replacement. | PR diff and text changes. | No rename/replacement unless scoped. | Rename or replacement appears. | High. | Required. | WORM where applicable. | Direct/semantic. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |
| Failure-closed HOLD policy check | Ensure guard failures route to HOLD. | Candidate guard result. | Any uncertainty routes HOLD. | Workaround or self-escalation implied. | High. | Required for exceptions. | Depends on failed area. | Router boundary. | Candidate guard report. | NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD. |

## 7. Protected Scope Diff Check

Future candidate rules must detect changes to Batch A target files, Batch B target files, Batch C target files, existing Phase 5 artifacts, existing AUTO-1 artifact, existing AUTO-2 artifact, registry files, agent files, Sovereign index, canonical WORM Event Schema, existing WORM records, audit evidence, formal approval evidence, `README.md`, `AGENTS.md`, `.github/workflows`, scripts, validation scripts, configs, schemas, secrets-related files, and deployment files.

Any protected scope modification should route to HOLD unless separately scoped, reviewed, and K-authorized. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 8. File Addition / Modification / Deletion Check

Future candidate rules must distinguish expected added files, unexpected added files, unexpected modified files, deleted files, binary files, generated files, config files, and executable files.

Unexpected deletion or unscoped modification must HOLD. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 9. .github/workflows Mutation Check

Future candidate rules must HOLD for workflow file addition unless separately authorized. Workflow file modification must HOLD unless separately authorized. Workflow self-modification must HOLD.

Workflow creation cannot be inferred from a candidate brief. Workflow implementation remains WORM REQUIRED where applicable. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 10. Scripts / Configs / Secrets Check

Future candidate rules must detect shell scripts, Python scripts, JavaScript / TypeScript scripts, validation scripts, GitHub Action configs, JSON schemas, YAML configs, `.env`, secrets, tokens, API keys, webhook configs, and deployment configs.

Any executable or secret-bearing artifact must HOLD unless separately authorized. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 11. README.md / AGENTS.md Check

Future candidate rules must HOLD for `README.md` modification unless separately scoped. `AGENTS.md` modification must HOLD unless separately scoped.

Global instruction changes must not be hidden inside automation PRs. Instruction changes require separate governance review. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 12. Registry / Agent Files Check

Future candidate rules must HOLD registry modifications unless separately scoped. Agent file modifications must HOLD unless separately scoped.

Physical Markdown count must not be treated as safe-managed count. Agent-like files must not be treated as activation authority. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 13. Sovereign Boundary Check

Future candidate rules must verify the Sovereign index remains `routing_enabled: false` unless separately authorized.

Any Sovereign routing mutation must HOLD. Sovereign routing enablement cannot be created by PR Guard. Sovereign authority cannot be created by automation. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 14. WORM Schema / WORM Record Check

Future candidate rules must HOLD canonical WORM Event Schema mutation, WORM record creation, and WORM draft creation unless separately scoped.

WORM REQUIRED future action must not be downgraded. Candidate brief WORM NOT REQUIRED applies only to the brief itself. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 15. Formal Approval / Audit Evidence Check

Future candidate rules must HOLD formal approval evidence creation. Audit evidence mutation must HOLD unless separately scoped.

PR-linked evidence must not be treated as formal approval evidence. Tier 2 comment must remain PR-linked evidence only. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 16. Count Model Check

Future candidate rules must calculate physical `agents/**/*.md` count, verify safe-managed total remains `53` unless separately authorized, and prevent physical count from being treated as safe-managed count or activation denominator.

`183` remains NOT OBSERVED unless directly verified. Count mismatch must HOLD. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 17. Forbidden Authority Wording Scan

Future candidate scan terms include:

- approved
- approval authority
- formal approval evidence
- authorized
- execution authorization
- activation authorization
- production authority
- risk acceptance
- lifecycle state
- final go/no-go
- production-ready
- operational
- canonical
- adopted
- selected
- implemented
- enabled
- activated
- deployed
- WORM record
- formal evidence
- Sovereign routing enabled
- auto-merge enabled

Such terms may appear only in negative, candidate, future, prohibited, non-decision, risk, or HOLD contexts. This scan is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 18. Command / Parser / IssueOps Activation Scan

Future candidate scan logic must detect whether a PR implies `/paex` command activation, command parser implementation, command executable status, IssueOps command deployment, GitHub Action trigger activation, Codex automatic execution authorization, or `/paex merge` as auto-merge.

All such implications must HOLD. This scan is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 19. Workflow / Automation Implementation Scan

Future candidate scan logic must detect whether a PR implies GitHub Actions workflow creation, automation implementation, automation activation, runtime automation, Codex automation activation, Tier 2 automation activation, post-merge automation activation, or production automation.

All such implications must HOLD unless separately authorized. This scan is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 20. Production Readiness / Go-live Scan

Future candidate scan logic must detect whether a PR implies production deployment, operations readiness, production authority, final go/no-go, lifecycle state, risk acceptance, safe-managed production use, agent activation, or runtime authority.

All such implications must HOLD unless separately authorized. This scan is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 21. Level 2 / Level 3 Boundary Scan

AUTO-3 supports future Level 2 design only. AUTO-3 does not implement Level 2 and does not qualify the system for Level 3.

Level 3 remains HOLD until Level 2 MVP is separately authorized, implemented, tested, and passes 3-5 low-risk PR validation cycles. Any PR implying Level 3 readiness from AUTO-3 alone must HOLD.

## 22. Rename Boundary Check

Future candidate rules must verify no `pace-ai` to `PAEX-GOS` rename, no repo-wide text replacement, and no silent rewriting of historical references.

Rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable. This check is NOT IMPLEMENTED / NOT ENABLED / NOT EXECUTABLE / HOLD.

## 23. K Authorization Verification Dependency

PR Guard cannot create K authorization. PR Guard can only verify future candidate evidence of K authorization.

K authorization must be explicit and tied to target PR and head SHA where applicable. Labels alone cannot replace K authorization. Comments by non-K actors cannot create K authorization. A stale head SHA must HOLD.

## 24. Exact Head SHA Lock Dependency

Merge-related checks must verify exact head SHA. If head SHA changes after authorization, HOLD. If authorization does not mention expected head SHA, HOLD for merge. If target PR and head SHA mismatch, HOLD.

## 25. Actor Verification Dependency

Actor verification remains a future dependency. GitHub username verification remains unresolved. Bot identity ambiguity remains unresolved. Issue / PR comment actor verification remains unresolved.

Unauthorized actors must HOLD. Actor verification is not implemented by this brief.

## 26. Failure-closed HOLD Policy

PR Guard must fail closed.

Candidate HOLD triggers include:

- unauthorized actor
- missing K authorization
- head SHA mismatch
- target PR mismatch
- protected scope touched
- unexpected file addition
- unexpected file modification
- file deletion
- count model mismatch
- safe-managed total mismatch
- Sovereign index changed unexpectedly
- WORM schema touched
- WORM record created
- formal approval evidence touched or created
- workflow modified unexpectedly
- script / config / secret created unexpectedly
- command parser ambiguity
- suspected prompt injection
- label spoofing risk
- GitHub write action failure
- validation uncertainty

No PR Guard behavior is implemented by this brief.

## 27. Candidate Output Report Format

Future candidate PR Guard report fields may include:

- Result: PASS / HOLD
- Target PR
- Target branch
- Target head commit
- Base commit
- Files added
- Files modified
- Files deleted
- Protected scope validation
- Workflow mutation validation
- Script / config / secret validation
- Count model validation
- safe-managed total validation
- Sovereign validation
- WORM validation
- Formal evidence validation
- Authority wording validation
- Command activation validation
- Automation implementation validation
- Production boundary validation
- Level 2 / Level 3 boundary validation
- Rename boundary validation
- Remaining risks
- Router decision

This brief does not implement a report generator.

## 28. Future Implementation Inputs

Future implementation inputs may include:

- exact protected scope path list
- Batch A / B / C target path inventory
- current safe-managed count source
- physical count command
- Sovereign index path
- WORM schema path
- WORM records path
- formal approval evidence path
- audit evidence path
- AUTO artifact paths
- allowed documentary-only target paths
- forbidden wording list
- actor verification source
- K authorization evidence format
- head SHA lock format
- failure policy

All are future inputs only. None are implemented, canonicalized, activated, or configured by this brief.

## 29. WORM REQUIRED Boundary

Future actions remain WORM REQUIRED where applicable, including:

- PR Guard implementation affecting formal governance execution
- validation script creation controlling evidence workflows
- workflow creation affecting approval / WORM / production evidence
- command parser implementation controlling issue comments
- automation activation
- formal approval evidence creation
- WORM record creation
- canonical schema mutation
- evidence validation model establishment
- production authority creation
- final go/no-go
- Sovereign / authority boundary mutation

This brief itself is documentary-only and WORM NOT REQUIRED.

## 30. Production Go-live Boundary

This brief does not create production deployment, runtime automation, operations readiness, final go/no-go, or production authority.

Future production use remains HOLD and requires separately scoped development, testing, security, deployment, evidence, WORM, authority, and K authorization gates.

## 31. Count Model Boundary

If this PR is merged, physical `agents/**/*.md` count may increase from `147` to `148`.

`148` is documentary Markdown count only.

`148` is not:

- safe-managed count
- agent-like count
- activation denominator
- approval
- authorization
- PR Guard implementation
- validation implementation
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

## 32. Non-decisions

This brief makes no decision and creates no establishment or activation for:

- PR Guard implementation
- PR Guard activation
- PR Guard check enablement
- PR Guard script creation
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
- existing AUTO-2 modification
- `pace-ai` to `PAEX-GOS` rename
- repo-wide text replacement

## 33. Rename Boundary

No `pace-ai` to `PAEX-GOS` rename is executed. No repo-wide text replacement is executed. Historical references are not silently rewritten.

This brief confirms no `pace-ai` to `PAEX-GOS` rename executed and no repo-wide text replacement executed.

Future rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 34. Router Decision

PROCEED only for documentary-only AUTO-3 PR Guard candidate implementation plan / validation design brief PR creation.

HOLD for PR Guard implementation, PR Guard activation, PR Guard check enablement, guard script creation, validation script creation, executable validation logic, GitHub Actions workflow creation, workflow file modification, automation implementation, automation activation, IssueOps command activation, command parser implementation, Codex automation activation, GitHub App installation, GitHub token creation, secret creation, API key creation, webhook creation, PR auto-merge enablement, automatic Codex execution authorization, automatic Guardian approval, automatic Tier 2 approval, formal approval evidence creation, WORM record creation, production deployment, runtime automation enablement, agent activation, safe-managed production use, Sovereign routing enablement, execution authorization, activation authorization, risk acceptance, lifecycle state, production authority, final go/no-go, backend implementation, evidence validation model establishment, canonical convention establishment, schema mutation, README.md / AGENTS.md modification, registry modification, agent file modification, existing AUTO-1 artifact modification, existing AUTO-2 artifact modification, `pace-ai` to `PAEX-GOS` rename, and repo-wide text replacement.
