# Helix — Governed Agentic Engineering Inside Lucy AIOS

## What Helix is

Helix is Lucy AIOS's governed software-engineering environment.

It is intended to support agentic architecture review, implementation planning, building, testing, training, verification, and evidence collection **without becoming an independent execution authority**.

The relationship is:

> **Lucy is the operating system. E.M.M.A. is the governance/evidence spine. Helix is the engineering workspace inside that system.**

---

## Why Helix exists

Software-engineering agents are useful precisely because they can reason about large repositories and produce substantial changes.

That creates a governance problem.

If the same agent can:

1. decide what should change,
2. authorize the change,
3. execute it,
4. declare it successful,

then planning, authority, execution, and verification have collapsed into one actor.

Helix is being built around the opposite structure.

---

## Governed Helix lifecycle

    Engineering Request
          ↓
    Lucy Admission
          ↓
    Task Identity
          ↓
    PrepareContext
          ↓
    Specialist Review
          ↓
    Sol Architecture
          ↓
    E.M.M.A. Receipt
          ↓
    Codex Build Proposal
          ↓
    Typed Helix Work
          ↓
    PreparedBundle
          ↓
    E.M.M.A. Governance
          ↓
    Human Approval
          ↓
    TaskExecutor
          ↓
    Governed Sandbox Broker
          ↓
    Independent Verification
          ↓
    Durable Evidence
          ↓
    Helix Result

---

## Admission before engineering work

Helix does not mint its own authority objects.

Lucy owns:

- task identity
- BuildTicket issuance
- WorkspaceLease issuance
- PrepareContext binding
- approval identity
- execution Runs
- verification/evidence identity

A useful shorthand is:

- request_id = who knocked
- task_id = what Lucy recognized
- ticket_id = what Lucy agreed to consider
- lease_id = where bounded planning/workspace scope exists

None of those identifiers alone authorize execution.

---

## PrepareContext

A PrepareContext binds later engineering preparation to one admitted Lucy task.

It is designed to prevent:

- stale task reuse
- cross-task context mixing
- silent scope expansion
- browser-owned authority
- uncorrelated proposals

A lease remains scope/workspace context. It is not permission to execute.

---

## PreparedBundle

A PreparedBundle binds an exact JobSpec and exact Lucy sandbox proposal to the admitted task context.

The browser submits an opaque bundle handle rather than becoming the source of the full execution payload.

Lucy revalidates the bundle, evidence bindings, task/ticket/lease correlation, and authorization state before the proposal reaches governance.

---

## Owner approval

Helix uses Lucy's existing owner-confirmation ceremony.

A Helix approval is correlated to the exact pending Lucy Run so a stale UI action cannot silently approve a different task that became pending later.

Approval means:

> **this exact governed action may continue**

It does not mean:

> **future actions are automatically allowed**

---

## Sol and Codex inside Helix

Helix currently defines two specialist roles.

### SOL_ARCHITECT

Purpose:

- architecture analysis
- interface review
- risk review
- test strategy
- tradeoff analysis

Rules:

- read-only specialist role
- model identity selected/configured by Lucy
- local workspace selected by Lucy
- no file edits through this lane
- no builds/tests through this lane
- no owner approval authority
- no memory-write authority
- output treated as unverified model output

### CODEX_BUILDER

Purpose:

- translate Lucy-recorded architecture into a concrete implementation/test proposal

Rules:

- cannot start from arbitrary browser-supplied Sol text
- must consume a Lucy-recorded Sol receipt for the same PrepareContext
- read-only specialist role
- produces a proposal, not an execution
- must later re-enter normal Helix/Lucy governance before any code-changing work

---

## No hidden agent-to-agent channel

Sol does not talk directly to Codex.

The intended handoff is:

    Sol
      ↓
    Lucy Run
      ↓
    E.M.M.A. specialist receipt
      ↓
    Lucy reloads and verifies parent output
      ↓
    Codex

This keeps shared context, provenance, and authority inside Lucy rather than inside private side channels between agents.

---

## Specialist preflight

Before a live Sol/Codex request, Lucy can perform a read-only readiness check.

It verifies:

- active PrepareContext
- original admission binding
- current WorkspaceLease
- explicit Sol model identity
- Codex provider readiness
- owner-approved local worktree mapping
- filesystem allow-list
- E.M.M.A. availability
- clear owner-approval lane

The browser is told whether the lane is ready without receiving the local filesystem path.

---

## Sandbox execution

Specialist output is intentionally separated from build execution.

A future implementation proposal must become typed Helix work and proceed through:

    proposal
      ↓
    Lucy admission / context
      ↓
    JobSpec + PreparedBundle
      ↓
    owner approval
      ↓
    TaskExecutor
      ↓
    sandbox_job
      ↓
    Governed Sandbox Broker
      ↓
    independent verification
      ↓
    evidence

The specialist lane itself does not call the Sandbox Broker.

---

## Current public verification snapshot

As of September 30, 2026, selected private-CI evidence includes:

- Helix Gate 4 / preflight: **83 tests passing**
- TypeScript compile: **passing**
- production dashboard build: **passing**
- production server bundle: **passing**
- Lucy specialist/admission suite: **106 tests passing**
- Lucy governed owner-approved round trip: **6 tests passing**

These verify specific contracts, not overall production readiness.

---

## Security properties being protected

Helix is designed to make the following failures difficult and visible:

- browser-selected execution identity
- browser-selected model/provider
- browser-selected local worktree
- stale approval applied to a replacement Run
- raw proposal submission bypass
- duplicate approval creation
- Sol-to-Codex hidden state transfer
- agent self-authorization
- generic shell authority
- execution claims without verification
- verification evidence detached from the execution that produced it

---

## Current stop line

The current specialist gate intentionally stops here:

    Helix
      ↓
    Lucy specialist preflight
      ↓
    Sol architecture
      ↓
    Lucy evidence
      ↓
    Codex implementation/test proposal
      ↓
    STOP

The next boundary is not "let Codex edit everything."

The next boundary is:

> **Translate a reviewed Codex proposal into typed Helix work and send it through the already-proven Lucy governance + owner approval + sandbox + verification path.**
