# scope-aligned-guidance

A lightweight skill for placing repository-local `SKILL.md` guidance at directory scopes that match where the guidance actually applies.

## Core idea

Place guidance at the narrowest directory shared by everything it governs.

When the same decision requires different guidance across directory scopes, place each guidance at the scope where it applies.

The directory structure expresses applicability, keeping each `SKILL.md` internally consistent.

## Example

```text
repo/
├── SKILL.md
├── parser/
│   └── SKILL.md
└── compiler/
    └── SKILL.md
```

Use the repository-root `SKILL.md` for guidance shared across the repository.

Use directory-local `SKILL.md` files where a subtree has guidance specific to that scope.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
