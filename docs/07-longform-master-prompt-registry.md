# YouTube Long-Form Master Prompt Registry

> The format layer of the pipeline. Where `docs/04-prompt-library.md` covers the *process* prompts (niche → ideation → script → optimization → scale), this doc covers the *format* prompts — the reusable visual-and-tonal blueprints that turn a finished script into a specific animated show. Each is a self-contained master prompt reverse-engineered from a proven, monetized YouTube channel.

**Status:** v1.0 · production
**Audience:** Strategists, script producers, and AI agents spinning up new long-form channels

---

## What this is

A working library of **modular master prompts** — one per proven YouTube long-form animation format. Each master prompt is a self-contained document: hand it any finished `{{SCRIPT}}` (plus `{{TOPIC}}` / `{{ERA}}` / `{{CHANNEL_NAME}}`) and a competent agent returns an episode visually and tonally locked to that format.

Formats are **building blocks.** The team spins up new channels by codename — *"spin up a CAVEDOODLE channel about the history of coffee"* — instead of reinventing an art direction, voice, and shot grammar every time. Every format here was dissected from a real channel that is already earning, so the look, pacing, and retention mechanics are copied from what the market has already paid for, not guessed.

---

## The Registry

Each row is a battle-tested format. **Economics proof** is the source channel's real performance — this is *why* the format is in the library. **Status** `HARDENED` = the master prompt cleared a 3-judge quality gate (or a direct senior audit against the global anti-slop rules) with zero critical issues.

| Codename | Source channel(s) | Economics proof | Status | Best for |
|---|---|---|---|---|
| **CAVEDOODLE** | Mack Explains (44.4K subs) | 20–25 min · daily cadence · 9–212K views | `HARDENED` | Question-format history/science explainers ("Did ancient humans have one partner?"). The caveman-stick-figure base format. |
| **CAVEDOODLE: NOIR** | Axen (41.7K subs) | 6.5–9 min · weekly · **21× views-to-subs** breakout (876K on the breakout video) | `HARDENED` | Single-question survival / disaster / negligence explainers. Dark, cinematic variant — same grammar, inverted sky-gradient + menace lighting. |
| **CAVEDOODLE: CANVAS** | Explain In Paint (42K subs) | 12–35 min · weekly · **10× views-to-subs** (876K breakout) | `HARDENED` | "The real story is weirder than the myth" origin stories (domestication, tech origins, food history). Warm paint-treatment variant. |
| **TALON** | Agent Flappy (119K subs) | 17–31 min · weekly · **~157K median views** | `HARDENED` | Flat 2D caricature "explained in N minutes" history — presidents, wars, disasters, scandals. Eagle-mascot narrator + archival punctuation. |
| **ATLAS** | Animated Historyy | 12–35 min · weekly · breakout format | `HARDENED` | "The whole story of X" — civilizations, empires, wars told chronologically with terrain maps + caricature portraits + then/now framing. |
| **DEEPDIVE** | Hey Historically | 15–75 min · weekly · premium tier | `HARDENED` | Single-topic deep history at high fact density (2–4 facts/min), chronically-online comedian narrator. |
| **SLUMBER** | Historian Sleepy | 3hr+ · weekly · extreme watch-hours **sleep** format | `HARDENED` | "Boring history for sleep" — slow narration over storybook oil paintings with slow Ken Burns. Sleep aid first, history second. |
| **STORYTIME** | Domics (7.18M) + TheOdd1sOut (20.8M) | 8–13 min · irregular · **lowest animation burden** | `HARDENED` | First-person personal/relatable storytime, comedic. Two sub-variants: DOMICS (near-monochrome, angular avatar) / ODD1SOUT (saturated, marshmallow avatar). |
| **FEATHER** | Jaiden Animations (15.1M subs) | 14–18 min · every 6–8 wks · **~8.5M median views** | `HARDENED` | First-person *expressive* storytime — the upgrade tier: real lip-sync, 4-tier character system, smears, 2× shot density, undercut sincerity. |
| **STICKWAR** | Alan Becker (33.7M subs) | 10–18 min · monthly · **12–29M views/episode** | `HARDENED` | SILENT stick-figure action/adventure (Animator vs. Animation lineage). Choreography *is* the product — no narration. Action/metaphor/battle topics only. |

### Family groupings

- **Caveman-explainer niche** — CAVEDOODLE, CAVEDOODLE: NOIR, CAVEDOODLE: CANVAS. Three siblings sharing a stick-figure-narrator skeleton but diverged in proportion, voice, and procedure. Pick by treatment: BASE (dry forensic), NOIR (grave/urgent survival-disaster), CANVAS (warmly-curious myth-vs-real).
- **Caricature-history cluster** — TALON, ATLAS, DEEPDIVE. All flat-caricature comedic history, scoped differently: TALON = single event/figure, ATLAS = whole-civilization sweep, DEEPDIVE = single-topic high-density deep dive. Pick by topic scope.
- **Storytime** — STORYTIME (minimal) and FEATHER (expressive) are the low and high tiers of first-person personal storytelling.
- **Standalone** — STICKWAR (silent action) stands alone.

---

## How the format-bible system works

Every master prompt follows the **same 11-section contract**, so any agent can pick up any format with zero prior context. The sections cover, in order: format identity → character/asset system → world & color rules → typography & UI → camera & staging → narration/voice → the script-to-shot-list procedure → per-shot prompt templates → the format's anti-slop rules → a verification checklist → variables. Because the contract is fixed, formats are swappable building blocks rather than bespoke one-offs.

Three things keep the library honest:

1. **Anti-slop rules.** A global rule set sits underneath every format's own §9. It bans the tells of generic AI animation — muddy color, off-model drift, dead-eyed characters, physics-defying motion, filler shots — and each format layers its own format-specific bans on top. "HARDENED" means a prompt passed against these rules.

2. **The deconstruction protocol.** No format is hand-written from imagination. To add one, the team runs a recon → eligibility gate → forensic deconstruction workflow: frames are harvested from the source channel, dissected shot-by-shot for art direction, motion, and script structure, and (where available) the source videos are re-watched for "motion truth." Only then is a master prompt synthesized and promoted. Undissected prompts are guesses; the protocol is what makes these copies of proven work.

3. **The full production pipeline.** The format prompt is one stage in a longer chain:

   **topic-validator** (niche/seed → validated angle + chosen format, through scope-lock → cashability → demand → saturation gates) → **script-generator** (topic + format → script, with a paired viral-title-generator and thumbnail step locking title ↔ thumbnail ↔ script so the title's promise is cashed in the first 30 seconds) → **format master prompt** (script → shot list → per-shot prompts, verified against the §10 checklist) → **upload-packager** (description, chapters from the beat structure, tags, end-screen/card timing, pre-publish checklist) → **retention protocol** (post-publish 24h/72h/7d/28d measurement, a causal triage tree — packaging → hook → beats → topic demand — feeding a per-channel learning log).

The registry is the index the pipeline picks from at the second gate. Everything upstream and downstream is format-agnostic; the master prompt is the only piece that changes per show.

---

## How the team accesses the full master prompts

The full 11-section master prompt texts are **internal, competitive IP** and are not published in this public repo. They live in three synchronized places for the team and its agents:

- **Supabase** — table `youtube_longform_master_prompts` in the Rising Tides Production project. One row per format keyed by `slug`, with `codename`, `source_channels`, `status`, `economics`, `best_for`, and the full `master_prompt` markdown. Query it from any agent or tool that already talks to the production database.
- **ocean-bedrock** — context collection `youtube-longform-master-prompts` in the Ocean-OS shared context store. One card per format (full master prompt + header metadata) plus an index card listing all ten. This is how Ocean-connected agents pull a format on demand.
- **Source repo** — the private `yt-longform-prompt-bible` repo is the source of truth. Each format lives at `styles/<slug>/MASTER-PROMPT.md`, alongside its `DISSECTION.md`, `JUDGE-LOG.md`, thumbnail playbook, and (where available) `MOTION-TRUTH.md`. Supabase and ocean-bedrock are mirrors of this repo — re-run the publishers after any prompt update to keep all three in sync.

Slug → codename map for lookups: `mackexplains`=CAVEDOODLE · `axen`=CAVEDOODLE: NOIR · `explaininpaint`=CAVEDOODLE: CANVAS · `agentflappy`=TALON · `animatedhistoryy`=ATLAS · `heyhistorically`=DEEPDIVE · `historiansleepy`=SLUMBER · `storytime-minimal`=STORYTIME · `storytime-expressive`=FEATHER · `alanbecker`=STICKWAR.
