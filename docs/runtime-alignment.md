# Runtime Alignment Guide

This note clarifies how the open `specula-method` assets align with the executable runtime profile used in `specula-framework`.

## Why two profiles

`specula-method` keeps a conceptual facilitation profile for open method documentation, and adds a runtime-compatible profile for technical integration.

- Conceptual profile: workshop-first, lightweight JSON examples.
- Runtime-compatible profile: strict `MODE | PHASE`, canonical `meta/payload` wrapper, and machine validation.

## Phase mapping

Canonical sequence used by runtime-compatible integrations:

- `0` Activation
- `1` Scenario Generation
- `1.5` Competitive Futures Mapping
- `2` Brand Archeology
- `3` Prototyping + Ethical Gate
- `4` Narrative Synthesis
- `5` Community Co-Creation
- `6` Guardian Monitoring

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

```json
{
  "meta": {
    "artifact_id": "...",
    "phase": "...",
    "mode": "...",
    "generated_at": "...",
    "validated_by_human": false,
    "related_artifacts": []
  },
  "payload": {}
}
```

