---
name: tpe-framework
description: >
  Core EnterpriseAI TPE (Think-Plan-Execute) Business Planning Framework.
  The Complete, Consistent and Comprehensive (3C) methodology for whole-firm
  business planning. This master skill orchestrates all six driver skills.
version: 1.0.0
author: EnterpriseAI
tags: [business-planning, strategy, management, tpe, enterprise]
---

# EnterpriseAI TPE Framework — Core Skill

## What Is TPE?

TPE (Think-Plan-Execute) is an academically validated management framework
(Routledge, HBR/Ivey) that creates a living, dynamic business plan covering
the entire firm — not just individual departments.

The 3C Principle:
- Complete: Every dimension of the business — no blind spots
- Consistent: All plans align with each other and with overall strategy
- Comprehensive: Deep enough to act on, broad enough to be strategic


## TPE Structure: Three Layers


### ==========================================================
### LAYER 1: STRATEGIC CONTEXT (WHAT)
### ==========================================================

Define where the organization is and where it wants to go.

#### 1A. Foundational Context

1. MISSION AND VISION
   - Define long-term mission and vision aligned with group/corporate objectives
   - Mission must be specific, measurable, and time-bound — not generic
   - Vision must paint a compelling picture of the desired future state
   - POOR: "Be the best company in our industry."
   - GOOD: "Become the leading provider of integrated financial services
     for European SMEs, achieving 15% market share in Benelux by 2028."

2. GROWTH STRATEGY
   - Organic growth paths (expand existing business)
   - Inorganic growth (M&A, investments)
   - Partnerships and alliances
   - Fixing or exiting unprofitable business units

3. COMPETITIVE ANALYSIS (SWOT)
   - Strengths: at least 3, with evidence
   - Weaknesses: at least 3, with honest assessment
   - Opportunities: at least 3, with market data
   - Threats: at least 3, with risk quantification
   - Market positioning and key differentiators vs. named competitors

4. INDUSTRY OVERVIEW
   - Key trends shaping the industry
   - Major challenges the industry faces
   - Opportunities emerging from market shifts
   - Regulatory changes affecting the industry
   - Must reference current data and sources


#### 1B. Strategic Direction — The Six Dimensions

These six questions define the STRATEGIC PLAYING FIELD. Every business plan
must answer all six explicitly. Together they form the bridge between the
strategic context (where are we) and the execution plans (how do we get there).

DIMENSION 1: LINE OF BUSINESS
   - Which business lines does the company operate in today?
   - Which business lines should it enter, grow, or exit?
   - How do these lines relate to each other (synergies, shared resources)?
   - What is the strategic role of each line (cash cow, growth engine,
     emerging bet, legacy)?
   → Links to: Portfolio Driver

DIMENSION 2: PRODUCTS AND SERVICES
   - What is the current product/service portfolio?
   - What new products/services are planned (2025-2028)?
   - How are products/services differentiated from competitors?
   - What is the innovation pipeline and R&D investment?
   - Which products/services are at end-of-life?
   → Links to: Portfolio Driver + Marketing Driver

DIMENSION 3: DISTRIBUTION CHANNELS
   - Through which channels does the company reach customers today?
   - B2C, B2B, online, retail, wholesale, partners, agents, API?
   - What is the performance of each channel (revenue, cost, satisfaction)?
   - Which channels should be expanded, optimized, or retired?
   - What is the digital vs. physical channel strategy?
   → Links to: Marketing Driver + Operational Driver

DIMENSION 4: CUSTOMER SEGMENTS
   - Who are the target customer groups? Define with specificity.
   - NOT "SMEs" but "manufacturing SMEs, 50-250 employees, Benelux region"
   - What are the needs, pain points, and buying behaviors per segment?
   - Which segments are primary, secondary, aspirational?
   - What is the current and target market share per segment?
   → Links to: Marketing Driver

DIMENSION 5: REACH / GEOGRAPHY
   - What is the current geographic footprint?
   - What is the expansion roadmap (which countries/regions, when)?
   - What are the regulatory, cultural, and operational barriers per market?
   - Is growth domestic-first or international-first?
   - What is the localization strategy per market?
   → Links to: Portfolio Driver + Marketing Driver + Operational Driver

DIMENSION 6: BUSINESS MODEL
   - How does the company make money? (subscription, transaction, licensing,
     freemium, advertising, consulting, hybrid?)
   - What is the revenue model per product/segment/channel?
   - What is the cost structure (fixed vs. variable)?
   - What is the unit economics (CAC, LTV, payback period)?
   - Is the business model scalable? What limits scale?
   → Links to: Financial Driver + Portfolio Driver

CRITICAL RULE: All six dimensions must be answered BEFORE moving to the
Execution Plans. If any dimension is unclear, Claude must ask the user
for clarification. The six dimensions act as the "contract" between
strategy and execution — every Execution Plan must trace back to at
least one dimension.

Data table format for Strategic Direction summary:
| Dimension | Current State | Target State 2028 | Key Actions | Links To |
|-----------|--------------|-------------------|-------------|----------|
| Line of Business | | | | Portfolio |
| Products/Services | | | | Portfolio + Marketing |
| Distribution Channels | | | | Marketing + Operations |
| Customer Segments | | | | Marketing |
| Reach/Geography | | | | Portfolio + Marketing + Operations |
| Business Model | | | | Financial + Portfolio |


### ==========================================================
### LAYER 2: EXECUTION PLANS (HOW) — Six Drivers
### ==========================================================

Six integrated driver plans that translate strategy into action.

Each driver plan MUST contain:
- Objectives with measurable targets per year (2025-2028)
- Key actions with owners and timelines
- Risk identification with mitigation strategies
- Cross-references to at least 2 other driver plans
- Explicit links back to which Strategic Direction dimensions it serves

The six drivers:

Driver 1: PORTFOLIO PLAN → skills/portfolio-driver.md
  Focus: Business lines, M&A, partnerships, growth paths
  Serves dimensions: Line of Business, Products/Services, Reach/Geography

Driver 2: MARKETING PLAN → skills/marketing-driver.md
  Focus: Customer segments, products/services, distribution channels
  Serves dimensions: Customer Segments, Products/Services, Distribution Channels, Reach/Geography

Driver 3: ORGANIZATIONAL PLAN → skills/organizational-driver.md
  Focus: Org structure, HR, culture, governance, D&I
  Serves dimensions: all (people enable everything)

Driver 4: OPERATIONAL PLAN → skills/operational-driver.md
  Focus: Processes, IT, customer service, automation
  Serves dimensions: Distribution Channels, Reach/Geography, Business Model

Driver 5: REPUTATIONAL PLAN → skills/reputation-driver.md
  Focus: Brand, external/internal communications, legal, compliance
  Serves dimensions: Customer Segments, Reach/Geography

Driver 6: FINANCIAL PLAN → skills/financial-driver.md
  Focus: Budgets, KPIs, risk management, performance tracking
  Serves dimensions: Business Model (primary), all others (integration)


### ==========================================================
### LAYER 3: PERFORMANCE (RESULT)
### ==========================================================

Define what success looks like and how it is measured.

Quantitative objectives:
- Income/Cost ratios
- Cash flow targets
- EBITDA margins
- Return on Investment (ROI)
- Revenue growth targets per year

Qualitative objectives:
- Market share leadership position
- Customer satisfaction scores
- Employee satisfaction and retention
- Complexity reduction metrics

Performance tracking rules:
- Each KPI must have an owner
- Review cadence: weekly (operational), monthly (tactical), quarterly (strategic)
- Dashboard: Excel with red/amber/green conditional formatting per KPI
- Every KPI must trace back to at least one driver AND one strategic dimension


## Workflow Instructions for Claude

### /tpe:full-plan workflow:
1. Gather Foundational Context (mission, vision, SWOT, industry)
2. Work through all Six Dimensions of Strategic Direction
3. Confirm Strategic Direction summary table with user before proceeding
4. Work through each 6 drivers (load each driver skill sequentially)
5. Run alignment check across all six plans
6. Generate Performance layer with KPIs per driver
7. Output: Word doc + Excel dashboard + PPTX executive summary

### /tpe:quick-scan workflow:
1. Ask for company, industry, planning maturity
2. Assess which of the 6 dimensions and 6 drivers are covered
3. Identify gaps and misalignments
4. Output: 1-page exec summary with RAG per dimension and per driver

### /tpe:alignment-check workflow:
1. Load all existing driver plans
2. Cross-reference targets, timelines, assumptions
3. Verify each driver traces to strategic dimensions
4. Flag inconsistencies with specific examples
5. Output: Alignment matrix

### /tpe:driver-audit workflow:
1. Select one or all six drivers
2. Assess against quality checklist in each driver skill
3. Verify linkage to Strategic Direction dimensions
4. Score on completeness, consistency, comprehensiveness (3C)
5. Output: Gap analysis report


## Cross-Driver Alignment Rules (MUST VERIFY)

1. Portfolio <-> Financial: Revenue projections match growth targets
2. Marketing <-> Portfolio: Customer segments map to product lines
3. Organizational <-> Operational: Headcount supports capacity needs
4. Reputation <-> Marketing: Brand matches marketing messaging
5. Financial <-> Organizational: Comp budgets match HR plans
6. Operational <-> Financial: IT investments in capex budgets

ADDITIONALLY — Strategic Direction traceability:
7. Every driver plan must reference which of the 6 dimensions it serves
8. Every dimension must be served by at least one driver plan
9. If a dimension has no driver coverage, Claude MUST flag the gap

On misalignment: Flag, explain conflict, suggest resolution, ask user.


## Formatting Standards

- Word: Professional layout, TOC, numbered sections, EnterpriseAI branding
- Excel: One tab per driver, summary dashboard tab, conditional formatting
- PPTX: Max 15 slides, one message per slide, executive-friendly
- Tables: Category | Specifics | 2025 | 2026 | 2027 | 2028 | Comments
- Strategic Direction: Always presented as the 6-dimension summary table


## Decision Framework

- Company has NO business plan → /tpe:full-plan (start with dimensions)
- Company has departmental plans → /tpe:alignment-check then fill gaps
- Company wants to validate → /tpe:quick-scan + /tpe:driver-audit
- Board/investor prep → /tpe:full-plan with PPTX focus

Escalate to human expertise when:
- Highly regulated industries needing legal compliance review
- M&A scenarios requiring due diligence
- Restructuring involving labor law
