---
name: tpe:scheduled-review
description: >
  Set up and execute recurring plan reviews. Compares actuals to targets,
  flags deviations, and prepares review agendas.
trigger: /tpe:scheduled-review
output: Review agenda + updated RAG dashboard + deviation report
skills_loaded: [tpe-framework, financial-driver]
estimated_time: 15-20 minutes per review cycle
---

# /tpe:scheduled-review — Recurring Plan Reviews

## What This Command Does
Establishes a cadence of plan reviews and executes them. Each review
compares actual performance to planned targets, updates the KPI dashboard,
and produces a focused agenda for the review meeting.

This is the "living document" engine — it keeps the TPE plan current.

## Input Required

### First-time setup:
- Review frequency: weekly (operational), monthly (tactical),
  quarterly (strategic), or combination
- Who attends each review level?
- Which KPIs are reviewed at each level?
- Where is actual performance data? (Excel, Google Sheets, ERP, manual)

### Each review cycle:
- Updated actuals (upload spreadsheet or enter manually)
- Any known changes to plans since last review
- Any escalation items from previous review

## Execution Workflow

### Step 1: Load Current State
- Read the latest TPE plan and KPI dashboard
- Read previous review notes (if available)
- Load updated actuals from user

### Step 2: Compare Actuals vs. Targets
For each KPI:
- Calculate variance (actual vs. target)
- Determine RAG status based on thresholds
- Identify trend (improving, stable, declining)
- Flag any KPI that changed RAG status since last review

### Step 3: Identify Deviations Requiring Discussion
Priority ranking:
- P1: KPIs that moved from GREEN to RED (critical)
- P2: KPIs that moved from GREEN to AMBER (early warning)
- P3: KPIs that have been AMBER for 2+ review cycles (persistent)
- P4: KPIs that moved from RED to AMBER (improving but not resolved)

### Step 4: Check Cross-Driver Impact
For each significant deviation:
- Which other drivers are affected?
- Does this deviation create a new alignment conflict?
- What action is needed in other drivers to compensate?

### Step 5: Produce Review Package

DOCUMENT 1: REVIEW AGENDA
```
TPE [WEEKLY/MONTHLY/QUARTERLY] REVIEW
Company: [name] | Period: [date range] | Meeting date: [date]

ATTENDEES: [list]

AGENDA

1. DASHBOARD UPDATE (5 min)
   - Overall RAG status per driver
   - KPIs that changed status since last review

2. PRIORITY ITEMS (20 min)
   [P1 items — discuss and decide]
   - KPI: [name] — was GREEN, now RED
     Current: [value] | Target: [value] | Gap: [value]
     Root cause: [assessment]
     Proposed action: [recommendation]
     Cross-driver impact: [which drivers affected]

3. EARLY WARNINGS (10 min)
   [P2 and P3 items — awareness and monitoring]

4. POSITIVE TRENDS (5 min)
   [P4 items and any GREEN improvements — celebrate progress]

5. PLAN UPDATES NEEDED (10 min)
   - Changes to targets or timelines
   - New risks or opportunities
   - Resource reallocation needs

6. ACTIONS AND OWNERS (5 min)
   | Action | Owner | Deadline | Driver |
   |--------|-------|----------|--------|

7. NEXT REVIEW: [date]
```

DOCUMENT 2: UPDATED KPI DASHBOARD
- Excel with current actuals populated
- RAG status updated
- Trend arrows added
- Variance column added

DOCUMENT 3: DEVIATION REPORT (for quarterly reviews)
```
QUARTERLY DEVIATION REPORT

EXECUTIVE SUMMARY
- [n] KPIs on track | [n] at risk | [n] off track
- Overall plan health: [assessment]

PER-DRIVER SUMMARY
| Driver | On Track | At Risk | Off Track | Overall |
|--------|----------|---------|-----------|---------|

SIGNIFICANT DEVIATIONS
[For each P1/P2:]
- Driver: [name]
- KPI: [name]
- Target: [value] | Actual: [value] | Variance: [%]
- Trend: [improving/stable/declining]
- Root cause: [analysis]
- Impact on other drivers: [assessment]
- Recommended action: [specific]
- Owner: [name] | Deadline: [date]

PLAN REVISION RECOMMENDATIONS
[If deviations require changing the plan itself, not just execution]
1. [Recommended change] — rationale — impact
```

## Review Cadence Best Practices
- WEEKLY: Operational KPIs only (process metrics, SLAs, daily numbers).
  15-minute standup format. Driver owners attend.
- MONTHLY: All driver KPIs. 45-minute review. Department heads attend.
  Focus on AMBER items before they become RED.
- QUARTERLY: Full strategic review including dimensions. 2-hour session.
  Executive team attends. Includes plan revision decisions.
- ANNUALLY: Full TPE plan refresh. Run /tpe:full-plan again with updated
  context. Half-day workshop format.

## Scheduling (Cowork Feature)
When Cowork scheduling is available:
- Set up recurring task to prompt user for updated actuals
- Auto-generate review agenda 2 days before scheduled review
- Send reminder via Gmail/Slack to review attendees
- Archive previous reviews for trend analysis
