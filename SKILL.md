---
name: scope-aligned-guidance
description: Align repository-local SKILL.md guidance with the scopes where it applies, using directory-local placement for target scope and work-type entry skills when the current kind of work changes which guidance is required. Use when creating, moving, splitting, sharing, routing, or reviewing repository-local SKILL.md files.
---

# Scope-aligned guidance

Keep repository-local guidance aligned with its actual applicability.

## Core rule

Express applicability at the narrowest scopes where guidance applies consistently.

Treat directory scope and work type as separate applicability axes.

Use directory placement when guidance applies throughout that directory scope.

Use a work-type entry skill when the current kind of work changes which guidance must be selected.

Use explicit applicability declarations when shared guidance applies to separate scopes.

For directory scopes, keep shared guidance at its actual applicable scopes rather than broadening it to a common ancestor solely for reuse.

## Route guidance by work type

When guidance selection differs by the current kind of work, give each work type that needs a distinct selection one explicit entry skill.

Keep repository-wide guidance at the repository-level entry point.

Use the repository-level entry point to route work-type-specific guidance selection to the corresponding work-type entry skill.

A work-type entry skill should identify guidance that always applies to that kind of work and route narrower work variants to any additional guidance they require.

Keep detailed downstream applicability rules in the work-type entry skill rather than repeating them in the repository-level entry point.

Use target-specific directory-local guidance in addition to work-type guidance when the work target falls within that directory scope.

For example, a repository may route review work to `skills/review/SKILL.md`, implementation work to `skills/implementation/SKILL.md`, and planning work to `skills/planning/SKILL.md`. The review entry may then route implementation review, plan review, design review, or source review to their additional applicable guidance.

## Share guidance across separate scopes

When the same guidance applies to separate directory scopes but not throughout their common ancestor, keep one canonical definition and explicitly declare it applicable from each governed scope.

When the same guidance applies from multiple work-type entries, have each applicable entry identify the same canonical definition.

Keep scopes and work types where the guidance does not apply outside those applicability declarations.

Keep shared guidance canonical instead of duplicating its definition across local `SKILL.md` files.

The location of the canonical definition does not by itself determine where the guidance applies.

## Split guidance by scope

When the same decision requires different guidance across directory scopes or work types, express each variant within the directory scope or work-type entry where it applies.

Use directory placement, work-type routing, and explicit applicability declarations to express where guidance applies.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review placement

When reviewing a `SKILL.md`:

1. Identify what each piece of guidance governs.
2. Identify whether its applicability depends on target directory, work type, or both.
3. Identify the narrowest scopes where that guidance applies consistently.
4. Keep repository-wide guidance at the repository-level entry point.
5. Use directory placement when one subtree is governed consistently.
6. Use a work-type entry skill when that kind of work needs a distinct guidance selection.
7. Keep one canonical definition for shared guidance and identify it from each applicable scope or work-type entry.
8. Split guidance when applicability requires different rules across scopes or work types.

Keep each directory-local `SKILL.md` focused on guidance for its target scope.

Keep each work-type entry `SKILL.md` focused on selecting the guidance required for that kind of work and its narrower variants.
