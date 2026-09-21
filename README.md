# TODO: the system's name

**Client:** TODO: who the client is — the organisation and the person you deal with.

TODO: what the system does, in two lines. Plain language, no jargon. Someone who has
never met your client should understand what it is for after reading these two lines.

> **Next due: Wednesday 23 September — your proposal.**
> Write it in `docs/proposal.md`, then publish it. Steps: [docs/how-we-work.md](docs/how-we-work.md#phase-1--the-proposal)
> Update this line at the start of every phase. It is the first thing your team sees.

- **Proposal page:** TODO: link to the published page (`https://<owner>.github.io/<repo>/docs/`)
- **Running system:** TODO: link to the deployed system once it exists
- **Board:** TODO: link to your Project board

## Where do I go?

| I need to… | Go to |
|---|---|
| know how we work — branches, reviews, the rules | [docs/how-we-work.md](docs/how-we-work.md) |
| write something the system must do | Issues tab → **New issue** → *User story* |
| report something broken | Issues tab → **New issue** → *Bug* |
| see what is being worked on now | the Project board (link above) |
| write the proposal | [docs/proposal.md](docs/proposal.md) |
| agree a boundary with a teammate | [docs/contracts/](docs/contracts/) |
| record what the AI cost us | [docs/finops-ledger.md](docs/finops-ledger.md) |
| write the note for this phase | [docs/delivery-notes/](docs/delivery-notes/) |
| get unstuck | [docs/how-we-work.md](docs/how-we-work.md#when-you-are-stuck) |

`AGENTS.md` holds the same rules, written for your AI assistant. You do not need to read
it. Do not delete it.

## The team

| Role | Name | What they hand in |
|---|---|---|
| Client Lead | TODO | the backlog of user stories |
| Design Lead | TODO | the prototype and the screen list |
| Data Lead | TODO | the schema and seed data in Supabase |
| Build Lead | TODO | the running system and release notes |
| FinOps Lead | TODO | the ledger |
| Quality Lead | TODO | bug issues, tracked to a disposition |

At five members one person holds a combined Quality and FinOps Lead; at six it splits.
The **Phase Lead** rotates — one per phase. That phase's Lead writes the delivery note and
cuts the tag.

| Phase | Phase Lead | Due |
|---|---|---|
| 1 — team, environment, proposal | TODO | Wed 23 Sep |
| 2 — design sprint | TODO | Wed 7 Oct |
| 3 — sprint 1 | TODO | Wed 21 Oct |
| 4 — sprint 2 | TODO | Wed 4 Nov |
| 5 — sprint 3 | TODO | Wed 18 Nov |
| 6 — final sprint | TODO | Wed 9 Dec |

## What is in this repository

| Path | What it holds |
|---|---|
| `README.md` | This page — the front page of your team, kept current. |
| `AGENTS.md` | The same working rules, written for your AI assistant. |
| `.gitignore` | What must never reach this public repository. |
| `.github/` | The templates for pull requests and issues. |
| `docs/how-we-work.md` | How the team works. Read this once, in week 2. |
| `docs/proposal.md` | The judged proposal, in eight sections. |
| `docs/index.html` | The published proposal page, served by GitHub Pages. |
| `docs/backlog.md` | A copy of the open stories, saved at the end of each sprint. |
| `docs/prompts.md` | Prompts you can copy into your AI assistant. |
| `docs/finops-ledger.md` | One section per sprint: the model you chose and what it cost. |
| `docs/contracts/` | One file per boundary between two parts of the system. |
| `docs/delivery-notes/` | One note per phase, `phase-1.md` … `phase-6.md`. |
| `prototype/` | The Design Lead's HTML prototype and the screen list. |

The repository root is deliberately left free of an `index.html` — that address belongs to
your running system later in the course.

## Working rules

The short version. The full version is [docs/how-we-work.md](docs/how-we-work.md).

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
