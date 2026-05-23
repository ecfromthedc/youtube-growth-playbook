# Step 5 Prompts — Monetization &amp; Scale

> Goal: Hit YouTube Partner Program (YPP), apply, start earning ad revenue, then duplicate the system on channel 2, 3, 4… The portfolio play.

---

## YPP requirements

YouTube Partner Program eligibility (US, 2026):
- **1,000 subscribers**
- **4,000 watch hours** in the past 12 months (~35–40K views at 10–15 min length)

Once both thresholds are hit → apply via YT Studio → wait for review (typically 1–4 weeks) → monetized.

---

## Prompt 5-1 — YPP Application Readiness Check

**Model:** Claude
**When to run:** When a channel is approaching YPP thresholds (within 80% of either)
**Input:** Channel stats + content theme overview
**Output:** Readiness audit + 10-item pre-application checklist

```
Our channel [CHANNEL NAME] is approaching YouTube Partner Program eligibility. Current stats:
- Subscribers: [N]
- Watch hours (last 12 months): [N]
- Total videos: [N]
- Channel age: [N months]

Give me a YPP readiness audit:
1. Technical eligibility — are we meeting thresholds? When will we if not yet?
2. Content policy audit — based on our content themes, are there any demonetization risks? Any adult themes, copyright issues, "limited ads" risks?
3. Community guidelines check — anything that could block approval?
4. Channel setup audit — is the about page, banner, channel trailer all optimized?
5. Pre-application checklist — 10 items to complete before clicking "apply"

Be specific about what we need to do before applying so we don't get rejected.
```

**Success criteria:**
- Specific demonetization risks identified (not generic "be careful with copyright")
- 10 checklist items are concrete and actionable
- Estimated timeline to threshold given current trajectory

---

## Pre-monetization revenue streams

You can earn before YPP via:

- **Brand deals** — sponsorships baked into the video (relevant niches: finance, tech, aviation often have early sponsor interest)
- **Affiliate marketing** — product links in the description
- **Lead magnets** — drive traffic to a free training or email list, monetize the audience separately

Set up brand-deal-ready language in the description from Day 1: "For sponsorship inquiries: [email]"

---

## The tags hack (most channels ignore this)

Two surfaces in YouTube Studio that materially affect distribution:

### Video tags
- Inside YouTube Studio → scroll down past description
- Help YouTube classify your content topically
- Help your content surface in search
- Example for celebrity niche: `celebrity news`, `Hollywood drama`, `pop culture`

### Description hashtags
- Top 3–5 hashtags at the very top of your description
- Make videos discoverable via clickable hashtag links
- Example: `#celebrities #HollywoodDrama #PopCulture`

### The vidIQ tag-stealing hack
1. Install the **vidIQ Chrome extension**
2. View any competitor video in the niche
3. Right sidebar shows the **exact tags they're using**
4. Copy and adapt for your videos in the same niche

This is the single most-undervalued hack in YouTube SEO.

---

## Prompt 5-2 — Channel #2 Niche Evaluation

**Model:** Claude
**When to run:** When channel 1 is mature (monetized, consistent $5K+/mo revenue) and the team has capacity
**Input:** Existing channel stats + 3 candidate niches for channel 2
**Output:** Ranked recommendation + 90-day launch plan

```
We have an established channel at [CHANNEL NAME] in the [NICHE] niche, now making $[N]/month.

We're ready to launch a second channel. Our team is experienced with [EXISTING NICHE] workflows. Evaluate the following candidate niches for our second channel based on:

- Learning curve leverage — can we reuse our existing skills or do we have to start over?
- Audience overlap — does it tap similar audiences we could cross-promote to?
- Team capacity — can our existing team handle this without doubling cost?
- RPM + scale potential
- Risk diversification — does this de-risk our portfolio vs. doubling down?

Candidate niches:
1. [NICHE A]
2. [NICHE B]
3. [NICHE C]

Rank them and recommend which to launch, which to hold, which to skip. Give a 90-day launch plan for the recommended one.
```

**Success criteria:**
- Explicit ranking (launch / hold / skip)
- 90-day launch plan with weekly milestones
- Team capacity assessment is realistic (not aspirational)

---

## Revenue maximization levers

Once monetized, the only levers that move revenue are:

1. **High RPM niche** — locked in at Stage 01, non-negotiable
2. **High APV** — longer watch = more ads shown per view = higher revenue per view
3. **Long-form only** — Shorts do not pay meaningfully. Keep 10–15 min standard
4. **Multiple channels** — the scale play

There is no fifth lever. Don't chase one.

---

## Scaling the portfolio

The hard part is channel 1 (figuring out the system).

| Channel | Difficulty | Why |
|---|---|---|
| Channel 1 | Hard | Building the system, hiring the team, learning the niche |
| Channel 2 | Easy | Same team, same SOPs, same prompts — only the niche + identity change |
| Channels 3–10 | Mechanical | Pure execution. Same playbook. |
| Channels 10+ | Operational | Now it's a real ops job — team capacity becomes the constraint |

When scaling, leverage:
- Same content team (writers, editors, thumbnail designers)
- Same AI prompt library
- Same SOPs
- Same analytics dashboard
- Same Script Bible methodology (run once per niche)

**Just swap the niche + channel identity.**

---

## The portfolio outcome

Scott Smith's snapshot:
- 22 active channels
- Combined ~$200K+/month
- Example 3-channel month: $38,262 (Channels A: $16,694, B: $15,129, C: $6,439)

The math at every scale:

| Channels | Average revenue / channel | Total monthly |
|---|---|---|
| 1 | $5K–$30K | $5K–$30K |
| 3 | $5K–$15K | $15K–$45K |
| 10 | $5K–$15K | $50K–$150K |
| 22 | $5K–$15K | $100K–$300K |

---

## Output deliverable: Portfolio Launch Plan (when adding channels)

The Stage 05 (Scale) artifact when launching a new channel:

```yaml
channel_n: 2
niche_locked: "..."
launch_date: "YYYY-MM-DD"
team_capacity_check: "passed | concerns: [...]"
shared_resources:
  - "Existing prompt library"
  - "Existing analytics dashboard"
  - "Existing writer/editor pool"
new_resources_required:
  - "New competitor analysis (Bible doesn't transfer across niches)"
  - "New thumbnail style exploration"
90_day_milestones:
  week_4: "First 4 videos published, CTR baseline established"
  week_8: "Topic clusters identified, doubling down on winners"
  week_12: "1K subs target, watch hours on track for YPP"
strategist_signoff: "[name] [date]"
```
