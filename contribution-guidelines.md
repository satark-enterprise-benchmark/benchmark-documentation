# Contribution guidelines

## Scope

Phase 1 contributions should improve **documentation accuracy**, **environment reproducibility**, and **honest readiness reporting**.

## Do

- Update `benchmark/` docs when source inspection finds corrections
- Keep diagrams (`*.mmd`) aligned with verified components
- Add non-secret `.env.example` and infra-only Compose under `benchmark/environment/` when helpful
- Record inaccessible submodules/assets in `repository-metadata.json`

## Do not

- Squash or rewrite upstream history
- Commit secrets or real PII
- Modify Satark AI product code from this organization
- Mark startup verified without a recorded successful run
- Replace missing HRMS SQL with invented procedures without labeling them as synthetic Phase 2 artifacts

## Branching

- Upstream tracking branches remain the fork defaults (`trunk`/`master`/`main`)
- Benchmark additions land on `benchmark-preparation`
- Central docs land on `benchmark-documentation` `main`
