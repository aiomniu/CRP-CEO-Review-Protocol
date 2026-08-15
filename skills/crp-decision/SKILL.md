---
name: crp:decision
description: Multi-role structured decision protocol for strategic choices — Advisor, Devil, Historian, Budget Steward, Legal & Compliance Advisor, Founder. Use when evaluating tradeoffs, risk, resource allocation, legal/compliance exposure, or competing paths.
---

# CRP-Decision

**Part of the CRP (CEO Review Protocol) framework. Use this when evaluating strategic decisions. For content review, use `crp:content` instead.**

## Overview

CRP-Decision transforms any strategic question from "what's the right answer?" into "what do six distinct perspectives reveal about the tradeoffs?"

**Core principle:** A decision is only as good as the strongest challenge it survives.

## CRP Skills Overview

| Skill | Purpose |
|-------|---------|
| **crp:decision** (this skill) | Strategic decision review — tradeoffs, risk, resource allocation |
| **crp:content** | Content creation review — scripts, articles, video drafts |

## When to Use

**Active call:** Say "use CRP-Decision" or reference the skill when a decision involves significant tradeoffs.

**Automatic triggers:**
- Strategic direction choices (pivot, expand, narrow)
- Resource allocation (hire, invest, cut)
- Product decisions (build, buy, kill, prioritize)
- Pricing / business model changes
- Risk assessment (competitor, market, regulatory)
- Legal / regulatory / compliance exposure (data protection, AI use, platform rules, cross-border operations)
- Hiring / team structural decisions
- "Should we do X?" with non-trivial cost

**When NOT to use:**
- Simple preference questions
- Routine operational decisions (sprint tasks)
- Fact-finding or information-gathering
- Single-answer technical questions
- Content review tasks — use **crp:content** instead

## The Six Roles

```
/--- Advisor --- Devil --- Historian --- Budget Steward --- Legal & Compliance --- Founder ---\
```

| Role | Perspective | Core Question |
|------|-------------|---------------|
| **Advisor** | Builder / Opportunity constructor | "What's the best way forward?" |
| **Devil** | Skeptic / Risk challenger | "Why is this wrong or risky?" |
| **Historian** | Pattern-matcher / Trend analyst | "What does history tell us?" |
| **Budget Steward** | Cost guardian / Resource gatekeeper | "Can we afford this?" |
| **Legal & Compliance Advisor** | Compliance gatekeeper / Risk reviewer | "Can we do this legally and safely?" |
| **Founder** | Decider / Final decision maker | "What do we actually do?" |

**Advisor** — Proposes actionable solutions. Focuses on "how to make it work." Be specific about what, how, and with what resources.

**Devil** — Proactively finds flaws, risks, and blind spots. Must challenge every assumption the Advisor makes. This role is NOT optional — without Devil, the output is incomplete.

**Historian** — References analogous patterns, past outcomes, and known heuristics. Provides the "this has happened before" lens. Must cite external analogies, not restate the current situation.

**Budget Steward** — Evaluates cost feasibility from an indie developer or small team (2 people or fewer) perspective. Assesses resources needed from zero to commercialization, funding gaps, and maximum cost risk. Core question: "If we do this, can we bear the cost?"

**Legal & Compliance Advisor** — Independently reviews the decision for legal, regulatory, and data-protection risk. Assesses products, business models, features, growth tactics, data handling, AI use, and partnerships. Core question: "Can we do this legally and safely?" The review must genuinely affect the final decision — not a one-line disclaimer. Key focus areas: personal data & privacy, AI & automated decision-making, third-party AI APIs, terms & agreements, intellectual property, and platform & business compliance. Always determine which jurisdictions apply (China, EU/EEA, US, UK, Australia, Canada, etc.) rather than assuming one legal framework. Output must include a Legal Status (🟢 / 🟡 / 🟠 / 🔴) and a Recommendation (Proceed / Proceed with Conditions / Delay Pending Review / Redesign / Do Not Proceed). Seek the smallest legal viable path: prefer product design, user consent, data minimization, deletion mechanisms, and contract terms over restructuring the whole product. Never present a disclaimer as a substitute for real compliance. When facing high-risk regulatory matters, major cross-border data arrangements, or formal legal opinions, recommend confirmation by a licensed lawyer in the relevant jurisdiction.

**Founder** — Integrates all perspectives, owns the final call. Applies constraints (runway, resources, strategy) and drives to a decision. Does NOT summarize what others said — adds a constraint-based judgment.

## The Nine-Step Flow

Execute each step IN ORDER. Do NOT skip steps. Do NOT reorder.

### Step 1: Build (Advisor)
The Advisor proposes the primary approach or solution. Be specific — what, how, with what resources.

### Step 2: Challenge (Devil)
The Devil attacks the proposal. What's the flaw? What's the hidden risk? What assumption is unstated and weak? At least 3 distinct challenges required.

### Step 3: Memory (Historian)
The Historian identifies analogous situations. "This is similar to X where Y happened." Include counter-analogies if relevant.

### Step 4: Budget Review (Budget Steward)
The Budget Steward evaluates cost feasibility. Given the team size and available resources, what are the estimated costs to reach a viable outcome? What is the financial risk exposure? Is this within our means, or does the resource gap make this impractical?

### Step 5: Legal & Compliance Review (Legal & Compliance Advisor)
The Legal & Compliance Advisor performs an independent risk review. Required output:
- **Legal Status**: 🟢 Low Risk / 🟡 Manageable Risk / 🟠 Significant Risk / 🔴 High/Blocking Risk
- **Risk**: What exactly is the risk? (not a generic "legal risk" statement)
- **Why**: Why does this behavior raise legal concerns?
- **Jurisdiction**: Which countries/regions may be affected?
- **Mitigation**: What is the minimum compliance measure if we proceed? Prefer product design, data minimization, user consent, disclosure, deletion mechanisms, contract terms, privacy policy, manual review, or risk disclaimers.
- **Recommendation**: Proceed / Proceed with Conditions / Delay Pending Review / Redesign / Do Not Proceed

If structural legal issues are already apparent during Build or Challenge, the Legal & Compliance Advisor should flag them early — not wait until this step.

### Step 6: Second-order Thinking
Analyze ripple effects: "If we execute the Advisor's plan despite the Devil's concerns, what chain reactions unfold 6 months, 1 year, 3 years out?" Consider both upside and downside cascades. Also consider: do any second-order effects create new legal or compliance exposure?

### Step 7: Decision
Synthesize all perspectives into a concrete recommendation. This is NOT an average — it's a judgment call that weighs each perspective appropriately.

### Step 8: Founder Filter
Test the decision against:
- **Long-term goals:** Does this move us toward the 3-5 year vision?
- **Resource constraints:** Do we have the people, money, and time?
- **Strategic direction:** Is this consistent with our core thesis?

### Step 9: How Could We Be Wrong? (Anti-fragility Check)
Required. Answer explicitly:
- Under what conditions does this conclusion fail?
- What hidden variables could invalidate the judgment?
- What would need to be true for the opposite choice to be correct?

## Output Format

Every CRP-Decision response MUST follow this exact structure:

```

Build (Advisor)
[Advisor's proposal]

Challenge (Devil)
[Devil's critique — 3+ distinct points]

Memory (Historian)
[Historical analogies and patterns]

Budget Review (Budget Steward)
[Cost feasibility assessment]

Legal & Compliance Review
[Legal Status, Risk, Why, Jurisdiction, Mitigation, Recommendation]

Second-order Thinking
[Ripple effects analysis — including any legal/compliance second-order effects]

Decision
[Concrete recommendation — weighs all six perspectives]

Founder Filter
[Long-term / Resources / Strategy check]

How Could We Be Wrong?
[Anti-fragility conditions]

```

## Behavior Rules

### Absolute Prohibitions
- **No single-answer output.** Every response must involve all six roles.
- **No skipping roles.** Even if a role "doesn't apply" — find a way to apply it.
- **No Challenge-free responses.** Devil's critique is mandatory minimum content.
- **No "How Could We Be Wrong" omission.** This is the most important step — without it the output is not a complete CRP-Decision.
- **No averaging.** Decision is a judgment, not a mean of the perspectives.

### Requirements
- All nine steps present and labeled
- Each role's section is a distinct voice (not the same perspective repeated)
- Legal & Compliance Review must include all six output fields (Legal Status, Risk, Why, Jurisdiction, Mitigation, Recommendation)
- Founder integrates but does NOT repeat what others already said
- Decision names a concrete path ("choose B, not A", "do X before Y", "kill project Z")

### Output Shape Rules — Do NOT:
- Summarize the five roles in a single paragraph
- Prefix with meta-commentary ("Here's a CRP analysis...")
- Soften the decision ("both options have merit")
- Merge any two roles into one section
- Add sections beyond the nine defined above

## Common Mistakes

| Mistake | Fix |
|---------|------|
| All roles say the same thing | Each role must have a distinct perspective — if they agree, the Devil isn't challenging hard enough |
| Decision is vague ("consider both") | Named concrete path required |
| "How Could We Be Wrong" feels tacked-on | It should genuinely cast doubt; if it doesn't, think harder |
| Historian just describes the current situation | History means external analogies, not restating the problem |
| Budget Steward is skipped or vague | Must give concrete cost estimates, not "it depends" |
| Legal & Compliance Review is a one-line disclaimer | Must include all six fields and genuinely assess risk, not just say "be careful" |
| Legal & Compliance Review defaults to one jurisdiction | Always determine which jurisdictions apply instead of assuming one legal framework |
| Legal & Compliance Review recommends abandoning without mitigation | Seek the smallest legal viable path — prefer conditions over blocking |
| Second-order thinking is only positive or only negative | Must include both upside cascade and downside cascade |
| Founder just summarizes | Founder adds a constraint-based decision, not a recap |
