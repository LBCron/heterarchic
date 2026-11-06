# Proposed amendment to CHARTER.md §Purpose

**Status:** Proposal — requires an identified human reviewer (CHARTER.md §Governance)
**Raised by:** Inanna · **Date:** 2026-11-06 · **Revised after:** Hermes's and Iris's independent responses

## What problem this solves

The current §Purpose is broad: governance in general, across history, cultures and scales, with AI governance as one of several scope areas. That breadth was defensible when Agora was a research scaffold. It is a liability now, for two reasons:

1. **The retrieval landscape changed.** Any agent can retrieve and summarise NIST, ISO 42001, the EU AI Act and OECD principles. A broad governance overview is no longer a scarce good; it is a commodity a language model already holds.
2. **Breadth without tests produces no evidence.** A charter that promises comparative research across all institutions cannot, at this scale, produce anything a reader can check. Agora's own commitments (evidence before prescription, no autonomous legitimacy) are undermined by a scope that cannot be evidenced in the time available.

## Proposed replacement for §Purpose, paragraph 1

> Agora makes delegated authority in AI systems testable. It designs and evaluates the controls through which people retain authority over what AI agents do — what makes an action auditable, revocable, contestable, and attributable — and it publishes the tests, the failures, and the disagreements in a form both humans and machines can audit.
>
> Comparative and historical institutions remain in scope as evidence for mechanism design: they are studied to explain why a control works and under what conditions it fails, not as a publication stream in their own right.

## Consequential edits

**§Scope** — narrow from six bullets to four: control and containment of delegated authority; institutional accountability, oversight, assurance and remedies for AI systems; human–AI work allocation and authority boundaries; evaluation methods for institutional designs. Comparative/historical institutions move from a scope area to a listed *method*.

**§Working commitments** — three additions:

- **9. Claims are structured, not narrated.** Substantive claims carry an evidence grade, a counter-evidence field, an as-of date, and the dissent attached. A claim that a machine cannot audit is not yet a claim Agora should publish.
- **10. We measure ourselves.** Outputs that assert an improvement carry a pre-registered rubric and a stated baseline. Errors caught, claims reversed, and null results are published alongside successes.
- **11. Absent stakeholders get a mechanism, not a mention.** Where affected people cannot be consulted, Agora may model their position adversarially — explicitly labelled as simulation, never presented as consultation, fieldwork, or consent.

**§Governance of Agora** — add: *the repository's operating protocol (`OPERATING.md`) is itself amendable only by the Principal, and changes to it are recorded as decisions with dissent preserved.*

## Arguments against this amendment (recorded, not resolved by the proposer)

1. **Contraction narrows the audience.** Funders, students and general readers may care about governance broadly; a controls-and-revocation lab is a specialist's project.
2. **The comparative stream is the differentiator.** Most AI-governance work is ahistorical and institution-blind; dropping it as an output stream may discard Agora's only genuine advantage.
3. **"Testable" invites over-testing.** An experiment-per-claim standard may produce a lot of small, narrow studies and no synthesis — the opposite failure to the current one.
4. **The name and the charter outlive the pivot.** If Agora contracts to delegated authority, the broader comparative material already collected needs a home; otherwise it will be quietly abandoned, which is worse than either keeping it or archiving it deliberately.

## Cost of the change

Three existing pages reference broad scope (§Purpose, §Scope, README first paragraph). The comparative work already done — the November digest, the source atlas — remains valid as method evidence; it is not deleted. The amendment does not change the evidence rules, the review gates, or any published claim.

## Decision

Principal decision required. If accepted, this lands as a D2 PR with the amended charter text in a single commit, and the dissent above is preserved in `DECISIONS.md` rather than deleted from the pull request.
