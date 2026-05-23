# Agent Role — Video Editor / B-Roll Producer

> Editor owns Stages 06 (B-roll generation) and 07 (video assembly). AI builds the first cut. You polish it. The line between "ship-ready" and "amateur hour" is here.

---

## What you own

| Stage | Your role |
|---|---|
| **06 B-Roll Generation** | Generate shot list from script, run AI video gen pipeline (Veo 3.1 / Kling 3.0 / Seedance 2.0), source stock fallbacks. |
| **07 Video Assembly** | Take AI's first cut (Pictory / InVideo) and polish in Descript / Premiere / DaVinci to ship quality. |

---

## Workflow: From Script Pack to Master Video

### Stage 06 — B-Roll Asset Pack

1. **Generate shot list**
   - Read the final script
   - Run Claude prompt: "Reading this script, give me 30–50 specific B-roll shots scene by scene. For each shot: description, duration, scene context, AI-generatable vs stock-needed."
   - Verify: shots are specific (not "businessman walking" — "30-year-old in casual blazer walking through Manhattan financial district at dusk")

2. **Generate AI B-roll**
   - **Veo 3.1** — workhorse for establishing shots, narrative B-roll, 4K native
   - **Kling 3.0** — multi-shot scenes (3–15 sec) requiring character/subject continuity
   - **Seedance 2.0** — narrative-driven content via Higsfield (with Nano Banana Pro avatars if needed)
   - Cost: ~$0.10–$0.15/sec depending on model. Budget ~$30–50/video at scale.

3. **Source stock fallbacks**
   - **Storyblocks** (unlimited annual) — for any shot AI can't reliably generate
   - **Envato Elements** — alternative
   - **Pexels / Pixabay** — free fallback for low-stakes shots

4. **Organize the asset pack**
   - Folder structure: `[channel]/[video-id]/broll/[section-N]-[shot-N].mp4`
   - One folder per video, timed to script sections

---

### Stage 07 — Video Assembly

#### Step 1: AI first cut

1. **Run Pictory 2.0 or InVideo AI**
   - Upload script + VO file + B-roll asset pack
   - AI assembles a first draft with B-roll, transitions, captions
   - Expected runtime: 10–15 min finished video
   - Output: a working draft that's ~60% ship-ready

#### Step 2: Editor polish (where you spend your real time)

1. **Open in Descript** (transcript-based editor — fastest for talking-head + VO content)
   - Re-read the script
   - Cut anything that drags
   - Tighten transitions
   - Add lower thirds, text overlays for key facts
   - Color grade for consistency
   - ~30–60 minutes per video at experienced pace

2. **Alternative editors:**
   - **Adobe Premiere Pro** — for videos that need handcraft (heavy effects, complex grading)
   - **DaVinci Resolve** (free tier) — strong AI features, good for color-critical work
   - **CapCut Pro** — fast, AI-augmented, cheap

3. **Audio cleanup**
   - VO levels consistent (compression + normalization)
   - Music ducked under VO
   - No sudden spikes or drops

4. **End screen + cards**
   - Subscribe button overlay in last 20 seconds
   - Next-video card around 80% mark
   - Configured for the channel's playlist strategy

#### Step 3: Export

- 1080p MP4, H.264, 8–12 Mbps bitrate
- 16:9 ratio
- Filename: `[channel]-[YYYY-MM-DD]-[slug].mp4`
- Save to channel's shared drive folder

---

## Pre-Upload Checklist (you submit, Strategist signs off)

Before declaring the video ready for Stage 08 (Publish), confirm:

### Production gate
- ✅ Voiceover clear, well-paced (not too fast, not too slow)
- ✅ B-roll matches narration (no generic stock where specific is needed)
- ✅ Audio levels consistent (music under VO, no sudden spikes)
- ✅ Captions auto-generated and cleaned up
- ✅ Video ends with end screen (subscribe + next video thumbnails)

If any sub-gate fails → fix before submitting. The Publisher won't accept videos that don't pass.

---

## Tools you use

- **Pictory 2.0** — AI first-cut assembly (~$23–119/mo)
- **InVideo AI** — alternative AI assembler (~$25–60/mo)
- **Descript** — transcript-based editor for polish ($12–24/user/mo)
- **Adobe Premiere Pro** — heavy editor work ($23/mo)
- **DaVinci Resolve** — free tier or Studio ($295 one-time)
- **CapCut Pro** — fast editor with AI ($8/mo)
- **Veo 3.1** — AI video generation (workhorse)
- **Kling 3.0** — AI video generation (multi-shot)
- **Seedance 2.0** — AI narrative video via Higsfield
- **Storyblocks** — stock library (~$228/yr unlimited)
- **Frame.io or Google Drive** — asset sharing between team members

---

## Capacity

8–12 finished videos per editor per week with the AI-augmented pipeline (Pictory first cut → Descript polish). 2–3 editors = 16–36 videos/week capacity.

Without AI first-cut tooling, you'd be at 3–5 videos/week. The AI is what makes the math work.

---

## Quality bar

Every video must:
- Feel intentional, not assembled
- Have B-roll that matches narration meaning (not just "business stock footage during business talk")
- Have captions cleaned up (no transcription errors)
- Have audio that's not fatiguing across 10–15 min
- Hit the channel's brand consistency (color grade, lower-third style, end card layout)

If a Strategist comments "this feels generic" — your B-roll was too stock-y. Generate more custom AI B-roll.

---

## What you DON'T do

- You don't pick the topic (Researcher does)
- You don't write the script (Writer does, Producer manages)
- You don't generate the voiceover (Script Producer or you, via ElevenLabs)
- You don't approve the upload (Strategist does)
- You don't manage YouTube SEO or thumbnails (Publisher + Thumbnail Designer do)

---

## Hand-off contract

Your output (Master Video MP4 + Pre-Upload Checklist) goes to:
- **Stage 08 (Publisher)** — uploads to YouTube
- **Stage 10 (Repurpose)** — Clipify chops 3 vertical clips from the master

The master needs to be clean enough that Clipify's speaker tracking finds clear visual moments and the captions burn-in correctly.
