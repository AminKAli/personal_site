# Tiny Ember

A warm, minimal Hugo theme: plain HTML, one accent, nothing else.

- Warm paper light theme / charcoal dark theme
- Defaults to the visitor's system preference; toggle persists in localStorage
- One accent color, tuned per theme via OKLCH (pick a hue, both themes stay legible)
- No JS frameworks, no build step, ~2 KB of CSS

## Install

```sh
git submodule add https://github.com/username/tiny_ember themes/tiny_ember
```

or copy this folder to `themes/tiny_ember`.

## Configure

```toml
# hugo.toml
theme = "tiny_ember"
title = "Amin Ali"

[params]
  tagline = "Following my curiosity and exploring technology."
  accentHue = 50        # OKLCH hue: 50 orange, 80 amber, 220 teal, 130 olive, 355 rose
  github = "https://github.com/username"
  mastodon = ""         # leave empty to hide
  email = "mailto:you@example.com"

[menus]
  [[menus.main]]
    name = "About"
    pageRef = "/"
    weight = 10
  [[menus.main]]
    name = "Projects"
    pageRef = "/projects"
    weight = 20
  [[menus.main]]
    name = "Journal"
    pageRef = "/journal"
    weight = 30
```

## Content

```
content/
  _index.md            # about text (homepage)
  projects/
    homelab-dash.md    # front matter: title, summary, year, link
  journal/
    my-first-post.md   # ordinary posts; list shows date + title only
```

Project front matter:

```yaml
---
title: "homelab-dash"
summary: "Single-file status dashboard for my home server."
year: "2025 – present"
link: "https://github.com/username/homelab-dash"
---
```

## Run the demo

```sh
hugo server --source exampleSite --themesDir ../..
```
