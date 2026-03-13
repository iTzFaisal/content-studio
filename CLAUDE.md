# CLAUDE.md

**Content Studio** - A professional workspace for document generation.

This file provides guidance to Claude Code (claude.ai/code) and OpenCode when working with code in this repository.

## Project Overview

Content Studio is a workspace for generating professional office documents using specialized AI skills.

### Document Generation Skills

| Skill  | Format       | Purpose |
| ------ | ------------ | ------- |
| `/docx` | Word (.docx) | Proposals, reports, white papers, contracts |
| `/xlsx` | Excel (.xlsx) | Financial models, data analysis, templates |
| `/pptx` | PowerPoint (.pptx) | Pitch decks, presentations, training materials |
| `/pdf` | PDF (.pdf) | Final deliverables, forms, professional documents |

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

## Using Document Skills

All skills are invoked by name with your instructions:

- `/docx` - Create, read, edit, or manipulate Word documents (.docx)
- `/xlsx` - Create, read, edit, or manipulate spreadsheets (.xlsx, .csv, .tsv)
- `/pptx` - Create, read, edit, or modify PowerPoint presentations (.pptx)
- `/pdf` - Work with PDF files including creation, merging, splitting, OCR

### Example Usage

```bash
# Create a professional document
/docx "Write a consulting proposal with executive summary, scope, timeline, and pricing"

# Build a presentation
/pptx "Create a 10-slide pitch deck for a SaaS startup"

# Generate a spreadsheet
/xlsx "Create a financial model with 24-month projections"

# Manipulate PDFs
/pdf "Merge these three reports into a single document"
```

**Skill Storage:** Skills are stored in `.agents/skills/` (for Opencode) and symlinked in `.claude/skills/` (for Claude Code). Each skill has a `SKILL.md` file with detailed documentation.

When document generation is requested, Claude will typically:

1. Use the appropriate skill to create or format the document
2. Save the output to the current working directory
3. Use meaningful filenames that describe the content

## Source

Skills are sourced from [anthropics/skills](https://github.com/anthropics/skills) — enterprise-grade document generation with native office format handling.
