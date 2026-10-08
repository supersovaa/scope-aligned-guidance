# scope-aligned-guidance

A lightweight skill for placing repository-local guidance where it applies and routing users and agents to canonical guidance from clear, concrete entry points.

## Core idea

Keep each rule defined in one canonical place.

Place references to that canonical definition wherever the rule actually applies.

Repeated links are useful routing, not duplicate rule definitions.

Prefer activation conditions based on recognizable work types and responsibilities, including work implied by a request, rather than individual decisions made during execution.

For each work type, link the public skills needed for that work directly from its entry point. Read those skills when that work begins. A request involving several work types uses them in sequence; supporting operations remain under their current work type.

Split work-type entries when their responsibilities or needed skills differ substantially. Repeated links to a canonical skill are intentional. Directory-local guidance remains scoped to its directory.

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

A shared writing rule can remain canonical in its external skill while both `planning/SKILL.md` and `review/SKILL.md` link to it directly.

`AGENTS.md` can also link to the same canonical rule when normal repository interaction needs it.

Directory placement expresses applicability when one subtree is governed consistently.

Task or root routing files express applicability when a work type is the clearer entry point.

## Installation

Install this repository as a skill folder in an agent environment that supports `SKILL.md`-based skills. Keep `SKILL.md` at the skill folder root and use the environment's skill discovery or registration mechanism. Activate it when placing, splitting, routing, or reviewing repository-local guidance.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
