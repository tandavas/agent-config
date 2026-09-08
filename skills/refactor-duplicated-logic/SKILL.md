---
name: refactor-duplicated-logic
description: Review or refactor code when duplicated logic or repeated conditional fragments are central to the task.
---

# Refactor Duplicated Logic

Decide whether extraction improves the code before changing it. Follow existing repository naming, placement, and visibility conventions.

## Choose a technique

- **Extract Method / Extract Function**: move duplicated or cohesive behavior into a clearly named helper.
- **Consolidate Duplicate Conditional Fragments**: lift repeated lines out of conditional branches.
- **Replace Inline Code with Function Call**: use an existing helper when it already expresses the intent.
- **Single Source of Truth (SSOT)**: give shared constants, defaults, configuration, or repeated literals one declaration site.
- **Parameter Object**: group three or more related arguments when they form one concept and named fields make call sites clearer.

Name helpers by intent and place them near their primary caller unless they are genuinely shared. Keep them private or module-local unless cross-module reuse is the goal.

## Decide whether to extract

Use the **Rule of Three** as a heuristic: two occurrences can be acceptable; consider extraction on the third. Consider extraction earlier when the duplicated block is non-trivial and divergence would create a realistic defect risk.

Avoid extraction when it introduces:

- **Speculative Generality**: an abstraction for a hypothetical future need.
- **Shape Divergence**: callers need different control flow or many optional parameters.
- **One-off Helpers**: a single-use helper that does not clarify a complex operation.
- **Clarity Loss**: readers must jump between scopes or files to follow a small linear flow.

During review, label extraction suggestions as **preference** unless extraction is necessary to resolve a demonstrated correctness or safety issue or satisfy an explicit project rule. Potential drift alone does not make extraction a **requirement**. Distinguish a required behavior fix from an optional extraction. Name the applicable technique or the smell being avoided so the trade-off is explicit.
