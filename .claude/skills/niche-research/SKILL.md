---
name: niche-research
description: Use when someone asks to research a topic, find trending AI content, discover what to post about this week, gather content angles, or get ideas for social media posts.
argument-hint: [optional topic]
---

## What This Skill Does

Researches AI topics and produces a structured content brief with key angles and source links. Research only — no post drafting. Output is saved to `references/research/`.

## Context to Load

Before starting, read:
- `context/me.md` — who Haris is and his positioning
- `context/current-priorities.md` — what he's focused on right now

This shapes which topics and angles are most relevant.

## Steps

### If $ARGUMENTS is provided (topic given):

1. Skip straight to Step 4 using the provided topic as the research subject.

### If no $ARGUMENTS (no topic given):

1. Run web searches to find 5 trending AI topics right now. Cast wide — general AI trends, not just solopreneur-specific. Good search queries to use:
   - "AI trends [current month year]"
   - "AI tools solopreneurs [current year]"
   - "what's new in AI this week"
   - "AI automation business [current year]"

2. Present the 5 topics in a numbered list. For each, include:
   - Topic name
   - One-sentence description of what it is
   - One-sentence on why it's relevant right now

3. Ask: "Which of these do you want to go deep on? Or type a different topic."

4. Wait for the user to pick before continuing.

### Research Phase (runs for all paths):

4. Run targeted web searches on the chosen topic across these 4 lenses:

   **Lens 1 — Trending news**
   What's happening with this topic right now? Recent announcements, releases, debates.
   Query example: "[topic] news 2026" or "[topic] latest developments"

   **Lens 2 — Pain points**
   What are solopreneurs and small business owners struggling with related to this topic?
   Query example: "[topic] problems solopreneurs" or "[topic] challenges small business"
   Look at Reddit, forums, community posts if available.

   **Lens 3 — Creator angles**
   What are AI creators and educators already posting about this topic?
   Query example: "[topic] LinkedIn" or "[topic] explained simply"
   Note what angles exist — don't copy, just map the space.

   **Lens 4 — Educational angle**
   What's the simplest way to explain this topic to a non-technical person?
   What misconception or gap exists that Haris could address?

5. Synthesize findings into the output brief (see Output Format below).

6. Determine the topic slug: lowercase, hyphens, max 5 words. Example: "ai-agents-for-solopreneurs"

7. Save the brief to: `references/research/YYYY-MM-DD-[topic-slug].md`
   Use today's actual date in YYYY-MM-DD format.

8. Tell the user the file was saved and where. Show the brief in chat as well.

## Output Format

```markdown
# Research Brief: [Topic Name]

**Date:** YYYY-MM-DD
**Topic:** [topic name]
**Relevance:** [one sentence on why this matters right now]

---

## Topic Summary

[2-3 sentences. What is this topic? Why is it trending? Keep it simple — explain like to a 15-year-old.]

---

## Key Angles & Hooks

These are specific angles you could write a post about. Each is a potential hook or framing.

1. **[Angle name]** — [One sentence describing the angle and why it would resonate]
2. **[Angle name]** — [One sentence]
3. **[Angle name]** — [One sentence]
4. **[Angle name]** — [One sentence]
5. **[Angle name]** — [One sentence]

---

## Pain Points Uncovered

What solopreneurs or business owners are struggling with related to this topic:

- [pain point]
- [pain point]
- [pain point]

---

## Sources

- [Title or description](URL)
- [Title or description](URL)
- [Title or description](URL)

---

## Notes

[Anything else worth flagging — gaps in the research, angles that seem oversaturated, or a specific hook that stood out.]
```

## Notes

- Always cite sources. Never include an angle that isn't grounded in something found during research.
- If web search returns thin results on a topic, say so and suggest a related topic that has more material.
- Keep all language in the output simple. No jargon without a plain-English explanation alongside it.
- Do NOT draft a LinkedIn post. Research only. If the user asks for a post, note that a LinkedIn Post Creator skill is on the backlog.
- If the user picks a topic outside of AI entirely, still run the skill but note in the output that it falls outside the core niche.
