# scope-aligned-guidance

A lightweight skill for placing repository-local guidance where it applies and routing users and agents to canonical guidance from clear, concrete entry points.

## Core idea

Keep each rule defined in one canonical place.

Place references to that canonical definition wherever the rule actually applies.

Repeated links are useful routing, not duplicate rule definitions.

Prefer entry conditions that describe concrete work or decisions, and keep the route from that entry point to the required guidance explicit and shallow.

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

Task or root routing files express applicability when a work type or decision is the clearer entry point.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
