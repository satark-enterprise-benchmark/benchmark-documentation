# Security guidelines

These environments will eventually support PII/security experiments. Phase 1 rules:

1. **No real customer or employee data.**
2. **No production credentials** in git, issues, or docs.
3. **Never commit** `.env` files with secrets, API tokens, SSH keys, or private certs.
4. Prefer `.env.example` with placeholders.
5. Keep benchmark-only changes under `benchmark/` (and docs repo); do not rewrite upstream business logic.
6. Do not introduce intentionally exploitable vulnerabilities in Phase 1.
7. Preserve upstream licenses and copyright notices.
8. Treat public forks as source mirrors, not as permission to host vulnerable internet-facing demos.
9. For ThingsBoard, respect **BUSL-1.1** production terms.
10. HRMS lacks schema/procs — do not invent procedure bodies for “demo completeness.”

## Future phases

Synthetic PII datasets, ground-truth findings, and remediation demos will be introduced under separate instructions with explicit data-handling controls.
