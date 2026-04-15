# APEX — AI Product Executive Agent
### A 6-stage autonomous product reasoning agent built for senior PM and Director-level decision making

**Live Demo → [eval4576.github.io/apex-agent](https://eval4576.github.io/apex-agent)**

---

## What It Does

APEX mirrors what a senior product leader actually does in a week — a connected, multi-step reasoning loop that takes raw, messy product signals and produces board-ready strategy through six autonomous stages.

This is not a chatbot. This is not a summarizer. This is a reasoning agent.

```
INGEST → SYNTHESIZE → DIAGNOSE → DEVIL'S ADVOCATE → STRATEGIZE → BRIEF
```

### Stage 01 · Signal Ingest
Classifies raw, multi-source input — user interviews, support tickets, NPS verbatims, usage metrics, sales objections, competitive intel — by source type, user segment, and confidence level. Flags data gaps and low-confidence signals explicitly before any synthesis begins.

### Stage 02 · Synthesis Engine
Clusters signals into Jobs-to-be-Done themes with frequency and severity ratings. **Detects signal conflicts between user segments** — surfacing when power users want the opposite of new users, and reasoning through how to resolve the tension. Surfaces minority signals that could be early indicators of larger problems. Can revise Stage 01 conclusions when synthesis reveals something classification missed.

### Stage 03 · Strategic Diagnosis
Scores opportunities on a 4-axis model: user frequency × pain severity × revenue impact × strategic alignment. Produces a force-ranked opportunity list with explicit trade-off reasoning. Generates an **anti-portfolio** — what is explicitly NOT being built and why. States the condition that would invert the entire conclusion.

### Stage 04 · Devil's Advocate
Argues against its own top recommendation as forcefully as possible. Presents a competing strategic thesis. Delivers a verdict with a revised confidence score. **No other PM agent does this.** The ability to stress-test your own recommendation before a VP review is the hallmark of senior-level product thinking.

### Stage 05 · Strategic Bet
Produces a single, opinionated recommendation — not a hedge. Includes a testable hypothesis, MVP definition, success metrics, phased sprint plan, risks with mitigations, and **kill criteria**: the conditions under which you would stop and walk away from the bet. Kill criteria are the clearest signal of intellectual honesty and resource discipline that Directors and VPs look for.

### Stage 06 · Executive Brief
Generates a copy-ready executive brief in your choice of format:
- **Amazon 6-Pager** — narrative format with Situation, Tenets, Goals, Plan, What We're Not Doing, and VP-level FAQ
- **Google PRFAQ** — Press Release, Problem, Solution, User Quote, Internal FAQ, External FAQ

Output copies as clean Markdown, ready to paste into a doc and send.

---

## The Reasoning Trace

Every stage surfaces its live reasoning in the right panel — not just the output, but the thinking. Conflict detection, confidence calibration, upstream revisions, minority signals. You can see exactly why the agent reached each conclusion and what would change it.

This is the feature that stops FAANG interviewers cold. It maps directly to how top tech companies evaluate AI product decisions: explainability, confidence calibration, and reasoning auditability.

---

## Why I Built This

Most PM agents do one thing: summarize feedback, generate a PRD, score opportunities. APEX does what a **senior PM actually does** — a connected reasoning loop where each stage informs the next, conflicts are surfaced rather than smoothed over, and the final recommendation has been stress-tested before it reaches leadership.

The architecture is modeled on how product reviews actually work at top-tier companies:

- **Signal conflict detection** mirrors the tension between user segments that every marketplace PM navigates daily
- **The anti-portfolio** mirrors the explicit scope discipline that Amazon and Google require in product reviews
- **Kill criteria** mirror the intellectual honesty that separates great product leaders from good ones
- **The Devil's Advocate stage** mirrors the designated challenger role in Google and Meta product reviews

Built from 8+ years of leading product across multi-sided marketplaces, platform APIs, and B2B SaaS — including Kitchen United (Google Ventures, $100M Series C) and Connected Dealer Services (CarRX).

Built as part of the **AI PM Toolkit** at [Motionova Labs](https://motionovalabs.com).

---

## Example Scenarios Included

| Scenario | Domain | Strategic Context |
|---|---|---|
| Ghost Kitchen Marketplace | Multi-sided Marketplace | Series A/B — scaling growth |
| Automotive SaaS (CarRX) | B2B SaaS | Series A/B — scaling growth |
| Platform API Monetization | Platform API Product | Series A/B — scaling growth |
| Retention Crisis | Enterprise SaaS | Turnaround — reversing decline |

---

## Built With

- **Vanilla HTML / CSS / JavaScript** — zero dependencies, runs in any browser
- **Anthropic Claude API** (`claude-sonnet-4-20250514`) — multi-turn sequential reasoning with state passing between stages
- **GitHub Pages** — zero-infrastructure deployment

---

## How to Run Locally

```bash
# Clone the repo
git clone https://github.com/eval4576/apex-agent.git

# Open directly in browser — no build step, no server, no backend
open index.html
```

The agent calls the Anthropic API directly from the browser. No backend required.

---

## The PM Thinking Behind the Architecture

**Why sequential stages instead of one big prompt?**
Each stage receives the prior stage's output as structured context. This means Stage 03 doesn't just see the raw signals — it sees what Stage 02 concluded about them, including any conflicts detected. Stage 04 argues against Stage 03's top pick. Stage 05 incorporates Stage 04's stress-test. The chain compounds. A single prompt can't do this.

**Why the Devil's Advocate stage?**
A recommendation that hasn't been challenged isn't a recommendation — it's a guess. Every senior PM has been in a review where a VP asked "what's the strongest argument against this?" The agent answers that question before the VP has to ask it.

**Why kill criteria?**
Kill criteria are the most underused PM tool in practice. Defining upfront when you'd walk away from a bet demonstrates resource discipline and intellectual honesty that VPs and Directors look for in senior candidates. Most PMs never define them. APEX forces it.

**Why two brief formats?**
Amazon and Google are the two most influential product cultures in the industry. Their document formats reflect fundamentally different communication philosophies — Amazon's narrative 6-pager vs. Google's PRFAQ. A PM who can write in both formats is demonstrably more versatile than one who defaults to slides.

---

## Part of the AI PM Toolkit

This is **Project 7 (Capstone)** in a series of AI tools built to demonstrate applied AI product management:

| # | Project | Status |
|---|---|---|
| 01 | AI Discovery Interview Analyzer | ✅ [Live](https://eval4576.github.io/AI-Discovery-Tool-Analyzer/) |
| 02 | AI Metrics Dashboard + Narrative | ✅ [Live](https://eval4576.github.io/ai-metrics-dashboard/) |
| 03 | AI PRD Generator | ✅ [Live](https://eval4576.github.io/ai-prd-generator/) |
| 04 | Marketplace AI Opportunity Audit | 🔜 Coming soon |
| 05 | AI Onboarding Flow Analyzer | 🔜 Coming soon |
| 06 | Product Strategy Memo Series | 🔜 Coming soon |
| **07** | **APEX — PM Agent Prototype (Capstone)** | **✅ Live** |

---

## About

Built by a Senior Product Manager with 8+ years across venture-backed marketplaces, platform APIs, and B2B SaaS — including Kitchen United (Google Ventures, $100M Series C) and Connected Dealer Services (CarRX).

**[Portfolio](https://motionovalabs.com) · [LinkedIn](#) · [GitHub](https://github.com/eval4576)**
