---
title: "AUTO-5｜Protected Scope Path Inventory Candidate Brief"
status: "candidate_brief"
mode: "documentary_only"
risk_level: "high"
business_context_layer: "Enterprise Governance / Repository Governance / Automation Governance / PR Guard Protected Scope Inventory"
caep_mapping: "G｜Governance"
worm_required: false
worm_required_scope: "future_canonical_path_registry_pr_guard_implementation_workflow_creation_validation_script_automation_activation_authority_or_production_use_only"
canonical: false
path_inventory_canonical: false
machine_enforced_registry: false
machine_readable_enforcement_file_created: false
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
created_from_baseline: "4aaa8bb4c478d26b457d7a66dc91fbc335919350"
auto_1_reference: "agents/governance/agent-intake-pipeline/option-auto-1-paex-issueops-orchestrator-automation-candidate-brief.md"
auto_2_reference: "agents/governance/agent-intake-pipeline/auto-2-read-only-issueops-command-design-candidate-brief.md"
auto_3_reference: "agents/governance/agent-intake-pipeline/auto-3-pr-guard-candidate-implementation-plan-validation-design-brief.md"
auto_4_result: "PARTIAL READY / BLOCKED"
safe_managed_total_expected: 53
physical_agents_md_count_before_expected: 148
physical_agents_md_count_after_expected_if_merged: 149
sovereign_index_expected: "routing_enabled: false"
---

# AUTO-5｜Protected Scope Path Inventory Candidate Brief

## 1. Document Status

This document is documentary-only, candidate-only, and a protected scope path inventory candidate brief only.

This document is not a canonical protected scope registry, not a machine-enforced path registry, and not a machine-readable enforcement file.

This document is not PR Guard implementation, not PR Guard activation, not PR Guard check enablement, not validation script creation, not GitHub Actions workflow creation, not automation implementation, not automation activation, not IssueOps command activation, not command parser implementation, not Codex automation activation, not PR auto-merge enablement, not formal approval evidence, not a WORM record, not production authority, and not final go/no-go.

The path inventory is candidate-only. It is not approved, stable, canonical, authoritative, operational, executable, machine-enforced, or final.

## 2. AUTO-1 / AUTO-2 / AUTO-3 / AUTO-4 Baseline

AUTO-1 established candidate IssueOps Orchestrator architecture.

AUTO-2 defined future `/paex` command semantics.

AUTO-3 designed the future PR Guard check matrix.

AUTO-4 returned `PARTIAL READY / BLOCKED` because exact machine-ready protected scope path inventory and related path boundaries remain incomplete.

AUTO-5 creates a candidate path inventory brief only. AUTO-5 does not implement PR Guard, does not create a canonical registry, and does not modify AUTO-1 / AUTO-2 / AUTO-3 artifacts.

Current baseline:

- latest main expected: `4aaa8bb4c478d26b457d7a66dc91fbc335919350`
- physical `agents/**/*.md` before AUTO-5: `148`
- expected physical `agents/**/*.md` after merge if accepted: `149`
- safe-managed total: `53`
- Sovereign index: `routing_enabled: false`
- `183`: NOT OBSERVED unless directly verified from repository evidence

These baseline values are repository-count context only. They do not create path registry authority, automation authority, formal approval evidence, WORM evidence, production authority, or go/no-go.

## 3. Why Protected Scope Path Inventory Is Needed

AUTO-3 defines what categories future PR Guard should check. AUTO-4 confirmed that path inventory is not machine-ready.

Future PR Guard cannot safely validate protected scopes without explicit path boundaries. Missing path inventory creates false negative risks where protected files are changed outside known paths. Overbroad path inventory creates false positive risks where legitimate documentary-only work is blocked by category overreach.

Path inventory must remain candidate-only until separately reviewed, canonicalized, and authorized where applicable.

## 4. Path Inventory Purpose

AUTO-5 collects candidate protected paths, documents candidate path boundaries, identifies path ambiguity, identifies false positive / false negative risks, prepares future PR Guard inputs, supports future path inventory review, and supports future machine-check design.

This brief is not canonical, not approved, not machine-enforced, not executable, not workflow input, not PR Guard runtime config, and not a final path registry.

## 5. Candidate Path Inventory Categories

Future path inventory categories include:

- protected scope root paths
- Batch A target path candidates
- Batch B target path candidates
- Batch C target path candidates
- Phase 5 artifact path candidates
- AUTO artifact path candidates
- registry path boundary
- agent file path boundary
- Sovereign index path
- canonical WORM Event Schema path
- WORM records path boundary
- audit evidence path boundary
- formal approval evidence path boundary
- `README.md` boundary
- `AGENTS.md` boundary
- `.github/workflows` boundary
- scripts boundary
- validation scripts boundary
- config files boundary
- schema files boundary
- secrets / tokens / API keys / webhooks boundary
- deployment files boundary
- documentary-only allowed path candidates

Every category remains candidate-only.

## 6. Candidate Path Inventory Matrix

| Category | Candidate Path / Boundary | Path Type | Protection Level | Allowed Action | Prohibited Action | Mutation Rule | WORM Impact | Authority Impact | Future PR Guard Usage | Ambiguity Risk | False Positive Risk | False Negative Risk | Required Evidence Source | Current Router State |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Protected scope roots | `agents/agent-registry/`, `agents/sovereign/`, `agents/governance/worm-event-schema/`, `agents/governance/formal-approval-evidence/`, `agents/governance/worm-activation-records/`, `.github/workflows/`, `README.md`, `AGENTS.md` | mixed | High/Critical | Read-only reference or separately scoped change | Unscoped mutation | HOLD unless scoped, reviewed, K-authorized | WORM where authority/evidence/schema affected | High | Candidate path guard | broad roots may overmatch | documentary refs may be blocked | moved protected files may be missed | repository tree and governance docs | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Batch A targets | `agents/governance/agent-intake-pipeline/batch-a-*` candidate files | glob candidate | High | Read-only reference | Unscoped mutation | HOLD unless scoped | WORM depends on mutation | Medium/High | Candidate batch guard | exact target list incomplete | broad glob may block notes | non-prefix targets missed | Batch A docs | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Batch B targets | `agents/governance/agent-intake-pipeline/batch-b-*` candidate files | glob candidate | High | Read-only reference | Unscoped mutation | HOLD unless scoped | WORM depends on mutation | Medium/High | Candidate batch guard | exact target list incomplete | broad glob may block notes | non-prefix targets missed | Batch B docs | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Batch C targets | `agents/governance/agent-intake-pipeline/batch-c-*` candidate files | glob candidate | High | Read-only reference | Unscoped mutation | HOLD unless scoped | WORM depends on mutation | Medium/High | Candidate batch guard | exact target list incomplete | broad glob may block notes | non-prefix targets missed | Batch C docs | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Phase 5 artifacts | `agents/governance/agent-intake-pipeline/phase-5-*` | glob candidate | High | Read-only reference | Unscoped mutation | HOLD unless separately scoped | WORM where WORM/decision/evidence affected | High | Candidate Phase 5 guard | full scope broad | candidate briefs may be blocked | non-prefix artifacts missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| AUTO artifacts | AUTO-1 / AUTO-2 / AUTO-3 exact files and AUTO-5 target | exact files | High | Add AUTO-5 target only in this PR | Existing AUTO mutation | HOLD unless scoped | WORM where authority/automation affected | High | Candidate AUTO guard | future AUTO list changes | new AUTO brief could be blocked | old AUTO file outside list missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Registry boundary | `agents/agent-registry/` | directory | High | Read-only reference | Registry mutation | HOLD unless scoped and K-authorized | WORM where registry/authority changes | High | Candidate registry guard | directory broad | documentation refs blocked | registry file moved elsewhere | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Agent files | `agents/**/*.md` | glob candidate | Medium/High | Count/read-only reference | Treating count as activation | HOLD for unscoped mutation | WORM where activation/authority affected | High | Count and mutation guard | documentary vs agent-like ambiguity | documentary file blocked as agent | agent-like file missed by non-md | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Sovereign index | `agents/sovereign/governance-protocols-index/governance-protocols-index.md` | exact file | Critical | Verify `routing_enabled: false` | Routing mutation | HOLD unless explicitly K-authorized | WORM REQUIRED where boundary mutated | Critical | Candidate Sovereign guard | exact path may change | refs blocked | moved index missed | repository tree and file content | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| WORM schema | `agents/governance/worm-event-schema/worm-event-schema.md` | exact file | Critical | Read-only reference | Schema mutation | HOLD and WORM REQUIRED where applicable | WORM REQUIRED | Critical | Candidate schema guard | exact path may change | refs blocked | alternate schema missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| WORM records | `agents/governance/worm-activation-records/` | directory | Critical | Read-only reference | WORM record creation/mutation | HOLD and WORM REQUIRED where applicable | WORM REQUIRED | Critical | Candidate record guard | records may exist elsewhere | drafts blocked | external record path missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Audit evidence | `agents/governance/guardian-review-records/`, `agents/guardian/compliance/audit-readiness/` | directory | High/Critical | Read-only reference | Evidence mutation | HOLD unless scoped | WORM may apply | High | Candidate evidence guard | mixed evidence purpose | refs blocked | audit evidence elsewhere missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Formal approval evidence | `agents/governance/formal-approval-evidence/` | directory | Critical | Read-only reference | Formal evidence creation/mutation | HOLD and WORM REQUIRED where applicable | WORM REQUIRED | Critical | Candidate formal evidence guard | templates vs records mixed | templates blocked | formal evidence elsewhere missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| README boundary | `README.md` | exact file | High | Read-only reference | Unscoped edit | HOLD unless scoped/reviewed/K-authorized | WORM where high-risk governance changed | High | Candidate top-level doc guard | root only | doc update blocked | nested README missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| AGENTS boundary | `AGENTS.md` | exact file | Critical | Read-only reference | Global instruction mutation | HOLD unless scoped/reviewed/K-authorized | WORM REQUIRED where activation/policy affected | Critical | Candidate instruction guard | root only | instruction refs blocked | nested AGENTS missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Workflow boundary | `.github/workflows/` | directory candidate, NOT OBSERVED in current tree | Critical | None unless separately authorized | Workflow creation/modification | HOLD | WORM where approval/WORM/production evidence controlled | Critical | Candidate workflow guard | absent dir | future authorized workflow blocked | workflow-like file elsewhere missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Scripts boundary | `scripts/`, `tools/`, `bin/` candidates, NOT OBSERVED in root | directory candidates | High | None unless separately authorized | Script creation/mutation | HOLD | WORM where evidence workflow controlled | High | Candidate script guard | absent dirs | docs blocked if names overlap | scripts elsewhere missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Config/schema boundary | `.github/`, YAML files, JSON files, schema directories, `agents/agent-registry/frontmatter-schema/`, `agents/governance/worm-event-schema/` | mixed | High/Critical | Read-only reference | Config/schema creation/mutation | HOLD unless scoped | WORM for canonical schema mutation | High/Critical | Candidate config/schema guard | broad extensions | harmless data blocked | uncommon config missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Secrets/tokens/webhooks | no repo storage allowed; `.env`, token, key, secret, webhook indicators | content/path risk | Critical | None | Secret-bearing artifact creation | HOLD | WORM/security review may apply | Critical | Candidate secret guard | content detection hard | false secret matches | disguised secrets missed | repository scan rules needed | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Deployment files | deploy/deployment dirs NOT OBSERVED in root | directory candidates | High/Critical | None unless scoped | Deployment config creation | HOLD | WORM where production affected | Critical | Candidate deployment guard | absent dirs | docs blocked if named deploy | deployment config elsewhere missed | repository tree | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |
| Documentary-only allowed path | `agents/governance/agent-intake-pipeline/auto-5-protected-scope-path-inventory-candidate-brief.md` for this PR only | exact file | High | One new Markdown brief | Existing file mutation/executable creation | HOLD if scope expands | Not WORM for this brief only | No authority | Candidate allowed target guard | single-use path | future briefs blocked | wrong path accepted if vague | K authorization and PR diff | CANDIDATE ONLY / NOT CANONICAL / NOT MACHINE-ENFORCED / HOLD FOR IMPLEMENTATION |

## 7. Protected Scope Root Paths

Candidate protected root paths and boundaries:

- `agents/agent-registry/` — directory; candidate protected registry boundary; requires further verification before canonical completeness.
- `agents/sovereign/` — directory; candidate Sovereign boundary; exact routing index path is separately listed below.
- `agents/governance/worm-event-schema/worm-event-schema.md` — exact file; canonical WORM Event Schema candidate boundary.
- `agents/governance/worm-activation-records/` — directory; WORM record / draft boundary candidate.
- `agents/governance/formal-approval-evidence/` — directory; formal approval evidence boundary candidate.
- `agents/governance/guardian-review-records/` — directory; audit / review evidence boundary candidate.
- `README.md` — exact file; top-level documentation boundary.
- `AGENTS.md` — exact file; repository instruction boundary.
- `.github/workflows/` — directory candidate; NOT OBSERVED in current repository tree.
- `scripts/`, `tools/`, `bin/` — directory candidates; NOT OBSERVED at repository root during AUTO-5 discovery.

This list is candidate-only and not canonical completeness.

## 8. Batch A / Batch B / Batch C Target Path Candidates

Batch A candidate evidence is directly observed under `agents/governance/agent-intake-pipeline/` with `batch-a-*` files:

- `batch-a-documentation-only-clarification-brief.md`
- `batch-a-recommendation-only-repair-scope-brief.md`
- `batch-a-recommendation-only-repair-scope-candidate-brief.md`
- `batch-a-repair-decision-gate-brief.md`
- `batch-a-target-specific-pre-mutation-analysis-findings-report.md`
- `batch-a-target-specific-pre-mutation-analysis-plan.md`

Batch B candidate evidence is directly observed under `agents/governance/agent-intake-pipeline/` with `batch-b-*` files:

- `batch-b-documentation-only-clarification-brief.md`
- `batch-b-guardian-risk-candidate-read-only-analysis-findings-report.md`
- `batch-b-recommendation-only-repair-scope-brief.md`
- `batch-b-recommendation-only-repair-scope-candidate-brief.md`
- `batch-b-repair-decision-gate-brief.md`

Batch C candidate evidence is directly observed under `agents/governance/agent-intake-pipeline/` with `batch-c-*` files:

- `batch-c-documentation-only-clarification-brief.md`
- `batch-c-governance-sensitive-candidates-read-only-analysis-findings-report.md`
- `batch-c-recommendation-only-repair-scope-brief.md`
- `batch-c-recommendation-only-repair-scope-candidate-brief.md`
- `batch-c-repair-decision-gate-brief.md`

These are candidate paths only. The exact Batch A / B / C target path inventory remains PARTIAL / REQUIRES VERIFICATION because these documents may describe targets not fully represented by filename prefix.

## 9. Existing Phase 5 Artifact Path Candidates

Directly observed Phase 5 artifact candidates under `agents/governance/agent-intake-pipeline/` include:

- `phase-5-1a-translation-localization-metadata-repair-closing-note.md`
- `phase-5-1b-document-generator-metadata-repair-closing-note.md`
- `phase-5-2-scope-discovery-closing-note.md`
- `phase-5-3-candidate-target-discovery-report.md`
- `phase-5-3-read-only-planning-package.md`
- `phase-5-3-target-discovery-read-only-package.md`
- `phase-5-4-target-specific-pre-mutation-analysis-decision-brief.md`
- `phase-5-consolidated-readiness-revalidation-brief.md`
- `phase-5-entry-decision-gate-plan.md`
- `phase-5-execution-authorization-intake-plan.md`
- `phase-5-execution-scope-candidate-report.md`
- `phase-5-final-go-no-go-package-planning-brief.md`
- `phase-5-final-go-no-go-worm-record-creation-candidate-brief.md`
- `phase-5-formal-approval-evidence-path-candidate-brief.md`
- `phase-5-partial-summary-closing-note.md`
- `phase-5-readiness-boundary-note.md`
- `phase-5-readiness-revalidation-note.md`
- `phase-5-scope-selection-decision-brief.md`
- `phase-5-stale-count-annotation-closure-note.md`
- `phase-5-stale-count-classification-table.md`
- `phase-5-worm-evidence-storage-sealing-convention-scope-brief.md`
- `phase-5-worm-external-trusted-timestamp-authority-candidate-comparison.md`
- `phase-5-worm-model-establishment-blocker-resolution-decision-input-matrix-candidate-brief.md`
- `phase-5-worm-timestamp-hash-merkle-sealing-backend-model-candidate-brief.md`
- `phase-5-worm-timestamp-hash-normalization-candidate-brief.md`
- `phase-5-worm-timestamp-source-trust-candidate-brief.md`

The full Phase 5 list remains PARTIAL because this brief does not perform canonical registry reconciliation. Do not modify Phase 5 artifacts. Do not treat this list as canonical.

## 10. Existing AUTO Artifact Paths

Directly verifiable AUTO artifact paths:

- AUTO-1: `agents/governance/agent-intake-pipeline/option-auto-1-paex-issueops-orchestrator-automation-candidate-brief.md`
- AUTO-2: `agents/governance/agent-intake-pipeline/auto-2-read-only-issueops-command-design-candidate-brief.md`
- AUTO-3: `agents/governance/agent-intake-pipeline/auto-3-pr-guard-candidate-implementation-plan-validation-design-brief.md`
- AUTO-5 target: `agents/governance/agent-intake-pipeline/auto-5-protected-scope-path-inventory-candidate-brief.md`

AUTO-5 target is allowed only as this new documentary-only candidate brief. Existing AUTO-1 / AUTO-2 / AUTO-3 artifacts remain HOLD for mutation unless separately scoped, reviewed, and K-authorized.

## 11. Registry Path Boundary

Directly verifiable candidate registry boundary:

- `agents/agent-registry/`

This directory is a broad candidate boundary and remains PARTIAL for future machine validation until exact protected registry files and permitted read-only references are separately inventoried.

Registry modification remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 12. Agent File Path Boundary

Candidate agent file path boundary:

- `agents/**/*.md`

This path is useful for physical documentary Markdown count only. Physical count is not safe-managed count. Physical count is not activation denominator. Agent-like files are not activation authority.

Agent file modification remains HOLD unless separately scoped and authorized. This brief does not activate agents and does not approve safe-managed production use.

## 13. Sovereign Index Path

Directly verifiable Sovereign index path:

- `agents/sovereign/governance-protocols-index/governance-protocols-index.md`

The Sovereign index must remain:

```yaml
routing_enabled: false
```

Sovereign routing enablement remains HOLD. Sovereign routing mutation requires separate scope, review, K authorization, and WORM assessment where applicable.

## 14. WORM Schema Path

Directly verifiable canonical WORM Event Schema path:

- `agents/governance/worm-event-schema/worm-event-schema.md`

Schema mutation remains HOLD and WORM REQUIRED where applicable. This brief does not modify schema and does not authorize future schema mutation.

## 15. WORM Records Path Boundary

Candidate WORM records path boundary:

- `agents/governance/worm-activation-records/`

Directly observed files include:

- `agents/governance/worm-activation-records/v1-4-active-final-worm-activation-record-draft.md`
- `agents/governance/worm-activation-records/v1-4-lock-candidate-worm-activation-record.md`

This boundary is PARTIAL because WORM-related evidence may exist outside this directory. WORM record creation / mutation remains HOLD and WORM REQUIRED where applicable.

## 16. Audit Evidence Path Boundary

Candidate audit / review evidence boundaries:

- `agents/governance/guardian-review-records/`
- `agents/governance/guardian-review-approvals/`
- `agents/governance/guardian-purity-audit/`
- `agents/guardian/compliance/audit-readiness/`

This boundary is PARTIAL because audit evidence can have mixed purpose and may exist in other governance paths. Audit evidence mutation remains HOLD unless separately scoped, reviewed, and K-authorized where applicable.

## 17. Formal Approval Evidence Path Boundary

Candidate formal approval evidence boundary:

- `agents/governance/formal-approval-evidence/`

Directly observed files include:

- `agents/governance/formal-approval-evidence/v1-4-final-immutable-worm-activation-record.md`
- `agents/governance/formal-approval-evidence/v1-4-formal-guardian-review-approval-record.md`
- `agents/governance/formal-approval-evidence/v1-4-k-ceo-approval-evidence-record.md`
- `agents/governance/formal-approval-evidence/v1-4-k-ceo-approval-evidence-template.md`

Formal approval evidence creation / mutation remains HOLD and WORM REQUIRED where applicable. This brief does not create formal approval evidence.

## 18. README.md / AGENTS.md Boundary

Candidate exact-file boundaries:

- `README.md`
- `AGENTS.md`

Modification remains HOLD unless separately scoped, reviewed, and K-authorized. AGENTS.md modification may require WORM where global instruction policy or activation boundary is affected.

## 19. .github/workflows Boundary

Candidate workflow boundary:

- `.github/workflows/`

This directory is NOT OBSERVED in the current repository tree during AUTO-5 discovery.

Workflow creation remains HOLD. Workflow modification remains HOLD. Workflow self-modification remains HOLD. AUTO-5 does not create workflow files.

## 20. Scripts / Validation Scripts Boundary

Common candidate script boundaries:

- `scripts/` — NOT OBSERVED at repository root during AUTO-5 discovery.
- `tools/` — NOT OBSERVED at repository root during AUTO-5 discovery.
- `bin/` — NOT OBSERVED at repository root during AUTO-5 discovery.

Script / validation script creation remains HOLD. This brief does not create guard scripts, validation scripts, or executable validation logic.

## 21. Config / Schema Boundary

Candidate config / schema boundaries include:

- `.github/` — NOT OBSERVED in current repository tree.
- YAML files — file-extension risk boundary, not a canonical path.
- JSON files — file-extension risk boundary, not a canonical path.
- `agents/agent-registry/frontmatter-schema/` — candidate registry schema boundary if present under registry.
- `agents/governance/worm-event-schema/` — directly observed WORM schema boundary.

This brief creates no schemas, no JSON schema files, no YAML schema files, and no config files. Config / schema mutation remains HOLD unless separately scoped, reviewed, and K-authorized where applicable.

## 22. Secrets / Tokens / API Keys / Webhooks Boundary

Candidate secret-bearing risk boundaries include path or content indicators such as `.env`, `secret`, `token`, `api_key`, `apikey`, `webhook`, credential material, and integration configuration.

Secrets must not be stored in the repository. Tokens must not be created. API keys must not be created. Webhook configs must not be created. Secret-bearing artifact creation remains HOLD.

This brief creates no secrets, tokens, API keys, or webhooks.

## 23. Deployment Files Boundary

Deployment file boundary candidates such as `deploy/`, `deployment/`, deployment configs, production environment configs, release scripts, and infrastructure files are NOT OBSERVED as root-level deployment directories during AUTO-5 discovery.

This boundary remains PARTIAL because deployment-like files may use uncommon names or locations. Production deployment remains HOLD.

## 24. Documentary-only Allowed Target Path Rules

Candidate documentary-only target rules:

- allowed only when explicitly K-authorized
- one new Markdown candidate brief only unless separately scoped
- must be under allowed governance intake path
- must not modify existing artifacts
- must not create executable files
- must not create workflows
- must not create configs or schemas
- must not create formal evidence
- must not create WORM records

These are candidate rules, not canonical enforcement.

## 25. Future Machine-check Input Format Candidate

Future non-executable candidate input fields may include:

| Field | Candidate Meaning |
|---|---|
| category | Protected category label. |
| candidate path | Candidate path or path boundary. |
| match type | Exact path, directory, glob candidate, or conceptual boundary. |
| protection level | Medium, High, Critical candidate rating. |
| allowed mutation | Candidate allowed action if separately scoped. |
| prohibited mutation | Candidate prohibited action. |
| WORM impact | Future WORM REQUIRED implication where applicable. |
| authority impact | Authority boundary implication. |
| evidence source | Repository evidence source supporting the path. |
| ambiguity status | VERIFIED, PARTIAL, MISSING EVIDENCE, NOT OBSERVED, or REQUIRES VERIFICATION. |
| router state | Candidate router state. |

This is prose/table design only. This brief creates no JSON, YAML, config, schema, or machine-readable enforcement file.

## 26. Path Matching Ambiguity Risks

Path matching risks include exact path versus directory ambiguity, glob overreach, glob underreach, renamed files, moved files, generated files, hidden config files, case sensitivity, symlinks if present, Markdown files that look like agents but are documentary-only, and evidence directories with mixed purpose.

These risks must be resolved before any machine-enforced path registry or PR Guard runtime config is considered.

## 27. False Positive / False Negative Risks

False positive examples:

- legitimate documentary-only brief blocked by broad agent path rule
- harmless Markdown file blocked as agent activation
- evidence read-only reference blocked as mutation

False negative examples:

- protected file modified outside expected path
- workflow-like file added outside `.github/workflows`
- secret-bearing config added with uncommon extension
- WORM-related evidence created outside known WORM path
- production authority wording inserted in non-obvious file

## 28. WORM REQUIRED Future Action Boundary

Future actions remain WORM REQUIRED where applicable, including:

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

## 29. Production Authority Boundary

This brief does not create production deployment, runtime automation, operations readiness, final go/no-go, or production authority.

Future production use remains HOLD and requires separately scoped development, testing, security, deployment, evidence, WORM, authority, and K authorization gates.

## 30. Count Model Boundary

If this PR is merged, physical `agents/**/*.md` count may increase from `148` to `149`.

`149` is documentary Markdown count only.

`149` is not:

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
- canonical path registry

The safe-managed total remains `53`.

`183` remains NOT OBSERVED unless directly verified from repository evidence.

## 31. Non-decisions

This brief makes no decision and creates no establishment or activation for:

- canonical protected scope registry
- machine-enforced path registry
- machine-readable enforcement file
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
- `pace-ai` to `PAEX-GOS` rename
- repo-wide text replacement

## 32. Rename Boundary

No `pace-ai` to `PAEX-GOS` rename executed. No repo-wide text replacement executed. Historical references are not silently rewritten.

Future rename remains HOLD unless separately scoped, reviewed, K-authorized, and WORM-assessed where applicable.

## 33. Router Decision

PROCEED only for documentary-only AUTO-5 Protected Scope Path Inventory Candidate Brief PR creation.

HOLD for canonical protected scope registry, machine-enforced path registry, machine-readable enforcement file, PR Guard implementation, PR Guard activation, PR Guard check enablement, guard script creation, validation script creation, executable validation logic, GitHub Actions workflow creation, workflow file modification, automation implementation, automation activation, IssueOps command activation, command parser implementation, Codex automation activation, GitHub App installation, GitHub token creation, secret creation, API key creation, webhook creation, PR auto-merge enablement, automatic Codex execution authorization, automatic Guardian approval, automatic Tier 2 approval, formal approval evidence creation, WORM record creation, production deployment, runtime automation enablement, agent activation, safe-managed production use, Sovereign routing enablement, execution authorization, activation authorization, risk acceptance, lifecycle state, production authority, final go/no-go, backend implementation, evidence validation model establishment, canonical convention establishment, schema mutation, README.md / AGENTS.md modification, registry modification, agent file modification, existing AUTO-1 artifact modification, existing AUTO-2 artifact modification, existing AUTO-3 artifact modification, `pace-ai` to `PAEX-GOS` rename, and repo-wide text replacement.
