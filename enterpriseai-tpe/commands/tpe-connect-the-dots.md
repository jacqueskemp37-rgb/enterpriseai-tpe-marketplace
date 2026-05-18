---
name: tpe:connect-the-dots
description: >
  Map interdependencies between existing sub-plans. Shows how decisions
  in one area ripple through the entire organization.
trigger: /tpe:connect-the-dots
output: Dependency map with impact analysis
skills_loaded: [tpe-framework]
estimated_time: 15-25 minutes
---

# /tpe:connect-the-dots — Map Plan Interdependencies

## What This Command Does
Takes existing plans and visualizes how they connect. Unlike alignment-check
(which finds conflicts), connect-the-dots maps the DEPENDENCIES — showing
what happens downstream when something changes upstream.

## Input Required
- Existing plans or documents (at least 2, ideally all available)
- Optionally: a specific change or decision to trace ("what if we acquire
  company X?" or "what if we cut IT budget by 20%?")

## Execution Workflow

### Step 1: Identify Key Decisions and Targets
From each document, extract:
- Major decisions (new product launch, market entry, M&A, restructuring)
- Quantified targets (revenue, headcount, budget, timeline)
- Assumptions that other plans depend on

### Step 2: Map Dependencies
For each key decision/target, trace:
- Which other plans DEPEND on this (downstream)
- Which other plans this DEPENDS ON (upstream)
- What is the confidence level of each dependency

Dependency types:
- HARD: One plan cannot execute without the other (e.g., hiring plan
  depends on approved budget)
- SOFT: Plans are related but can proceed independently with adjustments
- TIMING: Plans are sequence-dependent (e.g., IT system must be live
  before marketing campaign launches)

### Step 3: Impact Ripple Analysis
If user specified a "what if" scenario:
- Trace the change through all dependencies
- Quantify impact at each step
- Identify which plans need to be updated
- Flag any plans that become infeasible

### Step 4: Produce Dependency Map

Format:
```
ENTERPRISEAI TPE DEPENDENCY MAP
Company: [name]
Date: [date]

KEY DEPENDENCIES (ranked by criticality)

1. [Decision/Target] in [Driver]
   → Downstream impact on: [Driver list]
   → Depends on: [Driver list]
   → Type: HARD / SOFT / TIMING
   → If this changes: [ripple effect description]

DEPENDENCY MATRIX
| Source Driver | Target Driver | Dependency | Type | Criticality |
|-------------|--------------|-----------|------|-------------|

CRITICAL PATH
These dependencies MUST be resolved in sequence:
1. [First] → enables → [Second] → enables → [Third]

RISK CLUSTERS
Areas where multiple dependencies converge (high risk if disrupted):
- Cluster 1: [describe] — affects [n] drivers
- Cluster 2: [describe] — affects [n] drivers

WHAT-IF ANALYSIS (if requested)
Scenario: [user's scenario]
Impact chain:
  [Driver A]: [change] →
  [Driver B]: [resulting change] →
  [Driver C]: [resulting change]
Plans requiring update: [list]
Estimated effort to realign: [assessment]
```

## Value Proposition
This command makes the invisible visible. Most organizations don't realize
how interconnected their plans are until something changes and cascading
failures occur. Connect-the-dots prevents this by mapping dependencies
BEFORE problems arise.
