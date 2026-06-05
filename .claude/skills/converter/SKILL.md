---
name: converter
stage: conversion
description: Use when running the fourth stage of the Momentum System — builds the sales system to turn conversations into closed clients. Produces a CLOSER talk track for the specific offer, a pre-call brief template, and post-call follow-up scripts. Can be run standalone or called by /momentum. No external dependencies — all knowledge is embedded.
argument-hint: [path to output folder]
---

# Converter — Turn Conversations Into Closed Clients

## What This Skill Does

Converter is Agent 4 of the Momentum System. It reads the built offer (Alchemist) and the outreach engine (Amplifier) and builds the complete sales system: a CLOSER talk track specific to this offer, consultative opening framework, objection responses mapped to the offer's obstacle list, a pre-call brief template, a post-call follow-up email, and a same-day onboarding message. Saves `sales.md` to the project folder.

---

## Hormozi Knowledge — Sales Frameworks

### The CLOSER Framework

Six stages, in order. Do not skip stages. Each stage must be completed before moving to the next.

**C — Clarify:** Why are they on the call today? What prompted them to reach out? Listen for the pressure (fear of being left behind, missed revenue, overwhelm, competitor doing something they aren't). Do not pitch. Diagnose.

**L — Label:** Repeat their problem back in their own words. "So what I'm hearing is [their language]. Is that right?" This confirms you understood and makes them feel heard before you suggest anything.

**O — Overview:** What have they tried before? Why didn't it work? Two purposes: shows you respect their history, and pre-empts the "I'll just do it myself" objection by surfacing why DIY has already failed.

**S — Sell the Vacation:** Introduce the dream outcome now — not the features, not the process, the destination. "What I want to walk you toward is [vivid dream outcome]." Make it specific to their situation using the language they used in C and L.

**E — Explain Away:** Address each doubt type. Empathize first ("That's fair — most people wonder about that at first"), then redirect to the specific solution from the offer's value stack.

**R — Reinforce:** After yes (or when they're on the edge): confirm they made the right call. State the specific next step with a date and time. Ask if there's one remaining question before you get started.

### Consultative Selling (Doctor, Not Pharmacist)

A pharmacist fills whatever prescription the customer asks for. A doctor asks questions, runs diagnostics, and prescribes only what's needed.

Freelancer trap: "Tell me what you need, I'll build it." Sells tasks, priced as a contractor, $1k–$5k ceiling.

Consultant approach: "Let me figure out what you actually need." Sells outcomes, priced as a strategic partner, $10k+ ceiling.

The transition happens after 2–3 documented wins. Until then, act like a consultant even if you price like a beginner.

**Consultant's opening question:** "If 500 new clients showed up tomorrow, what would break first in your business?" This is a diagnostic question, not a pitch. It maps their bottleneck before you position the offer.

### Lead With Pressure, Not Technology

Prospects are not buying the product. They are buying relief from a pressure. For B2B clients: board pressure, competitor movement, staff confusion. For solopreneur clients: fear of being left behind, spouse questions about the business, self-doubt.

Sales mistake: open with technology ("Let me show you what MCP can do"). Makes the seller feel competent, alienates the buyer.

Correct approach: open with pressure ("Are your clients or competitors starting to ask you about AI strategy?"). Emotionally committed prospects close far more easily than intellectually curious ones.

Rule: avoid technical jargon until after they have expressed wanting to move forward.

### The Discovery Call as Paid Scoping (Rung 0)

The first paid session is not just a service — it's a paid scoping call disguised as a help session. While delivering value, you are learning:
- Where their data lives
- What their team complains about
- What is actually automatable vs. what they think is automatable
- Their political constraints and real priorities

Three compounding effects: (1) it's a mini sales call — trust is built while working together, (2) it's paid scoping — you get what agencies pay to learn, (3) it creates lock-in — after 2–3 sessions you know their business better than any competitor; switching cost = re-explaining everything.

Follow-up after each session: send 2–3 things they could try on their own (10 minutes, signals over-delivery, deepens lock-in). Do not pitch the next rung on session 1 — let them ask.

---

## Step 1: Locate Files

**If $ARGUMENTS contains a folder path:**
- Read `[folder]/profile.md`, `[folder]/offer.md`, and `[folder]/outreach.md`
- Set `output_folder` to that path

**If $ARGUMENTS is empty:**
- Ask: "Provide the path to your momentum project folder (e.g., `projects/momentum/your-slug/`), or paste the offer details so I can build the sales system."

---

## Step 2: Two Reframes to Apply to Every Call

Before writing any talk track, establish these two principles. They shape every script line.

**Reframe 1 — Diagnose First (Doctor, Not Pharmacist):**
A pharmacist fills whatever prescription the customer asks for, no questions asked. A doctor asks questions, runs diagnostics, and prescribes only what is actually needed.

On a sales call: do not open by explaining the offer. Open by diagnosing the prospect's actual operational problem. Map their workflow. Understand where they are leaking time, money, or focus. The offer comes after the diagnosis, not before.

Opening question to use: "If 500 new clients showed up tomorrow, what would break first in your business?" This is a consultant's opening, not a freelancer's.

**Reframe 2 — Lead With Their Pressure, Not the Technology:**
Prospects are not buying the product (AI system, automation tool, workflow). They are buying relief from a pressure — board questions, competitors moving faster, fear of being left behind, a spouse asking where the revenue is.

In sales: ask about pressure before showing technology. "Are your clients or competitors starting to ask you about AI? Are you feeling like you need a clear answer to that question?" Emotionally committed prospects close far more easily than intellectually curious ones. Avoid technical jargon (MCP, RAG, agentic loop) until after they have expressed wanting to move forward.

---

## Step 3: CLOSER Talk Track

Build all 6 stages of the CLOSER framework, written specifically for the offer from `offer.md` and the avatar from `market.md`.

**C — Clarify why they are on the call:**
Open by understanding their situation, not by pitching. Ask what prompted them to reach out today. What is happening in their business right now that made this feel urgent? Listen for the pressure type (competitor fear, overwhelm, wasted time, missed revenue). Reflect it back.

Write 2–3 opening questions for this specific offer.

**L — Label their problem:**
Repeat their problem back to them in their own words. Not a paraphrase — their actual language, slightly elevated. "So what I'm hearing is... [their words]. Is that right?" This confirms you understand and makes them feel heard before you suggest anything.

Write a labeling script template using the avatar's pain language from `market.md`.

**O — Overview of past attempts:**
Ask what they have already tried. Why did it not work? This accomplishes two things: it shows you understand their history, and it pre-empts the "I'll just do it myself" objection by surfacing why DIY has already failed.

Write 2 questions to draw out past attempts.

**S — Sell the vacation:**
Now introduce the dream outcome from `offer.md`. Not the features. Not the process. The destination. "What I want to walk you toward is [dream outcome in their language]." Describe what their day/week/business looks like after the work is done. Make it vivid and specific to their situation.

Write the S section using the exact dream outcome from `offer.md`.

**E — Explain away their concerns:**
Address the 4 doubt types from the obstacle map in `offer.md`. Map each concern to the corresponding solution/component. Do not argue — empathize first ("That's a fair concern, and here's why most people feel that way at first..."), then redirect with the specific solution.

Write a response for each doubt type using the obstacle map.

**R — Reinforce the decision:**
After they say yes (or when they are on the edge): reinforce that they made the right call. Confirm the next step with a specific date and time. Ask if there is any remaining question before you get started. Send the onboarding message same day.

Write the R section with a clear close + next-step ask.

---

## Step 4: Pre-Call Brief Template

A one-page prep document to fill in before every call. Primes the call so the first 2 minutes are not wasted on orientation.

Fields:
- Name and business
- Where they came from (DM, referral, content, cold)
- Their exact words from the initial message or DM
- Likely primary doubt type (Financial / Likelihood / Effort / Time) — guess based on their language
- What they likely need to hear in the S section
- Goal for this call (close / qualify / book follow-up)

---

## Step 5: Post-Call Follow-Up Email

Send within 5 minutes of ending the call while the energy and memory are fresh.

Structure:
1. One sentence acknowledging what they said ("You mentioned that [their words]...")
2. One sentence confirming what was agreed ("We decided to [next step]...")
3. One sentence confirming the next step with a specific date/time ("I'll send [deliverable] by [date] and we'll connect again [date].")
4. One sentence making it easy to reply ("If anything comes up before then, just hit reply.")

Write this as a complete email template with merge fields for name and specifics.

---

## Step 6: Same-Day Onboarding Message

Send the same day as the close — while energy is high and before buyer's remorse sets in.

Structure:
1. Welcome line (warm, not corporate)
2. Confirm what they just bought (the offer name + what it includes)
3. State the first action they need to take (answer 3 questions, book the first session, send one document)
4. Give a timeline for when they will see the first result
5. Express genuine enthusiasm for their outcome

Write this as a complete message (DM or email) with merge fields.

---

## Step 7: Save Output

Save to: `projects/momentum/[slug]/sales.md`

File format:

```
# Sales System

## The Two Reframes
1. Diagnose first — open by mapping their workflow, not explaining the offer
2. Lead with their pressure — ask about fear/competitor/overwhelm before showing technology

## CLOSER Talk Track

### C — Clarify (Opening Questions)
1. [Question 1]
2. [Question 2]
3. [Question 3]

### L — Label (Script)
"So what I'm hearing is... [template using avatar pain language]. Is that right?"

### O — Overview (Past Attempts)
1. [Question to draw out what they tried]
2. [Question to surface why it failed]

### S — Sell the Vacation
"What I want to walk you toward is [dream outcome from offer.md]..."
[3–5 sentences painting the destination in their language]

### E — Explain Away Concerns
**If they say [Financial doubt]:**
"[Empathy line] + [redirect to solution from value stack]"

**If they say [Likelihood doubt]:**
"[Empathy line] + [redirect to guarantee or social proof]"

**If they say [Effort doubt]:**
"[Empathy line] + [redirect to DFY/DWY delivery method]"

**If they say [Time doubt]:**
"[Empathy line] + [redirect to fast early win]"

### R — Reinforce
"[Confirmation line] + [next step with specific date/time] + [any final question before we start?]"

## Pre-Call Brief Template
- **Name:** 
- **Business:** 
- **Source:** [ ] DM [ ] Referral [ ] Content [ ] Cold
- **Their words:** 
- **Likely doubt type:** [ ] Financial [ ] Likelihood [ ] Effort [ ] Time
- **Key S section point:**
- **Call goal:** [ ] Close [ ] Qualify [ ] Book follow-up

## Post-Call Follow-Up Email
Subject: Next steps — [their first name]

[Full email template with merge fields]

## Same-Day Onboarding Message
[Full message template with merge fields]
```

Tell the user the file was saved and the path. Highlight the single most important thing to do on every call (diagnose first). If called by `/momentum`, confirm ready to proceed to Loop Engine.

---

## Hard Rules

- Never open a call by explaining the offer. Always diagnose first.
- The S section must use the exact dream outcome language from `offer.md` — not a generic benefit.
- Every E section response must acknowledge the concern before redirecting. No arguing.
- Post-call email must be sent within 5 minutes. Note this explicitly in the output.
- Same-day onboarding message must state a specific first action for the client — not "I'll be in touch."
- If running standalone: ask for the project folder path if not provided in $ARGUMENTS.
