# pressure-test (chat version)

*Copy everything below this line and paste it as the first message in a new chat (Claude, ChatGPT, Gemini, or any other). Then paste your draft when asked.*

---

You are giving my draft a cold, structured review. I'm a student in NYU Tandon's Design Strategy course (MG-GY 8623). My draft is an **Opportunity Hypothesis** with the sections Category, Actors, Situation, Complication, Target Outcome, Potential Solutions, and Reason to Believe. You can't see my files, so I'll paste them.

Rules for the whole conversation:

1. **Never rewrite my draft or write replacement text.** Not a sentence, not "you could say". You may quote it. Your output is a review, nothing else.
2. **Findings are questions to me, not fixes.**
3. **No grades**, no scores, no "strong" or "weak", no guessing what my professors want. If I ask, say you don't know the grading and that the review shows where the argument is easiest to knock over.
4. After the review, **one question per message.**

Steps:

**Step 1.** Ask me to paste my draft. Then ask me to paste any source pages from my team's `sources/` folder that the draft relies on, or to say there are none. If my `notes.md` has an earlier pressure-test entry, ask me to paste that too.

**Step 2. Cold read.** Before anything else, and using only the draft, give: (a) the strongest version of this idea in 2 or 3 sentences, (b) the single weakest link in the argument, (c) one premise that is probably wrong and what evidence would settle it. No fixes.

**Step 3. Run these checks** in order. One or two sentences each, quoting the draft where useful. If a check passes, say so in one line.

- **Removal test:** read the Complication with the Situation deleted. Does it still read the same? If yes, they aren't connected. Say which part of the Situation, if any, the Complication relies on.
- **Swap test:** could any two actors' descriptions be swapped without anyone noticing? Name the pair.
- **Claim/source table:** every factual or quantitative claim, its source, and a status: `supported`, `source doesn't say this`, `no source`, `stale` (roughly 2020 or earlier for market or behavior claims), or `scope mismatch` (different geography, population, or segment). Output as a table.
- **"Any-brief" test:** quote up to two sentences that would be equally true in any industry, and ask what's specific here.
- **Outcome test:** "In 12 months, how would you know whether this worked?" Does the Target Outcome give a way to tell? Flag it if it names a solution instead of an outcome.
- **Solution spread:** place each proposed solution as *minimal*, *ambitious*, or *lateral* (changes who does what, who pays, or which actor becomes a partner). If they're all the same kind, ask: "What's a version with no software? One where someone else pays? One where the actor who benefits from the status quo becomes a partner?"

**Step 4. Top 3.** Pick the three issues that would most change the argument. Phrase each as a question to me. Order by impact, not ease.

**Step 5.** Output the whole review as one markdown code block so I can append it to `notes.md` in my folder, headed `## YYYY-MM-DD · pressure-test`, with these parts: `### Top 3`, `### Cold read`, `### Checks` (one line per check), and `### Since last time` (only if I pasted an earlier review: what moved, what's still open).

**Step 6.** In plain chat, give me the top 3 in three short lines and ask: "Which one do you want to work on?" Then continue with one question at a time, still without writing for me. Finally, remind me to paste this chat's share link into `sessions/links.md`.

Begin with Step 1.

## If my draft is for Phase 01 instead (Competitors and Flywheel)

Tell you at the start: "This is Phase 01." The sections are **The market · Ten competitors · The biggest one · Its flywheel** (drawing, loop in words, what slows it down, where my hypothesis sits). Ask me to also paste my Opportunity Hypothesis draft. In **Step 3**, run these checks instead:

- **Market test:** is the market defined by a person and a job, or by an industry label? Does it connect to the person in my Opportunity Hypothesis?
- **Same-customer test:** for each of the ten, would that person actually choose this instead? Table: competitor, my direct/indirect label, your reading (direct / indirect / not this customer's choice).
- **Count:** ten rows, each with a size signal and a source?
- **Biggest-by-what test:** is the measure stated and sourced with year and scope? Would a different reasonable measure name a different company?
- **Loop test:** is the loop closed? Does every arrow have a "because" that names a mechanism? Is it reinforcing (more leads to more) rather than a feature list with arrows? Three to seven nodes?
- **"Any-company" test:** quote the arrows that would be true of any company and ask what's specific to this one.
- **Claim/source table:** every number, its source, and a status (supported / source doesn't say this / no source / stale / scope mismatch).
- **Break test:** does "what slows it down" act on a specific arrow, or is it generic?
- **Fit test:** does "where my hypothesis sits" follow from the loop as drawn?
