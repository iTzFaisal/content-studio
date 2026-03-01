# CLAUDE.md

**Content Studio** - A professional workspace for content creation and document generation.

This file provides guidance to Claude Code (claude.ai/code) and OpenCode when working with code in this repository.

## Project Overview

Content Studio is a multi-purpose workspace combining content expertise with professional document production:

### 1. Content Creation

Marketing, copywriting, and content skills help craft, refine, and optimize content:

- **Copy & Creative**: Copywriting, editing, ad creative, social content, humanizer
- **SEO & Content**: SEO audits, programmatic SEO, AI optimization, schema markup
- **Strategy**: Content strategy, pricing strategy, launch strategy, marketing ideas
- **CRO & Optimization**: Page CRO, form CRO, signup flows, onboarding, paywalls
- **Campaign & Growth**: Email sequences, cold email, paid ads, referral programs
- **Operations**: Analytics tracking, RevOps, sales enablement, churn prevention

### 2. Document Generation

Format content into professional deliverables:

- Word documents (.docx)
- Excel documents (.xlsx)
- PowerPoint presentations (.pptx)
- PDF files (.pdf)
- Markdown reports (.md)

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

## Creating Content & Documents

Content Studio uses a two-phase workflow:

1. **Content Phase**: Use marketing/writing skills to craft and refine content
2. **Document Phase**: Use office skills to format content into professional deliverables

### Content Skills

Invoke by name (e.g., `/copywriting`, `/seo-audit`, `/content-strategy`):

- **SEO**: `/seo-audit`, `/programmatic-seo`, `/ai-seo`, `/schema-markup`
- **Content**: `/copywriting`, `/copy-editing`, `/content-strategy`, `/social-content`, `/humanizer`
- **CRO**: `/page-cro`, `/form-cro`, `/signup-flow-cro`, `/onboarding-cro`, `/paywall-upgrade-cro`, `/popup-cro`
- **Campaigns**: `/email-sequence`, `/cold-email`, `/paid-ads`, `/ad-creative`, `/referral-program`
- **Strategy**: `/pricing-strategy`, `/launch-strategy`, `/marketing-ideas`, `/free-tool-strategy`, `/site-architecture`
- **Analytics**: `/analytics-tracking`, `/revops`, `/sales-enablement`, `/product-marketing-context`
- **Growth**: `/churn-prevention`, `/competitor-alternatives`, `/ab-test-setup`

### Document Skills

- `/docx` - Create, read, edit, or manipulate Word documents (.docx)
- `/xlsx` - Create, read, edit, or manipulate spreadsheets (.xlsx, .csv, .tsv)
- `/pptx` - Create, read, edit, or modify PowerPoint presentations (.pptx)
- `/pdf` - Work with PDF files including creation, merging, splitting, OCR

**Skill Storage:** Skills are stored in `.agents/skills/` (for Opencode) and symlinked in `.claude/skills/` (for Claude Code). Each skill has a `SKILL.md` file with detailed documentation.

When content or document generation is requested, Claude will typically:

1. Use the appropriate skill to create or format the content
2. Save the output to the current working directory
3. Use meaningful filenames that describe the content
