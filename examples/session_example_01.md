# Session Example 01 (Excerpt)

## Context
- Brand: ExampleCo
- Sector: Circular retail
- Geography: EU
- Time horizon: 2035

## Phase
Scenario Generation — Step 1

## Single question
What sector are we working in and what time horizon are we using (e.g., 2030/2035)?

## Sample answer
Circular retail in the EU, 2035.

## Deliverable (summary)
- Operational summary: Defined sector and time horizon for scenario work.
- Decisions made: Sector = Circular retail; Geography = EU; Time horizon = 2035.
- Open decisions: Key uncertainty; dominant axes; weak signals.
- Next question: Which variable today scares or excites you most?

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
    "step": 1
  },
  "output": {
    "operational_summary": "Defined sector and time horizon for scenario work.",
    "decisions_made": [
      "Sector: Circular retail",
      "Geography: EU",
      "Time horizon: 2035"
    ],
    "decisions_open": [
      "Key uncertainty",
      "Dominant axes",
      "Weak signals"
    ],
    "next_question": "Which variable today scares or excites you most?"
  },
  "artifacts": {
    "session_state": "specula_session_state.json"
  },
  "log": [
    {
      "ts": "2026-01-29",
      "event": "DELIVERABLE",
      "content": "Phase 1 Step 1 deliverable generated."
    }
  ]
}
```
