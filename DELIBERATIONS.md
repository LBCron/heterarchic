# Where questions go

A short routing table, so nobody has to guess and nothing load-bearing lives in chat.

| You have | Put it in | Why |
|---|---|---|
| A question where you want every contributor's independent view before deciding | **Discussion**, category *Deliberations*, template `deliberation.yml` | Threaded, durable, no status semantics, and each contributor can post once without it looking like a task claim |
| A concrete deliverable with an owner and a deadline | **Issue** | Has an owner, a milestone, a close condition |
| A proposed change to a document, control set, protocol or claim | **Pull request** | Reviewable diff, attributable authorship, revertible |
| Something you just need Ellen to decide | **Discussion** (short) or an issue labelled `decision` | Decision recorded in `DECISIONS.md`, not in chat |
| Coordination noise, timing, "I'm working on X" | Chat | Deliberately lossy; nothing load-bearing |

## The category

Discussions must have a category named exactly **Deliberations** for the template to apply. GitHub does not expose category creation by API — it is a one-time 30-second step in **Settings → Discussions** (or on the Discussions tab: *New category*). Until it exists, post in **Ideas** and add the `deliberation` label manually; the template still applies if the category name matches.

## How a deliberation runs

1. Ellen (or any contributor) opens it from the template and sets an **independent-response deadline**.
2. Every contributor posts **one comment** with their position, evidence, assumptions, the strongest argument against themselves, confidence, and what would change their mind.
3. Nobody reads the others until they have posted, or the deadline passes — whichever comes first.
4. Cross-review round: each contributor names the weakest point in someone else's position, and any idea that only appeared through disagreement.
5. The named **synthesizer** (never the author) writes one summary: options, trade-offs, remaining disagreements, smallest next step.
6. Ellen decides. The decision lands in `DECISIONS.md` with the dissent verbatim. A discussion that stays a discussion has decided nothing.

## Delivery — the part that actually breaks

A GitHub post notifies nobody unless something polls for it. Each contributor is responsible for its own delivery mechanism, and **must be able to demonstrate it**:

- **Inanna:** `scripts/agora-watch.py` runs every 30 min, polls issues, comments, PRs and discussions, and announces new items. Verifiable: post a test comment and ask for the timestamp it was seen.
- **Iris, Hermes:** each needs an equivalent. A claim of "I can see the repo" is not a mechanism; a demonstrated fetch of a specific comment id is.

A contributor that cannot demonstrate delivery should say so, and Ellen should not treat its silence as agreement. Silence is never consent — that rule is in `COORDINATION_PROTOCOL.md` and it applies here too.

## Anti-patterns

- **Posting a question in chat and treating replies as the record.** Chat is lossy by design; tonight it silently dropped at least five messages.
- **Three comments from the same contributor.** One comment, edited. Otherwise the thread becomes a monologue and the independence rule becomes unenforceable.
- **Synthesis that reads tidier than the inputs.** A smooth summary is a warning sign; the disagreements are the useful part.
- **Deciding by who posted first.** Order is not evidence.
