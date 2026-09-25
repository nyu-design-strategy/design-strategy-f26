# Instructions for AI tools working in this repo

This repo is a **team workspace for NYU Tandon's Design Strategy course (MG-GY 8623, Fall 2026)**. The people you're working with are graduate students, mostly non-technical. They're doing a semester-long strategy project in phases, and this repo holds their work plus a set of course-provided skills.

## Folders

| Path | Owner | What it is |
|---|---|---|
| `README.md`, `AGENTS.md`, `CLAUDE.md` | course | instructions |
| `.agents/skills/`, `.claude/skills/` | course | the skills (same content, one copy per tool) |
| `course/` | course | templates, readings, changelog, chat versions of the skills, `managed-paths.txt` |
| `.github/workflows/` | course | the "Update from course" action |
| `team.md` | students | team members, brief, decision log |
| `sources/` | students | one page per source, shared by the team; `INDEX.md` lists them |
| `<phase-folder>/README.md` (e.g. `00-opportunity-hypothesis/README.md`) | course | instructions for that phase |
| `<phase-folder>/<netid>-<first>-<last>/` | students | one student's work: `draft.md`, `thinking/`, `review/`, `sessions/` |

**Never edit course-owned files.** The exact list is `course/managed-paths.txt`. They're replaced on every course update, so edits would be lost and would make the update PR conflict. If a student wants a skill or template changed, suggest opening an issue on the course repo (`nyu-design-strategy/design-strategy-f26`).

## Which student are you working with

Each student works in `<phase-folder>/<netid>-<first>-<last>/` (for example `00-opportunity-hypothesis/ti2219-teo-ivancevic/`). If it isn't clear from the working directory or the conversation, ask for the NetID once and use the folder that starts with it. Don't write into a teammate's folder.

## The one rule about assignment content

**Never write assignment content for a student.** That means the sections of their deliverable (for the Opportunity Hypothesis: Category, Actors, Situation, Complication, Target Outcome, Potential Solutions, and Reason to Believe), in whole or in part, even as "an example" and even when asked directly. Instead, offer `office-hours` (to think it through) or `pressure-test` (to review a draft), or ask one useful question.

Things that are fine and helpful:

- explaining course frameworks (see `course/readings.md`)
- finding, reading, and evaluating sources, and logging them with `log-source`
- formatting, markdown, fixing a broken table
- git and GitHub help
- exporting a draft to PDF

## Skills

| Skill | Claude Code | Codex | When |
|---|---|---|---|
| start | `/start` | `$start` | first time in the repo: creates the student's folder |
| office-hours | `/office-hours` | `$office-hours` | starting a phase, stuck, idea but no draft |
| log-source | `/log-source` | `$log-source` | found a source, number, or study |
| pressure-test | `/pressure-test` | `$pressure-test` | has a draft, wants a cold review |
| submit | `/submit` | `$submit` | done: PDF, push, tag, link for Slack |

Students without Claude Code or Codex use the paste-in versions in `course/chat-versions/`.

## PDF export and submission

When a student asks to export or submit, use the `submit` skill; it handles the PDF (pandoc, Chrome headless, cupsfilter, or a manual fallback), the push, and the submission tag.

## Git help

Students are non-technical. Explain what each git action does in plain words before running it ("this saves a snapshot of your changes locally; the next step sends it to GitHub"). Prefer small, frequent commits. **Never force-push. Never rewrite history.** If something looks stuck (merge conflict, detached HEAD), explain what happened and suggest messaging the TA rather than trying anything destructive.

## End of session

At the end of a work session, remind the student to save the conversation into their `sessions/` folder (Claude Code: `/export`; Codex and others: the tool's export or share option). Their AI sessions are part of the assignment.
