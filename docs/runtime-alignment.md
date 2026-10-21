# Runtime Alignment Guide

This note clarifies how the open `specula-method` assets align with the executable runtime profile used in `specula-framework`.

## Why two profiles

`specula-method` keeps a conceptual facilitation profile for open method documentation, and adds a runtime-compatible profile for technical integration.

- Conceptual profile: workshop-first, lightweight JSON examples.
- Runtime-compatible profile: strict `MODE | PHASE`, canonical `meta/payload` wrapper, and machine validation.

## Phase mapping

Canonical sequence used by runtime-compatible integrations (v2.0). It matches the `phase` values of the schemas in `specula-framework/schemas/`:

- `0` Threshold & Framing (`phase0_activation`)
- `1` Scenario Generation (`phase1_scenarios`)
- `1.5` Competitive Futures Mapping (`phase1_5_competitive_map`)
- `2` Brand Archaeology & Value Stress Test (`phase2_brand_dna`)
- `3` Future Prototyping & Ethical + Impact Gate (`phase3_prototypes`, `phase3_refusals`)
- `4` Narrative Synthesis & Strategic Protocol (`phase4_narrative_system`, `preferable_future`, `decision_log`)
- `5` Co-creation & Community Governance (`phase5_cocreation`)
- `6` Activation & Specula Guardian (`phase6_guardian`)

The v1.1 sequence (seven phases plus Guardian Loop) is retired. Its mapping to v2.0 is in [Method Overview](./method-overview.md#phase-mapping-v11--v20).

## Fields added in framework 1.3

Framework 1.3 adds optional fields that carry the v2.0 method into runtime artifacts:

- `phase0_activation`: research question, time window, working rules, written consensus, threshold evidence
- `phase1_scenarios`: generic future archetype, closed megatrends, open variables, value the scenario is built against; `preferred` deprecated as `scenario_type`
- `phase2_brand_dna`: operational form of each value, stress-test result per scenario with reviewer, documented decisions with source type, counterexamples, fragile values, candidate values that fell
- `phase6_guardian`: drift classification with the rule applied, composite alerts, escalation owner and deadline
- New `decision_log` and `preferable_future` artifacts

## Schema profile mapping

- Conceptual:
  - `schemas/specula_session_state.json`
  - `schemas/specula_deliverable.json`
- Runtime-compatible:
  - `schemas/specula_runtime_artifact.schema.json`
  - `schemas/specula_runtime_step.schema.json`

## Minimal runtime output contract

1. First line header: `MODE: <mode> | PHASE: <phase>`
2. Maximum 6 lines before the question line
3. Exactly one question per step
4. Artifact uses canonical wrapper:
5. `meta` includes explainability fields: `decision_rationale`, `evidence_refs`, `tradeoffs`, `rejected_alternatives`
6. Phase advancement requires at least two human approvals from distinct validator roles

```json
{
  "meta": {
    "artifact_id": "...",
    "phase": "...",
    "mode": "...",
    "generated_at": "...",
    "validated_by_human": false,
    "related_artifacts": [],
    "decision_rationale": "...",
    "evidence_refs": ["..."],
    "tradeoffs": ["..."],
    "rejected_alternatives": ["..."]
  },
  "payload": {}
}
```
