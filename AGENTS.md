# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this is

The personal website of Md. Shadhin Ali, a molecular biologist (Biochemistry & Molecular Biology,
Jahangirnagar University; icddr,b; Dhaka, Bangladesh). It is served by GitHub Pages at
https://shadhin-ali002.github.io from the root of the `main` branch.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site: one page with Hero, About, Research, Skills, Publications, Contact sections |
| `style.css` | All styling. Colours are CSS variables in `:root`, with a dark-mode override |
| `photo.jpg` | Square 640×640 portrait used in the hero, shown as a circle |

There is no build step, framework, package manager or JavaScript bundle. Keep it that way unless
the owner asks otherwise.

## Rules

- **Facts must be real.** Do not invent jobs, titles, degrees, skills, projects, publications or
  results. Only use details the owner gave or that come from a verified source (e.g. a DOI record).
  If something is unknown, leave it out instead of adding a placeholder.
- **No private contact details.** Do not add an email address or phone number unless the owner
  explicitly asks. Contact currently goes through LinkedIn.
- **Keep it static.** Plain HTML and CSS; any JavaScript should be small and inline.
- **Keep both themes working.** Use the CSS variables (`--bg`, `--text`, `--accent`, …) rather than
  hard-coded colours, and check light and dark mode.
- **Keep it responsive.** The layout collapses to one column below 680px; check a phone width.
- **Images:** resize before committing (aim for under ~200 KB each) and always set `alt`, `width` and `height`.
- **Cache busting:** after changing `style.css`, bump the `?v=` number on its `<link>` in `index.html`.
- Keep the profile README repo (`../shadhin-ali002`) consistent with this site when facts change.

## Publishing

```sh
git add -A
git commit -m "Describe the change"
git push
```

GitHub Pages rebuilds automatically in about a minute. Check the build with:

```sh
gh api repos/shadhin-ali002/shadhin-ali002.github.io/pages/builds/latest --jq ".status"
```

Commit or push only when the owner asks.
