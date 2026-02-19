# Specula Method Agent

A facilitation layer for the Specula Method. The agent guides teams through the method one question at a time, enforces phase discipline, and produces reusable artifacts for traceability.

## Quickstart
1. Read the protocol:
   - `agent/specula-method-agent.md` (EN)
   - `agent/specula-method-agent.it.md` (IT)
2. Choose the contract profile:
   - Conceptual: `schemas/specula_session_state.json`, `schemas/specula_deliverable.json`
   - Runtime-compatible: `schemas/specula_runtime_artifact.schema.json`, `schemas/specula_runtime_step.schema.json`
3. Run a session:
   - Start in **Phase 0 (Activation)** with one question.
   - Keep explicit phase tracking (`0, 1, 1.5, 2, 3, 4, 5, 6`).
   - Produce one reusable artifact per step.

## Inputs required to start
- Sector
- Geography
- Time horizon
- Key uncertainty (at least one)

## Output contract (every step)
- `MODE: <mode> | PHASE: <phase>` header
- Operational summary (max 6 lines before question)
- Decisions made
- Open decisions
- Next single question
- Artifact JSON (conceptual or runtime-compatible profile, with explainability metadata in runtime mode)
- Advance phase only after two human approvals from distinct validator roles (runtime mode)

## Mode selection
- Maieutic (default): when inputs are vague or shallow
- Cognitive Sparring: when data is controversial or too convenient
- Values Custodian: when choices conflict with radical values
