---
name: monthly-review
description: >
  Generate a personal monthly review by reading all daily notes for a given month and synthesizing them into a structured reflection document. Trigger on: any request to do a monthly review, monthly reflection, month-end review, summarize a month, recap a month, "how did my month go", "review my month", "fill out the monthly template", or any mention of reviewing daily journal entries for a whole month.
---

# Monthly Review Skill

This skill reads daily journal notes for a specific month and synthesizes them into an honest, personal monthly review. The notes follow a consistent journaling format with morning gratitude, intentions, affirmations, and evening wins, lessons, and reflections.

## Step 1: Determine the Month

Figure out which month and year to review. If the user says "last month" or "review my month," use the current date to calculate which month they mean. If ambiguous, ask. You need both the month name and the year.

## Step 2: Read All Daily Notes

Notes are titled in the format `DD Month` (e.g., "01 March", "02 March", ..., "31 March"). The day is always zero-padded.

Read all notes for the month in parallel batches of 10-11 to keep things fast. Not every day will have a note — some months have 28, 29, 30, or 31 days. If a note doesn't exist, skip it silently.

Many notes will have empty evening sections (the morning was filled but the evening wasn't). That's normal — extract what's there and don't flag the gaps.

## Step 3: Synthesize Into the Review

This is the core of the skill. Read through every note carefully and produce the review. The goal is a document that feels like the user wrote it themselves — honest, specific, grounded. Not a corporate summary. Not a generic motivational recap. A real reflection that names real dates, real people, real moments, and real feelings.

### How to Synthesize Well

The daily notes contain raw, unfiltered journal entries. Your job is to find the signal across 28-31 days of living and distill it into something the user can look back on months or years later and immediately remember what that month was about.

**Be specific, not generic.** "Stayed active" is weak. "Yoga became a consistent habit, played basketball with friends, body feels more flexible but losing muscle mass" is what this review needs. Pull exact dates, names, project names, and details from the notes.

**Capture the emotional arc.** A month has a shape — it starts somewhere and ends somewhere different. Track how the mood, energy, and mindset shifted across the weeks. The reflections and lessons sections of the daily notes are where this lives.

**Don't sanitize.** If the notes contain frustration, guilt, tension, or difficult dynamics, the review should reflect that honestly. These are private reflections, not public posts. The challenges and growth are inseparable.

**Connect the dots.** The user won't always explicitly state a theme. If you see the same frustration appearing on the 5th, 10th, and 31st, that's a pattern worth naming. If a lesson from week 1 connects to a win in week 3, draw that line.

## Step 4: Output Format

Save as a markdown file:
`[Month] [Year] Monthly Review.md`

For example: `March 2026 Monthly Review.md`

### Template

Use this exact structure. Every section must be filled. Write in prose with bullet points — each bullet should be a full thought (1-2 sentences minimum), not a fragment.

```markdown
# [Year] [Month] Overview

**One sentence on how this month felt:**
[A single sentence that captures the overall emotional texture of the month. Not a summary of events — a feeling.]

---

## Wins
**What am I proud of this month?**

- [Win with specific detail and date where relevant]
- [Another win — name projects, people, milestones]
- [Continue for all meaningful wins across the month]

---

## Challenges
**What was difficult?**

- [Challenge with honest detail — what happened, how it felt, why it was hard]
- [Continue for all real challenges]

---

## Lessons Learned
**What did this month teach me?**

- [Lesson distilled into a clear statement, with the experience that taught it]
- [Continue — pull from the daily "Lessons" sections but synthesize, don't just list]

---

## Key Moments
**Memorable experiences, conversations, or insights:**

- **[Month Day]:** [What happened and why it mattered — 1-2 sentences]
- **[Month Day]:** [Continue chronologically through the month]
- [Include 10-15 moments the user would want to remember]

---

## Review by Area

**Health:**
[One paragraph. Cover: exercise/movement patterns, diet, sleep, energy levels, body changes.]

**Relationships:**
[One paragraph. Cover: family dynamics, friendships, social connection, any tensions or meaningful moments.]

**Work/Projects:**
[One paragraph. Cover: what was built, shipped, or progressed. Name every project.]

**Finances:**
[One paragraph. Cover: spending patterns, investments, financial decisions.]

**Personal Growth:**
[One paragraph. Cover: spiritual practice, self-awareness gains, mindset shifts, new knowledge, habits formed or broken.]

---

## Next Month Focus
**What do I want to prioritize?**

1. **[Priority]** — [Why this matters and what it looks like in practice]
2. **[Priority]** — [Why this matters and what it looks like in practice]
3. **[Priority]** — [Why this matters and what it looks like in practice]
```

### Guidance on Each Section

**Overview sentence:** This sets the tone. It should feel like a single exhale — honest, not performative. Not "A productive month with ups and downs."

**Wins:** Be generous. Include both big milestones and smaller ones that mattered. Aim for 10-15 items.

**Challenges:** Don't soften these. If something was hard, say why. This section is for looking back and saying "yeah, that was real."

**Lessons Learned:** Synthesize across the daily "Lessons" entries but don't just copy-paste. Find the deeper thread. Aim for 7-10 distilled lessons.

**Key Moments:** Chronological. Date-stamped with bold dates. Include significant dreams if the notes contain vivid ones with personal meaning.

**Review by Area:** Each area gets one dense paragraph. No bullet points inside these — write in flowing prose. Be specific and honest. End each area with a forward-looking observation.

**Next Month Focus:** Exactly 3 priorities. These should emerge naturally from the challenges, lessons, and area reviews.

## Step 5: Present and Iterate

After saving the file, keep the follow-up brief. Ask if anything needs adjusting — there may be context that isn't captured in the daily notes.
