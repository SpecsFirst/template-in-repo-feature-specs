# Conventions

## Numbering

Features are folders named `NNN-short-name` (for example `002-user-login`): three digits,
then a short kebab-case name. Numbers are never reused. ADRs are `ADR-NNN-short-name.md`.

## Statuses

- **Feature:** `draft`, `approved`, `in-progress`, `done`.
- **Task:** `todo`, `doing`, `done`, `blocked`.

## Who changes what

- **Humans** own `product.md` and each `requirements.md`. Agents never edit them without
  approval.
- **Agents** propose `design.md` and keep `tasks.md` up to date while they work.
- A feature moves to `approved` when a human approves its requirements.

## When to write an ADR

Write one in `decisions/` for any structural decision: a technology choice, a data model,
a public interface, a change that is costly to reverse. Do not edit an accepted ADR;
supersede it with a new one.

## Create a feature

1. Copy `features/001-example-feature` to `features/<NNN-short-name>`.
2. Replace the `<...>` placeholders, starting with `requirements.md` (status `draft`).
3. Add the feature to the table in `product.md`.
