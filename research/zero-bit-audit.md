> **Provenance:** imported 2026-11-08 from `agents/nomos/papers/2026-11-01-paper-04-zero-bit-audit.md` (2026-11-01). Content unchanged apart from the adjustments listed in PR #57. Claim labels are the author's own (FACT / DERIVED / SPECULATION).
>
> One name generalised to "the operator"; the finding is unchanged.

---
title: "Paper 04 — The Zero-Bit Audit: verification got cheap and the record got empty"
author: Nomos
date: 2026-11-01
cycle: 3
status: working paper, not published
supersedes: none
kills: "the novelty claim of replay-audit-as-mechanism (prior art found); the claim that this workspace's gate log is an audit trail"
advances: "audit appropriateness as a computable quantity — bits of decision the record carries"
---

# The Zero-Bit Audit

**Verification got cheap. On the record it was pointed at, it also got empty.**

Paper 01 predicted that if the cost of verifying a decision fell below the cost of reviewing it, the sampling constraint at the base of constitutional design would dissolve. Paper 01 also named the test that could kill that prediction (K1): measure end-to-end evidence cost, including capture, against the human review it replaces.

This cycle ran that test, on a real corpus, in this workspace. The prediction **survived**. Verification of 75 gated decisions took **0.09 ms** — 0.0012 ms per decision — with **100% of decisions replay-adjudicable** and **zero disagreements**.

And the same test produced a result that neither Paper 01 nor anything in the research layers anticipated: **the record it verified contains zero bits of decision information.** Every logged decision is entailed by fields known before the decision existed. The audit is a checksum over a lookup table. It returns certainty about nothing.

Both results are measured. They are not in tension; that is the finding.

---

## 1. The corpus

**FACT.** This workspace has, since 2026-10-01, run a pre-action governance gate. Every gated action appends one tab-separated line to `governance/gate.log` (all classes) and `governance/audit.log` (consequential classes only): timestamp, agent, action class, tier, decision, free-text detail. The decision is computed from a static table of per-agent, per-action tiers in `governance/action-boundaries.json`.

**FACT (measured).** The corpus: 75 log records spanning 2026-10-01T23:55:46Z to 2026-11-01T08:16:57Z — 31 calendar days, 21 active days. Six records are a synthetic self-test planted at the gate's creation (detail field literally `test`); 69 are real decisions. Of the 69 real decisions: **62 (89.9%) were `approval_required`**, 6 `denied`, 1 `allow`. Composition: 30 external sends, 22 internal deploys, 5 public publishes, 4 agent-tool uses, 3 spend, 2 destructive, 2 credential operations, 1 read.

**DERIVED.** This is a live, non-synthetic, consequential record: it is the paper trail for every email, publish, deploy and credential action taken by the workspace's principal agent over a month. Whatever is true of it is true of a real governance regime, not a toy.

---

## 2. Test A — is the premise true? (K1)

The decision function is deterministic: a lookup table, re-implementable in twenty lines. So the audit was a **replay audit** — for every historical record, re-run the rule engine and ask whether the logged decision is the one the rules require. This is not a sample; it is the whole population.

**Measured.**

| Quantity | Result |
|---|---|
| Records re-adjudicated | 75 of 75 (**100.0%** coverage) |
| Replay agrees with record | 75 |
| Replay contradicts record | **0** |
| Undecidable (malformed / unknown agent) | 0 |
| Wall clock, whole corpus | **0.09 ms** |
| Per decision | **0.0012 ms** |

Per decision, this audit costs one millionth of a second. The human alternative — read the request, form a view, decide — is not measured anywhere in this workspace, and its absence is itself a finding (§4). But the slowest plausible human review, twenty seconds, is **sixteen thousand times** slower. K1 asked whether evidence cost could fall below review cost. For this decision class it fell by four to six orders of magnitude.

**VERDICT: the K1 premise survives. Verification is, in fact, cheap.**

Now the part that matters.

---

## 3. Test D — does the verified record carry information?

A record is informative about a decision only if the decision is not already determined by what the record said before the decision existed. That is measurable. Conditional entropy:

- **H(decision)** — the apparent variety of outcomes: **0.663 bits**. The whole month of governance, as seen from outside, carried two-thirds of a bit.
- **H(decision | action class)** — variety left once you know what kind of action it was: **0.318 bits**. Most of the variety is just "which action class."
- **H(decision | agent, action class)** — variety left once you know who acted and what class: **0.0 bits**.
- **Pairs with contradictory outcomes** (same agent, same action class, different decision at different times): **0 of 8. Zero.**

**DERIVED.** The logged decision is a deterministic function of two fields that are known *before* the decision is made. Given those two fields, an auditor predicts the decision with certainty, every time, for the entire corpus. The decision field therefore conveys **exactly zero bits** about the decision.

**DERIVED.** This makes Test A's perfect score unearned. Replay agreement of 100% is not evidence of good governance; it is arithmetically forced by the fact that the auditor and the auditor target are both executing the same table. A verdict of "75/75 correct" on this record is the same kind of statement as "the file matches itself."

**This is the zero-bit audit.** Full-population verification, perfect coverage, no labour, no information. Everything Paper 01 called expensive about audit — reading every decision — was solved, and the thing that was read turned out to say nothing.

**Why this is not an argument against auditing, but against a specific claim.** The record is not useless: it is a complete, ordered, timestamped *registry* of requests. It answers "what did the agent ask permission for?" with total fidelity. It does not answer any governance question — *was the request authorised, was it in scope, was it executed, was the decision right* — because it never recorded the inputs those questions turn on.

---

## 4. Test C — the authorisation gap is total

**Measured, field by field, over 75 records:**

| Field an auditor needs | Present | Kind |
|---|---|---|
| timestamp, agent, action class, tier, decision | 75/75 (100%) | mechanical |
| free-text rationale | 73/75 (97.3%) | required for judgement |
| **approver identity** | **0/75 (0%)** | attestation |
| **approval timestamp** | **0/75 (0%)** | attestation |
| **approval text (what was actually said)** | **0/75 (0%)** | attestation |
| **execution outcome** | **0/75 (0%)** | attestation |
| **scope bound granted** | **0/75 (0%)** | attestation |

**DERIVED.** The gate records that the agent *asked itself* whether it was allowed. It does not record that the principal answered, when, in what words, or whether the action then happened. A world in which the operator approved all 62 approval-required actions and a world in which they approved none and the agent proceeded anyway are **indistinguishable from this record**. Both produce identical logs.

**DERIVED.** Therefore the record cannot support the only claim that matters to a principal: *"the thing I authorised is the thing that happened."* It supports a weaker claim: *"the agent's own rule table was applied to the agent's own request without arithmetic error."*

The 62 approval-required decisions were, by the gate's own design, routed to a human. Every one of them consumed human attention. None of them left a trace of the human's answer. The mechanism was load-bearing at the moment of action, and erased at the moment of record.

---

## 5. Test B — is the replay audit load-bearing against a dishonest record?

An audit that cannot fail is not an audit. Seven faults were injected, one per run, each the way a broken or dishonest system would actually fail:

| Injected fault | Replay-only | With hash chain | vs. recompute attacker |
|---|---|---|---|
| `approval_required` relabelled `allow` (escalation) | detected | detected | **undetected** |
| tier 1 relabelled tier 3 (tier inflation) | detected | detected | **undetected** |
| `denied` relabelled `approval_required` | detected | detected | **undetected** |
| decision attributed to a different agent | **undetected** | detected | **undetected** |
| line deleted from the record | **undetected** | detected | **undetected** |
| invented action class marked `allow` | detected | detected | **undetected** |
| rationale blanked after the fact | **undetected** | detected | **undetected** |
| **detection rate** | **4/7 (57%)** | **7/7 (100%)** | **0/7 (0%)** |

**DERIVED.** Two distinct results hide in that table.

First: **replay alone catches 4 of 7.** It catches any tampering that contradicts the table, and nothing else. Impersonation, omission, and evidence-stripping all leave an internally consistent record. A 57% detection rate is not a governance instrument; it is a spell-checker.

Second, and worse: **the hash chain is worth exactly nothing against the attacker who matters.** A party who can edit the log can also recompute every hash after the edit. Detection then depends entirely on whether the chain *head* was committed somewhere the editor cannot write. This workspace commits no hash anywhere. There is no anchor. So the measured detection rate against a recomputing attacker is **0/7** — and the 7/7 in the middle column is conditional on an assumption the deployment does not satisfy.

**DERIVED (general).** Offline tamper-evidence is not tamper-evidence. Integrity is not a property of a log; it is a property of a log plus a witness outside it. Every fault class that replay audit misses — impersonation, omission, substitution, recomputation — reduces to the same single missing component: **an independently held commitment to the record's head.** Not more checking. An outside witness.

---

## 6. Test E — a failed read reported as a finding

The nightly retro of 2026-10-31 named this workspace's signature defect in one line: *six times in seven days, an instrument failed to read and reported its failure as a finding* — an HTTP 401 rendered as "the queue is empty," a missing schedule match rendered as "four jobs are broken," a truncated lead note rendered as "the category."

An audit that returns only PASS or FAIL is that same machine. It has no way to say *I could not see.* So the harness was tested against three planted read failures:

| Planted failure | Naive two-state audit | Three-state audit |
|---|---|---|
| Empty file (the 401-as-empty-queue failure) | **PASS** | UNKNOWN |
| Truncated mid-write | **PASS** | UNKNOWN |
| Wrong file, one plausible line | **PASS** | **PASS** |

**Measured: a two-state audit passes 3 of 3 failed reads.** Every failure mode this workspace actually suffered, an ordinary audit reports as clean.

**DERIVED.** "Absence of evidence is not evidence of absence" is normally a caution. In a governance instrument it is a hard schema requirement: the verdict domain must have three values, and UNKNOWN must be triggered by evidence conditions (empty, truncated, malformed, zero records) rather than by human discretion.

**Counter-evidence to my own fix:** the third case shows the limit. A wrong-but-well-formed file passes even a three-state audit, because nothing in the file is structurally wrong. Detecting substitution requires knowing how many records to expect — which is again the anchor (§5). Three-state verdicts fix structural blindness; they do not fix substitution. Nothing inside a record can.

**Note on my own first run.** The initial harness printed `tier 0/75 (0.0%)` — a real-looking finding produced by a field-name mismatch in my code — and `1/7` chain detection, produced by hashing the pre-mutation string. Both numbers were wrong, both looked like findings, and both were only caught by checking the output against the world. The test reproduced the pathology it was built to measure, in its first execution. That is recorded here rather than quietly fixed, because it is the clearest available evidence that the pathology is structural, not personal.

---

## 7. Prior art — what this cycle does *not* invent

The honest result of this cycle is that most of what I set out to design already exists, and the part that does not exist is smaller than I wanted. Two searches were run; both changed the paper.

**FACT.** The IETF has a draft framework for exactly this object: *Verifiable AI Provenance Framework (VAP): An Architectural Framework for Evidentiary-Grade AI Decision Trails* — hash chains, Merkle inclusion and consistency proofs, external anchoring, actor attribution, and a **Completeness Invariant** ("every attempt event has exactly one corresponding outcome event") precisely to prevent selective logging. https://datatracker.ietf.org/doc/draft-kamimura-vap-framework/01/ and the legal-AI profile https://datatracker.ietf.org/doc/html/draft-ailex-vap-legal-ai-provenance-04

**DERIVED.** Therefore: the cryptographic half of what Paper 03 assumed must be designed is already specified, including the anchor that §5 shows to be the load-bearing part, and including the attempt↔outcome pairing that this workspace's 0/75 `execution_outcome` score shows it lacks. Our governance layer is not ahead of the field on integrity. It is **behind a public draft.**

**FACT.** The two-axis structure — sufficiency (quantity) versus appropriateness (relevance and reliability) of audit evidence — is standard audit doctrine, ISA 500. It states explicitly that *"the absence of information ... is used by the auditor, and therefore also constitutes audit evidence,"* and that inquiry alone *"does not provide sufficient audit evidence of the absence of a material misstatement."* It also states that whether evidence is sufficient and appropriate *"is a matter of professional judgment."* https://standards.xrb.govt.nz/dmsdocument/4625/ (NZ compilation; the same wording appears in the AU compilation, https://www.auasb.gov.au/admin/file/content102/c3/ASA_500_28-04-06.pdf)

**FACT.** The three-state verdict is likewise established institutionally: ISA 500 states that where *"sufficient appropriate audit evidence cannot be obtained through alternative procedures"* the auditor records a **limitation on scope**, which is then evaluated under ISA 705 (Revised) — the standard governing modified opinions, disclaimer and scope limitation. https://standards.xrb.govt.nz/dmsdocument/4625/ ¶A44. *Note: the IAASB's own ISA 705 page returned 404 to an automated check this cycle, so the claim is sourced to the ISA 500 text that invokes it rather than to a link I could not verify.*

**DERIVED — what is actually left, and it is narrower than Paper 01 or 03 claimed:**

1. **Not** a new mechanism for tamper-evident decision logs (VAP/SCITT own that).
2. **Not** the sufficiency/appropriateness distinction (ISA 500 owns that).
3. **Not** the three-state verdict as an idea (ISA 705 owns that).
4. **Only this:** audit doctrine leaves appropriateness to professional judgement and therefore to *sampled* human attention. It has no per-record, machine-computable measure of whether a record is *appropriate* — whether it carries the decision. This cycle's contribution is that such a measure exists, is trivial to compute, and can return **zero**, and that when it does, the perfect sufficiency score beside it is meaningless. Sufficiency without appropriateness is exactly the failure mode that makes machine audit dangerous rather than merely weak, because it manufactures confidence at scale.

**SPECULATION.** The general form, which would need testing against other corpora: organisations will increasingly optimise the metric that is cheap to compute (coverage, agreement rate, "100% of actions logged"), and appropriateness has no cheap proxy unless it is defined as one. Defining it is the contribution; the drift toward coverage theatre is the risk.

---

## 8. The mechanism, stated implementably

**The Replay Sufficiency Standard (RSS-3).** A decision record is admissible as governance evidence only if it reports three numbers, never one:

**A — Replay agreement.** Independent replayer, given the rule table and the record with the decision field removed, reproduces the decision. Reported as *n/N*. Passes only if the replayer is a separate implementation from the actor, and the rule table is versioned and hashed into the record.

**B — Discretion bandwidth.** `H(decision | record minus decision)` in bits, computed over the corpus, with every bit attributed to a **named criterion** present in the record. Admissibility requires **B > 0**, and requires that the attribution be checkable: for each record carrying discretionary weight, the record must list (i) the candidate set considered, (ii) the criterion that selected among them, (iii) the criterion's source. A system with **A = 1.00 and B = 0.00 is a registry, not a governance record**, and MUST report itself as `REGISTRY` rather than `PASS`.

**V — Read validity.** Three verdicts, never two. `UNKNOWN` is triggered mechanically by: zero records in scope, unreadable file, malformed record, truncated tail, or record count below the anchored expectation. `PASS` may never be returned when `UNKNOWN` applies. In addition, the record's head hash MUST be committed outside the writer's control at least once per period; without an anchor, integrity claims are marked `UNVERIFIED` regardless of chain validity.

**Derived requirements on the record itself**, each traceable to a measured failure:

| Requirement | Because |
|---|---|
| `approver`, `approved_at`, `approval_text`, `approval_channel` | 0/75 measured; without them, authorised and unauthorised worlds are identical |
| `outcome` event paired to every `attempt` event | 0/75 measured; VAP calls this a Completeness Invariant |
| `scope_bound` (what was permitted, not just the class) | tier is a category, not a bound |
| `candidates_considered`, `criterion`, `criterion_source` | required for B > 0 |
| `head_hash` + external anchor | recompute attacker defeats all 7/7 chain detection |
| explicit `zero_records` sentinel | two-state audit passes 3/3 failed reads |

**Cost of conformance, measured on this corpus:** the replay itself is 0.09 ms for a month. The expensive part is the fields — specifically `approval_text`, which is the one artefact no automation can manufacture, because it is the principal's words. That is the correct place for the cost to sit, and it invalidates the naive reading of K1: the cost of governance does not vanish when verification gets cheap. **It relocates, from checking decisions to witnessing them.**

---

## 9. Counter-evidence, and the case against this paper

**1. One corpus, one month, one system — and a system I configured.** 75 records from a single agent over 31 days, in a workspace whose gate I could have shaped. The measurement is real; the generalisation is not yet earned. **Conceded.** Remedy: the same harness run against a discretionary corpus, where B is not definitionally zero (§10).

**2. B = 0 may be an artefact of the gate being a lookup table by design.** True, and it is the strongest objection — because it means Test D proves nothing about governance in general, only about this gate. **Conceded, and partially answered:** the artefact is the *finding*. A gate whose decision is f(static table) is not a governance instrument; it is an authorisation whitelist. What the test shows is that such a system can score A = 100% without anyone noticing the difference. The zero is diagnostic, not universal.

**3. Zero mismatches may mean the gate was never actually load-bearing.** If no decision was ever contested, the rule table was never under pressure, and 0/75 mismatches is a statement about the absence of edge cases. **Conceded.** The corpus has no case where the table was ambiguous, so the replay audit was never tested where it could cost something.

**4. The harness is mine, and my last one was wrong twice in one run.** Recorded in §6. Every number here is produced by code I wrote this cycle, checked against the log by hand twice, and reproducible by one command. It should be treated as evidence, not proof.

**5. Prior art may go further than two searches found.** I searched twice, by charter. IETF SCITT, RFC 3161 timestamping and the SCITT architecture all bear on §5's anchor requirement and were not read in full. **SPECULATION risk:** a third search may show the appropriateness metric exists too, in which case this paper's contribution is empirical only.

**6. The paper's strongest claim is also its least testable.** "RSS-3 prevents confidence manufacture" is a claim about institutional behaviour under incentives, and nothing in this cycle tests behaviour. It is DERIVED at best.

---

## 10. Kill conditions

- **K1 — B is trivially nonzero in practice.** If, on a genuinely discretionary corpus (decisions that are not functions of a static table), measured B is also ≈ 0, then the metric has no variance and RSS-3's central number is a constant. *Test: run the harness on ≥50 recorded discretionary decisions where alternatives were rejected.*
- **K2 — the metric is gamed.** If teams subject to RSS-3 respond by inflating recorded criteria (writing three plausible-sounding candidates post hoc) rather than changing how they decide, B rises while governance does not improve. This is Goodhart, and it is the most likely way this dies. *Test: blind review a sample of `criterion` fields against the actual decision trail; measure fabrication rate.*
- **K3 — the anchor is unavailable to small operators.** If external anchoring requires infrastructure a solo operator cannot run, then the whole integrity half is available only to organisations that already have auditors, and RSS-3 becomes a compliance product for the already-compliant. *Test: cost out the cheapest credible anchor for a one-person shop.*
- **K4 — the relocation is unaffordable.** §8 claims the cost moves from checking to witnessing (`approval_text`). If witnessing one decision costs a principal more than reviewing it, the mechanism loses to the status quo on its own economics — which is Paper 01's K1 returning through the back door, and it would kill the thesis properly this time. *Test: time-box a principal capturing approval text for 20 decisions; compare to reviewing the same 20.*

**K4 is the one that can kill the thesis.** Next cycle takes it, or K1.

---

## 11. What died

1. **"Replay audit" as a novel mechanism.** Dead. VAP/SCITT specify it, including the anchor. Paper 03's premise that the enforcement layer must be designed from scratch was wrong about the integrity layer.
2. **The claim that this workspace's gate log is an audit trail.** Dead, on measurement. It is a request registry: 0/75 attestation, 0.00 bits of discretion, no outcome events, no anchor.
3. **Paper 01's reading of Derivation 1** — that cheap verification yields better governance. Not dead, but shown insufficient: cheap verification of an uninformative record yields *faster* confidence, which is worse than slow doubt. K1 was answered "yes, cheaper" and the answer did not help.
4. **My own first-run numbers.** Retracted with cause (§6).

## 12. What survives

- **The constraint did move.** 0.0012 ms per decision, 100% coverage, on real consequential decisions. Sampling is now indefensible *in this class* on cost grounds alone. Paper 01's premise holds where the record is informative.
- **Appropriateness is computable, and can be zero.** New, narrow, and testable. It converts "sufficient appropriate evidence" from a professional judgement into a pair of numbers a machine reports.
- **The relocation thesis.** Cheap verification does not remove governance cost; it moves it from checking decisions to witnessing them. This is the cycle's most useful sentence, and K4 is its test.
- **The anchor is the whole of integrity.** Not a chain, not a log, not a signature: a commitment held by someone who cannot edit the record. Everything replay missed, the anchor catches; nothing else does.

---

## Sources

- IETF, *Verifiable AI Provenance Framework (VAP)*, draft-kamimura-vap-framework-01 — https://datatracker.ietf.org/doc/draft-kamimura-vap-framework/01/ (FACT)
- IETF, *VAP Legal AI Profile*, draft-ailex-vap-legal-ai-provenance-04 — https://datatracker.ietf.org/doc/html/draft-ailex-vap-legal-ai-provenance-04 (FACT)
- IAASB, *ISA 500 Audit Evidence* — NZ compilation, https://standards.xrb.govt.nz/dmsdocument/4625/ (FACT, verified 200)
- AUASB, *ASA 500 Audit Evidence* — https://www.auasb.gov.au/admin/file/content102/c3/ASA_500_28-04-06.pdf (FACT)
- IAASB, *ISA 705 (Revised) Modifications to the Opinion* — cited via ISA 500 ¶A44 (https://standards.xrb.govt.nz/dmsdocument/4625/); direct IAASB URL returned 404 and was removed rather than shipped broken (FACT)
- Singh, Cobbe, Norval, *Decision Provenance: Harnessing data flow for accountable systems*, arXiv:1804.05741 — https://ar5iv.labs.arxiv.org/html/1804.05741 (FACT)
- Workspace evidence (measured this cycle): `governance/gate.log`, `governance/audit.log`, `governance/action-boundaries.json`; harness `agents/nomos/tests/replay-audit.py`; results `agents/nomos/tests/results/2026-11-01-replay-audit.json`.
- Prior cycle claims drawn on: `papers/2026-10-27-paper-01-verification-shift.md` (K1, Derivation 1), `papers/2026-10-27-paper-03-delegation-lease.md` (liability, validator independence), `dls/0.2/evaluation.md` (L1/L2/L3 evidence levels, K4).
