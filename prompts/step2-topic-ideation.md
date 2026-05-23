# Step 2 Prompts — Topic Ideation (The 4-Prompt Loop)

> Goal: Generate 5 validated, data-backed video topics — no guessing, no wasted production spend on dud videos.

This is the core ideation loop: **Claude → Claude → Gemini → Claude**, then human Google Trends verification.

---

## Prompt 2-1 — Channel Data Extraction

**Model:** Claude (with screenshot capability — Claude Pro or Max with Chrome extension)
**Input:** Screenshot of competitor channel's Videos tab (40 most recent uploads)
**Output:** Clean markdown table of 40 videos

```
I've attached a screenshot of the [NICHE] top channel's Videos tab showing the 40 most recent uploads.

Create a clean markdown table of the 40 most recent videos including:
| # | Video Title | View Count | Upload Date |

Extract every row visible in the screenshots (I'll attach more if needed). Preserve exact titles including emojis and punctuation. Express view counts as numbers (e.g., 1,200,000 not "1.2M").

If any data is unclear or missing in the screenshot, flag it with [UNCLEAR] rather than guessing.
```

**Success criteria:**
- 40 rows in the table (or as many as visible in screenshot)
- No hallucinated data — `[UNCLEAR]` flag used where source is illegible
- Exact title preservation

---

## Prompt 2-2 — Title Pattern Analysis

**Model:** Claude
**Input:** The table from Prompt 2-1
**Output:** Structural analysis of what's winning and why

```
Below is a table of the 40 most recent videos from a top channel in the [NICHE] niche, including titles, view counts, and upload dates.

Do a deep analysis and provide:

1. Top-performing title patterns — videos with view counts at least 2× the channel median. What recurring structures, words, hooks, number usage, emotional triggers, curiosity gaps do they share?

2. Underperforming title patterns — videos at or below 0.5× the median. What's failing? Why?

3. Topic themes — cluster the 40 videos into 5–7 topic themes. Which themes perform best and which flop?

4. Hook word frequency — list the 15 most frequent meaningful words/phrases in titles and their correlation with view count.

5. Upload timing patterns — is there any day-of-week or recency signal in the performance?

6. Final takeaways — 5 rules this channel is clearly following, and 3 gaps they're leaving on the table that a new entrant could exploit.

Be specific and data-backed. No generic advice.

[PASTE CHANNEL DATA TABLE HERE]
```

**Success criteria:**
- All 6 sections completed with specific data references
- "Gaps" section identifies actual gaps, not weaknesses (different thing)
- Recommendations specific to this niche, not transferable advice

---

## Prompt 2-3 — Build the Gemini Research Prompt

**Model:** Claude
**Input:** The niche analysis from Prompt 2-2
**Output:** A 150–300 word research prompt formatted for Gemini Deep Research

```
Based on the niche analysis we just did on [NICHE NAME], write me a sharp, specific research prompt I can paste into Gemini Deep Research. The goal is to surface:
- The 15–20 most relevant trending topics in this niche right now (last 90 days)
- Any news, releases, events, or cultural moments that could drive topical videos
- Recent breakthroughs, controversies, or debates in the space
- Upcoming calendar events in the next 60 days worth content-ing around
- 5 angles or perspectives on the niche that aren't yet saturated on YouTube

The prompt should be 150–300 words, specific to [NICHE NAME], and explicitly request source citations. Do NOT include generic language that would work for any niche.

Return only the prompt, nothing else — it'll go directly into Gemini.
```

**Success criteria:**
- Output is ONLY the prompt (no Claude commentary)
- 150–300 words
- Niche-specific language throughout

---

## Step: Run Gemini Deep Research

Paste Claude's output prompt into **Gemini Deep Research** (Gemini Advanced subscription required). Let it run end-to-end (typically 5–10 minutes for deep research mode). Return with the full output document.

---

## Prompt 2-4 — Topic Ranking

**Model:** Claude (1M context Opus preferred for full Gemini doc ingestion)
**Input:** Gemini's full research output
**Output:** 5 ranked topic recommendations

```
Below is Gemini Deep Research's output on the [NICHE NAME] niche. Our goal: identify the 5 video topics most likely to perform on YouTube for a new channel in this space.

Analyze all of this research and give me 5 ranked topic recommendations. For each:

1. Topic — the working title framing
2. Why it wins — specific signal in the research that points to demand
3. Target search intent — what viewer is looking for
4. Difficulty — is this saturated, under-covered, or wide-open?
5. Estimated view ceiling — based on comparable videos in the research
6. Evergreen vs. timely — will this age well or is it a 90-day window?
7. Suggested 3 title variations — different hooks for A/B consideration

Rank #1 through #5 with #1 being highest priority. End with a note on which 2 we should prioritize publishing FIRST based on urgency vs. quality.

[PASTE GEMINI RESEARCH HERE]
```

**Success criteria:**
- 5 distinct topics (no near-duplicates)
- Every topic has all 7 attributes
- Title variations are genuinely different hooks, not paraphrases
- Final note picks 2 priority topics with reasoning

---

## Manual gate: Google Trends verification (NON-NEGOTIABLE)

For each of the 5 ranked topics:

1. Go to trends.google.com
2. Search the topic
3. Filter: `United States` · `Past 12 months` · `YouTube Search`
4. Classify: rising / stable / declining
5. Compare all 5 side-by-side using "Compare" feature
6. **KILL any topic that's flat or declining** (unless truly evergreen — rare exception)
7. Screenshot results for the Topic Brief

Without this step, you will pay $75 to produce videos that never get watched. This is the highest-leverage 15 minutes in the entire pipeline.

---

## Output deliverable: Topic Brief

The Stage 02 hand-off to Stage 03 is a "Topic Brief" doc containing:

```yaml
niche: "..."
week_of: "YYYY-MM-DD"
topics_locked:
  - position: 1
    working_title: "..."
    title_variations:
      - "..."
      - "..."
      - "..."
    why_it_wins: "..."
    search_intent: "..."
    difficulty: "saturated | under-covered | wide-open"
    view_ceiling_estimate: ...
    timely_vs_evergreen: "..."
    google_trends_status: "rising | stable"
    google_trends_screenshot: "[path or link]"
  - position: 2
    ...
strategist_approval: "[name] [date]"
```

This brief is the input to Stage 03 (Script Creation).
