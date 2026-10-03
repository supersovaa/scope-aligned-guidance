# scope-aligned-guidance

A lightweight skill for placing and routing repository-local `SKILL.md` guidance at scopes that match where the guidance actually applies.

## Core idea

Use directory-local `SKILL.md` files for guidance tied to a target subtree.

Use work-phase `SKILL.md` entry points for guidance that must be selected by the activity being performed, such as review, implementation, or planning.

When both dimensions matter, apply both: the phase entry point selects work-specific guidance, while the directory-local file supplies target-specific rules.

Keep shared guidance canonical and route to it instead of duplicating it.

## Example

```text
repo/
├── AGENTS.md
├── skills/
│   ├── review/
│   │   └── SKILL.md
│   └── implementation/
│       └── SKILL.md
└── docs/
    └── implementation/
        └── SKILL.md
```

Use `AGENTS.md` as a lightweight router to the relevant work-phase entry point.

Use `skills/review/SKILL.md` when review work begins and `skills/implementation/SKILL.md` when implementation begins.

If the work targets `docs/implementation/`, also apply that directory-local `SKILL.md`.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
