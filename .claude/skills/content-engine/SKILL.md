---
name: content-engine
stage: attention
description: Use when someone needs to produce multi-platform content from a single idea. Takes a topic, brief, or path to niche-research or Momentum outreach.md — outputs a LinkedIn post, TikTok/Reels script, Instagram caption, Skool post, a repurposing map, and a 30-day content calendar. Reads brand-voice.md if available to match tone and pillars. Standalone or called after /brand-voice.
argument-hint: [topic or brief | path to outreach.md | path to niche-research brief | path to Momentum project folder (adds Content Engine tab to 90-day-plan.html)]
---

# Content Engine — Multi-Platform Content from One Idea

## What This Skill Does

Content Engine takes one idea and produces ready-to-publish content for every active platform in one pass. No rewriting, no reformatting by hand. It reads the brand voice if it exists, or asks for tone preferences if it doesn't. One input → four platform formats + a repurposing map + a 30-day content calendar.

Designed for solopreneurs who need to post consistently but have limited time. The system prioritizes quality over quantity: one strong, well-structured idea repurposed correctly beats five average posts.

**What you get:**
- LinkedIn post — 150–300 words, copywriting-first
- TikTok/Reels script — 60–90 seconds, spoken hook + retain + reward + CTA
- Instagram caption — 3 variants (short punchy, medium explanatory, story-format)
- Skool post — peer-sharing format, unbranded, problem-led, 150–200 words
- Repurposing map — one sentence showing how all 4 came from the same idea
- 30-day content calendar — grid of topics by week and platform, seeded from content pillars

**Saved to:** `projects/content-creation-system/drafts/[slug]/`

---

## Embedded Knowledge — Hormozi Content Unit Framework

Every piece of content has three jobs:

1. **Hook** — Stop the scroll. The first line must interrupt the pattern. Use a bold claim, a counterintuitive statement, a specific number, or a problem the reader immediately recognizes as their own. The hook earns the read. Without it, the rest doesn't matter.

2. **Retain** — Keep the reader reading. Once the hook works, deliver on it using one of three retention mechanics:
   - **Lists** — promise a number, deliver it. "3 reasons X" tells the brain what to expect and how long the commitment is.
   - **Steps** — promise a process. "Here's how to do X in 3 steps" implies a destination. The reader wants to see if the destination matches what they expected.
   - **Stories** — promise experience. A real story with stakes, obstacles, and an outcome makes the brain predict what happens next. The prediction keeps attention.

3. **Reward** — The payoff. The insight, the tool, the framework, the reframe. Something the reader would copy into a note, save, or share. The reward is what earns the next piece of content.

**Give / Ask ratio:** For every piece of content that includes an offer or CTA (the "Ask"), there should be at minimum 3.5 pieces that give without asking. Audiences disengage when they feel sold to before they've been helped.

**Length rule:** The content should be as long as it needs to be to deliver the reward — no longer. A 5-word hook that works beats a 50-word one. A 3-point list beats a 10-point list with 7 weak points.

---

## Embedded Knowledge — Platform Format Principles

### LinkedIn
- Opening line is everything. It shows in the feed before "See more." Make it the hook.
- Short paragraphs — 1–2 sentences each, line break between every paragraph.
- No bullet points in the first line.
- End with a question or a clear CTA (follow, comment, DM, link in comments).
- Optimal length: 150–300 words for authority posts; up to 600 for case studies and stories.
- No em dashes. No corporate jargon. Write like a person, not a press release.

### TikTok / Reels Script
- Spoken format. Write for how it sounds, not how it reads.
- Hook is the first 2–3 seconds (on screen or spoken). Must create immediate curiosity or recognition.
- Retain = deliver on the hook in 45–75 seconds. Steps or story format work best for education.
- Reward = the single takeaway. State it clearly. "So the next time you [X], remember [Y]."
- CTA = 1 action. Not "like, comment, share, and follow." One. "Follow for more of this."
- Pacing: short sentences. Pause beats. Write in lines, not paragraphs.
- Length: 60–90 seconds when read aloud at natural speaking pace.

### Instagram Caption
- Three variants because Instagram audience intent varies:
  - **Short (under 100 words):** Punchy hook + 1 insight + CTA. Works for quote-style posts and carousels with self-explanatory visuals.
  - **Medium (100–200 words):** Hook + retain (list or steps) + CTA. Works when the visual needs context.
  - **Story format (150–250 words):** Opening hook + mini story + lesson + CTA. Works for behind-the-scenes or case study posts.
- Always end with a question that's easy to answer (1–3 word answers encouraged engagement).
- No hashtag blocks inside the caption — clean first; suggest 3–5 relevant hashtags separately.

### Skool Post
- Peer-sharing tone. You're a community member sharing a resource — not a creator promoting content.
- No self-promotion, no personal references, no links to personal sites.
- Lead with the problem the content solves.
- Keep it under 200 words. Tighter is better.
- End with a low-friction question ("Which part was new to you?" or "Which step do you skip?")

---

## Step 1: Handle Arguments

**If $ARGUMENTS is a topic or brief (plain text):**
- Use the topic as the content seed
- Check if `references/brand/brand-voice.md` exists — if yes, read it and apply the tone/voice guide and content pillars
- Proceed to Step 2

**If $ARGUMENTS is a path to `outreach.md` (Momentum output):**
- Read the file, extract the 3 Hook→Retain→Reward content hooks
- Use each hook as a content seed — generate one full content unit per hook
- Proceed to Step 2 with all 3 seeds

**If $ARGUMENTS is a path to a niche-research brief:**
- Read the file, extract the top 2–3 angles identified
- Use each angle as a content seed
- Proceed to Step 2

**If $ARGUMENTS is empty:**
- Ask: "What topic do you want to create content about? Give me a rough idea or a sentence — I'll handle the rest."

---

## Step 2: Read Brand Voice (If Available)

Check if `references/brand/brand-voice.md` exists.

**If it exists:**
- Read the Positioning One-Liner, Content Pillars, and Tone/Voice Guide sections
- Confirm the topic aligns with one of the content pillars
- Apply the tone/voice rules to all output
- Note which pillar this piece belongs to (used in the content calendar)

**If it does not exist:**
- Proceed without it
- At the end of output, add: "Tip: Run /brand-voice to build your signature story, content pillars, and tone guide. Content Engine produces better-matched output when this exists."

---

## Step 3: Apply the Hook→Retain→Reward Structure

Before writing anything, plan the three elements:

**Hook:** What is the one-line pattern interrupt? (counterintuitive claim, specific number, recognized pain, bold opinion)

**Retain:** What mechanic keeps attention? (list, steps, or story)
- If list: how many items? (3–5 max; odd numbers work better)
- If steps: how many steps? (3 max for short-form; up to 5 for long LinkedIn)
- If story: what's the stakes, obstacle, and outcome?

**Reward:** What is the single takeaway the reader saves? (framework, tool, mental model, reframe)

State these three elements before writing the posts. This is the skeleton. The posts are the flesh.

---

## Step 4: Write the LinkedIn Post

Using the H→R→R skeleton, write the LinkedIn post.

Rules:
- First line = the hook. No warmup, no "I wanted to share..." — start with the hook.
- One sentence per paragraph. Two at most.
- Line break between every paragraph.
- Bold key terms or numbers if they add scannability.
- End with a question or one clear CTA.
- 150–300 words. Never exceed 400.
- No emojis. No em dashes. No bullet points in the opening section.

---

## Step 5: Write the TikTok/Reels Script

Write the spoken script. Format it as lines, not paragraphs — each line = one breath.

Structure:
```
[HOOK — 2-3 seconds spoken]
[state the bold claim or question that opens the video]

[RETAIN — 45–75 seconds]
[deliver the list / steps / story in spoken lines]
[pause beats shown as blank lines between sections]

[REWARD — 10-15 seconds]
[state the single takeaway clearly]

[CTA — 5 seconds]
[one action only]
```

Include direction notes in brackets for pacing: [pause], [hold up 3 fingers], [cut to screen recording].

Total reading time: 60–90 seconds at natural speaking pace. Verify by counting words: 130–180 words = 60–90 seconds.

---

## Step 6: Write the Instagram Captions (3 Variants)

Write all 3 variants. Label them clearly.

**Variant 1 — Short (under 100 words):**
Hook + 1 key insight + CTA. Works with a quote graphic or strong visual.

**Variant 2 — Medium (100–200 words):**
Hook + list or steps retain + reward + CTA + question.

**Variant 3 — Story format (150–250 words):**
Hook + mini story + lesson + CTA + question.

End each with a question. Suggest 3–5 hashtags below the caption (not inline).

---

## Step 7: Write the Skool Post

Peer-sharing format. Problem-led. No personal references.

Structure:
1. One-line context (what this content covers and who it is for)
2. Two-line description of the main insight
3. 3–5 bullet points with the most useful or surprising points
4. CTA question ("Which point surprised you?" or "Which step do you skip?")
5. Under 200 words total

---

## Step 8: Write the Repurposing Map

One short paragraph (3–5 sentences) showing how all 4 pieces came from the same idea. Name the core insight once. Explain how each format serves a different audience behavior (LinkedIn = reading, TikTok = watching, Instagram = scrolling, Skool = community discussion).

This is for the creator's reference — so they understand the logic and can replicate it next time.

---

## Step 9: Add to 30-Day Content Calendar

Check if a content calendar exists at `projects/content-creation-system/drafts/content-calendar.md`.

**If it exists:**
- Add this piece to the next available slot
- Assign it to the appropriate platform in the posting rotation

**If it does not exist:**
- Generate a new 30-day calendar using the content pillars from brand-voice.md (if available) or the topic areas discussed
- Structure: 5 columns (Mon–Fri), 4 weeks, each cell = topic + format + pillar
- Posting rhythm: LinkedIn daily (Mon–Fri), TikTok 3×/week, Instagram 3×/week, Skool 2×/week
- Leave specific post copy cells blank — they get filled when Content Engine is run for each topic

---

## Step 10: Save Output

Save all content to: `projects/content-creation-system/drafts/[topic-slug]/`

Files:
- `linkedin.md` — LinkedIn post
- `tiktok-script.md` — TikTok/Reels script with direction notes
- `instagram.md` — all 3 caption variants + hashtag suggestions
- `skool.md` — Skool community post
- `repurposing-map.md` — the one-paragraph repurposing explanation
- `content-calendar.md` — updated or newly created calendar (at parent folder level: `projects/content-creation-system/drafts/content-calendar.md`)

Tell the user the slug folder path and list the files saved. If this is the first time running Content Engine, remind them to run `/brand-voice` first to improve future output.

---

## Step 11: Generate HTML Output

**Detect Momentum context:**
- If `$ARGUMENTS` contained a path to a Momentum project folder (a folder containing `90-day-plan.html`), set `IS_MOMENTUM=true` and `MOMENTUM_FOLDER=[that path]`
- If IS_MOMENTUM=true, also save the full content output to `[MOMENTUM_FOLDER]/content-engine-[topic-slug].md`

**Generate the HTML:**

Determine the brand primary color: if IS_MOMENTUM=true, read the `--primary` CSS variable from `[MOMENTUM_FOLDER]/90-day-plan.html`; otherwise use `#1B6CA8`.

Sections to include:
- **LinkedIn Post** — formatted as a post preview card (slightly off-white background, serif-feel font)
- **TikTok/Reels Script** — script cards, direction notes `[in brackets]` styled in a muted color, each spoken line on its own row
- **Instagram Captions** — 3 labeled variant cards (Short / Medium / Story), hashtag suggestions below each
- **Skool Post** — peer-sharing card with a "Skool" label badge
- **Repurposing Map** — styled paragraph block explaining how all pieces connect
- **30-Day Content Calendar** — full HTML table with platform columns and weekly rows

**If standalone mode (IS_MOMENTUM=false):**
Call the frontend-design skill to generate the full HTML:
```
Skill(skill="frontend-design", args="Generate a production-grade, visually distinctive content engine output document in HTML. Design direction: choose a modern editorial or creative agency aesthetic. Brand color: PRIMARY=[resolved color hex]. Required sections: LinkedIn Post (post preview card, slightly off-white background, serif-feel font), TikTok/Reels Script (script cards with direction notes in muted color, each spoken line on its own row), Instagram Captions (3 labeled variant cards — Short, Medium, Story — hashtag suggestions below each), Skool Post (peer-sharing card with a Skool label badge), Repurposing Map (styled paragraph block), 30-Day Content Calendar (full HTML table with platform columns and weekly rows). Typography: Google Fonts @import — one distinctive heading font, no Inter, Roboto, or system fonts. CSS animations: subtle fade-in on sections, hover states on cards. Self-contained: no external CSS or JS — Google Fonts @import is the only allowed external dependency. Insert <!-- SECTION-NAME --> HTML comments as injection points for each section. Return the complete HTML shell with all CSS and structure — no bracketed placeholder text.")
```
After frontend-design returns the shell, fill in every `<!-- SECTION-NAME -->` injection point with the real content output.
Save as `projects/content-creation-system/drafts/[topic-slug]/content-[topic-slug].html`. Tell the user the path.

**If Momentum tab mode (IS_MOMENTUM=true):**
Generate the tab content as an HTML fragment (not a full `<!DOCTYPE html>` document). Use the CSS variables already defined in the parent `90-day-plan.html`: `--primary`, `--accent`, `--text`, `--text-muted`, `--bg`, `--border`, `--primary-light`. Scope any additional styles inside a `<style>` block with selectors prefixed by `#tab-content-engine` to avoid bleeding into other tabs. Do not redeclare the base font, colors, or layout variables — they are inherited from the parent. Render all 6 sections listed above.

Then update 90-day-plan.html:
1. Read `[MOMENTUM_FOLDER]/90-day-plan.html`
2. Find `<!-- TAB-BUTTONS-END -->` and insert before it:
   `<button class="tab-btn" data-tab="content-engine">Content Engine</button>`
3. Find `<!-- TAB-CONTENT-END -->` and insert before it the fragment wrapped in:
   `<div class="tab-content" id="tab-content-engine">[rendered HTML fragment]</div>`
4. If `data-tab="content-engine"` already exists (re-run), replace the existing content block.
5. Save the modified `90-day-plan.html`.
6. Tell the user: "Content Engine tab added to 90-day-plan.html."

---

## Hard Rules

- The LinkedIn post must open with the hook. No warmup lines ("I've been thinking about...", "Something important happened today...").
- The TikTok script must be 60–90 seconds when read aloud. Count the words. 130–180 words = on target. Flag and trim if over.
- The Skool post must contain no personal references, no links to personal profiles, and no mention of the creator's name or brand. It is a peer sharing a resource.
- The give/ask ratio rule: do not add a hard CTA (book a call, buy, sign up) to more than 1 in every 4 content pieces produced. Track against the calendar.
- Never produce content that hasn't been run through the H→R→R structure in Step 3. Generic content happens when the skeleton is skipped.
- If the topic does not align with any of the confirmed content pillars from brand-voice.md, flag it and ask: "This topic doesn't fall under your current content pillars. Should I add it as a new pillar, or adjust the angle so it fits an existing one?"
