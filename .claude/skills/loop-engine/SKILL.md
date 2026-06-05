---
name: loop-engine
stage: feedback
description: Use when running the fifth stage of the Momentum System — builds the follow-up and reactivation system to keep momentum after the first sale. Produces a closed-client testimonial/referral sequence, a "no" reactivation sequence using Dean Jackson's 9-word email, a ghost bump sequence, and an objection log template. Can be run standalone or called by /momentum. No external dependencies — all knowledge is embedded.
argument-hint: [path to output folder]
---

# Loop Engine — Keep Momentum Through Follow-Up and Reactivation

## What This Skill Does

Loop Engine is Agent 5 of the Momentum System. It reads all prior outputs and builds the system that converts closed clients into testimonials and referrals, reactivates lost leads on a 90-day schedule, recovers ghosted conversations, and logs objections back into the offer for continuous improvement. Saves `follow-up.md` to the project folder.

Most revenue is lost not in the sales conversation but after it — in the silence that follows. This skill closes that gap.

---

## Hormozi Knowledge — Follow-Up and Referral Frameworks

### Others Advertise for You ($100M Leads, Section IV)

Hormozi identifies a fifth advertising category beyond the Core Four: other people advertising for you. This includes referrals from closed clients, employees, partners, and affiliates. At scale, this channel multiplies output without operator time.

The mechanics for a 1-person business: every closed client is a potential referral source. The trigger is a specific result, not just satisfaction. Ask for the referral after the first visible win — not after payment, after they see something working.

### Dean Jackson's 9-Word Email

The most effective reactivation tool for cold prospects. Format:

"[First name], are you still looking for help with [specific thing]?"

Nothing else. No context. No signature beyond the name. No explanation of who you are.

Why it works: the simplicity signals no pressure. It reads like a genuine human check-in, not a follow-up sequence. The specificity ("help with [thing]") reminds them of the exact conversation without rehashing it. Prospects who ignored 3 previous follow-ups often respond to this one.

Use at Day 14 and Day 90 of the "no" reactivation sequence. The 90-day gap makes it feel like a fresh conversation.

### Testimonial Timing

Request testimonials after the first visible result — not after payment. "After payment" captures financial satisfaction. "After first result" captures the emotional transformation, which is what sells the next person.

Ask one specific question, not "write me a testimonial." The specific question format: "When [specific thing you built/set up] started working, what was the moment you realized it was worth doing? Just 2–3 sentences is perfect." This produces usable copy in the prospect's language.

### Ghost Sequence Psychology

Prospects go cold for benign reasons: busy, life happened, the message got buried. The ghost bump sequence respects this.

Day 3: assume benign cause, check in without pressure.
Day 7: deliver value with zero ask. Makes them feel good about seeing your name.
Day 14: the clean break. This message often generates a reply when nothing else did — because it removes pressure entirely. "I'll assume timing isn't right" gives them permission to re-engage later without awkwardness.

Never re-pitch in the ghost sequence. The goal is to stay in their consciousness positively, not to close a deal they weren't ready for.

### The Objection Feedback Loop

Every objection is data. An objection is either:
- A **sales problem** (your CLOSER scripting needs work)
- An **offer problem** (a component is missing or a doubt isn't being addressed)

After 5–10 logged objections, run `/alchemist` again to update the offer. The market is telling you what the offer is missing.

---

## Step 1: Locate Files

**If $ARGUMENTS contains a folder path:**
- Read `[folder]/profile.md`, `[folder]/offer.md`, `[folder]/outreach.md`, and `[folder]/sales.md`
- Set `output_folder` to that path

**If $ARGUMENTS is empty:**
- Ask: "Provide the path to your momentum project folder (e.g., `projects/momentum/your-slug/`), or paste the offer and sales details so I can build the follow-up system."

---

## Step 2: Closed Client Sequence

For every client who signs: three moments require a message.

**Moment 1 — Testimonial Request:**
Send after the first visible result (not after payment, after they see something working). Make it easy to respond — ask one specific question, not "write me a testimonial."

Format: "Hey [Name], quick question — when [specific thing you built/set up] started working, what was the moment you realized it was worth doing? Just 2–3 sentences is perfect."

Pull the "specific thing" from the offer's dream outcome in `offer.md`. Write this template with a merge field for the result.

**Moment 2 — Referral Ask (3 variants):**

Variant 1 — Direct ask (use when the client is visibly happy, mid-session or just after):
"Do you know one or two other [avatar type] who'd benefit from the same setup? I'd be glad to give them the same [offer name] at [price]. You'd be doing them a favor."

Variant 2 — Incentive ask (use when client has completed the engagement):
"I'm opening [N] spots this month for [offer name]. If you refer someone who books, I'll [give you X — a free session, a bonus, a discount on retainer]. Know anyone?"

Variant 3 — Introduce-me script (use when client is well-connected in the niche):
"If you have someone in mind, the easiest thing is just to intro me over email — even a one-liner like 'You should talk to [Name], they helped me [specific result]' is enough. Want me to write a suggested intro message you could copy and send?"

Write all 3 variants using the offer name, avatar type, and dream outcome from `offer.md`.

---

## Step 3: "No" Reactivation Sequence

For prospects who said no, maybe, or need time — do not let them go cold permanently. Schedule 4 touchpoints at increasing intervals.

**Day 7 — Warm check-in:**
One paragraph. Reference the call. Mention one specific thing they said. Offer one small, free value-add related to their problem (a tip, a link, a resource). No ask.

"Hey [Name], been thinking about [specific thing they mentioned] since our call. [Tip/resource]. No ask — just thought it might be useful."

**Day 14 — 9-word email (Dean Jackson format):**
Send exactly: "[First name], are you still looking for help with [specific thing]?"
Nothing else. No signature beyond the name. No explanation. The power is the simplicity.

**Day 30 — Nurture:**
One paragraph. Share a short result or case study relevant to their situation. "Thought of you when [client type] got [specific result] last week." End with a soft door-open: "If timing ever shifts, door's open."

**Day 90 — 9-word email (second round):**
Send exactly: "[First name], are you still looking for help with [specific thing]?"
Same format as Day 14. Many people who ignored the first one respond to this one — the gap in time makes it feel less like follow-up and more like a fresh conversation.

Write all 4 messages using the offer name and avatar pain language from `market.md` and `offer.md`.

---

## Step 4: Ghost Bump Sequence

For warm prospects who engaged in DM conversation and then went cold — no response after a positive exchange. Three messages, spaced out.

**Day 3 — Soft check-in:**
Assume benign reason for silence (busy, missed it). Short message. "Wanted to make sure my last message got through — sometimes they get buried. Happy to chat whenever works."

No re-pitching. No guilt. One sentence.

**Day 7 — Value add:**
Send something useful related to their specific problem or niche. A short insight, a relevant post, a tool. Zero ask. Just: "Saw this and thought of [their situation] — might be worth a look."

Pull from the content hooks built in `outreach.md` for a relevant piece to share.

**Day 14 — Clean break:**
Short, honest, no pressure. "I'll assume the timing isn't right — no worries at all. Door's open whenever it makes sense. Hope [their thing] is going well."

This message often gets a reply when nothing else did — because it signals you are not going to keep chasing them.

Write all 3 messages with merge fields for name and situation.

---

## Step 5: Objection Log Template

Every objection heard on a sales call should be logged. Over time, this log tells you whether objections are a sales problem (need better CLOSER scripting) or an offer problem (need a component added or removed).

Template fields:
- **Date**
- **Prospect type** (brief description matching avatar)
- **Objection heard** (their exact words in quotes)
- **Doubt type** (Financial / Likelihood / Effort / Time)
- **How it was handled** (what you said)
- **Outcome** (closed / no / follow-up)
- **Offer fix needed?** (yes/no — if yes, what component would have addressed this)

This log feeds back into the Alchemist. Run `/alchemist` again after 5–10 logged objections to update the offer.

---

## Step 6: Save Output

Save to: `projects/momentum/[slug]/follow-up.md`

File format:

```
# Follow-Up & Reactivation System

## Closed Client Sequence

### Testimonial Request
[Full message — merge fields: Name, specific result, offer name]

### Referral Ask — 3 Variants

**Variant 1 — Direct ask:**
[Full message]

**Variant 2 — Incentive ask:**
[Full message]

**Variant 3 — Introduce-me script:**
[Full message + suggested intro copy the client can forward]

## "No" Reactivation Sequence

**Day 7:**
[Full message]

**Day 14 (9-word email):**
[First name], are you still looking for help with [specific thing]?

**Day 30:**
[Full message]

**Day 90 (9-word email):**
[First name], are you still looking for help with [specific thing]?

## Ghost Bump Sequence

**Day 3:**
[Full message — 1 sentence]

**Day 7:**
[Full message — 1 short paragraph, value only]

**Day 14:**
[Full message — clean break]

## Objection Log Template
| Date | Prospect Type | Objection (their words) | Doubt Type | Handled With | Outcome | Offer Fix? |
|------|--------------|-------------------------|------------|--------------|---------|------------|
| | | | | | | |
```

Tell the user the file was saved and the path. Remind them to copy the objection log into a running spreadsheet and review it after every 5 calls. If called by `/momentum`, confirm ready for the orchestrator to compile the 30-day plan.

---

## Hard Rules

- The 9-word email must be exactly 9 words (or very close). Do not add context, pleasantries, or a signature beyond the name. The format is the mechanism.
- The ghost bump Day 14 message must not re-pitch. It is a clean exit that often generates a reply — do not ruin it by attaching an ask.
- The testimonial request must reference a specific result, not ask for a generic review.
- Every message must be written for the specific offer and avatar — not generic follow-up copy.
- The objection log instructions must include the instruction to run `/alchemist` again after 5–10 entries.
- If running standalone: ask for the project folder path if not provided in $ARGUMENTS.
