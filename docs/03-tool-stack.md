# Tool Stack — Everything The Team Uses

## Core AI Tools

### Claude (Anthropic)
- **What it's for:** Channel data extraction, title analysis, topic ranking, Script Bible generation, analytics interpretation
- **Plan:** Claude Pro ($20/mo) per user at minimum; Claude Team ($25/user/mo) once we have 3+ people running prompts
- **Why not free:** The **Claude Chrome extension** (Scott references it heavily) requires Pro. Also longer context windows matter for Script Bibles.
- **Owner:** Strategist + Researcher + Script Producer (3 seats minimum)
- **Setup:** Install Chrome extension on every team member's browser. Train on screenshot-to-paste workflow.

### Gemini (Google)
- **What it's for:** Deep Research mode for niche research; outline generation from Script Bible
- **Plan:** Gemini Advanced ($20/mo) — Deep Research is gated behind paid tier
- **Owner:** Researcher + Script Producer
- **Setup:** Use same Google account that owns YouTube channels for seamless access

### ElevenLabs (Voiceover)
- **What it's for:** AI voiceover for videos where human VO isn't required
- **Plan:** Creator ($22/mo) unlimited at decent quality; Pro ($99/mo) for higher quality + commercial rights
- **Owner:** Script Producer or Editor (shared seat fine)
- **Alternative:** PlayHT, Murf.ai

---

## YouTube-Specific Tools

### vidIQ
- **What it's for:** Competitor tag analysis, transcript pulling, channel intelligence, thumbnail analysis
- **Plan:** Boost ($7.50/mo) or Boost+ ($39/mo) — the paid tiers unlock the hacks Scott references
- **Owner:** Researcher (primary), Strategist (shared access)
- **Alternative:** TubeBuddy (similar, sometimes better for specific features)
- **CRITICAL:** This is where Scott's "tag hack" lives — see what competitor tags are actually being used

### YouTube Studio
- **What it's for:** Core upload + analytics + monetization management
- **Plan:** Free (comes with YouTube)
- **Owner:** Publisher + Strategist (both with appropriate role levels)
- **Role levels we need:**
  - **Manager** (Strategist): can upload, edit, view revenue
  - **Editor** (Researcher, Publisher): can upload, edit, no revenue
  - **Viewer (limited)** (Analytics-only team): view analytics, no uploads
- **Workflow:** Each client grants us appropriate roles. Avoid password sharing.

### Google Trends
- **What it's for:** Topic validation (rising / stable / declining)
- **Plan:** Free
- **Owner:** Researcher
- **Filter defaults:** United States, past 12 months, YouTube Search

### TubeBuddy (Optional)
- **What it's for:** Alternative to vidIQ; some find it better for keyword research
- **Plan:** Legend ($29/mo) for full features
- **Recommendation:** Start with vidIQ (Scott's pick); add TubeBuddy if we need additional features

---

## Production Tools

### Adobe Premiere Pro / DaVinci Resolve (Editor's Choice)
- **What it's for:** Video editing
- **Plan:** Premiere ($23/mo) or DaVinci (free tier is excellent)
- **Owner:** Video Editor
- **Recommendation:** Let editors use what they're fastest in. Output quality matters more than software.

### Canva Pro
- **What it's for:** Thumbnail design + quick graphics
- **Plan:** Canva Pro ($15/mo)
- **Owner:** Thumbnail Designer

### Photoshop (Thumbnail Designer)
- **What it's for:** High-end thumbnail production (Canva has limits)
- **Plan:** $23/mo single app
- **Owner:** Thumbnail Designer (optional — some designers prefer Canva)

### Frame.io or Google Drive (Asset Management)
- **What it's for:** Sharing raw footage, voiceovers, edits between team members
- **Plan:** Frame.io Free tier to start, or Google Drive Team
- **Owner:** Publisher + Editor

---

## Analytics & Research

### TubePulse / Social Blade
- **What it's for:** External view of any channel's growth trends, revenue estimates
- **Plan:** Free (Social Blade); TubePulse has paid tiers
- **Use case:** Competitor research during niche selection

### Noxinfluencer / HypeAuditor (Optional)
- **What it's for:** Deeper competitor channel audits
- **Plan:** Depends on scale
- **Recommendation:** Hold off until we're running 10+ channels

---

## Asset Sourcing (For Video B-Roll)

### Storyblocks
- **What it's for:** Stock video, audio, images
- **Plan:** $228/year (Unlimited All-Access)
- **Owner:** Editor (shared seat)

### Envato Elements
- **What it's for:** Stock footage + templates
- **Plan:** $198/year
- **Alternative to Storyblocks — pick one**

### Pexels / Pixabay
- **What it's for:** Free stock footage
- **Plan:** Free
- **Use case:** Budget videos or when paid stock doesn't have what we need

### Midjourney / Runway ML (AI Visuals)
- **What it's for:** AI-generated visuals when stock doesn't cut it; motion graphics
- **Plan:** Midjourney Pro ($60/mo), Runway Standard ($15/mo)
- **Owner:** Editor

---

## Operations & Project Management

### Notion (Common Stack)
- **What it's for:** Client pages, SOPs, topic briefs, script packs, reports
- **Plan:** Already in place
- **Setup:** Create a dedicated "YouTube Arm" workspace with templates for each client

### Slack (Common Stack)
- **What it's for:** Team coordination + client communication
- **Plan:** Already in place
- **Setup:**
  - `#yt-strategy` — internal strategic discussion
  - `#yt-analytics` — daily analytics posts
  - `#yt-production` — daily production status
  - Per-client channel for client comms (standard your team pattern)

### Trello (Common Stack)
- **What it's for:** Task tracking per client
- **Plan:** Already in place
- **Setup:** Board per client with lanes: Research → Script → Edit → Thumbnail → Publish → Live → Optimize

### Google Workspace (Common Stack)
- **What it's for:** Docs, Sheets, Drive
- **Plan:** Already in place

---

## Analytics Dashboard (To Build)

We should build an **internal your team dashboard** that pulls YouTube Analytics data into one view across all clients. Options:

### Option A: Google Sheets + YouTube Analytics API
- **Pros:** Free, flexible, team already fluent in Sheets
- **Cons:** Requires API setup, maintenance
- **Timeline:** 1 week for a junior dev or a junior dev in a weekend

### Option B: Looker Studio (Free from Google)
- **Pros:** Native YouTube Analytics connector, pretty dashboards
- **Cons:** Learning curve
- **Timeline:** A few days to build templates

### Option C: Existing SaaS (VidIQ Enterprise, Hootsuite Analytics, etc.)
- **Pros:** Plug-and-play
- **Cons:** Cost scales with clients
- **Recommendation:** Skip for now

**Recommended:** **Option B** (Looker Studio) — we build templates once, deploy per client.

---

## Monthly Cost Summary (At 5 Active Clients)

| Tool | Cost/Mo |
|------|---------|
| Claude Pro × 3 seats | $60 |
| Gemini Advanced × 2 seats | $40 |
| ElevenLabs Creator | $22 |
| vidIQ Boost+ | $39 |
| Canva Pro | $15 |
| Adobe Premiere (shared editor) | $23 |
| Midjourney Pro | $60 |
| Storyblocks (annualized /12) | $19 |
| **Tools Subtotal** | **~$278/mo** |
| Production labor (75 videos/mo × $100 avg) | $7,500 |
| **Total Cost of Goods Per Month** | **~$7,800** |

**Revenue at 5 clients × $3.5K avg:** $17,500/mo
**Gross margin at that level:** ~$9,700/mo = **~55% gross margin**

---

## First-Purchase Priority List

If we're budget-conscious at launch, buy in this order:

### Must Buy Day 1
1. Claude Pro (1 seat to start, team lead) — $20
2. Gemini Advanced (1 seat) — $20
3. vidIQ Boost+ (1 seat) — $39
4. ElevenLabs Creator (shared) — $22
5. Canva Pro (for Thumbnail designer) — $15

**Day 1 essential stack: $116/mo**

### Add By Month 2
6. Second Claude Pro seat — $20
7. Storyblocks annual — $228/yr
8. Adobe Premiere (if editor needs it) — $23

### Add By Month 3
9. Third Claude + Gemini seats
10. Midjourney Pro — $60
11. Team plans where it makes sense

---

## Setup Checklist (Week 1)

- [ ] Team lead purchases Day 1 stack
- [ ] Create shared 1Password vault: "YT Arm — Shared Tools"
- [ ] Install Claude Chrome extension on all team browsers
- [ ] Set up Slack channels (`#yt-*`)
- [ ] Create Notion workspace structure (client template + SOPs folder)
- [ ] Create Google Drive folder: "your team YouTube Arm" with subfolders per client
- [ ] Set up Looker Studio template for client analytics
- [ ] Draft initial SOP: "4-Prompt Claude Sequence" (Priority 1)
