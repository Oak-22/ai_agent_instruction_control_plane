# Global Instructions

This directory contains reusable instruction files intended to work
across repositories.

Use this layer for guidance that does not depend on a specific project,
such as general coding conventions, formatting rules, interface design
guidance, or agent working patterns.

## Scope

Files in this directory should remain portable. They should be usable in
multiple repositories without being rewritten for a specific codebase,
product domain, or team workflow.

## Current Files

- `artifact-formatting-preferences.md`
  Artifact and documentation formatting preferences
- `python.md`
  Reusable Python guidance
- `prompt-instruction-log.md`
  Prompt provenance for reusable instruction updates

## Boundary

Project-specific context, constraints, and operating rules do not belong
here. Place those in `../repo/`.

Global files should describe how to reason when local constraints are
unknown. They should explicitly defer to repo instructions when a
repository declares runtime, integration, privacy, deployment, or domain
requirements.
