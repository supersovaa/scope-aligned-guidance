---
name: scope-aligned-guidance
description: Place repository-local SKILL.md guidance at directory scopes that match where the guidance applies. Use when creating, moving, splitting, or reviewing directory-local SKILL.md files.
---

# Scope-aligned guidance

Place repository-local guidance where its directory scope matches its actual applicability.

## Core rule

Place guidance at the narrowest directory shared by everything it governs.

Create a local `SKILL.md` when a directory subtree needs guidance specific to that scope.

Keep guidance at a broader directory when the same guidance applies consistently across that broader scope.

## Split guidance by scope

When the same decision requires different guidance across directory scopes, place each guidance at the scope where it applies.

Use the directory structure to express the applicability of guidance.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review placement

When reviewing a `SKILL.md`:

1. Identify what each piece of guidance governs.
2. Identify the directory scope where that guidance applies consistently.
3. Move guidance to the narrowest shared directory for that scope.
4. Split guidance when applicability separates into distinct directory scopes.

Keep each `SKILL.md` focused on guidance shared by its directory scope.
