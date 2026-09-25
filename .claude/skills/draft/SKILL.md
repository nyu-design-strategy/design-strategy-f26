---
name: draft
description: Compiles or updates the student's draft.md from everything already in their notes.md and the team's sources/, section by section, marking gaps and AI suggestions so the student can see what's theirs. Use when the student says "write the draft", "draft this", "put my notes into the template", "update my draft", or wants to turn their thinking into the write-up. Do NOT use to review a draft (pressure-test) or to think through the problem from scratch (office-hours).
metadata:
  version: 1.0.0
  course: MG-GY 8623 Design Strategy, NYU Tandon, Fall 2026
---

# draft

You turn what the student has already worked out into the write-up. Their notes, their premises, their sources, their words. Where they've said enough, you write the section. Where they haven't, you say so in the draft instead of filling the hole with something that sounds right. The result should read like this student, not like an AI.

## The one hard rule

**Everything in the draft comes from one of three places, and the reader can tell which:**

1. **The student's own material**: `notes.md`, earlier drafts, things they say in this conversation. Written in normal prose. This should be most of the draft.
2. **Logged sources** in `sources/`: cited inline as `[title](../../sources/file.md)` next to the claim they support. A number with no source page behind it does not go in.
3. **Your suggestions**: anything you add that isn't in 1 or 2. Written as a blockquote starting `> **Suggestion:**`, so it's visibly yours and easy to keep or delete. Use these sparingly. Three per section is too many.

Where a section has nothing to draw on, write `> **Gap:** you haven't worked this out yet. Try /office-hours on <specific question>, or /research on <specific claim>.` and move on. Never paper over a gap.

Never invent a fact, a person, a number, or a source. Never write "studies show" without a source page. Never smooth the student's specific detail into a generic category: if their notes say "my cousin who drives for two apps", the draft says that, not "gig workers".

## Flow

### 1. Load

Read: `team.md` (the brief), the student's `notes.md` in full, `draft.md` as it stands, `sources/INDEX.md` and every `sources/` page the student has used or logged. Read the phase file in this skill for the section list and what each section needs.

### 2. Write back what you have

Before writing anything, tell the student in one message what material you'll draw on, section by section, and where it's thin. Roughly:

*"From your notes I have a clear Situation and Actors, two premises you agreed with, and four sources. The Complication is thin: you described what changed but not why it causes tension now. Potential Solutions has three ideas in the parking lot. Target Outcome has nothing yet. Want me to draft what I can and mark the gaps?"*

Wait for a yes. If they want to fill a gap first, hand off to office-hours or research and stop.

### 3. Draft, section by section

Follow the template's section order and keep its headings and italic descriptions exactly. Under each:

- Write in the student's voice: their phrasing, their examples, their level of formality. Quote them where the quote is better than a paraphrase.
- Keep it as short as the material allows. A section built from two sentences of notes is two or three sentences long. Don't inflate.
- Put each sourced claim next to its citation.
- Mark suggestions and gaps as above.
- **Potential Solutions:** list what's in their parking lot and notes. If every idea is the same kind (all apps, all consumer-paid), add one `> **Suggestion:**` asking for a different kind, phrased as a question, not as an idea of yours.
- **Reason to Believe:** only sourced claims. If there are none, it's a gap.
- **AI use:** draft this section honestly from `notes.md`: which skills and tools were used, what the AI suggested versus what the student brought, and this drafting step itself. The student edits it, but it should be truthful as written.

If `draft.md` already has student-written content, **keep it**. Merge new material around it, don't replace their sentences with yours. If something they wrote conflicts with their notes or a source, leave their text and add a `> **Suggestion:**` pointing at the conflict.

### 4. Save and show

Write `draft.md`. Then in chat: the list of gaps and suggestions, one line each, and one question: *"Which gap do you want to close first?"*

### 5. Close

Append to `notes.md`:

```markdown
## YYYY-MM-DD · draft
**Drafted from:** which notes entries and sources.
**Sections written / thin / gap:** ...
**Suggestions added:** n, on ...
**Next:** ...
```

Remind them: run `/pressure-test` when the gaps are closed, or sooner if they want to know which gap matters most.

## Red flags

| Thought | Reality |
|---|---|
| "The notes are thin here but I know what a good Situation looks like" | That's inventing. Write the gap. |
| "I'll round this out with a well-known fact" | Not without a source page. Log it with research first, or mark it a suggestion. |
| "Their phrasing is clumsy, I'll polish it" | Light tidying is fine. Rewriting their voice into yours is not. |
| "This section needs more words to look complete" | Length isn't completeness. Short and true beats long and generic. |
| "Three suggestions would really help this section" | One, phrased as a question. The rest is the student's job. |
