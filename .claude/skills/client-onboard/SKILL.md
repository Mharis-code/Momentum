---
name: client-onboard
stage: delivery
description: Use when a client has just closed and you need to set up the first 7 days professionally. Takes a client description — outputs a welcome message, kick-off call agenda, project brief template, first-week milestone checklist, and communication cadence. Sets the professional tone that earns referrals. Standalone.
argument-hint: [describe the new client: name, what they hired you for, start date, any context | optionally append a Momentum project folder path to add output to 90-day-plan.html]
---

# Client Onboard — The Professional First 7 Days

## What This Skill Does

The first 7 days after a client closes are the most important for referral rate. A client who feels disorganized, confused, or uncertain in the first week rarely refers. A client who feels they made the right decision — that their onboarding was smoother than they expected — almost always refers.

This skill builds the onboarding system that makes a solopreneur look like a professional operator from day one. Not because of templates, but because the right things happen at the right time, with the right tone.

**What you get:**
- Welcome message — sent within 1 hour of the signed agreement or verbal close
- Kick-off call agenda — structure for the first working call
- Project brief template — the document that aligns on scope, deliverables, and success criteria before work begins
- First-week milestone checklist — what needs to happen in days 1–7
- Communication cadence — how often to check in, through what channel, and with what format

**Saved to:** `projects/clients/[client-slug]/onboarding.md`

---

## Embedded Knowledge — Delivery Matches the Promise

From Hormozi ($100M Offers): the offer only works if delivery matches the promise. Client perception of whether they over-paid or under-paid is set in the first week — not at the end of the engagement. A client who feels over-delivered-to refers. A client who feels let down goes quiet. The referral ask in Loop Engine only activates if delivery has already earned it.

From Priestley (Oversubscribed): professional delivery is part of maintaining the oversubscribed flywheel. Satisfied clients generate demand for the next client — they become social proof, referral sources, and case studies. Onboarding is not a logistics step. It is the beginning of the next client acquisition cycle.

The first 7 days are not about delivering results. They are about confirming the decision. The client is still running a post-purchase evaluation — "did I make the right call?" — in the first week. Everything in the onboarding is designed to answer that question: yes.

**The three onboarding jobs:**
1. **Confirm the decision** — welcome them, restate what they can expect, set the first milestone
2. **Reduce uncertainty** — give them a clear picture of what happens next; remove unknowns
3. **Earn the right to ask for referrals** — the referral ask in Loop Engine only works if the client has already had a positive first experience

**Tone for all onboarding communication:**
- Warm but professional
- Specific — name the thing, name the date, name the next step
- No ambiguity — every message should end with exactly one next action and exactly one person responsible for it
- Confident — you've done this before (even if this is the first time)

---

## Step 1: Handle Arguments

**If $ARGUMENTS describes a new client:**
- Extract: client name, what they hired you for, start date (if known), any context about the engagement
- Proceed to Step 2

**If $ARGUMENTS is empty:**
- Ask: "Tell me about the new client. What's their name, what did they hire you to do, and when do you start? Any other context I should know?"

---

## Step 2: Write the Welcome Message

Send within 1 hour of close (same day at minimum).

Structure:
1. **Opening:** Genuine, specific welcome. Reference what they hired you for.
2. **Confirmation:** Restate what they can expect: the timeline, the first deliverable, and when they'll hear from you next.
3. **Next step:** One clear action item for each person. What do you need from them, and by when? What will you do next, and by when?
4. **Tone close:** Short, warm, professional. Not a wall of text.

Template (customize for each client):

```
Subject: Welcome — here's what happens next

Hi [Name],

Really glad you're in. Here's what I want you to know right away:

[What you'll deliver and by when — one sentence]

To get started, I need [specific thing from client] by [date]. I'll [specific thing you'll do] by [date].

I'll send a calendar invite for our kick-off call shortly — [proposed time or ask for availability].

Looking forward to working together.

[Your name]
```

Rules:
- Subject line must be clear, not clever. "Welcome" or "Next steps" beats a witty subject.
- Never send more than 3 action items in the welcome message. Overwhelm kills momentum.
- The welcome message is not the place to rehash the contract or re-explain the offer. That was the sales call. This is the start line.

---

## Step 3: Write the Kick-Off Call Agenda

The kick-off call aligns on scope, sets expectations, and establishes the working relationship. It is not a second sales call. It is the start of delivery.

Length: 45–60 minutes.

**Agenda:**

```
Kick-Off Call Agenda — [Client Name] + [Your Name]

Duration: 45–60 minutes
Date: [to be scheduled]

---

1. Welcome & quick re-alignment (5 min)
   - Restate the engagement scope in one paragraph
   - Confirm the start date and target completion date
   - Ask: "Does this match what you understood when we agreed to work together?"

2. Current state deep-dive (15–20 min)
   - [Specific diagnostic questions based on the engagement type]
   - Walk through their current workflow / system / situation
   - Note: listen more than talk here. This is your intake session.

3. Success criteria (10 min)
   - Ask: "90 days from now, what would need to be true for you to feel this was worth it?"
   - Confirm 1–2 measurable outcomes
   - Write these down and read them back

4. Immediate next steps (5 min)
   - What you need from them (and by when)
   - What they can expect from you (and by when)
   - Confirm communication channel (email, DM, Slack, etc.)

5. Questions (5 min)
   - Open floor: "What questions do you have for me right now?"
```

Write the diagnostic questions for Step 2 based on the engagement type provided. These should be specific to the work — not generic discovery questions, but "what does your current [specific workflow] look like, step by step?"

---

## Step 4: Write the Project Brief Template

A project brief is the one document both sides sign off on before work begins. It eliminates scope creep and sets the success criteria before the first deliverable is touched.

```
# Project Brief — [Project Name]
**Date:** YYYY-MM-DD
**Client:** [Name / Company]
**Consultant:** [Your Name]

---

## Engagement Summary
[2–3 sentences: what is being built or delivered, and why]

## Scope
**Included:**
- [Deliverable 1]
- [Deliverable 2]
- [Deliverable 3]

**Not included (out of scope):**
- [Thing 1 that was NOT agreed to]
- [Thing 2 that was NOT agreed to]

## Success Criteria
At the end of this engagement, we will consider the work complete when:
1. [Specific measurable outcome 1]
2. [Specific measurable outcome 2]

## Timeline
| Milestone | Owner | Due Date |
|-----------|-------|----------|
| Kick-off call | Both | [Date] |
| [Milestone 1] | [You] | [Date] |
| [Milestone 2] | [You/Client] | [Date] |
| Final delivery | [You] | [Date] |
| Review + sign-off | Client | [Date] |

## Communication
- Primary channel: [Email / Slack / WhatsApp / etc.]
- Check-in frequency: [Weekly call / Async updates on Fridays / etc.]
- Response time: [You respond within 24 hours on business days; client same]

## Payment
- Agreed fee: [Amount]
- Payment schedule: [Upfront / 50-50 / Monthly]
- Invoice date: [Date(s)]

---

Client signature: _________________________ Date: _______
Consultant signature: _____________________ Date: _______
```

Fill in the scope and success criteria based on what was described in $ARGUMENTS. Leave milestone dates as placeholders to be confirmed on the kick-off call.

---

## Step 5: Write the First-Week Milestone Checklist

A simple checklist of what needs to happen in days 1–7 to start the engagement right. Split by owner.

```
# First-Week Checklist — [Client Name]

## Your Tasks (Consultant)
- [ ] Day 0: Send welcome message
- [ ] Day 0–1: Send kick-off call invite
- [ ] Day 0–1: Share project brief for review
- [ ] Day 1–2: [First substantive action based on engagement type]
- [ ] Day 3–5: Kick-off call completed
- [ ] Day 5–7: First progress update sent (even if just one sentence)

## Client Tasks
- [ ] Day 0–1: Provide [specific thing needed from them]
- [ ] Day 1–3: Review and sign off on project brief
- [ ] Day 3–5: Attend kick-off call
- [ ] Day 5–7: Confirm [specific decision or access needed]
```

Write the client-specific tasks based on what the engagement requires.

---

## Step 6: Define the Communication Cadence

Clear rules for the working relationship prevent the most common source of client frustration: not knowing what's happening.

**During the engagement:**
- **Weekly async update** — every Friday, send a 3-sentence progress note: what was done this week, what's next, and one thing (if any) you need from them. Even if nothing changed, send it.
- **Milestone updates** — when a milestone is hit, send a one-paragraph note naming the milestone, what was delivered, and the next step.
- **Response time commitment** — state clearly: "I respond to messages on business days within 24 hours. If something is urgent, mark it URGENT in the subject line and I'll get back to you within 4 hours."

**For the client:**
- Set clear expectations about what they need to provide and when. If they go quiet, you will send one prompt, then move on and note the delay.

Write a one-paragraph communication norms note to include in the project brief or send separately.

---

## Step 7: Save Output

Save to: `projects/clients/[client-slug]/onboarding.md`

File format:

```
# Client Onboarding — [Client Name]
**Engagement:** [What was sold]
**Start date:** [Date]
**Project folder:** projects/clients/[slug]/

---

## Welcome Message
[Full message text]

## Kick-Off Call Agenda
[Full agenda]

## Project Brief
[Full template — filled in]

## First-Week Checklist
[Full checklist]

## Communication Cadence
[Norms paragraph]
```

Tell the user the file path. Remind them to send the welcome message today — not tomorrow, not after the kick-off call is scheduled. Same-day welcome messages set the tone that all subsequent communication will match.

---

## Step 8: Generate HTML Output

**Detect Momentum context:**
- If `$ARGUMENTS` contained a path to a Momentum project folder (a folder containing `90-day-plan.html`), set `IS_MOMENTUM=true` and `MOMENTUM_FOLDER=[that path]`
- If IS_MOMENTUM=true, also save the onboarding content to `[MOMENTUM_FOLDER]/onboarding.md`

**Generate the HTML:**

Determine the brand primary color: if IS_MOMENTUM=true, read the `--primary` CSS variable from `[MOMENTUM_FOLDER]/90-day-plan.html`; otherwise use `#1B6CA8`.

Sections to include:
- **Welcome Message** — styled email preview card (white card, email subject line as header, body text with subtle border-left accent)
- **Kick-Off Call Agenda** — vertical timeline layout: numbered steps with time allocations, each step in a card
- **Project Brief** — form-style layout with labeled sections (Scope, Success Criteria, Timeline as HTML table, Communication, Payment), signature lines at the bottom
- **First-Week Checklist** — two columns side by side labeled "Consultant" and "Client", each item as a checkbox row
- **Communication Cadence** — rules block styled as a summary card

**If standalone mode (IS_MOMENTUM=false):**
Call the frontend-design skill to generate the full HTML:
```
Skill(skill="frontend-design", args="Generate a production-grade, visually distinctive client onboarding kit in HTML — a clean, professional reference document a consultant can open during and between client calls. Design direction: choose a structured, trustworthy aesthetic (e.g. premium consulting or modern professional). Brand color: PRIMARY=[resolved color hex]. Required sections: Welcome Message (styled email preview card — white card, email subject line as header, body text with subtle border-left accent), Kick-Off Call Agenda (vertical timeline — numbered steps with time allocations, each step in a card), Project Brief (form-style layout with labeled sections for Scope, Success Criteria, Timeline as HTML table, Communication, Payment — signature lines at the bottom), First-Week Checklist (two columns labeled 'Consultant' and 'Client', each item as a checkbox row), Communication Cadence (rules block styled as a summary card). Typography: Google Fonts @import — one distinctive heading font, no Inter, Roboto, or system fonts. CSS animations: subtle fade-in on sections, hover states on cards. Self-contained: no external CSS or JS — Google Fonts @import is the only allowed external dependency. Insert <!-- SECTION-NAME --> HTML comments as injection points for each section. Return the complete HTML shell with all CSS and structure — no bracketed placeholder text.")
```
After frontend-design returns the shell, fill in every `<!-- SECTION-NAME -->` injection point with the real onboarding content.
Save as `projects/clients/[client-slug]/onboarding.html`. Tell the user the path.

**If Momentum tab mode (IS_MOMENTUM=true):**
Generate the tab content as an HTML fragment (not a full `<!DOCTYPE html>` document). Use the CSS variables already defined in the parent `90-day-plan.html`: `--primary`, `--accent`, `--text`, `--text-muted`, `--bg`, `--border`, `--primary-light`. Scope any additional styles inside a `<style>` block with selectors prefixed by `#tab-onboard` to avoid bleeding into other tabs. Do not redeclare the base font, colors, or layout variables — they are inherited from the parent. Render all 5 sections listed above.

Then update 90-day-plan.html:
1. Read `[MOMENTUM_FOLDER]/90-day-plan.html`
2. Find `<!-- TAB-BUTTONS-END -->` and insert before it:
   `<button class="tab-btn" data-tab="onboard">Client Onboard</button>`
3. Find `<!-- TAB-CONTENT-END -->` and insert before it the fragment wrapped in:
   `<div class="tab-content" id="tab-onboard">[rendered HTML fragment]</div>`
4. If `data-tab="onboard"` already exists (re-run), replace the existing content block.
5. Save the modified `90-day-plan.html`.
6. Tell the user: "Client Onboard tab added to 90-day-plan.html."

---

## Hard Rules

- The welcome message must be sent same day as close. Not next week. Not after the contract is fully signed if there's a verbal agreement. The moment they say yes, the onboarding begins.
- The kick-off call agenda must include a "success criteria" section. Closing without confirmed success criteria is the #1 cause of scope disputes.
- The project brief must list what is NOT included (out of scope). Most scope creep comes from ambiguity, not bad faith. Closing the ambiguity early is the consultant's job.
- Every communication should end with exactly one next step and exactly one person responsible. "Let me know if you have questions" is not a next step.
- The first-week checklist is not a guarantee of delivery. It is a minimum. If the engagement allows, do more. But never do less.
