# ledger-mirror Guidelines

This repo is the publication layer for append-only, cloneable receipt ledgers.

## Current phase

- scaffold-stage public repo
- workflow and policy baseline exists
- implementation has not landed yet

## What this repo must preserve

- append-only behavior
- deterministic layout
- offline verification
- neutral OSS positioning with no required hosted authority

## Before making changes

1. Read `README.md`, `SECURITY.md`, and `CONTRIBUTING.md`.
2. Inspect existing workflows and repo status.
3. Check whether the change affects ledger layout, checkpoint logic, verification flow, or operator docs.

## Current validation baseline

- `bash .github/scripts/check-baseline.sh`
- `gitleaks dir . --config gitleaks.toml`

## Target validation baseline once implementation lands

- format/lint
- unit tests
- layout and conformance tests
- offline clone-and-verify demo validation

## Repo rules

- Layout changes are contract changes and require explicit documentation.
- Do not introduce network-required verification into the core path.
- Favor deterministic file and directory structures over convenience abstractions.
- Human readability matters, but verifiability matters more.