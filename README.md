# Design Strategy · Fall 2026 · Team Workspace

**MG-GY 8623 · NYU Tandon · Prof. Sean Rhodes & Prof. Sam Dix · TA: Teo Ivancevic**

This is your team's repo for the semester project. It holds your brief, your work, and a set of AI thinking-partner skills built for this course. The skills ask you questions, push back on vague answers, and check your evidence. **They don't write your assignment.** The thinking and the writing stay yours.

---

## Set up (10 minutes, once)

1. **Accept the GitHub invite** you got by email. No GitHub account yet? Make a free one at github.com and send your username to your team's repo lead.
2. **Install [GitHub Desktop](https://desktop.github.com)**, sign in, and clone this repo (File → Clone repository → pick it from the list). Remember where you saved the folder.
3. **Open that folder in Claude Code or Codex** and type:

   | Tool | Type this |
   |---|---|
   | Claude Code | `/start` |
   | Codex | `$start` |

   It creates your folder, saves it to GitHub, and tells you what to do next.

Claude Code needs a paid Claude plan; Codex needs a paid ChatGPT plan. We strongly recommend one of them, because the skills work much better when the AI can see your files. If you'd rather not pay, see **Free chat option** at the bottom. You won't be graded differently.

Anything in this repo starting with a dot (`.claude`, `.agents`, `.github`) is plumbing for the tools. You can ignore it.

---

## The six moves

1. **`/office-hours`** (30 to 45 minutes). Six questions, one at a time, about who has this problem, what they do today, what changed, who benefits from the status quo, what you've seen yourself, and what would have to be true. Ends with one real-world task. Do the task.
2. **`/research`** when you want evidence. Give it a claim; it searches for and against it, reads what it finds, and logs the sources into the team's shared `sources/` folder for you.
3. **`/draft`** turns your notes and sources into `draft.md`, in your words. Where you haven't worked something out yet, it says so instead of making something up. Anything it adds on its own is marked as a suggestion.
4. **`/pressure-test`** gives the draft a cold read and finds the weakest link. Fix what matters, run it again.
5. **`/submit`** when you're done. PDF, saved to GitHub, frozen, link for Slack.

And in between, **just talk to it.** Ask it anything, argue with it, think out loud. It reads your notes at the start of every conversation, so you never re-explain your project.

**You don't keep notes; it does.** Every skill and every conversation writes a dated entry into your `notes.md`. That file is your record of how you used AI, which the course asks for. `/export` of a full transcript into `sessions/` is optional.

---

## How you use AI is part of the assignment

The course wants to see what *you* brought: something you knew that the AI didn't, a point where you disagreed and said why, a direction you chose that it didn't suggest. Your `notes.md` shows that, because every entry records what the AI contributed and what you did. The **AI use** section at the end of your draft summarizes it; `/draft` writes a first honest version and you edit it.

The AI in this repo has two rules it won't break: it never invents a fact or a source, and it never grades you. Everything else is fair game.

---

## Submitting

Type `/submit` (Codex: `$submit`). It makes the PDF from your draft, saves it to GitHub, marks that exact version as your submission, and prints a link. **Post the link in your team's Slack channel.** That's it.

The mark is permanent, so changes you push later won't alter what you submitted, and your `sessions/` folder is frozen with it. To resubmit before the deadline, run `/submit` again and post the new link. The latest one before the deadline counts.

Free chat: the steps are in `course/chat-versions/submit.md`.

---

## Course updates

New skills and templates arrive as a pull request called **Update from course**. It only ever touches course-owned files, never your work. **Your team's repo lead merges it** when it appears (every Monday, or when Teo announces one in Slack). If it ever reports a conflict, message Teo.

---

## Where things are

```
team.md                        your brief, members, decisions        YOURS
sources/                       one page per source, shared           YOURS
00-opportunity-hypothesis/
  <netid>-<first>-<last>/      draft.md, notes.md, sessions/            YOURS
course/                        templates, readings, changelog        COURSE
```

Don't edit course-owned files; they're replaced on every update. Want a skill changed? Open an issue on the course repo, `nyu-design-strategy/design-strategy-f26`. Good suggestions ship to the whole class.

---

## Free chat option

Any free AI account works (Claude, ChatGPT, Gemini). You paste a skill into the chat and save the results to the repo through the GitHub website. Setup steps are in `course/chat-versions/start.md`; the skills are in the same folder.

---

## Help

Post in your team's Slack channel or message Teo. Office hours are online; message Teo on Slack to schedule.
