---
name: tpe:alignment-check
description: >
  Cross-check departmental plans for consistency and completeness.
  Identifies where plans contradict, overlap, or leave gaps.
trigger: /tpe:alignment-check
output: Alignment matrix with conflicts and recommendations
skills_loaded: [tpe-framework]
estimated_time: 20-40 minutes
---

# /tpe:alignment-check — Verify Cross-Driver Alignment

## What This Command Does
Reads multiple existing plans/documents and systematically checks whether
they align with each other. This is the core TPE value proposition:
eliminating silos by making contradictions visible.

## Input Required
- At least 2 existing plan documents (ideally all 6 drivers)
- Can also work with departmental plans not yet formatted as TPE drivers

## Execution Workflow

### Step 1: Extract Key Data Points
From each document, extract:
- Revenue/growth targets with timelines
- Headcount numbers and hiring plans
- Budget allocations and investment plans
- Customer/market targets
- Capacity assumptions
- Timeline commitments

### Step 2: Run the Six Alignment Rules
From tpe-framework.md:

CHECK 1 — Portfolio <-> Financial:
- Do revenue projections in Financial match growth targets in Portfolio?
- Are M&A costs budgeted in Financial capex?
- Result: ALIGNED / CONFLICT / INCOMPLETE

CHECK 2 — Marketing <-> Portfolio:
- Do customer segments map to actual product/service lines?
- Are new products in Portfolio reflected in Marketing's GTM plan?
- Result: ALIGNED / CONFLICT / INCOMPLETE

CHECK 3 — Organizational <-> Operational:
- Does headcount plan support operational capacity needs?
- Are key operational roles included in HR hiring plan?
- Result: ALIGNED / CONFLICT / INCOMPLETE

CHECK 4 — Reputation <-> Marketing:
- Is brand positioning consistent with marketing messaging?
- Do PR targets align with marketing campaign calendar?
- Result: ALIGNED / CONFLICT / INCOMPLETE

CHECK 5 — Financial <-> Organizational:
- Do compensation budgets match HR headcount and salary bands?
- Are training/development costs included in Financial budget?
- Result: ALIGNED / CONFLICT / INCOMPLETE

CHECK 6 — Operational <-> Financial:
- Are IT investment plans reflected in capital expenditure budgets?
- Do operational efficiency targets match Financial cost reduction goals?
- Result: ALIGNED / CONFLICT / INCOMPLETE

### Step 3: Run Strategic Direction Traceability
- Is every dimension (Line of Business, Products, Channels, Customers,
  Geography, Business Model) covered by at least one driver?
- Are there dimensions with conflicting information across drivers?

### Step 4: Produce Alignment Matrix

Format:
```
ENTERPRISEAI TPE ALIGNMENT MATRIX
Company: [name]
Date: [date]

ALIGNMENT SUMMARY
Total checks: 6
Aligned: [n]  |  Conflicts: [n]  |  Incomplete: [n]

DETAILED MATRIX
| Check | Driver A | Driver B | Status | Issue | Resolution |
|-------|----------|----------|--------|-------|------------|
| 1 | Portfolio | Financial | CONFLICT | Revenue gap of 2M | Adjust Portfolio targets down or Financial up |
| 2 | Marketing | Portfolio | ALIGNED | — | — |
| ... | | | | | |

CONFLICT DETAIL
[For each CONFLICT:]
- What Driver A says: [specific quote/number]
- What Driver B says: [specific quote/number]
- The gap: [quantified]
- Suggested resolution options:
  Option A: Adjust [Driver A] to match [Driver B] — impact: [describe]
  Option B: Adjust [Driver B] to match [Driver A] — impact: [describe]
  Option C: Meet in the middle at [number] — impact: [describe]

DIMENSION COVERAGE
| Dimension | Covered By | Consistent? | Gaps |
|-----------|-----------|------------|------|

RECOMMENDED ACTIONS
1. [Most critical conflict] — resolve by [date]
2. ...
```

## Special Case: Non-TPE Documents
If user provides departmental plans not formatted as TPE drivers:
- First map each document to the closest TPE driver
- Extract relevant data points using same methodology
- Note in report which documents don't fully map to TPE structure
- Recommend converting to TPE format for ongoing alignment tracking
