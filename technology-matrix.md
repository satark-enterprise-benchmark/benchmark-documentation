# Technology matrix

Values below are **verified from source inspection** at acquisition baseline. Entries marked *claimed but not implemented* are called out explicitly.

| Repository | Language(s) | Architecture | Database | Messaging | Auth / identity | Main focus |
|---|---|---|---|---|---|---|
| ofbiz-enterprise | Java, Groovy, FreeMarker, XML | Enterprise modular monolith | H2 default; PostgreSQL / MySQL supported | Optional JMS; JobSandbox | OFBiz security / login entities; Shiro/ESAPI/JWT present | Enterprise workflows & shared PII entities |
| thingsboard-iot | Java; TypeScript/Angular UI | IoT modular monolith / optional MSA | PostgreSQL required; Timescale/Cassandra/Redis optional | In-memory default; Kafka optional; MQTT/CoAP/HTTP/LwM2M/SNMP | Tenant/customer/user model; JWT-style API security in platform | Async IoT + rule-engine data flow |
| yas-microservices | Java 25; TypeScript/Next.js | Microservices + BFF | PostgreSQL (DB-per-service); Redis; Elasticsearch optional | Kafka + Kafka Connect + Debezium CDC | Keycloak | Distributed PII across shop services |
| ibm-hybrid-modernization | Java EE/Jakarta; Quarkus 1.1; Dojo JS | Hybrid modernization / strangler | IBM Db2 `orderdb`; PostgreSQL catalog | Kafka (aged Strimzi/Kafka 2.5) | App-level customer model (Liberty); incomplete mirror | Legacy+modern coexistence |
| open-data-platform | Python, YAML, Shell, HCL, SQL | Data engineering lakehouse reference | PostgreSQL 18.6; Iceberg via Polaris/Garage | Kafka 4.3.1 + Debezium 3.6.1 | Platform/ops oriented (K8s) | CDC / lineage / analytical copies |
| dotnet-hrms-stored-procedures | C#; ASMX; .NET Framework 4.8 | Database-driven ASMX service | MySQL (client present; **schema/procs absent**) | None verified | Custom JWT + CSRF + bcrypt login | Stored-procedure PII tracing (**blocked**) |

## Additional verified notes

- **dbt** is mentioned in ODP marketing/docs intent but **not implemented** in the acquired tree.
- **ThingsBoard** production license is **BUSL-1.1** (not Apache-only for current major line).
- **IBM official repo** was unavailable; fork source is `yeekangc/...` WIP mirror.
- **HRMS** has **zero `*.sql` files**; only call sites `sp_Get_EmployeeForLogin` and `sp_Insert_AuditLog`.
