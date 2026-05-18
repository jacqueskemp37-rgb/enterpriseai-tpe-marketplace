---
name: tpe:driver-audit
description: >
  Assess one or all six drivers against TPE quality standards.
  Scores each driver on completeness, consistency, and comprehensiveness.
trigger: /tpe:driver-audit
output: Gap analysis report with scores and recommendations
skills_loaded: [tpe-framework, selected driver skill(s)]
estimated_time: 15-30 minutes per driver
---

# /tpe:driver-audit — Audit Driver Plans Against TPE Standards

## What This Command Does
Takes existing plans or documents and evaluates them against the TPE
quality checklist for each driver. Produces a scored gap analysis with
specific recommendations for improvement.

## Input Required
- Which driver(s) to audit: one specific driver or all six
- Existing plan documents (upload or share via Google Drive)
- Company context (if not already established in session)

## Execution Workflow

### Step 1: Load Documents
- Read all uploaded/shared documents
- Identify which driver(s) each document covers
- Flag any drivers with no corresponding document

### Step 2: Score Each Driver
For each driver being audited, evaluate against its quality checklist:

SCORING SYSTEM (per checklist item):
- GREEN (3): Fully addressed with measurable targets and evidence
- AMBER (2): Partially addressed, missing specificity or targets
- RED (1): Not addressed or only mentioned superficially
- MISSING (0): Completely absent

Calculate:
- Score per driver: sum of checklist scores / maximum possible score
- 3C Rating per driver:
  - Completeness: are all required sections present?
  - Consistency: does it align with other drivers?
  - Comprehensiveness: is it deep enough to act on?

### Step 3: Strategic Direction Traceability
- Check if each driver traces back to its assigned dimensions
- Flag drivers that claim to serve a dimension but lack substance

### Step 4: Cross-Driver Alignment Check
- If auditing multiple drivers: check alignment rules between them
- Flag contradictions (e.g., marketing targets 50K customers but
  operations supports only 30K)

### Step 5: Produce Gap Analysis Report

Format:
```
ENTERPRISEAI TPE DRIVER AUDIT REPORT
Company: [name]
Date: [date]
Audited: [which drivers]

EXECUTIVE SUMMARY
Overall Score: [X]% TPE Compliance
Drivers at risk: [list]
Top 3 gaps: [list]

DRIVER SCORECARD
| Driver | Score | Completeness | Consistency | Comprehensiveness | Rating |
|--------|-------|-------------|-------------|-------------------|--------|

PER-DRIVER DETAIL
[For each driver:]
- Overall score and RAG rating
- Checklist items scored individually
- Specific gaps identified with quotes from document
- Recommendations ranked by impact
- Cross-driver alignment issues

STRATEGIC DIRECTION TRACEABILITY
| Dimension | Covered By | Quality | Gaps |
|-----------|-----------|---------|------|

PRIORITY ACTIONS
1. [Highest impact gap] — Owner: [suggested] — Timeline: [suggested]
2. ...
3. ...
```

## Quality Standards
- Every checklist item must be scored, not skipped
- Recommendations must be specific and actionable, not generic
- Cross-references to actual content in the documents
- Priority actions must be ranked by impact, not just listed
