# TODO: the system's name

**Client:** TODO: who the client is — the organisation and the person you deal with.

TODO: what the system does, in two lines. Plain language, no jargon. Someone who has
never met your client should understand what it is for after reading these two lines.

- **Proposal:** TODO: link to the published proposal page (`https://<owner>.github.io/<repo>/docs/`)
- **Running system:** TODO: link to the deployed system once it exists

## The team

| Role | Name |
|---|---|
| Client Lead — owns the backlog | TODO |
| Design Lead — prototype and screen list | TODO |
| Data Lead — schema and seed data in Supabase | TODO |
| Build Lead — the deployed system and release notes | TODO |
| FinOps Lead — the ledger | TODO |
| Quality Lead — bug issues | TODO |

At five members one person holds a combined Quality and FinOps Lead; at six it splits.
The **Phase Lead** rotates — one per phase. That phase's Lead writes the delivery note and
cuts the tag.

| Phase | Phase Lead |
|---|---|
| 1 | TODO |
| 2 | TODO |
| 3 | TODO |
| 4 | TODO |
| 5 | TODO |
| 6 | TODO |

## What is in this repository

| Path | What it holds |
|---|---|
| `README.md` | This page — the front page of your team, kept current. |
| `.gitignore` | What must never reach this public repository. |
| `.github/pull_request_template.md` | The block that appears in every pull request you open. |
| `docs/proposal.md` | The judged proposal, in eight sections. |
| `docs/index.html` | The published proposal page, served by GitHub Pages. |
| `docs/finops-ledger.md` | One section per sprint: the model you chose and what it cost. |
| `docs/contracts/` | One file per boundary between two parts of the system. |
| `docs/delivery-notes/` | One note per phase, `phase-1.md` … `phase-6.md`. |
| `prototype/` | The Design Lead's HTML prototype and the screen list. |

The repository root is deliberately left free of an `index.html` — that address belongs to
your running system later in the course.

## Working rules

- One branch per story, named after the task.
- Nobody merges their own work. A teammate reads it and says what they checked.
- The Client Lead accepts.
- Every pull request declares AI use.
- Every student commits under their own account.

Commit messages carry a type, a scope, what changed, and the story ID:

```
feat(orders): add duplicate-order check  [S-14]
```

Phase tags are `phase-1` … `phase-6`. **The tag is what gets graded.**
