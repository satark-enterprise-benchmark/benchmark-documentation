# Satark Enterprise Benchmark Documentation

Central documentation for the **satark-enterprise-benchmark** GitHub organization.

This organization hosts six real-world application repositories used as Phase 1 foundation environments for evaluating Satark AI capabilities in:

- Application architecture understanding
- Data-flow discovery
- PII-relevant data surface mapping
- Security analysis readiness
- Future remediation demonstrations (Phase 2+)

## Organization

- **Organization:** [satark-enterprise-benchmark](https://github.com/satark-enterprise-benchmark)
- **Phase:** 1 — acquisition, architecture inspection, environment preparation, standardized documentation
- **Out of scope for Phase 1:** Satark AI product integration, synthetic PII injection, tokenization, remediation demos

## Quick links

| Document | Purpose |
|---|---|
| [organization-overview.md](organization-overview.md) | Why this org exists and how it is structured |
| [benchmark-objectives.md](benchmark-objectives.md) | What Phase 1 and later phases evaluate |
| [repository-catalog.md](repository-catalog.md) | All six application repos + this docs repo |
| [architecture-comparison.md](architecture-comparison.md) | Cross-repo architecture patterns |
| [technology-matrix.md](technology-matrix.md) | Verified languages, DBs, messaging, auth |
| [environment-status.md](environment-status.md) | Honest readiness and startup status |
| [setup-guidelines.md](setup-guidelines.md) | How to operate each environment |
| [security-guidelines.md](security-guidelines.md) | Data-handling and safety rules |
| [contribution-guidelines.md](contribution-guidelines.md) | How to extend Phase 1 artifacts |

## Repositories

| Repository | Pattern | Org URL |
|---|---|---|
| ofbiz-enterprise | Enterprise modular monolith ERP | https://github.com/satark-enterprise-benchmark/ofbiz-enterprise |
| thingsboard-iot | IoT / event-driven platform | https://github.com/satark-enterprise-benchmark/thingsboard-iot |
| yas-microservices | Distributed Spring microservices shop | https://github.com/satark-enterprise-benchmark/yas-microservices |
| ibm-hybrid-modernization | Legacy + Quarkus modernization hybrid | https://github.com/satark-enterprise-benchmark/ibm-hybrid-modernization |
| open-data-platform | Data lakehouse / CDC reference architecture | https://github.com/satark-enterprise-benchmark/open-data-platform |
| dotnet-hrms-stored-procedures | .NET ASMX + MySQL stored procedures | https://github.com/satark-enterprise-benchmark/dotnet-hrms-stored-procedures |

Each application repository contains a `benchmark/` tree on branch `benchmark-preparation`.

## Baseline metadata

Machine-readable acquisition baselines live in [`repository-baselines/`](repository-baselines/).

## Phase status

Phase 1 foundation is **ready for Phase 2 planning**. Application **startup** was not fully verified on the acquisition host for any environment (missing JDK 25 / Maven / .NET Framework IIS / Kind cluster resources as applicable). See [environment-status.md](environment-status.md).
