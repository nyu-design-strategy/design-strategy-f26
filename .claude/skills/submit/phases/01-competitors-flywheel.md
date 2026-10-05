# submit · Phase 01: Competitors and Flywheel

This phase has an individual deliverable and a team deliverable. Ask which one once: *"Submitting your own competitors and flywheel, or the team's downselect?"*

## Individual

- Draft: `01-competitors-flywheel/<netid>-<first>-<last>/draft.md`
- PDF: `competitors-flywheel-<netid>.pdf` (pdf-prefix = `competitors-flywheel`), in the student's folder
- Tag: `cf-<netid>` (tag-prefix = `cf`); resubmissions `cf-<netid>-v2`, `-v3`, ...
- Extra check, before the PDF: the draft embeds an image (`flywheel.png` or `.jpg`) that exists in the folder. If the draft has only a Mermaid block, or the image file is missing: push the current state first so it's on GitHub, then tell the student to open `draft.md` on github.com, screenshot the rendered diagram (or draw it in any tool), save it as `flywheel.png` in their folder, and run `/submit` again. Stop there.
- When making the PDF, write any temporary HTML into the student's folder so the relative image path resolves, and confirm the image appears in the PDF.
- Stage: the student's folder (including the image) and `sources/`.
- Notes entry: the student's `notes.md` in this phase folder.

## Team

- File: `team/01-downselect.md`
- PDF: `team/01-downselect.pdf`
- Tag: `cf-team`; resubmissions `cf-team-v2`, `-v3`, ...
- Who runs it: any member of the team. Say in chat that this is the team's submission and one link per team is enough.
- Checks, reported in one message, no judgment: the header's **Present** line is filled; both carried-forward hypotheses have a description and a reason; **Who we need to talk to** and **How we'll recruit them** each have at least one row per hypothesis, with an owner and a date; **AI use** has something in it.
- Stage: `team/`, `team.md`, and `sources/`.
- Notes entry: `team/notes.md`.
- Link: `https://github.com/<org>/<repo>/blob/cf-team/team/01-downselect.pdf`
