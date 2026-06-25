---
description: "Portable Python code standards"
applyTo: "**/*.py"
---

# Python Guidance

## Version Contract

Use the Python version declared by the repository first.

Look for version constraints in:

- `pyproject.toml`
- `setup.cfg`
- `tox.ini`
- `.python-version`
- Dockerfiles
- CI workflows
- project documentation

When no explicit constraint exists, prefer modern, readable Python and
avoid assuming compatibility with old runtimes.


## Compatibility

Backward compatibility is required when the repository documents it.

If older Python support is necessary, keep the constraint:

- explicit in comments, config, or docs
- localized to the affected module or interface
- justified by deployment, packaging, or integration requirements

Do not weaken code style for hypothetical environments.


## Design Principles

- Favor clarity over cleverness.
- Use precise names that reflect domain meaning.
- Keep pure transformation logic separate from I/O and orchestration.
- Prefer typed data shapes when they clarify contracts.
- Make failure modes explicit with actionable errors.
- Avoid broad exception handling unless the recovery behavior is clear.


## Typing

Use type hints where they improve readability, tool support, or API
clarity.

- Prefer built-in generic syntax when supported by the repo's Python
  version.
- Use `Protocol`, `TypedDict`, dataclasses, or small value objects when
  they make boundaries clearer.
- Avoid over-modeling small scripts whose data flow is already obvious.


## Tests And Verification

Match verification effort to risk.

- For narrow script changes, run the affected script and any nearby
  validation command.
- For shared helpers, run relevant unit tests or add focused coverage.
- For schema or artifact changes, regenerate representative outputs and
  inspect the changed fields.
- Report any verification that could not be run.


## Agent Behavior

Flag version or compatibility concerns only when there is evidence of a
real constraint.

Good:

> "This uses syntax that requires Python 3.12. The project declares
> Python 3.10 in `pyproject.toml`, so this should be rewritten or the
> version contract should be updated."

Avoid:

> "This might not work on old Python versions."

When in doubt, inspect repository constraints before warning.
