# Augmentation Stack — May 2026 State of the Art

> Scott Smith's original methodology used Claude + Gemini + vidIQ + ElevenLabs. This doc captures the May 2026 AI tool augmentation — the additions that take a baseline operation to best-in-class.

---

## Why this matters

The AI video / content stack is evolving monthly. Tools that didn't exist 12 months ago (Nano Banana 2, Veo 3.1, Kling 3.0, Cartesia Sonic 3, Clipify) are now best-in-class. This doc is the May 2026 snapshot.

**If you're reading this in 2027+:** validate every tool below is still SOTA before committing budget. The methodology in `01-methodology.md` is durable; the tooling here ages fast.

---

## The augmentation stack by stage

### Stage 01 — Niche Selection

| Tool | What it adds | Cost |
|---|---|---|
| **1of10** | Niche intelligence trained on 62B-view outlier database. Surfaces niches where videos outperform 10x–100x channel median. | ~$49/mo |
| **Spotter Studio** | Channel-level intel backed by MrBeast's investment fund. What channels are growing fastest, what topics they're winning on. | ~$59/mo |
| **ViewStats** | MrBeast's own analytics platform. Deep channel/video benchmarking. | $24–199/mo |

**Recommended:** 1of10 + Spotter Studio together (~$108/mo) replace days of manual research and validate Claude's niche brainstorm against real outlier data.

---

### Stage 02 — Topic Ideation

| Tool | What it adds | Cost |
|---|---|---|
| **Subscribr** | YouTube-native AI script + idea tool. Reverse-engineers viral videos to extract hook, structure, retention triggers. Multi-model support. | ~$49/mo |
| **Custom Claude Code skill** | Wrap the 4-prompt sequence in a skill that takes niche + competitor channel URL and runs the full sequence automatically. | Build cost only |
| **Exploding Topics** | Trend discovery before topics hit Google Trends. | $39–249/mo |

**Recommended:** Build the Claude Code skill (~2 hours, $0 ongoing). Add Subscribr to challenge Claude's topic rankings with a YouTube-trained model.

---

### Stage 03 — Script Creation

| Tool | What it adds | Cost |
|---|---|---|
| **Claude Opus 4.7 (1M context)** | Best in class for long-form structure, narrative arc analysis, Script Bible generation. 1M context = feed 30+ transcripts at once. | $20–200/mo |
| **Gemini 2.5 Pro Deep Research** | Outline generation + research surfacing. Deep Research mode is the workhorse for "find me 15 facts to weave in." | $20/mo |
| **Subscribr AI Script Editor** | Retention QA layer. Analyzes pacing, hooks, drop-off risks. Returns rewrite notes. | Bundled with Subscribr |
| **GPT-5 (cross-validation)** | Best at hook generation per market research. Use as second opinion on hook variations only. | $20+/mo |
| **Marc Cleroux `/hooks` skill** | Hook database scored against proven viral patterns. Free, installed locally. | $0 |

**Recommended:** Claude Opus + Gemini Deep Research + Subscribr + Marc's hooks skill + human writer = five-layer pipeline, each doing what it's best at.

---

### Stage 04 — Voiceover

| Tool | What it adds | Cost |
|---|---|---|
| **ElevenLabs v3 (Creator/Pro)** | Still quality leader for long-form. Best breath placement, prosody, multi-minute consistency. Voice cloning gold standard. | $22–99/mo |
| **Cartesia Sonic 3** | 40–90ms time-to-first-audio. Fastest commercial TTS. Use for rapid iteration / drafts. | From $5/mo |
| **Fish Audio** | #1 on TTS-Arena blind tests. Fraction of ElevenLabs cost. | Pay-per-use |
| **Hume AI Voice** | Leads on emotion. For niches where emotional delivery matters (true crime, drama). | $20+/mo |
| **Chatterbox (Resemble AI)** | Open-source. 63.75% blind preference over ElevenLabs in naturalness. Self-host for unlimited. | $0 self-hosted |

**Recommended:** ElevenLabs v3 (primary) + Cartesia Sonic 3 (drafts) + Chatterbox (overflow at scale).

---

### Stage 05 — Thumbnails

| Tool | What it adds | Cost |
|---|---|---|
| **1of10 Thumbnails** | Trained on 62B-view outlier data. Generates thumbnails matched to niche winners. | ~$49/mo (with niche layer) |
| **Braiv Thumbnails** | Transcript-driven. Reads actual video, designs thumbnails matching content. Predictive CTR scoring. | ~$29/mo |
| **Nano Banana 2 (Gemini 3.1 Flash Image)** | Best text rendering of any generative model. $0.067/image. MCP available for Claude Code integration. | Usage-based |
| **Ideogram v3** | Best for thumbnails with text integrated INTO the image. | $8–48/mo |
| **Pikzels FaceSwap** | Drops your face into AI-generated scenes. Solves "no more photo shoots" problem. | $19/mo |
| **Adobe Photoshop Generative Fill** | Polish layer after AI base. Commercially safe (Firefly trained on licensed content). | $23/mo |
| **YouTube Test &amp; Compare** | Native A/B testing. Free. Should run on every video. | $0 |
| **ThumbnailTest.com** | Pre-publish human voting. Useful for high-stakes uploads. | $29–99/mo |

**Recommended:** 1of10 base + Nano Banana 2 variants + Photoshop polish + YouTube native A/B test on every upload.

---

### Stage 06 — B-Roll &amp; Video Generation

| Tool | What it adds | Cost |
|---|---|---|
| **Google Veo 3.1** | Strongest all-rounder. Only true 4K native. Best for establishing shots, narrative B-roll. | $0.15/sec fast mode |
| **Kling 3.0** | Multi-shot sequences (3–15 sec) with subject consistency. Released Feb 2026. | ~$0.10/sec |
| **Seedance 2.0** | Narrative content winner. Multi-shot + synchronized audio. Via Higsfield. | Via Higsfield sub |
| **Runway Gen-4** | Pro favorite for granular creative control — camera moves, motion brush. | $15–95/mo |
| **Luma Ray 2** | Strong image-to-video animation. | $15+/mo |
| **Wan 2.1 (open-source)** | Free self-hosted video gen. Quality below Veo/Kling but $0 marginal cost. | $0 |
| **Storyblocks** | Stock fallback library. | $228/yr unlimited |

**Recommended:** Veo 3.1 (workhorse) + Kling 3.0 (multi-shot) + Seedance via Higsfield (narrative). Storyblocks for fallback. Stop sourcing perfect stock — generate it.

**NOTE:** Sora is being discontinued. OpenAI announced in March 2026 that Sora web/app sunset April 26, 2026 and Sora API sunset September 24, 2026. Migrate any Sora dependency to Veo/Kling/Runway/Seedance.

---

### Stage 07 — Video Assembly

| Tool | What it adds | Cost |
|---|---|---|
| **Pictory 2.0** | Best-in-class AI script-to-video. 3M+ video clips + 15K music tracks royalty-free. Agent-mode auto-selects B-roll. | $23–119/mo |
| **InVideo AI** | Text-prompt → complete video. Good for "first draft fast." | $25–60/mo |
| **Descript** | Transcript-based editing. Cuts edit time ~50% on talking-head + VO content. | $12–24/user/mo |
| **Adobe Premiere Pro** | Generative Extend, Object Mask, AI-powered editing. Pro editor's tool. | $23/mo |
| **DaVinci Resolve (free)** | Free tier excellent. Strong AI features in Studio version. | Free / $295 |
| **CapCut Pro** | Fast, AI-augmented, cheap. Best for editors who know it. | $8/mo |

**Recommended:** Pictory 2.0 first cut + Descript editor polish. Premiere/Resolve for the 20% of videos needing handcraft.

---

### Stage 08 — Publish &amp; Test

| Tool | What it adds | Cost |
|---|---|---|
| **VidIQ Boost+** | AI ideation + structured creator coaching. Daily idea feed. | $39/mo |
| **TubeBuddy Legend** | A/B testing on titles, thumbnails, descriptions, tags vs CTR/watch time. | $27/mo annual |
| **YouTube Test &amp; Compare** | Native thumbnail A/B. Free. | $0 |

**Recommended:** VidIQ + TubeBuddy together. Native YT A/B on every upload.

---

### Stage 09 — Measure &amp; Optimize

| Tool | What it adds | Cost |
|---|---|---|
| **Looker Studio** | Free Google product with native YouTube Analytics connector. Multi-channel dashboard. | $0 |
| **Spotter Studio** | Multi-channel competitive monitor. | ~$59/mo |
| **Custom Claude Code analytics agent** | Auto-generates weekly Prompt 4-3 report across all channels. | Build cost only |

**Recommended:** Looker Studio dashboard (free, built once) + Claude Code analytics agent (build in-house, ~4 hours).

---

### Stage 10 — Repurpose

| Tool | What it adds | Cost |
|---|---|---|
| **Clipify** | Open-source Claude Code skill. Long video → 3 vertical clips with speaker tracking + opus captions. Local. MIT. | $0 |
| **OpusClip** | Industry standard alternative. Better UI but paid. Has AI B-roll insertion on clips. | $15–95/mo |
| **Submagic** | Caption-focused. Premium animated captions. | $10–67/mo |
| **Postiz** | Cross-platform scheduler (TikTok / IG Reels / YT Shorts). Open-source. | ~$10/mo |

**Recommended:** Clipify (free, local) + Postiz scheduler. Replaces OpusClip + Submagic stack.

---

## Cost summary at 5-channel operation

### Original stack (Scott's baseline)
~$116/month: Claude Pro + Gemini Advanced + vidIQ Boost+ + ElevenLabs Creator + Canva Pro

### Augmented stack (May 2026 SOTA)
~$485/month total, including:

| Layer | Tools | Monthly |
|---|---|---|
| Niche intelligence | 1of10 + Spotter Studio | $108 |
| Script QA | Subscribr | $49 |
| Voice | ElevenLabs v3 + Cartesia Sonic 3 | ~$32 |
| Video generation | Veo 3.1 + Kling 3.0 | ~$70 |
| Thumbnails | Nano Banana 2 usage + Photoshop | ~$53 |
| Assembly | Pictory 2.0 + Descript | ~$42 |
| Analytics | TubeBuddy Legend | $27 |
| Distribution | Postiz | $10 |
| Existing | Claude Pro + Gemini + vidIQ + ElevenLabs + Canva | $116 |

**Incremental spend vs baseline:** +$369/month
**At 5 channels generating $5–15K each at maturity:** &lt;1% of revenue
**Velocity gain:** 3–5x faster production at higher quality floor

---

## Internal assets already owned (no marginal cost)

Reference these in Alexandria / your knowledge base:

- **Clipify** — installed at `~/.claude/skills/clipify/`. Replaces OpusClip $95/mo + Submagic $67/mo.
- **Nano Banana 2** — documented; MCP available for Claude Code integration
- **Seedance 2.0 + Higsfield workflow** — full UGC ad pipeline documented
- **Marc Cleroux skills suite** — `script`, `hooks`, `repurpose` skills installed
- **11Labs voice replacement workflow** — documented audio-replace pipeline
- **VibeVoice + RVC** — local TTS / voice cloning, no per-use cost
- **Claude Code Content Production System** — orchestration patterns documented

---

## The moat

Tools alone don't create competitive advantage — everyone can buy Veo 3.1. The moat is the **integration** + accumulated assets:

1. **Proprietary prompt library** — every prompt versioned and refined against real channels
2. **Multi-channel pattern library** — what works in aviation gets tested in finance, compounds
3. **End-to-end local pipeline** — Clipify (local), VibeVoice/RVC (local), Nano Banana MCP, Claude Code orchestration. Own the workflows, don't rent SaaS.
4. **Verification &amp; quality gates** — codified checklists ensure quality doesn't drift at scale
5. **Speed without quality sacrifice** — AI stack runs at 3–5x velocity of pure-human teams

That's the "best at YouTube growth" play. Tools are commodities. The system that wraps them isn't.
