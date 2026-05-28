---
name: Use Case Profile Template
title: Use Case Profile Template
description: Template for registering, describing and governing a new ESTRIX-powered application or use case.
layer: L3
context_layer: Application / Use Case Layer
pace_layer: Business Architecture / Use Case Template
risk_level: medium
status: template
owner: ESTRIX Core Steward
review_required: true
human_approval_required: false
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: false
version: v1.0
related_files:
  - ../../00_command/K_COMMAND_CENTER.md
  - ../../10_esthetix_arsenal/ESTHETIX_ARSENAL_CONTEXT.md
  - ../../20_estrix_core/ESTRIX_CORE_ENGINE_CONTEXT.md
  - ../../20_estrix_core/ESTRIX_EXTENSION_POLICY.md
  - ../../20_estrix_core/ESTRIX_MODULE_REGISTRY.md
  - ../../20_estrix_core/ESTRIX_USE_CASE_REGISTRY.md
  - AGENTS.md
---

# Use Case Profile Template

## 1. Purpose

This template defines the standard profile format for any new ESTRIX-powered Use Case.

A Use Case may be a new application, service brand, managed operation scenario, SaaS product line, vertical operating system, client implementation model, government project management scenario or internal enterprise operating system.

Core rule:

> A Use Case extends ESTRIX.  
> It does not redefine ESTRIX.

This profile helps Codex and human reviewers determine:

- what the Use Case is;
- who owns it;
- which ESTRIX Core modules it uses;
- which capabilities belong in Core versus Application;
- what data it touches;
- which Agents may operate inside it;
- which Guardian Reviews are required;
- whether K / CEO approval is needed;
- whether the Use Case may move from concept to pilot or active status.

This file should be copied when creating a new folder under:

```text
/agents/30_applications/<new_use_case_slug>/