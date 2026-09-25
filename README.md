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

## The five moves

1. **`/office-hours`** (30 to 45 minutes). Six questions, one at a time, about who has this problem, what they do today, what changed, who benefits from the status quo, what you've seen yourself, and what would have to be true. It ends with one real-world task. Do the task.
2. **`/log-source`** every time you find a number, study, or article worth using. It writes one page into the team's shared `sources/` folder and checks whether the source actually supports your claim.
3. **Write `draft.md` yourself.** It's in your folder, already set up from the template.
4. **`/pressure-test`** when you have a draft. A cold read that finds your weakest link. Fix what matters, run it again if you want.
5. **`/submit`** when you're done. It makes the PDF, saves it to GitHub, freezes your submission, and gives you the link to post in Slack.

Use `/office-hours` as many times as you want. It remembers where you left off.

---

## Your AI sessions are part of the assignment

At the end of every session, save the conversation into your `sessions/` folder. In Claude Code, type `/export`. In Codex or other tools, use the export or share option. Free chat: paste the share link into `sessions/links.md`.

What makes a session log interesting is what *you* brought: something you knew that the AI didn't, a point where you disagreed and said why, a direction you chose that it didn't suggest.

At the end of your draft, fill in the **AI use** section. The syllabus requires it.

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
  <netid>-<first>-<last>/      draft.md, thinking/, review/, sessions/   YOURS
course/                        templates, readings, changelog        COURSE
```

Don't edit course-owned files; they're replaced on every update. Want a skill changed? Open an issue on the course repo, `nyu-design-strategy/design-strategy-f26`. Good suggestions ship to the whole class.

---

## Free chat option

Any free AI account works (Claude, ChatGPT, Gemini). You paste a skill into the chat and save the results to the repo through the GitHub website. Setup steps are in `course/chat-versions/start.md`; the skills are in the same folder.

---

## Help

Post in your team's Slack channel or message Teo. Office hours are online; message Teo on Slack to schedule.
