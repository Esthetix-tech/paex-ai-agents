---
name: use-case-profile-template
title: Use Case Profile Template
description: Draft template for describing and governing a new ESTRIX-powered application or use case during intake.
layer: L3
context_layer: Application / Use Case Layer
pace_layer: Business Architecture / Use Case Template
risk_level: medium
status: draft
owner: Agent Repository Steward
review_required: true
human_approval_required: false
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: false
version: v1.0-intake-draft
related_files: []
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
```
