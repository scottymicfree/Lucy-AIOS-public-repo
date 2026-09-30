# Lucy AIOS — Public Architecture

## 1. Architectural objective

Lucy AIOS explores an owner-controlled AI operating architecture in which cognition, specialist intelligence, authority, execution, verification, and evidence are separate concerns.

The system is designed so that increasing model capability does not automatically increase runtime authority.

A compact statement of the architecture is:

> **Intelligence proposes. Lucy binds context. E.M.M.A. governs. Execution acts. Verification proves. Evidence remembers.**

---

## 2. Core execution path

    Input / Observation
          ↓
    Lucy Task + Context Identity
          ↓
    Intent + Capability Resolution
          ↓
    Reasoning / Planning
          ↓
    Optional Specialist Participation
          ↓
    Typed Work Proposal
          ↓
    E.M.M.A. Governance
       ↙          ↘
    Blocked     Human Approval
                    ↓
              Authorized Work
                    ↓
             Execution Boundary
                    ↓
        Native Capability / Sandbox
                    ↓
          Independent Verification
                    ↓
           E.M.M.A. Evidence
                    ↓
     Presentation / Eligible Learning

Eagle Eye may observe important prompt, admission, preparation, submission, and execution boundaries without becoming a second execution authority.

---

## 3. Major planes

### Cognitive plane

Responsible for understanding, reasoning, planning, retrieval, task context, competency selection, and specialist participation.

It may influence **what is proposed**.

It must not independently determine **what is authorized**.

### Authority plane

E.M.M.A. is the governance concept used to separate intelligence from permission.

The authority plane may consider:

- capability identity
- operation type
- subject / resource affected
- task identity
- origin of the request
- risk class
- approval state
- trust state
- applicable policy
- evidence bindings

The authority plane should remain stable even when the cognitive plane learns or changes.

### Execution plane

The execution plane performs allowed work through bounded interfaces such as:

- filesystem operations
- shell execution
- hardware telemetry
- application control
- browser automation
- sandboxed jobs
- simulation interfaces

Execution is not evidence by itself.

### Verification plane

Verification asks whether the intended post-condition occurred.

Examples:

- Was a file actually created?
- Is the process actually stopped?
- Did the sandbox job produce the expected artifacts?
- Did the external operation return the expected object?
- Did the requested test actually pass?

### Evidence plane

Lucy uses E.M.M.A. to preserve inspectable records of decisions, correlations, and outcomes.

The project intentionally treats:

- requested
- admitted
- prepared
- proposed
- approved
- executed
- verified
- recorded

as different states.

---

## 4. One Lucy, many specialists

Lucy is designed around **one governed Lucy** rather than a swarm of equal independent executors.

Specialists may:

- research
- propose
- analyze
- draft
- critique
- inspect
- design tests
- propose implementation work

They should not:

- silently grant themselves authority
- write durable memory as an ungoverned side effect
- bypass Lucy to communicate hidden state to another specialist
- become independent roots of trust
- turn model output directly into machine-side effects

A specialist's output is evidence and input to Lucy's governed process.

---

## 5. Helix engineering plane

Helix is Lucy's governed software-engineering environment.

It is not a second operating system and not an independent executor.

Helix participates in a Lucy-owned lifecycle:

    Helix request
          ↓
    Lucy admission
          ↓
    task / ticket / lease
          ↓
    PrepareContext
          ↓
    specialist architecture / build proposal
          ↓
    JobSpec + PreparedBundle
          ↓
    E.M.M.A. governance
          ↓
    owner approval
          ↓
    TaskExecutor
          ↓
    Governed Sandbox Broker
          ↓
    independent verification
          ↓
    durable evidence
          ↓
    Helix result

Important authority rule:

> **Admission grants recognition and scope. Governance grants permission. Execution produces facts. Verification establishes what actually happened.**

See [HELIX.md](HELIX.md).

---

## 6. Specialist orchestration

The current Helix design defines two public specialist roles.

### SOL_ARCHITECT

Used for:

- architecture
- interfaces
- risks
- test strategy
- tradeoffs

Sol output is treated as **unverified model output** and authorizes nothing.

### CODEX_BUILDER

Used for:

- implementation planning
- test planning
- converting Lucy-recorded architecture into a concrete engineering proposal

Codex cannot consume arbitrary browser-supplied Sol text. The intended handoff is:

    Sol
      ↓
    Lucy Run
      ↓
    E.M.M.A. specialist receipt
      ↓
    Lucy reloads and verifies parent output
      ↓
    Codex

This preserves provenance and prevents a hidden agent-to-agent authority channel.

---

## 7. Context identity

A serious multi-agent system needs to know **which task** a piece of context belongs to.

Lucy work carries task and mode identity through language ingress, semantic resolution, context queries, Helix preparation, and governed-run correlation.

This is intended to reduce:

- context leakage between tasks
- ambiguous referents
- cross-agent state confusion
- stale approval reuse
- orphaned execution evidence

PrepareContext is one example of this principle applied to governed engineering work.

---

## 8. R1 Cognitive Resource Fabric

Lucy research includes resource-aware cognition: task planning should account for machine resources and provider identity rather than assuming unlimited compute.

Current R1 areas include:

- provider provenance
- model identity
- learning eligibility
- workload arbitration
- memory pressure
- latency
- GPU / CPU availability
- execution eligibility

The goal is not merely to select a model, but to make compute allocation part of the operating system's reasoning.

---

## 9. Competency and professional profiles

Lucy is being designed so that domains can carry structured competencies, handbooks, quality gates, and professional rules without turning the central reasoning layer into one giant monolith.

A competency can help determine:

- what knowledge is relevant
- which specialist should participate
- which quality gates apply
- what evidence should be produced

Competency does not equal authority.

---

## 10. Governed sandbox execution

The Governed Sandbox Broker is the bounded execution foundation used for isolated software jobs.

Public architectural goals include:

- bounded operations
- separate workspaces
- network denial where required
- explicit authorization evidence
- no generic shell authority through Helix
- post-run verification
- evidence correlated to the exact governed Run

A model proposal does not call the broker directly.

---

## 11. Eagle Eye security observation

Eagle Eye is the observer/security layer around important boundaries.

Its role is to make suspicious or policy-relevant transitions visible and evidentiary.

It is not:

- a second approval system
- a second TaskExecutor
- a replacement for E.M.M.A.
- independent authority

Public areas include runtime observation, prompt-boundary monitoring, and evidence references around important Helix preparation/submission steps.

---

## 12. World and simulation layer

Lucy research also includes:

- World Studio concepts
- OpenUSD scene description
- NVIDIA Omniverse / Earth-2 foundations
- Earth observation ingestion
- planetary-boundary data
- prediction and simulation ledgers
- historical observation context
- mobility history
- digital-twin concepts

Observed, derived, predicted, and simulated data should remain distinguishable.

---

## 13. Public status discipline

Lucy intentionally distinguishes:

> **designed ≠ built ≠ wired ≠ verified ≠ live-proven ≠ production-ready**

A CI-verified contract does not automatically prove target-machine integration.

A live execution does not automatically prove every adjacent subsystem.

See [CURRENT_STATUS.md](CURRENT_STATUS.md).

---

## 14. Architectural invariant

The shortest description of Lucy's design is:

> **Stronger intelligence may improve the proposal. It does not inherit the authority to execute it.**
