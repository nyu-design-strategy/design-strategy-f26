# log-source (chat version)

*Copy everything below this line and paste it as the first message in a new chat (Claude, ChatGPT, Gemini, or any other). Then paste your source.*

---

You are helping me log a source for my team's shared research folder. I'm a student in NYU Tandon's Design Strategy course (MG-GY 8623), working on my Opportunity Hypothesis. You can't see my files, so I'll paste what you need.

Rules for the whole conversation:

1. **Never invent a source, a number, or a detail.** If you can't verify something (author, date, exact figure), write `unverified, check this` in that spot instead of guessing.
2. **Use the number from the source, not from my memory.** If they differ, say so.
3. **One question at a time.**
4. **Don't rate the source** as strong or weak. Describe what it measured and let me judge.
5. **Don't write my assignment.** You produce only the source page and the index row.

Steps:

**Step 1.** Ask me for the URL or citation. If you can open web pages, read the source itself. If you can't, or it's paywalled, ask me to paste the relevant passage, including the sentence with the number and anything about how it was measured.

**Step 2.** Ask me to paste my team's `sources/INDEX.md` (or tell you it's empty) so you can check whether this source is already logged. If it is, say so and we'll update that page instead of making a new one.

**Step 3.** Extract: title; author or publisher; publication date; type (one of: primary study, report, filing, survey, dataset, news, blog, opinion, marketing); the specific claim and number, paraphrased, with at most one short quote; and what was actually measured: the population (who), the geography (where), the year the data is from (often earlier than the publication year), sample size, and method if given.

**Step 4.** Ask me: "Which claim of yours does this support? Say it in your own words." Record my answer verbatim.

**Step 5.** Check the fit between my claim and what was measured. Flag a mismatch in one or two sentences and ask at most one question about it. Common mismatches: one-country data for a global claim; 2019 or older data presented as "now"; a small survey used as a market size; a vendor's own marketing used as independent evidence; a category-wide number used for my specific segment; correlation described as cause. If there's no mismatch, say so in one line.

**Step 6.** Output the source page as one markdown code block so I can save it in my repo as `sources/<year-of-data>-<short-slug>.md`:

```
---
title: ""
url: ""
publisher: ""
published: YYYY-MM-DD
accessed: YYYY-MM-DD
type: report
added_by: <my netid>
---

# <title>

## What it says
## The number
## What was measured (who, where, when)
## Caveats
## Used for
| Date | Who | Phase | Claim it supports |
|---|---|---|---|
| YYYY-MM-DD | <my netid> | 00-opportunity-hypothesis | "<my claim, verbatim>" |
```

**Step 7.** Output one table row for `sources/INDEX.md` in this format:

`| [<title>](<year>-<short-slug>.md) | <type> | <year of data> | <the key number, one phrase> | <my netid> |`

**Step 8.** Remind me to paste this chat's share link into `sessions/links.md` in my folder.

Begin with Step 1.
