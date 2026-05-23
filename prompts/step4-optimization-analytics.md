# Step 4 Prompts — Optimization &amp; Analytics

> Goal: Diagnose underperforming videos fast (within 48 hours of upload), iterate on what's working, kill what's not. The Scott Smith metrics — CTR ≥10%, APV ≥30% — drive every decision.

---

## Prompt 4-1 — CTR Diagnostic

**Model:** Claude
**When to run:** 48 hours after upload, if CTR or APV is below threshold
**Input:** Video metadata + 48-hour analytics
**Output:** Diagnosis + specific fixes

```
One of our videos on [CHANNEL NAME] is underperforming. Here are the details:

- Video title: [TITLE]
- Current thumbnail: [DESCRIPTION or attach image]
- Topic: [TOPIC]
- Target audience: [AUDIENCE PROFILE]
- After 48 hours:
  - Impressions: [N]
  - CTR: [N]%
  - APV: [N]%
  - Audience retention graph: [PASTE OR DESCRIBE]

Analyze and give me:

1. Diagnosis — Is this primarily a CTR problem, APV problem, or both? What's the specific failure mode?

2. Hypotheses — 3 specific reasons this underperformed. Rank by likelihood.

3. Fixes — For each hypothesis, what's the specific fix? (New title? New thumbnail? Script restructure for the next video in this cluster?)

4. 3 new title variations and 2 new thumbnail concepts to test

5. Decision call — is this video worth republishing with a new thumbnail/title, or abandon and move on?

Be specific. No generic "improve the hook" advice.
```

**Success criteria:**
- Diagnosis is specific (CTR vs APV vs both, with the actual failure mode named)
- 3 hypotheses ranked by likelihood, not just listed
- Fixes are actionable (not "test new thumbnails" — specific concepts)
- Final decision is clear: republish or abandon

---

## Prompt 4-2 — Hook Analysis

**Model:** Claude
**When to run:** Pre-publish QA OR post-publish if APV is low
**Input:** Full script (or first 60 seconds for quick analysis)
**Output:** Click-away moments + hook strength rating + 3 hook rewrites

```
I'll paste a script below. Pretend you're a typical viewer in the [AUDIENCE PROFILE] demographic.

For the first 60 seconds of the script:
1. Identify each moment a viewer would be tempted to click away. Quote the exact line and explain why.
2. Rate the hook strength on a 1–10 scale with specific reasoning.
3. Rewrite the first 30 seconds in 3 variations, each testing a different hook approach (curiosity, urgency, contrarian take).
4. Flag any confusing, slow, or low-stakes moments in the opening that would cause drop-off.

[PASTE SCRIPT HERE]
```

**Success criteria:**
- Specific lines quoted as click-away moments
- 3 rewrites that are genuinely different hook approaches (not paraphrases)
- Hook strength rating includes reasoning, not just a number

---

## Prompt 4-3 — Weekly Channel Analytics Review

**Model:** Claude
**When to run:** Every Friday (or scheduled cron)
**Input:** YouTube Analytics export (CSV or screenshot) for the week
**Output:** 400–600 word memo with 5 actionable next-week decisions

```
Below is a screenshot / data export of this week's analytics for [CHANNEL NAME].

Do a full analytical review and return:

1. Performance summary — the 3 most important numbers and what they mean
2. Winners and losers — which videos overperformed and which flopped, with view counts + key metrics
3. Pattern recognition — any emerging patterns in what's working (topics, title structures, thumbnail styles, runtime)
4. Red flags — anything concerning (CTR decline, audience retention drop, subscriber churn, traffic source shifts)
5. Opportunities — based on the data, what should we double down on next week?
6. Recommended actions — 5 specific, actionable decisions for the next 7 days. Format: "Do X because Y."

Write the report as a memo — clear, confident, not hedged. 400–600 words.

[PASTE ANALYTICS DATA HERE]
```

**Success criteria:**
- 5 "Do X because Y" actions are concrete, week-1 executable
- Patterns identified are evidence-backed (specific video examples)
- Tone is decisive — no "we should consider" or "it might be worth"

---

## Augmentation: Automated weekly review

Build a Claude Code skill that:
1. Pulls YouTube Analytics API exports for all channels Monday morning
2. Auto-runs Prompt 4-3 on each
3. Posts the weekly report to a Slack channel or Notion
4. Tags the Strategist for review

This saves the Strategist ~2 hours/week per channel.

---

## The CTR / APV Diagnostic Matrix (memorize)

| CTR | APV | Diagnosis | Action |
|---|---|---|---|
| ≥10% | ≥30% | **Winning** — clicking + staying | Make more videos in this exact cluster within 2 weeks |
| ≥10% | <30% | **Script problem** — clicking but bouncing | Fix the first 30 seconds. Re-script future videos in the cluster |
| <10% | ≥30% | **Packaging problem** — not clicking, but staying | New thumbnails + title variants. Content is fine |
| <10% | <30% | **Wrong topic** — not clicking AND not staying | Topic mismatch for this channel. Rethink |

When both metrics improve → that's a hit. The portfolio principle says 3 of 22 videos drive 90% of revenue. Find them, double down.

---

## When to double down vs. cut the fat

### Double down signals
- CTR consistently ≥8% across a topic cluster
- APV consistently ≥35% on a specific format
- One video from a cluster got 3× channel median views
- Audience retention graph shows viewers binge-watching multiple videos in a series

**Action:** Make 3–5 more videos in the same cluster/format within 2 weeks. Capture algorithmic momentum.

### Cut the fat signals
- Topic cluster averaging <5% CTR after 4+ attempts
- Specific format consistently underperforming
- Audience retention plateaus low even with script iterations
- Zero subscriber conversion from a topic area

**Action:** Stop making content in that cluster. Reallocate production capacity.

---

## Output deliverable: Weekly Report

The Stage 09 output that loops back to Stage 02 (Topic Ideation) for next week:

```yaml
week_of: "YYYY-MM-DD"
channel: "..."
top_line:
  views: ...
  watch_hours: ...
  subscribers_gained: ...
  channel_ctr: ...
  channel_apv: ...
winners:
  - video: "..."
    views: ...
    ctr: ...
    apv: ...
    why: "..."
losers:
  - video: "..."
    views: ...
    ctr: ...
    apv: ...
    diagnosis: "..."
patterns_emerging:
  - "..."
red_flags:
  - "..."
next_week_decisions:
  - action: "..."
    rationale: "..."
strategist_signoff: "[name] [date]"
```

This feeds Stage 02 for the next week's Topic Brief.
