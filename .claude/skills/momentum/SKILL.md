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

Call the frontend-design skill to generate the visual design layer:

```
Skill(skill="frontend-design", args="Generate a production-grade, visually distinctive 90-day business plan dashboard in HTML. Design direction: choose one bold aesthetic (e.g. editorial, luxury minimal, modern brutalist — pick what fits best given the brand color [PRIMARY]). Required structure: (1) sticky tab navigation bar — first tab '90-Day Plan', additional tabs injected via <!-- TAB-BUTTONS-END --> comment; (2) cover hero block with plan title and one-line business description; (3) executive summary block; (4) 3 month sections (Month 1: Validate & Build, Month 2: Execute & Iterate, Month 3: Close & Compound), each with 3–4 week subsections — each week has a context paragraph and a checklist of action items with custom styled checkboxes; (5) a 'Daily Non-Negotiables' highlight block; (6) a files reference block at the bottom. Brand colors: PRIMARY=[PRIMARY hex], ACCENT=[ACCENT hex]. Typography: use Google Fonts @import — one beautiful, distinctive font for headings (no Inter, Roboto, Arial, or system fonts). CSS animations: subtle fade-in on sections, smooth tab switching, hover states on checklist items and week blocks. Self-contained: no external CSS or JS — Google Fonts @import is the only allowed external dependency. Include @media print rules that remove decorative elements and keep content clean. Insert these HTML comment injection points exactly as written: <!-- COVER-TITLE -->, <!-- COVER-META -->, <!-- EXEC-SUMMARY -->, <!-- MONTH-1-CONTENT -->, <!-- MONTH-2-CONTENT -->, <!-- MONTH-3-CONTENT -->, <!-- DAILY-ACTIONS -->, <!-- FILES-LIST -->, <!-- TAB-BUTTONS-END -->, <!-- TAB-CONTENT-END -->. Return the complete HTML shell with all CSS and JS — no bracketed placeholder text, only structural HTML, styles, and the comment injection points.")
```

After frontend-design returns the HTML shell, inject the real content from the 5 agent output files into each `<!-- COMMENT -->` slot:

- `<!-- COVER-TITLE -->` — the offer name from offer.md
- `<!-- COVER-META -->` — generated date + one-line business description from profile.md
- `<!-- EXEC-SUMMARY -->` — 4 sentences: validated niche, offer name + price, daily action rhythm, 90-day milestone
- `<!-- MONTH-1-CONTENT -->` — full Week 1–4 HTML (week blocks, context paragraphs, action checklists) drawn from market.md, offer.md, outreach.md
- `<!-- MONTH-2-CONTENT -->` — full Week 5–8 HTML drawn from outreach.md, sales.md
- `<!-- MONTH-3-CONTENT -->` — full Week 9–12 HTML drawn from sales.md, follow-up.md
- `<!-- DAILY-ACTIONS -->` — daily rhythm checklist from outreach.md (N touches, content unit, reply queue, objection log)
- `<!-- FILES-LIST -->` — list of all project files with one-line descriptions

Do not alter the CSS, layout, or JS returned by frontend-design. Only inject content into the designated comment slots.

Save the completed file as `projects/momentum/[slug]/90-day-plan.html`.

---

### 6c: Check for Extended Agent Files

After generating the base 90-Day Plan tab, check whether any extended agent output files exist in `projects/momentum/[slug]/`. For each that exists, add its tab to the HTML before saving.

**Tab insertion method (same method all extended skills use):**
1. Insert a tab button before `<!-- TAB-BUTTONS-END -->`:
   `<button class="tab-btn" data-tab="[tab-id]">[Label]</button>`
2. Insert a tab content block before `<!-- TAB-CONTENT-END -->`:
   `<div class="tab-content" id="tab-[tab-id]">[rendered HTML content]</div>`
3. If a tab with that `data-tab` ID already exists (re-compile), replace the content block rather than inserting again.

**Files to check and their tab IDs / labels:**

| File | Tab ID | Tab Label | Content to render |
|------|--------|-----------|-------------------|
| `brand-voice.md` | `brand-voice` | Brand Voice | Signature story, one-liner, content pillars, platform bios, tone guide, 7-11-4 audit — styled as cards with brand color headings |
| `funnel.md` | `funnel` | Funnel Strategy | Lead magnet options, landing page copy, email sequence, bio CTAs, weekly rhythm table, booking page brief — structured document |
| `funnel.md` (landing page section only) | `landing-page` | Landing Page | Extract only the landing page copy and render it as a proper full-width landing page (hero section, bullets, CTA button, trust line) — no tab chrome inside |
| `content-engine*.md` | `content-engine` | Content Engine | All platform posts (LinkedIn, TikTok script, Instagram captions, Skool), repurposing map, calendar — formatted with platform headers |
| `case-study*.md` | `case-study` | Case Study | Before/after layout, quote block, LinkedIn post preview, DM proof blocks — one-pager style |
| `onboarding.md` | `onboard` | Client Onboard | Welcome message, kick-off agenda, project brief, first-week checklist, communication cadence — section-by-section |

**Landing Page tab styling spec (when rendering the `landing-page` tab from funnel.md):**
The landing page tab content must look like an actual deployable landing page — not a document. Use these inner styles scoped to `#tab-landing-page`:
- Full-width hero block with `background: var(--primary)`, white headline text, subheadline
- White body section, max-width 640px, centered
- Benefit bullets as large check-list items
- Social proof block as a styled testimonial card with quote marks
- CTA button: `background: var(--primary)`, white text, large padding, border-radius 8px, full width on mobile
- Trust line below button in muted text
- No nav, no footer, no document headers

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
  - 90-day-plan.html  ← open this in your browser (tabbed dashboard — gains new tabs as extended agents run)

Start with 90-day-plan.html. Open it in any browser — it's organized by month, follow it in order. Each time you run an extended agent (/brand-voice, /funnel-architect, /content-engine, /case-study, /client-onboard) and pass this folder path, a new tab will be added to this file.

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
- The 90-day-plan.html must be self-contained. No external CSS, CDN, or JS. Google Fonts @import is the one allowed external dependency — it degrades gracefully offline and is the only practical way to use distinctive typography without embedding font data URIs.
- The 90-day-plan.html is the master tabbed dashboard. Core agent outputs (market.md, offer.md, outreach.md, sales.md, follow-up.md, profile.md) remain markdown only. Extended agents (brand-voice, funnel-architect, content-engine, case-study, client-onboard) add HTML tabs to this file when called with a Momentum project folder path. All extended agent outputs must also exist as .md files.
- Do not add features, coaching, or extra commentary beyond what the 5 agents produce. The orchestrator compiles — it does not editorialize.
- If any agent fails or produces incomplete output: report the failure, explain what is missing, and ask the user whether to retry or proceed without that section.
