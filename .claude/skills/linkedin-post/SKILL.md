---
name: linkedin-post
description: Use when someone asks to write a LinkedIn post, draft a post about a topic, create LinkedIn content, or turn a research brief into a post.
argument-hint: [topic or path to research brief]
---

## What This Skill Does

Writes 2 LinkedIn post drafts per run. Each draft uses a different hook, angle, and structure — maximum contrast so you can pick the direction that resonates. Output is saved to `projects/content-creation-system/drafts/`.

## Context to Load

Before writing, read:
- `.claude/rules/communication-style.md` — tone, format rules, hard restrictions
- `context/me.md` — who Haris is, his positioning and audience

## Step 1: Detect Input Type

Look at $ARGUMENTS:

**If $ARGUMENTS is a file path** (ends in `.md` or contains `references/research/`):
- Read that file
- Extract: topic, key angles, pain points, any standout hooks from the brief
- Use this as the raw material for both drafts

**If $ARGUMENTS is a raw topic or idea** (plain text, not a file path):
- Use it directly as the subject
- Do not read any file

**If $ARGUMENTS is empty:**
- Ask: "What topic or idea do you want to write about? Or paste a path to a research brief."
- Wait for the answer before continuing.

## Step 2: Choose 2 Contrasting Directions

For each draft, independently pick:

**Hook style** — choose one per draft, and they must differ:
- Contrarian statement ("Most people are wrong about X")
- Bold claim ("X is the single most underrated tool for solopreneurs")
- Direct insight ("Here's what nobody tells you about X")
- Pattern interrupt ("I used to spend 4 hours on X. Now it takes 20 minutes.")
- Question ("What if you could X without hiring anyone?")
- Observation ("Something is changing in how solopreneurs work")

**Structure** — choose one per draft, and they must differ:
- **Short paragraphs** — 4-6 punchy paragraphs, each 1-3 sentences. Builds momentum line by line.
- **Numbered list** — "5 ways X changes everything for solopreneurs" or similar. Scannable, high shareability.
- **Story → insight** — Opens with a specific moment or observation, builds to a single takeaway.

**Angle** — must differ between drafts:
- Educational ("Here's how X works, explained simply")
- Personal/credibility ("What I learned building X")
- Audience pain ("The real reason solopreneurs struggle with X")
- Future vision ("What X means for the next 12 months")
- Contrarian ("Why everyone's approach to X is backwards")

State the chosen hook style, structure, and angle at the top of each draft so the choice is transparent.

## Step 3: Write Both Drafts

Apply these rules to every draft, no exceptions:

**Format:**
- 150-300 words per draft
- Short sentences. One idea per sentence.
- White space between paragraphs — never a wall of text
- Strong opening line that earns the next line

**Hard rules:**
- Never start with the word "I"
- No hashtags
- No links inside the post body
- No emojis
- No em dashes
- No corporate jargon
- No over-explaining — if it's obvious, cut it

**CTA:**
- Every post ends with an engagement question
- Question must be specific and easy to answer — not "what do you think?" but something like "What's one task you'd hand off to an AI agent first?"

**Tone** (from communication-style.md):
- Authoritative but humble
- Explain like to a 15-year-old — no jargon without a plain-English explanation immediately after
- Thought leadership, not lecture

## Step 4: Output Format

Present both drafts in this format in the chat:

---

### Draft A — [Hook Style] / [Structure] / [Angle]

[Post text]

---

### Draft B — [Hook Style] / [Structure] / [Angle]

[Post text]

---

**Which direction resonates more?** (You can also mix — take the hook from A and the structure from B.)

---

## Step 5: Save to File

Determine topic slug: lowercase, hyphens, max 5 words.

Save to: `projects/content-creation-system/drafts/YYYY-MM-DD-[topic-slug].md`

Use today's actual date. Create the `drafts/` folder if it doesn't exist.

File format:

```markdown
# LinkedIn Drafts: [Topic]

**Date:** YYYY-MM-DD
**Source:** [raw topic / or path to research brief used]

---

## Draft A — [Hook Style] / [Structure] / [Angle]

[Post text]

---

## Draft B — [Hook Style] / [Structure] / [Angle]

[Post text]

---

## Notes

[Anything worth flagging — which draft felt stronger and why, angles not explored, follow-up post ideas]
```

Tell the user the file was saved and the path.

## Notes

- If the research brief has a standout angle that's clearly the strongest, lean one draft into it. The other draft should explore a different angle entirely.
- If the topic is very broad, narrow it. A post about "AI for solopreneurs" is weak. A post about "how solopreneurs use AI to replace their morning admin routine" is strong. Narrow before writing.
- Never pad to hit 150 words. If the idea is tight and done at 130 words, it's done.
- Do not write a post that requires the reader to know Haris exists. Posts should stand alone as valuable content.
