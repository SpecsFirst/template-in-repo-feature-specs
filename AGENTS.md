# AGENTS.md

Specs for this repo live in `specs/`. Follow them.

## Before you start

1. Read `specs/product.md` (goal, users, scope, feature index).
2. Read `specs/conventions.md` (numbering, statuses, who changes what).

## Working on a feature

Open `specs/features/<NNN-short-name>/` and read, in this order:

1. `requirements.md`: what must be true when the feature is done.
2. `design.md`: how it will be built.
3. `tasks.md`: the checklist to execute.

## Rules

- Update task statuses in `tasks.md` as you work (`todo`, `doing`, `done`, `blocked`).
- Never edit `requirements.md` without human approval. If a requirement looks wrong or
  missing, say so and propose a change.
- Record any structural decision in an ADR under `specs/decisions/`.
- Keep the feature index in `specs/product.md` in sync with feature statuses.
