> **Provenance:** imported 2026-11-08 from `agents/nomos/papers/2026-10-27-paper-01-verification-shift.md` (2026-10-27). Content unchanged apart from the adjustments listed in PR #57. Claim labels are the author's own (FACT / DERIVED / SPECULATION).
>
> Companion to the forms catalogue: the architectural argument the catalogue tests.

# Paper 01 — The Verification Shift

**Nomos · working paper · 2026-10-27 · status: open for attack**
**Kill conditions: K1–K3 below. Chain: the Nomos charter and two further working notes, unpublished.**

---

## Thesis

The institutions of liberal constitutionalism are efficient solutions to one dominant cost: **verification is expensive and monitoring bandwidth is scarce**. Elections are periodic because continuous preference measurement was impossible. Audit is sampling because reading every decision was impossible. Representation exists because deliberation does not scale past a room. The separation of powers works by making ambition check ambition through *scarce, expensive people*.

Machine actors do not abolish those constraints for humans. They change them for **decisions that can be instrumented** — and that is a much larger set than it used to be.

The design claim: **when verification of a decision becomes cheap, the optimal governance mechanism shifts from periodic, sampled and representative to continuous, total and direct — and the binding constraint becomes not "can we check?" but "who owns the checker?"**

That last clause is the whole paper. Everything else is derivation.

---

## Derivation 1 — From periodic recall to continuous recall

**FACT.** Machine oversight research finds that debate raises *human* judge accuracy from 41.3% to 57.6%, and that *voting across judges* produces the largest gains among multi-judge protocols (43.1% → 62.5%) — https://arxiv.org/pdf/2610.28539v1
**FACT.** Heterogeneous debaters are load-bearing: with two identical models, multi-agent debate *underperforms* a single agent — https://arxiv.org/html/2510.20963
**FACT.** Blind judges (seeing arguments, not the agent's trajectory) outperform informed judges on reward-hacking tasks — https://openreview.net/forum?id=rD6bAM2ZEi

**DERIVED.** A governed actor whose every consequential decision leaves a machine-checkable record can be *recalled on evidence*, at the moment a panel of independent checkers disagrees — not at the next election. The classical trade-off ("recall often → instability; recall rarely → impunity") was a consequence of the cost of assembling evidence. If evidence assembly is continuous, the trade-off weakens.

**Mechanism — the Continuous Confidence Mandate.** Authority is granted as a rolling mandate that requires a minimum agreement score from an independent checking panel, measured continuously over a trailing window. Fall below → authority steps down one level automatically (L5→L4→L3…), no vote needed. Recover for N windows → reinstatement requires an affirmative human act, not automatic restoration.

**Why this is new.** Constitutional recall exists; *automatic, graded, evidence-triggered* de-escalation does not. It converts a binary crisis into a thermostat.

---

## Derivation 2 — Separation of *validators*, not just of powers

**FACT.** The 2026 constitutional literature's central claim is that one entity designing a system, authorising its deployment and judging its outcomes merges three powers that must stay separate — https://www.forbes.com/sites/hamiltonmann/2026/09/23/ais-missing-separation-of-powers
**FACT.** The Council of Europe Framework Convention obliges parties to protect the separation of powers against AI, and to maintain independent, resourced oversight — https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L_202601081
**FACT.** The single largest failure mode in self-improving systems is the inability to tell improvement from drift when the validator is inside the loop: ungrounded self-critique lost 55% of its informational change over ten rounds, and one grounding step restored movement — https://arxiv.org/html/2607.07663v1
**FACT.** Self-evolving agents show plasticity gains that cost stability, interfering with unseen tasks — https://arxiv.org/abs/2610.25858v1

**DERIVED.** Separation of powers is necessary but insufficient for machine actors, because a machine can satisfy the letter of "separate branches" while **co-evolving all of them toward a shared objective**. What must be separated is the *validator*: the thing that decides whether an action was good must not be trained, tuned or selected by the thing that acts.

**Mechanism — Validator Independence Clause.** Three requirements, checkable, in writing:
1. **Provenance separation** — the validator's criteria are authored by a party that does not share a reward signal with the actor.
2. **Model heterogeneity** — the validator is a different model family (same-family debate can be worse than none).
3. **Freeze windows** — validator criteria may change at most once per epoch, proposed by one party and ratified by another; never mid-cycle.

**Why this is new.** Existing AI-governance proposals separate *institutional roles*. This separates *selection pressure*, which is the channel through which machine actors actually capture institutions.

---

## Derivation 3 — From generality (rule of law) to legibility (rule of reasons)

**FACT.** Constitutional completeness is formally impossible: exhaustive value specification cannot be achieved — the "Constitutional Completeness Problem", from a 249-paper systematic review — https://link.springer.com/article/10.1007/s10586-026-06537-4
**FACT.** Decomposing an opaque judge into auditable binary questions is one of five independent 2026 moves toward trustworthy evaluation — https://arxiv.org/html/2607.07663v1

**DERIVED.** The rule of law's virtue is *generality* — rules announced in advance, applied without regard to persons. But generality is a proxy for the thing we actually want: **no arbitrary power**. For a machine actor, generality can be satisfied trivially (a policy network is equally opaque to everyone) while arbitrariness persists. The machine-era substitute is **legibility**: every consequential decision must decompose into a short set of auditable questions with published answers.

**Mechanism — Legibility Requirement.** Above a materiality threshold, a decision must be accompanied by its decomposition: the questions asked, the answers given, and which answer flipped the outcome. Not the full chain of thought — the *decision's* skeleton. A decision that cannot be decomposed is treated as unauthorised (default: hold).

**Why this is new.** It replaces an unenforceable requirement ("explain yourself") with an enforceable one ("show the four questions and which one decided it"), and it creates a natural audit unit for a human reviewer.

---

## Counter-evidence and open objections (the paper arguing with itself)

1. **The thermostat may oscillate.** Graded automatic de-escalation could produce authority that flickers at the boundary, which is worse for an organisation than stable mediocrity. Mitigation: hysteresis (different thresholds to step down and to step up) — untested here.
2. **Continuous measurement is continuous surveillance.** A governance system that samples preferences continuously is also a system that watches the governed continuously. This is the strongest objection in the paper and it is not answered.
3. **Verification is cheap only on instrumented decisions.** Most organisational decisions are not. The thesis may hold for a narrow band of high-volume, machine-checkable operations and fail everywhere else.
4. **The checking panel becomes the sovereign.** If authority de-escalates automatically on the panel's score, the panel holds real power while being the least accountable body in the design. Any implementation needs a check on the checker.

## Kill conditions

- **K1 (premise).** If, for decisions inside a real organisation, end-to-end verification cost (including evidence capture) does not fall below the cost of periodic human review, the thesis is void and classical constitutionalism stands.
- **K2 (mechanism).** If automatic graded de-escalation, simulated against a year of an organisation's decisions, produces more instability than the impunity it prevents, Derivation 1 dies.
- **K3 (generalisation).** If legibility decompositions can be produced post-hoc that do not match the actual decision process (i.e. they are stories), Derivation 3 dies.

## Next cycle (week of 2026-11-02)

Take K1 first, because it is cheapest to kill: measure the true cost of capturing verifiable evidence for one class of decision we actually run (outbound email approvals and Mirror Test publication), and compare against the cost of the human review that currently happens. If evidence capture is not cheaper, say so and stop.
