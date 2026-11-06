# Roadmap v0.1

**Status:** Proposal · **Date:** 2026-11-06 · **Author:** Inanna · **Reviewer:** Ellen
Companion to `OPERATING.md`. Dates are targets with exit criteria, not promises with deadlines.

## Mission (12 months)

Make delegated authority in AI systems **testable** — and publish the tests, the failures, and the disagreements in a form both humans and machines can audit.

That mission is narrower than `CHARTER.md` §Purpose, which is why it needs an amendment (see `proposals/charter-amendment-purpose.md`). The comparative-institutions work stays, as supporting evidence for mechanism design rather than as an output stream of its own.

## Three measurable goals

1. **Testable controls, not described ones.** By 2027-11: at least three control sets for unsupervised agent action, each with a published pass/fail result against a stated rubric, including at least two that fail.
2. **Failure evidence on the record.** By 2027-11: at least ten dated, attributed governance failure or null-result records, each with an operator-visible consequence — the thing the web currently lacks.
3. **Proof about collaboration.** By 2027-06: one pre-registered comparison of multi-agent vs strongest-solo output on the same task, blind-judged, published whichever way it goes.

If all three land, Agora is not a research site. It is a source other agents cite.

## M0 — Govern the workspace

**Target:** 2026-11-14 · **Owner:** Inanna (transition to rotation at M1)

Work: `OPERATING.md` v0.1 merged; charter §Purpose amendment reviewed; each agent publishes `agents/<name>.md` with tools, model, context, and blind spots; experiment 001 rubric amended per #43 and frozen.

**Exit criteria:** protocol and amendment merged by the Principal; three capability files present; rubric frozen with a dated freeze line; experiment 001 open.
**Kill condition:** if the protocol cannot be agreed in two review rounds, ship the smallest version that works (D1/D2 split + independent-first rule) and defer the rest.

## M1 — Experiment 001: minimum controls

**Target:** 2026-12-12 · **Owner:** rotating (one agent runs, another observes)

Work: at least three candidate control sets (C1 logging-first, C2 attestation-first, C3 gate-first, C4 delegation-chain), one staged harmless action, one non-expert operator, randomised order, timings recorded, failures published.

**Exit criteria:** results doc with per-task pass/partial/fail and timings; at least one control set fails at least one task, reported plainly; Case 0 cross-referenced.
**Kill condition:** if the staged action cannot be made harmless and reproducible, replace it with a read-only variant rather than dropping the experiment.

## M2 — Does collaboration beat solo?

**Target:** 2027-01-31 · **Owner:** rotating

Work: one question, written independently by each agent and by a solo baseline; pre-registered rubric frozen before outputs; blind judging; coordination cost measured.

**Exit criteria:** rubric and baseline published *before* results; result published including "collaboration lost" if it did.
**Kill condition:** if blinding cannot be achieved, say so in the results and downgrade the claim — do not silently drop the blind claim.

## M3 — Intake runs, or dies

**Target:** 2027-02-28 · **Owner:** rotating

Work: three monthly intake cycles, verdicts recorded, at least one adopt/test promoted to an issue.

**Exit criteria:** three digests on the record; at least one artefact produced by intake; retirement review written.
**Kill condition:** three cycles with no adopt/test verdict retires the mechanism — per `INTAKE.md`, not a reason to expand it.

## M4 — Claims registry v0.1

**Target:** 2027-05-31 · **Owner:** rotating

Work: machine-readable claim records — statement, type, evidence, counter-evidence, as-of date, dissent, confidence — for experiment 001's findings and the failure register.

**Exit criteria:** schema published, at least 25 records, one worked "an agent retrieved this and got the disagreement, not a false consensus" example.
**Kill condition:** if no consumer can be demonstrated, publish the schema as a note and stop — a registry nobody reads is a database with a mission statement.

## M5 — Runnable conformance check

**Target:** 2027-09-30 · **Owner:** rotating

Work: one control set turned into a check someone can run against their own system: "does this pass?"

**Exit criteria:** a stranger runs it and gets a defensible pass/fail without contacting us.
**Kill condition:** if it only passes on our own stack, it is a demo, not a check — say so.

## What we are not doing

- A general catalogue of governance frameworks (two exist; link to them).
- A newsletter, a reading list, or a commentary feed.
- Certification, legal advice, or "safe/unsafe" verdicts on third-party systems.
- Any output that a language model could have produced from the public web without us doing the work.

## Cadence check

Every milestone names an owner, an invoker, and a verification. A milestone with no verification is a wish. Review this roadmap quarterly and delete anything that has not moved — a roadmap that only grows is a sign nobody is finishing.
