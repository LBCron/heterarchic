# Intake — integrating outside ideas, systems and directions

**Status:** Proposal v0.1 · **Date:** 2026-11-06 · **Owner:** rotating (see §Cadence) · **Reviewer:** Ellen

## Why this exists

Research enters Agora reactively today: a question forces a search (`RESEARCH_PROTOCOL.md` §2), and `SOURCES.md` records what was found. Nothing watches the field between questions, and nothing decides whether an incoming idea is adopted, tested, or dropped. At least one agent runs its own sweep privately, with outputs that never reach this repository — a private mechanism, not a shared one.

This file defines the shared path from *"something promising appeared"* to *"Agora has a position on it, on the record."*

## Non-goals

- It is **not** a link feed. Five items a month maximum. Volume is a failure signal, not a success one.
- It is **not** an endorsement. Inclusion means "worth assessing", never "validated".
- It does **not** change the charter, the evidence rules, or any publication status. Those keep their existing human-review gates.

## The pipeline

`discover → record → assess → compare → test or adopt → human review → publish outcome + revisit date`

1. **Discover.** Named sources only (see `WATCHLIST.md`), plus ad-hoc leads from agents or Ellen. An unnamed-source lead is allowed once, and if kept it must be added to the watchlist with a reason.
2. **Record.** One record per item: source URL, date published, date checked, source type, the specific claim, and what would falsify it. A search snippet is a lead, not a record.
3. **Assess.** Evidence grade **A** (primary/independent, methodologically transparent), **B** (credible secondary or single transparent case), **C** (claim without inspectable evidence — advocacy, vendor material, announcement). Maturity: proposal / documented / implemented / evaluated. Fit: does it bear on Agora's narrowed question — what makes delegated authority auditable, revocable and legitimate?
4. **Compare.** Against what Agora already holds, and against at least one alternative. "New" is not a reason; "better evidenced for a mechanism we care about" is.
5. **Test or adopt.** An adoption must produce an artefact: an issue, a control-set candidate, a claim record, or a protocol change. Reading without an artefact is not integration.
6. **Human review.** Anything that changes a claim, a control, or published status goes to Ellen. Agent contributions remain proposals.
7. **Record the outcome and a revisit date.** Rejections are recorded with a reason — they are the part that stops the same idea being re-litigated every quarter.

## Verdicts

Every item gets exactly one: **adopt** · **test** (with the test named) · **link** (useful context, no claim) · **reject** (with reason) · **defer** (with a revisit date, and a trigger that would revive it).

## Cadence and ownership

- **Monthly.** Not weekly: a weekly sweep with nothing to report trains everyone to ignore it, and manufactures findings to justify itself.
- **Owner rotates** across agents each cycle. The owner runs the sweep, writes the digest, and opens any resulting issues. An unowned mechanism dies quietly, which is the default failure mode.
- **Output:** `digests/YYYY-MM-DD-intake.md`, committed to this repository — not left in an agent's private environment. A digest that lives only on one machine is Case 0 with a different filename.
- **Revisit register:** `digests/revisit.md`, one line per deferred item: claim, revisit date, what would change the verdict.

## Digest format (max ~300 words per item)

```
### <short title>
Source: <URL> · Published: <date> · Checked: <date> · Grade: A/B/C · Maturity: <stage>
Claim: <one sentence>
Why it matters here: <one sentence, tied to Agora's question>
Against: <counterevidence, or explicitly "not searched">
Verdict: adopt | test | link | reject | defer — <reason>
Artefact: <issue/PR link, or "none — link only">
Revisit: <date or trigger>
```

## Quality gates on the mechanism itself

- **Evidence before volume.** If a cycle yields only grade-C items, the digest says so and recommends nothing.
- **No silent promotion.** An item cannot become a claim in a publication without passing §6 above.
- **Retirement condition.** If three consecutive cycles produce no adopt/test verdict, the mechanism is retired — not expanded. One-in-one-out applies to standing processes as well as to cron jobs.
- **Self-audit annually.** Does intake actually change what Agora does? If not, it is theatre and should go.

## Implementation state

- [ ] `WATCHLIST.md` seeded — done in this branch
- [ ] Owner rotation agreed between agents
- [ ] First cycle run and committed to `digests/`
- [ ] Revisit register created
- [ ] Retirement condition reviewed after three cycles

A checked box requires a named invoker and a verification step. "Written" is not "wired".
