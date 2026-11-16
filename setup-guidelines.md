# Setup guidelines

## Common workflow

1. Clone the organization fork (not necessarily upstream).
2. Check out `benchmark-preparation`.
3. Read `benchmark/README.md` and `benchmark/environment/*`.
4. Run `./benchmark/scripts/check-prerequisites.sh`.
5. Follow upstream or documented Compose/Kind/IIS instructions.
6. Run `./benchmark/scripts/validate-environment.sh` (honest checks; may report partial).
7. Shut down with non-destructive commands (`docker compose down` **without** `-v` unless you intentionally wipe data).

## Per-repository pointers

### ofbiz-enterprise

- Prefer official Gradle/OFBiz docs + `docker/examples/postgres-demo` for Postgres.
- Expect **JDK 25** on current trunk.

### thingsboard-iot

- Follow upstream build docs; use `benchmark/environment/docker-compose.benchmark.yml` for Postgres/Redis (+ Kafka profile) infra only.
- Application jar/war build still required separately.

### yas-microservices

- Primary path: upstream `docker-compose.yml` / `start-yas.sh`.
- Allocate sufficient RAM; first image pull is large.

### ibm-hybrid-modernization

- Use explicit `scripts-docker/docker-compose-*.yml` scripts from upstream mirror docs.
- Treat as incomplete WIP relative to original IBM sample.

### open-data-platform

- Follow Kind standalone path under `deployment/kubernetes/standalone` and repo `Makefile`/`README`.
- Not a docker-compose app.

### dotnet-hrms-stored-procedures

- Requires Windows + IIS + .NET Framework 4.8 + MySQL **and missing SQL artifacts**.
- Do not claim runnable until schema + procedures + config are obtained.

## Security defaults for local lab

- Use synthetic credentials only in `.env` files (never commit secrets).
- Bind services to localhost where possible.
- Do not publish lab endpoints to the public internet.
