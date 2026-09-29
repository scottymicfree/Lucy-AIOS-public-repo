# Lucy AIOS — Proof of Concept

## Purpose

A proof of concept should demonstrate the architectural claim, not the size of the repository.

For Lucy, the important claim is:

> **A model or agent can request meaningful machine work without becoming the authority that permits that work.**

This public repository therefore focuses on small, understandable execution stories.

---

## POC A — Governed process read

### User intent

```text
list processes
```

### Expected contract

1. The request receives a task identity.
2. Lucy resolves the intent to an eligible process-inspection capability.
3. The request is classified as observational/read-only.
4. Governance evaluates the invocation.
5. The native capability executes.
6. The returned machine state is presented.
7. The result can be correlated with the governed run.

### What this proves

- natural language can resolve to a bounded capability
- machine access does not require raw shell freedom
- governance participates even in simple tool use
- result presentation can remain separate from authority

See [`examples/governed_process_read/README.md`](examples/governed_process_read/README.md).

---

## POC B — Governed file write

### User intent

```text
create a file
```

### Expected contract

1. The request receives a task identity.
2. Lucy resolves the request to a filesystem write capability.
3. Governance recognizes that the operation changes state.
4. Policy determines whether approval is required.
5. Execution is blocked until the required authorization exists.
6. The write is performed through the governed execution boundary.
7. A verifier checks the post-condition.
8. Evidence records the decision and result.

### What this proves

A planner, model, or agent cannot turn a proposal into a machine-side effect merely by producing convincing text.

See [`examples/governed_file_write/README.md`](examples/governed_file_write/README.md).

---

## Evidence standard

A strong Lucy demonstration should be able to show:

| Stage | Example evidence |
|---|---|
| Intent | user request / task ID |
| Resolution | capability selected |
| Governance | risk / policy decision |
| Approval | approval token or ceremony |
| Execution | bounded executor result |
| Verification | post-condition result |
| Evidence | durable correlated record |

---

## What would falsify the POC?

A POC should be considered incomplete if any of these are true:

- an agent can execute directly around governance
- approval is represented only as UI text
- an action is called "verified" without checking the result
- evidence cannot be correlated to the execution
- memory can silently change permission
- task identity is lost before execution
- a mocked path is presented as live machine execution

---

## Public evidence policy

The public repository should contain only evidence that is safe to disclose.

Do not publish:

- secrets
- credentials
- private user data
- machine identifiers that create unnecessary risk
- unpublished security-sensitive implementation details
- proprietary source merely to make a demo look impressive

The goal is reproducibility of the architectural claim, not disclosure of the private core.
