---
name: comparative-research
description: >
  Use this skill whenever the user asks to evaluate, compare, or recommend between real-world options — devices, tools, vendors, services, platforms, or any category where the right choice depends on market data, specs, and target-user fit. Trigger on phrases like "recommend a...", "which X should I buy/use/choose", "compare these options", "find the best...", "top N choices for...", "compare these for me...", "comparative research for...", or any time the user needs a structured, evidence-backed selection decision. Use this skill even if the user's question seems quick or casual — e.g. "which phone should I get?" — because proper candidate selection requires a structured process to avoid bias. This skill is critical any time data availability might otherwise skew the recommendation toward well-documented options over better-fit options.
---
 
# Comparative Market Research & Recommendation
 
A structured, bias-resistant process for evaluating options and producing a sourced, auditable recommendation.
 
> **Core failure mode this skill prevents:** Recommending well-documented options over better-fit options because their spec sheets are easier to research. This skill forces primary criterion supremacy at every phase.
 
---
 
## Phase 1: Requirements Extraction
 
Before any research, extract and confirm all of the following. Do NOT proceed until the **primary criterion** is unambiguous — everything else flows from it.
 
| # | What to capture | Why it matters |
|---|---|---|
| 1 | **Primary selection criterion** — the single most important factor | Governs candidate selection in Phase 3. Cannot be overridden by data convenience. |
| 2 | **Hard constraints** — pass/fail requirements every candidate must meet | Eliminates non-starters early |
| 3 | **Target user profile** — who will actually use this, their behavior, geography, income, buying channels | Purchasing context often matters as much as specs |
| 4 | **Budget / price range** — explicit bounds | Scopes the candidate pool |
| 5 | **Quantity and purpose** — how many, and what role each serves (e.g. "worst-case stress test" vs. "realistic floor") | Determines how many winners to name and what roles they fill |
| 6 | **What does NOT matter** — explicit noise elimination | Prevents irrelevant criteria from cluttering the analysis |
 
---
 
## Phase 2: Parallel Research
 
Run up to 3 research threads in parallel, each with a distinct focus:
 
| Thread | Focus | Sources | Output |
|---|---|---|---|
| **Market** | Market share, brand rankings, sales volumes, distribution channels, demographic penetration | Counterpoint, IDC, Canalys, Statista, GSMA | Forced-rank of all candidates by the PRIMARY criterion |
| **Specs** | Technical specifications vs. hard constraints | GSMArena, official manufacturer pages, 91mobiles, Smartprix, product pages | Pass/fail table for every candidate |
| **User-fit** | Target user behavior — how they buy, what they use, channel preferences, price sensitivity | Survey data, industry reports, news | Demographic alignment score per candidate |
 
### Research rules
 
- **Every claim must have a source URL.** No unsourced statistics, ever.
- **Missing data is declared, not fabricated.** Say: "No survey exists mapping X to Y — using Z as proxy. This is an assumption."
- **Distinguish installed base from new sales.** Installed base = what users have now. New sales = what they're buying next. Report both when available.
- **Capture distribution channel data.** For physical products, offline/online split and retail footprint are often more predictive than headline market share.
 
---
 
## Phase 3: Candidate Selection
 
> ⚠️ This is where most recommendation processes fail. Follow the sequence exactly.
 
### Step 3a — Forced-rank by primary criterion
 
Using ONLY the market/user-fit data from Phase 2, rank all potential candidates by the primary criterion. Write this ranking down **before** looking at spec completeness.
 
### Step 3b — Filter by hard constraints
 
Remove candidates that fail pass/fail requirements. Document each elimination with a specific reason — this goes in the **Eliminated Candidates** section of the report.
 
### Step 3c — Treat data gaps as risks, not disqualifiers
 
For high-ranking candidates with incomplete spec data:
- ✅ **Include them in the shortlist**
- ⚠️ **Flag each gap** with a specific verification action (e.g. "verify camera FOV post-purchase by recording a known-width object at 60cm")
- ❌ **Never drop** a high-ranking candidate because it's harder to research than a lower-ranking alternative
 
**Anti-pattern to avoid:**
> "Option B has all specs on GSMArena, so I'll include it. Option A is missing FOV data, so I'll mention it as a backup."
>
> This is wrong. If Option A ranks higher on the primary criterion, it goes in the top N with the FOV gap flagged. Option B's spec-sheet completeness is irrelevant to its ranking.
 
### Step 3d — Diversity check
 
Before finalizing:
- Does any single brand/category occupy more than one slot while scoring poorly on the primary criterion? Remove the weaker entry; replace with the next-best from a different brand/category.
- Do the top N collectively cover the user's stated purposes (e.g. worst-case AND realistic floor)?
 
---
 
## Phase 4: Evaluation Criteria Definition
 
Define **10 or fewer** criteria. For each:
 
- **What:** One-sentence definition
- **Why:** Why this criterion matters for *this specific decision*, tied to a concrete user requirement
- **Evidence:** Source data supporting the inclusion of this criterion
 
**Criteria ordering:**
1. Primary criterion first
2. Hard pass/fail constraints next
3. Differentiating factors last
 
**Anti-patterns to avoid:**
- Criteria that every candidate passes equally — these add noise without discrimination
- "Data availability" or "spec confidence" as a criterion — this directly biases toward well-documented options
 
---
 
## Phase 5: Per-Candidate Analysis
 
For each candidate in the top N:
 
**1. Spec table** — assess every criterion with a status icon:
- ✅ **PASS / CONFIRMED**
- ⚠️ **LIKELY PASS** — unconfirmed; state what's missing and how to verify
- ❓ **UNKNOWN** — state what's missing
- ❌ **FAIL**
 
**2. Sources** — URLs for every claim
 
**3. Strengths** — 2–4 bullets, evidence-grounded
 
**4. Weaknesses** — 2–4 bullets, evidence-grounded. Never omit.
 
---
 
## Phase 6: Comparison Matrix
 
Single table, all candidates side by side, all criteria as rows, status icons throughout. Must be scannable in 30 seconds.
 
---
 
## Phase 7: Recommendation
 
1. **Winner(s)** — one per role the user defined
2. **Why each winner wins** — 4–6 bullets, tied directly to criteria and evidence, leading with the primary criterion
3. **Why runners-up lost** — specific and evidence-based (e.g. "Samsung has minimal sub-₹10K market share per IDC, and vibration motor is unconfirmed")
4. **Purchase summary** — model / price / where to buy / purpose, one table
5. **Verification checklist** — post-purchase steps to confirm any unverified specs
 
---
 
## Phase 8: Assumptions & Gaps
 
Surface every assumption and data gap as a scannable table. Never bury them in prose.
 
| # | Item | Status |
|---|---|---|
| 1 | Description of assumption or gap | **Assumption** / **Risk — verify post-purchase** / **Known limitation** / **Trend to monitor** |
 
---
 
## Phase 9: Sources Index
 
Table mapping every source URL to what it was used for. Every claim in the report must be auditable from this index.
 
---
 
## Output Format
 
Save the report as a Markdown file with a descriptive filename (e.g. `phone-recommendation-2024.md`).
 
```
# [Title]
_Generated: YYYY-MM-DD_
---
## Context
## Evaluation Criteria (C1–C10)
## Eliminated Candidates
## Top N Candidates
## Comparison Matrix
## Recommendation
## Verification Checklist
## Assumptions & Gaps
## Sources Index
```
 
---
 
## Guardrails
 
| # | Rule |
|---|---|
| 1 | **Primary criterion supremacy.** Data availability, research convenience, and spec-sheet completeness are never selection criteria — they are verification risks to flag. |
| 2 | **No unsourced claims.** Every stat, market share figure, and spec needs a source URL. If unavailable: "no data available." Never fabricate. |
| 3 | **Assumptions are first-class outputs.** Every inference, proxy, and gap gets surfaced in the Assumptions table with the phrase "This is an assumption." |
| 4 | **Diversity over convenience.** Prefer covering different brands/categories over doubling up on whichever option has more available data. |
| 5 | **Installed base ≠ new sales.** Always distinguish and report both when available. |
| 6 | **Distribution channels matter.** How and where the target user purchases is as important as what they purchase. |
| 7 | **Confirm roles before recommending.** If multiple items are needed (e.g. worst-case + realistic floor), confirm which role each pick serves — don't just assert it. |