# sources/

One page per source, shared by the whole team, for the whole semester.

**Why one page per source:** you'll cite the same reports in your Opportunity Hypothesis, the team downselect, the Research Readout, and the final pitch. Writing down what a source actually measured once, carefully, saves everyone from re-reading it and from misquoting it later.

## How to add a source

Run `log-source` (`/log-source` in Claude Code, `$log-source` in Codex, or paste `course/chat-versions/log-source.md` into a chat). It reads the source, asks which of your claims it supports, checks the fit, writes the page, and updates `INDEX.md`.

You can also write a page by hand. Copy the structure from any existing page: frontmatter, then **What it says**, **The number**, **What was measured (who, where, when)**, **Caveats**, **Used for**.

## File names

`<year-of-data>-<short-slug>.md`, for example `2024-bls-gig-work-survey.md`.

## Reusing a teammate's source

Don't make a new page. Add a row to the **Used for** table at the bottom of the existing page with the date, your NetID, the phase, and the claim you're using it for. Then add your NetID to the "Used by" column in `INDEX.md`.

## What goes in Caveats

Anything that limits what the number can support: it's from one country, it's from 2019, it's a small survey, it's the vendor's own marketing. Not a judgment on whether the source is "good", just what it can and can't carry.
