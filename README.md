# scope-aligned-guidance

A lightweight skill for aligning repository-local `SKILL.md` guidance with the directory scopes and task phases where it actually applies.

## Core idea

Use directory scope and task phase as separate applicability axes.

Place target-specific guidance at the narrowest directory shared by everything it governs.

When guidance selection depends on the kind of work being performed, use a task-phase entry skill that routes to the additional guidance required for that work.

Keep the repository-level agent entry point lightweight: it should identify the work phase and route to that phase's entry skill instead of duplicating all downstream applicability rules.

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

## Task-phase routing example

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

The repository-level agent entry point routes review work to `skills/review/SKILL.md`, implementation work to `skills/implementation/SKILL.md`, planning work to `skills/planning/SKILL.md`, and so on.

Each phase entry identifies guidance that always applies in that phase and routes narrower variants to any additional skills they require.

Directory-local guidance still applies independently when the work target falls within its scope.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
