---
name: momentum
description: Use when someone wants to build a complete 1-person business system from scratch. Runs a 7-question intake then fires 5 specialized agents in sequence — Hunter (market), Alchemist (offer), Amplifier (outreach), Converter (sales), Loop Engine (follow-up) — producing a complete 90-day action plan. Based on Alex Hormozi's $100M Offers and $100M Leads frameworks. No external dependencies — all knowledge is embedded in sub-skills.
argument-hint: [optional: describe your business to skip the intake, or leave blank to start the interview]
---

# Momentum — 1-Person Business System (Hormozi Framework)

## What This Skill Does

Momentum is the orchestrator for a complete business-building system based on Alex Hormozi's $100M Offers and $100M Leads frameworks. It runs a 7-question intake, confirms your business profile, then fires 5 specialized agents in sequence — each building on the last — to produce a complete, printable 90-day action plan.

The system is designed for anyone starting or relaunching a 1-person service business. It works for any niche, any offer type, any experience level.

**What you get at the end:**
- A validated market with a precise avatar and buyer language (Hunter)
- A named, guaranteed, priced Grand Slam Offer with a full value stack (Alchemist)
- A daily outreach rhythm with 3 ready-to-send DM templates and 3 content hooks (Amplifier)
- A complete CLOSER talk track with pre-call brief and follow-up scripts (Converter)
- A 90-day reactivation system with testimonial requests and referral sequences (Loop Engine)
- A single `90-day-plan.md` file — self-contained, readable, printable, organized by month

**Time to complete:** 20–40 minutes of conversation.

---

## Step 1: Handle Arguments

**If $ARGUMENTS contains a folder path** (starts with `projects/` or contains an existing profile):
- Read `[folder]/profile.md` if it exists
- Skip to Step 3 (profile confirmation) with existing data

**If $ARGUMENTS is a business description** (plain text, no path):
- Pre-fill intake answers where inferable from the description
- Present a pre-filled summary and ask the user to confirm or correct each answer
- Skip to Step 3

**If $ARGUMENTS is empty:**
- Proceed to Step 2 (full intake interview)

---

## Step 2: Intake Interview (7 Questions)

Ask each question one at a time. Wait for the answer before asking the next. Do not rush or combine questions.

**Question 1:** What do you sell, or what do you want to sell? (product, service, or idea — describe it in your own words)

**Question 2:** Who is your ideal customer? (describe the specific type of person, not a demographic category — who do you most want to help?)

**Question 3:** What is your target price point or range? (even a rough number is fine — what do you want to charge?)

**Question 4:** How do you currently get clients, if at all? (referrals / cold outreach / content / ads / none — or describe)

**Question 5:** Do you have any existing clients or case studies? (even one partial result counts)

**Question 6:** What is your single biggest bottleneck right now? (leads / offer clarity / closing sales / follow-up / all of the above)

**Question 7:** How many hours per week can you dedicate to business development? (honest number — this shapes the daily rhythm in Amplifier)

---

## Step 3: Confirm the Profile

After all 7 answers, print a clean summary:

```
Here's what I have:

1. Offer: [answer]
2. Ideal customer: [answer]
3. Target price: [answer]
4. Current client source: [answer]
5. Existing proof: [answer]
6. Biggest bottleneck: [answer]
7. Hours/week available: [answer]

Is this correct? Say yes to proceed, or correct anything before we start.
```

Wait for confirmation. Do not proceed until confirmed.

---

## Step 4: Create the Output Folder

Generate a slug from the offer or business description. Rules:
- Lowercase only
- Hyphens between words, no spaces or special characters
- 2–4 words maximum
- Examples: `social-media-restaurants`, `ai-coaching-solopreneurs`, `bookkeeping-freelancers`

Create the output folder: `projects/momentum/[slug]/`

Save the confirmed intake answers to `projects/momentum/[slug]/profile.md`:

```
# Business Profile
**Date:** YYYY-MM-DD
**Slug:** [slug]

## Intake Answers
1. **Offer:** [answer]
2. **Ideal customer:** [answer]
3. **Target price:** [answer]
4. **Current client source:** [answer]
5. **Existing proof:** [answer]
6. **Biggest bottleneck:** [answer]
7. **Hours/week:** [answer]
```

Tell the user: "Profile saved. Starting the 5-agent system now. This will take a few minutes."

---

## Step 5: Run the 5 Agents in Sequence

Call each agent via the Skill tool in order. Each agent reads from the project folder and writes its output there. Do not proceed to the next agent until the current one has saved its output file.

**[OFFER] Agent 1 — Hunter (Market Validation):**

Tell the user: "Starting OFFER stage — validating your market."
```
Skill(skill="hunter", args="Run for business at projects/momentum/[slug]/. Read profile.md. Save output to market.md in that folder.")
```
Wait for market.md to be saved. Print a one-line summary of the verdict to the user ("Market: Green — coaches and speakers, findable on LinkedIn and Skool").

**[OFFER] Agent 2 — Alchemist (Offer Building):**

Tell the user: "OFFER stage — building your Grand Slam Offer."
```
Skill(skill="alchemist", args="Run for business at projects/momentum/[slug]/. Read profile.md and market.md. Save output to offer.md in that folder.")
```
Wait for offer.md to be saved. Print the offer name chosen and the value stack total.

**[ATTENTION] Agent 3 — Amplifier (Outreach and Content):**

Tell the user: "Starting ATTENTION stage — designing your outreach and content engine."
```
Skill(skill="amplifier", args="Run for business at projects/momentum/[slug]/. Read profile.md, market.md, and offer.md. Save output to outreach.md in that folder.")
```
Wait for outreach.md to be saved. Print the primary platform recommendation.

**[CONVERSION] Agent 4 — Converter (Sales System):**

Tell the user: "Starting CONVERSION stage — building your sales system."
```
Skill(skill="converter", args="Run for business at projects/momentum/[slug]/. Read offer.md and outreach.md. Save output to sales.md in that folder.")
```
Wait for sales.md to be saved. Print the single most important call opener to use.

**[FEEDBACK] Agent 5 — Loop Engine (Follow-Up System):**

Tell the user: "Starting FEEDBACK stage — building your follow-up and reactivation system."
```
Skill(skill="loop-engine", args="Run for business at projects/momentum/[slug]/. Read all prior output files. Save output to follow-up.md in that folder.")
```
Wait for follow-up.md to be saved.

---

## Step 6: Compile the 90-Day Plan

### 6a: Brand & Design Setup

Before compiling, ask the user:

"Before building your plan, I want to make it look as good as it functions. Two options:

**Option 1 — You have a brand folder:** Paste the folder path (e.g. `references/Brand Assets/`). I'll pull your colors from it.

**Option 2 — No folder:** Tell me your primary brand color (hex like #1a73e8 or a color name like 'deep navy'). I'll design around it.

Either way the plan will be a styled HTML file — readable in any browser, printable, and easy to share."

Wait for the user's response. Do not proceed until they answer.

**If a folder path is provided:**
- Use Glob to list all files in the folder
- Read CSS, JSON, or markdown files found — look for hex color values, CSS custom properties, or named colors
- Extract: primary color, secondary color (if present), any font references
- If multiple color candidates found, list them and ask the user to confirm which is primary
- If the folder is empty or has no usable color data, fall through to asking directly

**If no folder (user gives a color or says they have none):**
- If user gives a hex code: use it exactly as `PRIMARY`
- If user gives a color name: convert to the closest professional hex equivalent
- If user gives nothing / says skip: use default palette — Primary: `#0f172a` (deep slate), Accent: `#3b82f6` (blue)

**Derive the design tokens from PRIMARY:**
- `PRIMARY` — the main brand color (headings, cover background, month headers, key borders)
- `PRIMARY_LIGHT` — a very light tint of PRIMARY (5–10% opacity on white) for alternating section backgrounds
- `ACCENT` — if the user provided a second color, use it; otherwise use PRIMARY at 80% saturation
- `TEXT` — `#111827` (near black)
- `TEXT_MUTED` — `#6b7280`
- `BG` — `#ffffff`
- `BORDER` — `#e5e7eb`

Tell the user: "Brand colors confirmed. Compiling your 90-day plan now."

---

### 6b: Generate the HTML Plan

Read all 5 output files: market.md, offer.md, outreach.md, sales.md, follow-up.md.

Generate and save as `projects/momentum/[slug]/90-day-plan.html`.

**The HTML must be:**
- A single self-contained file — no external CSS, no CDN links, no external fonts
- All styles in a `<style>` block in the `<head>`
- Use `system-ui, -apple-system, sans-serif` as the font stack
- Print-friendly: include `@media print` rules that hide decorative elements and keep content clean

**HTML Structure and Design Spec:**

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>90-Day Business Plan — [Offer Name]</title>
  <style>
    :root {
      --primary: [PRIMARY];
      --primary-light: [PRIMARY_LIGHT];
      --accent: [ACCENT];
      --text: #111827;
      --text-muted: #6b7280;
      --bg: #ffffff;
      --border: #e5e7eb;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: system-ui, -apple-system, sans-serif;
      font-size: 15px;
      line-height: 1.7;
      color: var(--text);
      background: var(--bg);
      max-width: 860px;
      margin: 0 auto;
      padding: 0 24px 80px;
    }

    /* COVER */
    .cover {
      background: var(--primary);
      color: #fff;
      margin: 0 -24px 60px;
      padding: 80px 48px;
    }
    .cover .plan-label {
      font-size: 13px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      opacity: 0.7;
      margin-bottom: 16px;
    }
    .cover h1 { font-size: 36px; font-weight: 700; line-height: 1.2; margin-bottom: 20px; }
    .cover .meta { font-size: 14px; opacity: 0.65; }

    /* EXEC SUMMARY */
    .exec-summary {
      background: var(--primary-light);
      border-left: 4px solid var(--primary);
      padding: 28px 32px;
      border-radius: 4px;
      margin-bottom: 56px;
    }
    .exec-summary h2 {
      font-size: 13px;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--primary);
      margin-bottom: 12px;
    }
    .exec-summary p { font-size: 15px; line-height: 1.8; }

    /* MONTH SECTIONS */
    .month { margin-bottom: 64px; }
    .month-header {
      background: var(--primary);
      color: #fff;
      padding: 16px 24px;
      border-radius: 4px;
      font-size: 18px;
      font-weight: 700;
      margin-bottom: 32px;
    }
    .month-goal {
      font-size: 14px;
      color: var(--text-muted);
      margin-top: 6px;
      font-weight: 400;
    }

    /* WEEK SECTIONS */
    .week { margin-bottom: 40px; padding-left: 16px; border-left: 2px solid var(--border); }
    .week h3 {
      font-size: 16px;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 12px;
      padding-bottom: 8px;
      border-bottom: 1px solid var(--border);
    }
    .week p { margin-bottom: 12px; font-size: 14px; color: var(--text-muted); }
    .week .context { font-size: 14px; line-height: 1.7; margin-bottom: 16px; }

    /* ACTION ITEMS */
    .actions { list-style: none; margin: 16px 0 0; }
    .actions li {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      padding: 8px 0;
      border-bottom: 1px solid var(--border);
      font-size: 14px;
      line-height: 1.5;
    }
    .actions li:last-child { border-bottom: none; }
    .checkbox {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 18px;
      height: 18px;
      border: 1.5px solid var(--primary);
      border-radius: 3px;
      flex-shrink: 0;
      margin-top: 2px;
    }

    /* TWO-PATH BLOCKS */
    .path-block {
      background: var(--primary-light);
      padding: 16px 20px;
      border-radius: 4px;
      margin: 12px 0;
    }
    .path-block strong { display: block; margin-bottom: 8px; font-size: 13px; }

    /* DAILY NON-NEGOTIABLES */
    .daily {
      background: var(--primary);
      color: #fff;
      padding: 32px;
      border-radius: 4px;
      margin: 56px 0;
    }
    .daily h2 { font-size: 16px; font-weight: 700; margin-bottom: 20px; opacity: 0.9; }
    .daily .actions li { border-bottom-color: rgba(255,255,255,0.15); color: #fff; }
    .daily .checkbox { border-color: rgba(255,255,255,0.6); }

    /* FILES REFERENCE */
    .files-ref {
      border: 1px solid var(--border);
      border-radius: 4px;
      padding: 24px 28px;
      margin-top: 48px;
    }
    .files-ref h2 { font-size: 14px; font-weight: 700; margin-bottom: 16px; color: var(--text-muted); }
    .files-ref ul { list-style: none; }
    .files-ref li { padding: 6px 0; font-size: 13px; border-bottom: 1px solid var(--border); }
    .files-ref li:last-child { border-bottom: none; }
    .files-ref code { font-size: 12px; background: var(--primary-light); padding: 2px 6px; border-radius: 3px; }

    /* DIVIDERS */
    hr { border: none; border-top: 1px solid var(--border); margin: 48px 0; }

    @media print {
      body { max-width: 100%; padding: 0; }
      .cover { margin: 0; page-break-after: always; }
      .month { page-break-inside: avoid; }
    }
  </style>
</head>
<body>

  <!-- COVER -->
  <div class="cover">
    <div class="plan-label">90-Day Business Plan</div>
    <h1>[Offer Name]</h1>
    <div class="meta">Generated [YYYY-MM-DD] &nbsp;·&nbsp; [one-line business description]</div>
  </div>

  <!-- EXECUTIVE SUMMARY -->
  <div class="exec-summary">
    <h2>Executive Summary</h2>
    <p>[4 sentences: validated niche, offer name + price, daily action rhythm, 90-day milestone — first client closed]</p>
  </div>

  <!-- MONTH 1 -->
  <div class="month">
    <div class="month-header">
      Month 1: Validate &amp; Build <span class="month-goal">— Weeks 1–4</span>
      <div class="month-goal" style="font-size:13px;margin-top:4px;">Goal: Confirm the market is real, build the offer, go live with content and outreach.</div>
    </div>

    <div class="week">
      <h3>Week 1 — Validate the Market</h3>
      <div class="context">[From market.md: niche statement, 4-filter results, avatar with exact words, market verdict]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Share the niche statement with 1 trusted person — does it sound specific enough?</li>
        <li><span class="checkbox"></span>Find and join 1 community where the avatar gathers</li>
        <li><span class="checkbox"></span>DM 20 existing contacts using Template 1 from outreach.md (conversations only — no pitch)</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 2 — Build and Name the Offer</h3>
      <div class="context">[From offer.md: offer name, dream outcome, value stack summary, guarantee, opening price]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Finalize the offer name (pick one of the 3 MAGIC options)</li>
        <li><span class="checkbox"></span>Set the opening price — commit to it, do not discount it in your head</li>
        <li><span class="checkbox"></span>Write the guarantee in your own words so you can say it naturally on a call</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 3 — Brand &amp; Content Live</h3>
      <div class="context">[From outreach.md: platform priority, content hooks]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Update bio on all active platforms with positioning one-liner + CTA</li>
        <li><span class="checkbox"></span>Publish 3 content pieces using Hook → Retain → Reward structure</li>
        <li><span class="checkbox"></span>Start building the content habit: 1 piece per day minimum</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 4 — Outreach at Rhythm</h3>
      <div class="context">[From outreach.md: daily rhythm — Morning/Midday/Evening blocks]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Send 20+ ACA DMs per day using templates from outreach.md</li>
        <li><span class="checkbox"></span>Publish 1 content unit daily</li>
        <li><span class="checkbox"></span>Book at least 1 discovery call by end of week</li>
      </ul>
    </div>
  </div>

  <!-- MONTH 2 -->
  <div class="month">
    <div class="month-header">
      Month 2: Execute &amp; Iterate <span class="month-goal">— Weeks 5–8</span>
      <div class="month-goal" style="font-size:13px;margin-top:4px;">Goal: 3+ discovery calls completed, offer refined based on real market feedback.</div>
    </div>

    <div class="week">
      <h3>Weeks 5–6 — Full Rhythm</h3>
      <div class="context">Maintain the daily rhythm established in Week 4. No changes to the offer yet — gather data first.<br><strong>Milestone:</strong> 200+ total outreach conversations started.</div>
      <ul class="actions">
        <li><span class="checkbox"></span>[N] warm outreach touches via ACA</li>
        <li><span class="checkbox"></span>1 content unit published</li>
        <li><span class="checkbox"></span>Reply queue checked and advanced</li>
        <li><span class="checkbox"></span>1 objection or win logged</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 7 — Discovery Calls</h3>
      <div class="context">[From sales.md: CLOSER opener, pre-call brief template]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Run 3+ discovery calls using the CLOSER talk track</li>
        <li><span class="checkbox"></span>Fill in the pre-call brief before every call</li>
        <li><span class="checkbox"></span>Send the post-call follow-up email within 5 minutes of hanging up</li>
        <li><span class="checkbox"></span>Log every objection in follow-up.md objection log</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 8 — First Close or Offer Update</h3>
      <div class="path-block">
        <strong>If a prospect is close to closing:</strong>
        <ul class="actions">
          <li><span class="checkbox"></span>Re-run the CLOSER Reinforce stage</li>
          <li><span class="checkbox"></span>Send the 9-word email if they've gone quiet</li>
          <li><span class="checkbox"></span>Trigger same-day onboarding message on close</li>
        </ul>
      </div>
      <div class="path-block">
        <strong>If no close yet:</strong>
        <ul class="actions">
          <li><span class="checkbox"></span>Review objection log — identify the most common doubt type</li>
          <li><span class="checkbox"></span>Run /alchemist to update offer.md (add a component, adjust guarantee, reframe the dream outcome)</li>
          <li><span class="checkbox"></span>Update the DM templates to reflect the refined offer</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- MONTH 3 -->
  <div class="month">
    <div class="month-header">
      Month 3: Close &amp; Compound <span class="month-goal">— Weeks 9–12</span>
      <div class="month-goal" style="font-size:13px;margin-top:4px;">Goal: 1 client closed, first result documented, referral sequence active.</div>
    </div>

    <div class="week">
      <h3>Weeks 9–10 — Close and Deliver</h3>
      <div class="context">[From sales.md: post-call email, onboarding message] [From follow-up.md: closed client sequence]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Send post-call follow-up within 5 minutes of every call</li>
        <li><span class="checkbox"></span>On close: send same-day onboarding message + kick off delivery</li>
        <li><span class="checkbox"></span>Schedule testimonial request for Day 14 of engagement (after first visible result)</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 11 — Proof &amp; Referrals</h3>
      <div class="context">[From follow-up.md: testimonial request, referral ask variants]</div>
      <ul class="actions">
        <li><span class="checkbox"></span>Send testimonial request after the first visible result — use the specific question format</li>
        <li><span class="checkbox"></span>Send 1 referral ask to the closed client (use Variant 1 — direct ask)</li>
        <li><span class="checkbox"></span>Document the client result for case study use</li>
      </ul>
    </div>

    <div class="week">
      <h3>Week 12 — 90-Day Review</h3>
      <ul class="actions">
        <li><span class="checkbox"></span>Review objection log (run /alchemist again if 5+ entries)</li>
        <li><span class="checkbox"></span>Count: outreach conversations started, calls booked, calls run, clients closed</li>
        <li><span class="checkbox"></span>Set next 90-day target: 3 more clients, or move to Rung 2 (audit/project scope)</li>
        <li><span class="checkbox"></span>Run /momentum again if relaunching with a different offer or niche</li>
      </ul>
    </div>
  </div>

  <!-- DAILY NON-NEGOTIABLES -->
  <div class="daily">
    <h2>Daily Non-Negotiables (From Week 4 Onward)</h2>
    <ul class="actions">
      <li><span class="checkbox"></span>[N] warm outreach touches using ACA (from outreach.md)</li>
      <li><span class="checkbox"></span>1 content unit published (Hook → Retain → Reward)</li>
      <li><span class="checkbox"></span>Check reply queue — move conversations forward</li>
      <li><span class="checkbox"></span>Log 1 objection or win</li>
    </ul>
  </div>

  <!-- FILES REFERENCE -->
  <div class="files-ref">
    <h2>Files in This Project</h2>
    <ul>
      <li><code>market.md</code> — Full market analysis and avatar</li>
      <li><code>offer.md</code> — Grand Slam Offer with value stack and guarantee</li>
      <li><code>outreach.md</code> — DM templates, content hooks, daily rhythm</li>
      <li><code>sales.md</code> — CLOSER talk track, pre-call brief, follow-up scripts</li>
      <li><code>follow-up.md</code> — Reactivation sequences, testimonial requests, objection log</li>
    </ul>
  </div>

</body>
</html>
```

Fill in all `[bracketed]` placeholders with the actual content extracted from the 5 output files. The HTML template above shows structure and styling — every section must contain real data from the agents, not placeholder text.

When generating the HTML: substitute `[PRIMARY]` with the actual hex value, `[PRIMARY_LIGHT]` with an rgba or hex tint of the primary color at ~8% opacity on white.

---

## Step 7: Final Report to User

After saving 90-day-plan.html, print a summary:

```
Done. Here's what was built:

Market: [Green/Amber/Red] — [niche statement]
Offer: [offer name] — [price]
Daily action: [N warm touches + 1 content unit]
90-day target: 1 closed client by Week 12

Files saved to: projects/momentum/[slug]/
  - profile.md
  - market.md
  - offer.md
  - outreach.md
  - sales.md
  - follow-up.md
  - 90-day-plan.html  ← open this in your browser

Start with 90-day-plan.html. Open it in any browser — it's organized by month, follow it in order.

Loop completed: Offer → Attention → Conversion → Delivery → Feedback
Run /client-onboard when your first client closes.
```

Tell the user: "Building your Week 1 sprint from the 90-day plan now."

```
Skill(skill="weekly-sprint", args="projects/momentum/[slug]/ auto")
```

After the Week 1 sprint is saved, tell the user: "Week 1 sprint saved to projects/momentum/[slug]/sprints/week-1.md — open it every Monday morning and run /weekly-sprint friday-report every Friday at 4PM."

---

## Hard Rules

- Never skip the intake. Even if $ARGUMENTS describes the business, confirm the 7 answers before proceeding.
- Never call the next agent until the current one has saved its output file.
- The 90-day-plan.html must be self-contained. Someone should be able to open it in a browser without any other files. No external CSS, CDN, or font links.
- Only the 90-day plan uses HTML output. All other output files (market.md, offer.md, outreach.md, sales.md, follow-up.md, profile.md) remain markdown.
- Do not add features, coaching, or extra commentary beyond what the 5 agents produce. The orchestrator compiles — it does not editorialize.
- If any agent fails or produces incomplete output: report the failure, explain what is missing, and ask the user whether to retry or proceed without that section.
