---
name: financial-driver
description: >
  TPE Financial Driver — guides financial planning, capital management,
  budgeting, risk management, KPI tracking, and business performance.
  This is the INTEGRATION DRIVER that validates all other plans.
  Part of the EnterpriseAI 3C framework.
version: 1.0.0
author: EnterpriseAI
parent_skill: tpe-framework
serves_dimensions: [Business Model (primary), all others (integration)]
tags: [finance, budgeting, KPI, risk-management, performance, capital]
---

# Financial Driver Skill — "The Numbers That Prove the Plan Works"

## Purpose
The Financial Driver translates ALL other drivers into financial reality.
It is the ultimate alignment check: if the numbers do not work, the plan
does not work. This driver both constrains and enables the other five.

Serves Strategic Direction dimensions:
- Business Model (primary — defines how money is made)
- All others (integration — every dimension has financial impact)


## Required Sections

### 7.1 Financial Planning and Risk Management
- Financial sustainability: cost-income ratio, capital adequacy
- 3-year P&L projection (2025-2028) with stated assumptions
- Balance sheet projections (if applicable)
- Cash flow forecast with monthly granularity for Year 1
- Scenario analysis: base case, upside case, downside case

| Line Item | 2025 | 2026 | 2027 | 2028 | Assumptions |
|-----------|------|------|------|------|-------------|

### 7.2 Capital and Debt Management
- Current capital structure (equity vs. debt)
- Fundraising needs and timeline
- Financial sustainability strategies
- Debt management: terms, covenants, refinancing schedule
- Investor relations approach (if applicable)

### 7.3 Budgeting and Expense Control
- Annual budget process and timeline
- Expense forecasting methodology
- Cost control measures and efficiency targets
- Budget allocation by driver/department

| Department/Driver | Budget 2025 | Budget 2026 | Budget 2027 | Budget 2028 |
|-------------------|------------|------------|------------|------------|
| Portfolio growth  |            |            |            |            |
| Marketing         |            |            |            |            |
| Organization/HR   |            |            |            |            |
| Operations/IT     |            |            |            |            |
| Reputation/Legal  |            |            |            |            |

### 7.4 Risk Management and Compliance
- Financial risk register: market, credit, liquidity, operational
- Compliance and regulatory financial requirements
- Insurance coverage review
- Cybersecurity financial exposure
- Risk mitigation strategies with costs

### 7.5 Performance Management and KPIs
- KPI framework linked to each of the 6 drivers
- KPI owners and accountability
- Reporting cadence: daily, weekly, monthly, quarterly
- Dashboard design: red/amber/green thresholds per KPI

| KPI | Driver | Dimension | Owner | Target 2025 | Target 2026 | RAG Threshold |
|-----|--------|-----------|-------|------------|------------|---------------|

### 7.6 Tax Planning
- Tax structure optimization (within legal boundaries)
- Transfer pricing (if multi-entity)
- Tax incentive utilization (R&D credits, investment deductions)
- Tax compliance calendar

### 7.7 Business Performance Tracking
- Profit margins and ROI by business line
- Customer satisfaction metrics linked to revenue
- Employee engagement metrics linked to productivity
- Operational effectiveness metrics linked to cost


## Cross-Driver Alignment (MANDATORY — MOST CRITICAL)

Financial is the INTEGRATION DRIVER. It MUST align with ALL others:
- PORTFOLIO: Revenue projections must match growth targets exactly
- MARKETING: Marketing spend must match approved budgets
- ORGANIZATIONAL: People costs must match HR headcount plan
- OPERATIONAL: IT/capex investments must match operational roadmap
- REPUTATION: Legal, compliance, brand costs must be fully budgeted

SPECIFIC CHECKS Claude must perform:
1. Sum of all driver budgets <= Total approved budget
2. Revenue projections supported by Marketing customer/channel targets
3. Headcount cost matches Organizational headcount plan
4. Capex matches Operational IT roadmap investments
5. Growth targets match Portfolio business line projections
6. Business Model dimension is fully reflected in P&L structure

If ANY check fails, Claude MUST stop and flag the misalignment.


## Quality Checklist
- [ ] P&L covers 3+ years with stated assumptions
- [ ] Cash flow has monthly detail for Year 1
- [ ] At least 3 scenarios (base/up/down) are modeled
- [ ] Every KPI has a named owner
- [ ] Budget broken down by driver, not just department
- [ ] Risk register has at least 5 risks with quantified exposure
- [ ] All other 5 drivers' costs are reflected in the budget
- [ ] Business Model dimension from Strategic Direction is fully mapped


## Edge Cases
- Startup (pre-revenue): Focus on burn rate, runway, funding milestones.
  P&L shows path to break-even. Revenue projections are hypothesis-based.
- Non-profit: Replace profit metrics with impact-per-dollar metrics.
  Budget focuses on program vs. overhead ratios.
- Holding company: Consolidation view plus per-entity breakdown.
  Intercompany transactions and eliminations must be shown.
