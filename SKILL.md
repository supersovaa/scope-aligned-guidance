---
name: scope-aligned-guidance
description: Align repository-local SKILL.md guidance with the scopes where it applies, including directory scopes, work-phase entry points, and shared canonical definitions. Use when creating, moving, splitting, sharing, routing, or reviewing repository-local SKILL.md files.
---

# Scope-aligned guidance

Keep repository-local guidance aligned with its actual applicability.

## Core rule

Express applicability at the narrowest scopes where guidance applies consistently.

Use directory placement when guidance applies throughout a directory scope.

Use work-phase entry points when guidance must be selected by the kind of work being performed rather than only by the target directory.

Use explicit applicability declarations when shared guidance applies to separate scopes.

Do not broaden applicability to a common ancestor merely because separate subtrees or work phases share the same guidance.

## Route guidance by work phase

When the guidance to load depends on the work being performed, give that work phase a stable repository-local `SKILL.md` entry point.

Keep the entry point focused on selecting the canonical guidance required for that phase.

Prefer a direct route from the repository-level instruction file to the phase entry point over encoding the phase's full transitive skill set in the repository-level instruction file.

When a work phase and a target directory both matter, apply both scopes:

- the work-phase entry point selects guidance required for the current activity;
- the directory-local `SKILL.md` supplies rules specific to the target subtree.

A work-phase entry point does not replace directory-local guidance, and directory placement alone does not express work-phase applicability.

## Share guidance across separate scopes

When the same guidance applies to separate directory or work-phase scopes but not to their common ancestor, keep one canonical definition.

In each applicable scope, explicitly declare that the canonical guidance applies there and identify its definition.

Keep scopes where the guidance does not apply outside those applicability declarations.

Do not duplicate shared guidance across local `SKILL.md` files.

The location of the canonical definition does not by itself determine where the guidance applies.

## Split guidance by scope

When the same decision requires different guidance across scopes, express each variant within the scope where it applies.

Use directory placement, work-phase entry points, and explicit applicability declarations to express where guidance applies.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review placement

When reviewing a `SKILL.md`:

1. Identify what each piece of guidance governs.
2. Identify whether its applicability depends on directory scope, work phase, or both.
3. Use directory placement when one subtree is governed consistently.
4. Use a work-phase entry point when guidance must be selected by the activity being performed.
5. Keep one canonical definition and declare it applicable within each separate scope where it applies.
6. Split guidance when applicability requires different rules across scopes.
7. Keep repository-level routing focused on selecting entry points rather than repeating their transitive guidance.

Keep each local `SKILL.md` focused on guidance that applies to its scope or on routing to canonical guidance required by that scope.
