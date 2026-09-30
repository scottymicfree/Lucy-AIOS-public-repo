# Contributing to Lucy AIOS Public

Thank you for taking the time to examine Lucy.

At this stage, the most valuable contributions are **technical review, reproducible critique, documentation, test concepts, verifier ideas, public contract proposals, and architecture challenges**.

The canonical Lucy AIOS and Helix implementations are not contained in this repository.

---

## Good contributions

Examples:

- identify an ambiguous authority boundary
- describe a concrete E.M.M.A. governance bypass scenario
- challenge the one-Lucy invariant
- identify where Helix could accidentally become a second executor
- identify a stale-approval or Run-correlation failure
- identify a hidden specialist-to-specialist state channel
- propose a better verifier contract
- propose a safer public schema for admission, PrepareContext, PreparedBundle, or specialist receipts
- improve an architecture diagram
- improve evidence/status labeling
- identify a claim that needs stronger evidence
- compare Lucy or Helix to relevant published systems or research
- propose a reproducible benchmark for governed engineering

---

## Current review targets

The project particularly welcomes review of:

### E.M.M.A. governance
Can intelligence, memory, trust, or context silently influence permission?

### Helix
Can the engineering system bypass Lucy, select its own authority-bearing identity, or execute around the owner approval ceremony?

### Sol / Codex orchestration
Can one specialist influence another without a Lucy-recorded evidence handoff?

### Approval correlation
Can an approval intended for one Run be applied to a different pending action?

### Sandbox execution
Can generic shell/network authority escape the typed job boundary?

### Verification
Can execution be presented as successful without an independent check?

### Evidence
Can receipts be replayed, detached, forged, or attached to the wrong task?

### R1 / provider provenance
Can Lucy confuse which model/provider actually produced a result?

### Context identity
Can task context, mode identity, or professional competency leak across unrelated work?

---

## Please separate facts from proposals

Use language such as:

- **Observed:** ...
- **Reproduced:** ...
- **Verified:** ...
- **Proposed:** ...
- **Hypothesis:** ...
- **Not live-proven:** ...
- **Not verified:** ...

Lucy intentionally distinguishes:

> **designed ≠ built ≠ wired ≠ verified ≠ live-proven ≠ production-ready**

---

## Pull requests

Keep pull requests narrow.

A useful PR should explain:

1. What problem does this solve?
2. Which public contract or document changes?
3. What evidence supports the change?
4. Does the change alter a security or authority assumption?
5. How can another person verify it?
6. Does it strengthen or weaken the one-Lucy boundary?

---

## Private-core contributions

Do not submit:

- private Lucy source code
- private Helix source code
- leaked implementation details
- credentials or secrets
- machine-specific sensitive paths
- proprietary third-party material
- unpublished security details merely to make a public demo look impressive

Access to a private repository does not grant permission to republish its contents.

---

## Conduct

Be rigorous without being hostile.

Attack assumptions, evidence, boundaries, and code — not people.
