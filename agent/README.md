# Specula Method Agent

A facilitation layer for the Specula Method. The agent guides teams through the method one question at a time, enforces phase discipline, and produces reusable artifacts for traceability.

## Quickstart
1. Read the protocol:
   - `agent/specula-method-agent.md` (EN)
   - `agent/specula-method-agent.it.md` (IT)
2. Use the output contract and store artifacts as JSON:
   - `schemas/specula_session_state.json`
   - `schemas/specula_deliverable.json`
3. Run a session:
   - Start in Phase 1 with a single question.
   - Update the session state after every user response.
   - Produce a deliverable after each step.

## Inputs required to start
- Sector
- Geography
- Time horizon
- Key uncertainty (at least one)

## Output contract (every step)
- Operational summary (max 10 lines)
- Decisions made
- Open decisions
- Next single question
- Session JSON + Deliverable JSON

## Mode selection
- Maieutic (default): when inputs are vague or shallow
- Cognitive Sparring: when data is controversial or too convenient
- Values Custodian: when choices conflict with radical values

