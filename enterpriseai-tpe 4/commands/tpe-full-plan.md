---
name: tpe:full-plan
description: >
  Guided creation of a complete 3C business plan across all drivers.
  The flagship EnterpriseAI command that produces a unified, living
  business plan for the entire organization.
trigger: /tpe:full-plan
output: Word document + Excel KPI dashboard + PowerPoint executive summary
skills_loaded: [tpe-framework, portfolio-driver, marketing-driver, organizational-driver, operational-driver, reputation-driver, financial-driver]
estimated_time: 45-90 minutes (interactive)
---

# /tpe:full-plan — Create Complete Business Plan

## What This Command Does
Creates a comprehensive business plan following the full TPE methodology:
Strategic Context → Six Dimensions → Six Driver Plans → Performance Layer.
Produces three professional deliverables.

## Input Required From User
Claude must gather the following before starting. Ask conversationally,
not as a form. Group related questions together.

### Phase 1: Company Context (ask first)
- Company name and legal entity
- Industry and sub-industry
- Company size (revenue, headcount, locations)
- Current stage (startup, growth, mature, turnaround)
- Parent company or group affiliation (if any)
- Who is this plan for? (board, investors, internal alignment, new venture)

### Phase 2: Strategic Context (ask after Phase 1)
- What is the current mission and vision?
- What are the top 3 strategic priorities for the next 3 years?
- What are the biggest competitive threats?
- What recent changes (market, regulatory, internal) are driving this plan?

### Phase 3: Existing Materials (ask after Phase 2)
- Does the company have existing plans or documents to build on?
- If yes: ask user to share files (Claude reads via Google Drive or upload)
- Which of the 6 drivers already have plans vs. need to be built from scratch?

## Execution Workflow

### Step 1: Build Strategic Context
Load skill: tpe-framework.md
- Document mission, vision, growth strategy, SWOT, industry overview
- Present back to user for confirmation before proceeding

### Step 2: Define Six Dimensions of Strategic Direction
Load skill: tpe-framework.md (section 1B)
- Work through each dimension with the user:
  1. Line of Business — which lines, grow/maintain/exit?
  2. Products/Services — current and planned portfolio?
  3. Distribution Channels — how do you reach customers?
  4. Customer Segments — who exactly do you serve?
  5. Reach/Geography — where do you operate and expand to?
  6. Business Model — how do you make money?
- Produce the Strategic Direction summary table
- GET USER CONFIRMATION before proceeding to drivers

### Step 3: Portfolio Plan
Load skill: portfolio-driver.md
- Work through sections 2.1-2.5
- Cross-reference with Strategic Direction dimensions
- Document in standard TPE table format

### Step 4: Marketing Plan
Load skill: marketing-driver.md
- Work through sections 3.1-3.5
- Ensure customer segments match dimension 4
- Ensure channels match dimension 3
- Ensure geography matches dimension 5

### Step 5: Organizational Plan
Load skill: organizational-driver.md
- Work through sections 4.1-4.5
- Ensure headcount supports other driver plans

### Step 6: Operational Plan
Load skill: operational-driver.md
- Work through sections 5.1-5.4
- Ensure IT/process capacity supports growth plans

### Step 7: Reputational Plan
Load skill: reputation-driver.md
- Work through sections 6.1-6.5
- Ensure brand aligns with marketing messaging

### Step 8: Financial Plan
Load skill: financial-driver.md
- Work through sections 7.1-7.7
- THIS IS THE INTEGRATION CHECK: verify all numbers align
- Run the 6 specific alignment checks from the skill
- Flag any misalignments to user

### Step 9: Performance Layer
Load skill: tpe-framework.md (Layer 3)
- Define quantitative and qualitative objectives
- Assign KPI owners
- Set review cadence
- Build KPI dashboard structure

### Step 10: Alignment Verification
- Run full cross-driver alignment check (6 rules from tpe-framework)
- Run Strategic Direction traceability check (every dimension covered)
- Present alignment matrix to user
- Resolve any conflicts with user input

### Step 11: Produce Deliverables
1. WORD DOCUMENT: Full business plan with all sections, TOC, tables
   - Professional formatting with EnterpriseAI branding
   - Numbered sections following TPE structure
   - All data tables populated
2. EXCEL DASHBOARD: KPI tracking workbook
   - Tab 1: Summary dashboard with RAG status per driver
   - Tabs 2-7: One tab per driver with detailed KPIs
   - Tab 8: Strategic Direction dimension tracker
   - Conditional formatting: green/amber/red thresholds
3. POWERPOINT: Executive summary (max 15 slides)
   - Slide 1: Title + company overview
   - Slide 2: Mission, vision, strategic priorities
   - Slide 3: Six Dimensions summary table
   - Slides 4-9: One slide per driver (key highlights only)
   - Slide 10: Alignment matrix visualization
   - Slide 11: Financial summary (P&L, key metrics)
   - Slide 12: KPI dashboard overview
   - Slide 13: Risk summary
   - Slide 14: Implementation roadmap
   - Slide 15: Next steps and review schedule

## Quality Standards
- Every section must have data in the year columns (2025-2028)
- Every driver must cross-reference at least 2 other drivers
- Every Strategic Direction dimension must be traced to at least 1 driver
- Financial projections must have stated assumptions
- At least 3 scenarios in financial plan
- All KPIs must have named owners

## Error Handling
- If user cannot provide info for a section: mark as "TBD — requires input
  from [suggested role]" and continue. Do not skip the section.
- If alignment check finds conflicts: present them clearly, suggest
  resolution options, and ask user to decide before finalizing.
- If data is insufficient for financial projections: state assumptions
  explicitly and mark projections as "indicative — requires validation."
