---
name: user-journey-creator
description: >
  Design and document bespoke, high-quality user journeys for digital products. Use this skill
  whenever the user wants to map out, critique, redesign, or create a user journey, onboarding flow,
  feature walkthrough, or any end-to-end experience within an app or product. Trigger on phrases like
  "design the user journey", "map out the onboarding", "how should the user flow work", "create a
  journey for", "user journey for [feature/persona]", "review my onboarding flow", "what's the ideal
  journey for", or any time a user wants to think through how a person moves through a product —
  from first touch to repeated value. Also trigger when the user is working on retention flows,
  activation steps, aha moments, or progressive disclosure design.
---

# User Journey Creator

A skill for designing bespoke, high-quality user journeys grounded in product craft principles.

---

## Core Philosophy

Every journey decision must be evaluated against these 11 principles. They are **non-negotiable product quality bars**, not suggestions.

### The 11 Principles

1. **Bespoke to persona** — The journey must be tailored to who the user actually is. A B2B enterprise buyer and a solo developer need radically different paths. Generic journeys fail.

2. **Minimal time to value** — The user should experience a meaningful "win" as fast as possible. Every step that doesn't accelerate value delivery is a candidate for removal.

3. **Interactive guidance** — Don't dump instructions on the user. Guide them *as they do*. Tooltips, contextual hints, inline walkthroughs — the journey teaches through doing.

4. **Predictable** — Users should always know what's happening, what happens next, and how to reverse course. Surprise is the enemy of trust.

5. **Near-zero learning curve** — If someone needs to "figure it out", the design has failed. The interface should communicate its own usage.

6. **Progressive disclosure** — Surface only what the user needs right now. Complexity is revealed as they're ready for it — never front-loaded.

7. **Repeatable value** — The journey doesn't end at activation. It must be designed so value compounds with each return visit. The loop, not the landing.

8. **Low cognitive load** — Minimize decisions per screen. Minimize reading. Minimize thinking. One screen, one job. Every extra choice is friction.

9. **Forgiving errors** — Users will make mistakes. The product must forgive gracefully: clear error states, easy undo, confirmation before destructive actions. Design for human imperfection.

10. **Satisfying task completion** — Completing an action should *feel* good. Micro-animations, success states, confirmation moments. The emotional punctuation of UX.

11. **Eliminate anxiety** — Proactively answer the questions users haven't asked yet: "Is this saving?", "Did that work?", "What does this do?", "Can I undo this?" Silence creates doubt.

---

## Workflow

### Step 1: Define the Persona & Context

Before designing anything, extract:

- **Who is the user?** (role, technical sophistication, motivation)
- **What are they trying to accomplish?** (job-to-be-done, not feature usage)
- **What's the product?** (type, stage, primary value prop)
- **What's the entry point?** (direct link, organic discovery, referred, etc.)
- **What does success look like?** (the "aha moment" — the moment they *get* the value)

Ask the user for these if not provided. Don't proceed with a generic persona.

---

### Step 2: Map the Journey

Structure the journey as a sequence of **stages**, each with:

```
Stage Name
├── User Goal (what they're trying to do)
├── Product Action (what the product does / shows)
├── Principle Check (which of the 11 principles apply here)
├── Friction Points (what could go wrong or confuse)
└── Delight Opportunity (where to exceed expectations)
```

**Standard Journey Stages** (adapt as needed):

1. **Discovery / Entry** — First encounter with the product
2. **Sign-up / Onboarding Gate** — Account creation or access
3. **First-Run Experience** — The first meaningful interaction
4. **Aha Moment** — The specific action that delivers the core value
5. **Habit Formation** — First return visit / repeated use
6. **Power Usage** — Advanced features unlocked progressively
7. **Advocacy / Expansion** — Sharing, upgrading, inviting others

Not every product has all stages. Trim to what's relevant.

---

### Step 3: Apply the 11-Principle Audit

After mapping, audit each stage against the 11 principles. For each stage, ask:

- Does this minimize time to value?
- Is there any unnecessary cognitive load?
- What happens when the user makes a mistake here?
- Is there a moment of delight we're missing?
- Are we disclosing too much, too soon?
- Does the user know what happens next?
- Have we pre-answered any anxiety-causing questions?

Flag every violation clearly. Don't paper over problems.

---

### Step 4: Output Format

Deliver the journey as a **structured document** with:

1. **Persona Summary** (2–3 sentences)
2. **Aha Moment Definition** (the north star of the journey)
3. **Journey Map** (stage-by-stage, using the format above)
4. **Principle Audit** (per-stage violations and recommendations)
5. **Priority Fixes** (top 3–5 highest-leverage improvements, ranked)
6. **Open Questions** (unresolved decisions the PM needs to make)

If asked for a visual flow, produce a clear text-based flow diagram or suggest building one.

---

## Design Heuristics (Quick Reference)

**On cognitive load:**
- One primary action per screen
- Labels over icons (unless icons are universally understood)
- Default values wherever possible
- Smart defaults beat blank states

**On anxiety elimination:**
- Auto-save with visible confirmation
- Progress indicators for multi-step flows
- Inline validation (not post-submit errors)
- Tooltips on hover for anything ambiguous
- Optimistic UI for fast-feeling interactions

**On error recovery:**
- Never dead-end the user
- Undo > confirm dialogs (when reversible)
- Confirm dialogs with plain-English consequences for destructive actions
- Empty states are onboarding opportunities, not failures

**On delight:**
- Completion animations (subtle, purposeful)
- First-success celebration (the first win deserves acknowledgment)
- Progress bars that feel satisfying to fill
- Personalization cues early ("Hi [name], here's where you left off")

**On progressive disclosure:**
- Start with the 20% of features that deliver 80% of value
- Lock advanced settings behind "Advanced" toggles
- Introduce features contextually (when the user needs them, not before)
- Tooltips and empty states are the onboarding layer — not a separate tour

---

## Anti-Patterns to Call Out

When reviewing a user's existing journey, explicitly flag these:

| Anti-Pattern | Why It Fails |
|---|---|
| Feature dump on first run | Overwhelms, causes decision paralysis |
| Required tutorial before use | High drop-off, patronizing to experienced users |
| Irreversible actions without confirm | Destroys trust permanently |
| Blank empty states | Missed opportunity to guide and activate |
| Success states that don't exist | Value delivered without acknowledgment = no emotional anchor |
| Multi-field forms upfront | Kills conversion at the top of the funnel |
| Error messages that don't explain what to do | Users abandon instead of fixing |
| Passive waiting (no loading state) | Anxiety-inducing, feels broken |
| Features hidden behind discovery | Value locked away from the user |

---

## Sample Output Skeleton

```
## User Journey: [Product Name] — [Persona Name]

### Persona
[2–3 sentence description of who this user is, what they want, and their sophistication level]

### Aha Moment
[One clear sentence: "The user feels the product's value when they first ___"]

---

### Stage 1: [Stage Name]
**User Goal:** ...
**Product Action:** ...
**Principles Applied:** [list relevant ones]
**Friction Risks:** ...
**Delight Opportunity:** ...

[Repeat for each stage]

---

### Principle Audit Summary
[Table or list of violations found per stage]

### Priority Fixes
1. [Highest leverage fix] — [Why]
2. ...

### Open Questions
- [Decision that needs to be made before implementation]
```

---

## Notes for Claude

- Always push back if the persona is vague. A journey designed for "users" is a journey designed for no one.
- If the user gives you an existing flow to review, start with the Principle Audit before suggesting anything new.
- Flag when a journey is trying to do too much too fast — this is the #1 mistake in early-stage products.
- When in doubt, recommend *removing* a step rather than adding one.
- Prioritize ruthlessly. Not every fix matters equally. Rank by user impact, not implementation effort.