# Benchmark objectives

## Phase 1 (this phase) — Foundation

Evaluate and document whether Satark (and engineers) can:

1. Acquire and preserve real enterprise codebases
2. Correctly identify architecture patterns and technology stacks
3. Map databases, APIs, messaging, and async paths from source evidence
4. Produce reproducible environment setup guidance
5. Distinguish runnable stacks from incomplete / blocked stacks

**Not in Phase 1:** product integration, tokenization, synthetic vulnerability insertion, remediation demos, AI agents.

## Phase 2+ (future)

Expected follow-ons (separate instructions):

- Synthetic PII scenarios and ground-truth findings
- Remediation architecture designs
- Satark AI end-to-end demonstrations against these environments

## Per-repository evaluation focus

| Repository | Primary evaluation focus |
|---|---|
| ofbiz-enterprise | Complex enterprise business logic; PII across shared entities/services |
| thingsboard-iot | PII / identity movement through async IoT pipelines and rule engine |
| yas-microservices | Distributed PII ownership, duplication, cross-service events/CDC |
| ibm-hybrid-modernization | Dual-store coexistence during modernization; legacy+modern PII surfaces |
| open-data-platform | PII propagation through CDC, lakehouse, analytics, historical copies |
| dotnet-hrms-stored-procedures | API → C# → stored procedure → MySQL dependency understanding |

## Success criteria for Phase 1

- [x] Organization exists and is accessible
- [x] Six forks acquired with upstream history preserved
- [x] Standardized `benchmark/` structure populated from source inspection
- [x] Central documentation and comparison matrices published
- [x] Environment readiness reported honestly
- [ ] Full application startup verified on a prepared host (deferred — host toolchain gaps)
