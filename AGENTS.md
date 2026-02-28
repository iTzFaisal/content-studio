# AGENTS.md

This file orients agentic coding tools working in this repository. It is derived from and consistent with `CLAUDE.md`.

## 1) Repository Purpose

This is a document generation workspace focused on producing office files:

- Word documents (.docx)
- Excel spreadsheets (.xlsx)
- PowerPoint presentations (.pptx)
- PDF files (.pdf)
- Markdown reports (.md)

The output files in the repository root are the primary deliverables.

## 2) Key Dependencies

The repository is intentionally small. Currently installed dependencies:

- docx (^9.6.0) — JavaScript library for Word documents
- pptxgenjs (^4.0.1) — JavaScript library for PowerPoint

Do not add new dependencies unless the user explicitly requests it.

## 3) Toolchain Preferences (Required)

### Node.js

- Always install packages locally, never globally.
- Correct: `npm install <package>`
- Never: `npm install -g <package>`

### Python

- Use `uv` for Python execution and package management.
- Run scripts: `uv run <script.py>`
- Add packages: `uv add <package>`

## 4) Build, Lint, Test

There are currently no build, lint, or test scripts configured.

- `package.json` contains only dependencies and no scripts.
- No Makefile, pyproject.toml, or test runner configuration exists.

If you add tooling, you must update this file with exact commands.

### Running a Single Test

No test framework is configured yet.

When a test framework is introduced, document single-test commands such as:

- `npm test -- <test-file-or-pattern>`
- `uv run pytest -k <pattern> path/to/test_file.py`

## 5) Document Generation Workflow

When asked to create or edit office documents, use the appropriate skill:

- `/docx` — Word documents
- `/pptx` — PowerPoint presentations
- `/pdf` — PDF tasks (merge/split/OCR/creation)
- `/xlsx` — Spreadsheets and tabular data

**Skill Architecture:**
- `.agents/skills/` — Skill definitions for Opencode agent system
- `.claude/skills/` — Symlinks to `.agents/skills/` for Claude Code access
- Each skill directory contains `SKILL.md` with implementation details and `scripts/` for utilities

Expected behavior:

1. Use the correct skill for the document type.
2. Save the output to the repository root unless instructed otherwise.
3. Use descriptive filenames.

## 6) Code Style Guidelines

These guidelines apply to any scripts or code added to the repo.

### Imports

- Use explicit, named imports when supported.
- Group imports: standard library, third-party, then local.
- Keep import sections short and readable.

### Formatting

- Match the existing file style; avoid reformatting unrelated code.
- Use consistent indentation and spacing.
- Keep lines reasonably short for readability.

### Types

- This repo is JavaScript-only today; no TypeScript config exists.
- If you introduce TypeScript, document compiler settings here.
- Prefer well-defined object shapes over loose, unstructured data.

### Naming

- Use domain-specific names (document, section, slide, table).
- Prefer verbs for functions: `generateReport`, `buildSlideDeck`.
- Avoid abbreviations unless they are standard in this domain.

### Error Handling

- Validate inputs early.
- Provide actionable error messages with file paths.
- Do not swallow errors; rethrow with context if needed.

### File and Path Handling

- Use safe path operations instead of manual string concatenation.
- Keep output paths deterministic and easy to locate.
- Do not overwrite existing outputs unless asked.

## 7) Repository Hygiene

- Do not revert user changes unless explicitly requested.
- Avoid destructive git commands.
- Do not amend commits unless asked.
- Do not push unless explicitly requested.

## 8) Cursor/Copilot Rules

- No `.cursor/rules/`, `.cursorrules`, or `.github/copilot-instructions.md` were found in this repository.

## 9) When Adding Tooling

If you add any build/lint/test tooling:

- Update section 4 with concrete commands.
- Include “single test” instructions.
- Document any formatting or lint rules you introduce.

## 10) Document Quality Checks

- Verify outputs open correctly in their target apps.
- Confirm fonts/layout render as expected.
- Keep asset paths relative to repo root.

## 11) Security

- Do not place secrets or credentials in documents or config.
- Avoid embedding API keys in generated files.

## 12) Summary for Agents

This repo is intentionally minimal. Follow `CLAUDE.md`, use `uv` for Python,
install npm packages locally only, and use the document skills for office files.
