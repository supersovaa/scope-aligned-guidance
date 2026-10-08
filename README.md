# scope-aligned-guidance

A lightweight skill for making repository-local guidance activatable for the relevant work, applicable only in the right scopes, and directly routed to canonical guidance.

## Core idea

Separate three questions: can the agent recognize when guidance is needed (activation), where does it apply (applicability), and how does the selected entry point reach its canonical definition (routing)?

Make activation conditions recognizable from a user request, work type, or decision. For metadata-selected skills, the frontmatter `description` must advertise that work before the skill body is loaded. A link inside an unselected skill does not activate it.

Keep each rule defined in one canonical place. Place references to that definition wherever the rule actually applies. Repeated links are useful routing, not duplicate rule definitions.

Prefer concrete entry conditions and a shallow route to the required guidance.

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

A request to review an implementation should be recognizable as review work without mentioning `SKILL.md`. The review entry can then link directly to a shared canonical writing rule.

The same writing rule can remain canonical in its external skill while both `planning/SKILL.md` and `review/SKILL.md` link to it directly.

`AGENTS.md` can also link to the same canonical rule when normal repository interaction needs it.

Directory placement expresses applicability when one subtree is governed consistently.

Task or root routing files express applicability when a work type or decision is the clearer entry point.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
