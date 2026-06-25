# Prompt-To-Instruction Log

## Purpose

This file records prompts that produced reusable agent instructions.

Each entry preserves the concrete observation that triggered the rule,
then links to the instruction file where the reusable guidance lives.
The prompt may contain repository-specific context; the instruction
should extract the portable principle.


## Entry Format

Use this shape for new entries:

```text
ID:
Date:
Prompt:
Instruction:
Instruction File:
Status:
```


## Entries

### PIL-2026-06-23-001: Artifact Naming Consistency

ID: `PIL-2026-06-23-001`

Date: 2026-06-23

Prompt:

> Naming convention observation: Stage1 output file naming is slightly
> unstandardized. `extracted_stage1_metadata.json` vs
> `stage1_manifest.json` and
> `stage1_metadata_validation_report.json`
>
> Log this prompt and then write the instruction to one of the existing
> global/*.md files or write a new one if should exist on its own.
>
> Each instruction then could reference a specific prompt from the
> prompt log.
>
> The theory is that this can encode more contextual tokens,
> strengthening/expanding the agent context at runtime.

Instruction:

When creating or reviewing related artifacts, check whether file names
share a consistent scope, stage, artifact type, and ordering convention.
If a set mixes patterns, prefer a single naming scheme unless an
existing local convention or compatibility requirement explains the
difference.

Instruction File:

`artifact-formatting-preferences.md`

Status: Active
