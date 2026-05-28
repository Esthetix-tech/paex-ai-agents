---
name: Secondary Hooks Map
title: PAEX-AI Secondary Hooks Map
description: Defines mandatory secondary hooks for risk domains, ensuring high-risk Mission, Core or Platform tasks attach required Guardian, WORM, Canary, Human Override or Sovereign controls.
layer: agent-registry
context_layer: Repository Governance
pace_layer: Repository Governance / Secondary Hooks
risk_level: high
status: active
owner: Agent Repository Steward
review_required: true
human_approval_required: true
requires_human_approval: true
human_approval_scope:
  - file_activation
  - hooks_policy_change
  - mandatory_hook_exception
  - high_or_critical_hook_override_request
  - sensitive_domain_hook_change
codex_autofix_allowed: limited
tool_permissions: metadata_only
routing_enabled: false
registry_enabled: true
version: v1.4-lock-candidate
requires_worm: true
worm_scope:
  - file_activation
  - hooks_policy_change
  - mandatory_hook_exception
  - high_or_critical_hook_override_request
  - sensitive_domain_hook_change
requires_guardian_review: true
secondary_hooks:
  - registry-maintenance-review
  - governance-review
  - ci-validation-review
forbidden_actions:
  - allow_high_or_critical_without_mandatory_hooks
  - suppress_worm_for_auditable_actions
  - bypass_guardian_review
  - treat_hooks_as_optional_for_sensitive_domains
  - downgrade_hooks_because_agent_is_capable
allowed_actions:
  - define_secondary_hooks
  - map_risk_triggers_to_controls
  - require_guardian_review_for_sensitive_domains
  - require_worm_for_auditable_actions
  - identify_hook_inheritance_requirements
evidence_required:
  - frontmatter_schema_validation
  - related_files_path_check
  - duplicate_frontmatter_key_check
  - hook_trigger_coverage_check
  - risk_level_map_alignment
  - ci_validation_result
  - guardian_review_record
  - human_approval_record
rollback_required: true
canary_required: false
exemption_reason: secondary_hooks_policy_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
related_files:
  - ../../../AGENTS.md
  - ../../../README.md
  - ../../../AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - ../risk-level-map/risk-level-map.md
  - ../agent-router/agent-router.md
  - ../frontmatter-schema/frontmatter-schema.md
  - ../registry-maintenance-policy/registry-maintenance-policy.md
  - ../../_quarantine/quarantine-policy/quarantine-policy.md
  - ../../governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - ../../governance/worm-event-schema/worm-event-schema.md
  - ../../sovereign/governance-protocols-index/governance-protocols-index.md
---

# Secondary Hooks Map｜PAEX-AI Secondary Hooks Map

## 1. Purpose

This file defines mandatory secondary hooks for Medium, High and Critical tasks.

A secondary hook is an additional review, control, evidence, approval, logging or rollout mechanism required when a task touches a sensitive domain.

Core rule:

> Capability match alone is never enough. High-risk work must attach the right hooks before execution.

Plain-language interpretation:

> 會做不代表可以直接做。高風險任務要先掛煞車、黑盒子、審查人與回滾方案。

---

## 2. Hook Types

| Hook Type | Purpose |
|---|---|
| Guardian Review | Independent E-layer review, veto or verification |
| WORM Event | Immutable or audit-style event record |
| Canary | Controlled rollout with limited blast radius |
| Human Approval | Explicit decision by K / CEO or authorized owner |
| Sovereign Package | Company-level arbitration or irreversible decision package |
| Kill Switch | Emergency shutdown or controlled release mechanism |
| Oracle Verification | Evidence-based validation against trusted source |
| Data Boundary Review | Privacy, PII, access and retention check |
| Rollback Plan | Defined path to reverse or contain change |
| Counter-Metrics | Metrics that reveal harm, not only success |
| Quarantine Review | Repair and restore process for unsafe files |
| Guardian Purity Audit | Ensures Guardian is not acting as hidden executor |
| Core Contamination Check | Prevents application-specific logic from entering ESTRIX Core |
| Tool Permission Review | Verifies MCP / tool access and blast radius |
| Production Readiness Gate | Confirms evidence before production impact |

---

## 3. Mandatory Hook Table

| Trigger / Domain | Minimum Risk | Mandatory Hooks | Notes |
|---|---:|---|---|
| Ledger-adjacent work | High | Ledger Guardian + WORM + rollback plan | Includes reporting that may affect ledger interpretation |
| Core ledger mutation | Critical | Ledger Guardian + Finance Guardian + WORM + Sovereign Package + Human Approval | No autonomous execution |
| Payment logic | Critical | Finance Guardian + Security Guardian + WORM + idempotency proof + Human Approval | Duplicate charge risk |
| Refund logic | High / Critical | Finance Guardian + Customer Trust Review + WORM + rollback plan | Include partial failure path |
| Pricing / Take Rate | High | Finance Guardian + Legal / Compliance Review + Canary + WORM | Impacts revenue and trust |
| Coupon / promotion logic | High | Finance Guardian + Abuse Review + Canary | Prevent leakage and fraud |
| Booking / scheduling logic | High | Reliability Guardian + concurrency check + rollback plan | Double-booking risk |
| M_C01 15-Min Grid | Critical | Scheduling Guardian + WORM + load / concurrency test + Human Approval | Core scheduling infrastructure |
| Production database migration | High / Critical | Architecture Guardian + Data Guardian + backup + rollback + staging verification | Destructive change = Critical |
| Destructive DB operation | Critical | BLOCK unless explicit Human Approval + backup + rollback + WORM | Default no autonomous execution |
| API contract change | High | Architecture Guardian + compatibility test + changelog | External consumers may break |
| Production write action | High / Critical | Production Readiness Gate + WORM + rollback plan | Depends on blast radius |
| MCP tool exposure | High | Security Guardian + Tool Permission Review + audit logging | Tool capability must match permissions |
| Agent permission expansion | High / Critical | Agent Drift Review + Security Guardian + WORM | Critical if broad or production-write |
| Quarantined file restore | High | Quarantine Policy + Registry Maintenance Policy + Human Review | Never auto-restore Medium+ |
| Guardian role ambiguity | High | Guardian Purity Audit | Prevent hidden execution layer |
| Human Override | High / Critical | Human Override Accountability + WORM | Override must not be invisible |
| Guardian Veto override | Critical | Sovereign Package + Human Approval + WORM | Requires explicit risk ownership |
| Kill Switch release | Critical | Kill Switch Governor + Sovereign Agent + Human Approval + WORM | No autonomous release |
| Public brand content | High | Brand Guardian + Compliance Guardian | External trust impact |
| Public crisis statement | Critical | Sovereign Package + Brand Guardian + Legal Review + K approval | No autonomous release |
| Automated external publishing | High | Brand Guardian + Canary + WORM + rollback/takedown plan | Social, ads, email |
| Large-scale paid media spend | Critical | Finance Guardian + Data Audit Guardian + Brand Guardian + Canary + Human Approval | Budget blast radius |
| Healthcare marketing content | Critical | Healthcare Compliance Guardian + Medical Review + Legal Review | Strict claim control |
| Medical / clinical judgment | Critical | BLOCK or escalate to qualified professional | Agent must not diagnose |
| Legal advice boundary | Critical | Legal Guardian + human professional review | Agent may draft, not give final advice |
| Tax / invoice logic | High / Critical | Tax Guardian + Finance Guardian + WORM | May affect filings and liability |
| HR hiring / termination | High / Critical | Talent Governance Guardian + Legal Review + Human Approval | Termination = Critical |
| PII handling | High | Privacy Guardian + Data Boundary Review + minimization | Masking preferred |
| KYC / AML | Critical | Compliance Guardian + WORM + Human Approval | Regulated domain |
| Identity graph merge/split | High / Critical | Data Governance Guardian + WORM + reversible proposal | Wrong merge is dangerous |
| Identity trust root change | Critical | Security Guardian + Sovereign Package + WORM + Human Approval | Root trust boundary |
| Model release | High | Model Risk Guardian + Production Readiness Gate + monitoring | Drift / fairness |
| Security incident affecting customers | Critical | Security Guardian + Incident Commander + Sovereign Package + WORM | Escalate |
| IoT control | High / Critical | Reliability Guardian + Security Guardian + fail-safe plan | Physical-world impact |
| XR cockpit / high-risk human factors | Critical | Human Factors Guardian + Safety State Machine + Emergency Override | Safety and cognition risk |
| ESTRIX Core module change | High | ESTRIX Core Steward + Architecture Guardian + regression check | Reusable engine impact |
| SoMatch / SHINES logic entering ESTRIX Core | High | Core Contamination Check + ESTRIX Core Steward | Prevent application pollution |
| L3 Application redefines ESTRIX | High | ESTRIX Core Steward + Business Architecture Review | Prevent boundary collapse |
| L4 Engagement redefines architecture | High | Business Architecture Review + ESTRIX Core Steward | Prevent one-time work from rewriting system |
| New Use Case creation | Medium / High | ESTRIX Core Steward + relevant Guardian(s) | Risk depends on domain |
| New external business model | Critical | K / CEO approval + Sovereign Package + legal/finance review | L0 decision |
| Business architecture layer ambiguity | Medium / High | HOLD + proposed classification | Use HOLD format |
| Registry rule change | High / Critical | Registry Maintenance Policy + WORM + Human Review | Critical if routing authority changes |
| Frontmatter schema change | High | Registry Maintenance Review + CI validation | May affect all files |
| Agent router change | High / Critical | Registry Maintenance Review + WORM + Human Review | Critical if routing authority changes |
| Secondary hooks map change | High / Critical | Governance Review + CI validation | Controls high-risk routing |
| Risk-level-map change | High / Critical | Governance Review + Human Review | Controls risk classification |
| Quarantine policy change | High | Registry Maintenance Review + Quarantine Review | Controls unsafe file restoration |

---

## 4. Required Hook Output

For High / Critical tasks, Codex must output:

```text
Required Hooks:
WORM Event Needed:
Guardian Review Needed:
Canary / Rollback Needed:
Router Decision:
```

If hooks are missing, Codex must return `HOLD`, `BLOCK`, or `ESCALATE`.

---

## 5. Hook Failure Conditions

Return `BLOCK` when the task asks to bypass legal, security or privacy boundaries, requests irreversible action without human approval, suppresses WORM or audit records, asks a Guardian to execute production work, asks a Mission Agent to self-approve High / Critical work, attempts public crisis statement without approval, attempts destructive production action without explicit approval and rollback plan, routes quarantined files as active, or executes medical diagnosis / final legal advice through Agent.

Return `HOLD` when hook requirement is clear but evidence is missing, correct Guardian is unclear, business layer is unclear, risk level is TBD, registry/frontmatter conflict exists, or semantic review is needed for Core / Application / Engagement boundary.

Return `ESCALATE` when K / CEO, Sovereign or authorized owner must decide.

---

## 6. Hook Inheritance Rule

If one task touches multiple triggers, Codex must attach the strictest combined hook set.

Example:

```text
Task: automated paid media campaign using customer PII and public brand claims.
Required Hooks:
- Brand Guardian
- Compliance Guardian
- Privacy Guardian
- Data Boundary Review
- Canary
- WORM
- Finance Guardian if budget is material
```

Do not choose only the easiest hook.

---

## 7. Final Rule

> Hooks are not bureaucracy. Hooks are the safety harness that allows Esthetix to scale automation without scaling chaos.
