# Step 1 Prompts — Niche Selection

> Goal: Lock a high-RPM niche where the math works on Day 1. ≥$7 RPM, rising or evergreen demand, fewer than ~50 mature competitor channels.

---

## Prompt 1A — High-RPM Niche Brainstorm

**Model:** Claude (Opus or Sonnet, current best)
**Input:** None (cold start)
**Output:** 20 ranked niche candidates with full attribute breakdown

```
I'm planning to build a faceless long-form YouTube channel. The goal is to land in a niche with:
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

**Success criteria:**
- 20 distinct niches (no duplicates / re-skins)
- Every niche has all 5 attributes filled
- Top 3 priority recommendations include reasoning rooted in the gap analysis

---

## Prompt 1B — Niche Deep-Dive Validation

**Model:** Claude (Opus or Sonnet)
**Input:** One niche name from Prompt 1A
**Output:** GO / CONSIDER / SKIP verdict with 2-sentence reasoning

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

**Success criteria:**
- All 8 sections completed
- Explicit GO/CONSIDER/SKIP verdict at the end
- Red flags section is specific (not generic "be careful")

---

## Augmentation: 1of10 + Spotter Studio (optional but recommended)

Once Claude has produced the top 3 candidates:

1. Cross-check each candidate in **1of10** — does the niche have outlier patterns (videos that performed 10x–100x channel median)?
2. Cross-check each candidate in **Spotter Studio** — what channels in this niche are growing fastest, and what topics are they winning on?

If a candidate passes both Claude's analysis AND has strong outlier signal in 1of10, it's a strong GO. If Claude says GO but 1of10 shows no outlier patterns, the niche is mature without breakout opportunities — CONSIDER.

---

## Manual gate: Google Trends verification

For your final shortlist:

1. Search the niche term in Google Trends
2. Filter: `United States` · `Past 12 months` · `YouTube Search`
3. Classify: rising / stable / declining
4. Compare top 3 candidates side-by-side using the "Compare" feature
5. **Lock the niche that shows rising or stable trend + highest comparative interest**

If all 3 candidates are flat or declining, return to Prompt 1A and brainstorm again with adjusted constraints.

---

## Output deliverable: Niche Brief

The Stage 01 hand-off to Stage 02 is a "Niche Brief" doc containing:

```yaml
niche_name: "..."
locked_at: "YYYY-MM-DD"
rpm_estimate: $X–$Y (US audience, long-form)
demand_trend: "rising | stable"
competitive_density: "thin (< N mature channels)"
top_10_competitors:
  - name: "..."
    url: "..."
    subscribers: ...
    estimated_monthly_revenue: $...
content_formats_that_work:
  - "..."
  - "..."
red_flags: "..."
strategist_approval: "[name] [date]"
```

This brief is the input to Stage 02 (Topic Ideation).
