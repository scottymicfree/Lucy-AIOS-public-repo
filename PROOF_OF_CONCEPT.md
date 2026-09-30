# Lucy AIOS — Proof of Concept

## Purpose

A proof of concept should demonstrate the architectural claim, not the size of the repository.

For Lucy, the important claim is:

> **A model or agent can request meaningful machine work without becoming the authority that permits that work.**

The current public proof surface now includes ordinary capabilities, governed engineering, and specialist orchestration.

---

## POC A — Governed process read

### User intent

    list processes

### Expected contract

1. The request receives a task identity.
2. Lucy resolves the intent to a bounded process-inspection capability.
3. The request is classified as observational/read-only.
4. Governance evaluates the invocation.
5. The native capability executes.
6. The machine result is presented.
7. The result remains correlated with the governed Run.

### What this proves

- natural language can resolve to a bounded capability
- machine access does not require raw shell freedom
- governance participates even in simple tool use
- result presentation can remain separate from authority

---

## POC B — Governed file write

### User intent

    create a file

### Expected contract

1. The request receives a task identity.
2. Lucy resolves the request to a filesystem write capability.
3. Governance recognizes that the operation changes state.
4. Policy determines whether approval is required.
5. Execution remains blocked until required authorization exists.
6. The write occurs through the governed execution boundary.
7. A verifier checks the post-condition.
8. Evidence records the decision and result.

### What this proves

A planner, model, or agent cannot turn a proposal into a machine-side effect merely by producing convincing text.

---

## POC C — Governed Helix engineering round trip

### Engineering intent

A bounded software job should be prepared and executed without giving Helix direct execution authority.

### Expected contract

1. Helix submits a non-authorizing work request.
2. Lucy admits or rejects the request.
3. Lucy issues task identity, BuildTicket, WorkspaceLease, and PrepareContext.
4. Helix prepares an exact JobSpec and proposal.
5. Lucy attests a PreparedBundle.
6. The browser submits only the opaque PreparedBundle handle.
7. Lucy revalidates the exact bundle and evidence.
8. Lucy opens the existing owner-approval ceremony.
9. Approval is bound to the exact pending Lucy Run.
10. TaskExecutor dispatches the bounded sandbox job.
11. Governed Sandbox Broker performs the job.
12. Independent verification checks the result.
13. Lucy records durable evidence.
14. Helix receives the correlated result.

### What this proves

- Helix can coordinate engineering work without becoming a second executor
- the browser is not the source of authority-bearing payloads
- owner approval is correlated to one exact Run
- execution and verification stay separate
- the result can be tied back to the exact prepared engineering bundle

---

## POC D — Sol to Codex specialist handoff

### Specialist intent

Use one model for architecture and another for implementation planning without creating a hidden agent-to-agent authority channel.

### Expected contract

1. Helix asks Lucy for SOL_ARCHITECT.
2. Lucy validates the PrepareContext.
3. Lucy selects the configured model/provider/worktree.
4. The specialist call goes through Lucy's governed external-model lane.
5. Sol output is stored as unverified model output in the durable Lucy Run.
6. E.M.M.A. records a specialist receipt and output fingerprint.
7. Codex cannot start until Lucy has a valid Sol receipt for the same PrepareContext.
8. Lucy reloads and verifies the recorded Sol output.
9. CODEX_BUILDER receives the bounded Lucy-controlled context.
10. Codex returns an implementation/test proposal.
11. The flow stops before edits/build execution.

### What this proves

- specialists do not communicate through a private side channel
- browser users cannot choose hidden provider/model/run identities
- specialist output remains non-authorizing
- the handoff is evidence-bound
- stronger reasoning does not inherit execution permission

---

## POC E — Specialist preflight

Before the first live Sol/Codex request, Lucy can perform a read-only readiness check.

Preflight verifies:

- active PrepareContext
- valid admission/task/ticket/lease binding
- explicit Sol model identity
- ChatGPT-authenticated Codex readiness
- owner-approved worktree mapping
- worktree existence and allow-list compliance
- E.M.M.A. availability
- clear approval lane

Preflight makes no model request and grants no authority.

The local worktree path is not returned to the browser.

---

## Evidence standard

A strong Lucy demonstration should be able to show:

| Stage | Example evidence |
|---|---|
| Intent | user/Helix request + task identity |
| Admission | accepted scope |
| Context | PrepareContext / lease binding |
| Specialist | Lucy Run + specialist receipt |
| Resolution | capability / operation selected |
| Governance | risk / policy decision |
| Approval | exact pending Run correlation |
| Execution | bounded executor result |
| Verification | independent post-condition result |
| Evidence | durable correlated record |

---

## What would falsify the POC?

A POC should be considered incomplete if any of these are true:

- an agent or Helix can execute directly around governance
- approval is represented only as UI text
- a stale approval can approve a replacement Run
- browser input can silently replace server-owned execution identity
- specialists can pass hidden authority/state directly to each other
- an action is called verified without checking the result
- evidence cannot be correlated to the execution
- memory can silently change permission
- task identity is lost before execution
- a mocked path is presented as live machine execution
- specialist output is treated as trusted instruction merely because it is fluent

---

## Public evidence policy

The public repository should contain only evidence that is safe to disclose.

Do not publish:

- secrets
- credentials
- private user data
- unnecessary machine-specific paths
- unpublished security-sensitive implementation details
- proprietary source merely to make a demo look impressive

The goal is reproducibility of the architectural claim, not disclosure of the private core.
