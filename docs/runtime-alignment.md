# Runtime Alignment Guide

This note clarifies how the open `specula-method` assets align with the executable runtime profile used in `specula-framework`.

## Why two profiles

`specula-method` keeps a conceptual facilitation profile for open method documentation, and adds a runtime-compatible profile for technical integration.

- Conceptual profile: workshop-first, lightweight JSON examples.
- Runtime-compatible profile: strict `MODE | PHASE`, canonical `meta/payload` wrapper, and machine validation.

## Phase mapping

Canonical sequence used by runtime-compatible integrations (v1.1):

- `0` Activation & Governance
- `1` Framing & Ethical DNA
- `2` Scanning & Sensemaking
- `2.1` Competitive Futures Mapping
- `3` Scenario Weaving
- `4` Confrontation & Discursive Prototyping
- `5` Ethical + Impact Gate
- `6` Action Design
- `6.1` Narrative Synthesis
- `7` Platforming & Continuous Loop
- `+1` Guardian Loop (continuous)

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
