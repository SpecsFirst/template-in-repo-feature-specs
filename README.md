# template-in-repo-feature-specs

A [Copier](https://copier.readthedocs.io) template that adds specs to an existing code repo.
Specs live inside the repo, in `specs/`, one folder per feature with requirements, design
and tasks. `AGENTS.md` tells any agent or human where to start: product, conventions, feature.

## Use it

From the root of your code repo:

```bash
uv run --with copier copier copy https://github.com/SpecsFirst/template-in-repo-feature-specs .
```

Copier asks for the project title, then adds the files below. Your own files are untouched.
To pull in later template changes, run `copier update`.

If an `AGENTS.md` already exists, Copier asks before overwriting it: answer no and merge
the two by hand.

## What you get

```
.
├── AGENTS.md                            entry point for agents and humans
└── specs
    ├── conventions.md                   numbering, statuses, who changes what, ADRs
    ├── decisions
    │   └── ADR-001-short-name.md        architecture decision record
    ├── features
    │   └── 001-example-feature          copy and rename for each new feature
    │       ├── design.md
    │       ├── requirements.md
    │       └── tasks.md
    └── product.md                       goal, users, scope, feature index
```

The answers file `.copier-answers.yml` is also written (hidden); `copier update` needs it.
`README.md`, `LICENSE` and `copier.yml` stay in the template and are not copied.

## The method in short

- **Product first.** `product.md` states the goal, users and scope, and indexes features.
- **One folder per feature.** Requirements (owned by humans), then design, then tasks.
- **Statuses in the files.** Feature and task statuses are plain words, updated as work moves.
- **ADRs for structural decisions.** Each is a short, dated file in `specs/decisions/`.
- **Placeholders.** Examples use `<angle-bracket>` placeholders. Replace them.

## Develop the template

```bash
uv run --with copier copier copy --defaults --vcs-ref HEAD \
  --data project_title="Test" . <code repo dir>
```

Files keep their real names (`_templates_suffix: ""`), so they are readable on GitHub and
in the gallery. Only `{{ project_title }}` is substituted.

## License

CC0-1.0, see `LICENSE`.
