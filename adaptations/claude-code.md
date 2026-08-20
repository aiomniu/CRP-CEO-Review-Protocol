---
name: crp-claude-code
description: CRP adaptation for Claude Code — crp:decision and crp:content skill setup and slash-command usage
---

# Claude Code — CRP Adaptation

## Installing the Skills

Place the two skill files into your `.claude/skills/` directory:

```bash
cp skills/crp-decision/SKILL.md .claude/skills/crp-decision/SKILL.md
cp skills/crp-content/SKILL.md .claude/skills/crp-content/SKILL.md
```

## Slash Commands

Add to `.claude/commands/`:

### crp-decision.md

```markdown
---
name: crp-decision
description: Run crp:decision — structured multi-role decision analysis
---

# /crp-decision

Run a CRP decision review on a strategic question.

## How to use

/crp-decision [your strategic question]

Example:
/crp-decision We have $50k runway, 200 free users, 0 paying. Pivot to enterprise or double down on PLG?

## What happens

The agent activates `crp:decision` with six roles — Advisor, Devil, Historian, Budget Steward, Legal & Compliance Advisor, Founder — executing nine steps:

1. Build — Advisor proposes solution
2. Challenge — Devil attacks (3+ risks)
3. Memory — Historian cites patterns
4. Budget Review — Budget Steward evaluates cost feasibility
5. Legal & Compliance Review — Legal & Compliance Advisor assesses risk (Legal Status, Risk, Why, Jurisdiction, Mitigation, Recommendation)
6. Second-order Thinking — Ripple effects
7. Decision — Concrete recommendation
8. Founder Filter — Strategic consistency check
9. How Could We Be Wrong? — Anti-fragility check
```

### crp-content.md

```markdown
---
name: crp-content
description: Run crp:content — multi-role content review and rewrite
---

# /crp-content

Run a CRP content review on scripts, articles, or video drafts.

## How to use

/crp-content [paste your content]

Example:
/crp-content Here's my video script — can the hook be stronger?

## What happens

The agent activates `crp:content` with eight roles — Hook Analyst, Audience Psychologist, Story Editor, Trend Observer, Value Density Editor, Retention Auditor, Voice Guardian, Chief Editor — and produces:

1. Content Diagnosis — each role's analysis
2. Chief Editor Rewrite — a publish-ready revised version
3. Why This Version Is Better — brief comparison
```

## Auto-trigger

The agent auto-triggers the appropriate CRP skill when detecting:

**`crp:decision` triggers:** Resource allocation, product tradeoffs, risk assessment, pricing decisions, hiring decisions, "should we do X" with significant impact.

**`crp:content` triggers:** Draft scripts, articles, blog posts being reviewed for audience appeal, hook strength, or readability.
