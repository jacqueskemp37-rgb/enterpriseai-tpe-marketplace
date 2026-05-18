---
name: enterpriseai-tpe
description: >
  EnterpriseAI TPE (Think-Plan-Execute) — the Complete, Consistent & Comprehensive (3C)
  Business & Management Planning framework. Use this skill for ANY business planning,
  strategy, management, or organizational task. Triggers for: business plan, strategic plan,
  driver analysis, KPI dashboard, alignment check, TPE framework, business scan, full plan,
  onboarding, scheduled review, portfolio strategy, marketing plan, organizational design,
  operational planning, reputation management, financial planning, cross-driver alignment,
  connect the dots, dependency mapping, or any whole-firm planning request. This skill
  reduces complexity and opens up silos within the organization by connecting all
  departments into one integrated, living business plan.
license: EnterpriseAI
---

# EnterpriseAI TPE — Business Planning Framework

The EnterpriseAI TPE (Think-Plan-Execute) framework is the only management
methodology that combines strategic context, execution planning, and performance
management into one integrated, AI-powered system. Academically validated
(Routledge, HBR/Ivey) and applied across banking, technology, retail, and
other industries.

## Core Principle: 3C

- **Complete** — Every dimension of the business, no blind spots
- **Consistent** — All plans align with each other and with strategy
- **Comprehensive** — Deep enough to act on, broad enough to be strategic

## How to Use This Plugin

### Step 1 — Read the Core Framework
Always start by reading `skills/tpe-framework.md` to understand the 3-layer
structure (Strategic Context, Execution Plan, Performance Management) and the
6 drivers.

### Step 2 — Select the Right Command
Commands are in `commands/`. Each command maps to a specific output:

| Command file | When to use | Output |
|---|---|---|
| `tpe-onboard.md` | First-time user, new team member | Training PPTX |
| `tpe-quick-scan.md` | Rapid gap assessment | 1-page RAG summary |
| `tpe-full-plan.md` | Complete business plan | Word + Excel + PPTX |
| `tpe-driver-audit.md` | Score one or all drivers | Gap analysis report |
| `tpe-alignment-check.md` | Cross-check plans for consistency | Alignment matrix |
| `tpe-connect-the-dots.md` | Map interdependencies | Dependency map |
| `tpe-kpi-dashboard.md` | Build KPI tracker | Excel workbook |
| `tpe-scheduled-review.md` | Recurring plan review | Review agenda + dashboard |

### Step 3 — Load the Relevant Driver Skills
Driver skills are in `skills/`. Load the relevant driver(s) for context:

- `portfolio-driver.md` — Business lines, M&A, growth strategy
- `marketing-driver.md` — Customers, products, channels, go-to-market
- `organizational-driver.md` — Org structure, HR, culture, governance
- `operational-driver.md` — Processes, IT, automation, customer service
- `reputation-driver.md` — Brand, communications, legal, compliance
- `financial-driver.md` — Budgets, KPIs, risk, performance (integration driver)

### Step 4 — Use Sub-Agents for Parallel Analysis
For full-plan tasks, use `sub-agents/parallel-driver-analysis.md` to analyze
all 6 drivers simultaneously rather than sequentially.

## Quick Start (for new users)

1. Run the `/tpe:quick-scan` command to assess current planning maturity
2. Review RAG-rated results with leadership
3. Run `/tpe:full-plan` for the complete integrated business plan
4. Set up `/tpe:scheduled-review` for ongoing plan maintenance

## Available Connectors

This plugin integrates with Google Drive, Gmail, Slack, and Google Calendar
for saving deliverables, sending reviews, and scheduling recurring plan sessions.
Connect these via the Claude connector marketplace.
