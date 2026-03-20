# Alignment and Document Ownership

## Purpose

This file clarifies how `specula-method` aligns with:
- `specula-framework`: <https://github.com/oddtitoreal/specula-framework>
- `specula-skill`: <https://github.com/oddtitoreal/specula-skill>

## Role of This Repository

`specula-method` is the open methodology layer:
- strategic foresight branding process
- six-phase facilitation structure
- ethical framing and guidance assets
- conceptual and runtime-alignment references

## Ownership Matrix

| Content type | Canonical owner | Notes |
|---|---|---|
| Method narrative and facilitation profile | `specula-method` | Source of truth for open method process |
| Runtime governance specs and canonical terminology | `specula-framework` | Source of truth for runtime/spec implementation details |
| Constitution/state-machine technical subset | `specula-skill` | Implementation-focused subset for engineers |

## Boundary Rules

1. For runtime canonical terminology/enums, reference `specula-framework/specs/terminology.md`.
2. For executable runtime schemas and contracts, reference `specula-framework/schemas/`.
3. For constitution/state-machine implementation patterns, reference `specula-skill`.
4. Prefer links to canonical documents over duplicating content.

## Version Track Clarification

- `specula-method` uses the public method track (`v1.x`).
- `specula-framework` uses a framework/runtime track (`v2.3`, `v2.4.5.x` references).
- `specula-skill` uses a skill implementation track (`v0.1.x`).

Track numbers are related by mapping, not by direct numerical equivalence.

## Maintenance Checklist

Before merging cross-repo-impacting changes:
- Verify outbound links to framework/skill are valid.
- Re-check runtime-alignment references if canonical terminology changed.
- Update this file when ownership or boundaries change.
