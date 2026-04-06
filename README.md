# AI-Human Workflow Template

This repository is a reusable template scaffold for workflow artifacts
that sit next to product code in AI-assisted repositories.

## Purpose

The template formalizes three ideas:

- AI agents need explicit operating context
- teams need durable places to capture learning from real work
- workflow artifacts should be portable across repositories

## Template Contents

- `.github/agent-instructions/`
  Reusable and repository-specific guidance for AI-human development
  work.
- `engineering_knowledge_base/`
  Structured locations for incident capture, learning notes, and other
  workflow-derived engineering knowledge.

## Adoption Guidance

Use this template as checked-in repository structure.

If a team also maintains centralized canonical assets, those may be
linked into a live repository through symlinks, but the portable
template should remain copyable without machine-specific dependencies.

## Related Design Direction

This repository is a template scaffold, not a full implementation of
workflow-derived retrieval.

A related design direction is documented in
[`docs/workflow_derived_retrieval_for_ai_assisted_development.md`](docs/workflow_derived_retrieval_for_ai_assisted_development.md).
That note explains how workflow telemetry and retrieval practice could
extend this template in future systems without changing the template's
core identity.
