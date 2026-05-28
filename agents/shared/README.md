---
name: shared-readme
title: PAEX-AI Shared README
description: Draft README defining the purpose, boundaries and routing restrictions for shared repository support materials.
layer: shared
context_layer: Repository Governance
pace_layer: Repository Governance / Shared Support
risk_level: low
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

# PAEX-AI Shared README

## 1. Purpose

The `shared/` folder stores reusable support materials for the PAEX-AI Agent Repository.

It may contain templates, snippets, vocabulary, examples, formatting fragments and non-agent reference materials.

Core rule:

> `shared/` supports agents, protocols and governance files. It does not become an agent, governance authority or router target by itself.

## 2. Allowed Materials

The following materials may be stored in `shared/`:

- markdown templates;
- frontmatter examples;
- shared terminology lists;
- naming conventions;
- standard output snippets;
- decision package templates;
- review checklist fragments;
- prompt section fragments;
- glossary files;
- documentation fragments used by multiple agents;
- non-sensitive formatting examples.

## 3. Governance Boundary

Files in `shared/` must not be routed as execution agents.

Files in `shared/` must not grant routing authority.

Files in `shared/` must not expand tool permissions.

Files in `shared/` must not authorize production execution.

Files in `shared/` must not publish external content without human review.

## 4. Intake Status

This file is part of Phase 1 Low-risk / Documentation Agent Intake.

It is a draft documentation support file.

It is not active.

It is not a routing target.

It does not grant production execution permission.
