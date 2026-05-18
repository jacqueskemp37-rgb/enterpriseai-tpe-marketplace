---
name: parallel-driver-analysis
description: >
  Sub-agent that enables simultaneous assessment of all six drivers.
  Used when speed is critical (e.g., board prep, due diligence) to
  analyze multiple drivers in parallel rather than sequentially.
version: 1.0.0
author: EnterpriseAI
---

# Parallel Driver Analysis Sub-Agent

## Purpose
When a full sequential analysis of all 6 drivers would take too long,
this sub-agent enables Claude to analyze multiple drivers simultaneously.
Each driver analysis runs as an independent thread, then results are
merged and cross-checked for alignment.

## When to Use
- /tpe:full-plan with time pressure (need results in one session)
- /tpe:driver-audit of all 6 drivers simultaneously
- /tpe:alignment-check with large document sets
- Due diligence scenarios requiring rapid assessment

## How It Works

### Phase 1: PARALLEL ANALYSIS
Spawn 6 parallel analysis threads, one per driver:

Thread 1 — Portfolio Analysis:
  Load: portfolio-driver.md
  Task: Analyze all portfolio-related content from input documents
  Output: Structured portfolio driver assessment

Thread 2 — Marketing Analysis:
  Load: marketing-driver.md
  Task: Analyze all marketing-related content
  Output: Structured marketing driver assessment

Thread 3 — Organizational Analysis:
  Load: organizational-driver.md
  Task: Analyze all organization-related content
  Output: Structured organizational driver assessment

Thread 4 — Operational Analysis:
  Load: operational-driver.md
  Task: Analyze all operations-related content
  Output: Structured operational driver assessment

Thread 5 — Reputational Analysis:
  Load: reputation-driver.md
  Task: Analyze all reputation-related content
  Output: Structured reputational driver assessment

Thread 6 — Financial Analysis:
  Load: financial-driver.md
  Task: Analyze all financial content
  Output: Structured financial driver assessment

### Phase 2: MERGE AND CROSS-CHECK
Once all 6 threads complete:
1. Merge results into unified TPE structure
2. Run all 6 alignment rules from tpe-framework.md
3. Run Strategic Direction traceability check
4. Flag conflicts between parallel assessments
5. Produce consolidated report

### Phase 3: HUMAN VALIDATION
Present merged results to user:
- Highlight any areas where parallel threads produced conflicting
  interpretations of the same source data
- Ask user to resolve ambiguities
- Finalize consolidated assessment

## Performance Target
- Sequential analysis of 6 drivers: 60-90 minutes
- Parallel analysis with sub-agent: 20-30 minutes
- Quality should be equivalent; speed is the advantage

## Limitations
- Parallel threads cannot communicate with each other during analysis
- Cross-driver insights may be missed during parallel phase
  (caught during merge phase)
- Complex interdependencies are better handled sequentially
- User should validate merged results more carefully than sequential results

## Fallback
If parallel execution is not available in the current Cowork environment:
- Fall back to sequential analysis
- Prioritize drivers by user's stated urgency
- Offer to do 2-3 critical drivers first, remaining drivers in follow-up
