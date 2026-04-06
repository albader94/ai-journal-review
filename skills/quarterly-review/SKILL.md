---
name: quarterly-review
description: >
  Close out the current quarter and set up the next one by reading the quarterly note, all three monthly reviews, and synthesizing them into an end-of-quarter review + a new quarter plan. Trigger on: any request to do a quarterly review, close out a quarter, wrap up a quarter, set up next quarter, or any mention of quarterly planning or end-of-quarter review.
---

# Quarterly Review Skill

This skill does two things in one pass: closes out the ending quarter (Goals achieved, Goals missed, Key learnings) and drafts the new quarter's plan (Theme, Goals, Projects, Habits, Monthly Breakdown, Not-To-Do List). Both are output as a single markdown file.

## Step 1: Determine Which Quarters

Figure out which quarter is ending and which is starting. If the user says "close out Q1" or "quarterly review," use the current date to infer:
- Q1 = January-March, Q2 = April-June, Q3 = July-September, Q4 = October-December

If ambiguous, ask.

## Step 2: Read the Source Material

You need four things:

1. **The ending quarter's note** (e.g., "Q1") — contains the goals, theme, projects, habits, and monthly breakdown set at the start of the quarter. You'll evaluate performance against these.
2. **The three monthly reviews** — titled by month name (e.g., "January", "February", "March"). These contain the monthly overview, wins, challenges, lessons, key moments, area reviews, and next-month focus.
3. **The new quarter's note** (e.g., "Q2") — read this to see the template structure you need to fill.

Read all notes in parallel.

If any monthly review is missing or mostly empty, note it but work with what's available.

## Step 3: Close Out the Ending Quarter

Compare what actually happened (from the three monthly reviews) against what was planned (from the quarterly note). Be honest and specific.

### Goals Achieved

For each goal that was met or substantially met, write a short paragraph that names the goal, describes what was accomplished, and connects it back to the original intent. Include specific dates, numbers, or milestones where they exist.

If a goal was partially achieved, call it out as partial — describe what was done and what fell short. Partial achievements still belong here, not in "Goals missed."

### Goals Missed

For each goal that was clearly not achieved, write a short paragraph that names the goal, explains what happened (not just "didn't do it" but why — circumstances, pivots, priorities shifted), and whether it still matters going forward.

This is not a shame section. Goals get missed because life happens. The value is in understanding what derailed things, not in self-criticism.

Also check the **Habits of Flow** table and the **Not-To-Do List** from the quarterly note. If any habits were supposed to be built or broken and weren't, note them here.

### Key Learnings

These are the quarter-level insights — bigger than any single month's lessons. Pull from the monthly "Lessons Learned" sections but synthesize upward. What did three months of living teach that no single month could?

Aim for 4-6 substantial learnings, each as a paragraph. Each should have:
- The insight itself as a clear statement
- The evidence from the quarter that supports it
- Why it matters going forward

Look for patterns that span months — a frustration that appeared in month 1 and was still there in month 3, a lesson that kept deepening, a shift that happened gradually.

### Tone

Write honestly — not corporate performance review language. Not overly positive spin. If something failed, say it failed and why. If something unexpected became the real win of the quarter, name that.

## Step 4: Draft the New Quarter Plan

Before writing, review what emerged from the ending quarter — the challenges that remain, the lessons learned, the "Next Month Focus" from the final month, and any forward-looking observations from the area reviews.

### Draft first, then ask.

Write a complete proposal for all sections based on what you've synthesized. Then present it and explicitly ask:
- Does the theme resonate?
- Are the goals right, or are there priorities not visible in the data?
- Anything to add or remove?

### Template for the New Quarter

```markdown
## Theme
What is this quarter about? **[Theme Name]**

[1-2 sentences expanding on what the theme means.]

## Goals
3-5 outcomes I want to achieve by the end of the quarter:

1. **[Goal Name]:** [Description — specific, measurable where possible.]
2. **[Goal Name]:** [Description]
3. **[Goal Name]:** [Description]

## Projects
What will I actively work on?

[1-2 paragraphs describing active projects and how they connect to the goals.]

## The Habits of Flow (to Build/Maintain/Break)

| Habit | Action | Why |
|-------|--------|-----|
| [Habit] | Build/Maintain/Break — [what this looks like in practice] | [Why this matters this quarter] |

When deciding habits:
- **Build** = new habit not yet established
- **Maintain** = working habit from last quarter to keep going
- **Break** = habit to eliminate

Check the previous quarter's habits table. If a habit was supposed to be built and was, move it to "Maintain." If it was supposed to be broken and wasn't, carry it forward. Don't quietly drop unfinished habits.

## Monthly Breakdown

### Month 1:
Focus on... **[Theme for the month]**
- [3-5 specific actions or focuses]

### Month 2:
Focus on... **[Theme for the month]**
- [3-5 specific actions or focuses]

### Month 3:
Focus on... **[Theme for the month]**
- [3-5 specific actions or focuses]

The monthly breakdown should create a logical progression — month 1 sets things up, month 2 builds momentum, month 3 compounds or consolidates.

## Not-To-Do List

- **[Anti-pattern]:** [Why this is dangerous and what it looks like when it creeps in]
```

## Step 5: Output Format

Save as a single markdown file:
`Q[N] Review & Q[N+1] Plan.md`

For example: `Q1 Review & Q2 Plan.md`

The file should have two clearly separated sections:
1. The end-of-quarter review (for the ending quarter)
2. The new quarter plan (for the upcoming quarter)

Use `---` separators between the two major sections.

## Step 6: Present and Iterate

Share the file and flag 2-3 specific things you want input on — especially around the new quarter's theme and goals. Keep the follow-up brief. After feedback, update the file accordingly.
