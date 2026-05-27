---
name: agents-readme
title: PAEX-AI Agents Repository README
description: Root-level architecture and governance guide for the PAEX-AI agents repository, defining repository purpose, Business Architecture Context Stack, C-A-E-P agent layers, routing principles, frontmatter discipline, risk classification, secondary hooks, quarantine policy, PR / CI validation and v1.4 activation rules.
layer: agent-registry
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
registry_enabled: false
version: v1.4-candidate-patch-01
requires_worm: true
worm_scope:
  - readme_activation
  - repository_governance_baseline_change
  - v1_4_activation
  - architecture_layer_change
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
rollback_required: true
canary_required: false
related_files:
  - AGENTS_BUSINESS_ARCHITECTURE_RULE.md
  - 00_command/K_COMMAND_CENTER.md
  - 10_esthetix_arsenal/ESTHETIX_ARSENAL_CONTEXT.md
  - 10_esthetix_arsenal/ESTHETIX_GOVERNANCE_OS.md
  - 20_estrix_core/ESTRIX_CORE_ENGINE_CONTEXT.md
  - 20_estrix_core/ESTRIX_EXTENSION_POLICY.md
  - 20_estrix_core/ESTRIX_MODULE_REGISTRY.md
  - 20_estrix_core/ESTRIX_USE_CASE_REGISTRY.md
  - agent-registry/frontmatter-schema/frontmatter-schema.md
  - agent-registry/registry-maintenance-policy/registry-maintenance-policy.md
  - agent-registry/agent-router/agent-router.md
  - agent-registry/layer-map/layer-map.md
  - agent-registry/risk-level-map/risk-level-map.md
  - agent-registry/secondary-hooks-map/secondary-hooks-map.md
  - governance/core-governance-protocols/core-governance-protocols.md
  - governance/pr-ci-validation-checklist/pr-ci-validation-checklist.md
  - governance/worm-event-schema/worm-event-schema.md
  - sovereign/governance-protocols-index/governance-protocols-index.md
  - _quarantine/quarantine-policy/quarantine-policy.md
exemption_reason: repository_readme_only_no_direct_production_execution
exemption_scope:
  - canary_not_required_for_non_release_documentation_policy
exemption_approved_by: K / CEO
delegated_reviewer: Agent Repository Steward
exemption_review_required: true
exemption_review_date: 2026-05-26
---

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