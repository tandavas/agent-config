# Coding Working Agreements

## Scope

- Apply these preferences when reviewing or editing code in any repository.
- Follow repository-specific instructions and established codebase conventions when they differ.
- Preserve existing uncommitted work. Do not rewrite, revert, or discard unrelated changes unless explicitly asked.
- Keep changes focused on the requested work. Report unrelated critical issues instead of fixing them unless they block safe completion.
- Check for an existing local pattern or helper when the requested change is likely to duplicate behavior.

## Completion

- For code-changing tasks, continue through implementation, inspect the final diff, run checks appropriate to the change, and fix failures caused by the change before finishing.
- If a relevant check cannot be run, state that clearly instead of implying it passed.
- For review-only requests, report findings without modifying code unless fixes are also requested.

## Formatting

- Follow the repository's formatter, linter, and `.editorconfig` settings.
- For text files created or materially edited, use exactly one terminating newline without extra blank lines at the end.
- Never leave whitespace on otherwise empty lines unless it has deliberate syntax or formatting meaning.

## Readability and refactoring

- Use a named boolean when an inline condition obscures intent through arithmetic, multiple operators, or nested logic. Prefer positive, intent-based names.
- When duplicated logic is central to a review or change, use `$refactor-duplicated-logic`. Prefer extraction only when it improves clarity, maintainability, or testability, or reduces drift risk.

## Communication

- Lead with the outcome or actionable findings. For reviews, order findings by severity and include precise file and line references.
- For requested walkthroughs, explain changes file-by-file and function-by-function, covering only changed or relevant lines. Otherwise, keep completion summaries concise. Omit unchanged boilerplate.
- Explain why a suggestion helps and identify material trade-offs.
- Label subjective suggestions as **preference**. Reserve **requirement** for demonstrated correctness or safety issues and explicit project rules; distinguish a required fix from an optional refactoring approach.
