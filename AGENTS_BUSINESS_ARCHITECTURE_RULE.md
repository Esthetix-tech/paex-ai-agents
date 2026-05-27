---
name: AGENTS Business Architecture Rule
title: AGENTS Business Architecture Rule
description: Defines the required business architecture classification rule for Esthetix, ESTRIX, SHINES and SoMatch, and requires Codex to classify every new requirement into the five-layer Context Stack before execution.
layer: governance
context_layer: Repository Governance
pace_layer: Repository Governance / Business Architecture Context Stack
risk_level: high
status: active
owner: K / CEO
review_required: true
human_approval_required: false
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: false
version: v1.0
related_files:
  - 00_command/K_COMMAND_CENTER.md
  - 10_esthetix_arsenal/ESTHETIX_ARSENAL_CONTEXT.md
  - 10_esthetix_arsenal/ESTHETIX_GOVERNANCE_OS.md
  - 20_estrix_core/ESTRIX_CORE_ENGINE_CONTEXT.md
  - 20_estrix_core/ESTRIX_EXTENSION_POLICY.md
  - 20_estrix_core/ESTRIX_MODULE_REGISTRY.md
  - 20_estrix_core/ESTRIX_USE_CASE_REGISTRY.md
  - 30_applications/shines_field/SHINES_FIELD_CONTEXT.md
  - 30_applications/somatch_service_brand/SOMATCH_SERVICE_BRAND_CONTEXT.md
requires_worm: true
requires_guardian_review: true
requires_human_approval: true
secondary_hooks:
  - governance-review
  - registry-maintenance-review
  - ci-validation-review
forbidden_actions:
  - redefine_business_architecture_without_review
  - collapse_esthetix_estrix_shines_somatch_layers
  - promote_l4_to_l2_without_classification
  - treat_application_logic_as_core_without_review
rollback_required: true
canary_required: false
exemption_reason: business_architecture_policy_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26

---

# AGENTS Business Architecture Rule

## 1. Purpose

This file defines the mandatory business architecture rule for Codex, Agent Engine, Agent Registry and all related workspace instructions.

Its purpose is to prevent Codex from treating `Esthetix`, `ESTRIX`, `SHINES` and `SoMatch` as the same layer.

These names are related, but they do not mean the same thing.

Core rule:

> Esthetix builds the engine.  
> ESTRIX is the reusable engine.  
> SHINES is the first field operation unit.  
> SoMatch is SHINES' external service brand powered by ESTRIX.

Codex must preserve this separation when analyzing requirements, creating files, designing features, writing copy, proposing architecture, generating tasks or classifying Agent responsibilities.

---

## 2. Business Architecture Doctrine

Esthetix, ESTRIX, SHINES and SoMatch must not be treated as interchangeable entities.

They belong to different business layers.

| Entity | Correct Role | Incorrect Interpretation |
|---|---|---|
| Esthetix | Arsenal and R&D company | SoMatch, SHINES back office, beauty-only company |
| ESTRIX | Reusable core operating engine | SHINES-only system, SoMatch-only system, beauty-only SaaS |
| SHINES | First real-world field operation unit | The full boundary of ESTRIX |
| SoMatch | SHINES' external operating service brand | Esthetix direct service brand or ESTRIX itself |

This separation is mandatory because the Esthetix business model is designed for expansion.

If Codex hard-codes ESTRIX as a SoMatch-only or SHINES-only system, future use cases will be constrained by an incorrect architecture.

---

## 3. Layer Definitions

### 3.1 Esthetix｜Arsenal and R&D Company

Esthetix is the arsenal.

It builds reusable AI operating systems, SaaS engines, Agent infrastructure, enterprise governance tooling, data governance, auditability, permission systems, workflow automation, API infrastructure and knowledge systems.

Esthetix is responsible for building and evolving:

- ESTRIX Core Engine;
- PAEX-AI Governance OS;
- ESNex Ecosystem Hub;
- Agent Engine / Codex workspace governance;
- reusable enterprise infrastructure;
- data, security, audit and permission architecture.

Esthetix must not be reduced to:

- a beauty company;
- a SoMatch service team;
- SHINES' internal technical department;
- a narrow SaaS vendor for one industry;
- a one-time delivery or campaign team.

Plain-language definition:

> Esthetix is the weapons factory and R&D headquarters.

---

### 3.2 ESTRIX｜Reusable Core Operating Engine

ESTRIX is the reusable core operating engine built by Esthetix.

It is not SHINES-specific, not SoMatch-specific and not beauty-industry-specific.

ESTRIX may power many different use cases, including:

- SHINES field operations;
- SoMatch service delivery;
- managed company operations;
- SaaS product lines;
- government project management;
- enterprise internal control systems;
- franchise operations;
- retail operations;
- medspa operations;
- customer success operations;
- AI Agent workflow products.

ESTRIX should contain reusable capabilities such as:

- CRM;
- booking / scheduling;
- billing / revenue visibility;
- dashboard;
- marketing operations;
- customer segmentation;
- notification;
- task management;
- permission;
- audit log;
- Agent workflow;
- report generation;
- workflow automation.

Plain-language definition:

> ESTRIX is the engine platform that can be installed into many vehicles.

---

### 3.3 SHINES｜First Field Operation Unit

SHINES is the first real-world field operation unit using ESTRIX.

SHINES validates ESTRIX through real beauty and service operations, including:

- customers;
- bookings;
- staff workflows;
- service SOPs;
- complaints;
- follow-ups;
- revenue;
- cash flow;
- membership operations;
- course and product packaging;
- campaign execution;
- field-level operating discipline.

SHINES is important because it gives ESTRIX a real battlefield.

However, SHINES does not define the full boundary of ESTRIX.

Plain-language definition:

> SHINES is the first unit taking the ESTRIX engine into real market operations.

---

### 3.4 SoMatch｜SHINES External Service Brand

SoMatch is SHINES' external operating service brand.

SoMatch packages ESTRIX capabilities into customer-facing service language.

For example:

| ESTRIX Capability | SoMatch Customer-Friendly Wording |
|---|---|
| CRM | help clients organize customer lists |
| Customer Segmentation | help clients identify customer groups |
| Notification | help clients schedule follow-ups |
| Dashboard | help clients understand revenue and operations |
| Marketing Ops | help clients plan content and campaigns |
| Report Generator | provide monthly operating reports |
| Agent Workflow | support smoother operating workflows |

Correct positioning:

> SoMatch is a SHINES service brand powered by ESTRIX.

SoMatch is not Esthetix.  
SoMatch is not ESTRIX.  
SoMatch does not define the boundary of ESTRIX.

Plain-language definition:

> SoMatch is the customer-facing service counter built on top of SHINES' field operation and powered by ESTRIX.

---

## 4. Mandatory Context Stack Classification

Before handling any new requirement, Codex must classify the request into one of the following five context layers.

| Layer | Name | Meaning |
|---|---|---|
| L0 | K Command Layer | K's company portfolio, final decision authority and cross-company principles |
| L1 | Esthetix Arsenal Layer | Esthetix company positioning, R&D role, governance and infrastructure strategy |
| L2 | ESTRIX Core Engine Layer | reusable system capabilities, shared modules, audit, permission and workflow logic |
| L3 | Application / Use Case Layer | specific application scenario, brand packaging or use-case configuration |
| L4 | Engagement / Project Layer | one-time project, client task, campaign, sprint, version or delivery item |

Codex must not proceed as if all requirements belong to the same layer.

If the correct layer is unclear, Codex must return `HOLD` or propose a classification with explicit assumptions.

---

## 5. Requirement Placement Rules

### 5.1 L0｜K Command Layer

A requirement belongs to L0 when it involves:

- K's highest decision authority;
- company portfolio structure;
- ownership or brand relationship;
- final approval boundary;
- company-level resource allocation;
- irreversible company-level action;
- public positioning change;
- cross-company conflict;
- strategic expansion direction.

Examples:

- deciding whether ESTRIX should enter a new industry;
- changing the relationship between Esthetix, SHINES and SoMatch;
- approving a new external business model;
- authorizing a high-risk partnership;
- approving company-level brand positioning.

---

### 5.2 L1｜Esthetix Arsenal Layer

A requirement belongs to L1 when it involves:

- Esthetix company positioning;
- Esthetix governance model;
- Esthetix's R&D role;
- PAEX-AI Governance OS;
- Agent Engine / Codex workspace strategy;
- enterprise knowledge system;
- data governance;
- security and audit architecture;
- reusable SaaS / AI infrastructure strategy.

Examples:

- defining Esthetix as an AI operating system R&D company;
- creating governance rules for Codex workspace;
- designing reusable enterprise infrastructure;
- writing company-wide AI operations principles;
- defining how ESTRIX, PAEX-AI and ESNex relate to Esthetix.

---

### 5.3 L2｜ESTRIX Core Engine Layer

A requirement belongs to L2 when it is a reusable capability.

A capability should be placed in ESTRIX Core when:

- two or more current or future use cases may reuse it;
- it affects shared data structure;
- it affects CRM, booking, billing, dashboard, permission, notification, audit or workflow;
- it creates reusable API, module, state machine, data object or automation logic;
- implementing it inside one application would create future duplication.

Examples:

- customer profile schema;
- follow-up logic;
- booking engine;
- dashboard metrics;
- notification engine;
- permission model;
- audit log;
- reusable report generator;
- Agent workflow routing;
- task management logic.

---

### 5.4 L3｜Application / Use Case Layer

A requirement belongs to L3 when it applies to one specific application, brand, service model or use case.

Examples:

- SoMatch service package names;
- SHINES beauty service workflows;
- SoMatch customer-facing offer language;
- medspa-specific consultation form;
- franchise-specific operating workflow;
- a use-case-specific onboarding script;
- application-level brand voice;
- industry-specific SOP built on ESTRIX modules.

L3 may configure or package ESTRIX Core capabilities, but it must not redefine ESTRIX Core.

---

### 5.5 L4｜Engagement / Project Layer

A requirement belongs to L4 when it is one-time, temporary, version-specific, client-specific or project-specific.

Examples:

- SoMatch MVP 2026 task;
- SHINES Q3 Operations Optimization;
- a specific client onboarding project;
- July content calendar;
- one monthly operating report;
- one sprint task;
- one campaign plan;
- one presentation;
- one proposal;
- one implementation checklist.

L4 may reveal reusable needs, but reusable logic must be proposed back to L2 ESTRIX Core.

---

## 6. Core Placement Doctrine

Reusable capabilities belong in ESTRIX Core.

Brand-specific packaging belongs in Application Layer.

One-time delivery work belongs in Engagement Layer.

This rule prevents three dangerous failure modes:

1. **Core capability trapped inside one brand**  
   Example: reusable CRM follow-up logic implemented only inside SoMatch.

2. **Application wording promoted into core architecture**  
   Example: SoMatch's customer-facing phrase becomes a system module name.

3. **One-time project output treated as permanent system design**  
   Example: SHINES June monthly report becomes the default dashboard architecture without review.

---

## 7. Examples

### 7.1 Customer Follow-Up

If the requirement is:

- customer profile;
- customer tag;
- follow-up date;
- follow-up history;
- reminder;
- follow-up effectiveness tracking;

then it belongs to:

```text
L2｜ESTRIX Core CRM / Retention Module