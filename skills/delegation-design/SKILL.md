# Skill: Human–AI Delegation Design

**Name:** `delegation-design`  
**Status:** Draft 0.1  
**Purpose:** Specify and evaluate bounded work delegation to an AI or automation, including handoff, authorization, review, escalation, and revocation.

## Inputs

- Work task and workflow baseline.
- Human principal, accountable owner, AI/tool actors, downstream recipients, and affected parties.
- Data sensitivity, consequence level, integrations, permissions, and applicable rules.

## Procedure

1. Map the workflow from request through completion, external side effects, evidence capture, and correction. Identify failure containment boundaries.
2. Separate the work assignment (what outcome is requested) from the authority grant (what actions may be taken). Specify principal, agent, task, permitted resources/tools/actions, prohibited actions, limits/quotas, expiry, evidence, escalation, and revocation.
3. Define which steps are draft-only, require approval, or may execute within strict bounds. Use least privilege and deterministic enforcement at the integration/tool boundary. State how the policy fails closed.
4. Specify subdelegation constraints, audit record, human-readable notice, uncertainty handling, exception path, appeal/correction, and accountable owner. Define how revocation stops future and in-flight actions, and test actual behavior.
5. Start with a bounded, low-consequence pilot; compare with the existing baseline using quality, time, error, workload, equity/accessibility, privacy/security, and reversibility measures appropriate to the context.
6. Exercise adversarial and ordinary failure cases: ambiguous instruction, missing data, tool/API outage, prompt injection, overbroad scope, duplicate action, quota exhaustion, expired grant, revoked grant, and partial completion.
7. Report observed outcomes, failures, residual risk, and evidence limits. Treat confidence-based permission adjustment as an unvalidated hypothesis unless independently tested and governed.

## Quality checks

- Authority is explicit, scoped, time-limited, attributable, and enforceable—not merely described in a prompt.
- Consequential external actions have an approval rule, owner, and reliable audit trail.
- Expiry, revocation, retries, duplicates, partial completion, and in-flight behavior have executable tests.
- Metrics compare the workflow to a baseline and include harms, not just speed or task completion.
- Humans retain genuine capacity and authority to review, contest, correct, and stop.
- Follow root `RESEARCH_PROTOCOL.md`; never claim safe or effective based on schema validation alone.

## Failure modes

Do not equate task completion with authorization; model confidence with permission; a policy document with enforcement; a cancellation flag with stopping an in-flight external action; or a successful test vector with production safety.

## Output

A workflow map, proposed delegation record/policy, approval and escalation matrix, enforcement and revocation test plan, pilot evaluation plan, threat/failure cases, owner assignments, and explicit go/no-go criteria. If integration behavior is untested, label the policy as a design proposal, not an implemented control.
