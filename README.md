# AI-Human Workflow Template

This repository is a reusable template scaffold for AI-human
development workflows, including agent guidance and constraints and developer knowledge capture and retention

## Purpose

The template formalizes three ideas:

- AI agents need explicit operating context
- teams need durable places to capture learning from real work
- AI-assisted development workflows should be reusable and standardized across repositories

## Portfolio Role

This repository is part of my AI-native engineering methodology layer.

It is not a standalone portfolio product. It supports my project-facing
repositories by documenting reusable collaboration patterns, agent
workflows, and durable knowledge-capture practices.

Project-facing repositories include:

- `myHealth`
- `creative-workflow-batch-transformation-pipeline`
- `ai-infrastructure-financial-warehouse`

## Methodology Role

This repository defines the reusable operating system for AI-assisted
development: prompts, workflow templates, agent instructions, review
rituals, and reusable project scaffolding.

It answers:

> How should an AI-native engineering workflow be run?

## Related Methodology Repository

For applied case studies and observations from real AI-human
engineering work, see
[`ai-human-engineering-collaboration-case-studies-and-best-practices`](https://github.com/Oak-22/ai-human-engineering-collaboration-case-studies-and-best-practices).

## Template Contents

- `.github/agent-instructions/`
  Layered AI-human workflow guidance, separating reusable global instructions from repository-specific constraints and context.
- `engineering_knowledge_base/`
  Structured locations for incident capture, learning notes, and other
  workflow-derived engineering knowledge.

## Adoption Guidance

Use this template as checked-in repository structure.

The structure is portable. The knowledge content should be scope-aware.

In enterprise environments, most learning is repo-specific first,
especially in microservice architectures where implementation details,
incidents, and operational practices differ by service.

Use a federated model:

- `global`: cross-repo practices and stable standards
- `domain`: bounded-context guidance shared by related services
- `repo`: service-specific decisions, incidents, and runbooks

Start local by default. Promote only lessons that are stable and
reusable across services.

If a team also maintains centralized canonical assets, those may be
linked into a live repository through symlinks. Keep this template
copyable without machine-specific dependencies.

## Promotion Workflow

Use this lightweight process to avoid both duplication and overfitting:

1. Capture new learning in the repo where it occurred.
2. Mark candidate notes for promotion once reused or validated.
3. Promote to domain/global only after context-specific details are
  abstracted into reusable guidance.
4. Keep backlinks from promoted guidance to repo case evidence.

This preserves local relevance while building organization-wide
engineering memory over time.

## Related Design Direction

This repository is a template scaffold, not a full implementation of
workflow-derived retrieval.

A related design direction is documented in
[`docs/workflow_derived_retrieval_for_ai_assisted_development.md`](docs/workflow_derived_retrieval_for_ai_assisted_development.md).
That note explains how workflow telemetry and retrieval practice could
extend this template in future systems without changing the template's
core identity.
