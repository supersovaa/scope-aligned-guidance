# scope-aligned-guidance

A lightweight skill for aligning repository-local `SKILL.md` guidance with the directory scopes and work types where it actually applies.

## Core idea

Use directory scope and work type as separate applicability axes.

Place target-specific guidance at the narrowest directory shared by everything it governs.

When the current kind of work changes which guidance must be selected, use a work-type entry skill that routes to the additional guidance required for that work.

Keep repository-wide guidance at the repository-level entry point, and keep work-type-specific selection rules in the corresponding work-type entry.

## Directory-scope example

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

## Work-type routing example

```text
skills/
├── review/
│   └── SKILL.md
├── implementation/
│   └── SKILL.md
├── planning/
│   └── SKILL.md
├── design/
│   └── SKILL.md
├── testing/
│   └── SKILL.md
└── pr/
    └── SKILL.md
```

Create only the work-type entries that need their own guidance selection.

The repository-level agent entry point retains repository-wide guidance and routes review work to `skills/review/SKILL.md`, implementation work to `skills/implementation/SKILL.md`, planning work to `skills/planning/SKILL.md`, and other work types to their applicable entries.

Each work-type entry identifies guidance that always applies to that kind of work and routes narrower variants to any additional skills they require.

Directory-local guidance still applies independently when the work target falls within its scope.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
