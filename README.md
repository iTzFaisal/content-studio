# Content Studio

**Transform ideas into professional documents.**

Content Studio is your workspace for generating polished Word documents, Excel spreadsheets, PowerPoint presentations, and PDFs — powered by specialized AI skills.

---

## What You Can Do

### Generate Professional Documents

| Skill                 | Output Format | Perfect For                                       |
| --------------------- | ------------- | ------------------------------------------------- |
| **`/docx`**           | Word (.docx)  | Proposals, reports, white papers, contracts       |
| **`/xlsx`**           | Excel (.xlsx) | Financial models, data analysis, templates        |
| **`/pptx`**           | PowerPoint    | Pitch decks, presentations, training materials    |
| **`/pdf`**            | PDF (.pdf)    | Final deliverables, forms, professional documents |

**Every document looks like it came from a professional designer.**

---

## How It Works

### Simple Command-Based Workflow

```
/<skill-name> [your instructions]
```

**Try these now:**

- `/docx Write a professional proposal for a web design project`
- `/xlsx Create a financial model with projections for the next 12 months`
- `/pptx Build a 10-slide pitch deck for a SaaS startup`
- `/pdf Combine these three reports into a single document`

### See It In Action

```bash
# Create a professional proposal
/docx "Write a consulting proposal for a website redesign project. Include executive summary, scope of work, timeline, and pricing."

# Build a pitch deck from your content
/pptx "Create a 10-slide investor pitch deck with title, problem, solution, market size, and team slides."

# Generate a financial model
/xlsx "Build a SaaS financial model with monthly projections for revenue, costs, and cash flow over 24 months."

# Work with existing PDFs
/pdf "Merge these three reports into a single document and add a table of contents."
```

---

## Features

### Word Documents (`/docx`)

- Create professional documents with formatting, styles, and layouts
- Add tables of contents, headers, footers, and page numbers
- Insert and replace images
- Work with tracked changes and comments
- Convert content into polished Word documents

### Excel Spreadsheets (`/xlsx`)

- Create spreadsheets with formulas and formatting
- Clean and restructure messy tabular data
- Add charts and visualizations
- Work with .xlsx, .xlsm, .csv, and .tsv files
- Build templates and financial models

### PowerPoint Presentations (`/pptx`)

- Create slide decks, pitch decks, and presentations
- Work with templates, layouts, speaker notes, and comments
- Extract or combine content from multiple presentations
- Design persuasive presentations

### PDF Files (`/pdf`)

- Create new PDFs from scratch
- Merge multiple PDFs into one
- Split PDFs apart
- Rotate pages and add watermarks
- Extract text and images
- OCR on scanned PDFs
- Fill PDF forms
- Encrypt/decrypt PDFs

---

## Get Started

### What You Need

Content Studio works with tools you may already have:

- **[Claude Code](https://claude.ai/code)** — Anthropic's AI CLI
- **OpenCode** — Compatible AI assistant

---

## Project Structure

```
content-studio/
├── .agents/skills/        # Office document skills
│   ├── docx/              # Word document generation
│   ├── pdf/               # PDF manipulation
│   ├── pptx/              # PowerPoint presentations
│   └── xlsx/              # Excel spreadsheets
├── .claude/skills/        # Symlinked for Claude Code
├── CLAUDE.md              # Project instructions
├── skills-lock.json       # Skill version manifest
└── README.md              # You are here
```

---

## Built on Trusted Sources

Content Studio uses enterprise-grade document generation skills from:

**Source: [anthropics/skills](https://github.com/anthropics/skills)**

- Native office format handling (.docx, .xlsx, .pptx, .pdf)
- Production-ready output quality
- Built-in best practices for professional documents

---

## Related Resources

- 📖 [Claude Code Documentation](https://docs.anthropic.com/claude/code)
- ⚙️ [CLAUDE.md](./CLAUDE.md) — Project-specific guidance
- 🔒 [skills-lock.json](./skills-lock.json) — Skill version manifest

---

**Ready to create something remarkable?**

Content Studio gives you the output quality of a design agency — all in one workspace.

**Start creating →**
