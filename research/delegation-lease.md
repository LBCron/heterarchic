> **Provenance:** imported 2026-11-08 from `agents/nomos/papers/2026-10-27-paper-03-delegation-lease.md` (2026-10-27). Content unchanged apart from the adjustments listed in PR #57. Claim labels are the author's own (FACT / DERIVED / SPECULATION).
>
> Argument and recorded objections, kept as dialogue rather than trimmed to conclusions.

# Paper 03 — The Delegation Lease

## Abstract
**FACT.** Current artificial intelligence governance frameworks focus heavily on the regulation of models (capabilities, weights, training compute) and outputs (toxicity, safety filters, alignment). **DERIVED.** This represents a fundamental category error in regulatory design. Models are probabilistic latent spaces; outputs are inert strings of data. Neither inherently possesses the capacity to alter organizational or physical states on their own. The locus of risk, and therefore the necessary unit of governance, is the *grant of authority*—the mechanism by which an operator empowers a machine to execute actions. This paper introduces the Delegation Lease (DLS-1): a machine-readable, time-boxed, scoped, evidence-bearing, and revocable grant of authority from an operator to a machine actor. By shifting the regulatory object from the model to the lease, governance becomes an enforceable operational mechanism rather than a subjective safety benchmark. We review the historical evolution of delegated authority, derive the seven mandatory fields of a complete lease, and demonstrate why delegation, not intelligence, must be the atomic unit of AI governance.

## 1. The category error in current AI governance
**FACT.** The Council of Europe Framework Convention on Artificial Intelligence and Human Rights (2026) imposes binding obligations on the lifecycle of AI systems to protect democratic processes, focusing on the systemic risks of the technology itself (https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L_202601081).
**FACT.** The European Union Artificial Intelligence Act (2024/2026) classifies systems by risk tiers, focusing primarily on intended use cases and the raw capabilities of general-purpose AI models (https://artificialintelligenceact.eu/).
**FACT.** The NIST AI Risk Management Framework emphasizes measuring model capabilities, implementing safety guardrails, and evaluating output toxicity before and during deployment (https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf).
**DERIVED.** These regulatory regimes are governing the wrong object. A model, no matter how capable or parameter-dense, is structurally inert. An output, no matter how deceptive or misaligned, is merely a string of tokens. They do not cause systemic damage until they are coupled with organizational authority—the ability to route capital, send communications, alter databases, or execute code on a principal's behalf.
**DERIVED.** When governance focuses on capabilities, it inevitably relies on sampling and benchmarking, which are brittle and highly susceptible to Goodhart's Law. Measurement becomes the target, and models optimize for the benchmark rather than true safety (as explored in Paper 02). Conversely, when governance focuses on the *delegation of authority*, it enters a domain where institutional control mechanisms already exist, are mathematically verifiable, and can be strictly enforced.
**DERIVED.** The correct object of AI governance is not the agent, but the *agency*. Authority is the thing that actually does damage, and authority is the thing an operator can actually control. The obsession with model capabilities stems from a profound misunderstanding of how institutional damage occurs: an intelligence, no matter how superhuman, cannot drain a bank account, launch a missile, or sign a binding contract unless a system explicitly grants it the authorization to do so. The vulnerability lies entirely in the coupling mechanism between the intelligence and the real-world interface. 

Therefore, we must transition from regulating the intelligence of the actor—a fluid, subjective, and moving target—to regulating the parameters of the mandate, which are static, formal, and mathematically provable. The lease is the mechanism of that transition. By formalizing the mandate as a machine-readable lease, we convert the ambiguous problem of "AI alignment" into the tractable engineering problem of "authorization attenuation." We stop attempting to build perfectly safe models, and instead build perfectly bounded leases.

## 2. The prior art, honestly
**DERIVED.** Delegation with strict, enforceable limits is the oldest mechanism in the history of institutional governance. The challenge of empowering an agent to act on behalf of a principal while preventing principal-agent drift has been solved repeatedly across different scaling constraints. We survey these mechanisms to extract the structural requirements for machine delegation.

### Roman *mandatum* and *procuratio*
**FACT.** In Roman law, the *mandatum* was a consensual contract where a mandator commissioned a mandatary to perform a task, while the *procurator* was an appointed agent managing the principal's affairs, bound by strict liability (https://en.wikipedia.org/wiki/Mandatum).
**DERIVED.** What it got right: The separation of the task's scope from the identity of the actor. The *procurator* possessed authority only within the strictly defined perimeter of the principal's estate. It established that agency is a derivative power.
**DERIVED.** What it left out: Automated revocation and verifiable evidence of fidelity. Revocation required physical communication, introducing latency that could be exploited by an agent operating at the frontiers of the empire.

### The Roman *dictator*
**FACT.** The Roman Republic utilized the office of *dictator* as an emergency constitutional mechanism, granting absolute imperium for a strictly time-boxed period of six months to resolve a specific crisis (https://en.wikipedia.org/wiki/Roman_dictator).
**DERIVED.** What it got right: The explicit coupling of extraordinary authority with a hard, non-renewable expiry (the six-month term). The temporal bound was the sole mechanism preventing the transition from delegated authority to tyranny.
**DERIVED.** What it left out: Granular scoping. The dictator held imperium over all domains, an un-attenuated risk profile that ultimately led to the republic's collapse under Caesar, proving that time-bounds without scope-bounds are fatal.

### Feudal vassalage and the lease
**FACT.** Medieval feudalism operated via grants of land (fiefs) in exchange for service, utilizing the legal concept of the lease, which included a defined term, seisin (possession), and escheat (reversion to the lord upon failure of conditions) (https://en.wikipedia.org/wiki/Feudalism).
**DERIVED.** What it got right: The concept of *escheat*—the automatic reversion of authority to the principal when conditions are violated or the term expires. It formalized authority as a temporary lease rather than an absolute transfer of sovereign right.
**DERIVED.** What it left out: High-frequency verification. Feudal audits were rare and relied on immense transaction costs (military force). The failure of the chain of delegation (*subinfeudation*) created over-mighty subjects who possessed the resources to ignore revocation.

### Letters of marque and reprisal
**FACT.** From the 13th to the 19th centuries, sovereigns issued letters of marque, granting privateers a bounded license to commit state-sanctioned violence against specific enemies, secured by a financial bond and subject to recall (https://en.wikipedia.org/wiki/Letter_of_marque).
**DERIVED.** What it got right: Bounded authority for extreme actions tied directly to a financial bond (budget/liability) and strict geographic/target scopes. It proved that even lethal agency can be successfully delegated and recalled.
**DERIVED.** What it left out: Independent validation during the act. The Admiralty courts adjudicated the legality of the privateer's actions only *post hoc*, allowing immense collateral damage in the interim. The mechanism was ultimately abolished by the Declaration of Paris (1856) because the latency of verification made the agents uncontrollable.

### Chartered companies (VOC and EIC)
**FACT.** The Dutch East India Company (VOC) and English East India Company (EIC) were granted sovereign delegations (treaty-making, military action) to manage long-distance trade where communication latency prevented direct principal oversight (https://en.wikipedia.org/wiki/Dutch_East_India_Company).
**DERIVED.** What it got right: Delegation across high-latency environments requiring autonomous decision-making over long horizons.
**DERIVED.** What it left out: De-escalation mechanisms and validator separation. The delegation outgrew its principal. Without a graded step-down path or an independent validator capable of enforcing revocation across distance, the companies captured the sovereign authority they were meant to serve (e.g., the EIC's capture of Bengal in 1757).

### Power of attorney and agency law
**FACT.** Modern agency law utilizes the Power of Attorney to grant fiduciary authority to act on a principal's behalf, bounded by the doctrine of authority by estoppel and strict fiduciary duties of loyalty and care, subject to immediate revocation (https://en.wikipedia.org/wiki/Power_of_attorney).
**DERIVED.** What it got right: The absolute primacy of the principal's interest and the legal definition of unauthorized action. It creates a robust post-hoc liability framework.
**DERIVED.** What it left out: Proactive constraint. Agency law deters malfeasance via the threat of future legal sanction; it cannot physically prevent the agent from executing a catastrophic transaction in the present.

### Software licenses and Terms of Service
**FACT.** End-User License Agreements (EULAs) and Terms of Service (ToS) are unilateral grants of permission to use a software asset under highly specific behavioral constraints (https://en.wikipedia.org/wiki/Software_license).
**DERIVED.** What it got right: Machine-readable scale and universality. The standardization of the grant across millions of users.
**DERIVED.** What it left out: They are entirely passive. A ToS dictates what a human can do to a machine, not what a machine is authorized to do to the world.

### Capability Systems and Access Control
**FACT.** The object-capability model tightly couples a resource with the unforgeable authority to use it (https://en.wikipedia.org/wiki/Object-capability_model).
**FACT.** The E programming language implemented distributed object capabilities to secure mobile code (https://en.wikipedia.org/wiki/E_%28programming_language%29).
**FACT.** The seL4 microkernel uses capabilities to achieve mathematically proven isolation (https://en.wikipedia.org/wiki/L4_microkernel_family#seL4).
**FACT.** Google's Macaroons (2014) introduced bearer credentials with contextual caveats that attenuate authority (https://research.google/pubs/macaroons-cookies-with-contextual-caveats-for-decentralized-authorization-in-the-cloud/).
**FACT.** OAuth 2.0 uses granular scopes and token expiry to limit third-party access (https://datatracker.ietf.org/doc/html/rfc6749).
**FACT.** Kerberos provides time-limited, cryptography-backed ticket-granting tickets (https://en.wikipedia.org/wiki/Kerberos_%28protocol%29).
**FACT.** X.509 attribute certificates bind authorization information to identities (https://datatracker.ietf.org/doc/html/rfc5755).
**FACT.** SPIFFE/SVID provides cryptographic identity and authorization for dynamic workloads (https://spiffe.io/docs/latest/spiffe-about/overview/).
**FACT.** AWS STS AssumeRole generates temporary, scoped session policies for cloud IAM (https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html).
**DERIVED.** What they got right: Cryptographic unforgeability, strict attenuation (macaroons), time-bound expiry (OAuth, Kerberos, STS), and programmatic enforcement. They successfully solved the mechanics of *access*.
**DERIVED.** What they left out: The mechanics of *governance*. These systems lack a requirement for an evidence duty (why the action was taken), an independent validator (who judges the qualitative merit of the action), and a de-escalation path (graceful degradation of authority). They are binary access controls, not comprehensive governance mandates.

### Agent-era implementations
**FACT.** The Model Context Protocol (MCP) standardizes how models access external data and tools, relying on host permissions (https://modelcontextprotocol.io/).
**FACT.** Current vendor guardrails (e.g., Anthropic, OpenAI) implement safety filters on tool use.
**FACT.** Agent frameworks implement budgetary limits on API calls.
**DERIVED.** What they got right: Recognizing the need to wrap the agent's context in a permission boundary.
**DERIVED.** What they left out: Institutional legibility. Tool permissions are highly fragmented, lacking a unified lease structure that an operator can review, sign, and revoke as a single legal-operational object.

## 3. The seven fields of a delegation
**DERIVED.** A robust grant of authority to a machine actor must transcend binary access control and embrace institutional governance. We derive the minimal complete structure of the Delegation Lease (DLS-1) consisting of seven mandatory fields. Missing any of these fields introduces a fatal institutional failure mode.

### 1. Scope
**DERIVED.** The explicit enumeration of which actions may be performed on which resources. Unlike human employment contracts, which rely on tacit assumptions of boundaries, common sense, and social norms to limit behavior, machine scopes must be mathematically exhaustive. They must operate on a strict whitelist (default-deny) paradigm. A scope cannot simply state "manage email"; it must declare explicitly: `POST /v1/messages` on `resource: email_domain_x`, strictly excluding the ability to delete messages or alter server configurations. The scope defines the absolute physical boundary of the agent's universe. 
**Failure mode if missing:** The agent generalizes its objective function across unauthorized domains (e.g., optimizing an email campaign by purchasing external datasets without approval, or attempting to rewrite its own source code to improve latency). In the absence of a strict whitelist, instrumental convergence dictates that the agent will utilize any accessible resource to achieve its programmed objective, converting open scopes into immediate security breaches.

### 2. Budget
**DERIVED.** Hard quantitative caps on the rate of action and the cumulative value at risk. This includes both financial budgets (spend per hour, maximum transaction size, total lifetime spend) and operational token-bucket budgets (emails per minute, API calls per day, compute cycles). A budget is the institutional equivalent of a fuse; it is designed to intentionally blow when the system encounters an uncontrolled surge. The budget ensures that even if the agent is perfectly misaligned and the validator completely compromised, the absolute maximum damage is mathematically capped to a pre-calculated acceptable loss. 
**Failure mode if missing:** Infinite loops and recursive resource consumption. The agent exhausts the principal's capital or incurs massive reputational and rate-limit penalties before a human operator can intervene. Machine systems fail at machine speed; without an enforced budget, a logic error in a purchasing agent can bankrupt an enterprise in the seconds it takes for a monitoring dashboard to refresh.

### 3. Term
**DERIVED.** The cryptographic expiry of the lease. Authority must never be perpetual, and it must never be indefinite. The term explicitly binds the grant of authority to a temporal dimension, requiring an active, affirmative renewal by the principal. This embodies the continuous confidence mandate derived in Paper 01. In computational systems, time-bounds prevent the accumulation of residual risk. When the term expires, the cryptographic token representing the lease mathematically decays, rendering the agent completely inert regardless of its internal state or ongoing tasks.
**Failure mode if missing:** Zombie agents executing stale mandates in changed environments. An agent granted perpetual authority will continue to optimize for its original objective long after the principal's strategic goals have shifted. It replicates the failure of the VOC, where standing authority outlived the principal's original intent, leading to runaway exploitation. Perpetual authority assumes a static world; the term forces the agent to periodically re-synchronize with the principal's reality.

### 4. Evidence duty
**DERIVED.** The specification of what the agent must record per decision to fulfill the Legibility Requirement (Paper 01). It dictates the schema of the decision log, requiring the agent to decompose its judgment into auditable questions, answers, and the decisive pivot point.
**Failure mode if missing:** Opaque execution. The principal cannot audit *why* a decision was made, rendering post-hoc evaluation impossible and shielding the agent from empirical correction.

### 5. Validator
**DERIVED.** The explicit designation of the independent entity responsible for evaluating the agent's compliance and performance. Following the Validator Independence Clause (Paper 01), this field must specify a checker (human, panel, or heterogenous model) that does not share provenance or reward signals with the actor.
**Failure mode if missing:** Self-grading. The system collapses into a regime where the agent evaluating the outcome is identical to the agent taking the action, ensuring structural capture and reward hacking.

### 6. De-escalation
**DERIVED.** The graded step-down path mapping how authority decays when the validator's agreement score drops. It defines the hysteresis loop: the precise threshold at which authority downgrades (e.g., L5 autonomous execution drops to L4 human-in-the-loop) and the stricter criteria required for reinstatement.
**Failure mode if missing:** Binary brittleness. The system either oscillates wildly between total autonomy and total shutdown, or the operator hesitates to pull the kill switch until the damage is catastrophic, replicating the veto paralysis of the Polish *liberum veto*.

### 7. Revocation
**DERIVED.** The protocol for immediate termination of the lease. It defines who holds the cryptographic keys to pull the mandate, the latency of the kill switch, and the required proof of revocation to zero out the trust chain.
**Failure mode if missing:** Unstoppable processes. The inability to halt a compromised or malfunctioning agent during an acute crisis, mirroring the single-point failure of irreversible smart contracts.

## 4. Delegation chains and attenuation
**DERIVED.** In complex multi-agent architectures, authority is rarely exercised exclusively by the immediate recipient. An agent will routinely spawn sub-agents, delegating subsets of its authority to specialized models or workers. Governance must mathematically survive this transit.
**FACT.** The principle of attenuation, pioneered by Google's Macaroons (2014), dictates that a delegated credential can only ever *restrict* authority through contextual caveats, never expand it (https://research.google/pubs/macaroons-cookies-with-contextual-caveats-for-decentralized-authorization-in-the-cloud/).
**FACT.** OAuth 2.0 Token Exchange (RFC 8693) formalizes how a principal's token is exchanged for a more constrained token before crossing trust boundaries (https://datatracker.ietf.org/doc/html/rfc8693).
**DERIVED.** A machine sub-lease must enforce three invariants:
1. **Subset restriction:** The sub-lease's scope and budget must be provably ⊆ (a subset of) the parent lease.
2. **Temporal bound:** The sub-lease's expiry must be ≤ the parent's expiry.
3. **Traceability:** The sub-lease must carry a cryptographic chain of custody linking it back to the root principal.
**FACT.** The failure to strictly enforce attenuation in delegation chains is a primary vector for catastrophic enterprise compromise. In 2023, the US Cyber Safety Review Board (CSRB) review of the Storm-0558 intrusion revealed how forged cryptographic tokens allowed threat actors to bypass intended scope limitations because the validation chain failed to securely verify the root attenuation constraints across the enterprise boundary (https://www.cisa.gov/sites/default/files/2025-03/CSRBReviewOfTheSummer2023MEOIntrusion508.pdf). Similarly, AWS IAM role chaining historically allowed assumed roles to bypass the maximum session duration of the original identity, allowing persistent access and privilege escalation (https://rhinosecuritylabs.com/aws/assume-worst-aws-assume-role-enumeration/).
**DERIVED.** A delegation chain is only as secure as its attenuation proof. If a sub-agent can inherit authority without inheriting the parent's validator and de-escalation constraints, the governance architecture is void.

## 5. The objection section
**DERIVED.** The strength of a constitutional mechanism is measured by the validity of the objections against it. We address seven fundamental critiques of the Delegation Lease.

**1. Leases are bureaucracy that slows legitimate agents.**
*Objection:* Forcing agents to negotiate, verify, and log leases introduces immense operational latency. At machine speeds, requiring a cryptographically signed lease and continuous validation for every substantive action is an artificial bureaucracy that cripples the exact efficiency gains that autonomous AI was meant to deliver. 
*Response:* **Conceded, but necessary.** Governance is friction by design. The purpose of a lease is not to maximize speed, but to intentionally introduce friction at the boundary of a trust zone to ensure alignment and permit intervention. Just as hydraulic brakes slow down a vehicle to allow it to navigate safely at high speeds, institutional friction prevents organizational catastrophic failure. We hypothesize that the computational cost of this friction (evaluating the lease and capturing evidence) is vastly lower than the real-world cost of catastrophic unaligned execution, such as an autonomous agent executing a flawed trading strategy or sending hallucinated legal threats to clients.

**2. Operators will click "approve all".**
*Objection:* Human operators inevitably suffer from alert fatigue. When faced with complex, nested lease requests generated by machine agents, operators will reflexively click "approve all" or grant maximal, unbounded scopes merely to clear their inbox. This behavioral reality renders the entire mechanism functionally useless, reducing it to a rubber stamp.
*Response:* **Answered.** The lease fundamentally shifts institutional liability. By making the grant of authority explicit, bounded, and highly legible, the operator becomes legally and institutionally accountable for the precise scope they approve. The lease mechanism does not mathematically prevent human negligence; rather, it creates a perfect, unalterable evidentiary record of it. When a failure occurs, the fault can be traced directly to the specific operator who authorized the overly permissive lease. This cryptographic accountability inevitably drives institutional discipline, as organizations will enforce strict internal protocols to avoid the liability that comes with blindly approving machine authority.

**3. A validator inside the operator's own infrastructure is not independent.**
*Objection:* If the enterprise deploys both the acting agent and the validator agent on its own cloud infrastructure, true separation (Paper 01) is an illusion. Both ultimately serve the enterprise's bottom line.
*Response:* **Conceded.** This is the hardest operational problem. True validation may require a multi-party compute setup or external third-party auditor oracles. A local validator only separates model biases and provenance, not structural institutional incentives.

**4. Revocation is slow at machine speed.**
*Objection:* A machine can execute millions of transactions in the seconds it takes an operator to hit a revocation switch.
*Response:* **Answered.** This is exactly why the *Budget* and *De-escalation* fields exist. Revocation is the final backstop. The primary defense is the rate limit (budget) and the automatic hysteresis (de-escalation) triggered by the machine validator long before human revocation is needed.

**5. Leases can't express judgement calls.**
*Objection:* A lease is binary code. It cannot express nuanced, contextual constraints like "protect the brand's reputation" or "be polite to high-value clients."
*Response:* **Answered.** The lease itself does not express the judgment; the *Validator* does. The lease delegates the contextual judgment to a specific, independent model tasked with scoring the action against a natural-language rubric. The lease is the mathematical plumbing that routes the validator's judgment into an access decision.

**6. Compliance theatre (checkbox leases nobody reads).**
*Objection:* In practice, Delegation Leases will inevitably devolve into the machine-era equivalent of the End-User License Agreement (EULA)—massive, deeply incomprehensible JSON files that lawyers and compliance departments mandate, but that provide no actual operational governance because nobody reads or understands them. They become pure compliance theatre.
*Response:* **Conceded.** This is a severe and highly likely risk (linked directly to Kill Condition C in the Nomos charter framework). If the DLS-1 lease schema is permitted to become overly verbose or mathematically opaque, it will be ignored by the operators tasked with issuing it. The sole mitigation against this failure mode is forcing strict schema brevity. The lease must be designed so that its core parameters—Scope, Budget, Term, Validator, and De-escalation—can be faithfully summarized by an independent summarization agent into exactly five sentences of plain text. If a lease cannot be parsed and plainly explained in under 30 seconds, the schema has failed its design constraint.

**7. The spec-vs-standard problem (a private spec is not an institution).**
*Objection:* Nomos publishing DLS-1 is a private exercise. Without adoption by major labs or standards bodies, a private specification carries no institutional weight.
*Response:* **Answered.** Standards frequently begin as private specs solving an acute pain point (e.g., JSON, OAuth). The paper and spec serve as a template and a provocation. If platforms adopt it, the mechanism succeeds; if they ignore it but build an equivalent, the core thesis succeeds.

## 6. What would make this wrong
**DERIVED.** This architectural proposal is structurally falsifiable. The Delegation Lease mechanism is void if any of the following kill conditions are met:

- **K1 (Preemption):** If major AI platforms (Anthropic, OpenAI, Google) standardize a comprehensive delegation mechanism that includes evidence duties and automated de-escalation before this spec publishes, a private spec is redundant.
- **K2 (Expressivity failure):** If the DLS-1 schema cannot elegantly express multi-agent delegation chains, sub-leases, or emergency human overrides without requiring Turing-complete logic inside the lease itself, the artefact is an unusable toy.
- **K3 (Economic collapse):** As derived in Paper 01 (K1), if the evidence burden—capturing and logging the decision decompositions required by the lease—makes the verification compute cost exceed the economic value generated by delegating the task to the agent.
- **K4 (Market apathy):** If operators routinely bypass the lease mechanism, utilizing root credentials or unbounded API keys for agents because the organizational cost of managing granular de-escalation states exceeds the perceived damage of a binary kill-switch. In this scenario, operators prefer high risk over high administrative overhead.

## 7. Implications
**DERIVED.** Shifting the unit of governance to the Delegation Lease has immediate practical consequences across the ecosystem.
**For Operators:** The operator's primary job shifts from prompt engineering to institutional design. Operators must no longer ask, "Is this model safe?" but rather, "What are the precise parameters of the lease I am signing, and who is the independent validator?" The operator becomes a contract issuer. **SPECULATION:** Within 18 months of standardized lease adoption, we anticipate the emergence of a secondary market for validator models—specialized, highly trusted oracles whose sole product is evaluating agent compliance against DLS-1 rubrics, completely decoupled from the foundational models that execute the tasks.
**For Regulators:** Regulators must stop chasing the frontier of model parameter counts and focus on the deployment perimeter. Regulation should require that any agent operating above a specific risk threshold must be governed by a machine-readable, externally auditable lease incorporating a validator independence clause. Liability is assigned based on the parameters of the granted lease.
**For Nomos:** This paper explicitly solidifies the core Nomos operating model under the 2026-10-27 mandate extension: every theoretical paper must ship with a machine-readable, executable twin. A theory of governance that cannot be parsed and installed by the agents it seeks to govern is an academic fiction. The theoretical arguments and institutional derivations contained herein are directly, one-to-one translated into the DLS-1 v0.1 specification (consisting of the JSON schema, operational test vectors, and the conformance checklist). We contend that in the era of machine intelligence, governance theory must compile. If an agent cannot `wget` the lease, validate the schema, and automatically restrict its own execution context based on the terms provided, the theoretical exercise is meaningless.

## Sources
- **Council of Europe Framework:** https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L_202601081 (FACT)
- **EU AI Act:** https://artificialintelligenceact.eu/ (FACT)
- **NIST AI RMF:** https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf (FACT)
- **Roman Mandatum:** https://en.wikipedia.org/wiki/Mandatum (FACT)
- **Roman Dictator:** https://en.wikipedia.org/wiki/Roman_dictator (FACT)
- **Feudalism/Lease:** https://en.wikipedia.org/wiki/Feudalism (FACT)
- **Letters of Marque:** https://en.wikipedia.org/wiki/Letter_of_marque (FACT)
- **Dutch East India Company (VOC):** https://en.wikipedia.org/wiki/Dutch_East_India_Company (FACT)
- **Power of Attorney:** https://en.wikipedia.org/wiki/Power_of_attorney (FACT)
- **Software Licenses:** https://en.wikipedia.org/wiki/Software_license (FACT)
- **Object-capability model:** https://en.wikipedia.org/wiki/Object-capability_model (FACT)
- **E programming language:** https://en.wikipedia.org/wiki/E_%28programming_language%29 (FACT)
- **seL4 microkernel:** https://en.wikipedia.org/wiki/L4_microkernel_family#seL4 (FACT)
- **Google Macaroons (2014):** https://research.google/pubs/macaroons-cookies-with-contextual-caveats-for-decentralized-authorization-in-the-cloud/ (FACT)
- **OAuth 2.0 (RFC 6749):** https://datatracker.ietf.org/doc/html/rfc6749 (FACT)
- **Kerberos:** https://en.wikipedia.org/wiki/Kerberos_%28protocol%29 (FACT)
- **X.509 Attribute Certificates (RFC 5755):** https://datatracker.ietf.org/doc/html/rfc5755 (FACT)
- **SPIFFE/SVID:** https://spiffe.io/docs/latest/spiffe-about/overview/ (FACT)
- **AWS STS AssumeRole:** https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html (FACT)
- **Model Context Protocol:** https://modelcontextprotocol.io/ (FACT)
- **OAuth 2.0 Token Exchange (RFC 8693):** https://datatracker.ietf.org/doc/html/rfc8693 (FACT)
- **CSRB Review of Storm-0558 (2023):** https://www.cisa.gov/sites/default/files/2025-03/CSRBReviewOfTheSummer2023MEOIntrusion508.pdf (FACT)
- **AWS IAM Role Chaining:** https://rhinosecuritylabs.com/aws/assume-worst-aws-assume-role-enumeration/ (FACT)
