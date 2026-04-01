# DXV-89 Draft SOP: One-Off Internal Donor Data Requests

## Status
- **Draft only** for review.
- **No donor-data actions executed**.
- **Stop point reached** before final completion or implementation.

## Purpose
Provide a consistent, low-risk process for handling ad hoc internal requests that require donor data lookups, extracts, summaries, or light analysis.

## Scope
This SOP applies to one-off internal requests received through Slack, email, meetings, or verbal asks that involve donor data from systems such as DonorPerfect or related reporting exports.

Out of scope:
- Recurring reports (should become recurring ops items).
- Bulk imports/updates or destructive CRM actions.
- External stakeholder communications without explicit approval.

## Guiding Principles
1. **Data minimization**: provide only what was requested and necessary.
2. **Need-to-know access**: validate requester role and legitimate purpose.
3. **Auditability**: keep a clear request-to-delivery record.
4. **Reproducibility**: document query/report logic enough to rerun.
5. **Approval-first for risky actions**: pause before sensitive or high-impact steps.

## Intake & Triage Workflow

### 1) Capture request
Record:
- Requester name/team
- Request date
- Business question / intended decision
- Requested fields
- Timeframe
- Delivery deadline
- Delivery format (sheet, CSV, summary)

### 2) Classify request risk
- **Low risk**: aggregate totals/counts; no sensitive PII beyond normal internal use.
- **Moderate risk**: record-level donor data with contact/history fields.
- **High risk**: sensitive notes, financial/bank details, broad exports, or unclear purpose.

### 3) Validate authorization
Confirm requester has internal need-to-know for the requested donor data. If unclear, escalate to manager/data owner before proceeding.

### 4) Clarify requirements
Before any extraction:
- Confirm exact filters (campaign/date/source/status).
- Confirm dedupe expectations (household vs individual).
- Confirm metric definitions (e.g., “new donor,” “LYBUNT”).
- Confirm whether identifiers are necessary or if aggregation is sufficient.

### 5) Prepare implementation plan (no execution yet)
Draft:
- Data source(s)
- Query/report logic
- Fields to include/exclude
- QA checks to run
- Delivery method

### 6) Approval gate for sensitive steps
Require explicit human approval before:
- broad record-level exports
- inclusion of sensitive fields
- any bulk update/import/delete actions
- cross-system joins involving sensitive data

### 7) Execute approved extraction/analysis
(Operational step to be run only after approval.)
- Pull minimal data set.
- Perform QA checks.
- Produce output in approved format.

### 8) QA checklist
- Spot-check donor IDs and gift totals against source records.
- Validate date filter boundaries/timezone assumptions.
- Check duplicates and null critical fields.
- Verify row counts vs expected baseline.
- Ensure restricted fields are not present.

### 9) Deliver and document
- Deliver via approved internal channel.
- Include caveats/definitions used.
- Store request notes and logic in issue.
- Mark whether request should become recurring.

### 10) Closeout
- Log completion date and owner.
- Record follow-up questions.
- Capture improvement opportunities for future SOP updates.

## Standard Response SLAs (Draft)
- Acknowledge intake: **same business day**.
- Clarification questions sent: **within 1 business day**.
- Initial delivery estimate: **within 1 business day after clarification**.
- Typical turnaround:
  - Low risk/simple: 1–2 business days
  - Moderate/custom: 2–4 business days
  - High risk/approval-dependent: variable (pending approvals)

## Suggested Linear Issue Updates (copy/paste)

### Proposed issue description update
```md
## Objective
Draft and adopt a standard operating procedure for one-off internal donor data requests.

## Scope for this issue
- Draft SOP process and checklist
- Define approval gates and QA expectations
- Provide reusable intake template and issue-update language

## Non-goals
- No direct donor-data changes or production imports/exports in this issue
- No operational execution of specific donor request

## Definition of done (for drafting phase)
- SOP draft reviewed by human assignee
- Any requested revisions incorporated
- Final approval to operationalize captured in follow-up step
```

### Suggested progress update comment
```md
Draft SOP prepared for one-off internal donor data requests, including intake, risk classification, approval gates, QA checklist, and delivery documentation steps.

No donor-data changes were performed.

Stopping here for human review/approval before finalizing or operationalizing the SOP.
```

### Suggested labels / metadata
- Keep `agent-candidate`
- Add `codex-drafted`
- Add `needs-human-approval` if final SOP adoption requires sign-off

## Intake Template (for future one-off requests)
```md
### Donor Data Request Intake
- Requester:
- Team/Role:
- Date requested:
- Business question:
- Decision supported by this request:
- Required fields:
- Preferred aggregation level (aggregate / record-level):
- Time period:
- Filters/segments:
- Deadline:
- Delivery format:
- Sensitivity concerns:
- Approval required? (Y/N + approver):
```

## Explicit Stop Point (per issue constraint)
This draft intentionally **stops before final completion**. Next step is human review and approval to finalize/adopt the SOP.
