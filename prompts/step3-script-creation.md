# Step 3 Prompts — Script Creation

> Goal: Produce a research-packed, voiceover-ready 10–15 minute script. AI builds the Script Bible and the outline. A **human writer writes the final**. Never let AI write the full script.

---

## Step 3a: Pull 10 competitor transcripts

For the locked niche, identify the top channel's 10 highest-performing videos. For each:

1. Open the video on YouTube
2. Scroll to the description → click **Show Transcript** → **Copy Transcript**
3. Save with title + view count in the header

Alternative at scale: use **vidIQ** Chrome extension to pull transcripts programmatically.

**Output:** Single document with all 10 transcripts, clearly delimited:
```
--- VIDEO 1: "Exact Title" (1,234,567 views) ---
[transcript]

--- VIDEO 2: "Exact Title" (987,654 views) ---
[transcript]
...
```

---

## Prompt 3-1 — Script Bible Generation

**Model:** Claude Opus (1M context preferred — full transcripts are large)
**Input:** 10 competitor transcripts (delimited as above)
**Output:** A reusable "Script Bible" template for this niche

```
Below are 10 full transcripts from top-performing videos in the [NICHE NAME] niche, sourced from the competitor channel [CHANNEL NAME]. Each video's view count is listed with its transcript.

Do a deep, structural analysis and produce a Script Bible — the template of how this niche's winning videos actually work. Cover:

1. Hook structure — the first 30 seconds across all 10 videos. What's the pattern? (Pattern-interrupt, question, bold claim, time-sensitive urgency, etc.)

2. Narrative arc — how does the script progress from hook → body → CTA? Break into typical sections with timing estimates.

3. Research integration — how is data, facts, quotes woven in? What % of script is narration vs. evidence?

4. Tonal register — sentence length, reading level, emotional intensity, authority level. Match to audience.

5. Recurring phrases and transitions — the exact verbal glue this channel uses between sections.

6. Tension + payoff patterns — how does the script keep the viewer from clicking away? Look for open loops, delayed answers, callbacks.

7. CTA patterns — how do they handle "subscribe," "next video," or sponsor integrations? Where in the script?

8. Retention engineering — specific tactics visible in the writing that target retention (drop-offs, re-hooks, visual cues the writer is cueing).

Output the Script Bible as a reusable template that a human script writer could follow for ANY new topic in this niche.

[PASTE 10 TRANSCRIPTS HERE, clearly delimited with "--- VIDEO N: Title (View Count) ---"]
```

**Success criteria:**
- All 8 sections filled with niche-specific specifics (not generic advice)
- Output IS a template (action-oriented) not just an analysis
- "Recurring phrases and transitions" section has actual phrases quoted
- A writer with no prior experience in the niche could write a passable script using this Bible

The Bible is reusable — one Bible per niche, used across all videos in that niche.

---

## Prompt 3-2 — Script Outline from Bible + Title

**Model:** Gemini 2.5 Pro (or Claude — Gemini is better at multi-source research integration)
**Input:** Script Bible + one validated title from Stage 02
**Output:** Detailed script outline (NOT the full script)

```
I have a Script Bible for the [NICHE NAME] niche (pasted below). I need you to write a detailed script OUTLINE for the following video title:

Title: [TITLE HERE]

Do NOT write the full script. Produce an outline only. The outline should include:

1. Hook (first 30 seconds) — specific opening lines + visual cue notes. Match the Script Bible's hook pattern.

2. Section-by-section beats — each section with: section heading, word count target, key points to cover, research/facts to weave in, tension-payoff moment.

3. Research to surface — identify 8–15 specific facts, data points, quotes, or events from your research that MUST be in this script. Cite sources.

4. Transitions — the verbal glue between sections, following the Bible's tone.

5. CTA placement — where and how, matching the Bible's pattern.

6. Estimated runtime — based on word count assuming 150 wpm voiceover pace.

7. Writer's notes — 3–5 bullet points flagging any tricky spots, potential copyright issues, or moments where voiceover delivery matters.

The goal: a script writer should be able to take this outline and produce a publish-ready script in 2–4 hours without additional research.

[PASTE SCRIPT BIBLE HERE]
```

**Success criteria:**
- The outline is NOT a draft script — it's beats + research + notes
- 8–15 specific facts with source citations
- Word count targets per section sum to 1,500–2,200 words total (≈ 10–15 min at 150 wpm)
- Writer's notes flag specific risks (copyright, sensitive topics, complex pronunciations)

---

## Step 3c: Hand off to human script writer

Package three artifacts into a **Script Pack**:
1. Script Bible (from Prompt 3-1)
2. Detailed Outline (from Prompt 3-2)
3. Research notes (the Gemini Deep Research from Stage 02)

Send to the human script writer with a clear deadline (typically 24–48 hours) and the brand voice guide for the channel.

**Writer cost:** $25–$75 per script depending on experience tier.
**Writer output:** 10–15 minute video script (≈ 1,500–2,200 words), VO-ready.

**Why this step is human, not AI:** Scott's hard rule from the workshop — "If you have Claude or Gemini write the full script, you're wasting your time. Quality is garbage. Use AI for the Bible and the outline. Use a human for the final."

---

## Step 3d: Retention QA (optional augmentation)

After the writer returns the final draft, run it through **Subscribr's AI Script Editor**:
- Subscribr analyzes pacing, hook strength, retention triggers, drop-off risks
- Outputs rewrite suggestions for weak sections
- Writer revises based on feedback

This is a quality gate, not a replacement for the writer. Use to catch issues before sending to voiceover.

---

## Alternative QA: Claude hook analysis

If Subscribr isn't available, use Claude:

```
I'll paste a script below. Pretend you're a typical viewer in the [AUDIENCE PROFILE] demographic.

For the first 60 seconds of the script:
1. Identify each moment a viewer would be tempted to click away. Quote the exact line and explain why.
2. Rate the hook strength on a 1–10 scale with specific reasoning.
3. Rewrite the first 30 seconds in 3 variations, each testing a different hook approach (curiosity, urgency, contrarian take).
4. Flag any confusing, slow, or low-stakes moments in the opening that would cause drop-off.

[PASTE SCRIPT HERE]
```

---

## Output deliverable: Final Script

The Stage 03 hand-off to Stage 04 (voiceover), Stage 05 (thumbnails), and Stage 06 (B-roll) — runs in parallel:

```yaml
title: "..."
working_title_variants:
  - "..."
  - "..."
  - "..."
script_file: "[path to .md or .txt]"
word_count: ...
estimated_runtime: "11:30"
writer: "[name]"
revision_round: 1
retention_qa_passed: true | false
strategist_approval: "[name] [date]"
notes_for_voiceover:
  - "..."
notes_for_editor:
  - "..."
notes_for_thumbnail_designer:
  - "..."
```

This goes to VO (Stage 04), Thumbnail (Stage 05), and B-Roll (Stage 06) in parallel.
