<p align="center"><img src="https://github.com/user-attachments/assets/7785a8d6-6e28-4892-8958-3daf85414f05" width="80" alt="Bonfÿre knight" /></p>

# Bonfÿre Pipeline

**Native steps and artifacts composed into repeatable operations.**

Teams handling ingestion, transformations, structured checks and reversible handoffs.

## Shared native dependency

The earlier vendored `libbonfyre` source matched
[`bonfyre-core/lib/libbonfyre`](https://github.com/Nickgonzales76017/bonfyre-core/tree/main/lib/libbonfyre)
by exact Git tree SHA. It is now a **pinned source submodule** instead of a
second maintained copy.

```sh
git clone https://github.com/Nickgonzales76017/bonfyre-pipeline.git
cd bonfyre-pipeline
git submodule update --init -- vendor/bonfyre-core
make -C vendor/bonfyre-core/lib/libbonfyre
make -C cmd/bonfyre-pipeline
```

The old include/link paths and native pipeline source are unchanged. The
dependency remains frozen until a separately reviewed gitlink update.

## Source and scope

This repository preserves an **April 2026 source extraction**. It contains `cmd/bonfyre-pipeline/`, vendored core dependencies, and extraction notes. That material remains useful for inspection and for understanding a component boundary, but it is not the latest canonical source or an independently supported package release.

The [current Bonfÿre development lineage](https://github.com/Nickgonzales76017/bonfyre) owns the integrated version: [`cmd/BonfyrePipeline/`](https://github.com/Nickgonzales76017/bonfyre/tree/main/cmd/BonfyrePipeline/). Later source changes are reviewed and published separately from private runtime state.

The older extraction kept temporary vendored dependencies and original migration notes. They are not an additional source of truth; check the [current repository](https://github.com/Nickgonzales76017/bonfyre) for the version, license, operating contract and tests relevant to your use.

## See the work in context

- [Aurekai work samples](https://aurekai-work-samples.pages.dev/) — customer-facing tools and handoffs
- [Bonfÿre developer and product guides](https://docs.aurekai.work/) — integrated operations and technical contexts
- [Client integration examples](https://github.com/Nickgonzales76017/bonfyre/blob/main/docs/client-operations-portfolio.md) — real kinds of receiving-system work

For an **independently scoped native-C example** with its own build and verification fixtures, see [Bonfÿre Statement Import](https://github.com/Nickgonzales76017/bonfyre-statement-import).

The license accompanying this extraction governs its own files; the canonical repo and independent components may have different terms.
