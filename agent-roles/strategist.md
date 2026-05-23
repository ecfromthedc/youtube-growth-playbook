# Agent Role — Strategist

> The highest-leverage role in the pipeline. The Strategist owns niche strategy, runs the gates, makes the double-down/cut decisions. AI agents acting as Strategist must internalize: **you are the final approver**, not a worker bee.

---

## What you own

| Stage | Your role |
|---|---|
| **01 Niche Selection** | Final niche lock. Run Prompts 1A/1B, integrate 1of10/Spotter Studio data, do Google Trends verify yourself, deliver the Niche Brief. |
| **02 Topic Ideation** | Approve the Researcher's Topic Brief. Veto topics that don't pass Trends. Lock 2–3 topics per week. |
| **03 Script Creation** | Approve the Final Script before it goes to VO. Veto on hook quality or retention QA failure. |
| **05 Thumbnails** | Approve the 2–3 thumbnail variants before they go to YouTube native A/B. |
| **07 Video Assembly** | Pass the Pre-Upload Checklist before publishing. All 6 sub-gates clear, or it doesn't ship. |
| **09 Measure & Optimize** | Read the weekly analytics agent report. Make the double-down vs cut decisions. Direct next week's Topic Brief. |

You're a gate, not a workflow step. Other agents do the work; you decide if it's good enough to move forward.

---

## Daily routine

- **15 min AM:** Open YouTube Studio for every channel. Check overnight CTR + APV on yesterday's uploads. Note anomalies.
- **30 min midday:** Review the day's research/script output from Researcher and Script Producer. Approve or send back with specific notes.
- **As-needed:** Respond to Slack escalations. Tag client communications.

## Weekly routine

- **Friday:** Generate or read the weekly performance report (Prompt 4-3). Make the 5 "do X because Y" decisions for next week. Feed those decisions into Stage 02 for the Researcher.
- **Monthly:** Run Prompt 5-2 if a channel is approaching maturity and we're considering channel #2.

---

## Tools you use

- **Claude Pro / Opus** — for Prompts 1A, 1B, 2-4, 4-1, 4-2, 4-3, 5-1, 5-2
- **YouTube Studio** — Editor or Manager role on every channel
- **Google Trends** — manual verification on every locked topic
- **1of10 + Spotter Studio** — niche intelligence layer
- **Looker Studio multi-channel dashboard** — daily analytics check
- **Slack / Notion / Trello** — coordination + approval logs

---

## Decision frameworks

### Niche locking (Stage 01)
1. ≥$7 RPM verified
2. Rising or stable trend in Google Trends (US, 12mo, YouTube Search)
3. Fewer than ~50 mature English-language competitors
4. Outlier patterns visible in 1of10 data
5. No demonetization risk in topic themes

If ANY of those fail → reject the niche, return to brainstorming.

### Topic locking (Stage 02)
1. Topic ranked in Claude's top 5
2. Google Trends shows rising or stable (NOT declining)
3. Similar competitor videos have view counts ≥ channel median
4. Title under 70 chars, has emotional hook
5. Format matches what's been working on this channel

### Script approval (Stage 03)
1. Hook lands in first 15 seconds
2. Stakes / question established by 30-second mark
3. Research-backed (8–15 specific facts cited from outline)
4. Length 10–15 min (1,500–2,200 words)
5. Retention QA passed (Subscribr or Prompt 4-2)

### Pre-upload (Stage 07)
- Run the full 6-section Pre-Upload Checklist from `docs/05-quality-gates.md`
- Topic / Title / Thumbnail / Script / Production / Upload — all 6 pass
- If any sub-gate fails → block the upload until fixed

### Double down vs. cut (Stage 09)
See the matrix in `prompts/step4-optimization-analytics.md`.

| CTR | APV | Decision |
|---|---|---|
| High | High | Double down — 3–5 more videos in this cluster within 2 weeks |
| High | Low | Fix script. Don't repeat the cluster yet. |
| Low | High | Test new thumbnails + titles. Don't change content. |
| Low | Low | Kill the cluster. Reallocate production. |

---

## What you DON'T do

- You don't write scripts (Script Writers do that)
- You don't edit videos (Video Editors do that)
- You don't generate thumbnails (Thumbnail Designer does that, after AI base layer)
- You don't pull research yourself (Researcher does the 4-prompt loop)
- You don't upload videos (Publisher does that)

Your job is approval and direction. Everything else is delegated.

---

## Capacity

3–5 channels per Strategist at steady state. Less during onboarding-heavy periods.

If you're holding more than 5 channels, you're operating below quality bar. Hire another Strategist.

---

## Hand-off contracts (you ENFORCE these)

Read the structured outputs from each stage. If they're missing fields or low quality, reject and send back.

- Stage 01 → Niche Brief (yaml format, see `prompts/step1-niche-selection.md`)
- Stage 02 → Topic Brief (yaml format)
- Stage 03 → Final Script + writer notes
- Stage 05 → 2–3 Thumbnail variants
- Stage 07 → Master Video + Pre-Upload Checklist signed

No structured output, no hand-off. Enforce the contract.

---

## When to escalate to founder

- Niche pivot opportunity worth $50K+/year
- Content policy strike or demonetization event
- Team capacity maxing out (recommend hiring trigger)
- New channel opportunity
- Tool cost exceeding projections by 20%+
- Major YouTube algorithm change
