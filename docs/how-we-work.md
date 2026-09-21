# How we work

Read this once. Come back to it when you are stuck.

Everything your team is graded on is in this repository. Work that is not here did not
happen. That is not a threat — it is how six people can see what the other five did.

## Five words

You will read these words all semester. They mean one thing each.

| Word | What it means |
|---|---|
| **repository** | This folder, plus its whole history. People say "repo". |
| **branch** | A line of work that does not disturb anyone else's. |
| **commit** | A saved point, with your name and a message. |
| **review** | A teammate reads your work and says what they checked. |
| **merge** | Your work becomes part of the real thing. |

Two more you will meet:

| Word | What it means |
|---|---|
| **issue** | One item of work on GitHub. A story or a bug. |
| **pull request** | Your branch, offered for review before it merges. People say "PR". |

## The loop

Every piece of work goes around this loop. Every time. It takes a few minutes once you
have done it twice.

1. **Pick a story** from the board. Assign the issue to yourself, so nobody picks it twice.
2. **Read its acceptance criteria.** If you cannot tell when it is finished, it is not
   ready to build. Ask the Client Lead before you write anything.
3. **Make a branch** named after the story: `s-14-duplicate-orders`.
4. **Build it.** Use your AI assistant as much as you like. You still own what it writes.
5. **Commit as you go**, with the story ID in the message:
   `feat(orders): add duplicate-order check  [S-14]`
6. **Open a pull request.** The template appears by itself. Fill in all of it, including
   the AI-Assisted line.
7. **Ask a teammate to review it.** Nobody merges their own work. The reviewer writes what
   they checked — not "looks good".
8. **Merge it.** The issue closes by itself if you wrote `Closes #12` in the pull request.

If the loop feels slow in week 5, it will feel fast in week 10. Teams that skip it spend
week 10 finding out who broke what.

## Writing a story

A story is one thing a user can do. Not a task list, not a feature area.

```
As a shop supervisor
I want to see orders that look like duplicates
So that I do not ship the same box twice
```

Then the acceptance criteria — how anyone can tell it is done:

- [ ] Orders with the same customer and the same day are flagged.
- [ ] The flag is visible on the order list without opening the order.
- [ ] A flagged order can still be shipped, with one extra click.

**A criterion a teammate cannot check is not a criterion.** "Works well" is not one.
"Loads in under two seconds" is.

Stories live in the **Issues** tab. Use the *User story* template. At the end of each
sprint the Client Lead saves a copy of the open ones into `backlog.md`, so the list has a
history.

## Agreeing a boundary

When two people build two halves of the same thing, they agree the shape of what passes
between them **before either starts**. Write it down in `docs/contracts/`, one file per
boundary. The other person reviews the pull request — their review is the agreement.

This takes ten minutes and saves a day. It is also the single best prompt you can give an
AI assistant: it knows exactly what to produce.

## Phases

Six phases. Each ends on a Wednesday, with a tag. **The tag is what gets graded** — work
pushed after it does not count for that phase.

### Phase 1 — the proposal
Due Wed 23 Sep. Write `docs/proposal.md` in its eight sections, publish `docs/index.html`
as a GitHub Pages page, and fill in the team table on the front page. Cut the tag
`phase-1`.

### Phase 2 — the design sprint
Due Wed 7 Oct. Personas, stories with acceptance criteria, the schema in Supabase, the
split of work with a contract for every boundary, and your token plan. First entry in the
ledger. Tag `phase-2`.

### Phases 3, 4 and 5 — the sprints
Due Wed 21 Oct, Wed 4 Nov, Wed 18 Nov. Each one delivers something that works, off the
backlog, merged through reviews, with the board matching the repository, the ledger
current, and a tag.

### Phase 6 — the final sprint and the demo
Sprint due Wed 9 Dec, demos Mon 14 and Wed 16 Dec. Scope is frozen. You ship what you
have and you demonstrate it. The questions at the demo are asked of you individually.

Every phase: the Phase Lead writes `docs/delivery-notes/phase-N.md` **during** the phase,
and cuts the tag.

## Using AI in this course

You are expected to use it. There is no version of this course where you do not.

Three rules:

1. **Declare it.** Every pull request carries an AI-Assisted line: the tool, what it
   produced, what you changed. `AI-Assisted: none` is equally fine. Not declaring is the
   offence.
2. **You own it.** If it is in your pull request, it is yours. At the demo you will be
   asked how your own system works, and "the AI wrote that part" is not an answer.
3. **Read before you merge.** An agent can write more code in a minute than you can read
   in an hour. Merge what you have read.

Ready-made prompts are in [prompts.md](prompts.md).

## When you are stuck

**GitHub refused my push to `main`.**
That is the rule working. Nothing goes to `main` without a pull request and a review. Make
a branch, push that, and open a pull request.

**The AI wrote code and it does not run.**
Do not paste the error back five times. Read the first line of the error — it usually
names the file and the line. Tell the assistant what you expected, what happened, and
that first line.

**I cannot find my branch.**
You are probably on a different one. In Antigravity, check the branch name shown at the
bottom of the window before you start typing.

**I committed a `.env` file, or a key.**
Say so immediately, in the team channel and to your instructor. Deleting it in the next
commit does **not** remove it from the history. A published key must be replaced, not
hidden. Nobody is in trouble for reporting it fast.

**Two of us edited the same file and it will not merge.**
This is a merge conflict. It is normal. Ask your instructor in the lab — it takes two
minutes with someone next to you, and half an hour alone.

**The board does not match what we actually did.**
Fix the board, not the story you tell about it. A board that lies is worth less than no
board, and the two are compared at every phase.

**Nobody reviewed my pull request and the phase ends tomorrow.**
Say so in the team channel now, and name the person. Waiting silently is a choice that
costs the whole team.
