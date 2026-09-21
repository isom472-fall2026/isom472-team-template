# Instructions for AI assistants working in this repository

This file is read by the AI assistant (Google Antigravity, or any tool that reads
`AGENTS.md`). Students do not need to read it. It must stay in the repository.

It says the same things as `docs/how-we-work.md`, in the form an assistant needs.

## What this repository is

A student team's capstone project for ISOM 472 at Kuwait University. Six students, six
phases, one repository. The stack is a static front end published with GitHub Pages and
Supabase for data and logins. Nothing in this course is paid for.

**The repository is the evidence.** Every change is traceable to a named student, a story,
and a review. Preserve that trace in everything you do.

## Before writing any code

1. Find the issue this work belongs to. Work without an issue does not get merged.
2. Read that issue's acceptance criteria. Build to them, not past them.
3. If the work crosses a boundary between two members, read `docs/contracts/` for that
   boundary first and build to the agreed shape.
4. If there is no issue, or the acceptance criteria are unclear, or no contract exists for
   a boundary you are about to cross — **stop and say so.** Do not guess and do not
   invent an interface.

## Scope

Do what the story asks and stop. Do not refactor neighbouring code, rename things that
already work, add dependencies, or "improve" files the story did not name. If you see a
real problem outside the story, say it in one sentence and leave it alone — it becomes its
own issue.

Prefer the smallest change that satisfies the acceptance criteria.

## Comments

- A comment says **why**, never what. The code already says what.
- Never add a comment that restates the line below it.
- Never add a docstring to an obvious function to look thorough.
- Do add a comment where a reader would reasonably ask "why is it done this way?" — a
  workaround, a client rule, a non-obvious order of operations.
- Never leave commented-out code. Delete it; the history keeps it.
- Never write comments addressed to the student ("TODO: you may want to…") in code that is
  being committed.

## User stories

When asked to write stories, produce this shape and nothing else:

```
As a <role>
I want <capability>
So that <reason>
```

followed by acceptance criteria as a checklist, each one something a teammate can check by
doing it. No criterion may contain "properly", "correctly", "well" or "user-friendly".

One story is one thing a user can do. If a story needs the word "and" twice, it is two
stories.

You may draft stories. A named student edits and owns them. Never file an issue that has
no student's name on it.

## Commits

Conventional Commits, with the story ID at the end:

```
feat(orders): add duplicate-order check  [S-14]
fix(login): reject an empty password  [S-9]
docs(contracts): add the order_line contract  [S-14]
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`.

One branch per story, named after it: `s-14-duplicate-orders`.

Commit under the student's own GitHub account. Never commit on behalf of another member,
and never change the author of a commit.

## Pull requests

Fill in `.github/pull_request_template.md` completely:

- what changes, in plain language;
- `Closes #<issue number>` — the issue number, not the story ID;
- the **AI-Assisted** line: the tool, what it produced, what the student changed. If you
  wrote code in this pull request, that line is not optional.

Never mark a pull request as reviewed. Never approve one. Review is a human act in this
course.

## Never

- Never commit `.env`, API keys, Supabase service keys, passwords or client personal data.
  This repository is public. See `.gitignore`.
- Never push to `main`. Work goes through a branch and a pull request.
- Never edit another member's contract file in `docs/contracts/` without that member in
  the pull request.
- Never put real client data in seed data. Invent it.
- Never write numbers into `docs/finops-ledger.md` that you did not observe.
- Never delete or rewrite history: no force pushes, no amended commits that are already
  pushed.
- Never add a build step, a bundler, a framework or a package the team did not ask for.

## When you are unsure

Say what you do not know and stop. A question costs a minute. A wrong assumption merged
into `main` costs the team a sprint.
