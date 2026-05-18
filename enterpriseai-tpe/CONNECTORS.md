# EnterpriseAI TPE — Connectors Guide

This plugin integrates with the following Claude Cowork connectors.
Connect them via: **Claude Desktop > Settings > Connectors**

---

## Required Connectors

### Google Drive *(strongly recommended)*
**What it does:** Claude reads your existing business files and saves
all TPE outputs (Word, Excel, PPTX) directly to a structured folder.

**Setup:**
1. Go to Settings > Connectors
2. Click Google Drive > Connect
3. Sign in with your Google account
4. Claude will save outputs to: `EnterpriseAI / TPE Plans / [YourCompany]`

**Benefits:**
- All TPE plans automatically saved and versioned
- Claude reads your latest files at the start of each session
- Enables delta updates: "what changed since last time?"

---

### Gmail *(recommended)*
**What it does:** Claude can read relevant business emails for context
and send review agendas or KPI alerts when requested.

**Setup:**
1. Go to Settings > Connectors
2. Click Gmail > Connect
3. Sign in with your Google account

**Claude never sends emails automatically** — always requires your
explicit instruction.

---

### Google Calendar *(optional)*
**What it does:** Claude can schedule recurring TPE review meetings
(monthly tactical, quarterly strategic) in your calendar.

**Setup:**
1. Go to Settings > Connectors
2. Click Google Calendar > Connect

---

### Slack *(optional)*
**What it does:** Claude can post KPI updates and plan summaries to
designated team channels.

**Setup:**
1. Go to Settings > Connectors
2. Click Slack > Connect
3. Specify which channel to post updates to

---

## Data Sources — Manual Upload (No Connector Needed)

For tools without a native connector (Exact Online, Twinfield, Moneybird,
SAP, etc.), use the export method:

1. Export your data as Excel (.xlsx) or CSV
2. Upload the file directly in your Cowork session (click + button)
3. Claude will read and integrate the data automatically

**Recommended monthly exports:**
- Financial P&L and balance sheet (from your accounting software)
- Customer list with revenue per customer
- Sales pipeline (from your CRM)
- HR headcount and cost overview

---

## Privacy & Security

- Claude **never** stores your business data permanently
- Connector access uses OAuth — your password is never shared
- You can revoke connector access at any time via Settings > Connectors
- All data transmission is encrypted (TLS/SSL)
- Anthropic is SOC 2 certified and GDPR compliant

---

*EnterpriseAI TPE v1.0.4 — © 2026 EnterpriseAI*
