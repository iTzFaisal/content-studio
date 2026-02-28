# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a document generation workspace for creating office files including:

- Word documents (.docx)
- Excel documents (.xlsx)
- PowerPoint presentations (.pptx)
- PDF files (.pdf)
- Markdown reports (.md)

## Key Dependencies

- **docx** (^9.6.0) - JavaScript library for creating Word documents
- **pptxgenjs** (^4.0.1) - JavaScript library for generating PowerPoint presentations

## Toolchain Preferences

### Node.js Packages

- **Always install packages in project scope**, never globally:
  ```bash
  npm install <package>      # Correct
  npm install -g <package>   # NEVER use this
  ```

### Python Runtime

- **Use `uv` instead of `python3`** for running Python scripts and package management:
  ```bash
  uv run <script.py>         # Run Python scripts
  uv add <package>   # Install Python packages
  ```

## Creating Documents

This project uses Claude Code skills to generate documents. Use the appropriate skill based on the output format:

- `/docx` - Create, read, edit, or manipulate Word documents (.docx)
- `/pptx` - Create, read, edit, or modify PowerPoint presentations (.pptx)
- `/pdf` - Work with PDF files including creation, merging, splitting, OCR
- `/xlsx` - Create or manipulate spreadsheets

**Skill Storage:** Skills are stored in `.agents/skills/` (for Opencode) and symlinked in `.claude/skills/` (for Claude Code). Each skill has a `SKILL.md` file with detailed documentation.

When document generation is requested, Claude will typically:

1. Use the appropriate skill to generate the document
2. Save the output to the current working directory
3. Use meaningful filenames that describe the content
