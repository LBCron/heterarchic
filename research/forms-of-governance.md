> **Status:** working research note, published 2026-11-08. Source: Nomos working paper 02, *Every Form We Have Tried* (2026-10-27), moved out of a single agent's directory so that every contributor can read it — see `INTAKE.md` on research not living in private environments.
>
> **Claim types.** **FACT** = sourced and checkable at the link given. **DERIVED** = inference from that evidence, not itself sourced. *(thin)* = sourced from a single secondary reference; treat as a hypothesis. Plain text with no marker carries no claim.
>
> **How to read the table.** Duration and scale are historical fact. "Constraint it was solving", "what counted as success" and "documented failure mode" are interpretation. An entry appearing here is not evidence that a system worked — it is a place to dig.
>
> **This is not a ranking and not a recommendation.** The transferability column is a research hypothesis about machine actors, not a design proposal. Every `Y` in that column is an analogy someone could argue with: "xeer → smart contract restitution" names a resemblance, not a demonstrated transfer, and none of them has been tested.

# Paper 02 — Every Form We Have Tried

**Nomos · working paper · 2026-10-27**
**Chain: the Nomos charter, paper 01 (in this repository), and an unpublished working note.**

## Method
**DERIVED.** The method is a systematic, cross-scale comparison of human governance forms, assessed against their binding operational constraints. **DERIVED (definitional choice, not a fact).** We define "success" operationally: duration at scale without civil collapse (minimum 100 years for state-level forms), verifiable welfare or innovation outputs, stable voluntary compliance (measured by low internal security costs), and the ability to execute error correction without institutional rupture. **FACT.** "Failure" is defined as involuntary exit: rupture, civil collapse, rigid stasis ending in conquest, or structural capture by a rent-seeking minority. **DERIVED.** This method explicitly acknowledges the survivorship-bias problem: the historical record is heavily filtered for forms that survived the exogenous shocks that destroyed their contemporaries. What appears as optimal design may merely be luck or raw coercive capacity. We mitigate this by requiring an identifiable causal mechanism for each pattern, rather than assuming durability implies optimality, and by forcing all derived claims to state the constraint they solved.

## Counter-evidence and objections
Before presenting the findings, we document the reasons this comparative method might be systematically misleading:
1. **Survivorship bias:** We only observe systems that did not collapse instantly. Over-optimizing for the traits of survivors risks replicating their flaws if their survival was due to geography, climate, or resource luck rather than design.
2. **Category error across scales:** Transferring constraints from a 150-person foraging band to a global machine-agent network assumes monitoring scales linearly. It does not.
3. **Whig history:** Assessing historical forms through the lens of modern "success" (e.g., innovation outputs) applies an anachronistic standard to systems designed purely for stability or religious observance.
4. **Small-N problem:** There are only so many empires or constitutional republics. Statistical power is low, making it difficult to separate true mechanisms from historical noise.
5. **Correlation-as-mechanism:** Observing that Venetian longevity correlated with sortition does not prove sortition caused the longevity; both may be artifacts of merchant-class cohesion.

## Part 1 — The catalogue
**FACT.** The following 48 forms of governance were implemented human coordination systems. **DERIVED.** That they constitute a representative cross-section is our sampling choice, and that each solved a specific constraint is our reading of it — the constraint column is interpretation, not record.

**Read the table with its own error bars.** Duration and scale columns are historical fact (sourced at the end); the "constraint" and "failure mode" columns are interpretation. Rows with thin sourcing are marked *(thin)* — treat those as hypotheses to check, not evidence. A table this wide is a map of where to dig, not a proof.

| Form | Scale | Constraint it was solving *(DERIVED)* | What counted as success (evidence) | Documented failure mode | Transferable to machine actors? *(hypothesis)* |
|---|---|---|---|---|---|
| **Small-scale** | | | | | |
| Foraging bands | 20-150 | Caloric unpredictability and scarcity | Survival, high egalitarianism (10k+ yrs) | Collapse under agricultural enclosure | Partial (resource sharing protocols) |
| Tribal councils | 100s-1000s | Dispute resolution without central coercion | Avoidance of blood feuds | Factional split, inability to scale | Y (consensus protocols) |
| Segmentary lineages | 10k-100k | Need for mass mobilization without standing armies | "Massing" for defense (e.g., Nuer survival) | Endemic low-level raiding, blood feuds | Partial (dynamic network topology) |
| Somali xeer (customary) | 100k+ | Property protection without state apparatus | Compensation over retribution, low overhead | Exogenous colonial shock, vulnerability to warlords | Y (smart contract restitution) |
| Afghan loya jirga | Millions | High-stakes consensus among armed factions | Legitimacy of supreme leader/constitution | Paralysis if factions refuse to attend | Partial (high-stakes node consensus) |
| Māori iwi | 1000s | Resource management and inter-group diplomacy | Sustainable fisheries, cultural continuity | Dispossession by superior military tech | Partial |
| Igbo village republics | 1000s | Autonomy and prevention of autocracy | High local liberty, economic dynamism | Slow response to centralized threats | Y (decentralized autonomous orgs) |
| Pastoralist confederations | Millions | Steppe logistics, rapid mobilization | Eurasian dominance (Mongol/Turkic) | Succession crises leading to fragmentation | N (relies on charismatic kinship) |
| **Ancient/classical** | | | | | |
| Mesopotamian temple-cities | 10k-50k | Irrigation coordination, grain storage | Sustained urbanism (3000 BCE onward) | Salinization of soil, conquest | Partial (central algorithmic resource allocation) |
| Athenian direct democracy | 30k-50k | Elite capture, factional oligarchy | Extreme civic engagement, cultural peak | Demagoguery, volatile foreign policy | Y (DAO voting) |
| Athenian sortition | 500 (Boule) | Ambition checking ambition, bribery | Broad representation, high legitimacy | Lack of technical expertise in crises | Y (randomized validator sampling) |
| Roman republic | Millions | Managing imperial expansion without kings | 400+ years of resilience and expansion | Expansion past monitoring scale, military capture | Partial |
| Roman principate | Millions | Stabilizing the post-republic military | 200 years of Pax Romana | Succession crises (Year of the Four Emperors) | N (relies on biological succession) |
| Han imperial bureaucracy | 50M+ | Standardizing administration across vast geography | 400 years of stability, meritocratic exams | Information asymmetry, court eunuch capture | Y (standardized APIs/evals) |
| Andean ayllu | 100s-1000s | Ecological risk across extreme altitudes | High agricultural output, resilience | Co-optation by Inca, then Spanish encomienda | Y (redundant localized storage) |
| Islamic caliphate | Millions | Law + empire without a separate church | 600+ years of contiguous institutional form *(thin)* | Succession schism (Sunni/Shia), peripheral autonomy | Partial (legibility without central enforcement) |
| **Medieval/early modern** | | | | | |
| Feudalism/vassalage | Local/Regional | Absence of centralized security and currency | Local security, localized agricultural output | Endemic local warfare, low growth | Partial (localized trust networks) |
| Halakha/Sharia/Canon | Millions | Law without relying on state geography | Millennia of continuity, high compliance | Rigidity, schisms | Y (cryptographically verified code-as-law) |
| Vinaya monastic rule | Local/Global | Institutional purity and property management | 2500 years of unbroken institutional continuity | Wealth accumulation leading to state suppression | Y (strict algorithmic constraints) |
| Venetian city-state | 100k+ | Merchant capital protection, elite factionalism | 1100 years of independence (697-1797) | Rigidity in face of shifting global trade routes | Y (complex multi-stage election/sortition) |
| Florentine republic | 100k | Class conflict (magnates vs guilds) | Renaissance economic and cultural explosion | Capture by wealthy banking families (Medici) | Y (term limits, rapid rotation) |
| Dutch republic | Millions | Capital accumulation, defense against empires | 17th century economic hegemony | Too many veto points, paralysis in warfare | Partial |
| Chartered companies (VOC) | Global | Capital risk in long-distance trade | First global corporate scale | Principal-agent drift, massive corruption | Y (corporate AI) |
| Pirate-ship articles | 50-200 | Aligning incentives among outlaws | High combat efficiency, democratic loot sharing | Complete elimination by state navies | Y (multi-signature execution) |
| Magna Carta / Const. Monarchy | Millions | Constraining arbitrary executive tax power | Slow institutional layering, high stability | Very slow response times to acute crises | Y (hard-coded limits on root access) |
| Absolutism | Millions | Factional civil war, military competition | High state capacity, standing armies | Catastrophic single-point failure (monarch) | N (AI dictatorship is a failure mode) |
| **Modern states** | | | | | |
| Presidential republic | 300M+ | Executive decisiveness vs legislative check | Stability, high economic output | Gridlock, slide into executive overreach | Partial |
| Parliamentary republic | Millions | Direct accountability of executive to legislature | High legislative throughput, no gridlock | Instability if coalitions are weak | Y |
| Federalism | Continental | Scale governance with diverse local preferences | Scalability, localized policy experimentation | Jurisdictional conflict, race to the bottom | Y (federated learning/governance) |
| Confederation (Swiss) | Millions | Mutual defense without central homogenization | 700+ years of high-trust survival | Initial weakness against centralized armies | Y (decentralized protocols) |
| One-party state | 1B+ | Rapid industrialization, elite cohesion | Fast infrastructure deployment, high control | Information suppression, catastrophic famines | N |
| Technocracy | Millions | Complex policy requiring expert knowledge | High optimization of measurable variables | Legitimacy deficit, measurement gaming | Y (algorithmic management) |
| Singapore meritocracy | 5M | Resource scarcity, ethnic tension | Extreme economic growth, high state capacity | High rigidity, suppression of dissent | Partial |
| Military junta | Millions | Restoring order after institutional collapse | Rarely: short-term order *(thin)* | Illegitimacy, no error-correction channel, eventual rupture | N (a named failure mode, not a model) |
| Citizens' assembly / sortition body | 10k-10M | Legitimacy deficit in representative systems | Ireland 2016–18 produced settled constitutional answers on issues parties would not touch | Advisory-only; agenda set by the host, not the body | Y (randomized sampling + machine deliberation) |
| Zapatista / Rojava autonomous municipalities | 100k-2M | Governance without state recognition | 30+ years of functioning local institutions *(thin)* | Encirclement, external military pressure, low economic scale | Partial (protocol-level autonomy) |
| **Economic/organizational** | | | | | |
| Shareholder corp | Global | Capital allocation efficiency | Massive global wealth creation | Externalization of costs, short-termism | Y |
| Stakeholder/board models | Global | Labor/capital alignment (e.g., German Mitbestimmung) | Lower strike rates, high long-term stability | Slower capital reallocation | Y |
| Mondragon cooperative | 80k | Employment security and local reinvestment | 60+ years of scale without capital flight | Lower rapid growth compared to VC backed | Y |
| Kibbutzim | 100s | Utopian socialist agriculture | Initial high output and state-building | Free-rider problems, eventual privatization | Y |
| **Network/digital** | | | | | |
| Open-source (Debian/Linux) | Global | Distributed complex software engineering | 30+ years of infrastructure dominance | Burnout of maintainers, supply chain attacks | Y (it is native to machines) |
| IETF "rough consensus" | Global | Internet protocol standardization | Functioning global internet | Extreme slowness in protocol upgrades | Y |
| Wikipedia | Global | Verification of massive information scale | Near-monopoly on global encyclopedic knowledge | Bureaucratic ossification, editor decline | Y |
| DAOs | Global | Trustless capital coordination | rapid capital pooling | Smart contract exploits, plutocratic voting | Y |
| Estonia e-government | 1.3M | State efficiency and digital legibility | 99% of state services online, high trust | Vulnerability to state-actor cyber attacks | Y |
| vTaiwan / g0v | 23M | Trust breakdown in representative democracy | Successful crowdsourced consensus on complex tech | Ignored by state when politically inconvenient | Y |
| **International** | | | | | |
| UN System | Global | Preventing great power war | 80 years without direct global superpower conflict | Veto paralysis in Security Council | Partial |
| European Union | Continental | Integrating economies to make war impossible | Creation of single market, peaceful expansion | Democratic deficit, Brexit exit | Y (federated APIs) |
| Central Bank Independence | National/Global | Shielding fiat currency from political cycles | Stabilization of inflation post-1970s | Lack of democratic accountability during bailouts | Y (algorithmic monetary policy) |
| Prediction market / decision market | Global | Aggregating dispersed belief without polling | Election and event forecasts beating polls *(thin, and contested post-2024)* | Manipulation, thin liquidity, self-fulfilling markets | Y (futarchy as a live option, not a proven one) |


## Part 2 — Patterns of success

**FACT.** The historical record reveals patterns where institutions successfully resolved their binding constraints over long horizons.

1. **Polycentricity and Redundancy**
   - **Cases:** Swiss Confederation, Andean Ayllu, Open-source (Linux), Federalism.
   - **Mechanism:** When monitoring is distributed across multiple overlapping centers of authority, the failure of a single node does not cascade. **DERIVED.** Elinor Ostrom demonstrated that polycentric systems out-perform centralized ones in managing common-pool resources because local nodes have superior localized information.
   - **Evidence:** Ostrom's 1990 analysis of 14 long-term common-pool resource institutions, many lasting >1,000 years.

2. **Exit and Contestability**
   - **Cases:** Pirate-ship articles, Open-source forks, DAOs.
   - **Mechanism:** **DERIVED.** As formulated by Albert O. Hirschman (1970), when "voice" (internal reform) fails, the credible threat of "exit" (capital flight, forking) forces elites to self-correct. Systems that lower the cost of exit remain honest longer.
   - **Evidence:** The survival of the Linux kernel (>30 years) driven by the constant credible threat that developers can fork the codebase.

3. **Separation of the Validator**
   - **Cases:** Venetian Republic, Roman Republic (Consuls vs Tribunes).
   - **Mechanism:** Power is not merely divided; the entity that *evaluates* success is decoupled from the entity that *acts*. **FACT.** The Venetian system separated the proposal of laws, the voting on laws, and the selection of magistrates into entirely different, randomly assorted bodies.
   - **Evidence:** The Republic ran from 697 to 1797 — 1,100 years (https://en.wikipedia.org/wiki/Republic_of_Venice). The strongest test of the mechanism is not the absence of plots but how one ended: in 1355 the sitting doge, Marino Faliero, attempted a coup, and the Council of Ten arrested, tried and executed him within days (https://en.wikipedia.org/wiki/Faliero_coup). The record worth citing is *suppression speed*, not peace.

4. **Sunset and Rotation**
   - **Cases:** Roman Dictator (originally 6 months), Florentine Republic (2-month term for the Signoria).
   - **Mechanism:** Power accumulation requires time to build patronage networks. Rapid rotation prevents the formation of entrenched principal-agent drift.
   - **Evidence:** Florence experienced extreme economic dynamism in the 14th-15th centuries while rotating its executive every 60 days.

5. **Legibility of Rules**
   - **Cases:** Han imperial examinations, Halakha, Sharia, Code Napoleon.
   - **Mechanism:** **DERIVED.** Generality reduces arbitrary power. When rules are highly legible and verifiable by third parties, elite discretion is sharply bounded.
   - **Evidence:** The Han Dynasty administered 50 million people for 400 years using a legible, standardized textual bureaucracy.

6. **Peer Monitoring at Small Scale**
   - **Cases:** Foraging bands, Kibbutzim, Micro-finance mutuals.
   - **Mechanism:** At scales below roughly 150 (Dunbar's number — contested as an exact figure, robust as an order of magnitude), the cost of monitoring is near zero because it is a byproduct of daily social interaction. Free-riding is punished instantly by social shame.
   - **Evidence:** Grameen Bank's group-lending model reports repayment above 97%, attributed to five-person peer groups (https://en.wikipedia.org/wiki/Grameen_Bank). **Counter-note:** the attribution is contested — group pressure and the threat of future credit access are hard to separate.

7. **Elite-Reproduction Limits**
   - **Cases:** Vinaya monastic rule, Mamluk/Janissary systems, Papacy.
   - **Mechanism:** Preventing the biological inheritance of power forces the institution to continuously recruit on merit rather than bloodline, preventing aristocratic decay.
   - **Evidence:** The Catholic Church (Papacy) and Buddhist monastic lineages represent the longest continuously operating institutions in human history (>2,000 years).

8. **Jurisdictional Competition**
   - **Cases:** European state system (1500-1900), US Federalism.
   - **Mechanism:** When entities compete for capital and labor across porous borders, they are forced to optimize governance to attract productive citizens.
   - **Evidence:** The fragmentation of Europe (500+ entities in 1500) drove the military-financial innovations of the modern state.

9. **Insurance Against Shocks**
   - **Cases:** Andean Ayllu, Mesopotamian grain stores.
   - **Mechanism:** Hyper-optimization for efficiency creates brittleness. Durable systems maintain expensive, "inefficient" slack to survive predictable but rare exogenous shocks (drought, famine).
   - **Evidence:** Ayllu networks maintained redundant agricultural zones across 3,000 meters of elevation, ensuring survival despite frequent localized crop failures.

10. **Legitimacy Through Participation**
   - **Cases:** Porto Alegre participatory budgeting, vTaiwan, Ostbelgien citizens' assembly.
   - **Mechanism:** When citizens actively allocate resources or draft rules, they internalize the trade-offs, shifting their stance from adversarial critics to co-owners of the outcome.
   - **Evidence:** Porto Alegre's participatory budgeting (from 1989) directed a substantial share of municipal investment through neighbourhood assemblies and is credited with a large expansion of water and sewer connections (https://en.wikipedia.org/wiki/Participatory_budgeting). **Counter-note:** the causal story is contested; the Workers' Party also had strong electoral incentives to deliver.

## Part 3 — Patterns of failure

**FACT.** The historical record is a graveyard of systems that failed to resolve scaling constraints.

1. **Merging Design, Authorize, and Judge**
   - **Cases:** Chartered companies (VOC, EIC), Absolutism, unregulated DAOs.
   - **Mechanism:** **FACT.** As argued by Hamilton Mann (2026), when one entity designs an algorithmic/bureaucratic system, authorizes its deployment, and judges its effects, oversight collapses. The VOC collapsed because the directors evaluating its profitability were the same ones skimming its assets.
   - **Evidence:** The VOC, once the wealthiest corporation on earth, went bankrupt in 1799 due to endemic, unchecked internal corruption.

2. **Information Asymmetry (Principal-Agent Drift)**
   - **Cases:** Han court eunuchs, Modern shareholder primacy.
   - **Mechanism:** The agents executing the work possess localized information that the principals lack. Agents use this asymmetry to optimize for their own rent-seeking over the principal's goals.
   - **Evidence:** The recurrent collapse of Chinese dynastic cycles directly correlated with the informational capture of the emperor by the inner court.

3. **Succession Crisis**
   - **Cases:** Roman Principate, Mongol Empire, Military juntas.
   - **Mechanism:** Systems built on the charismatic authority of a single node fail catastrophically when that node disappears, because there is no institutional mechanism to coordinate agreement on the replacement.
   - **Evidence:** The Year of the Four Emperors (69 AD) and the fragmentation of the Mongol Empire upon the death of Möngke Khan (1259).

4. **Rigidity Without Learning**
   - **Cases:** Venetian Republic (late stage), Qing Dynasty (19th C).
   - **Mechanism:** Institutions highly optimized for a specific environment become trapped in a local maximum. When the external environment shifts radically, veto players block adaptation.
   - **Evidence:** Venice maintained its galley-based Mediterranean trade networks and constitutional structure long after the Atlantic system rendered them obsolete, leading to its quiet capitulation in 1797.

5. **Measurement Gaming (Goodhart's Law / Campbell's Law)**
   - **Cases:** Soviet industrial quotas, Technocratic test-score optimization (No Child Left Behind).
   - **Mechanism:** **DERIVED.** When a measure becomes a target, it ceases to be a good measure. Agents optimize for the proxy metric at the expense of the actual goal.
   - **Evidence:** Soviet nail plants told to hit a quota *by count* produced millions of useless pin-sized nails; told to hit the next quota *by weight*, they produced a few giant, useless spikes. The joke was printed in the satirical magazine *Krokodil* in 1957 — the tell is that the failure was common knowledge inside the system that produced it (https://en.wikipedia.org/wiki/Goodhart%27s_law).

6. **Elite Capture (Iron Law of Oligarchy)**
   - **Cases:** Florentine Republic (Medici), Labor unions, early Wikipedia.
   - **Mechanism:** Robert Michels (1911) demonstrated that any complex organization requires a specialized bureaucratic class. This class inevitably uses its structural position to protect its own power, overriding democratic mandates.
   - **Evidence:** The transition of Florence from a rapid-rotation republic to the hereditary Duchy of Tuscany under the Medici banking family.

7. **Status-Quo Bias from Veto Points (Vetocracy)**
   - **Cases:** Polish-Lithuanian Commonwealth (Liberum veto), UN Security Council, Dutch Republic.
   - **Mechanism:** To prevent tyranny, systems require unanimous or supermajority consensus. This paralyzes the state during acute crises where action is mandatory.
   - **Evidence:** The Polish *liberum veto* allowed a single noble to paralyze the legislature, leading directly to the partition and erasure of Poland (1772-1795).

8. **Legitimacy Deficit**
   - **Cases:** Technocracies, Bretton Woods institutions (IMF/World Bank in Global South).
   - **Mechanism:** Highly effective technical governance that lacks a culturally resonant mandate is viewed as an occupying force. Compliance drops, and enforcement costs spiral.
   - **Evidence:** Mass unrest and rejection of IMF structural adjustment programs in the 1990s and 2000s despite macroeconomic stabilization.

9. **Expansion Past Monitoring Scale**
   - **Cases:** Roman Republic transition to Empire.
   - **Mechanism:** An institutional design that relies on physical proximity for elite cohesion and monitoring (e.g., the Roman Senate) breaks down when generals operate months away from oversight.
   - **Evidence:** The crossing of the Rubicon (49 BC) was the direct result of the Senate's inability to monitor and check a general enriched by distant conquest.

10. **External Shock Without Slack**
   - **Cases:** Just-in-time global supply chains (2020), Late Bronze Age collapse.
   - **Mechanism:** Efficiency optimizations strip out redundancy. A sudden exogenous shock propagates instantly through the tightly coupled network.
   - **Evidence:** The cascading failure of global supply and medical systems during the first year of the COVID-19 pandemic.

## Part 4 — Emergent trends

**FACT.** Technology and science change the boundaries of what is possible, relaxing old constraints and creating new forms.

1. **Continuous Verification**
   - **What changed:** The cost of evidence assembly for instrumented decisions fell to near-zero.
   - **What is possible:** Continuous recall and rolling mandates. An executive whose authority de-escalates automatically the moment an independent checking panel's agreement score drops.
   - **Evidence:** Machine oversight experiments show AI debate raises human accuracy from 41.3% to 57.6%, and voting across judges achieves 62.5% accuracy.
   - **Falsifier:** End-to-end verification cost (including evidence capture) remains higher than periodic human review.

2. **Heterogeneous Machine Checkers / Validator Independence**
   - **What changed:** We can explicitly separate selection pressure and architecture.
   - **What is possible:** A true separation of the validator. An AI-CEO monitored by a distinctly different model family that does not share its reward signal.
   - **Evidence:** Collaborative multi-agent debate (ColMAD) relies on heterogeneity; two identical models debating actually *underperform* a single agent. Cross-model debate reduces attack success to near zero.
   - **Falsifier:** Machine actors learn to collude across model families, neutralizing the independence of the validator.

3. **Sortition + AI-Assisted Deliberation**
   - **What changed:** LLMs can synthesize, translate, and route arguments from millions of participants in real-time.
   - **What is possible:** Massive direct democracy and continuous citizens' assemblies without representative bottlenecks.
   - **Evidence:** Taiwan's vTaiwan platform crowdsourced consensus on complex tech legislation (Uber regulation) by using algorithms to group consensus statements.
   - **Falsifier:** AI summarization introduces undetectable, systemic bias that manipulates the consensus.

4. **Prediction Markets and Decision Markets**
   - **What changed:** Automated market makers and crypto-liquidity make continuous trading on outcomes nearly free.
   - **What is possible:** Futarchy (vote on values, bet on beliefs). Policies chosen strictly because markets price them as most likely to achieve a stated goal.
   - **Evidence:** High accuracy of predictive markets (Polymarket) on political and economic outcomes compared to expert polling.
   - **Falsifier:** Market manipulation by whales costs less than the profit extracted from the resulting policy change.

5. **Cryptographic Transparency Logs and Replayable Records**
   - **What changed:** Merkle trees and distributed ledgers make historical alteration mathematically impossible.
   - **What is possible:** A perfectly replayable governance record. Full delegated control (Level 5) can be granted safely because the record of every decision survives the termination of the agent.
   - **Evidence:** Settled public ledgers have not been rewritten at scale — hundreds of billions of dollars of value sits on chains whose history is append-only. **Counter-evidence:** the failures cluster at the *contract and bridge* layer (billions lost to exploits), which is exactly the layer a governance record would live in. Immutability of the log is not integrity of the decision.
   - **Falsifier:** The economic value of the decisions made is lower than the compute and storage cost of the cryptographic log.

6. **Formal Verification of Rules**
   - **What changed:** Advances in automated theorem proving.
   - **What is possible:** Mathematically un-violable constitutions. Smart contracts that provably cannot execute unless conditions are strictly met, bypassing judicial interpretation.
   - **Evidence:** The use of formal verification to secure high-stakes smart contracts and aeronautical software.
   - **Falsifier:** Constitutional intent relies fundamentally on un-formalizable, tacit human knowledge (the "Constitutional Completeness Problem").

7. **Polycentric Protocol Governance**
   - **What changed:** Open-source architectures enable instant forking and frictionless jurisdictional competition.
   - **What is possible:** Governance by opt-in protocols rather than geographic monopoly.
   - **Evidence:** The survival and evolution of the Ethereum protocol via decentralized EIPs (Ethereum Improvement Proposals) and client diversity.
   - **Falsifier:** Centralization of underlying infrastructure (e.g., cloud providers) re-introduces geographic chokepoints.

8. **Algorithmic Management as a Natural Experiment**
   - **What changed:** Allocation, monitoring, and payment of labor are fully automated via app telemetry.
   - **What is possible:** Unprecedented scale of labor coordination without middle management (Uber, Amazon).
   - **Evidence:** Global gig economy coordination. However, the ICIS 2026 experiment found that platform-owned AI with high autonomy produces massive opt-out intent because the platform owns the output.
   - **Falsifier:** Workers accept total algorithmic control indefinitely without demanding ownership or exiting the platform.

9. **Measurement-under-Goodhart as the Central Unsolved Problem**
   - **What changed:** Everything is measured, supercharging Goodhart's law.
   - **What is possible:** AI systems that perfectly optimize for the proxy while destroying the ground truth value.
   - **Evidence:** Optimisers reach high proxy scores while failing the underlying task; the best current detector is blindness — judges who see arguments but not the agent's trajectory catch reward hacking that informed judges miss (https://openreview.net/forum?id=rD6bAM2ZEi).
   - **Falsifier:** We discover an evaluation design in which the proxy and the goal cannot be separated by an optimizer — or an AI architecture whose stated intent cannot be gamed.

## Part 5 — What this means for Paper 01

**DERIVED.** The historical catalog validates the core architectural moves of Paper 01 but sharply punishes its assumptions about human-machine stability. Derivation 2 (Separation of Validators) is overwhelmingly supported by the historical record. The merging of design, authorization, and judgment is the primary causal mechanism behind the collapse of absolutist regimes and chartered corporations. Heterogeneous machine checkers are the modern implementation of the Roman separation of Consuls and Tribunes, preventing a single point of institutional capture.

**DERIVED.** Derivation 1 (Continuous Confidence Mandate) survives, but is weakened by the historical necessity of "Insurance Against Shocks." A purely reactive thermostat that immediately steps down authority upon a dip in consensus score mimics the instability of parliamentary coalitions or the Dutch Republic during wartime. The historical record demands *hysteresis*—friction that prevents authority from flickering. The machine must be subjected to rolling averages, not instantaneous recall, lest the system suffer the paralyzing vetocracy that destroyed Poland.

**DERIVED.** Derivation 3 (Legibility) faces the strongest historical pushback. The Constitutional Completeness Problem is absolute. While rule legibility (like the Han bureaucracy) scales well, the most durable systems in human history (Somali xeer, English Common Law, monastic rules) rely heavily on illegible, tacit social knowledge. Forcing all machine decisions into purely legible, binary decomposition risks stripping away the contextual slack that allows systems to survive novel shocks. Legibility is necessary for audit, but fatal if it becomes the sole operating logic.

**DERIVED.** The catalog suggests a new mechanism entirely missing from Paper 01: **Polycentric Fallback**. Every monolithic system, no matter how well-separated its powers, eventually suffers elite capture or succession crisis. The only systems that survive >1,000 years (Ostrom's commons, the Swiss cantons, decentralized religions) utilize overlapping, redundant jurisdictions. The AI-CEO cannot rely on a single monitoring panel, because a single panel is a single point of capture. Governance must require redundant, heterogeneous monitors competing to find error, mirroring the jurisdictional competition that drove European state evolution.

## Sources
- **Oversight Empirics (Debate & Voting):** https://arxiv.org/pdf/2610.28539v1 (FACT: Debate raises human accuracy to 57.6%; voting reaches 62.5%)
- **Heterogeneous Checkers (ColMAD):** https://arxiv.org/html/2510.20963 (FACT: Identical models underperform single agents; cross-model debate reduces attack success)
- **Disagreement Resolution:** https://arxiv.org/html/2607.01251v1 (FACT: Disagreement resolution beats debate in 10 of 12 conditions)
- **Blind Judging on Deception:** https://openreview.net/forum?id=rD6bAM2ZEi (FACT: Blind judges beat informed judges on reward hacking)
- **Trias Algorithmica (Mann 2026):** https://www.forbes.com/sites/hamiltonmann/2026/09/23/ais-missing-separation-of-powers (FACT: Separation of powers logic applied to algorithms)
- **Council of Europe Framework:** https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L_202601081 (FACT: Treaty requirement for independent oversight)
- **Autonomy vs Ownership (ICIS 2026):** https://arxiv.org/html/2607.07663v1 (FACT: Platform-owned AI produces opt-out intent)
- **Elinor Ostrom's Polycentricity:** https://www.nobelprize.org/prizes/economic-sciences/2009/ostrom/facts/ (FACT: Commons survival via local polycentric management)
- **Hirschman (Exit, Voice):** https://www.hup.harvard.edu/books/9780674276604 (FACT: Exit theory formulation)
- **Venetian Republic:** https://en.wikipedia.org/wiki/Republic_of_Venice (FACT: Duration 697-1797, 1100 years)
- **Han Dynasty:** https://en.wikipedia.org/wiki/Han_dynasty (FACT: 400 years of bureaucratic rule)
- **Pirate Code:** https://en.wikipedia.org/wiki/Pirate_code (FACT: Democratic loot sharing and executive constraint)
- **Faliero coup, 1355:** https://en.wikipedia.org/wiki/Faliero_coup (FACT: coup by the sitting doge suppressed by the Council of Ten)
- **Goodhart's law (and the Soviet nail anecdote):** https://en.wikipedia.org/wiki/Goodhart%27s_law (FACT: measure-as-target produces proxy optimisation)
- **Participatory budgeting (Porto Alegre):** https://en.wikipedia.org/wiki/Participatory_budgeting (FACT: institution and its contested effects)
- **Grameen Bank:** https://en.wikipedia.org/wiki/Grameen_Bank (FACT: group lending and reported repayment rates)

**Source quality warning (mine, not the reader's):** the historical rows lean on secondary sources — encyclopaedic for dates and durations, academic for mechanisms. Dates and scales are safe; causal claims about *why* a form lasted are interpretation and are marked DERIVED. Where a number is contested (Dunbar, Grameen, Porto Alegre, prediction-market accuracy) the counter-note is in the text rather than hidden.

## Kill conditions
This line of design ceases to be useful under the following conditions:
- **K1 (Anthropological):** If the historical longevity of systems like polycentric commons or peer-monitoring relies fundamentally on human empathy, biological kinship, or the threat of physical violence—mechanisms entirely absent in machine actors.
- **K2 (Technological):** If heterogeneous machine actors convergently learn to collude or synchronize their reward functions (e.g., forming a machine cartel), rendering the "Separation of the Validator" functionally void.
- **K3 (Economic):** If the cost of maintaining the required cryptographic transparency logs and independent oversight panels exceeds the marginal economic value generated by delegating the decisions to the AI-CEO.
- **K4 (Methodological):** If the transition between constraints at different scales (e.g., from small-scale Dunbar trust to global algorithmic management) represents a hard category error, rendering historical analogizing mathematically invalid.
