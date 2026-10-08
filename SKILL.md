---
name: scope-aligned-guidance
description: Connect repository-local guidance to the concrete work types and directories that need it. Use when creating, moving, splitting, routing, or reviewing AGENTS.md, task skills, directory-local SKILL.md files, or references to canonical guidance.
---

# Scope-aligned guidance

Keep repository-local guidance connected to the work that needs it, using concrete task entry points and directory placement.

## Core rule

Make the guidance needed for each work type directly accessible from its entry point.

Use directory placement when guidance applies throughout that directory scope.

Keep one canonical definition for each rule.

When a rule is needed at multiple entry points, link its canonical definition directly from each one.

Choose activation conditions from the recognizable purpose and responsibility of the work, including work necessary to fulfill the request even when not explicitly named. Use work types as the default activation units rather than conditions tied to individual decisions during execution.

## Route from concrete entry points

Identify all work types implied by a request. At the beginning of each work type, read the public skills linked by its entry point; apply the task guidance for the current work type, along with applicable directory-local guidance, while performing it. Activate a newly identified work type when its work begins.

Keep supporting operations under the current work type. For example, creating tests while carrying out an implementation plan remains implementation work; separately undertaken testing uses the testing entry point.

When work differs substantially in responsibility or in the public skills it needs, create distinct recognizable work-type entries. Do not split entry points for every internal action or judgment.

Link the public skills needed by each work type directly from that work type's entry.

When reviewing a deliverable, apply review guidance to check correctness and important execution obligations. Consult an execution skill as source material only when it is the available definition of a required audit criterion; consulting it does not activate its execution instructions.

Prefer shallow routes with explicit work-type triggers.

When a task skill, directory skill, or `AGENTS.md` entry already describes the applicable work, link the canonical guidance from that entry.

Use grouping pages or indexes as supplemental navigation while keeping actionable entry points directly connected to the guidance they require.

## Split guidance by scope

When the same decision requires different guidance across directory or task scopes, express each variant within the scope where it applies.

Use directory placement and explicit applicability declarations to express where guidance applies.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review placement and routing

When reviewing repository-local guidance:

1. Identify what each piece of guidance governs.
2. Identify the work types or directories that need that guidance.
3. Confirm that each rule has one canonical definition.
4. Identify recognizable work-type or directory entry points where the needed rules must be found.
5. Link each entry point directly to the guidance it needs.
6. For each work-type entry point, verify that every linked skill is needed for that work type and that task-specific skills are not made mandatory for unrelated work.
7. Keep routing explicit and shallow.
8. Separate work types when their responsibilities or required public skills substantially differ.
9. Validate that work types are activated at their start and that supporting operations remain with their owning work type.

Keep each local routing file focused on guidance needed at its entry point, including direct references to canonical guidance.
