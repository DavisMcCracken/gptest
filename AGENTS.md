# AGENTS.md

## Project overview

**gptest** is a documentation-only repository for Linear issue **DXV-89**. It contains a draft Standard Operating Procedure (SOP) for one-off internal donor data requests. There is no application source code, build tooling, or runnable services.

| File | Purpose |
|------|---------|
| `README.md` | Entry point; links to the SOP draft |
| `DXV-89_sop_draft.md` | Full SOP draft with intake workflow, QA checklist, and Linear issue update templates |

## Cursor Cloud specific instructions

### Environment

This repo has **no dependencies to install** and **no services to start**. Development work here is limited to editing and reviewing Markdown.

### Lint / test / build

There are no configured lint, test, or build commands. To sanity-check documentation changes, validate markdown structure manually or with a one-off script (see validation example in setup notes).

### Running the "application"

There is no application. The core artifact is the SOP markdown file. A successful workflow means:

1. `git status` shows a clean or expected working tree.
2. `README.md` and `DXV-89_sop_draft.md` are present and readable.
3. The SOP contains expected sections: Purpose, Scope, Intake workflow, QA checklist, Linear templates, and the explicit stop point.

### External systems (not in this repo)

The SOP references DonorPerfect, Slack, email, and Linear as operational context for real donor-data workflows. These are **not** integrated or runnable from this repository.
