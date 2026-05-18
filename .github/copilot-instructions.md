# GitHub Copilot Instructions for this Repository

This repository is minimal: a static site with a single entrypoint. The goal of these instructions is to help AI agents be productive quickly by describing the project's structure, expected workflows, and notable patterns discovered in the codebase.

**Big Picture**
- **Type:** Static website (single-page) — no build system detected.
- **Entry point:** index.html — the whole site is delivered from this file.
- **Why:** The project appears to be a simple static artifact rather than a multi-component app; changes will usually be made directly in `index.html` or added alongside it.

**Developer workflows**
- **Run / preview:** Open `index.html` in a browser or use a static server (examples below).
  - Quick local preview: `npx http-server .` or `python -m http.server 8000`
- **No tests/build:** No package.json, build scripts, or test harness were found. Avoid adding complex tooling without user direction.

**Project-specific conventions & patterns**
- Keep changes minimal and localized to `index.html` unless user asks to add assets or tooling.
- If adding JavaScript or CSS, prefer placing files in top-level folders named `js/` or `css/` and reference them from `index.html`.

**Integration points & dependencies**
- No external package manager files detected (no `package.json`, `requirements.txt`, or similar). External libraries, if needed, should be added via CDN links in `index.html` or by explicitly adding a package manifest after consulting the repo owner.

**What an AI agent should do on first changes**
- Inspect `index.html` to identify markup, inline scripts, and linked assets.
- If you need to add tools (linters/build/test), propose them to the user first and include minimal configs only after approval.

**Examples (from this repo)**
- Entry point example: [index.html](index.html#L1) — modify this file for content and static behavior changes.

**Safety & scope notes**
- Do not invent hidden services, servers, or CI configs — this repository contains only static files.
- When asked to implement features that imply server-side logic, propose minimal local alternatives (e.g., static JSON, third-party APIs) and ask for confirmation.

If anything here is unclear or you want me to expand specific sections (build setup, CI, test harness, or adding a frontend framework), tell me which direction you prefer and I'll update this file.
