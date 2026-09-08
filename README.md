# Personal Agent Configuration

My evolving Codex preferences and reusable skills, independent of any project. Adopt what fits your workflow.

## Contents

- `AGENTS.md`: global coding and review preferences.
- `skills/refactor-duplicated-logic/SKILL.md`: guidance for extracting duplicated logic.
- `skills/refactor-duplicated-logic/agents/openai.yaml`: skill display metadata.

## Reuse with Codex

Copy `AGENTS.md` into your Codex home directory (normally `~/.codex/AGENTS.md`). Merge with any existing instructions before replacing them.

Ask Codex to install the skill from this repository:

```text
Use $skill-installer to install skills/refactor-duplicated-logic from tandavas/agent-config.
```

The installer places the skill in your personal Codex skills directory so it can be used across projects. Private repositories require GitHub access.

Start a new task to load updated global instructions. The skill can be selected automatically for relevant work or explicitly invoked with `$refactor-duplicated-logic`.

Keep project-specific instructions in each project's own repository.

## Maintaining this repository

These files are copies of the local configuration, not an automatic sync. After editing them, copy the updated files into your active Codex configuration. If you edit the installed files instead, copy those changes back here before committing.

Only store intentional instructions and skill resources here. Account credentials, task history, caches, and other Codex application data do not belong in this repository.
