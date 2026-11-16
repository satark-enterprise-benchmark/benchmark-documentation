# Repository catalog

## Application repositories

### 1. ofbiz-enterprise

- **Org URL:** https://github.com/satark-enterprise-benchmark/ofbiz-enterprise
- **Upstream:** https://github.com/apache/ofbiz-framework
- **Default branch:** `trunk`
- **Baseline SHA:** `fe96fcc0dcfa71cc3db87676bc179b11652ae798`
- **Acquisition (UTC):** 2026-11-16T21:10:24Z
- **License:** Apache-2.0
- **Maintained:** Actively maintained upstream
- **Benchmark branch:** `benchmark-preparation`
- **Pattern:** Modular monolith ERP (Entity Engine + Service Engine + Web)

### 2. thingsboard-iot

- **Org URL:** https://github.com/satark-enterprise-benchmark/thingsboard-iot
- **Upstream:** https://github.com/thingsboard/thingsboard
- **Default branch:** `master`
- **Baseline SHA:** `1b7dee3e0b5729cf4d272677ec37c19c9f4bdb69`
- **Acquisition (UTC):** 2026-11-16T21:10:24Z
- **License:** BUSL-1.1 (LICENSE; GitHub API reported NOASSERTION)
- **Maintained:** Actively maintained upstream
- **Benchmark branch:** `benchmark-preparation`
- **Pattern:** IoT platform; monolith or microservices; Rule Engine; device transports

### 3. yas-microservices

- **Org URL:** https://github.com/satark-enterprise-benchmark/yas-microservices
- **Upstream:** https://github.com/nashtech-garage/yas
- **Default branch:** `main`
- **Baseline SHA:** `179e813568c345bad3fce985088b5535e57481aa`
- **Acquisition (UTC):** 2026-11-16T21:10:24Z
- **License:** MIT
- **Maintained:** Available; recent activity in 2026
- **Benchmark branch:** `benchmark-preparation`
- **Pattern:** Spring Boot ecommerce microservices + BFFs + Keycloak + Kafka/CDC

### 4. ibm-hybrid-modernization

- **Org URL:** https://github.com/satark-enterprise-benchmark/ibm-hybrid-modernization
- **Originally requested:** https://github.com/IBM/application-modernization-javaee-quarkus (**404 at acquisition**)
- **Actual fork source:** https://github.com/yeekangc/application-modernization-javaee-quarkus
- **Default branch:** `master`
- **Baseline SHA:** `fba9759fae18697a65d021a97a90a393f7a68625`
- **Acquisition (UTC):** 2026-11-16T21:10:24Z
- **License:** Apache-2.0
- **Maintained:** Incomplete WIP mirror; last push 2020-12-07; official IBM + nheidloff mirrors unavailable
- **Benchmark branch:** `benchmark-preparation`
- **Pattern:** Java EE monolith + Quarkus catalog strangler + Kafka price events

### 5. open-data-platform

- **Org URL:** https://github.com/satark-enterprise-benchmark/open-data-platform
- **Upstream:** https://github.com/MehdiTAZI/open-data-platform-reference-architecture
- **Default branch:** `main`
- **Baseline SHA:** `30591c18e1694ff4e14c6adf161c6df228757412`
- **Acquisition (UTC):** 2026-11-16T21:10:24Z
- **License:** Apache-2.0 (LICENSE in repo; API NOASSERTION)
- **Maintained:** Available reference architecture
- **Benchmark branch:** `benchmark-preparation`
- **Pattern:** Kubernetes lakehouse reference (Kafka/Debezium/Spark/Iceberg/Trino/Airflow/PostgreSQL)

### 6. dotnet-hrms-stored-procedures

- **Org URL:** https://github.com/satark-enterprise-benchmark/dotnet-hrms-stored-procedures
- **Upstream:** https://github.com/SiliconcareDev/hrms-backend
- **Default branch:** `main`
- **Baseline SHA:** `7b01d9f2087f8dd2fa608cb1333ab162bdfbaa0b`
- **Acquisition (UTC):** 2026-11-16T21:10:24Z
- **License:** None declared
- **Maintained:** Available; limited surface (auth ASMX)
- **Benchmark branch:** `benchmark-preparation`
- **Pattern:** .NET Framework 4.8 ASMX + MySQL stored procedures
- **Critical gap:** README references `db.sql`; **no `*.sql` files or procedure definitions present** in upstream/fork

## Documentation repository

- **URL:** https://github.com/satark-enterprise-benchmark/benchmark-documentation
- **Role:** Central catalog, matrices, readiness, baselines, diagrams
