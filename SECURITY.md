# Security Policy

## Reporting a security issue

Please do **not** publish a working governance bypass, credential exposure, sandbox escape, specialist-routing bypass, or other sensitive exploit in a public GitHub issue.

For sensitive reports, contact:

**Randy Webb**  
scottymicfree@gmail.com

Include:

- affected component or public contract
- preconditions
- expected behavior
- observed behavior
- reproduction steps
- potential impact
- whether the issue is already public

---

## Scope of interest

Particularly useful reports include:

- E.M.M.A. governance bypasses
- owner-approval bypasses
- stale approval applied to the wrong Run
- Helix becoming an unintended second executor
- raw proposal / browser-payload authority bypasses
- specialist privilege escalation
- hidden Sol-to-Codex state or authority channels
- context leakage between tasks
- memory influencing authority
- Sandbox Broker escape paths
- generic shell authority exposed through Helix
- verifier spoofing
- execution evidence detached from the actual Run
- evidence tampering
- provider/model provenance confusion
- unsafe handling of secrets
- local worktree/path disclosure
- ambiguous capability classification
- Eagle Eye observation gaps around sensitive boundaries

---

## Public-repository note

This repository is primarily architecture and proof material. The canonical Lucy AIOS and Helix implementations are private.

A documentation inconsistency can still be security-relevant if it would cause an implementer to weaken an authority, context, evidence, or verification boundary.

The public repository intentionally avoids publishing machine-specific paths, secrets, credentials, and unnecessary implementation details.
