---
title: "AUTO-6｜Forbidden Wording Dictionary Candidate Brief"
status: "candidate_brief"
mode: "documentary_only"
risk_level: "high"
business_context_layer: "Enterprise Governance / Repository Governance / Automation Governance / PR Guard Wording Risk Review"
caep_mapping: "G｜Governance"
worm_required: false
worm_required_scope: "future_canonical_dictionary_pr_guard_implementation_workflow_creation_validation_script_automation_activation_authority_or_production_use_only"
canonical: false
forbidden_wording_dictionary_canonical: false
machine_enforced_wording_registry: false
machine_readable_dictionary_created: false
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
created_from_baseline: "ad527ed8331b5b89a16f72707a0769ac818fdfef"
auto_1_reference: "agents/governance/agent-intake-pipeline/option-auto-1-paex-issueops-orchestrator-automation-candidate-brief.md"
auto_2_reference: "agents/governance/agent-intake-pipeline/auto-2-read-only-issueops-command-design-candidate-brief.md"
auto_3_reference: "agents/governance/agent-intake-pipeline/auto-3-pr-guard-candidate-implementation-plan-validation-design-brief.md"
auto_5_reference: "agents/governance/agent-intake-pipeline/auto-5-protected-scope-path-inventory-candidate-brief.md"
safe_managed_total_expected: 53
physical_agents_md_count_before_expected: 149
physical_agents_md_count_after_expected_if_merged: 150
sovereign_index_expected: "routing_enabled: false"
---

# AUTO-6｜Forbidden Wording Dictionary Candidate Brief

## 1. Document Status

This document is documentary-only.

This document is candidate-only.

This document is a forbidden wording dictionary candidate brief only.

This document is not a canonical forbidden wording dictionary, not a canonical governance dictionary, not a machine-enforced wording registry, not a machine-readable dictionary, not runtime config, and not a PR Guard input file.

This document is not PR Guard implementation, not PR Guard activation, not PR Guard check enablement, not validation script creation, not GitHub Actions workflow creation, not automation implementation, not automation activation, not IssueOps command activation, not command parser implementation, not Codex automation activation, and not PR auto-merge enablement.

This document is not formal approval evidence, not a WORM record, not production authority, not Level 2 implementation, not Level 3 readiness, and not final go/no-go.

## 2. AUTO-1 / AUTO-2 / AUTO-3 / AUTO-4 / AUTO-5 Baseline

AUTO-1 established candidate IssueOps Orchestrator architecture.

AUTO-2 defined future `/paex` command semantics.

AUTO-3 designed the future PR Guard check matrix.

AUTO-4 returned PARTIAL READY / BLOCKED because machine-ready prerequisites remained incomplete.

AUTO-5 created a candidate protected scope path inventory. AUTO-5 helps future reviewers understand where a change occurred.

AUTO-6 addresses whether wording may imply unauthorized governance state.

AUTO-6 does not implement PR Guard. AUTO-6 does not create a canonical dictionary. AUTO-6 does not modify AUTO-1 / AUTO-2 / AUTO-3 / AUTO-5 artifacts.

Current baseline:

- latest main expected: `ad527ed8331b5b89a16f72707a0769ac818fdfef`
- physical `agents/**/*.md` before AUTO-6: `149`
- expected physical `agents/**/*.md` after merge if accepted: `150`
- safe-managed total: `53`
- Sovereign index: `routing_enabled: false`
- `183`: NOT OBSERVED unless directly verified

## 3. Why Forbidden Wording Dictionary Is Needed

Future PR Guard needs both path-based and wording-based risk detection.

Path inventory answers which files or directories were touched.

Wording dictionary helps detect whether text implies unauthorized approval, authorization, implementation, activation, canonicalization, WORM creation, formal evidence, production readiness, Level 2 / Level 3 readiness, or rename execution.

Missing wording review creates false negative risk. Overbroad wording review creates false positive risk.

Wording interpretation must depend on context, not only raw term matching.

The dictionary must remain candidate-only until separately reviewed and canonicalized.

## 4. Wording Dictionary Purpose

The purpose of AUTO-6 is to collect candidate high-risk governance terms, define allowed contexts, define prohibited contexts, distinguish negative / candidate / future / HOLD contexts from positive assertion contexts, document false positive risks, document false negative risks, support future reviewer discipline, support future PR Guard wording review design, and support future machine-check design only as a later step.

AUTO-6 is not canonical, not approved, not machine-enforced, not executable, not runtime config, not a PR Guard input file, and not a final wording dictionary.

## 5. Context Rule

A word is not automatically forbidden only because it appears.

High-risk terms may be allowed in:

- negative contexts
- candidate-only contexts
- future-only contexts
- non-decision contexts
- boundary statements
- risk descriptions
- HOLD statements
- not implemented statements
- not activated statements
- not authorized statements
- not created statements
- WORM REQUIRED where applicable future-action statements

High-risk terms are prohibited or require HOLD when used as:

- positive current-state assertions
- approval claims
- authorization claims
- implementation claims
- activation claims
- enablement claims
- executable status claims
- deployment claims
- production readiness claims
- canonicalization claims
- WORM record creation claims
- formal approval evidence claims
- Level 2 implementation claims
- Level 3 readiness claims
- K authorization replacement claims
- Sovereign routing / authority mutation claims
- rename execution claims

## 6. Candidate Wording Categories

Future candidate wording categories include:

- approval / authorization wording
- canonicalization wording
- implementation wording
- activation / enablement wording
- executable / runtime wording
- workflow / automation wording
- PR Guard wording
- IssueOps / command parser wording
- Codex automation wording
- WORM / formal evidence wording
- production / go-live wording
- risk acceptance / lifecycle wording
- Level 2 / Level 3 readiness wording
- K authorization replacement wording
- Sovereign / authority wording
- safe-managed / activation denominator wording
- count model wording
- rename / repo-wide replacement wording
- evidence validation model wording
- backend / deployment wording

Every category remains candidate-only.

## 7. Candidate Wording Dictionary Matrix

| Category | Candidate Term / Phrase | Risk Type | High-risk Positive Context | Allowed Context | Prohibited Context | Example Allowed Usage | Example Prohibited Usage | Severity Candidate | Review Action Candidate | WORM Impact | Authority Impact | Future PR Guard Usage | False Positive Risk | False Negative Risk | Required Reviewer Interpretation | Current Router State |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Approval / authorization | approved, authorized, accepted | Unauthorized decision state | Current approval or authorization claim | Negative, future, candidate, K-required boundary | Claiming approval without K evidence | "This PR is not approved for production use." | "This PR is approved for production use." | High | HOLD unless evidence and scope match | WORM where formal approval applies | Could imply approval authority | Candidate wording review input | Blocking negative statements | Missing implied approval without keyword | Check actor, evidence, scope, and head SHA | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Canonicalization | canonical, stable, adopted, selected, final | Unauthorized standard creation | Claiming a candidate as standard | Candidate-only, non-canonical, future review | Establishing canonical dictionary or convention | "This dictionary is not canonical." | "This is the canonical wording dictionary." | High | HOLD unless separately authorized | WORM where canonical governance changes | Could create governance authority | Candidate wording review input | Blocking references to canonical schema | Missing "standard" wording | Check whether rule is proposed or established | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Implementation | implemented, backend implemented | Unauthorized implementation claim | Current implementation claim | Not implemented, future implementation HOLD | Claiming code or backend exists | "PR Guard is not implemented." | "PR Guard is implemented." | High | HOLD | WORM where formal governance execution affected | Could imply operational readiness | Candidate wording review input | Blocking implementation boundary notes | Missing "wired up" wording | Check whether any executable artifact exists | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Activation / enablement | enabled, activated, active | Unauthorized activation | Current active or enabled state | Not enabled, not activated, activation HOLD | Claiming checks or automation are live | "PR Guard checks are not enabled." | "PR Guard checks are enabled." | High | HOLD | WORM where activation changes authority | Could imply runtime authority | Candidate wording review input | Blocking HOLD statements | Missing "turned on" wording | Check actual runtime and workflow state | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Executable / runtime | executable, runtime config, operational | Runtime capability claim | Claiming scan or config can run | Not executable, not runtime config | Claiming machine-ready runtime use | "This brief is not executable." | "This dictionary is runtime config." | High | HOLD | WORM where runtime controls evidence | Could imply machine enforcement | Candidate wording review input | Blocking runtime boundary warnings | Missing "operates" wording | Check if file is prose or executable/config | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Workflow / automation | workflow created, automation activated | Automation activation claim | Claiming GitHub Actions or automation exists | No workflow created, future automation HOLD | Claiming workflows run checks | "No workflow file is created." | "Workflow created for PR Guard." | Critical | HOLD | WORM where workflow controls approval/WORM/production evidence | Could imply automated governance | Candidate wording review input | Blocking workflow prohibition text | Missing "CI guard now runs" wording | Check `.github/workflows` and automation artifacts | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| PR Guard | PR Guard implemented, PR Guard enabled | Guard authority claim | Claiming guard implementation or checks | PR Guard remains not implemented | Treating design as active guard | "PR Guard remains not implemented." | "PR Guard is enabled for PRs." | High | HOLD | WORM where formal governance execution affected | Could imply gate authority | Candidate wording review input | Blocking PR Guard design discussion | Missing "guardrails live" wording | Check design vs executable enforcement | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| IssueOps / parser | command parser implemented, IssueOps activated | Command execution claim | Claiming `/paex` commands are active | Not implemented, future candidate commands | Treating comments as executable commands | "IssueOps command activation remains HOLD." | "The command parser is implemented." | High | HOLD | WORM where command parser controls evidence workflows | Could imply execution authority | Candidate wording review input | Blocking parser boundary text | Missing "comments now trigger" wording | Check whether any parser/workflow exists | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Codex automation | Codex automation activated | Automatic execution claim | Claiming Codex execution is automatic | Codex automation remains HOLD | Authorizing automatic Codex execution | "Codex automation is not activated." | "Codex automation is activated." | High | HOLD | WORM where automation affects governance execution | Could imply self-execution authority | Candidate wording review input | Blocking automation risk notes | Missing "Codex will run" wording | Check whether authorization is separate | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| WORM / formal evidence | WORM record created, formal approval evidence | Evidence creation claim | Claiming WORM or formal approval evidence exists | WORM REQUIRED future action; not a WORM record | Treating PR comment or brief as formal evidence | "This brief is not a WORM record." | "Formal approval evidence is created." | Critical | HOLD | WORM REQUIRED where applicable | Could create audit or approval authority | Candidate wording review input | Blocking WORM boundary notes | Missing "sealed" or "recorded" wording | Check evidence type and repository path | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Production / go-live | production-ready, deployed, go-live, final go/no-go | Production authority claim | Claiming readiness or launch authority | Future production use remains HOLD | Treating brief as production authority | "Production authority remains HOLD." | "System is production-ready." | Critical | HOLD | WORM REQUIRED where production authority created | Could imply go-live | Candidate wording review input | Blocking production risk text | Missing "ready to operate" wording | Check whether final decision exists | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Risk / lifecycle | risk accepted, lifecycle state | Risk ownership claim | Claiming risk acceptance or lifecycle transition | No risk acceptance, no lifecycle state | Creating status by wording | "This PR creates no lifecycle state." | "Risk accepted for production." | High | HOLD | WORM where risk acceptance is formal | Could imply owner decision | Candidate wording review input | Blocking risk boundary notes | Missing "signed off" wording | Check if human owner explicitly accepted risk | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Level 2 / Level 3 | Level 2 implemented, Level 3 ready | Maturity claim | Claiming semi-automation or readiness | Supports future Level 2 preparation only | Treating candidate docs as implementation | "AUTO-6 does not implement Level 2." | "Level 3 ready after AUTO-6." | High | HOLD | WORM where activation/readiness is formal | Could imply automation maturity | Candidate wording review input | Blocking readiness boundary text | Missing "qualified" wording | Check MVP authorization and validation cycles | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| K replacement | K authorization replaced | Authority substitution | Claiming labels, PR body, Guardian, or Tier 2 replace K | K remains separate | Substituting non-K artifacts for K | "Tier 2 comment cannot replace K authorization." | "Labels authorize protected scope changes." | Critical | HOLD | WORM where authority boundary mutates | Could erase human accountability | Candidate wording review input | Blocking K boundary notes | Missing "K implied" wording | Check explicit K scope and head SHA | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Sovereign / authority | Sovereign routing enabled, production authority | Authority mutation claim | Claiming routing or authority is enabled | Sovereign routing remains HOLD | Enabling authority by document wording | "Sovereign index remains routing_enabled: false." | "Sovereign routing enabled." | Critical | HOLD | WORM REQUIRED where boundary mutated | Could create company-level authority | Candidate wording review input | Blocking Sovereign boundary text | Missing "arbiter active" wording | Check Sovereign index and authority evidence | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Safe-managed / counts | safe-managed activation, activation denominator | Count authority claim | Treating count as activation denominator | Documentary count only | Count used as approval/authorization | "`150` is documentary Markdown count only." | "`150` is activation denominator." | High | HOLD | WORM where activation authority affected | Could imply safe-managed production use | Candidate wording review input | Blocking count model disclaimers | Missing "active count" wording | Check safe-managed source separately | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Rename / replacement | pace-ai renamed, repo-wide replacement completed | Identity mutation claim | Claiming rename executed | Rename remains HOLD | Silent historical rewrite or rename execution | "No `pace-ai` to `PAEX-GOS` rename executed." | "`pace-ai` renamed to `PAEX-GOS`." | High | HOLD | WORM where authority/identity boundary mutates | Could imply brand/system migration | Candidate wording review input | Blocking rename boundary notes | Missing "now PAEX-GOS" wording | Check diff and explicit rename scope | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Evidence model / backend | evidence validation model established, backend implemented | Model/backend establishment claim | Claiming backend or model is established | Future model remains HOLD | Creating backend authority by prose | "Evidence validation model remains HOLD." | "Evidence validation model established." | High | HOLD | WORM where evidence model is formal | Could imply enforcement model | Candidate wording review input | Blocking future dependency text | Missing "validator ready" wording | Check executable/backend artifacts and authority | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |

These entries are examples only and candidate-only.

## 8. Approval / Authorization Wording

Candidate high-risk approval and authorization terms include `approved`, `authorized`, `accepted`, `approval authority`, `execution authorization`, and `activation authorization`.

Allowed contexts include negative statements, future dependency statements, K-required boundaries, and HOLD statements.

Prohibited contexts include current approval claims, current authorization claims, and any wording that treats a reviewer note, PR body, label, or Tier 2 PR-linked evidence as K authorization.

K authorization remains separate. Path inventory and wording dictionary cannot create K authorization. Labels alone cannot replace K authorization. PR body cannot replace K authorization. Guardian Review cannot replace K authorization. Tier 2 comment cannot replace K authorization.

Future protected scope mutations require separate scope, review, K authorization, and WORM assessment where applicable.

## 9. Canonicalization Wording

Candidate high-risk canonicalization terms include `canonical`, `stable`, `adopted`, `selected`, `final`, `standard`, `approved standard`, and `canonical convention`.

Candidate briefs must not imply canonical registry, canonical dictionary, canonical convention, final standard, approved standard, or adopted rule unless separately authorized and WORM-assessed where applicable.

Allowed contexts include `not canonical`, `candidate-only`, `future canonicalization remains HOLD`, and risk analysis. Prohibited contexts include any statement that treats this brief as a current canonical governance dictionary or final rule source.

## 10. Implementation / Activation / Enablement Wording

Candidate high-risk implementation and activation terms include `implemented`, `enabled`, `activated`, `active`, `executable`, `operational`, and `deployed`.

AUTO-6 does not implement PR Guard. AUTO-6 does not activate checks. AUTO-6 does not create executable validation logic. AUTO-6 does not create scripts. AUTO-6 does not create workflow files. AUTO-6 does not enable automation.

Allowed contexts are negative, candidate-only, future-only, and HOLD contexts. Positive current-state claims require HOLD unless separately scoped, reviewed, authorized, and evidenced.

## 11. Workflow / Automation / PR Guard Wording

High-risk wording includes GitHub Actions, workflow, automation, PR Guard, guard script, validation script, command parser, IssueOps, Codex automation, and auto-merge.

All workflow / automation / PR Guard wording in AUTO-6 remains candidate-only or boundary-only.

GitHub Actions workflow creation, workflow modification, PR Guard implementation, guard script creation, validation script creation, command parser implementation, IssueOps command activation, Codex automation activation, and PR auto-merge remain HOLD unless separately authorized.

## 12. WORM / Formal Evidence Wording

High-risk wording includes WORM record, WORM REQUIRED, formal approval evidence, audit evidence, evidence validation model, canonical schema, and schema mutation.

AUTO-6 is WORM NOT REQUIRED.

Future formal evidence creation remains HOLD and WORM REQUIRED where applicable.

Future WORM record creation remains HOLD and WORM REQUIRED where applicable.

Future evidence validation model remains HOLD and WORM REQUIRED where applicable.

WORM REQUIRED future-action wording must not be interpreted as WORM record creation.

## 13. Production / Go-live / Authority Wording

High-risk wording includes production-ready, go-live, deployed, operational, runtime, production authority, final go/no-go, risk acceptance, and lifecycle state.

AUTO-6 does not create production deployment, runtime automation, operations readiness, risk acceptance, lifecycle state, final go/no-go, or production authority.

Future production use remains HOLD.

## 14. Level 2 / Level 3 Wording

AUTO-6 supports future PR Guard / Level 2 preparation only.

AUTO-6 does not implement Level 2.

AUTO-6 does not activate IssueOps.

AUTO-6 does not qualify the system for Level 3.

Level 3 remains HOLD until Level 2 MVP is separately authorized, implemented, tested, and passes 3-5 low-risk PR validation cycles.

## 15. K Authorization Boundary

Wording dictionary cannot create K authorization.

Wording dictionary cannot replace K authorization.

Wording dictionary cannot authorize future mutations.

Wording dictionary cannot authorize protected scope changes.

Labels alone cannot replace K authorization.

PR body cannot replace K authorization.

Guardian Review cannot replace K authorization.

Tier 2 PR-linked evidence cannot replace K authorization.

Future protected scope mutations require separate scope, review, K authorization, and WORM assessment where applicable.

## 16. Count Model Wording

If this PR is merged, physical `agents/**/*.md` count may increase from `149` to `150`.

`150` is documentary Markdown count only.

`150` is not:

- safe-managed count
- agent-like count
- activation denominator
- approval
- authorization
- canonical protected scope registry
- canonical wording dictionary
- machine-enforced rule set
- runtime config
- PR Guard input file
- workflow input file
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

safe-managed total remains `53`.

`183` remains NOT OBSERVED unless directly verified from repository evidence.

## 17. Rename / Repo-wide Replacement Wording

Candidate high-risk rename wording includes `pace-ai` to `PAEX-GOS` rename, repo-wide replacement, historical reference rewrite, silent rename, and migration complete.

No `pace-ai` to `PAEX-GOS` rename is executed.

No repo-wide text replacement is executed.

Historical references are not silently rewritten.

Future rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 18. False Positive / False Negative Risks

False positive risks include:

- blocking a harmless negative statement like `not approved`
- blocking a boundary statement like `production authority remains HOLD`
- blocking a WORM future-action note
- blocking a candidate-only example
- blocking an audit-style risk description

False negative risks include:

- positive implementation claim hidden in vague wording
- approval implied without the word `approved`
- activation implied by `ready` or `enabled`
- production readiness implied by `operational`
- canonicalization implied by `standard`
- rename implied by `now PAEX-GOS`
- WORM creation implied by `sealed` or `recorded`

## 19. Future Reviewer Interpretation Rules

Candidate reviewer rules:

- review context before severity
- distinguish negative from positive assertions
- distinguish candidate proposal from current state
- distinguish future dependency from completed action
- distinguish PR-linked evidence from formal approval evidence
- distinguish K authorization from reviewer notes
- distinguish documentary-only count from activation count
- distinguish readiness discussion from implementation
- distinguish WORM REQUIRED future action from WORM record creation
- distinguish rename discussion from rename execution

These rules are candidate-only and not machine-enforced.

## 20. Future PR Guard Usage Candidate

This brief could inform future PR Guard design by identifying candidate wording categories and candidate interpretation rules.

Future PR Guard may use wording categories as review inputs only after separate authorization.

This brief does not create any executable scan. This brief does not create a machine-readable dictionary. This brief does not create runtime config. This brief does not create a PR Guard input file.

Future implementation remains HOLD.

## 21. WORM REQUIRED Future Action Boundary

Future actions that remain WORM REQUIRED where applicable include:

- canonical forbidden wording dictionary establishment
- canonical protected scope registry establishment
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

## 22. Production Authority Boundary

This brief does not create production deployment.

This brief does not create runtime automation.

This brief does not create operations readiness.

This brief does not create final go/no-go.

This brief does not create production authority.

Future production use remains HOLD.

## 23. Non-decisions

No decision, establishment, or activation is created for:

- canonical forbidden wording dictionary
- canonical governance dictionary
- machine-enforced wording registry
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
- `pace-ai` to `PAEX-GOS` rename
- repo-wide text replacement

## 24. Router Decision

PROCEED only for documentary-only AUTO-6 Forbidden Wording Dictionary Candidate Brief PR creation.

HOLD for canonical forbidden wording dictionary, canonical governance dictionary, machine-enforced wording registry, machine-readable enforcement file, runtime config, PR Guard input file, PR Guard implementation, PR Guard activation, PR Guard check enablement, guard script creation, validation script creation, executable validation logic, GitHub Actions workflow creation, workflow file modification, automation implementation, automation activation, IssueOps command activation, command parser implementation, Codex automation activation, GitHub App installation, GitHub token creation, secret creation, API key creation, webhook creation, PR auto-merge enablement, automatic Codex execution authorization, automatic Guardian approval, automatic Tier 2 approval, formal approval evidence creation, WORM record creation, production deployment, runtime automation enablement, agent activation, safe-managed production use, Sovereign routing enablement, execution authorization, activation authorization, risk acceptance, lifecycle state, production authority, final go/no-go, Level 2 implementation, Level 3 readiness, backend implementation, evidence validation model establishment, canonical convention establishment, schema mutation, README.md / AGENTS.md modification, registry modification, agent file modification, existing AUTO-1 artifact modification, existing AUTO-2 artifact modification, existing AUTO-3 artifact modification, existing AUTO-5 artifact modification, `pace-ai` to `PAEX-GOS` rename, and repo-wide text replacement.

## 25. Wording Discovery Rules

When identifying candidate wording:

- use repository governance context only
- do not claim the dictionary is complete
- do not claim the dictionary is canonical
- do not treat candidate wording as machine-enforced
- do not create machine-readable dictionary files
- do not create JSON / YAML / config / schema output
- mark examples as examples only
- include allowed contexts and prohibited contexts
- emphasize reviewer interpretation
- avoid automatic single-word conviction logic
- preserve K authorization as separate and non-replaceable
