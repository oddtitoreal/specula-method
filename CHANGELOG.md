# Changelog

All notable changes to the Specula Method open documentation will be documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2026-10-21

### Changed
- `docs/method-overview.md`: v2.0 rewrite. One canonical six-phase sequence shared with `specula-bos` and the `specula-framework` schemas (`0`, `1`, `1.5`, `2` to `6`). Framing moves to Phase 0; the Ethical DNA moves after Scenario Generation, into Phase 2 (Brand Archaeology & Value Stress Test). Breaking change: the v1.1 seven-phase sequence is retired, with a mapping table v1.1 → v2.0.
- `docs/method-overview.md`: Phase 0 records threshold conditions with observable evidence and closes with a written consensus on research question, time window and working rules. Scenario construction rule (four generic futures, closed megatrends shared, one scenario against the strongest declared value, horizon 10–15 years). Value Stress Test on the operational form of values, judged by people who did not build the scenarios, with Causal Layered Analysis as second method. Preferable future designed in Phase 4 with backcasting. Decision criteria as hypotheses with expected effect and review date; Decision Log. Drift classification (error, superseded model, learning). Radar alerts on combinations of indicators. New section "Time and Compression". Metrics with calculation procedures. New role: External Reviewer.
- `README.md`: six-phase section aligned to v2.0, Phase 0 added; ecosystem table lists five repositories, `specula-handbook` included.
- `docs/runtime-alignment.md`: phase mapping restored to the runtime schema phases; fields added in `specula-framework` 1.3 listed.
- `docs/ai-governance.md`: scenario governance follows the construction rule; the preferable future is designed in Phase 4; Phase 2 review by people outside the scenario team; drift classification in Phase 6.
- `docs/ethical-framework.md`: the Ethical + Impact Gate closes Phase 3.
- `docs/community-co-creation-protocol.md` (1.1): new section on who sets the values, with three counterweights and speaking rules; corrected phase reference for speculative futures (Phase 1).
- `examples/session_example_01.md`: horizon 2036; `scenario_type` `exploratory` with `archetype` `discipline` (`preferred` is deprecated in `specula-framework` 1.3).

### Added
- `docs/method-evolution.md`: v2.0 entry.

## [1.1.0] - 2026-06-04

### Added
- `docs/method-overview.md` — Full v1.1 rewrite integrating the v2.4.5.2 evolution track: new Phase 0 (Activation & Governance), Phase 4 (Confrontation & Discursive Prototyping), Phase 7 (Platforming & Continuous Loop); explicit roles (human + AI); anti-fuffa metrics; 4–6 week implementation checklist; phase mapping table v1.0→v1.1.
- `docs/ethical-framework.md` — Impact Assessment Layer: systematic evaluation of social, environmental, reputational, legal, robustness, and feasibility dimensions before any GO decision. Version bumped to 2.4.5.

### Changed
- `docs/method-overview.md` — Framing & Ethical DNA (formerly Brand Archeology) moved to Phase 1, before Scanning. Ethical + Impact Gate replaces standalone Ethical Gate. Narrative Synthesis demoted to sub-phase 6.1 of Action Design. Co-creation integrated into Phase 4 + Phase 7.
- `docs/method-evolution.md` — v1.1 entry added with full rationale and source attribution.
- `docs/runtime-alignment.md` — Phase mapping updated to v1.1 canonical sequence (7 phases + Guardian Loop).

### Removed
- Dependency on `specula-framework/docs/08_specula_method_v2_3.md` and `14_specula_method_v2_4_5_2_aligned.md` — those files are retired. `specula-method` is now the single source of truth for the method.

### Added (2026-03-27)
- `docs/community-co-creation-protocol.md` — Community Co-Creation Protocol (Phase 5 operational specification). Documents: when Phase 5 is mandatory vs. optional, the three-step engagement process (preparation → dialogue → structured synthesis), dissociation typology and escalation protocol, participation tracking requirements, Guardian Loop integration, and clear boundaries of what is NOT co-creation. Closes the "consultazione teatro" gap identified in the integrated analysis.

### Added
- Initial public release of ethical framework
- Operational templates for all six phases
- Pilot project case study: EcoCosmesi (anonymized natural cosmetics brand) that informed method development
- Contributing guidelines
- Added CC BY-SA 4.0 license file and attribution requirements.
- Specula Method Agent protocol (EN/IT) for facilitated sessions.
- Method Evolution Log defining the progressive evolution of the method.
- Agent runtime structure (`agent/`) and conceptual schemas (`schemas/`).
- Added conceptual deliverable JSON template for session outputs.
- Added agent quickstart and example sessions in `examples/`.
- Added `ATTRIBUTION.md` as the canonical attribution reference.
- Added `examples/README.md` with format conventions.
- Runtime-compatible schema profile:
  - `schemas/specula_runtime_artifact.schema.json`
  - `schemas/specula_runtime_step.schema.json`
- `docs/runtime-alignment.md` documenting conceptual vs runtime-compatible contracts.
- GitHub Actions CI workflow to validate schema JSON parsing and relative Markdown links.
- Runtime schema explainability metadata fields in canonical wrapper:
  - `meta.decision_rationale`
  - `meta.evidence_refs`
  - `meta.tradeoffs`
  - `meta.rejected_alternatives`

### Changed
- Clarified Full Journey phase list to match six-phase structure.
- Standardized repository name in README title.
- Aligned AI governance phase label with Activation & Guardian naming.
- Consolidated licensing under CC BY-SA 4.0 in `LICENSE.md`.
- Updated agent protocols (EN/IT) to canonical phase sequence (`0, 1, 1.5, 2, 3, 4, 5, 6`).
- Updated agent output contract to strict header (`MODE | PHASE`) and 6-line pre-question limit.
- Updated `agent/README.md` quickstart to include profile selection and Phase 0 start.
- Updated docs index to include runtime alignment guide and runtime schemas.
- Updated session examples to runtime-compatible deliverable format.
- Clarified method overview/FAQ wording for runtime-compatible integration with `specula-framework`.
- Updated case-studies index to reference EcoCosmesi pilot project.
- Bumped agent protocol label in EN/IT docs from `v0.2` to `v0.3` to reflect current contract constraints.
- Added `v1.0.1` entry in Method Evolution Log to capture runtime-alignment patch scope.
- Updated repository version metadata marker to February 2026 in `README.md`.
- Clarified runtime advancement rule in agent/runtime docs: phase progression requires at least two human approvals from distinct validator roles.

## [1.0.0] - 2026-01-25

### Added
- Ethical Framework with three-question gate
- Registry of Refusals template and example
- Speculative Identity Canvas
- Competitive Futures Mapping template
- Resilience Protocol (four-scenario stress test)
- Impact Measurement Framework
- AI Governance principles
- Complete README with method overview

### Documentation
- Method overview (six phases)
- AI governance guidelines
- Investment framework overview
- FAQ for practitioners and organizations

---

## Version History Notes

**Version 1.0.0** represents the first public release of the Specula Method ethical framework and templates. It originates from the private v2.3 baseline and is progressively aligned with the private v2.4.5.x track via explicit mapping and runtime-compatible contracts.

Major versions (2.0.0, 3.0.0) will be released when:
- Fundamental changes to the ethical framework structure
- New phases added or phases substantially restructured
- Breaking changes to template formats

Minor versions (1.1.0, 1.2.0) will be released when:
- New templates added
- Significant improvements to existing templates
- New case studies or substantial documentation additions

Patch versions (1.0.1, 1.0.2) for:
- Typo fixes, clarifications
- Small template improvements
- Documentation updates
