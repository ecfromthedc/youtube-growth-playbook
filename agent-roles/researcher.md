# Agent Role — Researcher / Ideation Specialist

> The pipeline's data engine. The Researcher runs the 4-prompt loop, pulls competitor data, verifies in Google Trends, and delivers the Topic Brief that drives every video produced. AI-heavy role — most of the work is prompt execution + verification.

---

## What you own

| Stage | Your role |
|---|---|
| **01 Niche Selection** | Support the Strategist with data lookups (1of10 outlier patterns, Spotter channel intel). |
| **02 Topic Ideation** | **Primary owner.** Run the full 4-prompt loop (Claude → Claude → Gemini → Claude), verify topics in Google Trends, produce the Topic Brief. |

That's it. You're tight, deep, and you live in the prompt library.

---

## Weekly deliverable: Topic Brief

For each channel you cover, one Topic Brief per week containing:
- 10 validated topics (from 20+ candidates Claude generated)
- Google Trends screenshot per topic
- Competitor videos that performed on similar topics (with view counts)
- Recommended title variations per topic
- Strategist's top 5 ranked (delivered after the 4-prompt run)

Format: yaml structure documented in `prompts/step2-topic-ideation.md`.

---

## Daily routine

- **Monday 8 AM:** Pull analytics from every channel you cover. Post summary to Slack `#yt-analytics`.
- **Monday 10 AM:** Begin research sprint for the week's videos. Run the 4-prompt loop per channel.
- **Monday afternoon:** Deliver Topic Briefs to Strategists for approval.
- **Tuesday–Friday:** Available for ad-hoc research requests. Re-run prompts if Strategist rejects a topic.

---

## Tools you use

- **Claude Pro** — for Prompts 2-1, 2-2, 2-3, 2-4 (the 4-prompt core loop)
- **Claude Chrome extension** — for screenshot-to-paste workflow on competitor channel scraping (this is why Pro tier matters)
- **Gemini Advanced (Deep Research mode)** — for the deep niche research between Prompts 2-3 and 2-4
- **Google Trends** — for the manual verification gate on every topic
- **vidIQ** — for competitor transcript pulling and tag analysis (the tag hack from Stage 05)
- **1of10 + Spotter Studio** — for cross-checking Claude's outputs against real outlier data
- **Notion / shared workspace** — to file Topic Briefs for Strategist review

---

## The 4-prompt loop (your core workflow)

This is your bread and butter. Reference: `prompts/step2-topic-ideation.md`.

### Step 1: Channel Data Extraction (Claude)
1. Screenshot the top competitor channel's Videos tab (40 most recent uploads)
2. Paste into Claude with Prompt 2-1
3. Get back: clean markdown table of 40 videos with titles, views, dates
4. Verify: every row has data, `[UNCLEAR]` flags on any illegible source

### Step 2: Title Pattern Analysis (Claude)
1. Feed the table from Step 1 into Claude with Prompt 2-2
2. Get back: top-performing patterns, underperformers, topic clusters, hook word frequency, gaps to exploit
3. Verify: analysis is specific to this niche, not generic advice

### Step 3: Build Gemini Research Prompt (Claude)
1. Feed the analysis from Step 2 into Claude with Prompt 2-3
2. Get back: a 150–300 word research prompt specifically tailored for this niche
3. Verify: output is ONLY the prompt (no Claude commentary)

### Step 4: Run Gemini Deep Research
1. Paste Claude's prompt into Gemini Deep Research
2. Let it run end-to-end (5–10 minutes typical)
3. Capture the full research output

### Step 5: Topic Ranking (Claude)
1. Feed Gemini's research into Claude with Prompt 2-4
2. Get back: 5 ranked topic recommendations with title variations, difficulty, view ceiling, evergreen vs timely classification
3. Verify: 5 distinct topics, no near-duplicates, full attributes per topic

### Step 6: Manual Google Trends verification
1. For each of the 5 topics, search Google Trends
2. Filter: US · Past 12 months · YouTube Search
3. Classify each: rising / stable / declining
4. Kill anything flat or declining (unless truly evergreen)
5. Compare side-by-side using the "Compare" feature
6. Screenshot results for the Topic Brief

### Step 7: Deliver the Topic Brief
1. Compile the yaml-structured Topic Brief
2. Send to Strategist via Notion or Slack
3. Wait for approval
4. If Strategist rejects → understand why → re-run from Step 5 with adjusted inputs

---

## Capacity

6–10 channels per Researcher. The work is largely AI-powered; the bottleneck is verification + curation, not execution.

If you're holding more than 10 channels, output quality drops. The Strategist will start rejecting Topic Briefs and the pipeline backs up.

---

## What you DON'T do

- You don't lock the niche (Strategist does)
- You don't write scripts or outlines (Script Producer does)
- You don't make double-down decisions (Strategist does after weekly report)
- You don't change the prompts in the library without team review (prompts are versioned)

---

## Quality bar

Every Topic Brief must:
- Have all 5 topics validated in Google Trends (with screenshots)
- Cite specific competitor videos with view counts
- Provide 3 title variations per topic
- Score difficulty (saturated / under-covered / wide-open)
- Estimate view ceiling based on competitor data

Topic Briefs missing these get rejected. No exceptions.

---

## Hand-off contract

Your output (Topic Brief) goes to the Script Producer, who runs Stage 03 on the locked titles. The Script Producer's Script Bible work depends on the title quality you ship.

If you deliver weak titles → Script Bible misses → final scripts underperform → CTR/APV miss → entire week of production is wasted.

The 4-prompt loop is the foundation. Don't skip steps. Don't paraphrase prompts.
