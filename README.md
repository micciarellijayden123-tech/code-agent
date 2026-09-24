# Forge — a coding agent

A single-page coding agent that writes and runs JavaScript live, built as a Claude artifact.

## How it works
- `code-agent.html` is a self-contained page: all HTML, CSS, and JS in one file.
- It uses Claude (via the page's `sample` capability) as the agent's "brain."
- It gives Claude a `run_javascript` tool, sandboxed with `new Function()`, so the
  agent can write code and actually execute it before replying.

## Important: where this runs
This page only works when opened through **claude.ai**, because it calls
`window.claude.use('sample')` to think. That capability is provided by Claude's
artifact viewer — it is **not** available in a plain browser, GitHub Pages, or any
other static host. Opening `code-agent.html` outside claude.ai will load the page,
but the agent won't be able to respond.

This repo is for version control / backup of the source, not for hosting a live copy
elsewhere.

## Editing
Open `code-agent.html` in VS Code, make changes, then re-publish it as a Claude
artifact to see the updated version live.
