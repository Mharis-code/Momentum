---
name: hunter
stage: offer
description: Use when running the first stage of the Momentum System — validates a market before building an offer. Applies Hormozi's 4-filter market test, builds a precise avatar with exact buyer language, and returns a green/amber/red verdict. Can be run standalone or called by /momentum. No external dependencies — all knowledge is embedded.
argument-hint: [path to output folder, or describe the business inline]
---

# Hunter — Validate the Market Before You Build the Offer

## What This Skill Does

Hunter is Agent 1 of the Momentum System. It stress-tests a market using Alex Hormozi's 4-filter criteria from $100M Offers, builds a precise avatar with exact buyer language, and returns a green / amber / red verdict. Saves `market.md` to the output folder.

Run this before building any offer. A weak market cannot be fixed by a great offer.

---

## Hormozi Knowledge — Market Validation Frameworks

### The 4 Market Criteria ($100M Offers)

Hormozi's rule: there are only 4 things that make a market good or bad. A great market can make a mediocre offer work. A great offer cannot save a bad market.

**Criterion 1 — Massive Pain:** The problem must be painful enough that people are actively seeking solutions, spending money, and talking about it. Pain = urgency = willingness to pay. Low-pain markets produce low conversion rates regardless of offer quality.

**Criterion 2 — Purchasing Power:** The target customer must have money to spend and a track record of spending it on solutions like this. If the market has the pain but no budget (e.g., broke college students), the math never works.

**Criterion 3 — Easy to Target:** You must be able to find these people. They must congregate — in groups, communities, forums, hashtags, associations, events. Untargetable markets require paid ads at scale to penetrate, which is not a Rung 1 strategy.

**Criterion 4 — Growing:** Is the number of people with this problem increasing or decreasing? A growing market creates natural momentum. A shrinking market requires fighting for market share.

### The Niche Sizing Problem

Hormozi's warning: "Small businesses and solopreneurs" is not a niche — it's half the economy. A yoga studio owner and a SaaS founder share nothing: different language, different fears, different results, different channels. One message cannot speak to both.

The goal: narrow enough that you can target with a single message, wide enough that 1,000+ potential clients exist.

### Avatar Precision

The avatar is not a demographic. It is a person you could pick out of a room by what they say. The key data point is **buyer language** — the exact words they use when describing their problem to a friend, not the polished marketing version.

Examples:
- Weak: "operational inefficiency" → Strong: "I spend half my morning on emails that don't move anything forward"
- Weak: "client acquisition challenges" → Strong: "I have no idea where my next client is coming from"

Buyer language is found in: community posts, Reddit threads, DMs, discovery call transcripts, Amazon book reviews in the niche.

---

## Step 1: Locate the Business Profile

**If $ARGUMENTS contains a folder path** (contains `projects/` or `output/`):
- Read `[folder]/profile.md` for intake answers
- Set `output_folder` to that path

**If $ARGUMENTS is a business description** (plain text):
- Treat it as the business description
- Ask: "Where should I save the output? Provide a folder path or I will create `projects/momentum/[auto-slug]/`."

**If $ARGUMENTS is empty:**
- Ask: "What business are we validating? Describe the offer and ideal customer in a few sentences."

---

## Step 2: Apply the 4-Filter Market Test

Score each filter: **pass** / **amber** (proceed with caution) / **fail**.
For every amber or fail: write a one-line fix suggestion.

**Filter 1 — Are they already paying for solutions?**
Evidence: existing services, software, coaches, courses, consultants in the space. No spending = no urgency.

**Filter 2 — Is the pain painful and recurring?**
Recurring = weekly problem = recurring revenue opportunity. One-off problems (planning a wedding, moving house) are weak markets.

**Filter 3 — Are they findable online?**
Name specific communities, LinkedIn groups, subreddits, Skool communities, hashtags, associations. "Yes they're on LinkedIn" is not an answer. "Yes — they're in the Restaurant Owners Network group (18k members)" is.

**Filter 4 — Is the market growing?**
Assess from industry trends, hiring data, media attention, AI tool adoption curves, search volume direction. Even "stable" is amber in a world where most markets are growing.

---

## Step 3: Niche Sizing Check

After the 4-filter test, assess the niche size:

**Too broad:** Cannot be targeted with one message. Narrow with a specific descriptor: industry + stage + specific problem. Example: "coaches" → "health coaches with 1–3 years in business struggling to fill their calendar."

**Too thin** (under ~1,000 identifiable, reachable people): Not enough volume. Suggest the adjacent niche one level up.

**Right-sized:** You can name where they gather, what keywords they search, and 3–5 accounts they follow.

---

## Step 4: Build the Avatar

Three attributes, all specific:

**Who they are (demographics):**
Role, stage, revenue range or team size, location if relevant. Specific enough that you could describe them to someone and they'd picture the same person.

**Their exact words (buyer language):**
Three phrases in quotes — the words they would use describing their problem to a friend. Not marketing language. Not what you think they should say. What they actually say.

**Where they live online:**
2–3 specific platforms, community names, or accounts. Not "LinkedIn" — "LinkedIn + the Coaches Corner Skool group + @name on Twitter."

---

## Step 5: Market Verdict

**Green:** All 4 filters pass, niche is right-sized, avatar is identifiable. Proceed to Alchemist.

**Amber:** 1–2 filters are weak but fixable. State the specific caveat and the fix required before proceeding.

**Red:** 2+ filters fail or niche is fundamentally unworkable. Do not proceed to offer building. Give a concrete alternative niche or pivot.

---

## Step 6: Save Output

Generate a slug from the business description (lowercase, hyphens). Example: `social-media-restaurants`.

Save to: `projects/momentum/[slug]/market.md`

Create the folder if it does not exist.

```
# Market Analysis
**Business:** [one-line description]
**Date:** YYYY-MM-DD

## Niche Statement
I help [specific avatar] achieve [specific outcome] via [vehicle/method].

## 4-Filter Test
| Filter | Result | Notes |
|--------|--------|-------|
| Already paying for solutions | ✅/⚠️/❌ | [evidence or fix] |
| Painful and recurring | ✅/⚠️/❌ | [evidence or fix] |
| Findable online | ✅/⚠️/❌ | [specific communities/platforms] |
| Growing market | ✅/⚠️/❌ | [trend evidence] |

## Niche Size Check
[Right-sized / Too broad — narrowed to: X / Too thin — adjacent: Y]

## Avatar
**Who they are:** [specific demographics]
**Their exact words:**
- "[phrase 1]"
- "[phrase 2]"
- "[phrase 3]"
**Where they live online:** [specific platforms, communities, accounts]

## Market Verdict
**[Green / Amber / Red]** — [2–3 sentences. If Amber: state the caveat. If Red: state the pivot.]
```

Tell the user the file was saved with the full path. If called by `/momentum`, confirm ready to proceed to Alchemist.

---

## Hard Rules

- Never validate a market on enthusiasm alone. Apply all 4 filters even when the idea feels obvious.
- Pain language must be in quotes and must sound like a real person talking to a friend — not a marketer.
- Never give a Green verdict if 2+ filters are amber or worse.
- "Small businesses" and "solopreneurs" alone are not niches. Always narrow.
- If running standalone and no folder is provided: ask before proceeding.
