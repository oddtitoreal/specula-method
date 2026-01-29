# Session Example 02 (Excerpt)

## Context
- Brand: ExampleCo
- Sector: Circular retail
- Geography: EU
- Time horizon: 2035

## Phase
Scenario Generation — Step 2

## Single question
Which variable today scares or excites you most?

## Sample answer
The speed of EU regulation on AI-driven pricing.

## Deliverable (summary)
- Operational summary: Captured key uncertainty around regulation speed.
- Decisions made: Key uncertainty = EU AI pricing regulation pace.
- Open decisions: Second uncertainty for scenario axes; weak signals.
- Next question: Which second uncertainty would you pair with it to build scenarios?

## Deliverable JSON (example)
```json
{
  "meta": {
    "method": "SPECULA",
    "version": "0.1",
    "language": "en-US"
  },
  "phase": {
    "current": "SCENARIOS",
    "step": 2
  },
  "output": {
    "operational_summary": "Captured key uncertainty around regulation speed.",
    "decisions_made": [
      "Key uncertainty: EU AI pricing regulation pace"
    ],
    "decisions_open": [
      "Second uncertainty for scenario axes",
      "Weak signals"
    ],
    "next_question": "Which second uncertainty would you pair with it to build scenarios?"
  },
  "artifacts": {
    "session_state": "specula_session_state.json"
  },
  "log": [
    {
      "ts": "2026-01-29",
      "event": "DELIVERABLE",
      "content": "Phase 1 Step 2 deliverable generated."
    }
  ]
}
```
