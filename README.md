# Guardrail — Claude Code Prompt Handbook

A reusable prompt library for working with Claude Code without drifting off-pattern, duplicating logic, or spending context re-explaining architecture.

## What this project is

This repository contains a single-page HTML handbook that presents a curated set of fill-in-the-blank prompts for different stages of software development:

- starting a new project
- understanding an existing codebase
- auditing architectural drift
- implementing features using existing patterns
- documenting reusable conventions in `CLAUDE.md`
- debugging with a root-cause mindset

The handbook is designed to help you:

- discover and reuse source-of-truth implementations
- avoid speculative abstractions
- keep dependencies flowing in the intended direction
- verify changes with tests, linting, and build checks
- keep Claude focused on the current task instead of re-learning the whole codebase every session

## Live demo / published page

If GitHub Pages is enabled for this repository, the site can be published from the repository settings and viewed as a static page.

## Features

- dark, terminal-inspired UI
- searchable prompt library
- grouped prompt categories
- editable prompt text in a modal
- one-click copy of the edited prompt
- placeholder highlighting for `[PLACEHOLDERS]`
- mobile-friendly navigation
- no backend or external data storage

## Prompt categories

The handbook is organized into four groups:

### Getting Started
Prompts for setting up the mental model and foundation of a project.

- **START-00 — The Core Workflow (read first)**
- **START-01 — New Project — Discovery**
- **START-02 — New Project — Build the Foundation**
- **START-03 — Write CLAUDE.md**

### Understanding a Codebase
Prompts for mapping, auditing, and finding canonical patterns in an existing repository.

- **MAP-01 — Find the Golden Patterns**
- **MAP-02 — Existing Project — First Audit**

### Building Features
Prompts for implementing features while reusing the existing architecture.

- **BUILD-01 — Simple Feature — One-Shot**
- **BUILD-02 — Search-First Prompt**
- **BUILD-03 — Medium Feature**

### Debugging
The handbook’s workflow also emphasizes fixing root causes and verifying with compiler/linter/test feedback.

## How to use the prompts

1. Open the handbook in your browser.
2. Search for the prompt that matches your task.
3. Open the prompt card.
4. Replace the placeholders with your project details.
5. Copy the prompt into Claude Code.
6. Run the suggested verification steps after implementation.

## Editing the prompt library

All prompt content lives in the `PROMPTS` array inside the main HTML file.

To update the handbook:

- edit the prompt title, blurb, tags, or body
- add new prompt objects to `PROMPTS`
- regroup prompts by changing the `cat` and `catLabel` fields
- keep prompts short, reusable, and specific

## Project structure

This repository is intentionally simple:

- `index.html` — the full app
- `claude-code-prompt-handbook.html` — alternate HTML version / previous revision

The app is built as a static HTML document with embedded CSS and JavaScript.

## Tech stack

- HTML
- CSS
- JavaScript
- Google Fonts: Inter and IBM Plex Mono

## Local usage

You can use the handbook by opening `index.html` directly in a browser.

If you want to serve it locally, use any static file server, for example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## GitHub Pages

This repository can be published as a GitHub Pages site because it is a static HTML project.

To enable it:

1. Go to the repository **Settings**.
2. Open **Pages**.
3. Choose the branch and root folder that contain `index.html`.
4. Save.

## Contributing

When adding or changing prompts, follow the handbook’s own philosophy:

- prefer reuse over duplication
- challenge assumptions
- keep shared guidance concise
- keep prompts actionable
- verify changes with build/test feedback where applicable

## License

Add a license here if you plan to share or redistribute the handbook publicly.