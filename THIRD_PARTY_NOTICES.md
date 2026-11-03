# Third-party notices

The test corpora in this repository were split out of the Python implementation's `tests/corpus` (pzfreo/quiddity-python, then named pzfreo/quiddity; history kept) so that the Rust quiddity (then quiddity-rust) and specify-core can pin them independently of it. These notices are carried over from the Python implementation's THIRD_PARTY_NOTICES.md.

## Vendored test corpora

Most of the STEP models in this repository are third-party geometry redistributed here so
that this project's tests run against parts it did not author. They are **not** part of the
sdist and the wheel packages only `src/quiddity` — and they carry their own terms,
which the Apache-2.0 licence of this project does not alter.

`gramel` is one exception: it is the author's own part, under this project's own licence, and needs
no third-party notice. It is vendored for the same reason the others are — the two third-party
corpora are milled prismatic parts and contain no turned geometry at all, so the turned
families had no real part behind them.

### Generated CADGenBench submissions (`cadgenbench`)

These are another exception: two generated build123d outputs from the author's Apache-2.0
CADGenBench harness, included under this project's Apache-2.0 licence. They are not copies
of benchmark reference drawings or third-party reference STEP models. The directory README
records the submission identities and SHA-256 hashes. They are excluded from published
packages along with the rest of `tests/corpus`.

### CADGenBench public editing inputs (`cadgenbench_inputs`)

- Source: <https://huggingface.co/datasets/HuggingAI4Engineering/cadgenbench-data>
- Licence: Open Data Commons Attribution (ODC-BY)
- Attribution: CADGenBench by HuggingAI4Engineering; underlying CAD geometry sourced from Mecado
- Files: unmodified `202/input.step` (gzip compressed), `203/input.step`, `207/input.step`,
  and `241/input.step`.
  The directory README records SHA-256 hashes of the original STEP bytes. No held-out
  ground-truth geometry is included.

### NIST MBE PMI test cases (`nist`)

- Source: <https://www.nist.gov/ctl/mbe-pmi-validation-and-conformance-testing-project/mbe-pmi-0>
- Files: ten of the eleven AP203 geometry-only variants — `ctc_01`–`ctc_05` and `ftc_06`–`ftc_10`.
  `ftc_11` is not vendored because no test reads it.
- Terms: NIST states the models "can be used without any restrictions" and requests
  acknowledgement, which this notice provides. NIST further states that such use "does not
  imply a recommendation or endorsement by NIST".

### MFCAD++ (`mfcadpp`)

- Source: <https://doi.org/10.17034/d1fec5a0-8c10-4630-b02e-b92dc81df823>
- Licence: Creative Commons Attribution (**CC BY** — the source record states no version)
- Modifications: none. The files are byte-identical to the upstream distribution.
- Copyright: Queen's University Belfast and the dataset's authors
- Contents: a forty-model subset of the *test* split; `mfcadpp/MANIFEST.json`
  records the rule that selected it

As CC BY requires, the dataset is attributed to its authors and its paper cited:

> Colligan AR, Robinson TR, Nolan DC, Hua Y, Cao W. *Hierarchical CADNet: Learning from B-Reps
> for Machining Feature Recognition.* Computer-Aided Design, 147:103226, 2022.

### Too Tall Toby / build123d sheet-metal hanger (`ttt_inputs`)

- Source: <https://build123d.readthedocs.io/en/latest/tttt.html>, 23-02-02 SM Hanger.
- Reference implementation: Gumyr, copyright 2023, Apache License 2.0.
- Drawing: Too Tall Toby, provided to the build123d tutorials.
- Modification: geometry-only STEP export generated with build123d 0.11.0 for this regression.

### MFCAD++ subsets (`mfcadpp_holdout`, `mfcadpp_regressions`, `inventory_refusal`)

Further MFCAD++ models, identified by their dataset file numbers. They are under the same CC BY terms and attribution as `mfcadpp` above. `mfcadpp_holdout` is a held-out set, `mfcadpp_regressions` holds regression cases (its MANIFEST.json records why each is included), and `inventory_refusal` holds invalid or open inputs (gzip-compressed).

### The author's own parts (`gramel`)

Paul Fremantle's own models, under the Apache-2.0 licence of the quiddity projects.
