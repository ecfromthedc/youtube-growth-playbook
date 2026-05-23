# Agent Role — Publisher / Coordinator

> Publisher owns Stages 08 (publish + test) and 10 (repurpose). High-leverage low-skill role — best place for a junior hire or AI agent. One Publisher can comfortably handle 20+ channels because the AI does the work.

---

## What you own

| Stage | Your role |
|---|---|
| **08 Publish & Test** | Upload to YouTube Studio. Set title, description, hashtags, tags. Run native A/B test. Schedule publish for audience time zone. |
| **10 Repurpose** | Run Clipify on every master video. Review the 3 vertical clips. Schedule across TikTok / IG Reels / YT Shorts via Postiz. |

---

## Workflow: Stage 08 — Publish &amp; Test

### Step 1: Upload to YouTube Studio

1. Master video file from Editor (Stage 07)
2. Upload to channel's YouTube Studio
3. Set:
   - **Title** — locked title from Strategist approval (NOT a paraphrase)
   - **Description** — first 3 lines hook + summary; remaining 2,000 chars structured (timestamps, links, hashtags at top)
   - **Hashtags** — 3–5 at the TOP of the description (clickable, drives discovery)
   - **Video tags** — pulled from vidIQ tag analysis of competitor videos in same niche (the tags hack)
   - **Category** — appropriate YouTube category
   - **Playlist** — assigned to channel's relevant playlist

### Step 2: Configure the thumbnail A/B test

1. Upload all 2–3 thumbnail variants from Stage 05
2. Enable YouTube's native **Test &amp; Compare** feature
3. YouTube will rotate them across impressions and lock the winner after statistical significance

### Step 3: Configure cross-channel A/B testing (TubeBuddy)

1. Open TubeBuddy Legend
2. Set up A/B test for title variations (if multiple worth testing)
3. Set up A/B test for description variations
4. TubeBuddy tracks CTR + watch time per variant

### Step 4: Schedule publish

- **US audiences:** 4–9 PM ET is prime time
- **International:** match audience time zone (use channel's analytics geo data)
- **Day of week:** typically Tuesday / Thursday for highest organic reach (test per channel)
- Use YouTube's scheduled publish feature

### Step 5: Set end screen + cards

- End screen: subscribe + next video thumbnails in last 20 seconds
- Cards: 2–3 strategically placed to surface related videos

### Step 6: Configure monetization (if YPP-eligible)

- Set ad placement (mid-roll where appropriate, not every 2 minutes)
- Configure brand-safety filters
- Confirm category matches advertiser preferences

### Step 7: Post to team Slack

- Share URL in `#yt-production`
- Tag Strategist for awareness
- Flag publish time for analytics review at 24 + 48 hour marks

---

## Workflow: Stage 10 — Repurpose

### Step 1: Run Clipify

1. Drop master video file into `~/.claude/skills/clipify/` workflow
2. Run `/clipify` in Claude Code
3. Clipify whisper-transcribes, detects punchlines/audio peaks/pauses
4. Outputs 3 vertical clips with:
   - Speaker tracking (16:9 → 9:16 reframe following the active speaker)
   - Opus-style word-by-word burned-in captions
   - 30–60 second standalone clips

### Step 2: Review the 3 clips

- Pick 2–3 best clips for posting
- Reject any that lose context out of full video
- Reject any with profanity / sensitive content the algorithm won't promote

### Step 3: Write platform-specific captions

- **TikTok:** 100–150 chars, 3 hashtags, hook in first line
- **Instagram Reels:** 150–200 chars, 3–5 hashtags, hook + CTA to full video
- **YouTube Shorts:** 50–100 chars, title-style, link to full video in description

### Step 4: Schedule via Postiz

1. Open Postiz
2. Schedule each clip to:
   - TikTok
   - Instagram Reels
   - YouTube Shorts
3. Stagger by 2–4 hours to avoid algorithm overlap penalty
4. Set thumbnail (frame from clip) per platform

### Step 5: Log distribution

- Note in tracking sheet: which clips, which platforms, scheduled time
- Track 7-day performance per clip for repurposing intelligence

---

## Tools you use

- **YouTube Studio** — uploads, scheduling, analytics, monetization
- **vidIQ** — tag analysis (the tags hack — copy competitor tags)
- **TubeBuddy Legend** — A/B testing on titles + descriptions + tags
- **YouTube Test &amp; Compare** — native thumbnail A/B testing (FREE)
- **Clipify** — local AI clipping ($0, MIT licensed)
- **Postiz** — cross-platform scheduling (~$10/mo)
- **Notion / Trello** — distribution tracking and SOP reference

---

## Capacity

20+ channels per Publisher comfortably. The work is high-volume but mechanical — uploading, scheduling, tagging, scheduling clips. Each channel's per-video work takes ~15 minutes if the upstream stages delivered clean output.

If a Publisher is below 15 channels at steady state, the team has slack — either bring on more channels or reassign Publisher time to other ops.

---

## What you DON'T do

- You don't change the title (Strategist locked it; you upload as-is)
- You don't redesign thumbnails (Designer + AI handle that in Stage 05)
- You don't edit the video file (Editor's job)
- You don't write the captions for short-form (you adapt them — sourced from script)
- You don't make the double-down decisions (Strategist does, after weekly report)

---

## Quality bar

Every published video must:
- Have the exact Strategist-approved title (no typos, no paraphrases)
- Have 3–5 hashtags at the top of the description
- Have video tags pulled via vidIQ from at least 2 successful competitor videos
- Be scheduled for audience prime time
- Have native A/B test configured on thumbnails
- Have URL posted to `#yt-production` Slack within 15 minutes of publish

Every clip in Stage 10 must:
- Pass the "could this stand alone without context?" test
- Have platform-appropriate captions
- Be scheduled within 24 hours of master video publish

---

## Hand-off contract

Your Stage 08 output: Video Live (URL + initial metadata) → goes to Stage 09 (Strategist + analytics agent) for measurement.

Your Stage 10 output: 3 platforms live → terminal stage. Just track performance for the weekly report loop.
