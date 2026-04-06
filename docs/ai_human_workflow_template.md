# AI-Human Workflow Template

This repository contains workflow artifacts that are useful beyond a
single codebase and can be treated as reusable infrastructure for
AI-assisted development.

## Why These Artifacts Exist

AI-assisted development can improve short-term delivery speed, but it
can also reduce how much implementation reasoning remains in the
developer's head after the task is done.

That creates a real risk of knowledge atrophy:

- weaker retention of system behavior
- repeated rediscovery of past fixes
- slower onboarding for new contributors
- over-reliance on externalized reasoning

## Template Pattern

The reusable pattern in this repository separates workflow artifacts
into two categories:

- `.github/agent-instructions/`
  Operating guidance for human plus AI development
- `engineering_knowledge_base/`
  Learning artifacts derived from real engineering work

This repository itself is the copyable scaffold for those workflow
artifacts.


