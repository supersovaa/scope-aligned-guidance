---
name: scope-aligned-guidance
description: Align repository-local SKILL.md guidance with the scopes where it applies, using directory-local placement for target scope and task-phase entry skills for work-type routing. Use when creating, moving, splitting, sharing, routing, or reviewing repository-local SKILL.md files.
---

# Scope-aligned guidance

Keep repository-local guidance aligned with its actual applicability.

## Core rule

Express applicability at the narrowest scopes where guidance applies consistently.

Treat directory scope and task phase as separate applicability axes.

Use directory placement when guidance applies throughout that directory scope.

Use a task-phase entry skill when guidance selection depends on the kind or timing of work being performed.

Use explicit applicability declarations when shared guidance applies to separate scopes.

Do not broaden applicability to a common ancestor merely because separate subtrees or work phases share the same guidance.

## Route guidance by task phase

When an agent must choose among multiple guidance sets based on the current kind of work, give each recurring work phase one explicit entry skill.

Keep the repository-level agent entry point focused on routing the current work to the appropriate phase entry skill.

A phase entry skill should identify guidance that always applies in that phase and route narrower work variants to the additional guidance they require.

Keep detailed downstream applicability rules in the phase entry skill rather than repeating them in the repository-level entry point.

Use target-specific directory-local guidance in addition to phase guidance when the work target falls within that directory scope.

Do not use phase routing to replace target-specific directory guidance.

For example, a repository may route review work to `skills/review/SKILL.md`, implementation work to `skills/implementation/SKILL.md`, and planning work to `skills/planning/SKILL.md`. The review entry may then route implementation review, plan review, design review, or source review to their additional applicable guidance.

## Share guidance across separate scopes

When the same guidance applies to separate directory scopes or work phases but not to their common ancestor, keep one canonical definition.

In each applicable scope or phase entry, explicitly declare that the canonical guidance applies there and identify its definition.

Keep scopes and phases where the guidance does not apply outside those applicability declarations.

Do not duplicate shared guidance across local `SKILL.md` files.

The location of the canonical definition does not by itself determine where the guidance applies.

## Split guidance by scope

When the same decision requires different guidance across directory scopes or work phases, express each variant within the scope where it applies.

Use directory placement, phase routing, and explicit applicability declarations to express where guidance applies.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review placement

When reviewing a `SKILL.md`:

1. Identify what each piece of guidance governs.
2. Identify whether its applicability depends on target directory, task phase, or both.
3. Identify the narrowest scopes where that guidance applies consistently.
4. Use directory placement when one subtree is governed consistently.
5. Use a phase entry skill when a recurring kind of work needs a stable routing entry.
6. Keep one canonical definition and declare it applicable within each separate scope or phase where it applies.
7. Split guidance when applicability requires different rules across scopes or phases.

Keep each directory-local `SKILL.md` focused on guidance for its target scope.

Keep each task-phase entry `SKILL.md` focused on selecting the guidance required for that phase and its narrower variants.
