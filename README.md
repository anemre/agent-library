# Agents

This repository stores reusable agents and skills.

## Structure

- `agents/` contains one directory per agent.
- `skills/` contains globally reusable skills.
- `.agents/` contains agent working state such as plans and task slices.
- `DOMAIN.md` contains shared vocabulary for this repository.

## Composition Model

Agents and skills are separate concepts:

- An **agent** defines a role, operating judgment, lifecycle, and default workflow.
- A **skill** defines a reusable procedure with trigger conditions and expected artifacts.
- A **manifest** declares how one agent composes globally reusable skills.

Agent manifests live next to the agent entrypoint:

```text
agents/
  refactorer/
    AGENT.md
    MANIFEST.md
```

Skills should not assume they belong to one agent. Agents decide whether a skill is required, part of the default workflow, optional, or not applicable.
