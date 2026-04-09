# Migration Batch 1

This is the first extraction batch for `bonfyre-pipeline`.

## Goal

Move the live `BonfyrePipeline` binary into its own public-facing repo while keeping its core dependency boundary explicit.

## Batch Contents

### 1. `BonfyrePipeline`

Current source:

- `/Users/nickgonzales/Projects/bonfyre-oss/cmd/BonfyrePipeline`

Target:

- `cmd/bonfyre-pipeline/`

### 2. `libbonfyre` dependency slice

Current source:

- `/Users/nickgonzales/Projects/bonfyre-core/lib/libbonfyre`

Target:

- `vendor/bonfyre-core/lib/libbonfyre/`

## Acceptance Criteria

1. the pipeline binary builds from its extracted path
2. the local vendored `libbonfyre` builds
3. the repo can serve as a clean backlink target from the live Bonfyre page

## Progress

- imported:
  - `BonfyrePipeline`
  - vendored `libbonfyre` dependency slice
- verification:
  - vendored `libbonfyre` builds locally
  - `bonfyre-pipeline` builds from the extracted path
  - usage surface runs from the extracted binary
