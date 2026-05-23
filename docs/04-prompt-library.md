# Prompt Library — Ready To Copy & Paste

These are the prompts for the 5-step system. I've written them based on Scott's workflow with your team's quality standards layered on top. Test and iterate on live channels — these are v1.

All prompts assume **Claude 4.5 Opus or Sonnet** (whichever is current best). Adjust model selection if behavior changes.

---

## STEP 1 PROMPTS: Niche Selection

### Prompt 1A — High-RPM Niche Brainstorm (Claude)

```
I'm planning to build a faceless long-form YouTube channel for a client. The goal is to land in a niche with:
- Minimum $7 RPM (US audience, long-form video)
- Rising or stable demand (not declining)
- Fewer than 50 mature English-language channels in the space
- Evergreen appeal (still valuable in 3–5 years)
- Not overly reliant on the operator being on-camera

Give me 20 niche candidates ranked by your estimate of RPM × demand × gap. For each, give:
- Niche name + 2-line description
- Estimated RPM range (low, likely, high)
- Top 3 competitor channels in that niche, with rough subscriber count
- 2 reasons this niche has a gap
- 2 risks or concerns

After the list, tell me which 3 you'd prioritize investigating further and why.
```

### Prompt 1B — Niche Deep-Dive Validation (Claude)

```
I'm evaluating [NICHE NAME] as a faceless long-form YouTube channel opportunity. 

Do a deep analysis covering:
1. Audience profile (demographics, geography, income proxy, buying intent)
2. Advertiser categories that target this audience and typical CPMs
3. Top 10 channels in this niche with subscriber counts and estimated monthly revenue
4. Content formats that work in this niche (interview, explainer, ranking, news, etc.)
5. Content formats that fail in this niche
6. Seasonal or cyclical patterns
7. Overlapping adjacent niches we could expand into later
8. Red flags (copyright risks, advertiser-unfriendly topics, demonetization risks, bot-farmed channels)

End with: "GO / CONSIDER / SKIP" with a 2-sentence verdict.
```

---

## STEP 2 PROMPTS: Video Ideation (The 4-Prompt Core Loop)

### Prompt 2-1 — Channel Data Extraction (Claude, with screenshot)

```
I've attached a screenshot of the [NICHE] top channel's Videos tab showing the 40 most recent uploads.

Create a clean markdown table of the 40 most recent videos including:
| # | Video Title | View Count | Upload Date |

Extract every row visible in the screenshots (I'll attach more if needed). Preserve exact titles including emojis and punctuation. Express view counts as numbers (e.g., 1,200,000 not "1.2M").

If any data is unclear or missing in the screenshot, flag it with [UNCLEAR] rather than guessing.
```

### Prompt 2-2 — Title Pattern Analysis (Claude)

```
Below is a table of the 40 most recent videos from a top channel in the [NICHE] niche, including titles, view counts, and upload dates.

Do a deep analysis and provide:

1. **Top-performing title patterns** — look at videos with view counts at least 2× the channel median. What recurring structures, words, hooks, number usage, emotional triggers, curiosity gaps do they share?

2. **Underperforming title patterns** — videos at or below 0.5× the median. What's failing? Why?

3. **Topic themes** — cluster the 40 videos into 5–7 topic themes. Which themes perform best and which flop?

4. **Hook word frequency** — list the 15 most frequent meaningful words/phrases in titles and their correlation with view count.

5. **Upload timing patterns** — is there any day-of-week or recency signal in the performance?

6. **Final takeaways** — 5 rules this channel is clearly following, and 3 gaps they're leaving on the table that a new entrant could exploit.

Be specific and data-backed. No generic advice.

[PASTE CHANNEL DATA TABLE HERE]
```

### Prompt 2-3 — Build the Gemini Research Prompt (Claude)

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

### → Gemini Deep Research

Paste Claude's prompt into Gemini Deep Research. Let it run. Return with results.

### Prompt 2-4 — Topic Ranking from Gemini Research (Claude)

```
Below is Gemini Deep Research's output on the [NICHE NAME] niche. Our goal: identify the 5 video topics most likely to perform on YouTube for a new channel in this space.

Analyze all of this research and give me 5 ranked topic recommendations. For each:

1. **Topic** — the working title framing
2. **Why it wins** — specific signal in the research that points to demand
3. **Target search intent** — what viewer is looking for
4. **Difficulty** — is this saturated, under-covered, or wide-open?
5. **Estimated view ceiling** — based on comparable videos in the research
6. **Evergreen vs. timely** — will this age well or is it a 90-day window?
7. **Suggested 3 title variations** — different hooks for A/B consideration

Rank #1 through #5 with #1 being highest priority. End with a note on which 2 we should prioritize publishing FIRST based on urgency vs. quality.

[PASTE GEMINI RESEARCH HERE]
```

### Google Trends Verification (Human Workflow, No Prompt)

For each of the 5 topics:
1. Go to trends.google.com
2. Search the topic
3. Filter: `United States` | `Past 12 months` | `YouTube Search`
4. Check: rising / stable / declining
5. Compare all 5 side-by-side using Google Trends' "Compare" feature
6. **Kill any topic that's flat or declining (unless truly evergreen)**
7. Screenshot results for the Topic Brief

---

## STEP 3 PROMPTS: Script Creation

### Prompt 3-1 — Script Bible Generation (Claude)

```
Below are 10 full transcripts from top-performing videos in the [NICHE NAME] niche, sourced from the competitor channel [CHANNEL NAME]. Each video's view count is listed with its transcript.

Do a deep, structural analysis and produce a **Script Bible** — the template of how this niche's winning videos actually work. Cover:

1. **Hook structure** — the first 30 seconds across all 10 videos. What's the pattern? (Pattern-interrupt, question, bold claim, time-sensitive urgency, etc.)

2. **Narrative arc** — how does the script progress from hook → body → CTA? Break into typical sections with timing estimates.

3. **Research integration** — how is data, facts, quotes woven in? What % of script is narration vs. evidence?

4. **Tonal register** — sentence length, reading level, emotional intensity, authority level. Match to audience.

5. **Recurring phrases and transitions** — the exact verbal glue this channel uses between sections.

6. **Tension + payoff patterns** — how does the script keep the viewer from clicking away? Look for open loops, delayed answers, callbacks.

7. **CTA patterns** — how do they handle "subscribe," "next video," or sponsor integrations? Where in the script?

8. **Retention engineering** — specific tactics visible in the writing that target retention (drop-offs, re-hooks, visual cues the writer is cueing).

Output the Script Bible as a reusable template that a human script writer could follow for ANY new topic in this niche.

[PASTE 10 TRANSCRIPTS HERE, clearly delimited with "--- VIDEO N: Title (View Count) ---"]
```

### Prompt 3-2 — Script Outline from Bible + Title (Gemini)

```
I have a Script Bible for the [NICHE NAME] niche (pasted below). I need you to write a detailed script OUTLINE for the following video title:

**Title:** [TITLE HERE]

Do NOT write the full script. Produce an outline only. The outline should include:

1. **Hook (first 30 seconds)** — specific opening lines + visual cue notes. Match the Script Bible's hook pattern.

2. **Section-by-section beats** — each section with: section heading, word count target, key points to cover, research/facts to weave in, tension-payoff moment.

3. **Research to surface** — identify 8–15 specific facts, data points, quotes, or events from your research that MUST be in this script. Cite sources.

4. **Transitions** — the verbal glue between sections, following the Bible's tone.

5. **CTA placement** — where and how, matching the Bible's pattern.

6. **Estimated runtime** — based on word count assuming 150 wpm voiceover pace.

7. **Writer's notes** — 3–5 bullet points flagging any tricky spots, potential copyright issues, or moments where voiceover delivery matters.

The goal: a script writer should be able to take this outline and produce a publish-ready script in 2–4 hours without additional research.

[PASTE SCRIPT BIBLE HERE]
```

---

## STEP 4 PROMPTS: Optimization + Analytics

### Prompt 4-1 — CTR Diagnostic (Claude)

```
One of our videos on [CHANNEL NAME] is underperforming. Here are the details:

- **Video title:** [TITLE]
- **Current thumbnail:** [DESCRIPTION or attach image]
- **Topic:** [TOPIC]
- **Target audience:** [AUDIENCE PROFILE]
- **After 48 hours:**
  - Impressions: [N]
  - CTR: [N]%
  - APV: [N]%
  - Audience retention graph: [PASTE OR DESCRIBE]

Analyze and give me:

1. **Diagnosis** — Is this primarily a CTR problem, APV problem, or both? What's the specific failure mode?

2. **Hypotheses** — 3 specific reasons this underperformed. Rank by likelihood.

3. **Fixes** — For each hypothesis, what's the specific fix? (New title? New thumbnail? Script restructure for the next video in this cluster?)

4. **3 new title variations** and **2 new thumbnail concepts** to test

5. **Decision call** — is this video worth republishing with a new thumbnail/title, or abandon and move on?

Be specific. No generic "improve the hook" advice.
```

### Prompt 4-2 — Hook Analysis (Claude)

```
I'll paste a script below. Pretend you're a typical viewer in the [AUDIENCE PROFILE] demographic.

For the first 60 seconds of the script:
1. Identify each moment a viewer would be tempted to click away. Quote the exact line and explain why.
2. Rate the hook strength on a 1–10 scale with specific reasoning.
3. Rewrite the first 30 seconds in 3 variations, each testing a different hook approach (curiosity, urgency, contrarian take).
4. Flag any confusing, slow, or low-stakes moments in the opening that would cause drop-off.

[PASTE SCRIPT HERE]
```

### Prompt 4-3 — Weekly Channel Analytics Review (Claude)

```
Below is a screenshot / data export of this week's analytics for [CLIENT CHANNEL NAME].

Do a full analytical review and return:

1. **Performance summary** — the 3 most important numbers and what they mean
2. **Winners and losers** — which videos overperformed and which flopped, with view counts + key metrics
3. **Pattern recognition** — any emerging patterns in what's working (topics, title structures, thumbnail styles, runtime)
4. **Red flags** — anything concerning (CTR decline, audience retention drop, subscriber churn, traffic source shifts)
5. **Opportunities** — based on the data, what should we double down on next week?
6. **Recommended actions** — 5 specific, actionable decisions for the next 7 days. Format: "Do X because Y."

Write the report as a client-facing memo — clear, confident, not hedged. 400–600 words.

[PASTE ANALYTICS DATA HERE]
```

---

## STEP 5 PROMPTS: Monetization + Scaling

### Prompt 5-1 — YPP Application Readiness Check (Claude)

```
Our channel [CHANNEL NAME] is approaching YouTube Partner Program eligibility. Current stats:
- Subscribers: [N]
- Watch hours (last 12 months): [N]
- Total videos: [N]
- Channel age: [N months]

Give me a YPP readiness audit:
1. **Technical eligibility** — are we meeting thresholds? When will we if not yet?
2. **Content policy audit** — based on our content themes, are there any demonetization risks? Any adult themes, copyright issues, "limited ads" risks?
3. **Community guidelines check** — anything that could block approval?
4. **Channel setup audit** — is the about page, banner, channel trailer all optimized?
5. **Pre-application checklist** — 10 items to complete before clicking "apply"

Be specific about what we need to do before applying so we don't get rejected.
```

### Prompt 5-2 — Channel #2 Niche Evaluation (Claude)

```
We have an established channel at [CHANNEL NAME] in the [NICHE] niche, now making $[N]/month.

We're ready to launch a second channel. Our team is experienced with [EXISTING NICHE] workflows. Evaluate the following candidate niches for our second channel based on:

- **Learning curve leverage** — can we reuse our existing skills or do we have to start over?
- **Audience overlap** — does it tap similar audiences we could cross-promote to?
- **Team capacity** — can our existing team handle this without doubling cost?
- **RPM + scale potential**
- **Risk diversification** — does this de-risk our portfolio vs. doubling down?

Candidate niches:
1. [NICHE A]
2. [NICHE B]
3. [NICHE C]

Rank them and recommend which to launch, which to hold, which to skip. Give a 90-day launch plan for the recommended one.
```

---

## Prompt Maintenance

- Store master copies of all prompts in **Notion → your team YouTube Arm → Prompt Library**
- Version each prompt (v1, v2 after significant rewrites)
- Log outcomes: every time we run a prompt on a real channel, note the result → use data to iterate
- **Monthly review:** Strategist + Researcher review which prompts are producing great output vs. mediocre; refine or rewrite as needed.
