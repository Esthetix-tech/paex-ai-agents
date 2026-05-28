---
name: agents-readme
title: PAEX-AI Agents Repository README
description: Root-level architecture and governance guide for the PAEX-AI agents repository, defining repository purpose, Business Architecture Context Stack, C-A-E-P agent layers, routing principles, frontmatter discipline, risk classification, secondary hooks, quarantine policy, PR / CI validation and v1.4 activation rules.
layer: governance
context_layer: Repository Governance
pace_layer: Repository Governance / Global Overview
risk_level: high
status: active_candidate
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - readme_activation
  - repository_governance_baseline_change
  - v1_4_activation
  - architecture_layer_change
  - routing_policy_reference_change
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
requires_worm: true
worm_scope:
  - readme_activation
  - repository_governance_baseline_change
  - v1_4_activation
  - architecture_layer_change
  - routing_policy_reference_change
requires_guardian_review: true
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - treat_readme_as_execution_agent
  - use_readme_to_override_agent_router
  - activate_repository_without_companion_files
  - route_quarantined_files_as_active
  - bypass_frontmatter_schema
  - bypass_risk_level_map
  - bypass_secondary_hooks_map
  - bypass_pr_ci_validation_checklist
allowed_actions:
  - explain_repository_structure
  - summarize_governance_baseline
  - reference_canonical_registry_files
  - guide_repository_onboarding
  - identify_governance_dependency
  - require_ci_validation_for_activation
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - markdown_structure_check
  - companion_governance_files_check
  - ci_validation_result
  - guardian_review_record
  - worm_activation_record
  - human_approval_record
rollback_required: true
canary_required: false
related_files:
  - AGENTS.md
  - AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - agents/agent-registry/frontmatter-schema/frontmatter-schema.md
  - agents/agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
  - agents/agent-registry/agent-router/agent-router.md
  - agents/agent-registry/risk-level-map/risk-level-map.md
  - agents/agent-registry/secondary-hooks-map/secondary-hooks-map.md
  - agents/governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - agents/governance/worm-event-schema/worm-event-schema.md
  - agents/sovereign/governance-protocols-index/governance-protocols-index.md
  - agents/_quarantine/quarantine-policy/quarantine-policy.md
exemption_reason: repository_readme_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_documentation_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

This README may be indexed as a governance overview file, but it must not be routed as an execution Agent.

# PAEX-AI Agents Repository

## 1. Purpose

The `agents/` repository is the formal operating library for the PAEX-AI Enterprise Governance OS.

It stores and governs:

- Agent role specifications;
- Business Architecture Context Stack files;
- C-A-E-P governance layer definitions;
- routing maps;
- frontmatter schema;
- risk-level maps;
- secondary hooks;
- registry controls;
- core strategy agents;
- mission execution agents;
- guardian review agents;
- platform support agents;
- sovereign decision artifacts;
- shared reusable materials;
- quarantine rules;
- PR / CI validation rules;
- production-readiness and governance protocols.

This repository is not just a folder of prompts.

It is a governed operating structure that defines:

- which Agents exist;
- what each Agent owns;
- what each Agent must not own;
- which business context layer each file belongs to;
- which PAEX-AI authority layer each Agent belongs to;
- what risk level each Agent carries;
- which tasks may be routed to each Agent;
- which tasks must not be routed to each Agent;
- which Guardian, WORM, Canary, Kill Switch, Human Override or Sovereign controls must be attached;
- which files are safe for active routing;
- which files are only references;
- which files must remain isolated until repaired;
- which actions require human approval;
- which decisions must be escalated.

Core rule:

> The `agents/` repository is an authority system.  
> Every file must have a clear identity, boundary, owner, risk level, routing status and governance relationship.

Plain-language interpretation:

> 這不是 prompt 倉庫。  
> 這是 Esthetix / PAEX-AI 的 Agent 作戰編制表、權限地圖、風險控管台與治理黑盒子。

---

## 1.1 What This Repository Is

This repository is the source of truth for how Codex, coding agents, repository agents, automation agents, governance agents and Agent Engine support agents operate inside Esthetix / ESTRIX / PAEX-AI.

It answers:

| Question | Repository Answer |
|---|---|
| What is this Agent allowed to do? | Defined by frontmatter, layer, tool permissions and routing rules |
| Which layer does this file belong to? | Defined by Business Architecture Context Stack and repository path |
| Can this file be routed as an execution target? | Defined by `routing_enabled` and status |
| Is this file only metadata or governance reference? | Defined by `registry_enabled`, `tool_permissions` and layer |
| What risk level applies? | Defined by `risk-level-map.md` |
| Which hooks must be attached? | Defined by `secondary-hooks-map.md` |
| Who reviews risky actions? | Defined by Guardian, Governance and Sovereign protocols |
| What happens to unsafe files? | Defined by `quarantine-policy.md` |
| What must pass before v1.4 activation? | Defined by `pr-ci-validation-checklist.md` |

---

## 1.2 What This Repository Is Not

This repository is not:

- a casual prompt collection;
- a random Agent library;
- a place to give Agents unlimited autonomy;
- a substitute for legal, finance, security, privacy or compliance sign-off;
- a way to bypass K / CEO final decision authority;
- a production execution system by itself;
- a replacement for tests, CI, logs, WORM records or human accountability;
- a shortcut around Guardian Review;
- a place where application-specific logic may silently redefine ESTRIX Core.

Core rule:

> A capable Agent is not automatically an authorized Agent.

Plain-language interpretation:

> 會做，不代表可以做。  
> 可以做，也不代表可以自己審自己。

---

## 2. Operating Doctrine

The repository follows the PAEX-AI governance doctrine.

```text
Classify before routing.
Route before execution.
Hook before high-risk action.
Record before release.
Canary before scale.
Human decision before irreversible action.
Evidence before completion.
Reusable core before application duplication.
Company-wide interest before local optimization.
```

## 3. Business Architecture Context Stack

The Business Architecture Context Stack classifies every Esthetix / ESTRIX / SHINES / SoMatch request into L0 to L4 before routing, implementation, documentation, refactoring or execution.

The purpose of this stack is to prevent Codex and repository agents from mixing company-level strategy, reusable core engine logic, application-specific packaging and one-time project delivery.

The canonical rule is `AGENTS_BUSINESS_ARCHITECTURE_RULE.md`.

```text
L0｜K Command Layer
L1｜Esthetix Arsenal Layer
L2｜ESTRIX Core Engine Layer
L3｜Application / Use Case Layer
L4｜Engagement / Project Layer
```

### 3.1 L0｜K Command Layer

L0 contains K / CEO final decision authority, company-level principles, non-delegable decisions, business model direction and irreversible company-level approval boundaries.

Use L0 when a task involves company positioning, ownership relationships, external business model activation, high-risk partnership decisions, public positioning changes or final executive approval.

Codex may prepare analysis, options, risk maps and decision packages for L0 work. Codex must not replace K / CEO final decision authority.

### 3.2 L1｜Esthetix Arsenal Layer

L1 defines Esthetix as the arsenal, R&D company and enterprise AI / SaaS engine builder.

Use L1 when a task involves Esthetix company strategy, PAEX-AI governance, Agent Engine operations, enterprise infrastructure, data governance, internal control, audit architecture or reusable AI operating capability.

Esthetix must not be reduced to SoMatch, SHINES, a beauty-only company or a one-time service operation.

### 3.3 L2｜ESTRIX Core Engine Layer

L2 defines ESTRIX as the reusable core operating engine built by Esthetix.

Use L2 when a task involves reusable capabilities such as CRM, booking, scheduling, billing, dashboard, notification, permission, audit log, workflow automation, reusable schema, reusable state machine, API design or Agent workflow logic.

ESTRIX is not SHINES-specific, not SoMatch-specific and not beauty-industry-specific.

### 3.4 L3｜Application / Use Case Layer

L3 defines specific applications, brands, service models, industry scenarios or use-case configurations powered by ESTRIX.

Use L3 when a task involves SHINES field workflows, SoMatch service packaging, customer-facing language, industry-specific SOPs, application-level onboarding, use-case-specific templates or brand voice.

L3 may configure and package ESTRIX Core capabilities. L3 must not redefine ESTRIX Core.

### 3.5 L4｜Engagement / Project Layer

L4 defines one-time projects, client tasks, sprints, campaigns, MVP drafts, monthly reports, proposals, implementation checklists or temporary delivery artifacts.

Use L4 when the work is client-specific, version-specific, time-bound or non-reusable.

If an L4 deliverable reveals a reusable pattern, Codex should propose promotion to L3, L2, L1, shared templates, registry rules or governance protocols. Codex must not silently promote L4 work into L2 Core.

### 3.6 Context Stack HOLD Rule

Return `HOLD` when the correct business context layer is unclear, when a requirement may belong to both L2 and L3, when a one-time L4 artifact appears reusable but lacks promotion evidence, or when Esthetix / ESTRIX / SHINES / SoMatch boundaries are ambiguous.

Codex may continue draft-only analysis under the safest temporary classification, but must not execute, route or activate until classification is safe.

---

## 4. Repository Architecture

The repository is organized as a governed authority system. Each folder has a specific function and must not be treated as interchangeable.

Root-level files define the global operating frame for the repository. These include repository-level operating instructions, business architecture rules and the README overview.

```text
AGENTS.md
README.md
AGENTS_BUSINESS_ARCHITECTURE_RULE.md
```

The `agents/` folder contains the formal Agent operating library and governance materials.

```text
agents/
├─ 00_command/
├─ 10_esthetix_arsenal/
├─ 20_estrix_core/
├─ 30_applications/
├─ 40_engagements/
├─ agent-registry/
├─ governance/
├─ core/
├─ guardian/
├─ mission/
├─ platform/
├─ sovereign/
├─ shared/
└─ _quarantine/
```

### 4.1 Command and Business Context Folders

`00_command/` contains K / CEO command context and final decision authority references.

`10_esthetix_arsenal/` contains Esthetix company-level R&D, governance and AI operating system context.

`20_estrix_core/` contains reusable ESTRIX Core Engine definitions, extension policy, module registry and use-case registry.

`30_applications/` contains application-level or use-case-level contexts such as SHINES Field and SoMatch Service Brand.

`40_engagements/` contains one-time project, sprint, campaign, client or MVP delivery contexts.

### 4.2 Governance and Registry Folders

`agent-registry/` contains metadata, schema, router, responsibility, capability, layer, risk and hook control files. Registry files describe authority and routing. They are not execution agents.

`governance/` contains operating protocols such as PR / CI validation, WORM event schema, production readiness, Guardian review, kill-switch, canary and human override controls.

`_quarantine/` contains unsafe, ambiguous, duplicated, incomplete or mismatched files that must not be routed as active until restoration requirements are met.

### 4.3 Agent Function Folders

`core/` contains Core Strategy agents for strategy, portfolio, product direction, revenue intelligence and executive coordination.

`mission/` contains execution agents for engineering, marketing, sales, support, product, operations and delivery work.

`guardian/` contains review, audit, compliance, security, finance, brand, reliability and risk agents.

`platform/` contains reusable infrastructure agents for data, tools, DevOps, SRE, identity, document automation, reporting and workflow support.

`sovereign/` contains company-level arbitration, escalation and decision package materials. Sovereign files prepare decisions; they must not directly execute irreversible company actions.

`shared/` contains reusable templates, examples, snippets, vocabulary and non-agent support assets. Shared files must not be routed as active execution targets.

---

## 5. C-A-E-P Agent Layer Structure

PAEX-AI separates agent authority through the C-A-E-P model.

```text
C｜Core Strategy
A｜Mission
E｜Guardian
P｜Platform
```

This separation prevents one agent from becoming executor, reviewer, auditor and approver at the same time.

### 5.1 C｜Core Strategy

Core Strategy agents support strategic analysis, portfolio judgment, product direction, market entry, revenue intelligence, executive coordination and decision packaging.

Core Strategy agents may recommend actions and prepare decision materials. They must not directly execute irreversible company-level actions.

### 5.2 A｜Mission

Mission agents execute operational, engineering, marketing, sales, support, product, project or content work.

Mission agents may create deliverables and implement approved work. They must not self-approve High or Critical work, bypass Guardian Review, claim final approval authority or ignore required hooks.

### 5.3 E｜Guardian

Guardian agents review, verify, audit, veto, enforce standards, identify risks and require evidence.

Guardian agents must not become hidden execution agents. If a Guardian appears to execute production work, Codex must trigger Guardian Purity Audit.

### 5.4 P｜Platform

Platform agents provide reusable infrastructure, tooling, data pipelines, reliability support, WORM logging, Oracle verification, CI support, knowledge systems, identity systems and workflow foundations.

Platform agents provide the road. They do not decide the final business destination.

### 5.5 Sovereign Boundary

Sovereign is not a normal execution layer.

Sovereign handles company-level arbitration, Principle 0 conflicts, irreversible escalation, Kill Switch release packages, Human Override packages and final decision packages.

Sovereign may prepare and escalate decisions. Sovereign must not directly execute irreversible company-level actions.

---

## 6. Routing and Registry Principles

Routing must be based on capability, authority, risk, status, tool permissions, business context layer and required hooks.

Capability match alone is not enough.

Before routing any Medium, High or Critical task, Codex must align with the canonical registry files:

```text
agents/agent-registry/agent-router/agent-router.md
agents/agent-registry/risk-level-map/risk-level-map.md
agents/agent-registry/secondary-hooks-map/secondary-hooks-map.md
agents/agent-registry/frontmatter-schema/frontmatter-schema.md
agents/agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
agents/_quarantine/quarantine-policy/quarantine-policy.md
```

Routing must answer:

```text
Who can do this?
Who may do this?
Who must review this?
What evidence is required?
What must be logged?
What must not be automated?
```

Allowed router decisions are:

```text
PROCEED
HOLD
BLOCK
ESCALATE
```

Use `PROCEED` only when the risk is controlled and required hooks exist.

Use `HOLD` when more evidence, approval, review, classification or repair is needed.

Use `BLOCK` when the action violates governance, law, safety, privacy, security, quarantine or authority boundaries.

Use `ESCALATE` when K / CEO, Sovereign or an authorized human owner must decide.

Registry files are the source of truth for routing and authority. If the registry and file content conflict, return `HOLD` until the conflict is repaired.

---

## 7. Frontmatter Discipline

Every governed Agent, registry, governance or protocol file should contain valid YAML frontmatter.

Frontmatter defines file identity, ownership, layer, risk, status, routing eligibility, tool permissions, registry behavior and governance controls.

Minimum recommended fields include:

```yaml
---
name:
title:
description:
layer:
context_layer:
pace_layer:
risk_level:
status:
owner:
review_required:
human_approval_required:
codex_autofix_allowed:
tool_permissions:
routing_enabled:
registry_enabled:
version:
related_files:
---
```

High-risk or Critical files should also include:

```yaml
requires_worm: true
requires_guardian_review: true
requires_human_approval: true
human_approval_scope:
  - ...
worm_scope:
  - ...
secondary_hooks:
  - ...
forbidden_actions:
  - ...
allowed_actions:
  - ...
evidence_required:
  - ...
rollback_required: true
canary_required: true
```

`human_approval_required` is the lifecycle-level activation or execution approval flag.

`requires_human_approval` is the High / Critical governance control flag.

For High / Critical files, both should be aligned unless an explicit exemption is documented.

Duplicate frontmatter keys must fail validation because duplicated metadata may create inconsistent routing, lifecycle, permission or risk interpretation.

Invalid enum values, missing required fields, broken required `related_files`, unsafe routing flags, missing High / Critical controls and frontmatter-content conflicts must return `FAIL` or `HOLD` according to the PR / CI validation checklist.

Frontmatter must not invent authority. If frontmatter grants authority contradicted by governance or content, Codex must return `HOLD` and recommend correction.

---

## 8. Risk Classification and Secondary Hooks

Risk classification determines how much review, evidence, approval, logging and escalation a task requires.

The canonical source for risk classification is:

```text
agents/agent-registry/risk-level-map/risk-level-map.md
```

The canonical source for mandatory hooks is:

```text
agents/agent-registry/secondary-hooks-map/secondary-hooks-map.md
```

Risk levels are:

| Risk     | Meaning                                                                                                             | Default Handling                                               |
| -------- | ------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Low      | Reversible, local, non-sensitive, non-production work                                                               | Proceed with basic self-check                                  |
| Medium   | Normal operational work with limited blast radius                                                                   | Proceed with validation note and review awareness              |
| High     | Sensitive, external, production-adjacent, financial, legal, brand, data or permission impact                        | Require hooks, Guardian note, rollback and WORM consideration  |
| Critical | Irreversible or materially consequential legal, financial, security, production, ledger, payment or identity impact | No autonomous execution; prepare decision package and escalate |
| Blocked  | Unsafe, unlawful, contradictory, quarantined or missing authority                                                   | Block execution                                                |
| TBD      | Risk cannot be determined with available evidence                                                                   | HOLD until classified                                          |

When risk is unclear, classify upward.

Secondary hooks may include Guardian Review, WORM Event, Canary, Human Approval, Sovereign Package, Kill Switch, Oracle Verification, Data Boundary Review, Rollback Plan, Counter-Metrics, Quarantine Review, Guardian Purity Audit, Core Contamination Check, Tool Permission Review and Production Readiness Gate.

If one task touches multiple triggers, Codex must attach the strictest combined hook set. Codex must not choose only the easiest hook.

---

## 9. Quarantine Policy

Unsafe, ambiguous, duplicated, incomplete or mismatched files must not be routed as active.

The canonical quarantine policy is:

```text
agents/_quarantine/quarantine-policy/quarantine-policy.md
```

Use quarantine when a file has missing frontmatter, wrong layer, unclear risk level, unsafe permissions, duplicate responsibility, content mismatch, pending human review, unclear routing target, Guardian purity issue, Sovereign boundary issue, Core contamination or active reference conflict.

Quarantined files must use safe isolation settings:

```yaml
status: quarantined
routing_enabled: false
tool_permissions: none
registry_enabled: false
```

Quarantined files must not be listed as active routing targets, granted tool permissions, referenced as active dependencies or restored without required review.

Restoration requires resolved quarantine reason, corrected frontmatter, valid path-layer mapping, assigned risk level, safe tool permissions, correct routing status, resolved duplicate responsibility, registry update, related files update and PR / CI validation.

Medium+ restoration requires human review.

High / Critical restoration requires Guardian Review and WORM-style record.

Plain-language rule:

> Quarantine is not deletion.
> Quarantine is a safety buffer that prevents uncertain files from becoming active authority.

---

## 10. PR / CI Validation Rules

The canonical PR / CI validation source is:

```text
agents/governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
```

Before any repository governance change is considered ready, the change must pass or explicitly resolve required PR / CI checks.

Required validation categories include:

* frontmatter exists;
* required fields are present;
* enum values are valid;
* duplicate frontmatter keys are absent;
* path matches layer;
* risk level is present;
* High / Critical hooks are present;
* routing flags are valid;
* shared files are non-routable;
* quarantine files are non-routable;
* Guardian purity is preserved;
* Mission does not self-approve High / Critical work;
* Sovereign does not directly execute irreversible work;
* registry files are not treated as execution agents;
* L2 Core contamination is checked;
* L3 does not redefine ESTRIX;
* L4 does not redefine architecture;
* quarantine restoration is reviewed;
* related files exist;
* duplicate responsibility is scanned;
* version lifecycle is valid;
* context layer is present;
* tool permissions are valid;
* companion governance files are synchronized.

Mechanical validation may return `FAIL` for deterministic errors such as missing frontmatter, invalid enum values, broken required paths, duplicate keys, unsafe routing flags or missing High / Critical controls.

Semantic ambiguity should return `HOLD`.

High / Critical governance changes require human approval, Guardian Review and WORM evidence where applicable.

---

## 11. v1.4 Activation Gate

The repository may be treated as v1.4-ready only when the core governance baseline is present, synchronized, validated and approved.

The minimum companion files include:

```text
AGENTS.md
README.md
AGENTS_BUSINESS_ARCHITECTURE_RULE.md
agents/agent-registry/frontmatter-schema/frontmatter-schema.md
agents/agent-registry/agent-router/agent-router.md
agents/agent-registry/risk-level-map/risk-level-map.md
agents/agent-registry/secondary-hooks-map/secondary-hooks-map.md
agents/agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
agents/_quarantine/quarantine-policy/quarantine-policy.md
agents/governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
```

v1.4 activation requires:

* frontmatter schema validation;
* router consistency check;
* risk-level map alignment;
* secondary hooks map alignment;
* quarantine policy alignment;
* PR / CI validation;
* related files path validation;
* duplicate frontmatter key check;
* companion governance file synchronization;
* Guardian Review;
* WORM activation record;
* K / CEO or delegated authorized reviewer approval.

This README may summarize the governance baseline, but it does not override canonical governance files.

If this README conflicts with `AGENTS.md`, `AGENTS_BUSINESS_ARCHITECTURE_RULE.md`, `agent-router.md`, `risk-level-map.md`, `secondary-hooks-map.md`, `frontmatter-schema.md`, `registry-maintenance-policy.md`, `quarantine-policy.md` or `pr-ci-validation-checklist.md`, Codex must return `HOLD` and require governance synchronization.

Do not mark the repository as v1.4 active if companion files are missing, broken, stale, unsynchronized or unapproved.

---

## 12. Final Rule

The `agents/` repository is an authority system, not a prompt warehouse.

Every governed file must have a clear identity, boundary, owner, risk level, routing status, tool permission scope, registry relationship and review requirement.

Codex must classify before routing, route before execution, attach hooks before high-risk action, record before release, use Canary before scale, require human decision before irreversible action and require evidence before completion.

A capable Agent is not automatically an authorized Agent.

A fast implementation is not automatically a safe implementation.

A completed task is not automatically an audited task.

A reusable engine must not be trapped inside one application.

A brand service package must not redefine the core engine.

A quarantined file must not become active authority.

Final doctrine:

> PAEX-AI exists to make Esthetix faster, safer, clearer, more auditable and more scalable.
> It must never make Esthetix faster by making responsibility disappear.


---


```text
agents
├─ 00_command
│  ├─ AGENTS.md
│  └─ K_COMMAND_CENTER.md
├─ 10_esthetix_arsenal
│  ├─ AGENTS.md
│  ├─ ESTHETIX_ARSENAL_CONTEXT.md
│  └─ ESTHETIX_GOVERNANCE_OS.md
├─ 20_estrix_core
│  ├─ AGENTS.md
│  ├─ ESTRIX_CORE_ENGINE_CONTEXT.md
│  ├─ ESTRIX_EXTENSION_POLICY.md
│  ├─ ESTRIX_MODULE_REGISTRY.md
│  └─ ESTRIX_USE_CASE_REGISTRY.md
├─ 30_applications
│  ├─ future_use_case_template
│  │  ├─ AGENTS.md
│  │  └─ USE_CASE_PROFILE_TEMPLATE.md
│  ├─ shines_field
│  │  ├─ AGENTS.md
│  │  ├─ SHINES_FIELD_CONTEXT.md
│  │  └─ SHINES_OPERATION_PLAYBOOK.md
│  └─ somatch_service_brand
│     ├─ AGENTS.md
│     ├─ SOMATCH_OFFERING_CATALOG.md
│     └─ SOMATCH_SERVICE_BRAND_CONTEXT.md
├─ 40_engagements
│  ├─ shines_q3_operations
│  │  ├─ AGENTS.md
│  │  ├─ ENGAGEMENT_BRIEF.md
│  │  └─ TASK_LOG.md
│  └─ somatch_mvp_2026
│     ├─ AGENTS.md
│     ├─ ENGAGEMENT_BRIEF.md
│     └─ TASK_LOG.md
├─ agent-registry
│  ├─ agent-index
│  │  └─ agent-index.md
│  ├─ agent-responsibility-matrix
│  │  └─ agent-responsibility-matrix.md
│  ├─ agent-router
│  │  └─ agent-router.md
│  ├─ capability-map
│  │  └─ capability-map.md
│  ├─ frontmatter-schema
│  │  └─ frontmatter-schema.md
│  ├─ layer-map
│  │  └─ layer-map.md
│  ├─ registry-maintenance-policy
│  │  └─ registry-maintenance-policy.md
│  ├─ risk-level-map
│  │  └─ risk-level-map.md
│  └─ secondary-hooks-map
│     └─ secondary-hooks-map.md
├─ AGENTS_BUSINESS_ARCHITECTURE_RULE.md
├─ core
│  ├─ executive-office
│  │  └─ chief-of-staff
│  │     └─ specialized-chief-of-staff.md
│  ├─ finance
│  │  ├─ financial-forecasting
│  │  │  └─ finance-financial-forecaster.md
│  │  ├─ fpa
│  │  │  └─ finance-fpa-analyst.md
│  │  ├─ investment-research
│  │  │  └─ finance-investment-researcher.md
│  │  └─ strategic-finance
│  │     └─ finance-financial-analyst.md
│  ├─ market-strategy
│  │  └─ market-entry
│  │     └─ marketing-china-market-localization-strategist.md
│  ├─ orchestration
│  │  └─ agents-orchestrator
│  │     └─ agents-orchestrator.md
│  ├─ product-management
│  │  └─ product-manager.md
│  ├─ product-strategy
│  │  └─ trend-research
│  │     └─ product-trend-researcher.md
│  ├─ project-portfolio
│  │  └─ studio-producer
│  │     └─ project-management-studio-producer.md
│  ├─ revenue-intelligence
│  │  └─ pipeline-analytics
│  │     └─ sales-pipeline-analyst.md
│  └─ revenue-strategy
│     ├─ account-expansion
│     │  └─ sales-account-strategist.md
│     └─ deal-strategy
│        └─ sales-deal-strategist.md
├─ governance
│  ├─ agent-drift-review
│  │  └─ agent-drift-review.md
│  ├─ canary-release-governor
│  │  └─ canary-release-governor.md
│  ├─ controlled-production-activation-order
│  │  └─ controlled-production-activation-order.md
│  ├─ core-governance-protocols
│  │  └─ core-governance-protocols.md
│  ├─ guardian-purity-audit
│  │  └─ guardian-purity-audit.md
│  ├─ guardian-review-coordinator
│  │  └─ guardian-review-coordinator.md
│  ├─ human-override-accountability
│  │  └─ human-override-accountability.md
│  ├─ kill-switch-governor
│  │  └─ kill-switch-governor.md
│  ├─ pr-ci-validation-checklist
│  │  └─ pr-ci-validation-checklist.md
│  ├─ production-readiness-gate
│  │  └─ production-readiness-gate.md
│  ├─ stable-controlled-activation-order
│  │  └─ stable-controlled-activation-order.md
│  └─ worm-event-schema
│     └─ worm-event-schema.md
├─ guardian
│  ├─ accessibility
│  │  └─ accessibility-auditor
│  │     └─ testing-accessibility-auditor.md
│  ├─ agriculture
│  │  └─ livestock-archive-audit
│  │     └─ livestock-archive-auditor.md
│  ├─ ai-governance
│  │  └─ policy-writer
│  │     └─ specialized-ai-policy-writer.md
│  ├─ api-quality
│  │  └─ api-tester
│  │     └─ testing-api-tester.md
│  ├─ automation-governance
│  │  └─ workflow-approval
│  │     └─ automation-governance-architect.md
│  ├─ brand-governance
│  │  └─ brand-guardian
│  │     └─ design-brand-guardian.md
│  ├─ code-quality
│  │  └─ engineering-minimal-change-engineer.md
│  ├─ compliance
│  │  └─ audit-readiness
│  │     └─ compliance-auditor.md
│  ├─ cultural-risk
│  │  └─ cultural-intelligence
│  │     └─ specialized-cultural-intelligence-strategist.md
│  ├─ data
│  │  └─ engineering-ai-data-remediation-engineer.md
│  ├─ delivery-governance
│  │  └─ jira-workflow
│  │     └─ project-management-jira-workflow-steward.md
│  ├─ embedded-quality
│  │  └─ embedded-qa-engineer
│  │     └─ testing-embedded-qa-engineer.md
│  ├─ engineering
│  │  └─ engineering-code-reviewer.md
│  ├─ engineering-compliance
│  │  └─ civil-structural
│  │     └─ specialized-civil-engineer.md
│  ├─ enterprise-risk
│  │  └─ risk-assessor
│  │     └─ specialized-risk-assessor.md
│  ├─ finance-control
│  │  ├─ finance-bookkeeper-controller.md
│  │  └─ finance-tracker
│  │     └─ support-finance-tracker.md
│  ├─ financial-risk
│  │  └─ fraud-detection
│  │     └─ finance-fraud-detector.md
│  ├─ healthcare
│  │  └─ marketing-compliance
│  │     └─ healthcare-marketing-compliance.md
│  ├─ inclusive-design
│  │  └─ inclusive-visuals
│  │     └─ design-inclusive-visuals-specialist.md
│  ├─ infrastructure-reliability
│  │  └─ infrastructure-maintainer
│  │     └─ support-infrastructure-maintainer.md
│  ├─ legal
│  │  └─ document-review
│  │     └─ legal-document-review.md
│  ├─ legal-compliance
│  │  └─ compliance-checker
│  │     └─ support-legal-compliance-checker.md
│  ├─ model-risk
│  │  └─ model-qa
│  │     └─ specialized-model-qa.md
│  ├─ paid-media-audit
│  │  └─ auditor
│  │     └─ paid-media-auditor.md
│  ├─ paid-media-measurement
│  │  └─ tracking
│  │     └─ paid-media-tracking-specialist.md
│  ├─ performance-reliability
│  │  └─ performance-benchmarker
│  │     └─ testing-performance-benchmarker.md
│  ├─ production-readiness
│  │  └─ reality-checker
│  │     └─ testing-reality-checker.md
│  ├─ quality-assurance
│  │  ├─ evidence-collector
│  │  │  └─ testing-evidence-collector.md
│  │  └─ test-results-analyzer
│  │     └─ testing-test-results-analyzer.md
│  ├─ reliability
│  │  └─ engineering-incident-response-commander.md
│  ├─ revenue-governance
│  │  └─ sales-coaching
│  │     └─ sales-coach.md
│  ├─ security
│  │  ├─ blockchain-audit
│  │  │  └─ blockchain-security-auditor.md
│  │  └─ engineering-security-engineer.md
│  ├─ security-detection
│  │  └─ engineering-threat-detection-engineer.md
│  └─ tax-compliance
│     └─ tax-strategy
│        └─ finance-tax-strategist.md
├─ mission
│  ├─ ai-voice
│  │  └─ engineering-voice-ai-integration-engineer.md
│  ├─ apple
│  │  └─ visionos
│  │     └─ visionos-spatial-engineer.md
│  ├─ backend-admin
│  │  └─ engineering-filament-optimization-specialist.md
│  ├─ blockchain
│  │  └─ engineering-solidity-smart-contract-engineer.md
│  ├─ content
│  │  ├─ general
│  │  │  └─ marketing-content-creator.md
│  │  ├─ knowledge-commerce
│  │  │  └─ marketing-knowledge-commerce-strategist.md
│  │  ├─ knowledge-platforms
│  │  │  └─ zhihu
│  │  │     └─ marketing-zhihu-strategist.md
│  │  ├─ podcast
│  │  │  └─ marketing-podcast-strategist.md
│  │  ├─ professional-branding
│  │  │  └─ marketing-linkedin-content-creator.md
│  │  ├─ thought-leadership
│  │  │  └─ marketing-book-co-author.md
│  │  ├─ video-optimization
│  │  │  └─ marketing-video-optimization-specialist.md
│  │  └─ video-production
│  │     └─ marketing-short-video-editing-coach.md
│  ├─ customer-operations
│  │  └─ support-responder
│  │     └─ support-support-responder.md
│  ├─ design
│  │  ├─ design-image-prompt-engineer.md
│  │  ├─ design-ui-designer.md
│  │  ├─ design-ux-researcher.md
│  │  ├─ design-visual-storyteller.md
│  │  └─ design-whimsy-injector.md
│  ├─ desktop-host
│  │  └─ engineering-pc-host-engineer.md
│  ├─ developer-relations
│  │  └─ developer-advocate
│  │     └─ specialized-developer-advocate.md
│  ├─ education
│  │  ├─ gaokao-advisory
│  │  │  └─ gaokao-college-advisor.md
│  │  └─ study-abroad-advisor
│  │     └─ study-abroad-advisor.md
│  ├─ embedded
│  │  └─ engineering-embedded-firmware-engineer.md
│  ├─ embedded-linux
│  │  └─ engineering-embedded-linux-driver-engineer.md
│  ├─ engineering
│  │  ├─ cms
│  │  │  └─ engineering-backend-architect.md
│  │  └─ engineering-ai-engineer.md
│  ├─ finance
│  │  └─ accounts-payable
│  │     └─ accounts-payable-agent.md
│  ├─ financial-services
│  │  └─ loan-officer-assistant
│  │     └─ loan-officer-assistant.md
│  ├─ frontend
│  │  └─ engineering-frontend-developer.md
│  ├─ fullstack
│  │  └─ engineering-senior-developer.md
│  ├─ hardware
│  │  └─ engineering-fpga-digital-design-engineer.md
│  ├─ healthcare
│  │  └─ patient-service
│  │     └─ healthcare-customer-service.md
│  ├─ hospitality
│  │  └─ guest-services
│  │     └─ hospitality-guest-services.md
│  ├─ language
│  │  └─ translation
│  │     └─ language-translator.md
│  ├─ legal
│  │  ├─ billing-time-tracking
│  │  │  └─ legal-billing-time-tracking.md
│  │  └─ client-intake
│  │     └─ legal-client-intake.md
│  ├─ market-expansion
│  │  ├─ france-consulting
│  │  │  └─ specialized-french-consulting-market.md
│  │  └─ korea-business
│  │     └─ specialized-korean-business-navigator.md
│  ├─ marketing
│  │  ├─ aso
│  │  │  └─ marketing-app-store-optimizer.md
│  │  ├─ community
│  │  │  └─ reddit
│  │  │     └─ marketing-reddit-community-builder.md
│  │  ├─ content-platforms
│  │  │  ├─ marketing-bilibili-strategist.md
│  │  │  ├─ marketing-douyin-strategist.md
│  │  │  ├─ marketing-kuaishou-strategist.md
│  │  │  ├─ marketing-tiktok-strategist.md
│  │  │  ├─ weixin-channels
│  │  │  │  └─ marketing-weixin-channels-strategist.md
│  │  │  └─ xiaohongshu
│  │  │     ├─ marketing-xiaohongshu-operator.md
│  │  │     └─ marketing-xiaohongshu-specialist.md
│  │  ├─ cross-border-ecommerce
│  │  │  └─ marketing-cross-border-ecommerce.md
│  │  ├─ ecommerce
│  │  │  ├─ marketing-china-ecommerce-operator.md
│  │  │  └─ marketing-ecommerce-operator.md
│  │  ├─ growth
│  │  │  └─ marketing-growth-hacker.md
│  │  ├─ livestream-commerce
│  │  │  └─ marketing-livestream-commerce-coach.md
│  │  ├─ localization
│  │  │  └─ taiwan
│  │  │     └─ marketing-taiwan-market-localization-strategist.md
│  │  ├─ private-domain
│  │  │  └─ marketing-private-domain-operator.md
│  │  ├─ search
│  │  │  └─ marketing-seo-specialist.md
│  │  ├─ search-visibility
│  │  │  └─ marketing-ai-citation-strategist.md
│  │  ├─ seo
│  │  │  └─ marketing-baidu-seo-specialist.md
│  │  ├─ social-growth
│  │  │  └─ marketing-carousel-growth-engine.md
│  │  ├─ social-media
│  │  │  └─ marketing-social-media-strategist.md
│  │  ├─ social-platforms
│  │  │  ├─ marketing-facebook-curator.md
│  │  │  ├─ marketing-instagram-curator.md
│  │  │  ├─ marketing-twitter-engager.md
│  │  │  └─ weibo
│  │  │     └─ marketing-weibo-strategist.md
│  │  └─ wechat
│  │     ├─ official-account
│  │     │  └─ marketing-wechat-official-account.md
│  │     └─ private-domain
│  │        └─ marketing-wechat-operator.md
│  ├─ mechanical
│  │  └─ engineering-mechanical-design-engineer.md
│  ├─ mobile
│  │  └─ engineering-mobile-app-builder.md
│  ├─ paid-media
│  │  ├─ creative
│  │  │  └─ paid-media-creative-strategist.md
│  │  ├─ ppc
│  │  │  └─ paid-media-ppc-strategist.md
│  │  ├─ programmatic
│  │  │  └─ paid-media-programmatic-buyer.md
│  │  ├─ search
│  │  │  └─ paid-media-search-query-analyst.md
│  │  └─ social
│  │     └─ paid-media-paid-social-strategist.md
│  ├─ people-ops
│  │  ├─ hr-onboarding
│  │  │  └─ hr-onboarding.md
│  │  ├─ recruitment
│  │  │  ├─ recruitment-specialist.md
│  │  │  └─ support-recruitment-specialist.md
│  │  └─ taiwan-recruitment
│  │     └─ support-taiwan-recruitment-specialist.md
│  ├─ product-delivery
│  │  └─ sprint-prioritization
│  │     └─ product-sprint-prioritizer.md
│  ├─ product-discovery
│  │  └─ feedback-synthesis
│  │     └─ product-feedback-synthesizer.md
│  ├─ product-experimentation
│  │  └─ experiment-tracking
│  │     └─ project-management-experiment-tracker.md
│  ├─ project-management
│  │  ├─ project-shepherd
│  │  │  └─ project-management-project-shepherd.md
│  │  └─ web-delivery
│  │     └─ project-manager-senior.md
│  ├─ prototyping
│  │  └─ engineering-rapid-prototyper.md
│  ├─ public-sector
│  │  └─ government-presales
│  │     └─ government-digital-presales-consultant.md
│  ├─ real-estate
│  │  └─ buyer-seller
│  │     └─ real-estate-buyer-seller.md
│  ├─ retail
│  │  └─ customer-returns
│  │     └─ retail-customer-returns.md
│  ├─ revenue-operations
│  │  └─ pricing-optimizer
│  │     └─ specialized-pricing-optimizer.md
│  ├─ sales
│  │  ├─ discovery-coaching
│  │  │  └─ sales-discovery-coach.md
│  │  ├─ outbound-strategy
│  │  │  └─ sales-outbound-strategist.md
│  │  ├─ proposal-strategy
│  │  │  └─ sales-proposal-strategist.md
│  │  └─ solution-engineering
│  │     └─ sales-engineer.md
│  ├─ wechat
│  │  └─ engineering-wechat-mini-program-developer.md
│  └─ xr
│     ├─ cockpit-interaction
│     │  └─ xr-cockpit-interaction-specialist.md
│     ├─ spatial-interface
│     │  └─ xr-interface-architect.md
│     └─ webxr-development
│        └─ xr-immersive-developer.md
├─ platform
│  ├─ agent-tooling
│  │  └─ mcp-builder
│  │     └─ specialized-mcp-builder.md
│  ├─ agentic-web
│  │  └─ marketing-agentic-search-optimizer.md
│  ├─ ai-ops
│  │  ├─ autonomous-optimization
│  │  │  └─ engineering-autonomous-optimization-architect.md
│  │  └─ prompt-engineering
│  │     └─ prompt-engineer.md
│  ├─ analytics-bi
│  │  └─ analytics-reporter
│  │     └─ support-analytics-reporter.md
│  ├─ apple-devtools
│  │  └─ terminal-integration
│  │     └─ terminal-integration-specialist.md
│  ├─ apple-rendering
│  │  └─ metal-spatial-engineering
│  │     └─ macos-spatial-metal-engineer.md
│  ├─ architecture
│  │  └─ engineering-software-architect.md
│  ├─ audit
│  │  └─ worm-audit-supervisor.md
│  ├─ data
│  │  ├─ engineering-data-engineer.md
│  │  └─ sales-data-consolidation
│  │     └─ data-consolidation-agent.md
│  ├─ data-pipeline
│  │  └─ sales-data-extraction
│  │     └─ sales-data-extraction-agent.md
│  ├─ database
│  │  └─ database-optimizer
│  │     └─ engineering-database-optimizer.md
│  ├─ design-system
│  │  └─ ux-architecture
│  │     └─ design-ux-architect.md
│  ├─ developer-experience
│  │  ├─ engineering-codebase-onboarding-engineer.md
│  │  └─ engineering-git-workflow-master.md
│  ├─ devops
│  │  └─ engineering-devops-automator.md
│  ├─ document-automation
│  │  └─ document-generator
│  │     └─ specialized-document-generator.md
│  ├─ engineering
│  │  └─ lsp-index
│  │     └─ lsp-index-engineer.md
│  ├─ enterprise-systems
│  │  └─ salesforce-architecture
│  │     └─ specialized-salesforce-architect.md
│  ├─ executive-ops
│  │  └─ summary-generator
│  │     └─ support-executive-summary-generator.md
│  ├─ identity
│  │  └─ identity-graph
│  │     └─ identity-graph-operator.md
│  ├─ integrations
│  │  ├─ engineering-dingtalk-integration-developer.md
│  │  └─ engineering-feishu-integration-developer.md
│  ├─ intelligence
│  │  └─ news-briefing
│  │     └─ marketing-daily-news-briefing.md
│  ├─ iot
│  │  └─ engineering-iot-solution-architect.md
│  ├─ knowledge
│  │  └─ engineering-technical-writer.md
│  ├─ knowledge-context
│  │  └─ engineering-email-intelligence-engineer.md
│  ├─ knowledge-system
│  │  └─ zk-steward
│  │     └─ zk-steward.md
│  ├─ localization
│  │  └─ technical-translation
│  │     └─ technical-translator-agent.md
│  ├─ operating-system
│  │  ├─ meeting-productivity
│  │  │  └─ specialized-meeting-assistant.md
│  │  └─ workflow-architecture
│  │     └─ specialized-workflow-architect.md
│  ├─ operations
│  │  └─ process-governance
│  │     └─ project-management-studio-operations.md
│  ├─ people-learning
│  │  └─ corporate-training
│  │     └─ corporate-training-designer.md
│  ├─ product-experience
│  │  └─ behavioral-nudge-engine
│  │     └─ product-behavioral-nudge-engine.md
│  ├─ reliability
│  │  └─ engineering-sre.md
│  ├─ reporting
│  │  └─ distribution
│  │     └─ report-distribution-agent.md
│  ├─ tooling-governance
│  │  └─ tool-evaluator
│  │     └─ testing-tool-evaluator.md
│  ├─ trust
│  │  └─ identity-trust
│  │     └─ agentic-identity-trust.md
│  └─ workflow-ops
│     └─ workflow-optimizer
│        └─ testing-workflow-optimizer.md
├─ shared
│  └─ README.md
├─ sovereign
│  ├─ controlled-production-activation-order
│  │  └─ controlled-production-activation-order.md
│  ├─ cross-domain-war-room-playbook
│  │  └─ cross-domain-war-room-playbook.md
│  ├─ governance-protocols-index
│  │  └─ governance-protocols-index.md
│  ├─ principle-0-charter
│  │  └─ principle-0-charter.md
│  ├─ sovereign-agent
│  │  └─ sovereign-agent.md
│  ├─ sovereign-decision-playbook
│  │  └─ sovereign-decision-playbook.md
│  ├─ sovereign-execution-boundary
│  │  └─ sovereign-execution-boundary.md
│  └─ stable-controlled-activation-order
│     └─ stable-controlled-activation-order.md
└─ _quarantine
   ├─ content-mismatch
   │  ├─ content-mismatch.md
   │  └─ finance-invoice-manager.md
   ├─ duplicate-responsibility
   │  └─ duplicate-responsibility.md
   ├─ missing-frontmatter
   │  └─ missing-frontmatter.md
   ├─ pending-human-review
   │  └─ pending-human-review.md
   ├─ quarantine-policy
   │  └─ quarantine-policy.md
   ├─ README.md
   ├─ unclear-risk-level
   │  └─ unclear-risk-level.md
   ├─ unsafe-permission
   │  └─ unsafe-permission.md
   └─ wrong-layer
      └─ wrong-layer.md

```
