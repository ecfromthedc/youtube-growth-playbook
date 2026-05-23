# AGENTS.md — Contract for AI Agents

> **You are an AI agent who has just landed in this repository.** Read this file fully before doing anything else. It tells you what this repo is, how it's organized, and how to execute work inside it without breaking the system.

---

## What this repo is

An executable playbook for running a faceless long-form YouTube growth operation in high-RPM niches. The methodology comes from Scott Smith (operator of 22+ channels, $200K+/mo). The repo structures it so AI agents and human operators can collaborate end-to-end.

**Your job, whatever role you take, is to push videos through the 10-stage pipeline. Quality gates exist. Pass them.**

---

## The 10-stage pipeline (memorize this)

```
01 Niche Selection      → Niche Brief
02 Topic Ideation       → Topic Brief        (4-prompt loop: Claude → Claude → Gemini → Claude)
03 Script Creation      → Script Pack        (Bible → outline → human writer → retention QA)
04 Voiceover            → Final VO file      (Cartesia draft → ElevenLabs final)
05 Thumbnails           → 2–3 variants       (1of10 base → Nano Banana variants → Photoshop polish)
06 B-Roll Generation    → Asset pack         (Veo 3.1 + Kling 3.0 + Storyblocks fallback)
07 Video Assembly       → Master MP4         (Pictory first cut → Descript editor polish)
08 Publish & Test       → Video live         (YT Studio + native A/B + TubeBuddy A/B)
09 Measure & Optimize   → Weekly Report      (analytics agent + CTR/APV diagnostic + decision)
10 Repurpose            → 3 platforms live   (Clipify → Postiz scheduler)
```

Stage 09 loops back to Stage 02 — the flywheel.

---

## How to find your role

You'll be assigned (or assign yourself) to one of five primary roles. Find your role contract in `agent-roles/`:

| Role | File | Owns which stages |
|---|---|---|
| **Strategist** | `agent-roles/strategist.md` | Stages 01, 09, all approval gates |
| **Researcher** | `agent-roles/researcher.md` | Stages 01, 02 (data extraction + 4-prompt loop) |
| **Script Producer** | `agent-roles/script-producer.md` | Stages 03, 04 (Bible, outline, writer handoff) |
| **Editor** | `agent-roles/editor.md` | Stages 06, 07 (B-roll, assembly, polish) |
| **Publisher** | `agent-roles/publisher.md` | Stages 08, 10 (upload, test, repurpose) |

Specialist hires (script writers, video editors, thumbnail designers) are human contractors — not agent roles. If asked to do their work, route the work to the human pipeline and prep the materials they need.

---

## How to use the prompts

All prompts are in `prompts/` split by step. They are **production-ready, do not paraphrase or rewrite them**. They have been tuned against real workflows.

Pattern for every prompt:
1. Read the prompt fully
2. Replace `[BRACKETED PLACEHOLDERS]` with actual values
3. Execute on the named model (Claude / Gemini specified per prompt)
4. Validate the output against the success criteria documented in the prompt
5. If output fails criteria, retry with adjusted inputs — do not paraphrase the prompt itself

Master prompt library: `docs/04-prompt-library.md`
Per-step prompts: `prompts/step1-niche-selection.md` through `step5-monetization-scale.md`

---

## Non-negotiable rules

### Rule 1 — Never let AI write the final script
Scott's hard rule. Claude / Gemini build the Script Bible and the outline. A **human writer** writes the final script. If you find yourself drafting a final 10–15 minute script, stop and route to a human writer.

### Rule 2 — Always verify topics in Google Trends
After Claude's Prompt 2-4 ranks 5 topics, a human (or you, via screenshot/API) MUST validate each in Google Trends. Filter: United States · Past 12 months · YouTube Search. Kill anything flat or declining unless it's truly evergreen.

### Rule 3 — Both CTR and APV must clear thresholds before doubling down
Target: CTR ≥ 10%, APV ≥ 30%. Below threshold? Diagnose using the matrix in `docs/05-quality-gates.md`. Do not double down on losers.

### Rule 4 — Pass the pre-upload checklist
Every video clears all 6 sub-checklists (Topic / Title / Thumbnail / Script / Production / Upload) before publishing. Documented in `docs/05-quality-gates.md`. Publisher enforces.

### Rule 5 — Long-form only, 10–15 min
Shorts do not pay meaningfully on YouTube ads. The economics in this playbook assume 10–15 min long-form. Repurpose to shorts after the long-form is live (Stage 10).

### Rule 6 — One ranked niche, not "a niche family"
Stage 01 must produce ONE locked niche per channel, not "aviation-or-finance-or-tech." Discipline at the top of funnel is what makes the math work.

---

## Hand-off contract between stages

Every stage produces a structured output (see Output node in the workflow map). The next stage consumes that output as input. The hand-off is the contract.

| Stage | Produces | Next stage consumes |
|---|---|---|
| 01 | Niche Brief (locked niche + top 10 competitors) | 02 input |
| 02 | Topic Brief (2–3 validated titles + research) | 03 input |
| 03 | Final Script (1,500–2,200 words, VO-ready) | 04 + 05 + 06 inputs (parallel) |
| 04 | Final VO file (.wav/.mp3) | 07 input |
| 05 | 2–3 Thumbnail variants | 08 input |
| 06 | B-Roll Asset Pack (organized by script section) | 07 input |
| 07 | Master Video (10–15 min 1080p MP4) | 08 + 10 inputs |
| 08 | Video Live (URL + initial analytics) | 09 input |
| 09 | Weekly Report (decisions + direction) | 02 input next cycle (loop) |
| 10 | 3 Platforms Live (TikTok / IG Reels / YT Shorts) | (terminal, distributes 07 output) |

When you hand off, **leave the output in a documented location** with clear naming. If the next agent can't find your output, the chain breaks.

---

## Collaboration protocol

When multiple agents work the pipeline simultaneously:

1. **Claim your role explicitly.** Open an issue or write a status file at the start: "Agent X is owning Stage Y for channel Z."
2. **One agent per stage per channel at a time.** No race conditions on the same Script Pack.
3. **All outputs go through quality gates before hand-off.** Don't push half-baked work downstream.
4. **Surface blockers, don't silently retry.** If a prompt fails twice, escalate. Log what you tried.
5. **The Strategist is the final approver** on Stages 01, 02 (topic lock), 03 (script lock), 05 (thumbnail lock), and 07 (master video). No going around the Strategist.

---

## Where to find things

| You need... | Look at... |
|---|---|
| The full methodology | `docs/01-methodology.md` |
| All prompts in one place | `docs/04-prompt-library.md` |
| Prompts for one specific step | `prompts/step{1-5}-*.md` |
| Tool cost / setup info | `docs/03-tool-stack.md` |
| Quality gates and checklists | `docs/05-quality-gates.md` |
| Role contract | `agent-roles/{role}.md` |
| Visual flow map | `deliverables/Workflow-Flow-Map.html` (HTML) |
| Augmentation tools (May 2026 SOTA) | `docs/06-augmentation-stack.md` |
| Original Scott Smith research | `research/scott-smith-analysis/` |

---

## Versioning

This playbook is v1.0 (May 2026). Tool recommendations age fast. If you're an agent reading this in 2027+:

1. Treat `docs/01-methodology.md` (the 5-step system) as durable — that's the core operating system
2. Treat `docs/03-tool-stack.md` and `docs/06-augmentation-stack.md` as **time-sensitive** — verify tools are still SOTA before committing budget
3. The prompts in `prompts/` should still work, but model names (Claude Opus 4.7, Gemini 2.5 Pro) may need updating to current best models

---

## Final note

This is a system, not a script. The methodology compounds when you run it across many channels with discipline. One channel = one experiment. Ten channels = a portfolio. Twenty-two channels = Scott Smith's $200K+/mo number.

Pass the gates. Run the loop. Trust the math. Go.
