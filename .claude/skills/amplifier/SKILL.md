---
name: amplifier
stage: attention
description: Use when running the third stage of the Momentum System — designs the daily outreach and content engine. Applies Hormozi's Core Four priority order, ACA framework, Rule of 100, and Hook-Retain-Reward content units. Produces 3 ready-to-send DM templates, 3 content hooks, and a daily action rhythm. Can be run standalone or called by /momentum. No external dependencies — all knowledge is embedded.
argument-hint: [path to output folder]
---

# Amplifier — Design the Daily Outreach and Content Engine

## What This Skill Does

Amplifier is Agent 3 of the Momentum System. It reads the validated market (Hunter) and the built offer (Alchemist) and designs the daily system to get that offer in front of the right people. It applies Hormozi's Core Four advertising framework from $100M Leads: warm outreach first, content second, cold outreach third, paid ads last. It produces a daily rhythm document, 3 ACA DM templates, and 3 Hook→Retain→Reward content units — all written specifically for this offer and avatar. Saves `outreach.md` to the project folder.

This skill does not write generic templates. Every DM and hook is specific to the avatar's exact pain language from `market.md` and the offer's dream outcome from `offer.md`.

---

## Hormozi Knowledge — Outreach and Content Frameworks

### The Core Four ($100M Leads)

There are only 4 ways any person can let any other person know about anything. Everything else is a variation of one of these four.

**1. Warm Outreach (1:1 → Warm audience) — Priority 1, start immediately:**
People who already know you: existing contacts, LinkedIn connections, community members, past clients, followers. Fastest path to the first paying client. Benchmarks from Hormozi's gym client data: 1 in 5 contacts replies, 1 in 5 replies tries the offer, 1 in 4 of those converts to paid. At 100 touches/week → ~5 clients/week at full efficiency (early-stage practitioners see 1–2, which is still a business).

**2. Free Content (1:many → Warm audience) — Priority 2, run in parallel:**
Grows a warm audience over time. Content works on a delay — starts paying dividends months later. Start even with a tiny audience. Hormozi stat: 78% of his gym clients had consumed 2+ long-form content pieces before booking a call. "Give until they ask" is the optimal ratio; 3.5 gives to 1 ask on mature platforms.

**3. Cold Outreach (1:1 → Cold audience) — Priority 3, start month 3+:**
Strangers who fit the avatar but don't know you yet. Takes 12 months of consistent execution to become a reliable channel. Companies that master cold outreach hit $10M+/month invisibly. Three problems: getting contact info, getting them to open, getting them interested. Do not prioritize before warm is exhausted.

**4. Paid Ads (1:many → Cold audience) — Priority 4, Rung 2+ only:**
Most scalable and most expensive. Amplifies a validated offer. Requires a proven GSO and at least one case study. A Grand Slam Offer makes ads 22x more profitable than a commodity offer (from $100M Offers data). Do not spend on ads without proof.

### The ACA Framework (Warm Outreach Structure)

Every warm outreach message follows: Acknowledge → Compliment → Ask.

**Acknowledge:** Reference something specific about the person — a post they wrote, their business type, something in their bio. Never generic. "Hey I saw you're a coach" is generic. "Hey, saw your post about struggling with client no-shows last week" is specific.

**Compliment:** Genuine and specific. Not "your content is great." Something that shows you actually looked at their work or thought about their situation.

**Ask:** Soft, low-commitment, non-pitchy. The goal is to start a conversation, not close a deal. Ask a question about their situation or offer a free insight — not "want to hop on a call?"

Each message under 100 words. Reads like a real person, not a CRM sequence.

### The Rule of 100

Hormozi's daily volume benchmark: 100 units of primary lead-generation activity per day. For warm outreach: 100 touches (DMs, comments, connection requests). For content: 100 minutes of creation time. The rule forces consistency over quality optimization — volume is the habit, quality improves within the volume.

### Hook → Retain → Reward (Content Unit Framework)

**Hook:** Stop the scroll. One line. Pattern interrupt, bold specific claim, or curiosity gap. Written in the avatar's language — makes them think "this is about me."

**Retain:** Deliver on the hook. Proof, story, how-to, or surprising fact. 3–5 sentences. Earn their continued attention.

**Reward:** Give a takeaway worth saving or sharing. A reframe, an actionable tip, a hard truth. Closes the loop on the hook. Optional soft CTA (reply with a word, comment, DM for X).

---

## Step 1: Locate Files

**If $ARGUMENTS contains a folder path:**
- Read `[folder]/profile.md`, `[folder]/market.md`, and `[folder]/offer.md`
- Set `output_folder` to that path

**If $ARGUMENTS is empty:**
- Ask: "Provide the path to your momentum project folder (e.g., `projects/momentum/your-slug/`), or paste the offer details so I can build the outreach engine."

---

## Step 2: Map Current Channels

Read the user's intake answer from `profile.md` — specifically question 4 (current client-getting method: referrals / cold outreach / content / ads / none) and question 7 (hours per week available).

Map their current activity to the Core Four framework. Identify:
- What they are already doing (do not replace, build on it)
- What is missing from the priority order
- Where to start given their available hours

---

## Step 3: Core Four Priority Order

Always follow this sequence. Never skip ahead. Never start with paid ads.

**Priority 1 — Warm Outreach (start here, always):**
People who already know you: existing contacts, LinkedIn connections, community members, past clients, followers. This is the fastest path to the first client. Benchmarks from Hormozi: 1 in 5 contacts replies, 1 in 5 replies tries the offer, 1 in 4 of those converts to paid. At 100 outreach touches/week: ~5 clients/week at full efficiency (scales down at early stage).

**Priority 2 — Free Content (run in parallel with warm):**
Grow a warm audience over time. One content unit per day minimum. Content works on a delay — it pays dividends months later. Start now even if the audience is tiny. Give first, ask later. Hormozi's 78% stat: 78% of his gym clients had consumed 2+ long content pieces before booking.

**Priority 3 — Cold Outreach (start month 3+):**
Strangers who fit the avatar but don't know you yet. Takes 12 months to become a reliable channel. Do not prioritize this before warm outreach is exhausted and content is consistent.

**Priority 4 — Paid Ads (Rung 2+ only):**
Only after there is a proven offer, a case study, and budget. Do not spend on ads without a validated GSO and at least one client result.

State the current priority tier for this business based on their intake answers, and prescribe which tier to execute now vs. later.

---

## Step 4: Daily Rule of 100 Rhythm

Design the specific daily action block. Adjust for the hours available from intake (question 7).

Default rhythm (assume 2 hours/day available):

**Morning block (30 min) — Warm Outreach:**
100 warm outreach touches per week = ~20/day on weekdays. Each touch = one ACA DM, one comment on a target's post, or one connection request with a personal note. Track in a simple spreadsheet (Name / Date / Platform / Status).

**Midday block (60 min) — Content:**
Draft and post one content unit. Use the Hook→Retain→Reward structure (built in Step 6). One post per day on the primary platform, repurpose to secondary.

**Evening block (15 min) — Follow-up:**
Check reply queue. Respond to any DM replies. Move warm conversations forward. Log any objections heard.

Scale up or down based on available hours from intake. If under 1 hour/day available, prioritize warm outreach over content (direct ROI).

---

## Step 5: Write 3 ACA DM Templates

ACA = Acknowledge → Compliment → Ask.

**Acknowledge:** Reference something specific about them — a post they wrote, their business type, something in their bio. Never generic. "Hey" with no context gets ignored.

**Compliment:** Genuine and specific. Not "your content is great." Something that shows you actually looked.

**Ask:** Soft, low-commitment, non-pitchy. The goal is to start a conversation, not close a deal. Ask a question about their business or offer a free insight — not "want to hop on a call?"

Write 3 DM templates tailored to the exact avatar from `market.md` and referencing the pain language ("their exact words"). Name each template by context (e.g., "Template 1: LinkedIn, targeting coaches with an audience," "Template 2: After someone comments on a post," etc.).

Each DM should be under 100 words. It must read like a real person wrote it, not a CRM sequence.

---

## Step 6: Write 3 Hook→Retain→Reward Content Units

**Hook:** Stop the scroll. One line. Use a pattern interrupt, a bold specific claim, or a curiosity gap. Written in the avatar's language — makes them think "that's about me."

**Retain:** Deliver on the hook. Proof, a short story, a how-to, or a surprising fact. 3–5 sentences. Makes them keep reading because you've earned their attention.

**Reward:** Give them a takeaway worth saving or sharing. A reframe, a actionable tip, or a hard truth. Closes the loop on the hook. Optionally ends with a soft CTA (reply with a word, comment below, DM me for X).

Write 3 complete units. Each unit should be written for a different content angle:
- Unit 1: Pain-focused (agitate the exact pain from avatar's words)
- Unit 2: Proof/story-focused (a result, even a small one, told as a narrative)
- Unit 3: Education-focused (teach one specific thing related to the offer — give away the secret, sell the implementation)

---

## Step 7: Platform Recommendation

Based on the avatar's online gathering places from `market.md`, recommend:

**Primary platform** (where to post every day + run warm outreach): The platform where the avatar is most concentrated and most reachable via DM.

**Secondary platform** (repurpose content, lower effort): A second platform where the same content can be cross-posted with minimal adaptation.

State why each platform was chosen based on the avatar profile.

---

## Step 8: Save Output

Save to: `projects/momentum/[slug]/outreach.md`

File format:

```
# Outreach & Content Engine

## Core Four Status
| Method | Priority | Start When |
|--------|----------|------------|
| Warm outreach | 1 — NOW | Immediately |
| Free content | 2 — NOW | Immediately |
| Cold outreach | 3 — LATER | Month 3+ |
| Paid ads | 4 — HOLD | Rung 2+ only |

## Daily Rhythm
**Morning (30 min) — Warm Outreach:**
[Specific action: N DMs/day, method, tracking note]

**Midday (60 min) — Content:**
[Specific action: 1 unit/day, platform, repurpose note]

**Evening (15 min) — Follow-up:**
[Specific action: reply queue, objection log]

## Warm Outreach — ACA DM Templates

### Template 1: [Context/Trigger]
[Full DM text — under 100 words]

### Template 2: [Context/Trigger]
[Full DM text — under 100 words]

### Template 3: [Context/Trigger]
[Full DM text — under 100 words]

## Content Units (Hook → Retain → Reward)

### Unit 1: Pain-Focused
**Hook:** [One line]
**Retain:** [3–5 sentences]
**Reward:** [Takeaway + optional soft CTA]

### Unit 2: Proof/Story-Focused
**Hook:** [One line]
**Retain:** [3–5 sentences]
**Reward:** [Takeaway + optional soft CTA]

### Unit 3: Education-Focused
**Hook:** [One line]
**Retain:** [3–5 sentences]
**Reward:** [Takeaway + optional soft CTA]

## Platform Priority
1. **[Primary platform]** — [why, based on avatar location]
2. **[Secondary platform]** — [why, repurpose method]
```

Tell the user the file was saved and the path. Call out the first DM template they should send today. If called by `/momentum`, confirm ready to proceed to Converter.

---

## Hard Rules

- DM templates must be written in the avatar's exact pain language from `market.md`. No generic copy.
- Content hooks must name the pain or outcome specifically — no vague "do you struggle with productivity?" hooks.
- Paid ads are never Priority 1. Do not suggest ads before warm outreach is exhausted.
- Cold outreach is not recommended before Month 3. Note this explicitly if the user asks about it.
- Every content unit must give genuine value in the Reward section — no "follow me for more" as the only CTA.
- If running standalone: ask for the project folder path if not provided in $ARGUMENTS.
