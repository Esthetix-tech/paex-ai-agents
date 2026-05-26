---
name: Registry Maintenance Policy
title: PACE-AI Agent Registry Maintenance Policy
description: Defines how the agent registry, router, responsibility matrix, capability map, layer map, risk map and secondary hooks are maintained, reviewed, repaired and audited.
layer: agent-registry
pace_layer: Platform / Repository Governance
risk_level: high
status: stable
owner: Agent Repository Steward
review_required: true
human_approval_required: true
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.0
related_files:
  - agent-registry/agent-index.md
  - agent-registry/agent-responsibility-matrix.md
  - agent-registry/agent-router.md
  - agent-registry/capability-map.md
  - agent-registry/layer-map.md
  - agent-registry/risk-level-map.md
  - agent-registry/secondary-hooks-map.md
  - agent-registry/frontmatter-schema.md
  - governance/core-governance-protocols.md
  - governance/guardian-review-coordinator.md
  - governance/agent-drift-review.md
  - governance/production-readiness-gate.md
  - _quarantine/README.md
  - _quarantine/quarantine-policy.md
---

# PACE-AI Agent Registry Maintenance Policy

## 1. Purpose

This file defines how the `agents/agent-registry/` layer is maintained, reviewed, repaired and audited.

The Agent Registry is the dispatch brain of the `agents/` repository.

It tells Codex, human operators, orchestration tools and future automation layers:

- which Agents exist;
- where each Agent lives;
- what each Agent owns;
- what each Agent must not own;
- what each Agent can safely do;
- what risk level each Agent carries;
- which files may be routed;
- which files are only governance references;
- which Guardian or governance protocol must be attached;
- which files are quarantined, deprecated or retired.

Core rule:

> The registry must reflect operational truth. If the registry lies, the router becomes dangerous.

This policy exists to prevent repository drift from becoming governance failure.

A wrong registry entry can cause:

- the wrong Agent to receive a task;
- a Mission Agent to self-review High Risk work;
- a quarantined file to be treated as active;
- a draft file to receive production routing;
- a High Risk workflow to bypass Guardian Review;
- a Critical workflow to appear automatable;
- a duplicate Agent to create unclear ownership;
- Codex to repair metadata while accidentally expanding authority.

Therefore, registry maintenance is not clerical cleanup.

It is authority control.

---

## 2. Governance Positioning

The Agent Registry belongs to the `agent-registry` repository layer and functions as a Platform / Repository Governance control surface.

It is not itself a Mission Agent.

It does not execute frontline work.

It does not approve business decisions.

It does not override Guardian or Sovereign governance.

Its job is to ensure that routing, responsibility, capability, risk and layer placement remain accurate.

In PACE-AI terms:

| Registry Function | Governance Meaning |
|---|---|
| Agent index | Identity control |
| Responsibility matrix | Ownership control |
| Router | Dispatch control |
| Capability map | Capability visibility |
| Layer map | Authority boundary control |
| Risk-level map | Risk classification control |
| Secondary hooks map | Companion review and escalation control |
| Frontmatter schema | Metadata contract |
| Maintenance policy | Registry governance law |

The registry must be maintained as a source of truth.  
If the registry and the actual file content conflict, the conflict must be resolved before production routing.

---

## 3. Controlled Registry Files

This policy governs the following files.

| File | Function | Governance Risk |
|---|---|---|
| `agent-index.md` | Canonical list of active, draft, stable, deprecated, retired and quarantined Agents / artifacts. | If wrong, the system may believe nonexistent or unsafe capabilities are available. |
| `agent-responsibility-matrix.md` | Defines primary ownership, non-ownership, escalation paths and final decision boundaries. | If wrong, accountability becomes blurred. |
| `agent-router.md` | Defines task-to-Agent routing logic. | If wrong, tasks may go to unsafe or unauthorized Agents. |
| `capability-map.md` | Maps capability tags to Agents and support files. | If wrong, capabilities may be overstated or duplicated. |
| `layer-map.md` | Defines PACE layer placement and boundary rules. | If wrong, Agents may operate at the wrong authority layer. |
| `risk-level-map.md` | Defines risk classification standards and Agent-level risk mapping. | If wrong, High / Critical workflows may be under-controlled. |
| `secondary-hooks-map.md` | Defines companion reviewers, fallback Agents and mandatory governance hooks. | If wrong, workflows may bypass Guardian, WORM, Canary or Kill Switch controls. |
| `frontmatter-schema.md` | Defines the required metadata contract for formal files. | If wrong, the registry loses identity and authority consistency. |
| `registry-maintenance-policy.md` | Defines this maintenance policy. | If weakened, the entire registry can drift. |

These files should be treated as controlled governance artifacts.

Codex may propose repairs, but should not silently rewrite their authority model.

---

## 4. Maintenance Principles

## 4.1 Single Source of Registry Truth

No Agent or governance artifact should be considered production-ready unless it is represented consistently across the required registry surfaces.

For a stable routable Agent, the following must agree:

- YAML frontmatter;
- file path;
- `agent-index.md`;
- `agent-responsibility-matrix.md`;
- `agent-router.md`;
- `capability-map.md`;
- `layer-map.md`;
- `risk-level-map.md`;
- `secondary-hooks-map.md`, if applicable.

If these disagree, the registry is not safe.

Example:

```text
File says:
risk_level: high

risk-level-map says:
medium

router routes it as:
low-risk automation

Result:
Registry conflict. Must be repaired before routing.