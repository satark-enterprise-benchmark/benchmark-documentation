# Architecture comparison

## Pattern coverage

These six repositories were selected to cover distinct enterprise architecture shapes that stress different PII-discovery problems.

| Repository | Architecture pattern | Coupling | Primary PII challenge |
|---|---|---|---|
| ofbiz-enterprise | Modular monolith ERP | Shared entity/service catalog | PII woven through shared Party/Order/Accounting entities and services |
| thingsboard-iot | IoT platform (monolith or MSA) | Queue + rule chains | Tenant/customer/user identity across device telemetry and async processors |
| yas-microservices | Microservices + BFF | Network + Kafka/CDC | Distributed ownership, duplicated customer data, CDC fan-out |
| ibm-hybrid-modernization | Legacy + strangler coexistence | Dual DB + Kafka | Customer/order PII on Db2 while catalog modernizes on Postgres |
| open-data-platform | Lakehouse / CDC pipelines | Event + object storage | Historical copies and analytical transformations of source data |
| dotnet-hrms-stored-procedures | ASMX + DB-centric | Stored procedures | Business logic hidden in MySQL procedures (definitions currently missing) |

## Communication styles

| Repository | Sync APIs | Async / streaming | Notes |
|---|---|---|---|
| ofbiz-enterprise | HTTP / OFBiz control / REST-style services | JobSandbox; optional JMS | Entity Engine is the persistence hub |
| thingsboard-iot | REST + WebSocket | MQTT/CoAP/HTTP transports; Kafka optional | Rule Engine is central processing graph |
| yas-microservices | REST via BFFs/services | Kafka + Debezium CDC | Database-per-service on shared Postgres server |
| ibm-hybrid-modernization | JAX-RS on Liberty; Quarkus REST | Kafka product-price events | Nginx front; dual backends |
| open-data-platform | Trino SQL; Airflow ops | Kafka + Debezium CDC; Spark jobs | Kind/K8s standalone; not a single business app |
| dotnet-hrms-stored-procedures | ASMX SOAP/JSON endpoints | None verified | Thin API; DB intended as logic host |

## Data ownership models

1. **Shared schema monolith** — OFBiz entity definitions dominate.
2. **Platform multi-tenant** — ThingsBoard tenant/customer hierarchy.
3. **Service-owned databases** — YAS logical DBs per service.
4. **Dual-store migration** — IBM Db2 + Postgres coexistence.
5. **Pipeline copies** — ODP bronze/silver/gold lakehouse layers.
6. **Procedure-owned logic** — HRMS (blocked without SQL definitions).
