# AGENTS.md

## Project overview

**gptest** is a documentation-only repository for RMHCK Linear planning artifacts. It contains draft SOPs and infrastructure plans. There is no application source code, build tooling, or runnable services.

| File | Purpose |
|------|---------|
| `README.md` | Entry point; links to issue artifacts |
| `DXV-89_sop_draft.md` | SOP draft for one-off internal donor data requests |
| `RMH-144_n8n_fedora_plan.md` | n8n on Fedora deployment plan, threat/ops notes, approval gates |
| `docs/n8n/` | Reference Compose and config templates for RMH-144 (planning only) |

## Cursor Cloud specific instructions

### Environment

This repo has **no dependencies to install** and **no services to start**. Development work here is limited to editing and reviewing Markdown.

### Lint / test / build

There are no configured lint, test, or build commands. To sanity-check documentation changes, validate markdown structure manually or with a one-off script (see validation example in setup notes).

### Running the "application"

There is no application. The core artifact is the SOP markdown file. A successful workflow means:

1. `git status` shows a clean or expected working tree.
2. `README.md` and issue artifact markdown files are present and readable.
3. Each artifact contains expected sections and an explicit stop point before production execution or credential use.

### External systems (not in this repo)

The SOP references DonorPerfect, Slack, email, and Linear as operational context for real donor-data workflows. These are **not** integrated or runnable from this repository.
