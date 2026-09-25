# Design Strategy · Fall 2026 · Team Workspace

**MG-GY 8623 · NYU Tandon · Prof. Sean Rhodes & Prof. Sam Dix · TA: Teo Ivancevic**

This is your team's repo for the semester project: your brief, your work, and an AI set up to work on it with you.

---

## How it works

Open this folder in Claude Code or Codex and talk to the AI the way you'd talk to it anywhere else. Brainstorm, argue, ask it to explain something, ask it to write. Two things make it different from a normal chat:

- **It remembers.** Every conversation and every skill writes a dated entry into your `notes.md`, and the AI reads that file, your team's brief, and your team's sources at the start of each conversation. You never re-explain your project.
- **It has two rules.** It never invents a fact or a source, and it never grades you. Anything it adds to your draft that didn't come from you or from a logged source is marked as a suggestion, so you always know what's yours.

On top of that, five skills run the parts of the work that benefit from structure. Type them like commands (`/office-hours` in Claude Code, `$office-hours` in Codex).

---

## Set up (10 minutes, once)

1. **Accept the GitHub invite** from your email. No account yet? Make a free one at github.com and send your username to your team's repo lead.
2. **Install [GitHub Desktop](https://desktop.github.com)**, sign in, and clone this repo (File → Clone repository → pick it from the list).
3. **Open that folder in Claude Code or Codex** and type `/start`. It makes your folder and tells you what's next.

Claude Code needs a paid Claude plan; Codex a paid ChatGPT plan. We strongly recommend one, because the AI works much better when it can see your files. If you'd rather not pay, see **Free chat option** at the bottom. You won't be graded differently. Anything starting with a dot (`.claude`, `.agents`, `.github`) is plumbing; ignore it.

---

## The loop

```
/office-hours  →  /research  →  /draft  →  /pressure-test  →  /submit
      ↑                                          │
      └──────────── back to the gaps ────────────┘
```

1. **`/office-hours`** (30 to 45 min). Six questions, one at a time, about who has this problem, what they do today, what changed, who benefits from the status quo, what you've seen yourself, and what would have to be true. Ends with one real-world task. Do the task.
2. **`/research`** when you want evidence. Give it a claim; it searches for and against it, reads what it finds, and logs the sources for the whole team.
3. **`/draft`** writes `draft.md` from your notes and sources, in your words. Where you haven't worked something out, it marks a gap instead of making something up.
4. **`/pressure-test`** gives the draft a cold read and finds the weakest link. Go back to office-hours or research for what it finds, then `/draft` again.
5. **`/submit`** when you're done. PDF, saved to GitHub, frozen, link to post in your team's Slack channel. Resubmit before the deadline the same way; the latest link counts.

Run any of them as often as you like. Between them, just talk.

---

## How you use AI is part of the assignment

The course wants to see what *you* brought: something you knew that the AI didn't, a point where you disagreed and said why, a direction you chose that it didn't suggest. Your `notes.md` shows that, because every entry records what the AI contributed and what you did. The **AI use** section at the end of your draft summarizes it; `/draft` writes a first honest version and you edit it.

---

## Where things are

```
team.md                        your brief, members, decisions        YOURS
sources/                       one page per source, shared           YOURS
00-opportunity-hypothesis/
  <netid>-<first>-<last>/      draft.md, notes.md, sessions/         YOURS
course/                        templates, readings, changelog        COURSE
```

Don't edit course-owned files; they're replaced on every update. Updates arrive as a pull request called **Update from course**; your team's repo lead merges it. Want a skill changed? Open an issue on `nyu-design-strategy/design-strategy-f26`. Good suggestions ship to the whole class.

---

## Free chat option

Any free AI account works (Claude, ChatGPT, Gemini). You paste a skill into the chat and save the results to the repo through the GitHub website. Steps are in `course/chat-versions/start.md`; the skills are in the same folder.

---

## Help

Post in your team's Slack channel or message Teo. Office hours are online; message Teo on Slack to schedule.
