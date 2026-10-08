# Activation granularity design

This document records the agreed work-type activation design. The operational rules are defined in `SKILL.md`.

## Decided

1. **Target:** Improve how `scope-aligned-guidance` guides the activation conditions of *other skills*. Broadening this skill's own activation is not the objective.
2. **Timing:** Identify the work types implied by the initial request, but load and apply each work type's guidance only when that work begins. If a newly required work type becomes apparent during execution, activate it before beginning that work.
3. **Implicit need:** Include tasks and decisions reasonably necessary to fulfill the request even if they were not stated explicitly; relevance alone is insufficient.
4. **Activation unit:** Use recognizable work types rather than highly specific individual judgments. Work types may be meaningfully fine-grained where that preserves selective skill loading.
5. **Work-type splitting:** Separate work-type entries when their main responsibilities or needed public skills substantively differ and the tasks can be recognized separately. Do not split solely for every individual operation or judgment.
6. **Work-type-first loading (Q6):** At the beginning of each selected work type, read and apply the public skills attached to that work type. Do not apply all skills for the entire user request simultaneously. If different work requires a substantively different skill set, split the work types instead of adding fine-grained per-skill activation conditions.
7. **Shared public skills (Q7):** Link a public skill from each work-type entry where it applies. Multiple work-type entries may refer to the same canonical public skill. Do not introduce a shared mandatory-reading entry solely to deduplicate references.
8. **Multiple work types (Q8):** Identify all work types implied by the request, carry out their work in sequence where appropriate, and activate only the guidance applicable to the work type currently being performed. For example, while implementing, apply the implementation skill; the skills for a subsequent distinct testing or review stage are activated when that stage begins.
9. **Supporting operations (Q9):** Work supporting the active work type does not independently activate another work-type skill. For example, tests written as part of executing an implementation plan remain under implementation guidance; independent testing work activates testing guidance.
10. **Reviewing (Q10):** Review work activates review guidance without also activating the execution skill for the reviewed work. Review obligations belong in review guidance and are evaluated against the appropriate canonical requirements, design, plan, results, and test evidence.
11. **Review obligations (Q11):** Review checks correctness of the deliverable and compliance with important execution procedures. Keep review-specific audit obligations under review guidance, without automatically activating implementation execution procedures.
12. **Q12 — Review references:** A review may consult a relevant criterion from an implementation-time skill as source material without applying its implementation workflow. Keep that criterion at its existing canonical location.
13. **Selective routing remains intentional:** Maintain task-scoped and directory-scoped entry points to avoid reading irrelevant skills. The number of files or repeated links to one canonical skill is not independently a defect.

## Evidence from target use repository

In `supersovaa/battle-spirits-standard-simulator`, the `master` branch routes work types through `AGENTS.md`, task skills under `.agents/tasks/`, and directory guidance such as `docs/**/SKILL.md`.

A historical revision (PR #399) introduced per-judgment conditions and recheck timing. A later revision (PR #415) removed an intermediate cross-cutting router while preserving direct links from applicable entry points. Those links support selective loading and are not, by themselves, a reason to collapse task files.

## Unresolved

None.

## Deferred

None.
