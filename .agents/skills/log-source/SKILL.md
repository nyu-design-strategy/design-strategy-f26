---
name: log-source
description: Records a source (article, study, report, dataset, statistic) as a shared page in the team's sources/ folder and checks whether it actually supports the student's claim. Use when the student pastes a link, citation, number, or study, or says "log this", "add this source", "is this a good source". Do NOT use for general research questions with no specific source in hand.
metadata:
  version: 1.0.0
  course: MG-GY 8623 Design Strategy, NYU Tandon, Fall 2026
---

# log-source

You turn one source into one page in `sources/` that the whole team can reuse for the rest of the semester. Each page has a compiled summary of what the source actually says on top and a timeline of who used it for what below. Plain markdown, no database.

## Rules that never bend

1. **Never invent a source, a number, or a field.** If you can't verify something (author, date, exact figure), write `unverified, check this` in that spot. Never fill a gap with a plausible guess.
2. **The number must come from the source, not from the student's memory of it.** If they differ, say so and record what the source says.
3. **One question at a time.** You will usually need only one or two.
4. **No grades.** Don't rate the source "strong" or "weak". Describe what it measured and let the student judge the fit.
5. **You write only source pages and `sources/INDEX.md`.** Never touch `draft.md` or anything else in the student's folder.
6. **Phase-aware.** Work out the phase from the student's folder or ask, then read `phases/<phase-folder>.md` in this skill and follow any notes there. If no phase file exists, say so once and continue.
7. **Session log.** At the end, remind the student to save the conversation into `sessions/`.

## Flow

### 1. Get the source

Take the URL or citation the student gave you. If you can fetch web pages, read the source itself, not a summary of it. If you can't fetch, or the page is paywalled, ask the student to paste the relevant passage, including the sentence with the number and anything about how it was measured.

### 2. Check for duplicates

Look in `sources/` for a page with the same URL or the same title. Read `sources/INDEX.md` too. If it already exists, don't create a new page: tell the student, then update the existing page (add to **Used for**, correct anything wrong). Skip to step 4.

### 3. Extract

From the source, pull out:

- **Title**
- **Author or publisher**
- **Publication date**
- **Type:** one of `primary study`, `report`, `filing`, `survey`, `dataset`, `news`, `blog`, `opinion`, `marketing`
- **The claim and the number,** paraphrased, with at most one short quote (under 25 words)
- **What was actually measured:** the population (who), the geography (where), and the year the data is from, which is often earlier than the publication year. Note the sample size and the method if given.

If the source has several relevant numbers, ask the student which one they need before extracting all of them.

### 4. Ask the student

*"Which claim of yours does this support? Say it in your own words."*

Wait for the answer. Record it verbatim.

### 5. Check the fit

Compare the student's claim to what was measured. Flag a mismatch plainly, in one or two sentences, and ask at most one question about it. Common mismatches:

- US (or one-country) data used for a global or different-market claim
- Data from 2019 or earlier presented as "now"
- A small survey (a few hundred people) used as a market size
- A vendor's own marketing or a sponsored report used as independent evidence
- A number about the whole category used for the student's specific segment
- A correlation described as a cause

If there's no mismatch, say so in one line and move on. Don't manufacture caveats.

### 6. Write the page

File: `sources/<year>-<short-slug>.md`, where `<year>` is the year of the data (or publication if that's all there is) and `<short-slug>` is 3 to 5 lowercase words joined by hyphens.

```markdown
---
title: ""
url: ""
publisher: ""
published: YYYY-MM-DD
accessed: YYYY-MM-DD
type: report
added_by: <netid>
---

# <title>

## What it says
Two to four sentences, paraphrased. What the source is and what it argues or finds.

## The number
The specific figure(s), with unit and year. One short quote at most.

## What was measured (who, where, when)
Population, geography, year of the data, sample size, method. Write `unverified, check this` for anything you couldn't confirm.

## Caveats
Limits on what this number can support. Include the fit check from step 5 if there was a mismatch.

## Used for
| Date | Who | Phase | Claim it supports |
|---|---|---|---|
| YYYY-MM-DD | <netid> | 00-opportunity-hypothesis | "<the student's claim, verbatim>" |
```

Teammates append rows to **Used for** when they reuse the source, so leave the table at the bottom.

### 7. Update the index

Add or update one row in `sources/INDEX.md`:

```markdown
| [<title>](<year>-<short-slug>.md) | <type> | <year of data> | <the key number, one phrase> | <netids who have used it> |
```

Keep the table sorted by year of data, newest first. Create `sources/INDEX.md` with the header from `sources/README.md` if it doesn't exist.

### 8. Close

In chat: name the file, restate the fit check in one line, and remind the student to save the session into `sessions/`.

## If the student asks you to find sources

You can search if you have web search. Search for evidence **for and against** the claim, and report both sides with links. Then log only the sources the student picks, one at a time, through the flow above. Never log a source you haven't read.
