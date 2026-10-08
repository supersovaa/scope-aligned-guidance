# scope-aligned-guidance

A lightweight skill for placing repository-local guidance where it is needed and routing users and agents to canonical guidance from concrete work-type and directory entry points.

## Core idea

Make the guidance needed for each work type directly accessible from its entry point.

Keep each rule defined in one canonical place and link it from the entry points that need it.

Prefer activation conditions based on recognizable work types and responsibilities, including work implied by a request, rather than individual decisions made during execution.

For each work type, link the public skills needed for that work directly from its entry point. Read those skills when that work begins. A request involving several work types uses them in sequence; supporting operations remain under their current work type.

Split work-type entries when their responsibilities or needed skills differ substantially. Directory-local guidance remains scoped to its directory.

During review, apply review guidance. If an important audit criterion exists only in an execution skill, consult that criterion as source material without activating the execution procedure.

Keep routes from entry points to the canonical guidance explicit and shallow.

## Example

```text
repo/
├── AGENTS.md
├── .agents/
│   └── tasks/
│       ├── planning/
│       │   └── SKILL.md
│       └── review/
│           └── SKILL.md
└── docs/
    └── SKILL.md
```

`planning/SKILL.md` links directly to guidance needed for planning work. `review/SKILL.md` links directly to guidance needed for reviews. Neither entry point requires the other's task-specific guidance.

`docs/SKILL.md` provides guidance needed throughout `docs/`.

`AGENTS.md` can point to the planning and review entry points without making their task-specific guidance mandatory for all repository work.

## Installation

Install this repository as a skill folder in an agent environment that supports `SKILL.md`-based skills. Keep `SKILL.md` at the skill folder root and use the environment's skill discovery or registration mechanism. Activate it when placing, splitting, routing, or reviewing repository-local guidance.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
