---
name: tpe:kpi-dashboard
description: >
  Generate KPIs for each driver aligned to strategy, with owners
  and RAG thresholds. Produces an Excel dashboard.
trigger: /tpe:kpi-dashboard
output: Excel workbook with KPI dashboard per driver
skills_loaded: [tpe-framework, financial-driver]
estimated_time: 20-30 minutes
---

# /tpe:kpi-dashboard — Build KPI Dashboard

## What This Command Does
Creates a comprehensive KPI framework linked to each driver and strategic
dimension. Produces an Excel workbook ready for ongoing performance tracking.

## Input Required
- Completed driver plans (or at least targets from /tpe:full-plan)
- Preferred review cadence (weekly/monthly/quarterly)
- Who are the KPI owners? (names or roles)

## Execution Workflow

### Step 1: Extract Targets From Each Driver
For each of the 6 drivers, identify:
- Quantitative targets with year columns
- Qualitative goals
- Critical success factors

### Step 2: Define KPIs Per Driver

PORTFOLIO KPIs:
- Revenue per business line (vs. target)
- Market share per line
- M&A pipeline status
- Partnership value delivered
- Lines at risk (below target performance)

MARKETING KPIs:
- Customer acquisition per segment
- Revenue per channel
- Customer acquisition cost (CAC)
- Customer lifetime value (LTV)
- Market penetration per geography
- Net Promoter Score per segment

ORGANIZATIONAL KPIs:
- Headcount vs. plan
- Employee satisfaction score
- Voluntary turnover rate
- Training hours per employee
- D&I metrics vs. targets
- Succession readiness (% of key roles with identified successor)

OPERATIONAL KPIs:
- Process cycle times vs. targets
- System uptime / availability
- Customer service SLA achievement
- Automation adoption rate
- IT project delivery (on time, on budget)
- Cybersecurity incident count

REPUTATIONAL KPIs:
- Brand awareness score
- Media coverage (volume and sentiment)
- Social media engagement
- Compliance audit results
- ESG score / sustainability metrics
- Employee advocacy score

FINANCIAL KPIs:
- Revenue vs. budget
- EBITDA margin
- Cost-income ratio
- Cash flow vs. forecast
- ROI on key investments
- Budget variance per driver

### Step 3: Assign Owners and Thresholds

For each KPI define:
- Owner (name or role)
- GREEN threshold (on track)
- AMBER threshold (at risk — needs attention)
- RED threshold (off track — action required)
- Review frequency (daily/weekly/monthly/quarterly)
- Data source (where does the number come from?)

### Step 4: Link to Strategic Dimensions
Map each KPI to the Strategic Direction dimension(s) it measures:

| KPI | Driver | Dimension(s) | Frequency |
|-----|--------|-------------|-----------|

### Step 5: Produce Excel Workbook

TAB STRUCTURE:
- Tab 1: EXECUTIVE DASHBOARD
  - RAG summary per driver (6 boxes, color coded)
  - Top 5 KPIs at risk
  - Trend arrows (improving/stable/declining)
  - Strategic Direction dimension coverage

- Tab 2: PORTFOLIO KPIs
  - All portfolio KPIs with actuals, targets, RAG, trend
  - Conditional formatting applied

- Tab 3: MARKETING KPIs
  - All marketing KPIs with same format

- Tab 4: ORGANIZATIONAL KPIs
- Tab 5: OPERATIONAL KPIs
- Tab 6: REPUTATIONAL KPIs
- Tab 7: FINANCIAL KPIs

- Tab 8: DIMENSION TRACKER
  - One row per strategic dimension
  - Linked KPIs per dimension
  - Overall dimension health (RAG)

- Tab 9: DATA INPUT
  - Where users enter actual values each period
  - Formulas auto-calculate RAG status
  - Protected formulas, editable data cells

## Formatting Standards
- Conditional formatting: GREEN (#00B050), AMBER (#FFC000), RED (#FF0000)
- Headers in EnterpriseAI blue (#2E75B6)
- Frozen header rows and first columns
- Print-friendly layout (landscape, fit to page)
- Charts: sparklines for trends where possible
