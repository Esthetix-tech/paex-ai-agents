
---

# 2. `shared/README.md`

```markdown
---
name: shared-readme
title: PACE-AI Shared README
description: Defines the purpose, boundaries and routing restrictions of the shared folder for reusable templates, snippets, vocabulary and non-agent supporting materials.
layer: shared
pace_layer: Repository Governance / Shared Support
risk_level: medium
status: active
owner: Agent Repository Steward
review_required: true
human_approval_required: false
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: false
version: v1.0
related_files:
  - agent-registry/frontmatter-schema/frontmatter-schema.md
  - agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
  - agent-registry/agent-router/agent-router.md
  - agent-registry/layer-map/layer-map.md
  - agent-registry/risk-level-map/risk-level-map.md
  - _quarantine/quarantine-policy/quarantine-policy.md
---

# PACE-AI Shared README

## 1. Purpose

The `shared/` folder stores reusable support materials for the PACE-AI Agent Repository.

It is used for common templates, shared language, reusable snippets, vocabulary lists, formatting examples, reference fragments and non-routing support assets.

Core rule:

> `shared/` supports agents, protocols and governance files. It does not become an agent, governance authority or router target by itself.

This folder is a shared toolbox, not an operating role.

---

## 2. What Belongs in `shared/`

The following materials may be stored in `shared/`:

- Common markdown templates.
- Reusable YAML frontmatter examples.
- Shared terminology lists.
- Naming conventions.
- Standard output snippets.
- Decision package templates.
- Review checklist fragments.
- Prompt section fragments.
- Common glossary files.
- Style conventions.
- Documentation fragments used across multiple agents.
- Non-sensitive examples for testing formatting.
- Common tables used by multiple files.
- Reusable Codex instruction fragments.
- Standard final definition blocks.
- Standard Codex handling rule blocks.
- Common risk vocabulary.
- Common status vocabulary.
- Common routing examples.
- Non-authoritative example outputs.

Example structure:

```text
shared/
├─ templates/
│  ├─ agent-role-spec-template.md
│  ├─ governance-protocol-template.md
│  ├─ sovereign-playbook-template.md
│  └─ decision-output-template.md
├─ glossary/
│  ├─ pace-terms.md
│  ├─ risk-terms.md
│  └─ governance-terms.md
├─ snippets/
│  ├─ codex-handling-rules.md
│  ├─ final-definition-block.md
│  ├─ worm-required-notice.md
│  └─ guardian-review-required-notice.md
└─ examples/
   ├─ frontmatter-example.md
   ├─ review-output-example.md
   └─ decision-package-example.md