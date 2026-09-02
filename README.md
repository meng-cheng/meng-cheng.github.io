# meng-cheng.github.io

Personal academic site — [meng-cheng.github.io](https://meng-cheng.github.io).

Jekyll 4, no theme. Built and deployed by GitHub Actions
(`.github/workflows/pages.yml`) on every push to `master`.

## Local preview

```sh
bundle install          # first time only
bundle exec jekyll serve # -> http://localhost:4000, rebuilds on save
```

Local and CI use the same `Gemfile`, so what you see locally is what deploys.

## Writing

**A note** — run the script from the repo root:

```sh
bin/new-note "Anomalies in symmetric tensor gauge theories"
```

It writes `_posts/2026-09-01-anomalies-in-symmetric-tensor-gauge-theories.md`
with the front matter filled in, prints the path, and opens it in vim (or
`$EDITOR`). To write one by hand instead, that front matter is just:

```yaml
---
title: 'Anomalies in symmetric tensor gauge theories'
date: 2026-09-01
tags:
  - math
---
```

Use **single** quotes around the title. Double-quoted YAML treats a backslash as
an escape, so a title containing LaTeX (`$\mathbb{Z}_2$`) breaks the build.

No `permalink` needed: `_config.yml` sets `/posts/:year/:month/:title/`, so the
URL follows the filename date. (The first note carries an explicit `permalink`
from before that pattern existed — an explicit one always wins, which is what
keeps its published URL stable. Leave it be.)

**A talk** — add `_talks/slug.md` with `title`, `type`, `venue`, `date`,
`location`, and an explicit `permalink`.

**Teaching** — add `_teaching/slug.md`; `/teaching/` lists the collection
automatically.

## Math

MathJax 3 loads automatically on posts (`math: true` is a default in
`_config.yml`); add `math: true` to any other page's front matter to opt in.
Write `$inline$` and `$$display$$` as usual — kramdown rewrites `$$…$$` into
`\[…\]`, which MathJax reads natively, so grepping built HTML for `$$` finds
nothing. That is expected.

Shorthands defined in `_includes/head.html`:

| Macro | Expands to |
| ----- | ---------- |
| `\Z`  | `\mathcal{Z}` |
| `\bZ` | `\mathbb{Z}` |
| `\U`  | `\mathrm{U}(1)` |

Add more in the same `macros` block. They are JavaScript strings, so escape the
backslash — `'\\mathbb{Z}'`. For one taking arguments, use the array form:
`HH: ['\\mathcal{H}^{#1}', 1]` gives `\HH{7}`.

## Layout

```
_config.yml            site config, collections, front-matter defaults
_data/navigation.yml   the top nav
_layouts/              default -> page / post / talk
_includes/             head, nav, profile, footer, icon, read-time
_pages/                one file per top-level page
_posts/  _talks/       content
assets/css/main.scss   the entire stylesheet
bin/new-note           scaffolds a new note
.github/workflows/     build + deploy
```

Layouts are assigned by `_config.yml` defaults, so front matter rarely needs a
`layout:` line.

Originally forked from [academicpages](https://github.com/academicpages/academicpages.github.io)
(a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/));
the theme was removed in favour of hand-written layouts, but the visual design
is still theirs. See LICENSE.
