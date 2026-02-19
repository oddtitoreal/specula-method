# Changelog

All notable changes to the Specula Method open documentation will be documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial public release of ethical framework
- Operational templates for all six phases
- Case study: La Saponaria Care Intelligence
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
- Fixed case-studies index link for La Saponaria (`case_study_saponaria.md`).
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
