# Environment status

Statuses use only: **Completed**, **Partial**, **Blocked**, **Not started**.

## Readiness table

| Repository | Forked | Inspected | Structure ready | Environment configured | Startup verified |
|---|---|---|---|---|---|
| ofbiz-enterprise | Completed | Completed | Completed | Partial | Not started |
| thingsboard-iot | Completed | Completed | Completed | Partial | Not started |
| yas-microservices | Completed | Completed | Completed | Partial | Not started |
| ibm-hybrid-modernization | Completed | Completed | Completed | Partial | Not started |
| open-data-platform | Completed | Completed | Completed | Partial | Not started |
| dotnet-hrms-stored-procedures | Completed | Completed | Completed | Blocked | Blocked |

## Why startup is not Completed

Acquisition host lacked a verified full run for each stack:

| Repository | Primary blocker for startup verification |
|---|---|
| ofbiz-enterprise | Trunk requires **JDK 25**; not present on acquisition host |
| thingsboard-iot | Needs **JDK 25 + Maven 3.9.x**; heavy build; optional Kafka/Cassandra |
| yas-microservices | Full compose needs **≥16GB RAM** and long first boot; not run end-to-end |
| ibm-hybrid-modernization | Multi-compose Db2 (privileged) + Liberty + Quarkus; aged Quarkus 1.1; not run |
| open-data-platform | Requires **Kind/Kubernetes** standalone bring-up; not executed |
| dotnet-hrms-stored-procedures | **Missing `db.sql` / stored procedures / Web.config**; runtime blocked |

## Docker Compose availability

| Repository | Upstream Compose | Benchmark Compose added |
|---|---|---|
| ofbiz-enterprise | Yes (`docker/examples/postgres-demo`) | No (reuse upstream) |
| thingsboard-iot | No suitable root prod compose | Yes — infra-only `benchmark/environment/docker-compose.benchmark.yml` |
| yas-microservices | Yes (`docker-compose.yml` + profiles) | No (reuse upstream) |
| ibm-hybrid-modernization | Yes (multiple `scripts-docker/docker-compose-*.yml`) | No (reuse upstream; avoid ambiguous root compose) |
| open-data-platform | No (Kind/K8s) | No (not practical as simple Compose) |
| dotnet-hrms-stored-procedures | No | No (blocked without DB artifacts; Windows/IIS native) |

## Standardized scripts

Each app repo exposes:

```bash
./benchmark/scripts/check-prerequisites.sh
./benchmark/scripts/environment-info.sh
./benchmark/scripts/validate-environment.sh
```

on branch `benchmark-preparation`.

## Soft validation performed on acquisition host (2026-11-16)

| Check | Result |
|---|---|
| Docker Engine | Available (29.8.0) |
| Java / JDK 25 | Missing |
| Maven | Missing |
| Kind | Missing |
| `docker compose config` on YAS `docker-compose.yml` | OK |
| `docker compose config` on ThingsBoard `benchmark/environment/docker-compose.benchmark.yml` | OK |
| Full stack `up` + app health | Not started |

