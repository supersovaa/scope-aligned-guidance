# scope-aligned-guidance

A lightweight skill for selecting, scoping, and routing repository-local guidance as part of ordinary agent-facing repository work.

## Core idea

Separate three questions: can the agent recognize when guidance is needed (activation), where does it apply (applicability), and how does the selected entry point reach its canonical definition (routing)?

Activate from the work's intent or context: organizing repository instructions, setting up task workflows, or deciding which guidance applies to ongoing work. The user need not name `SKILL.md`, `AGENTS.md`, or report a failure. For metadata-selected skills, the frontmatter `description` must advertise these situations before the skill body is loaded. A link inside an unselected skill does not activate it.

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

A request to review an implementation can be recognized as review work without mentioning `SKILL.md`. When configuring the review workflow or deciding its applicable guidance, the review entry can link directly to a shared canonical writing rule.

The same writing rule can remain canonical in its external skill while both `planning/SKILL.md` and `review/SKILL.md` link to it directly.

`AGENTS.md` can also link to the same canonical rule when normal repository interaction needs it.

Directory placement expresses applicability when one subtree is governed consistently.

Task or root routing files express applicability when a work type or decision is the clearer entry point.

## Files

- `SKILL.md` — installable skill definition.
- `README.md` — overview and usage.
- `LICENSE` — MIT License.
