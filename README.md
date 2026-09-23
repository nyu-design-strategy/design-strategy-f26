# Design Strategy · Fall 2026 · Project Workspace

**MG-GY 8623 · NYU Tandon · Prof. Sean Rhodes & Prof. Sam Dix · TA: Teo Ivancevic**

This repo is two things at once:

1. **Your team's workspace for the semester project**, from your individual Opportunity Hypothesis to the final pitch in week 15.
2. **A set of AI thinking-partner skills built for this course.** They work in Claude Code and Codex, and we'll keep adding to them during the semester.

Your team repo receives updates from the course (new skills, new phase folders, templates) without ever touching your own work.

---

## The one idea behind this

**The skills won't write your assignment for you.** They ask you questions, push back on vague answers, check your evidence, and tell you where your argument is weakest. The thinking and the writing stay yours.

This follows the course AI policy: use AI a lot, and with intention. Default AI output conforms to the norm, and generic output reads as generic, whoever or whatever wrote it. These skills point the AI at the hard part of strategy work (figuring out what's actually true and what's actually interesting) instead of the easy part (producing text that sounds right).

---

## Get set up (about 10 minutes)

### 1. Accept your invites

You'll get an email invite to the **nyu-design-strategy** GitHub organization and to your team's repo. If you don't have a GitHub account yet, create a free one at github.com and send your username to Teo.

### 2. Choose how you'll work

| | **Recommended: Claude Code or Codex** | **Free option: any AI chat** |
|---|---|---|
| What you need | A paid Claude plan (Claude Code) or a paid ChatGPT plan (Codex) | Any free account: Claude, ChatGPT, Gemini |
| How it works | The AI works inside your repo. It reads your files, runs the skills, and saves notes where they belong. | You paste a skill into a chat and save the results to the repo yourself through the GitHub website. |
| Setup | Install **GitHub Desktop**, clone your team repo, then open that folder in Claude Code or Codex. | Nothing to install. |

We strongly encourage the paid option, since the skills work much better when the AI can see your files. The free option is fully supported, though, and you won't be graded differently for using it.

### 3. Run your first skill

| Tool | Type this |
|---|---|
| Claude Code | `/office-hours` |
| Codex | `$office-hours` |
| Free chat | Open `course/chat-versions/office-hours.md`, copy all of it, and paste it into a new chat |

---

## What's in the repo

Some files belong to the course, and some belong to you.

```
├── README.md                      COURSE  this file
├── AGENTS.md                      COURSE  instructions every AI tool reads
├── CLAUDE.md                      COURSE  points Claude Code to AGENTS.md
├── .agents/skills/                COURSE  the skills (Codex)
├── .claude/skills/                COURSE  the same skills (Claude Code)
├── course/                        COURSE  templates, readings, changelog, chat versions
├── .github/workflows/             COURSE  the "Update from course" button
│
├── team.md                        YOURS   who's on the team, your brief, key decisions
├── sources/                       YOURS   one page per source, shared by the whole team
├── 00-opportunity-hypothesis/
│   ├── README.md                  COURSE  instructions for this phase
│   └── <your-netid>/              YOURS
│       ├── draft.md               your hypothesis
│       ├── thinking/              notes from /office-hours
│       ├── review/                notes from /pressure-test
│       └── sessions/              your AI conversations
└── 01-differentiation-deep-dive/  appears when that phase starts
```

**The rule: don't edit course-owned files.** They get replaced every time you update. If you want a skill to work differently, open an issue on the course repo. We mean it: the skills get better from your feedback, and good suggestions will be shipped to the whole class.

---

## The skills

| Skill | Use it when | What you walk away with |
|---|---|---|
| **office-hours** | You haven't written anything yet, or you're stuck. | A conversation, one question at a time, about who has this problem, what they do today, what changed, who benefits from the problem staying unsolved, what you've seen with your own eyes, and what would have to be true. You end up with notes in `thinking/`, a list of premises you agreed or disagreed with, and one concrete real-world task to do next. |
| **log-source** | Every time you find a number, study, or article worth using. | One page in `sources/` recording what the source actually says, the specific figure, its date, and which of your claims it supports. Your whole team shares these, and you'll reuse them in later phases. |
| **pressure-test** | You have a draft. *(Arrives through a course update during week 5.)* | A cold read from an AI that hasn't seen your earlier conversations. It covers the strongest version of your idea, your weakest link, whether your sections actually connect, which claims have no evidence, and how different your solutions really are from each other. Notes are saved to `review/`. **It never edits your draft.** |

The same skills carry through the whole semester. They check which phase folder you're working in and adjust what they ask.

---

## Opportunity Hypothesis: a suggested workflow

The Opportunity Hypothesis is **individual**. Each team member works in their own folder, `00-opportunity-hypothesis/<your-netid>/`.

1. **Start with `office-hours`** (30 to 45 minutes). Do the task it gives you at the end. One real conversation with someone who lives with the problem beats three more articles.
2. **Log sources as you go** with `log-source`. Don't wait until the end to go looking for evidence for claims you've already written.
3. **Write `draft.md` yourself**, starting from `course/templates/opportunity-hypothesis.md`.
4. **Run `pressure-test`**, fix what matters, and run it again if you want a second look.
5. **Make sure your AI sessions are saved** in `sessions/` (see the next section).
6. **Submit** (see Submitting, below).

After everyone submits, your team reads each other's folders and downselects to two hypotheses together.

---

## Your AI sessions are part of the assignment

The course asks you to show how you used AI. In this repo, that means your `sessions/` folder.

- **Claude Code:** at the end of a session, type `/export` and save the file into `sessions/`.
- **Codex or other tools:** use your tool's export or share option, or copy the conversation into a file in `sessions/`.
- **Free chat:** use the chat's share-link feature and paste the link into `sessions/links.md`.

What makes a session log interesting isn't how many times the AI pushed you. It's what *you* brought: something you knew that the AI didn't, a point where you disagreed with it and said why, or a direction you chose that it didn't suggest.

At the end of your draft, add a short **AI use** note: which tools you used, how they helped, and where they fell short. The syllabus requires this disclosure.

---

## Submitting

1. **Make a PDF.** Ask your AI to "export my draft.md to PDF," or open the file in any editor and save it as a PDF. Name it `opportunity-hypothesis-<your-netid>.pdf`, save it in your folder, and commit and push.
2. **Create a release.** On your team repo's GitHub page, go to **Releases → Draft a new release**. Click **Choose a tag**, type `oh-<your-netid>`, and select **Create new tag**. Set the title to *Opportunity Hypothesis – Your Name*, drag your PDF into the attachments box, and click **Publish release**.
3. **Post in Slack.** Under **Assets** on your release, right-click your PDF, copy the link, and post it in the assignment's Slack channel before the deadline.

A release freezes that exact version of the repo, including your `sessions/` folder. Changes you push later won't alter your submission. To resubmit before the deadline, create a new release named `oh-<your-netid>-v2` and post the new link. Your latest submission before the deadline is the one that counts.

---

## Getting updates from the course

When we announce an update in Slack (or you see something new in `course/CHANGELOG.md`), **one person per team** does this:

1. Go to your team repo's **Actions** tab, click **Update from course**, then **Run workflow**, then **Run workflow** again.
2. Within about a minute, a pull request called **Update from course** appears under **Pull requests**. Open it and click **Merge**.

The update also runs automatically every Monday morning, so if you see that pull request waiting, merge it. It only touches course-owned files. If it ever reports a conflict, someone edited a course-owned file; message Teo and we'll sort it out.

---

## FAQ

**Do I have to use Claude Code or Codex?** No. They're strongly encouraged, but the free chat option is fully supported.

**Will using AI lower my grade?** No. Whether you used AI doesn't matter. How interesting and original your thinking is does.

**Can my teammates see my draft?** Yes, because it's a shared team repo. You write your hypothesis individually, and reading each other's work ahead of the team downselect is expected. Copying each other's work is not.

**Can I make the repo public for my portfolio?** Keep it private during the semester. From week 7 on, your field research will include notes about real people. Ask us at the end of the semester.

**The skill wrote a section for me anyway.** Tell it to stop and ask you questions instead. If it keeps happening, open an issue on the course repo so we can fix the skill.

**Something is broken.** Post in the course Slack or message Teo.

---

## For course staff

- Skills are edited in `.agents/skills/<skill>/` and mirrored to `.claude/skills/`. Phase-specific instructions live in `<skill>/phases/<phase-folder>.md`.
- `course/managed-paths.txt` lists every path the course owns. **Never list a folder students write in.** For phase folders, list only their `README.md`.
- Test every change on the sandbox team repo before announcing it, and add an entry to `course/CHANGELOG.md`.
- Anything that isn't ready for students, and all grading material, lives in the private staff repo, never here.

---

*Questions: teo.ivancevic@nyu.edu · Office hours by appointment, 2 MetroTech Center, Room 828*
