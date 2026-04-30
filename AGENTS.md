# GubGub — AI Agent Instructions

## Hard Constraints

- **Vanilla JavaScript only** — no frameworks, no jQuery, no build tools, no Node.js
- **Single-file HTML preferred** — HTML + CSS + JS inline in one `.html` file
- **Static hosting** — GitHub Pages or `file://` only, no backend
- **ES2020+** — `const` over `let`, arrow functions, template literals, async/await, no `var`, no classes, no `this`
- **Local-first** — the app must work by opening `index.html` directly with `file://`

## What This Repo Is

GubGub is a lightweight single-file GitHub repository browser. It lists repositories for a GitHub user or organization, opens a repository tree, and displays files in the browser.

The current app formerly called **TooToo** is now **GubGub**. The lighter/current browser formerly called **TooToo LT** is now **TooToo**.

Key file: [`index.html`](index.html) — the canonical current version.

Use [`0-gubgub-agenda.md`](0-gubgub-agenda.md) for priorities and [`0-gubgub-journal.md`](0-gubgub-journal.md) for recent notes.

## UX Philosophy

GubGub should feel like a fast, lightweight file and repo browser.

- On repo load, show the root README by itself when available
- Keep advanced repo intelligence in the **Stats** button
- Keep exploration features in **Discover**
- Avoid adding new panels to the default file view unless explicitly requested
- Prefer direct, visible, useful behavior over clever feature panels
- If a feature duplicates an existing button or workflow, pause and ask before implementing

## Style Conventions

- CSS custom properties for colors/sizes — see `:root` near the top of `<style>`
- `rem` units for font sizes where practical
- Template literals are fine for repeated/inline HTML
- Use `document.createElement` when it makes complex DOM easier to read
- Use delegated `addEventListener` handlers; do not add inline `on*=` attributes
- External CDN dependencies are acceptable when the app still has no build step
- Keep code beginner-readable; if a student cannot follow the logic, simplify it

## Development Workflow

- Edit [`index.html`](index.html) directly; it is the canonical single-file app
- Make small, reversible changes rather than impressive rewrites
- Archive dated snapshots as `index-YYYY-MM-DD-HH-MM.html` before larger rewrites
- Keep changelogs in `README.md` with dated bullet entries when the README is maintained
- Test by opening [`gubgub-test.html`](gubgub-test.html) and by manually opening `index.html`
- Do not use `.archive/` files as source references unless explicitly asked
