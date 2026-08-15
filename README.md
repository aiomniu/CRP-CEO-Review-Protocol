<p align="center">
  <img src="https://img.shields.io/badge/status-stable-brightgreen" alt="Status: Stable">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License: MIT">
  <img src="https://img.shields.io/badge/platforms-Claude%20Code%20%7C%20ChatGPT%20%7C%20Codex%20%7C%20Universal-8A2BE2" alt="Platforms">
</p>

<h1 align="center">CRP — CEO Review Protocol</h1>
<p align="center"><em>Two skills, one framework: decisions and content each get their own review flow.</em></p>

---

## What is CRP?

**CRP** is a structured multi-role framework with two separate skills:

- **`crp:decision`** — strategic decision review
- **`crp:content`** — content review and rewrite

The shared principle is the same: a result is only as good as the strongest challenge it survives. The execution is different depending on whether you are making a decision or reviewing content.

## Why CRP?

Most AI assistants give you **one answer** — a single perspective optimized for coherence and confidence. CRP is different:

| Traditional AI | CRP |
|:---|:---|
| One voice, one answer | Multiple roles with conflicting perspectives |
| Optimizes for sounding right | Tests for being wrong |
| Confirmation bias amplified | Confirmation bias reduced |
| Cost is an afterthought | Cost feasibility is built in |
| Answers "what should we do?" or "how should this read?" | Separates decision review from content review |

**Use `crp:decision` when:** the task involves significant money, strategy, resources, or risk.

**Use `crp:content` when:** the task involves scripts, articles, or video drafts that need stronger hooks, structure, or rewrite quality.

## The Skills

| Skill | Role Set | Core Use |
|:---|:---|:---|
| `crp:decision` | Advisor, Devil, Historian, Budget Steward, Legal & Compliance Advisor, Founder | Strategic decisions, tradeoffs, risk, legal/compliance, resource allocation |
| `crp:content` | Hook Analyst, Audience Psychologist, Story Editor, Trend Observer, Retention Auditor, Voice Guardian, Chief Editor | Content diagnosis and rewrite |

## The Decision Skill Flow

`crp:decision` follows this sequence:

```
Build (Advisor)
→ Challenge (Devil)
→ Memory (Historian)
→ Budget Review (Budget Steward)
→ Legal & Compliance Review (Legal & Compliance Advisor)
→ Second-order Thinking
→ Decision
→ Founder Filter
→ How Could We Be Wrong?
```

## The Content Skill Flow

`crp:content` follows this sequence:

```
Idea Evaluation
→ Public Interest Check
→ Hook Review
→ Story Structure
→ Emotional Resonance
→ Differentiation
→ Retention Prediction
→ Voice Protection
→ Chief Editor Rewrite
→ Final Content
```

## Quick Start

### Claude Code

```bash
# Copy the skills into your Claude skills directory
cp skills/crp-decision/SKILL.md .claude/skills/crp-decision/SKILL.md
cp skills/crp-content/SKILL.md .claude/skills/crp-content/SKILL.md

# Then use:
/crp-decision Should we pivot to enterprise or keep doing PLG?
/crp-content Rewrite this video script so the hook is stronger.
```

### ChatGPT (GPTs)

1. Create a new GPT
2. In "Instructions", paste the content from `adaptations/chatgpt-gpts.md`
3. Done

### Any LLM

Paste the content from `adaptations/universal.md` into the system prompt.

### Codex

Add the instructions from `adaptations/codex.md` to your Codex system setup.

## Output Formats

### `crp:decision`

```

Build (Advisor)
[proposal]

Challenge (Devil)
[3+ risks]

Memory (Historian)
[historical patterns]

Budget Review (Budget Steward)
[cost feasibility]

Legal & Compliance Review
[Legal Status, Risk, Why, Jurisdiction, Mitigation, Recommendation]

Second-order Thinking
[ripple effects]

Decision
[concrete recommendation]

Founder Filter
[strategy check]

How Could We Be Wrong?
[failure conditions]

```

### `crp:content`

```
Content Diagnosis:

Hook Analyst:
[analysis]

Audience Psychologist:
[analysis]

Story Editor:
[analysis]

Trend Observer:
[analysis]

Retention Auditor:
[analysis]

Voice Guardian:
[analysis]

Chief Editor Rewrite:
[rewrite]

Why This Version Is Better:
[brief explanation]
```

## Behavior Rules

| Rule | Why |
|:---|:---|
| Use the right skill for the right task | Decision review and content review solve different problems |
| Keep role voices distinct | Each role catches different blind spots |
| Do not skip mandatory checks | Devil / Legal & Compliance Review / anti-fragility for decisions; Chief Editor rewrite for content |
| Preserve authenticity | Stronger output should not erase the original voice or intent |
| Keep the final output actionable | Decisions should end in a concrete path; content should end in a publishable rewrite |

## Repository Structure

```
CRP-CEO-Review-Protocol/
├── skills/
│   ├── crp-decision/
│   │   └── SKILL.md
│   └── crp-content/
│       └── SKILL.md
├── adaptations/
│   ├── claude-code.md
│   ├── chatgpt-gpts.md
│   ├── codex.md
│   └── universal.md
├── README.md
├── CONTRIBUTING.md
├── MAINTENANCE.md
└── LICENSE
```

## Keeping Updated

**We continuously improve CRP** based on real-world usage and community feedback. If you've installed CRP as a skill:

- **Check for updates periodically** — we recommend reviewing the latest version monthly or at the start of each new project cycle
- **If you use an AI agent** (Claude Code, Codex, etc.) — tell the agent to check this repository for updates. A well-configured agent will read the latest skill files, compare them with your local copy, and apply any changes
- **Manual update**: `git pull` the latest from this repo and re-copy the relevant `skills/` files to your skills directory

Changes are always backward-compatible. We do not break the core framework — we strengthen it.

## Status

**Stable** — The core framework has been refined through many strategic reviews and content rewrites. Multi-platform adaptations are maintained.

## License

MIT — free for personal and commercial use. Improve the protocol and share back.

---

<p align="center">
  <em>Built for users who want better decisions and better content.</em>
</p>
