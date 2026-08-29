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

**A note** — add `_posts/YYYY-MM-DD-slug.md`:

```yaml
---
title: "..."
date: 2026-09-14
tags: [math]
---
```

No `permalink` needed: `_config.yml` sets `/posts/:year/:month/:title/`, so the
URL follows the filename date. (The first note carries an explicit `permalink`
from before that pattern existed — an explicit one always wins, which is what
keeps its published URL stable. Leave it be.)

MathJax 3 loads automatically on posts (`math: true` is a default in
`_config.yml`); add `math: true` to any other page's front matter to opt in.
Write `$inline$` and `$$display$$` as usual.

**A talk** — add `_talks/slug.md` with `title`, `type`, `venue`, `date`,
`location`, and an explicit `permalink`.

**Teaching** — add `_teaching/slug.md`; `/teaching/` lists the collection
automatically.

## Layout

```
_config.yml            site config
_data/navigation.yml   the top nav
_layouts/              default -> page / post / talk
_includes/             head, nav, profile, footer, icon, read-time
_pages/                one file per top-level page
_posts/  _talks/       content
assets/css/main.scss   the entire stylesheet
```

Originally forked from [academicpages](https://github.com/academicpages/academicpages.github.io)
(a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/));
the theme was removed in favour of hand-written layouts, but the visual design
is still theirs. See LICENSE.
