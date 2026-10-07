---
name: scope-aligned-guidance
description: Align repository-local guidance with the scopes where it applies and with the entry points from which it is discovered. Use when creating, moving, splitting, sharing, routing, or reviewing AGENTS.md, task skills, directory-local SKILL.md files, or references to canonical guidance.
---

# Scope-aligned guidance

Keep repository-local guidance aligned with its actual applicability and make each applicable entry point route to it directly.

## Core rule

Express applicability at the narrowest scopes where guidance applies consistently.

Use directory placement when guidance applies throughout that directory scope.

Use explicit applicability declarations when shared guidance applies to separate scopes.

Keep one canonical definition for each rule.

Place references to that definition at every concrete entry point where the rule applies.

Choose entry conditions that can be recognized directly from the current work or decision.

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

## Review placement and routing

When reviewing repository-local guidance:

1. Identify what each piece of guidance governs.
2. Identify the directory or task scopes where that guidance applies consistently.
3. Keep one canonical definition for each shared rule.
4. Identify the concrete work or decision entry points from which the rule must be discovered.
5. Link each applicable entry point directly to the canonical definition.
6. Keep routing explicit and shallow.
7. Split guidance when applicability requires different rules across scopes.

Keep each local routing file focused on guidance that applies to its scope or on direct references to shared canonical guidance.
