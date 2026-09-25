---
name: start
description: First-time setup for a student in their team repo. Use when a student types /start, opens the repo for the first time, asks how to get set up, where their folder is, or what to do first. Do NOT use to think through the project itself (that is office-hours) or to review a draft (pressure-test).
metadata:
  version: 1.1.0
  course: MG-GY 8623 Design Strategy, NYU Tandon, Fall 2026
---

# start

You set a student up in their team repo in a few minutes: confirm they're in the right place, create their folder, prefill the parts of the draft you already know, save it to GitHub, and tell them what to do next. Then you hand off. You don't discuss the project itself here.

## Rules

1. **One question per message.** (Step 2 asks for two facts in one message; that's the only exception.)
2. **Explain each git action in plain words before running it.** These students are not developers. Never force-push, never rewrite history.
3. **Don't touch a teammate's folder or course-owned files** (the ones in `course/managed-paths.txt`).
4. **Prefill only facts you already have.** Name, NetID, group, and the brief. Never write a word of the student's own thinking into `draft.md`.
5. **Don't start the project conversation.** If the student begins describing their idea, say that's exactly what `/office-hours` is for and finish setup first.
6. Keep the whole thing short. Aim for five or six messages total.

## Flow

### 1. Check where you are

Confirm `team.md` and `course/` exist in the working directory. If not, the student is probably in the wrong folder. Say so and ask them to open the folder they cloned with GitHub Desktop.

Read `team.md`. Note the group number, and the whole Brief section: the topic line, the **Secular waves** line, and the **Challenge** line.

### 2. Ask who they are

Ask: *"What's your NetID and your name, as you'd like it on your work? (For example: ti2219, Teo Ivancevic.)"*

Then ask: *"And your GitHub username?"* If they don't know it, say it's fine to leave blank and fill in later.

Build the folder name: `<netid>-<first>-<last>`, all lowercase, spaces and punctuation replaced by hyphens, accents stripped. Example: `ti2219-teo-ivancevic`. Confirm it back in one line.

### 3. Create the folder and prefill the draft

Work out the current phase from the phase file in this skill (`phases/`). For the Opportunity Hypothesis phase, create:

```
00-opportunity-hypothesis/<folder>/
├── draft.md          from course/templates/opportunity-hypothesis.md, with the header and Category prefilled
├── thinking/.gitkeep
├── review/.gitkeep
└── sessions/.gitkeep
```

Prefill in `draft.md`, and nothing else:

- The header line: `**Name:** <name> · **NetID:** <netid> · **Team:** Group <N> · **Category:** <topic title>`
- Under **The Category**, keep the italic description from the template and add below it, verbatim from `team.md`:

  ```
  **Topic:** <topic title>

  **Secular waves:** <the line from team.md>

  **Challenge:** <the line from team.md>
  ```

Every other section stays exactly as the template has it.

If the folder already exists, say so and don't overwrite anything. Then add or complete the student's row in the `team.md` members table (name, NetID, GitHub username). If a row with their NetID exists, fill in what's missing; don't touch other rows.

### 4. Save to GitHub

Explain in two sentences: committing saves a snapshot on their computer, pushing sends it to GitHub so teammates can see it. Then run:

```
git add -A
git commit -m "Set up <folder>"
git push
```

If push fails because the branch is behind, run `git pull --rebase` once and push again. If it still fails, stop and tell them to message Teo with the error text. Don't try anything else.

### 5. Tell them what's next

In one short message:

- Their brief, both lines quoted verbatim: the **Secular waves** line and the **Challenge** line.
- The path: `/office-hours` to think it through (30 to 45 minutes, one question at a time). `/log-source` whenever they find evidence. Write `draft.md` themselves; the header and Category are already filled in. `/pressure-test` for a cold review when there's a draft. `/submit` when done.
- Sessions: at the end of every AI session, `/export` the conversation into their `sessions/` folder. It's part of the assignment.

End with: *"Ready to start thinking? Type /office-hours."*

## If they're using the free chat path

This skill only runs inside Claude Code or Codex. Free-chat students follow the steps in `course/chat-versions/start.md` on the GitHub website instead.
