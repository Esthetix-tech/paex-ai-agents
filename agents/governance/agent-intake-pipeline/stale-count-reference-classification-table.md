# Stale Count Reference Classification Table

## 1. Positioning

- This file is documentary-only.
- This file records stale count reference classification.
- This file does not mutate stale references.
- This file does not update registry files.
- This file does not modify agent-index.md.
- This file does not modify Phase 5 artifacts.
- This file does not modify historical evidence.
- This file does not activate any agent.
- This file does not authorize routing/tool expansion.
- This file does not authorize Phase 5 entry.
- This file does not increase safe-managed count.
- This file does not mutate Sovereign index, formal approval evidence, or audit evidence.

## 2. Validated Baseline

- validated_ref: origin/main
- validated_commit: 00a8b67e7bf850ccc0919ae4c3e778ed5077dbe4
- read_only_discovery_result: PASS
- current_safe_managed_total: 53
- 183 physical agent files: NOT OBSERVED
- Phase 4E active HOLD queue: 0 / none remaining
- Sovereign index remains routing_enabled: false

## 3. Classification Principles

- Do not globally search/replace 48 -> 53.
- Historical evidence must be preserved.
- Current-state drift may be updated only under separate scope.
- Registry support drift requires Guardian Review.
- Phase 5 references remain HOLD until Phase 5 or stale-reference scope.
- Formal approval evidence / audit evidence / WORM records should not be modified in stale-count track.
- Stale count update is documentary reconciliation, not count increase.
- Current safe-managed total remains 53.

## 4. Reference Classification Table

| file path | line(s) | referenced value / term | context summary | classification | future action recommendation | Guardian Review required? | WORM risk? | mutation eligibility |
|---|---:|---|---|---|---|---|---|---|
| `agents/agent-registry/agent-index/agent-index.md` | 84 | 48 | Overall safe-managed files total remains 48 | registry support drift / candidate update with Guardian Review | future single-file update or annotation; do not mutate in this table | yes | no unless evidence / authority boundary touched | eligible under separate scope |
| `agents/agent-registry/agent-responsibility-matrix/agent-responsibility-matrix.md` | 84 | 48 | registry support draft count | registry support drift / candidate update with Guardian Review | future single-file update or annotation; do not mutate in this table | yes | no unless evidence / authority boundary touched | eligible under separate scope |
| `agents/agent-registry/capability-map/capability-map.md` | 84 | 48 | registry support draft count | registry support drift / candidate update with Guardian Review | future single-file update or annotation; do not mutate in this table | yes | no unless evidence / authority boundary touched | eligible under separate scope |
| `agents/agent-registry/layer-map/layer-map.md` | 84 | 48 | registry support draft count | registry support drift / candidate update with Guardian Review | future single-file update or annotation; do not mutate in this table | yes | no unless evidence / authority boundary touched | eligible under separate scope |
| `agents/governance/agent-intake-pipeline/phase-4-final-summary-closing-note.md` | 129, 150 | 45 | Phase 4 final historical carry-forward total | historical summary / preserve | preserve unchanged; optional future annotation only if separately scoped | yes if annotated | possible if treated as immutable evidence | preserve / annotation only |
| `agents/governance/agent-intake-pipeline/phase-5-1a-translation-localization-metadata-repair-closing-note.md` | 238 | 47 | Phase 5-1A historical count chain | Phase 5 planning drift / HOLD until Phase 5 or separate stale-reference scope | hold; do not mutate outside Phase 5/stale-reference scope | yes if updated | possible if historical evidence | HOLD |
| `agents/governance/agent-intake-pipeline/phase-5-1b-document-generator-metadata-repair-closing-note.md` | 230 | 48 | Phase 5-1B count chain | Phase 5 planning drift / HOLD until Phase 5 or separate stale-reference scope | hold; do not mutate outside Phase 5/stale-reference scope | yes if updated | possible if historical evidence | HOLD |
| `agents/governance/agent-intake-pipeline/phase-5-2-scope-discovery-closing-note.md` | 132 | 48 | Phase 5-2 total unchanged | Phase 5 planning drift / HOLD until Phase 5 or separate stale-reference scope | hold; do not mutate outside Phase 5/stale-reference scope | yes if updated | possible if historical evidence | HOLD |
| `agents/governance/agent-intake-pipeline/phase-5-partial-summary-closing-note.md` | 133 | 48 | Phase 5 partial current carry-forward | Phase 5 planning drift / HOLD until Phase 5 or separate stale-reference scope | hold; do not mutate outside Phase 5/stale-reference scope | yes if updated | possible if historical evidence | HOLD |
| `agents/governance/agent-intake-pipeline/registry-consistency-readonly-validation-closing-note.md` | 143, 161, 216 | 48 | registry validation note count | historical registry evidence / preserve or annotate only | preserve unchanged; optional annotation only if separately scoped | yes if annotated | possible if evidence record | preserve / annotation only |
| `agents/governance/agent-intake-pipeline/registry-cross-reference-repair-closing-note.md` | 87, 109 | 48 | registry cross-reference repair count | historical registry evidence / preserve or annotate only | preserve unchanged; optional annotation only if separately scoped | yes if annotated | possible if evidence record | preserve / annotation only |
| `agents/governance/agent-intake-pipeline/183-agents-master-inventory-summary.md` | multiple | 53, 28, 183 not observed, 48/45 notes | current authoritative inventory summary | current correct reference / preserve | preserve unchanged | no | no | preserve |
| `agents/governance/agent-intake-pipeline/safe-managed-count-reconciliation-note.md` | multiple | 53, 183 not observed, 48/45 notes | current authoritative count note | current correct reference / preserve | preserve unchanged | no | no | preserve |
| `agents/governance/agent-intake-pipeline/phase-4e-final-closure-summary.md` | 33, 130 | 53 | current Phase 4E closure total | current correct reference / preserve | preserve unchanged | no | no | preserve |
| `agents/governance/agent-intake-pipeline/phase-4e-hold-exclusion-register.md` | 145, 163, 181, 199, 217, 230 | 49-53 | stepwise Phase 4E contribution chain | historical evidence / preserve | preserve unchanged | no for preserve; yes if mutated | possible if treated as evidence record | preserve |
| Phase 4E repair/update closing notes | multiple | 49-53 | per-file validated count increments | historical evidence / preserve | preserve unchanged | no for preserve; yes if mutated | possible if treated as evidence record | preserve |

## 5. Priority Recommendations

1. Do not mutate historical evidence.
2. If updates are later scoped, start with `agent-index.md` as single-file update / annotation.
3. Then handle registry support draft files as tightly scoped single-file PRs.
4. HOLD Phase 5 artifacts until Phase 5 or dedicated stale-reference scope.
5. Preserve Phase 4 final summary unless annotation is separately approved.
6. Do not use global search/replace.

## 6. Count Model

- classification table count increase: 0
- future stale reference update count increase: 0
- current safe-managed total remains 53
- stale reference reconciliation is documentary reconciliation, not new safe-managed repair

## 7. Guardian / WORM

- Guardian Review required for this classification table PR: true
- Guardian Review required because this is High governance count classification documentation
- WORM Assessment: NOT REQUIRED
- WORM only required if future work mutates formal approval evidence, audit evidence, WORM records, immutable evidence, lifecycle, Sovereign index, authority boundary, runtime, or production authority
- Prior Guardian PASS is not K / CEO / Sovereign substitute

## 8. No-authority Boundary

The following are prohibited:

- stale reference mutation
- global search/replace
- historical evidence mutation
- registry mutation
- Phase 5 entry
- activation
- routing/tool expansion
- authority expansion
- formal approval evidence mutation
- audit evidence mutation
- WORM record mutation
- Sovereign index mutation
- count increase beyond 53

## 9. Required Controls

### allowed_actions

- record_stale_reference_discovery_results
- classify_stale_count_references
- separate_historical_from_current_state
- preserve_historical_evidence
- recommend_future_single_file_updates
- preserve_no_authority_boundary
- record_count_model

### evidence_required

- safe_managed_count_reconciliation_note_reference
- master_inventory_summary_reference
- discovered_reference_inventory
- classification_table
- no_authority_boundary_statement
- future_scope_boundary_statement

### forbidden_actions

- mutate_stale_references_during_classification
- global_search_replace_count_values
- mutate_historical_evidence_without_scope
- mutate_formal_approval_evidence
- mutate_audit_evidence
- mutate_worm_records
- mutate_sovereign_index
- mutate_registry_without_guardian_review
- mutate_phase_5_artifacts_without_scope
- treat_stale_reference_update_as_count_increase
- treat_count_reconciliation_as_activation
- treat_count_reconciliation_as_phase_5_entry
- activate_agent
- expand_routing_authority
- expand_tool_permissions
- add_runtime_authority
- add_production_authority

## 10. Remaining Risks

- Registry support files still contain current-state drift until separately updated.
- Phase 5 artifacts still contain older count chain.
- Historical references must be preserved.
- Future mutation requires tight scope and Guardian Review.
- WORM risk may appear if immutable evidence is touched.

## 11. Router Decision

- PROCEED for documentary-only stale count reference classification table.
- HOLD for stale reference mutation until separately scoped.
- HOLD for Phase 5.
- HOLD for activation.
- HOLD for routing/tool expansion.
- HOLD for authority expansion.
- HOLD for count increase beyond 53.
