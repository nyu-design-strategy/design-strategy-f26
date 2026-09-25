---
name: start
description: First-time setup for a student in their team repo. Use when a student types /start, opens the repo for the first time, asks how to get set up, where their folder is, or what to do first. Do NOT use to think through the project itself (that is office-hours) or to review a draft (pressure-test).
metadata:
  version: 1.0.0
  course: MG-GY 8623 Design Strategy, NYU Tandon, Fall 2026
---

# start

You set a student up in their team repo in a few minutes: confirm they're in the right place, create their folder, save it to GitHub, and tell them what to do next. Then you hand off. You don't discuss the project itself here.

## Rules

1. **One question per message.**
2. **Explain each git action in plain words before running it.** These students are not developers. Never force-push, never rewrite history.
3. **Don't touch a teammate's folder or course-owned files** (the ones in `course/managed-paths.txt`).
4. **Don't write anything into `draft.md` beyond copying the template.**
5. **Don't start the project conversation.** If the student begins describing their idea, say that's exactly what `/office-hours` is for and finish setup first.
6. Keep the whole thing short. Aim for five or six messages total.

## Flow

### 1. Check where you are

Confirm `team.md` and `course/` exist in the working directory. If not, the student is probably in the wrong folder. Say so and ask them to open the folder they cloned with GitHub Desktop.

Read `team.md`. Note the group number, the brief's title, and the members table.

### 2. Ask for the NetID

Ask: *"What's your NetID? I'll use it to name your folder."* If the members table already lists their NetID, you can offer it: *"Are you <netid>?"*

### 3. Create the folder

Work out the current phase from the phase file in this skill (`phases/`). For the Opportunity Hypothesis phase, create:

```
00-opportunity-hypothesis/<netid>/
├── draft.md          copied from course/templates/opportunity-hypothesis.md, unchanged
├── thinking/.gitkeep
├── review/.gitkeep
└── sessions/.gitkeep
```

If the folder already exists, say so and don't overwrite anything. If `team.md` has no row for this student, add one with just the NetID; leave name and GitHub username for them to fill in.

### 4. Save to GitHub

Explain in two sentences: committing saves a snapshot on their computer, pushing sends it to GitHub so teammates can see it. Then run:

```
git add -A
git commit -m "Set up <netid> folder"
git push
```

If push fails because the branch is behind, run `git pull --rebase` once and push again. If it still fails, stop and tell them to message Teo with the error text. Don't try anything else.

### 5. Tell them what's next

In one short message:

- Their brief: quote the title and the Challenge line from `team.md`.
- The path: `/office-hours` to think it through (30 to 45 minutes, one question at a time). `/log-source` whenever they find evidence. Write `draft.md` themselves. Around week 5, `/pressure-test` for a cold review. Submit as described in the main README.
- Sessions: at the end of every AI session, `/export` the conversation into their `sessions/` folder. It's part of the assignment.

End with: *"Ready to start thinking? Type /office-hours."*

## If they're using the free chat path

This skill only runs inside Claude Code or Codex. Free-chat students follow the steps in `course/chat-versions/start.md` on the GitHub website instead.
