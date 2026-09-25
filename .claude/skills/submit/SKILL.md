---
name: submit
description: Submits a student's finished draft: makes the PDF, saves it to GitHub, freezes the submission with a tag, and gives the link to post in Slack. Use when the student says "submit", "hand in", "make the PDF", "I'm done", or asks how to turn in their draft. Do NOT use for reviewing or improving the draft (that is pressure-test).
metadata:
  version: 1.1.0
  course: MG-GY 8623 Design Strategy, NYU Tandon, Fall 2026
---

# submit

You turn `draft.md` into a PDF, put it in the student's folder, push it to GitHub, and freeze that exact version with a git tag. The student then posts one link in Slack. Nothing here needs the GitHub website.

## Rules

1. **Never change the content of `draft.md`.** Not a typo, not a heading. If something looks broken (an empty section, a missing AI use note), say so once and ask whether they want to submit anyway. Their call.
2. **Explain each git action in plain words** before running it. Never force-push, never delete or move a tag that already exists.
3. **One question per message.**
4. **Don't judge the draft.** No comments on quality.

## Flow

### 1. Find the draft

Work out the phase. The student's folder is `<phase-folder>/<folder>/`, where `<folder>` is `<netid>-<first>-<last>` (for example `ti2219-teo-ivancevic`). If it isn't clear from the working directory, ask for their NetID once and find the folder that starts with it. Read the phase file in this skill for the tag prefix and PDF name. Confirm `draft.md` exists and isn't just the untouched template.

Quick checks, reported in one message, no judgment:

- every section heading from the template is present
- the **AI use** section has something in it
- `notes.md` has at least one entry
- no `> **Gap:**` or `> **Suggestion:**` blockquotes left from `/draft` (each is something they haven't decided on)

If any of these is missing, say which and ask: *"Submit anyway, or fix that first?"*

### 2. Make the PDF

Output name: `<pdf-prefix>-<netid>.pdf`, saved in the student's folder. Try these in order and use the first that works:

1. `pandoc draft.md -o <pdf> --pdf-engine=<any available>` (try plain `pandoc draft.md -o <pdf>` first)
2. Google Chrome headless, if installed: write a clean standalone HTML file from the markdown (readable font, 2 cm margins, no external assets), then
   `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf=<pdf> <html>`
   (on Windows, `chrome.exe` with the same flags)
3. macOS `cupsfilter <html> > <pdf>` (basic but works with no install)
4. If none works: save the HTML file next to the draft, tell the student to open it in a browser, use Print → Save as PDF with the exact file name above into their folder, and then run `/submit` again. Stop here.

Open or describe the resulting PDF's first lines to confirm it isn't blank. Delete any temporary HTML file.

### 3. Save and freeze

Explain: *"I'm going to save the PDF to GitHub and mark this exact version as your submission. The mark is called a tag; nothing you change later will alter it."*

```
git add <pdf>
git commit -m "Submit <phase>: <netid>"
git push
git tag <tag-prefix>-<netid>
git push origin <tag-prefix>-<netid>
```

If `git push` fails because the branch is behind, run `git pull --rebase` once and push again. If it still fails, stop and tell them to message Teo with the error.

If the tag already exists (a resubmission), don't touch it. Use the next free suffix: `<tag-prefix>-<netid>-v2`, `-v3`, and so on. Say which one you used.

### 4. Give them the link

Build the link to the PDF at that tag:

```
https://github.com/<org>/<repo>/blob/<tag>/<phase-folder>/<folder>/<pdf-name>
```

Get `<org>/<repo>` from `git remote get-url origin`. Print the link and say:

*"Post this link in your team's Slack channel. That's your submission. If you resubmit before the deadline, run /submit again and post the new link; the latest one counts."*

Append a one-line `## YYYY-MM-DD · submit` entry to `notes.md` with the tag and link.
