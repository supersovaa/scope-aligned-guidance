---
name: scope-aligned-guidance
description: Place repository-local SKILL.md guidance at scopes that match where the guidance applies, including sharing one definition across separate directory scopes without broadening its applicability. Use when creating, moving, splitting, sharing, or reviewing directory-local SKILL.md files.
---

# Scope-aligned guidance

Place repository-local guidance where its effective scope matches its actual applicability.

## Core rule

Place guidance at the narrowest scope where it applies consistently.

Use a broader directory only when the guidance applies consistently throughout that broader directory scope.

Do not move guidance to a common ancestor merely because separate subtrees share it.

## Share guidance across separate scopes

When the same guidance applies to separate directory scopes but not to their common ancestor, keep one canonical definition.

In each applicable scope, explicitly declare that the canonical guidance applies there and identify its definition.

Keep scopes where the guidance does not apply outside those applicability declarations.

Do not duplicate shared guidance across local `SKILL.md` files.

The location of the canonical definition does not by itself broaden where the guidance applies.

## Split guidance by scope

When the same decision requires different guidance across directory scopes, place each guidance at the scope where it applies.

Use directory placement and explicit applicability declarations to express where guidance applies.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review placement

When reviewing a `SKILL.md`:

1. Identify what each piece of guidance governs.
2. Identify the directory scopes where that guidance applies consistently.
3. Keep guidance local when those scopes form one consistently governed subtree.
4. Keep one canonical definition and declare it applicable within each separate scope where it applies.
5. Split guidance when applicability requires different rules across scopes.

Keep each local `SKILL.md` focused on guidance that applies to its directory scope.
