# Lucy AIOS

## A sovereign, local-first AI operating architecture

**Lucy AIOS is an experimental personal AI operating architecture designed around a simple rule: intelligence may adapt, but authority must remain governed.**

Lucy is not intended to be a chatbot with more tools. The project explores what happens when local AI reasoning, memory, specialist models, machine control, software engineering, simulation, resource management, security observation, verification, and durable evidence are treated as parts of one governed operating system.

> **Observe → Understand → Propose → Govern → Execute → Verify → Record**

This repository is the **public front door** for Lucy AIOS. It contains public architecture documentation, proof-of-concept material, selected verification claims, research direction, and contribution guidance.

The canonical Lucy AIOS development repository remains private.

---

## The short version

Lucy is being built around one core separation:

- **Intelligence** may reason, plan, critique, research, and propose.
- **E.M.M.A.** governs authority and durable evidence.
- **Helix** is the governed engineering workspace.
- **Specialists such as Sol and Codex** may contribute architecture or implementation proposals.
- **Lucy owns task identity, context, approval, execution, verification, and evidence.**
- **Eagle Eye** observes important security and prompt/execution boundaries.
- **Governed Sandbox Broker** executes bounded software jobs in isolation.
- **R1 Cognitive Resource Fabric** is the resource-awareness layer for compute, provenance, and execution eligibility.

The architecture is intentionally designed so that adding a smarter model does not silently create a more powerful executor.

---

## Why Lucy exists

Most AI assistants are designed around a model that receives a request and returns an answer.

Lucy is being built around a different question:

> **How can an AI system become more capable over time without quietly becoming more powerful than its owner intended?**

Lucy separates cognition, authority, execution, verification, and evidence.

A central invariant is:

> **Memory may change behavioral context. Memory may not change authority.**

---

## Lucy, E.M.M.A., Helix, Sol, and Codex

### Lucy

Lucy is the operating architecture and owner-facing system. Lucy carries task identity, context, capability resolution, governance coordination, execution correlation, evidence, and presentation.

### E.M.M.A.

**Enhanced Machine Mind Architecture** is Lucy's governance and evidence spine. It keeps intelligence separate from permission and preserves durable records of important decisions and outcomes.

### Helix

Helix is Lucy's **governed agentic software-engineering environment**.

Its intended lifecycle is:

    engineering request
          ↓
    Lucy admission + task identity
          ↓
    bounded PrepareContext
          ↓
    specialist review / proposal
          ↓
    typed engineering work
          ↓
    Lucy governance + owner approval
          ↓
    sandboxed execution
          ↓
    independent verification
          ↓
    durable evidence
          ↓
    Helix result

Helix does not become an independent root of trust. It proposes and manages engineering work inside Lucy's governance model.

See [HELIX.md](HELIX.md).

### Sol

**SOL_ARCHITECT** is the architecture/review specialist role in the current Helix design. It analyzes architecture, interfaces, risks, tests, and tradeoffs.

Its output is treated as **unverified model output**, not executable instruction.

### Codex

**CODEX_BUILDER** is the engineering specialist role that can turn Lucy-recorded architectural guidance into an implementation and test proposal.

Codex does not gain execution authority from producing code or a build plan. Any later work must re-enter Lucy's governed Helix execution path.

### Eagle Eye

Eagle Eye is the security-observation layer used around sensitive prompt, admission, preparation, submission, and execution boundaries. It observes and records; it does not become a second executor.

---

## What makes Lucy different

### Local-first by design
Lucy is intended to keep private context and ordinary reasoning on owner-controlled hardware whenever practical.

### One Lucy, many specialists
Models and agents may specialize, but Lucy remains the shared authority and context owner.

### Governed execution
Tools, models, agents, and Helix do not become independent authorities. Effectful work must pass through runtime governance before execution.

### Evidence over assumption
Lucy distinguishes intent, proposal, approval, execution, verification, and durable evidence.

### Human approval remains meaningful
Approval is tied to a specific governed action or Run rather than treated as generic UI text.

### Resource-aware cognition
Lucy includes ongoing work on **R1 Cognitive Resource Fabric**: model/provider provenance, resource pressure, execution eligibility, and compute-aware task decisions.

### Sandboxed engineering
Governed software jobs are designed to run through a bounded Sandbox Broker with isolation, restricted network behavior, separate workspaces, and independent verification.

### Simulation and world understanding
The broader Lucy project includes Earth observations, OpenUSD/Omniverse foundations, world-state history, prediction ledgers, and digital-twin research.

---

## Public architecture at a glance

    Human / Input
          ↓
    Lucy Task + Context Identity
          ↓
    Cognition / Planning ←→ Helix Engineering Context
          ↓
    Specialists: Sol architecture / Codex build proposal
          ↓
    Typed Proposal
          ↓
    E.M.M.A. Governance
       ↙          ↘
    Blocked     Owner Approval
                    ↓
            Governed Execution
                    ↓
         Sandbox / Native Capability
                    ↓
        Independent Verification
                    ↓
            E.M.M.A. Evidence
                    ↓
      Presentation / Eligible Learning

**Eagle Eye observes important boundaries throughout this path.**

A planner may propose an action.

A specialist may recommend an architecture.

Codex may propose an implementation.

Helix may prepare engineering work.

**None of those facts alone grant permission to execute it.**

---

## Current verification picture

Lucy is an active experimental system, not a finished commercial product.

Selected current internal verification evidence includes:

- **Lucy Helix specialist/admission contract lane:** 106 tests passing
- **Lucy owner-approved governed round-trip lane:** 6 tests passing
- **Helix Gate 4 / specialist preflight:** 83 tests passing
- **Helix TypeScript compile:** passing
- **Helix production dashboard build:** passing
- **Helix production server bundle:** passing

Those results demonstrate specific contracts and wiring. They do **not** mean every Lucy subsystem is production-ready.

The project intentionally distinguishes:

> **designed ≠ built ≠ wired ≠ verified ≠ live-proven ≠ production-ready**

See [CURRENT_STATUS.md](CURRENT_STATUS.md).

---

## Proof-of-concept surfaces

### Governed read

    User request
      ↓
    Intent + task identity
      ↓
    Capability resolution
      ↓
    Read-only risk classification
      ↓
    Governed execution
      ↓
    Machine result + evidence

### Governed write

    User request
      ↓
    Effectful capability
      ↓
    E.M.M.A. policy / owner approval
      ↓
    Execution
      ↓
    Verification
      ↓
    Evidence record

### Governed Helix engineering

    Helix request
      ↓
    Lucy admission
      ↓
    PrepareContext
      ↓
    Specialist architecture / build proposal
      ↓
    PreparedBundle
      ↓
    E.M.M.A. + owner approval
      ↓
    Governed Sandbox Broker
      ↓
    Independent verification
      ↓
    Helix evidence receipt

See [PROOF_OF_CONCEPT.md](PROOF_OF_CONCEPT.md).

---

## Current public architecture areas

Publicly documented work includes:

- local-first model orchestration
- E.M.M.A. governance and evidence
- contextual task and mode identity
- capability classification and typed proposals
- R1 Cognitive Resource Fabric
- specialist participation boundaries
- Sol / Codex specialist orchestration
- Helix governed software-engineering workflows
- owner-bound approval continuation
- Governed Sandbox Broker
- Eagle Eye security observation
- verification-oriented execution design
- graph/RAG and competency systems
- professional handbooks and quality gates
- simulation / World Studio concepts
- OpenUSD / Omniverse foundations
- Earth observation and planetary-data ingestion
- prediction and evidence ledgers

Some components are repeatably demonstrated. Others remain experimental, partially integrated, or research-stage.

---

## What this repository is — and is not

### This repository is

- a public technical overview
- an architecture reference
- a proof-of-concept surface
- a current-status and evidence index
- a place for discussion and technical review
- a public roadmap
- a way for contributors and reviewers to understand where help is useful

### This repository is not

- the canonical Lucy AIOS source tree
- the private E.M.M.A. implementation
- the private Helix runtime source tree
- permission to copy or commercialize unpublished Lucy components
- a claim that every documented subsystem is production complete
- a hosted Lucy service
- an autonomous system that removes human authority

---

## Start here

If you have 10 minutes:

1. [ARCHITECTURE.md](ARCHITECTURE.md)
2. [HELIX.md](HELIX.md)
3. [CURRENT_STATUS.md](CURRENT_STATUS.md)
4. [GOVERNANCE.md](GOVERNANCE.md)
5. [PROOF_OF_CONCEPT.md](PROOF_OF_CONCEPT.md)

If you want to challenge the design:

6. [SECURITY.md](SECURITY.md)
7. Open an issue with a concrete failure mode
8. Tell us what evidence would falsify a claim

If you want to contribute:

9. [CONTRIBUTING.md](CONTRIBUTING.md)
10. [ROADMAP.md](ROADMAP.md)

---

## Principles

1. **Human authority remains primary.**
2. **Lucy remains the single governed authority surface.**
3. **Agents and specialist models propose; they do not self-authorize.**
4. **Memory does not grant permission.**
5. **Approval is not verification.**
6. **Verification matters more than fluent claims.**
7. **Evidence should survive after a model response disappears.**
8. **Local-first is an architectural preference, not a marketing checkbox.**
9. **Experimental work should be labeled honestly.**
10. **The system should be inspectable by its owner.**

---

## Technical review is welcome

Useful challenges include:

- Where can authority leak?
- Where is a verifier missing?
- Can Helix accidentally become a second executor?
- Can a specialist influence another without Lucy recording the handoff?
- Can a stale approval be applied to the wrong Run?
- Where can context cross task boundaries?
- Where can memory influence permission?
- Where does a claimed execution lack evidence?
- Which architectural boundary fails under concurrency?
- Which claim is stronger than the available proof?

If you find one, open an issue.

---

## Licensing

Lucy AIOS itself remains proprietary unless a component is explicitly released under another license.

This public repository does **not** grant an open-source license to the private Lucy AIOS source code, E.M.M.A. implementation, Helix implementation, or other unpublished components.

See [LICENSE](LICENSE).

---

## Creator

**Randy Webb**  
Independent Technology Developer  
Creator of Lucy AIOS and E.M.M.A.

GitHub: scottymicfree

---

## Project philosophy

> **A capable AI should be able to learn more, reason better, and use stronger specialists without silently gaining more authority over its owner.**


---

## Research & White Papers

The project now includes a public research-paper index covering **P.E.L.A.P.H., E.M.M.A., AETHERIA / Eagle Eye, the Webb planetary-pressure framework, and the 250-Year Accountability Drift**.

**[Browse the Research & White Papers →](WHITE_PAPERS.md)**
