# Session Example 03 (Excerpt)

## Context
- Brand: Il posto delle fragole (community space for youth)
- Sector: Social innovation / Community space
- Geography: Pesaro, Italy
- Time horizon: 2030

## Phase
Brand Archeology (Phase 2) — Speculative Identity Model: Radical Values extraction

## Single question
Looking at everything the co-design process surfaced, what is the one thing this space would *never* do — even if it seemed pragmatic or popular?

## Sample answer
It would never become a space where young people are *users* of a service designed by adults. If that happens, the whole thing collapses. The ownership has to flow toward the young people, not stay with us.

## Deliverable (summary)
- MODE | PHASE: `archaeology | 2`
- Operational summary: First refusal candidate identified. Ownership asymmetry named as structural threat to core identity.
- Decisions made: "User/provider asymmetry" added to Registry of Refusals.
- Open decisions: How to encode governance that ensures youth co-ownership over time.
- Next question: What does "ownership" concretely look like for someone who's 17 and just walked in for the first time?

## Deliverable JSON (runtime-compatible example)
```json
{
  "assistant_text": "MODE: archaeology | PHASE: 2\nFirst structural refusal candidate identified from co-design output.\nWhat does ownership look like for someone who just arrived?",
  "artifact": {
    "meta": {
      "artifact_id": "artifact-posto-fragole-02",
      "phase": "2",
      "mode": "archaeology",
      "generated_at": "2026-01-15T11:30:00Z",
      "validated_by_human": true,
      "related_artifacts": ["artifact-posto-fragole-01"],
      "decision_rationale": "Co-design material consistently positioned young people as protagonists, not recipients. Refusal emerges from structural risk of adult-managed spaces defaulting to service-provider logic.",
      "evidence_refs": [
        "codesign:workshop_3_vision",
        "codesign:workshop_1_accoglienza_inclusione",
        "codesign:collage_totem_zuppa"
      ],
      "tradeoffs": [
        "Youth ownership may reduce predictability and operational efficiency in early phase.",
        "Adult partners accept slower decision cycles in exchange for structural coherence."
      ],
      "rejected_alternatives": [
        "Graduated ownership model delayed to year 2.",
        "Hybrid adult-youth governance with adult veto."
      ]
    },
    "payload": {
      "speculative_identity": {
        "radical_values": [
          {
            "id": "rv_abitability",
            "name": "Abitabilità",
            "descriptive_form": "Uno spazio in cui si sta bene",
            "operational_form": "If it doesn't improve the quality of being together, it's not a valid choice.",
            "refusal_trigger": "Any decision optimising for attendance at the cost of relational quality"
          },
          {
            "id": "rv_enabling",
            "name": "Abilitazione",
            "descriptive_form": "Accesso a strumenti e competenze",
            "operational_form": "Care is infrastructure, not assistance.",
            "refusal_trigger": "Programming decisions made without direct youth input or co-governance"
          }
        ],
        "registry_of_refusals": [
          {
            "refusal_id": "refusal_ownership_asymmetry",
            "description": "The space will not become one where young people are users of adult-designed services.",
            "trigger_condition": "Programming decisions made without direct youth input or co-governance",
            "logged_at": "phase_2_session_3",
            "source": "co-design workshop 3 — vision exercise"
          }
        ],
        "identity_tension": {
          "tension_id": "tension_care_vs_innovation",
          "pole_a": "Cura (protection, warmth, safety)",
          "pole_b": "Innovazione (technology, creative risk, experimentation)",
          "resolution": "Care redefined as infrastructure that enables power. Safety is not the opposite of risk — it is the condition that makes risk possible.",
          "resolution_type": "reframing",
          "governance_impact": "Abilitazione principle takes priority 1 alongside Abitabilità and Non giudizio."
        },
        "maieutic_question": "What does ownership look like for someone who just arrived?"
      }
    }
  }
}
```
