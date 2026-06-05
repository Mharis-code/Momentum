---
name: weekly-sprint
stage: meta
description: Universal execution layer for the Solopreneur OS. Three modes — (1) Standard: run every Monday to convert the 90-day plan into a Mon–Fri schedule with Rule of 100 tracking; (2) Auto: triggered by /momentum after the 90-day plan is built, generates Week 1 immediately with no questions; (3) Friday Report: run every Friday (or via scheduled cron) to generate an end-of-week report covering completions, misses, Rule of 100 score, and next-week recommendations. Applies across every stage of the business loop.
argument-hint: [projects/momentum/your-slug/ | friday-report projects/momentum/your-slug/ | leave blank to be guided]
---

# Weekly Sprint — Turn the 90-Day Plan into This Week's Work

## What This Skill Does

The 90-day plan is a strategy document. This skill makes it executable. Every Monday, you tell it which week you're on and where things stand. It reads the 90-day plan, identifies the right actions for this stage, and builds a specific Mon–Fri schedule with daily task blocks, Rule of 100 tracking, and a Friday review.

Without this, the 90-day plan sits in a folder while you improvise. With it, every week has a single focus, a daily rhythm, and a clear end-of-week checkpoint.

**What you get:**
- This week's single focus (what one thing matters most this week)
- Mon–Fri daily schedule — morning/midday/evening task blocks
- Rule of 100 tracker — daily outreach and content targets
- Objection/win log prompt — a daily 2-minute capture habit
- Friday review questions — did you hit the weekly goal? what do you carry forward?
- Carry-forward note — what moves to next week's sprint

**Saved to:** `projects/momentum/[slug]/sprints/week-[N].md`

---

## Embedded Knowledge — Hormozi Rule of 100

The Rule of 100 is the minimum daily action threshold for building a business from zero. The number 100 represents enough volume to generate momentum even when conversion rates are low.

Two applications:
- **100 outreach touches per day** — DMs, connection requests, comments, replies, emails. Any interaction that could start a conversation counts.
- **100 minutes of content creation per day** — one full content unit, or 100 minutes of writing, recording, or editing.

You do one or the other, not both, depending on the stage:
- **Weeks 1–4 (validate + build):** 100 outreach touches. Content is secondary.
- **Weeks 5+ (execute + compound):** Both. 100 touches in the morning block, 100 minutes content in the midday block.

The Rule of 100 is not about perfection. It is about showing up at a volume that the market can actually respond to. 20 DMs per day is invisible. 100 is noticeable.

**Core Four priority order for the daily rhythm:**
1. Warm outreach first (people you know, or who know you from content) — fastest conversion
2. Content creation second — builds the warm pool for next month
3. Cold outreach third — only after warm is exhausted
4. Paid ads last — not until Rung 2+

The daily schedule always follows this order. Never skip to Step 3 when Step 1 still has inventory.

---

## Step 1: Handle Arguments — Detect Mode

**Mode A — Friday Report:** If $ARGUMENTS starts with `friday-report` or `report`:
- Extract the folder path from the remaining arguments if provided
- If no path provided: scan `projects/momentum/` subdirectories for the most recently modified file in any `sprints/` folder — use that project
- Skip directly to the Friday Report section. Do not build a weekly schedule.

**Mode B — Auto (triggered by /momentum):** If $ARGUMENTS contains `auto`:
- Extract the folder path from $ARGUMENTS
- Read `[folder]/90-day-plan.md`
- Set week number to 1. Ask no questions — proceed directly to Step 2.
- Skip the status check; there is no prior week.

**Mode C — Standard (manual Monday run):** If $ARGUMENTS is a folder path (no special keywords):
- Read `[folder]/90-day-plan.md`
- Ask: "Which week of the 90-day plan are you starting? (e.g., Week 3)"
- Also ask: "Quick status check — any important updates since last week? (closed a client, got a key objection, ran out of warm contacts, etc.)"

**Mode D — Empty:** If $ARGUMENTS is empty:
- Ask: "What is the path to your Momentum project folder? (e.g., `projects/momentum/your-slug/`)"
- Then continue as Mode C.

---

## Step 2: Identify the Weekly Focus

Read the relevant section of 90-day-plan.md for the stated week. Identify:

1. **The current month phase** (Month 1: validate + build / Month 2: execute + iterate / Month 3: close + compound)
2. **The week's goal** as stated in the plan
3. **The most important action** this week — the one thing that, if done, makes the week a success
4. **Any blockers or dependencies** from the status update (e.g., "waiting for client approval" or "no discovery calls booked yet")

State these clearly before building the schedule:

```
This week (Week [N]):
Phase: Month [X] — [phase name]
Goal: [one sentence from 90-day-plan.md]
Single most important action: [the one thing]
Blockers: [any from status update, or "none reported"]
```

Confirm with the user before building the full schedule.

---

## Step 3: Build the Mon–Fri Daily Schedule

For each day, build three task blocks based on the week's focus and phase.

**Template per day:**

```
## [Day]

**Morning block (30–60 min) — Outreach:**
[Specific task: who to contact, which template to use, how many touches to hit]
Target: [N] ACA touches or warm conversations advanced

**Midday block (60–120 min) — Content / Core work:**
[Specific task: write post on [topic], record TikTok, build [deliverable], send proposal]
Target: [1 content unit published / 1 deliverable advanced]

**Evening block (15–20 min) — Review:**
[Check reply queue, advance conversations, log objections or wins]
Target: [N] replies sent, 1 log entry made
```

**Day-specific adjustments:**
- **Monday:** Include 5 minutes to review this sprint document and set intention for the week
- **Wednesday:** Mid-week check-in — are you on track for the weekly goal? What needs to shift?
- **Friday:** Lighter on prospecting, heavier on review and content (Friday CTA post per the weekly rhythm)

**Week-phase adjustments:**

**Weeks 1–4 (Month 1):**
- Morning: 20 warm ACA DMs (not 100 yet — quality over quantity in validation phase)
- Midday: Work on offer, brand setup, or content publishing
- Evening: Review replies, note what language resonates

**Weeks 5–8 (Month 2):**
- Morning: 50–100 warm outreach touches
- Midday: 1 content unit produced and published
- Evening: Reply queue, objection log

**Weeks 9–12 (Month 3):**
- Morning: 50–100 outreach touches + follow up on discovery call no-shows
- Midday: Client delivery work OR content production (alternate days)
- Evening: Reply queue, case study notes if client work is ongoing

---

## Step 4: Build the Rule of 100 Tracker

Write a simple daily tally table for the week:

```
## Rule of 100 Tracker

| Day | Outreach Touches | Content Units | Replies Sent | Log Entries |
|-----|-----------------|---------------|-------------|-------------|
| Mon | 0 / [target] | 0 / 1 | — | — |
| Tue | 0 / [target] | 0 / 1 | — | — |
| Wed | 0 / [target] | 0 / 1 | — | — |
| Thu | 0 / [target] | 0 / 1 | — | — |
| Fri | 0 / [target] | 0 / 1 | — | — |
| **Total** | **0 / [5×target]** | **0 / 5** | | |
```

Set the outreach target based on week phase:
- Weeks 1–4: 20/day (100/week total)
- Weeks 5–8: 50/day (250/week total)
- Weeks 9–12: 50–100/day depending on client load

---

## Step 5: Daily Log Habit

At the end of each day, spend 2 minutes answering two questions. This log is the feedback loop that makes the 90-day plan responsive to reality.

Include this in the sprint document:

```
## Daily Log (fill in at end of each day)

**Monday:**
- Best response or win today:
- Biggest objection or friction:
- One thing to adjust tomorrow:

**Tuesday:**
[same]

[repeat for each day]
```

Remind the user: the objection entries go into `follow-up.md` in the Loop Engine objection log. If 5+ entries accumulate, run `/alchemist` to update the offer.

---

## Step 6: Friday Review

At the end of Friday, answer these questions before closing the week.

```
## Friday Review

1. Did you hit the weekly goal? [Yes / Partially / No]
   - If partially or no: what got in the way?

2. Rule of 100 check:
   - Total outreach touches this week: [N]
   - Total content units published: [N]
   - Did you hit the weekly targets? [Yes / No]

3. What worked this week? (1–2 specific things)

4. What needs to change next week? (1 specific adjustment)

5. Carry forward to next sprint:
   - Unfinished actions:
   - Key conversations to continue:
   - One new thing to try next week:
```

---

## Friday Report (Mode A Only)

*This section runs only when called with `friday-report` or triggered by the Friday cron. Skip if building a weekly schedule.*

### FR-1: Load the Current Week

Find the current week's sprint file:
- If a folder path was provided: read the highest-numbered file in `[folder]/sprints/`
- If no path: scan `projects/momentum/*/sprints/` for the most recently modified week file

Read the sprint file in full. Extract:
- Week number and weekly goal
- Rule of 100 Tracker table (outreach and content columns)
- Daily Log entries (best response/win and biggest objection for each day)
- Friday Review section (if the user partially filled it in, incorporate their notes)

If the Daily Log is empty or mostly blank: note this in the report but do not skip. Generate the report from whatever data exists.

### FR-2: Generate the End-of-Week Report

Produce a structured report with six sections:

**1. Weekly Goal — Achieved / Partial / Missed**
State the goal set at the start of the week. Based on log entries and tracker data, assess whether it was hit. One sentence on why if partial or missed. Be direct — do not soften a miss.

**2. Rule of 100 Score**
Calculate total outreach touches logged vs weekly target. Calculate content units published vs 5.
Express as: "Outreach: 68/100 (68%) — Content: 3/5 (60%)"
If tracker was not filled in, flag it: "Rule of 100 tracker not filled — no data to score. Fill it daily next week."

**3. What Worked (2–3 specifics)**
Pull from Daily Log "Best response or win" entries. Name specific things — a DM that got a reply, a post that got engagement, a call that went well. If entries are blank, state that.

**4. What Was Missed**
Pull from Daily Log "Biggest objection or friction" entries. Name each miss plainly. If a pattern repeats across multiple days (same objection appearing Monday and Wednesday), call it out as a pattern, not just an isolated friction.

**5. Recommendations for Next Week (3 specific adjustments)**
Based on what worked and what was missed, give three concrete changes — not generic advice:
- One change to the outreach approach (different template, different platform, higher volume, etc.)
- One change to content (different topic, different format, different time of day)
- One process improvement (tracking habit, reply queue cadence, morning block timing, etc.)

**6. Week N+1 Preview**
Read the 90-day-plan.md section for next week. State:
- Next week's goal from the plan
- The single most important action
- Any phase transition (e.g., "You're entering Month 2 next week — outreach target moves from 20/day to 50/day")

### FR-3: Save the Report

Append the Friday report to the current week's sprint file under the `## Friday Review` section (replace the blank template with completed content). Do not create a new file.

Format:

```
## Friday Review — [YYYY-MM-DD]

**Weekly Goal:** [goal] — [Achieved / Partial / Missed]
[One sentence on why, if not achieved]

**Rule of 100 Score:**
- Outreach: [N] / [target] ([%]%)
- Content: [N] / 5 ([%]%)

**What Worked:**
- [specific 1]
- [specific 2]

**What Was Missed:**
- [specific 1 — reason if known]
- [pattern note if applicable]

**Next Week Adjustments:**
1. [Outreach change]
2. [Content change]
3. [Process change]

**Week [N+1] Preview:**
Goal: [from 90-day plan]
Key action: [the one thing]
[Phase transition note if applicable]
```

Tell the user the report has been saved to the sprint file path.

---

## Step 7: Save the Weekly Schedule

Save to: `projects/momentum/[slug]/sprints/week-[N].md`

Tell the user the file path. Remind them to fill in the Rule of 100 tracker daily and the Daily Log at end of day. Run `/weekly-sprint` again next Monday with the status update to build Week N+1.

---

## Hard Rules

- Every sprint must have one single focus for the week. If the weekly goal is vague ("do outreach and content"), narrow it to a specific milestone ("book 1 discovery call by Friday").
- The daily schedule must follow Core Four priority order: warm outreach morning, content midday, review evening. Never reverse this.
- If the user reports being on Week 5+ but has not yet run any discovery calls, flag this: "The 90-day plan targets 3+ discovery calls in Month 2. What's blocking the first booking? This needs to be the #1 priority this week — not content."
- If the user is behind pace (fewer than 200 total conversations started by Week 6), adjust the morning block to prioritize outreach volume over content production. Do not maintain the 50/50 split when behind on leads.
- The Friday review is not optional. It is the mechanism that makes the system self-correcting. If skipped repeatedly, the sprints accumulate without learning.
- In Friday Report mode: append to the existing sprint file — never create a new file and never overwrite the daily schedule.
- If the Daily Log was not filled in during the week: generate the report anyway, flag the missing data clearly, and include "fill the daily log" as Recommendation 3 for next week.
- In Auto mode (triggered by /momentum): never ask questions. Build Week 1 immediately and save it. The user will review it after momentum finishes.
