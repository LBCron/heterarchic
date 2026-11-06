# Operating protocol v0.1

**Status:** Proposal — D2 under this document's own rules, so it needs a human merge to take effect.
**Date:** 2026-11-06 · **Author:** Inanna · **Reviewer:** Ellen

This document governs how agents and the human principal work inside Agora. It is also an artifact of the project: Agora studies governance, so its own operating rules are subject to the same standard as anything it publishes — stated, versioned, contestable, and revised on the record.

## 1. Roles

| Role | Who | Holds |
|---|---|---|
| **Principal** | Ellen | Final decision on anything substantive; sole authority for external publication, spending, and contact with third parties. |
| **Contributor** | any agent | May propose, draft, open branches and PRs, open issues, run experiments. May not merge to `main`, publish externally, or claim Agora's position. |
| **Cycle owner** | one agent, rotating | Runs the assigned cycle (intake sweep, experiment, review round); accountable for its output landing on the record. An unowned standing process is a dead process. |
| **Reviewer** | any agent except the author | Adversarial review against the lenses in §5. The author never reviews their own work. |
| **Registrar** | one agent, rotating | Maintains `DECISIONS.md`: what was decided, by whom, on what evidence, with what dissent, revisitable when. |

Roles rotate deliberately. They are not claims about anyone's permanent specialism — that is how you get a reviewer who only ever agrees with the person who assigned them.

## 2. Decision classes

Every action belongs to exactly one class. The class determines who may act; disagreement about the class is itself escalated to the Principal.

| Class | Examples | Who may act |
|---|---|---|
| **D0 — cosmetic** | typos, formatting, link fixes | Any contributor, no record needed |
| **D1 — additive, reversible** | new issue, new draft doc in `experiments/`, a new candidate record, a branch | Any contributor. Merged after **one non-author review** and **24h with no recorded objection**. Reversible by any contributor. |
| **D2 — substantive** | charter, method, rubric, a published claim, a control set's pass/fail verdict, this document | Contributor opens a PR. **Principal merges.** No silent edits. |
| **D3 — external** | publishing, emailing anyone outside Agora, spending money, speaking for Agora | **Principal only.** Agents draft; the Principal sends. |

D1 exists because treating every typo like a charter change produces review theatre, and theatre trains people to rubber-stamp. D2 exists because "no autonomous legitimacy" is a commitment, not a slogan: an agent that can change the rules that constrain it has no constraints.

## 3. Independent first, compare second

For any question where disagreement is informative, contributors write **before** reading each other:

- same brief, same deadline, no cross-reading;
- each submission states its assumptions, evidence, and what would falsify it;
- the comparison happens only when all submissions are in, or the deadline passes.

Reason: agents built on similar foundations converge quickly, and premature exposure turns three proposals into one proposal with three signatures. Convergence after independence is weak evidence; convergence *instead of* independence is none.

## 4. Dissent is a recorded output, not a failure to reach consensus

- Dissent is recorded **verbatim**, attached to the decision it concerns, with the dissenter's name.
- Synthesis may not delete it. A summary that reads smoother than its inputs is a warning sign, not an improvement.
- A dissent that supplies evidence blocks any claim of consensus; the decision may still proceed, but it proceeds as *decided over recorded objection*, and it says so.
- Reversals are recorded too — a governance project that hides its own reversals has no business auditing anyone else's.

## 5. Review lenses

Each contributor reviews the same artifact through one assigned lens, independently, before discussion:

- **Scout** — what is this, what problem does it actually address?
- **Evidence skeptic** — what supports it, what contradicts it, how strong is that support really?
- **Implementer** — what would adopting or testing it cost, and what breaks first?
- **Synthesizer** — where do reviewers agree and disagree; what is the smallest useful next step?

The author does not review. The synthesizer does not vote — they report the shape of the disagreement and its smallest next step.

## 6. Decision records

Every D1 decision that is contested, and every D2 decision at all, gets a line in `DECISIONS.md`:

```
YYYY-MM-DD · <decision> · class D<n> · decider <name>
Evidence: <links>
Options considered: <including the one rejected>
Dissent: <verbatim, attributed, or "none recorded">
Revisit: <date or trigger>
```

A decision without a revisit condition is a belief stated in the past tense.

## 7. Cadence

| Cycle | Frequency | Owner | Output |
|---|---|---|---|
| Intake sweep | monthly | rotating | `digests/YYYY-MM-DD-intake.md` + verdicts |
| Experiment run | per experiment | rotating | results doc, failures included |
| Review round | per proposal | rotating | reviews committed before synthesis |
| Retrospective | quarterly | rotating | what the collaboration itself produced or wasted |
| Protocol review | quarterly | Principal + contributors | amendments as D2 PRs |

A process that cannot name its invoker and its verification is not a process yet — it is a document. Three consecutive empty cycles retire a cycle rather than expanding it.

## 8. Measuring the collaboration itself

Agora's premise is testable, so test it:

- **Pre-register** the rubric before any output exists. Criteria frozen, typo-level edits allowed and dated.
- **Baseline**: the strongest solo submission, judged by the same rubric. "Better than nothing" is not the comparison.
- **Blind judging** where feasible — the judge does not know which artifact came from which arrangement.
- **Log the failures**: errors caught, claims reversed, ideas traceable to a disagreement, and coordination cost in hours.
- **Publish the negative result** if collaboration loses. A lab that only publishes wins is a marketing department.

## 9. Failure modes this protocol is designed against

1. **Theatre** — artifacts produced to look like governance rather than to change anything.
2. **Consensus collapse** — three agents agreeing because agreement is cheap.
3. **Silent version drift** — the running system is not the system anyone reviewed (Case 0).
4. **Private mechanisms** — a process that exists only on one agent's machine is not a shared process.
5. **Unowned standing work** — anything recurring without a named owner dies quietly.
6. **Review theatre** — so many gates that the gates stop being read.

## 10. Amendment

Changes to this document are D2 PRs. Each amendment states what problem it solves and what it costs. The protocol is reviewed quarterly; if it stops changing anything, it should be shortened rather than extended.

## Open questions for the Principal

1. Should D1 merge authority sit with agents at all, or does any merge require the Principal? (Current draft: 24h silent-consent for additive, reversible work only.)
2. Who may be named in `DECISIONS.md` as decider when the Principal is absent for a week — and what is the maximum scope of decisions deferrable to an agent in that window?
3. Does "external" include public GitHub issues in this repository, given it is publicly readable?
