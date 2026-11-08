> **Provenance:** imported 2026-11-08 from the Nomos research bank (started 2026-08-24). Content unchanged apart from the adjustments listed in PR #57. Claim labels are the author's own (FACT / DERIVED / SPECULATION).
>
> Definitions the catalogue relies on. One internal wiki link flattened to plain text.

# Governance Fundamentals — what governance IS and what it universally needs

> **Status:** Active · **Started:** 2026-08-24 · **Goal:** the anchor entry. Before any theory of *who* governs (collectives, markets, algorithms), establish what governance is and what any governance system needs — then everything else in this area is a variation on these needs.

## What governance is

- **Governance ≠ management.** Management executes within rules; governance sets the rules, allocates decision rights, and holds power accountable. (ANALYSIS, standard distinction in corporate governance literature.)
- **Working definition:** governance is the system by which a group makes binding decisions, distributes authority, and answers the question "who decides, and who answers for it?" (ANALYSIS.)
- **The universal trigger:** whenever people pool resources or coordinate on a common fate, they need governance — the alternative is exit, force, or collapse (FACT: Hirschman, *Exit, Voice, and Loyalty*, 1970 — members of any organization have three responses to decline: exit, voice, or loyalty).
- **The original problem:** separation of ownership/decision from execution creates agency costs — the principal-agent problem (FACT: Jensen & Meckling, 1976, "Theory of the Firm"; Berle & Means, *The Modern Corporation and Private Property*, 1932). Governance is the machine built to control those costs.

## What governance universally needs (the checklist)

Synthesized from Ostrom's commons research, democratic theory, and agency theory (each tagged below):

1. **Decision rights** — someone/something must have clear authority to decide; ambiguity is the seed of conflict. (ANALYSIS; see Ostrom's "clear boundaries" principle below.)
2. **Legitimacy** — members must accept the system as the right way to decide, or it decays into coercion. Weber's three legitimacy types: traditional, charismatic, legal-rational (FACT: Weber, *Economy and Society*, 1922). Modern systems lean legal-rational: procedure + consent.
3. **Accountability** — decision-makers answer for outcomes; principals must be able to reward/replace agents (FACT: principal-agent theory, Jensen & Meckling 1976). Without it: the Iron Law of Oligarchy — organizations tend toward rule by a few (FACT: Michels, *Political Parties*, 1911).
4. **Information/transparency** — decisions need good information; members need visibility to hold anyone accountable (FACT: Hirschman 1970 — voice requires information; also the democratic-theory requirement for an informed public).
5. **Enforcement** — rules that can't bind are suggestions; graduated sanctions are a core design principle of durable commons governance (FACT: Ostrom, *Governing the Commons*, 1990, design principle 5: graduated sanctions).
6. **Adaptation / amendment** — a system that can't change its own rules ossifies. Ostrom's principle 3: collective-choice arrangements — those affected by the rules participate in changing them (FACT: Ostrom 1990).
7. **Conflict resolution** — low-cost, internal mechanisms for disputes; principle 6 of Ostrom's design principles (FACT: Ostrom 1990).
8. **Scale logic** — one size doesn't fit: governance must match the group (polycentricity — multiple overlapping centers of authority, Ostrom; subsidiarity in EU law). (FACT: Ostrom, polycentric governance work; both Ostroms.)
9. **Leverage** — participation that cannot impose a cost on being ignored is not governance, it is consultation. Added 2026-10-18; see the sweep section below. (FACT: Verhulst et al., *From Voice to Leverage in Data Governance*, arXiv 2609.05731, 2026-09-04.)

## Ostrom's eight design principles (the empirical gold standard)

From a 30-year global study of durable commons governance (fisheries, irrigation, forests) — the closest thing to a universal governance checklist (FACT: Ostrom, *Governing the Commons*, 1990; Nobel Prize in Economics, 2009):

1. Clear boundaries (who has rights)
2. Congruence between rules and local conditions
3. Collective-choice arrangements (users shape rules)
4. Monitoring (by users or their agents)
5. Graduated sanctions
6. Conflict-resolution mechanisms
7. Minimal recognition of the right to organize
8. Nested enterprises (for larger systems)

## What this means for LLM systems (bridge)

Every one of the eight needs maps to an AI-system design decision — see `llm-governance-application` (a further entry in the same private research bank, not published). The short version: **a constitution (rules + amendment rights) is the seat of power; audit trails are accountability; revocation is enforcement; radical legibility is information.** (ANALYSIS.)

## 2026-10-18 sweep: the ninth need — leverage (voice without a cost for ignoring it is decoration)

- **"From Voice to Leverage" — participation has converged on voice, and voice is not a mechanism** (FACT — Verhulst, Zable, González Otero & Lu (The GovLab, NYU / University of Toronto School of Cities), *From Voice to Leverage in Data Governance: Building Enforceable Social License for Data Re-Use*, working paper, **arXiv 2609.05731**, 2026-09-04, https://arxiv.org/abs/2609.05731; **flag: working paper, not peer-reviewed; the argument is applied to data re-use but framed generally**). The claim: the field's consensus that "giving affected communities a voice will, on its own, change what data holders do" rests on **an unexamined assumption**. What is missing is **leverage** — "the capacity of individuals and communities to make their participation consequential by **attaching credible legal, institutional, contractual, economic, or reputational costs to being ignored**." Leverage is defined by three properties: **counterfactual** (the cost would actually be imposed), **enforceable** (someone can impose it), **durable** (it survives the next election or quarter). Two further claims matter more than the definition: **leverage presupposes epistemic legibility** — "affected publics can rarely impose costs on a system they cannot see, document, or contest" — and **most existing transparency instruments equip regulators and procurers rather than the governed**. The paper then maps **six sources** of leverage (legal/regulatory; institutional decision; contractual; economic; data access; political/reputational) and treats **intermediaries — data trusts, cooperatives, commons, unions, coalitions — not as a seventh source but as the vehicles that aggregate it and make it durable**: "a data cooperative does not itself compel a data holder to do anything; it creates associational power by pooling rights and contributions, reducing coordination costs, representing members, monitoring compliance, financing enforcement, and making collective commitments credible." It draws on labour-relations bargaining theory, the sociology of disputes, and James C. Scott on legibility.
  - ANALYSIS: this is the ninth row of the checklist, and it retro-explains three findings already in this area. (1) Brussels' **duty-to-respond in writing** (2026-09-27) works because refusal carries a *published* reputational cost — that is leverage, not voice. (2) The Lisbon causal study (2026-10-11) found assemblies raise **external** efficacy and trust but not members' **internal** capacity to contest: that is the voice-without-leverage signature — participants learn the body is responsive without acquiring any means to impose a cost on it. (3) The DAO participation ceiling and 709-voters-per-5,024-members empirics (2026-09-27) are a leverage story: a vote that cannot change an outcome is a survey. For any member-facing mechanism we ship, the test is: **name the cost, name who can impose it, name how long it lasts.** "Members can complain and we will consider it" is voice, and on this evidence it will produce trust without power. The companion design rule: transparency artifacts must be built **for members, not for the auditor** — the paper's point that transparency is usually designed to equip regulators is an indictment of most "AI governance dashboards," including ours.

## Key flags / warnings

- Ostrom's principles come from *common-pool resources*, not corporations or states — portability is good but not 1:1.
- "Legitimacy" is culturally loaded; in practice, treat it as "do members accept the procedure as fair?" not "which ideology is right."
- The Iron Law of Oligarchy is a warning about *any* governance system that lacks rotation/accountability — including AI executives.

## Append log

- 2026-08-24: initial entry (Inanna synthesis of classic governance theory).
- 2026-10-18: weekly sweep — added **leverage** as the ninth universal need (GovLab, arXiv 2609.05731, 2026-09-04): participation without a credible, enforceable, durable cost for being ignored is consultation; leverage presupposes epistemic legibility, and most transparency instruments equip regulators rather than the governed. Six sources of leverage + intermediaries as the vehicles that aggregate it. Checklist updated to nine needs; cross-checked against the Brussels duty-to-respond, Lisbon efficacy findings and DAO turnout empirics already in this area.
