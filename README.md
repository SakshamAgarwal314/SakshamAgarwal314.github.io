# Personal website — Saksham Agarwal

Plain HTML + CSS + ~15 lines of vanilla JS. No build step, no framework, no npm.

## Files

| File | What it is |
| --- | --- |
| `index.html` | All the markup — three sections, one per tab |
| `styles.css` | All the styling; tokens (colors, sizes) live in `:root` at the top |
| `background.mp4` | The header video |
| `logo-github.png`, `logo-linkedin.png`, `logo-email.png` | Social icons |

## Run it locally

Double-click `index.html`. That's it.

(If the video misbehaves from `file://`, serve it instead: `python3 -m http.server` then open http://localhost:8000)

## Deploy to GitHub Pages — free

1. Create a repo named exactly `SakshamAgarwal314.github.io`
2. Put these files in the repo root
3. `git add . && git commit -m "site" && git push`
4. Live at https://SakshamAgarwal314.github.io in about a minute

To use a custom domain later: buy one, add a file named `CNAME` containing just the domain, and point the domain's DNS at GitHub Pages.

## How things work

**Tab switching** — each tab is a `<section class="page">`. The script at the bottom of `index.html` shows one and sets `hidden` on the others, then marks the matching nav link `.is-active`. It reads the URL hash, so `#projects` deep-links and the back button works.

**Header video** — the `<video>` is oversized (300% height) and rotated `-10deg` inside `.header-video`, which clips it. That angles the Milky Way band to run near-horizontal across the strip. Change the rotation in `styles.css` under `.header-video video`.

**Changing colors** — edit the variables in `:root` at the top of `styles.css`. `--accent` is the navy on the resume button and link hovers.

## Adding a project

Copy one `.row` block inside `#page-projects` and change the text. Nothing else needs touching — the rules and spacing come from CSS.
# SakshamAgarwal314.github.io
