# Activation granularity design (Draft)

This document records decisions from the ongoing design grill. It is a provisional design artifact, not an active skill rule.

## Decided

1. **Target:** Improve how `scope-aligned-guidance` guides the activation conditions of *other skills*. Broadening this skill's own activation is not the objective.
2. **Timing:** Prefer selecting applicable skills from the initial user request. If a need becomes apparent only during execution, activate the necessary skill before the relevant work.
3. **Implicit need:** Include tasks and decisions reasonably necessary to fulfill the request even if they were not stated explicitly; relevance alone is insufficient.
4. **Activation unit:** Use recognizable work types rather than highly specific individual judgments. Work types may be meaningfully fine-grained where that preserves selective skill loading.
5. **Work-type splitting:** Separate work-type entries when their main responsibilities or needed public skills substantively differ and the tasks can be recognized separately. Do not split solely for every individual operation or judgment.
6. **Work-type-first loading (Q6):** Once a work type is selected, read all public skills attached to that work type at the start. If different work requires a substantively different set, split the work types instead of adding fine-grained per-skill activation conditions. When a further work type becomes necessary during execution, load its skills then.
7. **Selective routing remains intentional:** Maintain task-scoped and directory-scoped entry points to avoid reading irrelevant skills. The number of files or repeated links to one canonical skill is not independently a defect.

## Evidence from target use repository

In `supersovaa/battle-spirits-standard-simulator`, the `master` branch routes work types through `AGENTS.md`, task skills under `.agents/tasks/`, and directory guidance such as `docs/**/SKILL.md`.

A historical revision (PR #399) introduced per-judgment conditions and recheck timing. A later revision (PR #415) removed an intermediate cross-cutting router while preserving direct links from applicable entry points. Those links support selective loading and are not, by themselves, a reason to collapse task files.

## Unresolved

- How to treat shared public skills that span multiple work types without reintroducing fine-grained decision-trigger rules.
- How to express recognizable work-type triggers while keeping selective loading.
- How to word the resulting changes in `SKILL.md` and `README.md`.

## Deferred

None.
