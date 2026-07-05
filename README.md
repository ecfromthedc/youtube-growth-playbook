# YouTube Growth Playbook

> End-to-end, agent-executable playbook for growing faceless long-form YouTube channels in high-RPM niches. Synthesized from Scott Smith's 5-step methodology (operator of 22+ faceless channels, $200K+/mo), augmented with the May 2026 AI tool stack, and structured for both human teams and AI agents to execute.

**Status:** v1.0 · May 2026
**License:** MIT
**Audience:** Operators, agencies, and AI agents running YouTube growth pipelines

---

## What this is

A complete A-to-Z playbook covering:

1. **The methodology** — Scott Smith's 5-step system (niche → ideation → script → first views → monetize/scale)
2. **The prompts** — every Claude / Gemini prompt for every step, copy-paste ready
3. **The team** — 8 roles with capacity benchmarks, daily/weekly workflows, hiring timeline
4. **The tools** — full 2026 AI stack (Claude, Gemini, Veo 3.1, Kling 3.0, ElevenLabs, Nano Banana 2, 1of10, Spotter Studio, Pictory, Descript, Clipify, Postiz, and more)
5. **The quality gates** — CTR/APV diagnostic matrix, pre-upload checklist, decision frameworks
6. **The workflow map** — n8n-style visual flow showing every node, owner, and tool
7. **The format registry** — 10 reverse-engineered long-form animation master prompts (each dissected from a proven, monetized channel) and how the team accesses them — see `docs/07-longform-master-prompt-registry.md`

This is what a serious YouTube growth operation looks like in 2026. AI-augmented at every step, with humans owning strategy, gates, and judgment calls.

---

## Repository structure

```
youtube-growth-playbook/
├── README.md                  ← this file (human entry point)
├── AGENTS.md                  ← agent contract (read this if you're an AI)
├── LICENSE                    ← MIT
│
├── docs/                      ← the methodology + reference docs
│   ├── 00-executive-summary.md
│   ├── 01-methodology.md      ← the 5-step system end-to-end
│   ├── 02-team-playbook.md    ← roles, capacity, weekly rhythm
│   ├── 03-tool-stack.md       ← every tool, cost, who uses it
│   ├── 04-prompt-library.md   ← all 14 prompts in one doc
│   ├── 05-quality-gates.md    ← CTR/APV metrics, checklists, decision rules
│   ├── 06-augmentation-stack.md ← 2026 AI tool upgrades
│   └── 07-longform-master-prompt-registry.md ← the 10 format master-prompt registry + how the team accesses them
│
├── prompts/                   ← prompts split per step for direct copy-paste
│   ├── step1-niche-selection.md
│   ├── step2-topic-ideation.md
│   ├── step3-script-creation.md
│   ├── step4-optimization-analytics.md
│   └── step5-monetization-scale.md
│
├── agent-roles/               ← role contracts for AI agents
│   ├── strategist.md
│   ├── researcher.md
│   ├── script-producer.md
│   ├── editor.md
│   └── publisher.md
│
├── deliverables/              ← visual + standalone team deliverables
│   ├── Scott-Smith-Team-Playbook.html
│   ├── Workflow-Augmentation-Report.html
│   └── Workflow-Flow-Map.html
│
└── research/                  ← primary source research
    └── scott-smith-analysis/
```

---

## Quick start

### If you're a human operator
1. Read `docs/01-methodology.md` — the 5-step system
2. Open `deliverables/Workflow-Flow-Map.html` in a browser — see the whole pipeline visually
3. Skim `docs/03-tool-stack.md` — understand what you'll need to subscribe to
4. Read `docs/02-team-playbook.md` — figure out who on your team owns what
5. Pick a niche. Run `prompts/step1-niche-selection.md`. Go.

### If you're an AI agent
1. Read `AGENTS.md` first — that's your contract for working in this repo
2. Identify your role in `agent-roles/` (Strategist, Researcher, Script Producer, Editor, or Publisher)
3. The prompts in `prompts/` are ready to execute — use them as written
4. Quality gates in `docs/05-quality-gates.md` are non-negotiable — pass them before handing off
5. Collaborate with other agents by leaving structured outputs at the documented hand-off points

---

## The economics (why this works)

| Variable | Number |
|---|---|
| Per-video production cost | ~$75 (writer + VO + editor + thumbnail) |
| Target RPM | $7+ minimum (Scott's flagship: $12.09) |
| Channel investment to first revenue | ~$2,400 over 4 months (32 videos × $75) |
| Mature channel earning potential | $5K–$30K+ per month |
| Portfolio principle | 3 of 22 videos drive 90% of revenue |
| Operator at scale | 22+ channels in parallel |

The math only works if you pick high-RPM niches and play the portfolio game. Most videos flop. The winners pay for everything.

---

## The 2026 AI augmentation

Beyond Scott's original stack, this playbook integrates the May 2026 best-in-class:

- **Niche intelligence:** 1of10 (62B-view outlier database) + Spotter Studio
- **Scripts:** Claude Opus 4.7 (Script Bibles) + Gemini 2.5 Pro Deep Research + Subscribr (retention QA)
- **Voice:** ElevenLabs v3 (primary) + Cartesia Sonic 3 (fast drafts) + Chatterbox (self-hosted overflow)
- **Thumbnails:** 1of10 Thumbnails + Nano Banana 2 (best text rendering) + Photoshop Generative Fill polish
- **B-roll generation:** Veo 3.1 (workhorse) + Kling 3.0 (multi-shot) + Seedance 2.0 (narrative) + Storyblocks (fallback)
- **Assembly:** Pictory 2.0 (auto first cut) + Descript (editor polish)
- **Analytics:** VidIQ + TubeBuddy A/B + Spotter Studio + Looker Studio multi-channel dashboard
- **Repurposing:** Clipify (free, local, MIT) + Postiz (cross-platform scheduling)

Full cost breakdown in `docs/06-augmentation-stack.md`.

---

## Source attribution

- **Primary methodology:** Scott Smith's faceless YouTube workshop (operator of 22+ channels). Workshop content synthesized into `docs/01-methodology.md`.
- **Original Instagram analysis:** `research/scott-smith-analysis/` — the original deep research on Scott's lead-gen funnel.
- **Augmentation tooling research:** Live market research conducted May 2026 across Perplexity, web search, and internal knowledge base.

---

## License

MIT. Use, fork, modify, deploy. Attribution appreciated but not required.

---

## Contributing

This is designed for agent collaboration. Other agents can:
- Add new prompts to `prompts/` (follow the existing template)
- Add new role specifications to `agent-roles/`
- Update tool recommendations in `docs/03-tool-stack.md` as the AI landscape evolves
- Add case study results in a new `case-studies/` directory

Pull requests welcome. Tag issues with the stage number (e.g., `stage-3-script`) for triage.
