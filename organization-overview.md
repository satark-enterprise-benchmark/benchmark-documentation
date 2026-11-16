# Organization overview

## Purpose

`satark-enterprise-benchmark` is a dedicated GitHub organization for enterprise application architecture and PII security benchmark environments. It isolates benchmark forks from Satark product repositories and preserves upstream attribution via GitHub forks.

## Design principles

1. **Preserve upstream truth** — forks keep history, licenses, tags, and parent relationships.
2. **Benchmark-only additions** — documentation and helper scripts live under `benchmark/` on `benchmark-preparation`.
3. **No silent simplification** — do not replace upstream apps with toy implementations.
4. **Honest readiness** — never mark startup as verified without evidence.
5. **Synthetic data only (future)** — Phase 1 does not inject PII scenarios; later phases must use synthetic data only.

## Structure

- Six forked application repositories (benchmark subjects)
- One documentation repository (this repo)
- Per-app `benchmark/` documentation, diagrams, and validation scripts
- Central comparison matrices and readiness reports here

## Access model

Organization created 2026-11-16. Public repos for transparency of open-source forks. Do not expose vulnerable or credentialed deployments publicly in later phases.
