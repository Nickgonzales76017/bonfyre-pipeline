# bonfyre-pipeline

Unified pipeline entry repo for Bonfyre.

This repo is a public entry vector for the single-process pipeline surface:

- gate
- ingest
- hash
- index
- compress
- meter
- stitch
- ledger

## Why This Exists

The live `BonfyrePipeline` runtime currently lives in:

- `/Users/nickgonzales/Projects/bonfyre-oss/cmd/BonfyrePipeline`

This repo gives that surface its own clear entry point so the Bonfyre page can link to it directly.

## Current Layout

- `cmd/bonfyre-pipeline/`
  - extracted pipeline binary source
- `vendor/bonfyre-core/lib/libbonfyre/`
  - temporary local dependency slice for extraction validation
- `docs/`
  - extraction notes

## Dependency Note

This repo currently vendors only the minimum `bonfyre-core` dependency surface needed to build locally:

- `lib/libbonfyre`

That is a migration convenience, not the long-term dependency model.
