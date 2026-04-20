<!--
=== ARCHIVAL METADATA ===
Source Repository: antigravity-config (private)
Source Commit:     ea86a319d7c9effb5b7d3ffb566386687b97ff2f
Source Date:       2026-01-16 09:28:00 +0800
Source Path:       workflows/product-launch-audit.md
Archived:          2026-04-20
Status:            Pre-A1 historical evidence
Significance:      First multi-expert workflow — orchestrates 5 specialized
                   role prompts in sequence (Architect → PM → Analyst →
                   Strategist → VC). Precursor to A1's Trinity Council model.
==========================
-->

---
description: Run a comprehensive 5-stage product audit involving Architect, PM, Analyst, MVP Strategist, and Investor personas.
---

# Product Launch Audit Workflow

This workflow orchestrates a deep-dive audit of your product, simulating a professional advisory board.

## Prerequisites
- Ensure `.agent/skills/product-audit-experts/` exists.
- The agent should have read access to the entire codebase.

## Workflow Steps

### 1. 🏗️ Technical Health Check (Architect)
> **Goal**: Assess technical debt, security, and compliance.

1. Read the expert guide: `view_file .agent/skills/product-audit-experts/architect-health-check.md`
2. **Action**: Scan the codebase, `package.json`, and existing documentation.
3. **Execute**: Create a report at `docs/01_ARCHITECTURAL_HEALTH_CHECK.md` following the guide's framework.

### 2. 🎨 Product Gap Analysis (Product Manager)
> **Goal**: Identify UX gaps and feature holes.

1. Read the expert guide: `view_file .agent/skills/product-audit-experts/pm-gap-analysis.md`
2. **Input**: Read the Architect's report: `view_file docs/01_ARCHITECTURAL_HEALTH_CHECK.md` and current PRD/docs.
3. **Execute**: Create a report at `docs/02_PRODUCT_GAP_ANALYSIS.md`.

### 3. 📊 Spec & Pitch Creation (Analyst)
> **Goal**: Document the "What" and "Why".

1. Read the expert guide: `view_file .agent/skills/product-audit-experts/analyst-spec-writer.md`
2. **Input**: Read both previous reports (`docs/01...`, `docs/02...`).
3. **Execute**: Create the master document at `docs/03_PRODUCT_SPEC_AND_PITCH.md`.

### 4. 🧭 MVP Definition (Strategist)
> **Goal**: Define the "How" and "When".

1. Read the expert guide: `view_file .agent/skills/product-audit-experts/mvp-strategist.md`
2. **Input**: Read the Spec: `view_file docs/03_PRODUCT_SPEC_AND_PITCH.md`.
3. **Execute**: Create the roadmap at `docs/04_MVP_AND_ROADMAP.md`.

### 5. 🦈 Investment Analysis (VC Investor)
> **Goal**: The Final Verdict.

1. Read the expert guide: `view_file .agent/skills/product-audit-experts/vc-investor.md`
2. **Input**: Read ALL previous documents.
3. **Execute**: Create the investment memo at `docs/05_INVESTOR_MARKET_ANALYSIS.md`.

## Final Step
- Notify the user that the full audit package is ready in the `docs/` folder.
