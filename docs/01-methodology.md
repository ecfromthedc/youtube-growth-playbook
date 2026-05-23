# The Methodology — Decoded Step by Step
## Scott Smith's 5-Step System for Faceless AI YouTube Channels

This is the actual workflow, reconstructed from the recording in the order Scott teaches it. Where the audio cut off or was unclear, I've filled in with context from the rest of the session.

---

## STEP 1: Niche Selection (Audio Cut Off — Reconstructed From Context)

**Goal:** Pick a niche where the math works on Day 1.

### The Non-Negotiables
1. **High RPM** — target $7+ per 1,000 views minimum. Scott's flagship channel runs at **$12.09 RPM**. Aviation, finance, legal, medical, and tech-adjacent niches consistently pay top RPMs.
2. **Rising or evergreen demand** — not a dying fad.
3. **Gap in the market** — demand exists but competition is thin. Scott calls these "goldmine niches."

### The RPM Reality (Why Niche > Everything)
- $12 RPM niche: 100K views = $1,200
- $2 RPM niche (gaming, kids, most entertainment): 100K views = $200
- **Same effort, 6× the revenue.** Niche choice compounds forever.

### Student Examples From The Workshop
- Kurt: $8+ RPM
- John Galooch: $8+ RPM
- Scott's own: $12.09 RPM (aviation — B21 Raider, F15E, MQ4C Triton Drone as topic examples)

### How To Find Them (Implied Workflow)
Because the audio cut off on the exact "niche finder" method, the implied flow matches Step 2's pattern:
1. Use Claude + Gemini to brainstorm 20+ high-RPM niches
2. Use Google Trends to validate rising demand over 12 months
3. Use YouTube search to check competitive density (how many channels, how big, how recent)
4. Prioritize niches with rising trends + fewer than ~50 mature channels

---

## STEP 2: Video Ideation (The 4-Prompt Sequence)

**Goal:** Generate validated, data-backed video topics — no guessing, no wasted $75 on dud videos.

### The Exact Workflow (Prompts 1–4)

#### Prompt 1 → Claude (Channel Data Extraction)
- Take a screenshot of the top competitor channel's Videos tab (showing the 40 most recent uploads)
- Paste screenshot into Claude (this is why the **Claude Chrome extension** matters — screenshot-to-paste is frictionless)
- Prompt Claude to **build a table of the 40 most recent videos** with:
  - Video title
  - View count
  - Upload date

#### Prompt 2 → Claude (Title Pattern Analysis)
- Feed Claude the table from Prompt 1
- Prompt: **"Run a full analysis of every video title. Identify top-performing title patterns, which topics work, which don't, and why."**
- Output: an analysis of what's working in this niche

#### Prompt 3 → Claude (Build the Gemini Research Prompt)
- Prompt Claude: **"Write a short, sharp prompt I can give Gemini to research this niche and find the top trending topics right now."**
- Claude returns a tailored research prompt

#### → Gemini (Deep Niche Research)
- Paste Claude's prompt into **Gemini Deep Research**
- Gemini goes out, researches the entire niche, returns a comprehensive research doc with trending topics, recent angles, surfacing news, etc.

#### Prompt 4 → Claude (Topic Ranking)
- Feed Claude the Gemini research
- Prompt: **"Analyze all of this research and give me the top 5 topics ranked by potential to perform on YouTube in this niche."**
- Output: 5 ranked topic recommendations

### The Critical Verification Step → Google Trends
**This is where Scott hammered the point: do not let AI do everything.**

For each of the 5 topics Claude recommended:
1. Search the topic in **Google Trends**
2. Filter: **United States** (highest-earning audience) + **Past 12 months** + **YouTube Search** (not general Google)
3. Classify each as: Rising / Stable / Declining
4. **Keep rising + stable. Kill declining** (unless truly evergreen).
5. **Compare topics side by side** in Google Trends for relative demand

**Why this matters:** Scott's aviation example — B21 Raider and F15E both trending up (keep), AIAA Aviation totally flat (skip — would be $75 wasted, $0 earned).

> **Scott's quote:** *"AI is a tool. It's not a replacement for your brain. Verify the data. Verify the research. The people who let AI do everything end up with channels that make no money."*

---

## STEP 3: Script Creation (The "Script Bible" System)

**Goal:** Produce a research-packed, data-driven script ready for voiceover — without writing it yourself.

### Sub-Step 3a: Build the Script Bible
1. On the competitor channel, open 10 top-performing videos
2. For each: scroll to **Show Transcript** at the bottom of the description → **Copy Transcript**
3. Paste all 10 transcripts into a single document
4. Alternatively: use **vidIQ** to grab transcripts programmatically (faster at scale)
5. Send all 10 transcripts to Claude with the Script Bible prompt:
   - **"Do a full in-depth analysis of all 10 of these transcripts. Produce a Script Bible covering: hook patterns, pacing, structure, recurring phrases, transition tactics, CTA patterns, tonal register, and narrative arc."**
6. Claude returns the **Script Bible** — the template of how this niche's winning scripts actually work.

### Sub-Step 3b: Outline Generation (NOT the full script)
1. Pick 2–3 validated titles from Step 2
2. Send to Gemini: `Script Bible + titles` with prompt:
   - **"Using this Script Bible as the template, write a full in-depth script outline for each of these titles. The outline should include: the hook, the chapters/beats, the research to weave in, and the CTA. Do NOT write the full script."**
3. Gemini returns a detailed outline per title

### Sub-Step 3c: Hand Off to Human Script Writer
- Package: Script Bible + Outline + Gemini research notes = **The Script Pack**
- Human script writer takes the Pack and writes the final script
- Scott's warning: **"If you have Claude/Gemini write the full script, you're wasting your time. Quality is garbage."**
- Writer charges (roughly) → part of the $75/video cost

### Sub-Step 3d: Final Delivery
- Writer returns a **research-packed, voiceover-ready final script**
- This goes to:
  - Voice-over artist
  - Video editor
  - Thumbnail designer

> **Scott's insight:** *"You didn't write a word, you didn't edit a frame. You got the video idea, you got the script pack, you handed it to the team, they handed you back a video."*

---

## STEP 4: Getting Your First Views

**Goal:** Get one video past 1,000 views. That's the signal you're "in the game."

### The Two Parallel Goals
1. **Data collection** — figure out what's working vs. not
2. **First 1K views** — the algorithmic threshold that unlocks broader distribution

### The Two Benchmarks That Actually Matter

| Metric | Target | What It Means |
|--------|--------|---------------|
| **CTR** (Click-Through Rate) | 10%+ | Of people who see your thumbnail, 10% click |
| **APV** (Average Percentage Viewed) | 30%+ | Viewers watch at least 30% of the video |

**Diagnostic logic:**
- High CTR, low APV → Thumbnail/title are hooking but **script isn't holding** → fix script, especially first 30 seconds
- Low CTR, high APV → People who watch love it, but **thumbnail/title aren't pulling** → fix thumbnail + title
- Both low → Wrong topic or wrong niche match

### The Reality Scott Hammers
- **Most early videos flop.** That's normal. The algorithm is testing you.
- **80% of your videos will get <1,000 views.** Plan for it. Don't panic.
- **3 of 22 videos will drive 90% of the revenue.** (The YouTube portfolio principle — Steph from the workshop nailed it: "10% of the stocks make up 90% of the value. Bingo.")
- **The snowball effect:** When ONE video pops, YouTube sends ALL your videos to more people. One hit lifts the whole channel.

### Publishing Cadence
- **Minimum 2 videos per week**. Below that you're not giving the algorithm enough to learn from.

### AI As Your Optimization Partner (After Upload)
Use Claude to:
- Generate **title variations** for A/B mental testing
- **Analyze your hooks** (paste script, ask "why would someone stop watching in the first 30 seconds?")
- **Interpret your analytics** (paste screenshots from YT Analytics → ask Claude for takeaways)
- **SEO optimize descriptions + tags**

### When to Abandon a Channel or Niche
**Never.** Scott: *"If it's not working, something YOU'RE doing is wrong. Check your data. Your analytics tell you the answer."*

---

## STEP 5: Monetize + Scale

### Requirements To Get Paid
YouTube Partner Program (YPP) needs:
1. **1,000 subscribers**
2. **4,000 watch hours** (~35–40K views if videos are 10–15 min long)

Once you hit both → apply → wait for review → monetized.

### Pre-Monetization Revenue (Scott's Pro Tip)
You can earn **before** YPP via:
- **Brand deals** (sponsorships in the video)
- **Affiliate marketing** (product links in description)

This is important for your team: **we can generate client revenue before the algorithm pays out.**

### Revenue Maximization Levers
1. **High RPM niche** (established in Step 1 — non-negotiable)
2. **High APV** (longer watch → more ads shown per view → higher revenue per view)
3. **Long-form only** — **Shorts do not pay meaningfully.** 10–15 min is the sweet spot.
4. **Multiple channels** (the scale play)

### Tags Hack (Undersold in Most YT Advice)
Scott emphasized these because **most people ignore them:**

**Video Tags** (inside YouTube Studio → scroll down):
- These help YT understand topical classification
- Help your content appear in search
- Example (celebrity niche): `celebrity news`, `Hollywood drama`, `pop culture`

**Description Tags / Hashtags** (top 3–5 hashtags above video title):
- Make videos discoverable via clickable hashtag links
- Use 3–5 relevant hashtags: `#celebrities #HollywoodDrama #PopCulture`

**The vidIQ Hack:**
- Install vidIQ Chrome extension
- When viewing a competitor's video, the right sidebar shows **the exact tags they're using**
- Copy/adapt their tags for your own videos in the same niche

### Scaling The Portfolio
- Channel 1 → prove the system → $30K+ potential
- Channel 2 → **easier** (same content team, same process, no learning curve)
- Channel 3, 4, 5… → compound income streams
- Scott runs **22 channels**. Example month he showed:
  - Channel A: $16,694 (2.2M views, ~$7.59 RPM)
  - Channel B: $15,129 (1.8M views, $8.37 RPM)
  - Channel C: $6,439 (744K views, $8.65 RPM)
  - **Total: $38,262 in one month across 3 channels**

### When Scaling, Leverage Existing Resources
- Same content team (writers, editors, thumbnail designers)
- Same AI prompt library
- Same SOPs
- Same analytics dashboard
- **Just swap the niche + channel identity**

---

## The Full Optimization Checklist

### Before Upload
- [ ] Strong topic (trending on Google Trends + gap in niche)
- [ ] SEO-optimized title (keyword-bearing + curiosity-driving)
- [ ] Click-worthy thumbnail
- [ ] Script holds first 30 seconds (if yes, viewer usually finishes)
- [ ] AI-assisted research + topic verification done
- [ ] Video tags set in YT Studio
- [ ] 3–5 hashtags in description

### After Upload
- [ ] Monitor CTR (first 24–48 hours tells you a lot)
- [ ] Monitor APV (drop-off points tell you what's failing)
- [ ] Run AI analysis on underperformers
- [ ] Double down on what's working (more videos in that vein)
- [ ] Cut the fat (stop making what's not working)

---

## Scott's Big Insights (Worth Internalizing For The your team Team)

1. **"You need a few videos to really pop off. The rest carry weight, but those few drive everything."**
2. **"Don't let AI do everything. Use it as a channel partner, not a replacement."**
3. **"Most people are too focused on going viral. Play the numbers game and wait for the one that pops."**
4. **"Shorts don't pay. Long-form only."**
5. **"The snowball effect is real. One hit pulls the whole channel up."**
6. **"Check your data. Numbers don't lie. If you think a niche is dead, something you're doing is wrong."**
7. **"It's like an investment portfolio: 10% of the stocks make up 90% of the value."**

---
