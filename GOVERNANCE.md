# E.M.M.A. Governance — Public Overview

## Enhanced Machine Mind Architecture

E.M.M.A. is Lucy AIOS's governance and evidence concept for keeping machine authority separate from model intelligence.

The public description intentionally focuses on contracts and invariants rather than disclosing private implementation details.

---

## The problem

A capable model can:

- produce persuasive plans
- call tools
- write code
- imitate confidence
- learn preferences
- coordinate specialists
- inspect large repositories
- propose substantial software changes

None of those capabilities should automatically grant authority over the machine.

---

## Core rule

> **Knowledge may influence proposals. It may not silently create permission.**

A learned preference such as "use PowerShell" may affect how Lucy prepares work.

A Sol architecture recommendation may affect a Codex proposal.

A Codex implementation plan may affect a Helix JobSpec.

None of those facts grant permission to execute.

---

## Governance lifecycle

    Proposed
      ↓
    Policy / Risk Decision
      ├── deny → Blocked + Evidence
      ├── approval required → Human Approval
      └── allow
      ↓
    Authorized
      ↓
    Executed
      ↓
    Verified / Verification Failed
      ↓
    Recorded

---

## Design expectations

### Explicit capability identity
Governance should evaluate a concrete operation, not an abstract promise.

### Invocation-level judgment
A tool may be safe in one invocation and dangerous in another.

### Expiring and scoped authority
Authorization should be bounded to the action, Run, scope, and time where appropriate.

### Run-bound approval
When a UI or subsystem presents an approval, Lucy should be able to prove which pending Run the owner is approving.

This protects against stale approval applying to a different task.

### Evidence
Governance decisions and important handoffs should leave inspectable evidence.

### No specialist privilege escalation
Sol, Codex, Helix, or another specialist should not be able to transform expertise into runtime authority.

### No hidden agent-to-agent authority channel
One specialist's output should reach another through Lucy-controlled context/evidence rather than through an untracked side channel.

---

## Admission is not authorization

Lucy deliberately separates recognition/scope from permission.

For governed Helix work:

- request identity says who asked
- task identity says what Lucy recognized
- BuildTicket says what Lucy agreed to consider
- WorkspaceLease says where bounded scope exists
- PrepareContext binds later preparation to that task
- PreparedBundle binds exact prepared work
- governance determines whether execution may proceed

None of the earlier objects is itself execution authority.

---

## Approval is not verification

Approval answers:

> May this action be attempted?

Verification answers:

> Did the intended result actually occur?

They are different gates.

A successful owner approval followed by a failed execution is still a failed execution.

A successful execution without independent verification should not be presented as verified.

---

## Memory boundary

Durable personal understanding can make Lucy more useful.

It can also create a dangerous failure mode if learned context changes permission.

Therefore:

> **Memory may change behavioral context. Memory may not change authority.**

This remains one of the project's central invariants.

---

## Specialist output boundary

Sol and Codex outputs are treated as model-generated evidence/proposals.

Current specialist receipts explicitly preserve the idea that the output is:

- unverified model output
- not trusted as executable instruction
- not execution authority
- not promotion authority
- not memory-write authority

A later engineering step must re-enter normal Lucy governance.

---

## Eagle Eye

Eagle Eye is used as an observer/security boundary around selected prompt, preparation, submission, and execution transitions.

Eagle Eye does not replace E.M.M.A. and does not execute work.

Its purpose is to make sensitive transitions more visible and evidentiary.

---

## Trust states

Lucy research has used bounded trust-state concepts such as:

- **SAFE**
- **PARTNER**
- **SOVEREIGN**

These are governance concepts, not personality labels.

A trust state should never mean "the AI may now ignore the owner."

---

## Responsible disclosure

If you identify a path that appears capable of bypassing governance, do not publish a working exploit in a public issue.

See [SECURITY.md](SECURITY.md).
