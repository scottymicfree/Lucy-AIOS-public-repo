# Security Policy

## Reporting a security issue

Please do **not** publish a working governance bypass, credential exposure, sandbox escape, or other sensitive exploit in a public GitHub issue.

For sensitive reports, contact:

**Randy Webb**  
`scottymicfree@gmail.com`

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

- governance bypasses
- approval bypasses
- agent privilege escalation
- context leakage between tasks
- memory influencing authority
- sandbox escape paths
- verifier spoofing
- evidence tampering
- provider-provenance confusion
- unsafe handling of secrets
- ambiguous capability classification

---

## Public-repository note

This repository is primarily architecture and proof material. The canonical Lucy AIOS implementation is private.

A documentation inconsistency can still be security-relevant if it would cause an implementer to weaken a boundary.
