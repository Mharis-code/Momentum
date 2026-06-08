---
name: funnel-architect
stage: attention
description: Use when building a lead gen funnel that converts content viewers into discovery call bookings. Takes a Momentum project folder path or offer/avatar description — outputs a lead magnet concept, landing page copy, 5-email welcome sequence, platform bio CTAs, weekly posting rhythm, and a booking page brief. Bridges the gap between content (Amplifier) and sales (Converter). Standalone or called after /momentum.
argument-hint: [path to momentum project folder, OR describe your offer and ideal customer]
---

# Funnel Architect — Convert Viewers to Booked Calls

## What This Skill Does

Funnel Architect builds the conversion layer between "people who see your content" and "people who book a call with you." Most solopreneurs stop at content and outreach and wonder why they're not getting inquiries. The gap is the funnel: the lead magnet that earns the email address, the welcome sequence that builds enough trust to book, and the bio CTAs that send every new follower toward a low-friction first step.

This agent is the bridge. Amplifier gets you visible. Funnel Architect captures that visibility and turns it into booked calls.

**What you get:**
- A lead magnet concept — one specific, high-value giveaway matched to the avatar's #1 pain
- Landing page copy — headline, 3 benefit bullets, social proof placeholder, single CTA
- 5-email welcome sequence — Day 0 through Day 8, ending with a soft discovery call ask
- Platform bio CTAs — platform-specific one-liners that drive every new follower to the lead magnet
- Weekly posting rhythm — Mon/Wed/Fri cadence tied to campaign phases
- Booking page brief — what to put on the Calendly or booking page to qualify leads before the call

**Saved to:** `projects/momentum/[slug]/funnel.md` (if called from Momentum) OR `projects/funnels/[slug]/funnel.md` (if standalone)

---

## Embedded Knowledge — Priestley's Campaign-Driven Enterprise

Daniel Priestley's Campaign-Driven Enterprise identifies three operating rhythms for a solo business:

### The Three Rhythms

**Weekly micro-campaigns (70% of revenue):**
The engine that runs continuously. Three posts per week in a consistent rhythm:
- Monday: authority post (teach, explain, prove expertise)
- Wednesday: engagement post (question, opinion, story — invites response)
- Friday: CTA post (soft offer, lead magnet, invite to book)

This rhythm runs regardless of what else is happening. It is the minimum baseline for staying visible and building the 7-11-4 threshold with the audience.

**Quarterly spotlight campaigns (30% of revenue):**
A bigger event every 90 days: a workshop, a challenge, a case study drop, a masterclass, a limited-offer window. These generate spikes in attention and conversions above the weekly baseline.

Five phases of a quarterly campaign:
1. **Planning** — define the hook, the mechanism, the outcome, and the offer
2. **Build-up** — 3–4 weeks of content that seeds demand without announcing the event
3. **Oversubscribed release** — announce with scarcity ("limited spots," "first 10 people get X")
4. **Follow-through** — deliver, over-deliver, collect testimonials
5. **Celebrate/Innovate** — share results publicly, compound the proof, decide what to run next

**Annual big-message (positioning anchor):**
One annual theme that all content and campaigns build toward. It is the mountain everyone is climbing. Example: "The Year of the AI OS" — all content in the year points toward one big idea.

### Product-for-Prospects vs. Core Offering

Every business needs two things:
- **Core offering** — the main service or product (DFY, DWY, project, retainer)
- **Product-for-prospects** — a low-friction, free or cheap entry point that demonstrates value before any commitment is asked

The product-for-prospects is the lead magnet. Its job is NOT to generate revenue. Its job is to move strangers from "I've seen this person online" to "I've gotten real value from them." Once that shift happens, the discovery call ask feels natural, not pushy.

A strong product-for-prospects:
- Solves one specific problem the ideal client has right now
- Can be consumed in under 30 minutes
- Delivers a real win, not just information
- Makes the person think: "If this was free, what is the paid version like?"

---

## Embedded Knowledge — Hormozi Core Four (Funnel Application)

Hormozi's Core Four defines the priority order for lead generation:

1. **Warm outreach first** — People who already know you. Fastest to convert.
2. **Free content second** — The 7-11-4 accumulation engine. Takes time to compound but compounds forever.
3. **Cold outreach third** — Strangers. Lower conversion rate; higher volume required. Use after warm is exhausted.
4. **Paid ads last** — Only after organic systems are validated. Never before.

The funnel sits at the intersection of Step 2 and Step 1: content builds the audience (warm), and the funnel captures the warmest members of that audience before they go cold again. The lead magnet is the net. The welcome sequence is the rope that pulls them closer.

Without the funnel, content builds an audience that never converts. The viewer likes the post, moves on, and never books. The lead magnet is the reason to give an email address. The welcome sequence is the reason to book the call.

---

## Step 1: Handle Arguments

**If $ARGUMENTS contains a Momentum project folder path:**
- Read `[folder]/profile.md` for the intake answers
- Read `[folder]/offer.md` for the offer name, dream outcome, guarantee, and value stack
- Read `[folder]/market.md` for the avatar, their exact pain language, and where they gather online
- Set `output_folder` to `[folder]/funnel.md`
- Set `slug` from the existing folder name

**If $ARGUMENTS is a plain description (offer + avatar):**
- Extract: offer name (or working title), avatar description, target price, avatar's #1 pain
- Ask any clarifying questions before proceeding
- Set `output_folder` to `projects/funnels/[slug]/funnel.md`

**If $ARGUMENTS is empty:**
- Ask: "Describe your offer and your ideal customer in a sentence or two. Or pass the path to a Momentum project folder (e.g., `projects/momentum/your-slug/`)."

---

## Step 2: Build the Lead Magnet Concept

A lead magnet is not a PDF of everything you know. It is the one-specific-thing that solves the avatar's most immediate, recognizable problem in under 30 minutes.

**To find the right lead magnet, ask:**
1. What is the avatar's most painful, urgent, and frequently-searched problem right now?
2. What is one specific result you can deliver in 20–30 minutes that they would immediately recognize as valuable?
3. What quick win would make them think "if this was free, what is the paid version like?"

**Lead magnet formats (choose the simplest that works):**
- **Checklist** — "The 7-step AI OS Setup Checklist for Solopreneurs" (15 min to use)
- **Template** — "The Client Onboarding Template I Use for Every New Client" (use immediately)
- **Mini guide** — "The 3 AI Workflows Every Solopreneur Should Automate First" (20 min to read)
- **Video walkthrough** — "Watch Me Set Up a 10-Minute AI System for a Bookkeeper" (15 min to watch)
- **Scorecard** — "Rate Your AI Readiness in 5 Minutes" (interactive, self-qualifying)

**Do not use:**
- Ebooks over 20 pages (they don't get read)
- Generic "Ultimate Guides" (not specific enough to feel like a win)
- Webinars longer than 45 minutes (too much commitment for a cold lead)

Generate 2–3 lead magnet options with a one-line explanation of why each one works. Mark the recommended option.

---

## Step 3: Write the Landing Page Copy

The landing page exists to convert: a visitor arrives, reads the page, and either leaves their email or leaves. Nothing else should be on the page.

**Structure:**

**Headline (1 line):**
The dream outcome, stated as a result the avatar wants. Use their exact language from the avatar profile.
Formula: "[Specific result] in [time frame] — for [specific avatar]"
Example: "Build an AI system that saves you 5 hours a week — even if you've never used Claude before"

**Subheadline (1–2 lines):**
What they'll get and how. Make the low-friction nature clear.
Example: "Free checklist: 7 steps to set up your AI OS before the end of the week"

**3 Benefit Bullets:**
Each bullet = one specific thing they get + why it matters. Lead with the outcome, not the feature.
- "A step-by-step setup guide — so you know exactly what to build first"
- "The 3 workflows most solopreneurs skip — and why skipping them costs 2+ hours/week"
- "A done-in-20-minutes template — so you can implement today, not someday"

**Social Proof Placeholder:**
A line that will hold a testimonial or result once one exists. Write it as a bracket note: "[Insert testimonial from [avatar type] after using the lead magnet]"

**CTA Button:**
One action. No navigation, no other links. The button text should complete the sentence "I want to ___."
Examples: "Get the free checklist," "Download the template," "Show me the 3 workflows"

**Below-fold trust line (optional):**
One line that removes friction. "No spam. Unsubscribe any time." or "Instant access — no sales call required."

---

## Step 4: Write the 5-Email Welcome Sequence

Each email has one job. Send them in order, spaced as specified.

**Email 1 — Day 0: Deliver**
Send immediately after opt-in.
- Subject: "Here's [lead magnet name] — plus one thing most people miss"
- Deliver the lead magnet (link or attached)
- Add one tip that goes beyond the lead magnet (builds goodwill immediately)
- CTA: none — just deliver
- Length: 150–200 words

**Email 2 — Day 2: Story**
- Subject: "Why I built this (the honest version)"
- Tell the origin story from the signature story (compressed to 150 words)
- Connect the story to the lead magnet — why did you create this specific resource?
- CTA: soft reply ask ("What's the biggest thing you're trying to figure out with AI right now?")
- Length: 150–250 words

**Email 3 — Day 4: Insight**
- Subject: "The thing nobody tells you about [avatar's core problem]"
- Deliver one counterintuitive insight or framework relevant to the avatar
- This is a pure value email — no offer, no CTA beyond "hit reply if this resonates"
- Length: 200–300 words

**Email 4 — Day 6: Case Study / Proof**
- Subject: "What happened when [client type] [did the thing]"
- Share a result: a client's outcome, your own result, or a documented example
- Be specific: hours saved, cost reduced, revenue gained
- End with: "I help [avatar type] do [specific thing]. If that's relevant to where you are right now, here's how to explore it further: [link to booking page]"
- CTA: link to booking page
- Length: 200–300 words

**Email 5 — Day 8: Soft Ask**
- Subject: "One question before I move on"
- Reference the lead magnet they downloaded — "You grabbed [X] 8 days ago"
- Ask one direct question: "Have you had a chance to use it? What came up?"
- Include a low-friction invitation: "If you're at the point where you want to build this with help, I have [N] spots open for a free 20-minute AI OS call. Here's how to grab one: [booking link]"
- CTA: booking link
- Length: 100–150 words — short on purpose

Write the full text of all 5 emails with subject lines. Use the avatar's exact pain language throughout.

---

## Step 5: Write Platform Bio CTAs

For each platform, write a bio update that ends with a CTA pointing to the lead magnet.

**LinkedIn Headline update:**
Existing positioning one-liner + "| Free [lead magnet name] below"

**TikTok Bio (160 chars max):**
"[What you do for who] + Get the free [lead magnet name]: [link placeholder]"

**Instagram Bio (150 chars max):**
"[Positioning one-liner] + Free [lead magnet name] in bio"

**Skool Bio (250 chars max):**
"[Peer framing — what you know and share] + [Link to lead magnet]"

Flag if any exceed character limits.

---

## Step 6: Write the Weekly Posting Rhythm

Based on Priestley's three-post-per-week micro-campaign rhythm:

**Monday — Authority Post:**
Topic: something that demonstrates expertise or disproves a common myth in the niche
Goal: build trust with new followers
Format: LinkedIn post (use /content-engine to produce full version)
No CTA — pure value

**Wednesday — Engagement Post:**
Topic: a question, opinion, or "agree or disagree?" that the avatar has strong feelings about
Goal: generate comments and replies (11-interaction accumulation)
Format: short LinkedIn post or TikTok
CTA: "Comment below" or "Reply and tell me"

**Friday — CTA Post:**
Topic: a result, a case study, or a reminder of the transformation you help with
Goal: drive to the lead magnet or booking page
Format: LinkedIn post or Instagram story
CTA: direct link to lead magnet or "DM me [keyword] for the link"

Generate 4 weeks of topic suggestions for the Mon/Wed/Fri rhythm, based on the offer and content pillars. Leave the full post copy blank — use /content-engine to write each piece.

---

## Step 7: Write the Booking Page Brief

The booking page (Calendly, TidyCal, or equivalent) is the last step before a discovery call. It should do two things: qualify the prospect and set expectations.

**Page title:**
"[Offer name] — Free Discovery Call" or "AI OS Strategy Call — [Your Name]"

**What to include:**
1. **One-line description** of what the call covers (not "meet and chat" — "30-minute session where we map your biggest operational bottleneck and identify the AI workflow that would fix it first")
2. **Who this call is for** — 2–3 bullet points describing the ideal candidate. This pre-qualifies. Anyone who doesn't fit those bullets should self-select out.
3. **What to expect** — 3 bullet points: what you'll cover, what they'll get, what comes after if it's a fit
4. **A pre-call question** — one question in the booking form: "What's the biggest thing you're trying to solve right now?" This warms up the conversation before the call starts.

Write the full booking page copy.

---

## Step 8: Save Output

Save to: `projects/momentum/[slug]/funnel.md` OR `projects/funnels/[slug]/funnel.md`

File format:

```
# Funnel — [Offer Name]

## Lead Magnet
**Selected option:** [name + format]
**Why it works:** [one sentence]

## Landing Page Copy
### Headline
[Text]

### Subheadline
[Text]

### 3 Benefit Bullets
- [Bullet 1]
- [Bullet 2]
- [Bullet 3]

### CTA Button
[Text]

## Welcome Sequence

### Email 1 — Day 0
Subject: [Subject]
[Full email body]

[Repeat for emails 2–5]

## Platform Bio CTAs
**LinkedIn Headline:** [Text]
**TikTok:** [Text — char count]
**Instagram:** [Text — char count]
**Skool:** [Text — char count]

## Weekly Rhythm — 4-Week Topic Plan
| Week | Monday (Authority) | Wednesday (Engagement) | Friday (CTA) |
|------|-------------------|----------------------|-------------|
| 1 | [Topic] | [Topic] | [Topic] |
[...]

## Booking Page Copy
[Full page brief]
```

Tell the user the file path. Remind them that to produce the actual posts for the weekly rhythm, they should run `/content-engine [topic]` for each Monday/Wednesday/Friday topic.

---

## Step 9: Generate HTML Outputs

This step produces TWO HTML outputs: a Funnel Strategy document and a standalone Landing Page.

**Detect Momentum context:**
- If `$ARGUMENTS` contained a path to a Momentum project folder (a folder containing `90-day-plan.html`), set `IS_MOMENTUM=true` and `MOMENTUM_FOLDER=[that path]`

**Read brand color:** If IS_MOMENTUM=true, check `[MOMENTUM_FOLDER]/90-day-plan.html` for the `--primary` CSS variable. Use that value as `PRIMARY`. If not found, use `#1B6CA8`.

---

### Output A — Funnel Strategy HTML

A styled reference document with all funnel components. Self-contained, no external dependencies.

Sections to render:
- **Lead Magnet** — selected option in a callout card (name, format, why it works), dismissed options below in muted text
- **Landing Page Copy** — headline as large text, subheadline, 3 benefit bullets, social proof placeholder styled as a testimonial card, CTA button text, trust line
- **Welcome Sequence** — 5 email cards, one per day, each with subject line in bold and body text
- **Platform Bio CTAs** — card per platform with character count badge
- **Weekly Posting Rhythm** — the 4-week Mon/Wed/Fri table rendered as an HTML table
- **Booking Page Brief** — formatted as a spec card with all sections

**If IS_MOMENTUM=true — insert Funnel Strategy tab into 90-day-plan.html:**
1. Read `[MOMENTUM_FOLDER]/90-day-plan.html`
2. Find `<!-- TAB-BUTTONS-END -->` and insert before it:
   `<button class="tab-btn" data-tab="funnel">Funnel Strategy</button>`
3. Find `<!-- TAB-CONTENT-END -->` and insert before it the Funnel Strategy HTML wrapped in:
   `<div class="tab-content" id="tab-funnel">[funnel strategy content]</div>`
4. If `data-tab="funnel"` already exists (re-run), replace the existing content block.

**If standalone:** Save as `[output_folder]/funnel-strategy.html`

---

### Output B — Landing Page HTML

A proper, deployable landing page built from the landing page copy written in Step 3. It must look like an actual product landing page — not a document, not a dashboard.

**Landing page structure and styling:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>[Lead Magnet Name] — [Your Name]</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: system-ui, -apple-system, sans-serif; color: #111827; background: #fff; }

    .lp-hero {
      background: [PRIMARY];
      color: #fff;
      padding: 80px 24px 72px;
      text-align: center;
    }
    .lp-hero h1 {
      font-size: clamp(28px, 5vw, 48px);
      font-weight: 800;
      line-height: 1.15;
      max-width: 720px;
      margin: 0 auto 20px;
    }
    .lp-hero p {
      font-size: clamp(16px, 2.5vw, 20px);
      opacity: 0.85;
      max-width: 560px;
      margin: 0 auto;
      line-height: 1.6;
    }

    .lp-body {
      max-width: 640px;
      margin: 0 auto;
      padding: 64px 24px;
    }

    .lp-bullets { list-style: none; margin: 0 0 48px; }
    .lp-bullets li {
      display: flex;
      align-items: flex-start;
      gap: 14px;
      padding: 16px 0;
      border-bottom: 1px solid #e5e7eb;
      font-size: 17px;
      line-height: 1.6;
    }
    .lp-bullets li:last-child { border-bottom: none; }
    .lp-check {
      flex-shrink: 0;
      width: 24px;
      height: 24px;
      background: [PRIMARY];
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 2px;
    }
    .lp-check::after {
      content: '';
      width: 10px;
      height: 6px;
      border-left: 2px solid #fff;
      border-bottom: 2px solid #fff;
      transform: rotate(-45deg) translate(1px, -1px);
    }

    .lp-testimonial {
      background: #f9fafb;
      border-left: 4px solid [PRIMARY];
      padding: 24px 28px;
      border-radius: 0 8px 8px 0;
      margin: 0 0 48px;
    }
    .lp-testimonial blockquote {
      font-size: 17px;
      line-height: 1.7;
      font-style: italic;
      color: #374151;
      margin-bottom: 12px;
    }
    .lp-testimonial cite { font-size: 14px; color: #6b7280; font-style: normal; }

    .lp-cta-wrap { text-align: center; margin-bottom: 16px; }
    .lp-cta {
      display: inline-block;
      background: [PRIMARY];
      color: #fff;
      font-size: 18px;
      font-weight: 700;
      padding: 18px 48px;
      border-radius: 8px;
      text-decoration: none;
      width: 100%;
      max-width: 400px;
    }
    .lp-trust {
      text-align: center;
      font-size: 13px;
      color: #9ca3af;
      margin-top: 12px;
    }

    @media (max-width: 600px) {
      .lp-hero { padding: 56px 20px 48px; }
      .lp-body { padding: 48px 20px; }
    }
  </style>
</head>
<body>

  <div class="lp-hero">
    <h1>[Headline from Step 3]</h1>
    <p>[Subheadline from Step 3]</p>
  </div>

  <div class="lp-body">
    <ul class="lp-bullets">
      <li><span class="lp-check"></span>[Benefit bullet 1 from Step 3]</li>
      <li><span class="lp-check"></span>[Benefit bullet 2 from Step 3]</li>
      <li><span class="lp-check"></span>[Benefit bullet 3 from Step 3]</li>
    </ul>

    <div class="lp-testimonial">
      <blockquote>[Social proof placeholder text from Step 3 — use "Insert testimonial here" styling]</blockquote>
      <cite>[Avatar type] — [role/niche]</cite>
    </div>

    <div class="lp-cta-wrap">
      <a href="#" class="lp-cta">[CTA button text from Step 3]</a>
    </div>
    <p class="lp-trust">[Trust line from Step 3]</p>
  </div>

</body>
</html>
```

Fill in all `[bracketed]` placeholders with the actual content from Step 3. Substitute `[PRIMARY]` with the actual hex value.

**If IS_MOMENTUM=true — insert Landing Page tab into 90-day-plan.html:**
1. The landing page must look like an actual landing page inside the tab — use an `<iframe srcdoc="...">` to isolate its styles from the dashboard. Set the iframe to `width: 100%; height: 90vh; border: none;` and pass the full landing page HTML as the `srcdoc` attribute (HTML-encoded). OR embed the landing page HTML directly inside `<div class="tab-content" id="tab-landing-page">` with scoped styles (prefix all classes with `.tab-landing-page` to avoid conflicts).
2. Preferred approach: direct embed with scoped styles (prefix every landing page CSS class with `#tab-landing-page ` so styles don't bleed into other tabs).
3. Find `<!-- TAB-BUTTONS-END -->` and insert before it:
   `<button class="tab-btn" data-tab="landing-page">Landing Page</button>`
4. Find `<!-- TAB-CONTENT-END -->` and insert before it the scoped landing page HTML wrapped in:
   `<div class="tab-content" id="tab-landing-page" style="padding:0;">[scoped landing page HTML]</div>`
5. If tabs already exist, replace rather than insert.
6. Save the modified `90-day-plan.html`.
7. Tell the user: "Funnel Strategy and Landing Page tabs added to 90-day-plan.html."

**If standalone (no Momentum folder):**
- Save landing page as `[output_folder]/landing-page.html`
- Tell the user the paths for both `funnel-strategy.html` and `landing-page.html`.

---

## Hard Rules

- The lead magnet must solve one specific problem. Never propose a generic "ultimate guide" or "complete overview." If you cannot name the specific pain it solves in one sentence, the concept is too broad.
- The landing page must have exactly one CTA. No navigation links, no "learn more" buttons, no secondary offers.
- Email 5 (the soft ask) must be short — 100–150 words maximum. Its brevity is the mechanism. A long ask email reads as desperation.
- Every email must have a subject line. Write it as something the ideal client would actually open.
- The weekly rhythm must follow the Mon/Wed/Fri structure. The Monday post is authority — never CTA. The Friday post is CTA — never pure education. Swapping these breaks the pattern.
- If the avatar pain language is unavailable (no market.md, no description provided), ask for it before writing the landing page or email sequence. Generic pain language produces generic copy.
