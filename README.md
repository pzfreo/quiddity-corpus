# quiddity-corpus

STEP test corpora shared by [quiddity-rust](https://github.com/pzfreo/quiddity-rust) and [specify-core-rust](https://github.com/pzfreo/specify-core-rust). Consumers pin a commit of this repository and check the files' digests: quiddity-rust's `tests/fixtures/corpus.json` and `tests/corpus_files.rs`.

These files were split out of [pzfreo/quiddity](https://github.com/pzfreo/quiddity)'s `tests/corpus`, with history kept, when the Python implementation was retired in favour of the Rust one. Their content is identical to `tests/corpus` at quiddity commit `6d544e0`, the revision quiddity-rust's CI pinned.

| Directory | What it is |
|---|---|
| `nist` | NIST MBE PMI test cases (AP203 geometry-only variants) |
| `mfcadpp`, `mfcadpp_holdout`, `mfcadpp_regressions`, `inventory_refusal` | MFCAD++ models (CC BY) |
| `cadgenbench_inputs` | CADGenBench public editing inputs (ODC-BY) |
| `cadgenbench` | Generated CADGenBench submissions (Apache-2.0) |
| `ttt_inputs` | Too Tall Toby / build123d sheet-metal hanger (Apache-2.0 reference) |
| `gramel` | The author's own turned parts (Apache-2.0) |

Each set carries its own terms; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). Nothing here is part of any published package.
