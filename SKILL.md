---
name: scope-aligned-guidance
description: Align repository-local guidance with the tasks that activate it, the scopes where it applies, and direct routes to canonical rules. Use when repository skills or AGENTS.md guidance are missed or invoked too broadly, or when placing, splitting, sharing, routing, or reviewing guidance across work types and directories.
---

# Scope-aligned guidance

Make repository-local guidance discoverable for the work that needs it, applicable within its intended scopes, and directly routable to one canonical definition.

## Core rule

Treat activation, applicability, and routing as separate requirements.

- Activation determines whether the agent recognizes that guidance is needed for the current work.
- Applicability determines which directory, work type, or decision the guidance governs.
- Routing takes an applicable entry point to the canonical rule.

Express applicability at the narrowest scopes where guidance applies consistently.

Use directory placement when guidance applies throughout that directory scope.

Use explicit applicability declarations when shared guidance applies to separate scopes.

Keep one canonical definition for each rule.

Place references to that definition at every concrete entry point where the rule applies.

## Make guidance activatable

Identify the externally recognizable user requests, work types, and decisions that should cause the guidance to be used.

Expose these triggers at an entry point the agent can see *before* it needs the guidance. For a skill selected from metadata, use its frontmatter `description`; for an already-consulted repository or task router, state the relevant work condition there.

Describe the task or decision, not just the guidance file to edit or the internal step that follows selection. Do not require the user to name a skill or perform a step that the skill can carry out after activation.

Keep activation boundaries aligned with responsibility: recognize relevant work without drawing in unrelated tasks. Keep detailed execution conditions in the selected guidance.

A link inside an unread or unselected `SKILL.md` cannot make that skill activate. Ensure the applicable entry point is discoverable in the target agent environment before relying on its links.

## Share guidance across separate scopes

When the same guidance applies to separate scopes, keep one canonical definition.

In each applicable scope or task entry point, explicitly declare that the canonical guidance applies there and identify its definition.

Repeat references wherever they make the applicable guidance directly discoverable.

Repeated references are routing, not duplicate guidance definitions.

The location of the canonical definition does not by itself determine where the guidance applies.

## Route from concrete entry points

Route from a concrete work type or decision directly to the canonical guidance that governs it.

Prefer shallow routes with explicit triggers.

When a task skill, directory skill, or `AGENTS.md` entry already describes the applicable work, link the canonical guidance from that entry.

Use grouping pages or indexes as supplemental navigation while keeping actionable entry points directly connected to the guidance they require.

A rule may be linked from several entry points while remaining defined in one canonical location.

## Split guidance by scope

When the same decision requires different guidance across directory or task scopes, express each variant within the scope where it applies.

Use directory placement and explicit applicability declarations to express where guidance applies.

Prefer separate, internally consistent scopes over parent-child rule resolution.

## Review activation, placement, and routing

When reviewing repository-local guidance:

1. Identify the work and decisions that each piece of guidance governs.
2. Check that relevant requests and decisions can activate the entry point before its body is read, without requiring internal steps or skill names.
3. Identify the directory or task scopes where that guidance applies consistently.
4. Keep one canonical definition for each shared rule.
5. Identify the concrete work or decision entry points from which the rule must be discovered.
6. Link each applicable entry point directly to the canonical definition.
7. Keep routing explicit and shallow; split guidance when applicability requires different rules.
8. Check a task that should activate the guidance and an unrelated task that should not.

Keep each local routing file focused on guidance that applies to its scope or on direct references to shared canonical guidance.
