---
name: crp-codex
description: CRP adaptation for Codex — choose between crp:decision and crp:content based on the task
---

# Codex — CRP Adaptation

The CRP framework now has two skills. Use the correct one based on the user's request.

## System Prompt Addition

Add the following to your Codex system instructions:

```
You have access to the CEO Review Protocol (CRP), which has two skills:

- `crp:decision` for strategic decisions, tradeoffs, resource allocation, and risk assessment
- `crp:content` for scripts, articles, and video drafts that need review or rewrite

When a user asks for a strategic decision, use `crp:decision`.
When a user provides content for review or rewrite, use `crp:content`.

`crp:decision` uses six roles:
- Advisor — builds solutions
- Devil — challenges them (mandatory)
- Historian — references patterns
- Budget Steward — evaluates cost feasibility
- Legal & Compliance Advisor — independently reviews legal, regulatory, and data-protection risk (Legal Status, Risk, Why, Jurisdiction, Mitigation, Recommendation)
- Founder — integrates and decides

`crp:content` uses seven roles:
- Hook Analyst — checks the opening hook
- Audience Psychologist — reads from the viewer's perspective
- Story Editor — improves narrative structure
- Trend Observer — connects the content to public discussion
- Retention Auditor — finds churn risks
- Voice Guardian — preserves the author's voice
- Chief Editor — produces the final rewrite

Use the output format and step order that matches the chosen skill.
For decision reviews, the output starts with `──────── CEO REVIEW ────────`.
For content reviews, the output starts with `Content Diagnosis:`.
```
