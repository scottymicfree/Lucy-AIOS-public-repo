# Lucy AIOS — Current Public Status

**Status date: September 30, 2026**

This document is a public-facing snapshot of the current Lucy architecture. It intentionally separates architecture claims from verification claims.

The canonical implementation remains private.

---

## Status vocabulary

Lucy uses these words deliberately:

| State | Meaning |
|---|---|
| **Designed** | architecture or contract exists |
| **Built** | implementation exists |
| **Wired** | implementation participates in the intended runtime path |
| **Verified** | repeatable tests or evidence demonstrate the stated contract |
| **Live-proven** | demonstrated on the target machine/environment |
| **Production-ready** | mature enough for supported operational use |

A subsystem may be verified without being production-ready.

---

## Core system

### Lucy runtime
**Status:** active experimental system.

Lucy carries task/context identity, capability resolution, governance coordination, execution correlation, evidence, and presentation.

### E.M.M.A.
**Status:** active governance/evidence spine.

Current work uses E.M.M.A. as the durable evidence source for admission, preparation, specialist handoff, submission checks, and execution correlation.

### One-Lucy invariant
**Status:** architectural invariant.

Lucy is designed to avoid duplicate roots of execution authority. Specialists and engineering subsystems operate through Lucy rather than becoming independent owners of permission.

---

## Helix

**Status:** governed engineering architecture is built and CI-verified through the owner-approval/evidence boundary.

Current verified contracts include:

- Lucy-owned Helix admission
- task identity
- BuildTicket
- WorkspaceLease
- PrepareContext
- PreparedBundle
- handle-only browser submission
- exact owner-approval Run correlation
- governed sandbox-job continuation
- independent verification evidence
- server-owned Sol-to-Codex specialist handoff
- specialist preflight

Helix remains subordinate to Lucy governance.

See [HELIX.md](HELIX.md).

---

## Sol / Codex specialist orchestration

### Sol architect role
**Status:** contract, orchestration, provider boundary, and CI verification complete; live machine model identity still requires explicit configuration.

SOL_ARCHITECT is used for architecture, interface, risk, and test reasoning.

Lucy refuses to silently label an unspecified provider-default model as Sol.

### Codex builder role
**Status:** contract, orchestration, provider boundary, and CI verification complete.

CODEX_BUILDER consumes a Lucy-recorded Sol receipt for the same PrepareContext and returns an implementation/test proposal.

The proposal is not executable authority.

### Browser boundary
**Status:** verified.

The Helix browser does not choose:

- provider
- model
- local worktree path
- Lucy Run ID
- approval identity
- parent Sol receipt
- execution authority

Those remain server/Lucy-owned.

---

## Specialist preflight

**Status:** verified.

Before a live specialist request, Lucy can check:

- PrepareContext validity
- admission/task/ticket/lease binding
- current WorkspaceLease validity
- explicit Sol model configuration
- ChatGPT-authenticated Codex provider readiness
- local workspace mapping
- workspace existence / provider allow-list
- E.M.M.A. writability
- whether Lucy's approval lane is clear

Preflight:

- makes no model request
- consumes no approval
- executes no build
- discloses no local filesystem path to the browser

---

## Governed Sandbox Broker

**Status:** isolated governed execution foundation previously live-proven in Linux/Bubblewrap and integrated into the Helix governance design.

Design goals include:

- bounded job operations
- separate workspace
- network denied where required
- explicit authorization evidence
- independent verification
- no generic shell authority exposed through Helix

---

## Eagle Eye

**Status:** active security-observation architecture with prompt/boundary monitoring foundations.

Eagle Eye observes important security and execution boundaries. It does not grant authority or execute work.

---

## R1 Cognitive Resource Fabric

**Status:** active integration/research stream.

R1 work includes:

- resource-aware cognition
- provider provenance
- measured model identity
- learning eligibility
- execution/resource arbitration

The purpose is to make compute and provider identity part of the operating system's reasoning rather than an invisible implementation detail.

---

## Competency graph and professional profiles

**Status:** partially implemented / ongoing.

The design separates domain competencies and professional handbooks from Lucy's central reasoning loop.

Examples include:

- software engineering
- landscaping and trades knowledge
- quality gates
- handbook rules
- competency resolution

Competency affects what expertise and quality gates apply. It does not grant execution authority.

---

## World / Earth / simulation work

**Status:** active research and foundation work.

Current project areas include:

- OpenUSD scene descriptions
- NVIDIA Omniverse / Earth-2 foundations
- Earth observation ingestion
- planetary-boundary variables
- mobility history
- prediction ledgers
- observation history
- digital-twin / World Studio concepts

Observed, derived, predicted, and simulated states are intended to remain distinguishable.

---

## Current verification snapshot

Selected private-CI evidence as of September 30, 2026:

| Surface | Verification |
|---|---:|
| Lucy specialist/admission contracts | 106 passing |
| Lucy owner-approved Helix runtime round trip | 6 passing |
| Helix Gate 4 / specialist preflight | 83 passing |
| Helix TypeScript compile | passing |
| Helix production dashboard build | passing |
| Helix production server bundle | passing |

These counts support specific regression suites. They are not a global score for Lucy.

---

## Current live-machine gap

The next specialist milestone is intentionally machine-specific:

1. configure the real owner-approved Helix worktree mapping
2. pin the exact model identifier used for the Sol architect role
3. require specialist preflight to report READY
4. run one live Sol request through Lucy owner approval
5. collect the Lucy-recorded Sol receipt
6. run one Codex builder request through Lucy owner approval
7. collect the Codex implementation/test proposal
8. stop before code edits/build execution

Only after that should a Codex proposal be translated into typed Helix engineering work and re-enter the existing Lucy-governed sandbox path.

---

## Not claimed

This public repo does not claim that:

- Lucy is finished
- every subsystem is live-integrated
- specialist model output is trustworthy by default
- all CI-proven flows have been live-proven on every target machine
- Helix is independently autonomous
- a passing test count equals production readiness

The goal is to make the evidence boundary visible rather than hide uncertainty behind polished language.
