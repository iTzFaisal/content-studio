# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) and OpenCode when working with code in this repository.

## Project Overview

This is a multi-purpose workspace with two main capabilities:

### 1. Document Generation

Creating professional office files including:

- Word documents (.docx)
- Excel documents (.xlsx)
- PowerPoint presentations (.pptx)
- PDF files (.pdf)
- Markdown reports (.md)

### 2. Marketing & Content Operations

A comprehensive toolkit for marketing, SEO, content, and growth:

- **SEO & Content**: SEO audits, programmatic SEO, AI optimization, schema markup
- **Copy & Creative**: Copywriting, editing, ad creative, social content
- **CRO & Optimization**: Page CRO, form CRO, signup flows, onboarding, paywalls
- **Campaign & Growth**: Email sequences, cold email, paid ads, referral programs
- **Strategy**: Pricing, launch strategy, content strategy, marketing ideas
- **Operations**: Analytics tracking, RevOps, sales enablement, churn prevention

## Key Dependencies

- **docx** (^9.6.0) — Word document creation (via skill)
- **pptxgenjs** (^4.0.1) — PowerPoint presentation generation (via skill)
- **xlsx** — Excel and spreadsheet manipulation (via skill)
- **pdf** — PDF creation, merging, splitting, OCR (via skill)

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

This project uses Claude Code skills to generate documents and perform marketing operations. Use the appropriate skill based on the output format:

### Office Document Skills

- `/docx` - Create, read, edit, or manipulate Word documents (.docx)
- `/xlsx` - Create, read, edit, or manipulate spreadsheets (.xlsx, .csv, .tsv)
- `/pptx` - Create, read, edit, or modify PowerPoint presentations (.pptx)
- `/pdf` - Work with PDF files including creation, merging, splitting, OCR

### Marketing Skills

Invoke by name (e.g., `/seo-audit`, `/copywriting`, `/cold-email`). Available categories:

- **SEO**: `/seo-audit`, `/programmatic-seo`, `/ai-seo`, `/schema-markup`
- **Content**: `/copywriting`, `/copy-editing`, `/content-strategy`, `/social-content`, `/humanizer`
- **CRO**: `/page-cro`, `/form-cro`, `/signup-flow-cro`, `/onboarding-cro`, `/paywall-upgrade-cro`, `/popup-cro`
- **Campaigns**: `/email-sequence`, `/cold-email`, `/paid-ads`, `/ad-creative`, `/referral-program`
- **Strategy**: `/pricing-strategy`, `/launch-strategy`, `/marketing-ideas`, `/free-tool-strategy`, `/site-architecture`
- **Analytics**: `/analytics-tracking`, `/revops`, `/sales-enablement`, `/product-marketing-context`
- **Growth**: `/churn-prevention`, `/competitor-alternatives`, `/ab-test-setup`

**Skill Storage:** Skills are stored in `.agents/skills/` (for Opencode) and symlinked in `.claude/skills/` (for Claude Code). Each skill has a `SKILL.md` file with detailed documentation.

When document generation is requested, Claude will typically:

1. Use the appropriate skill to generate the document
2. Save the output to the current working directory
3. Use meaningful filenames that describe the content
