# TKH Method I v1.2.1 — static final-submission package

This is the user's selected **v1.2.1** implementation, repackaged on 12 October 2026 to match the six assessment deliverables. The numerical backend, frozen configuration, input data, fitted hierarchies and scientific results are unchanged. Later v1.3.0 and subsequent retrieval experiments are not included. The original archive is identified by SHA-256 `d09b3b10263327437fdc9a385fc9cea375c4471c6724f80d081178bd1fd21d10`.

**For the assessed 3–5-page submission, use [the five-page assessment report](report/TKH%20M1%20Report.pdf).** The requested [illustrated reading edition](report.pdf) has **nine pages: the same five assessment pages plus four full-size landscape figure plates**. It includes every distinct picture from `visualization/` and `report/figures/`; PNG/SVG pairs are alternate formats, not separate pictures. See [DELIVERABLES.md](DELIVERABLES.md) for all submission items. `START_HERE.html` is an optional pre-rendered reader with local links and complete member lists; it uses no JavaScript or server. There is no interactive application in this submission.

## Deliverable paths

| Required item | Entry point |
|---|---|
| Runnable repository ZIP and pinned dependencies | `src/`, `tests/`, `configs/`, `schemas/`, `requirements.lock` (65 exact pins) |
| Hierarchy per snapshot | `hierarchies/2020/hierarchy.json`, `hierarchies/2022/hierarchy.json`, `hierarchies/2024/hierarchy.json` |
| Temporal log | `temporal_events.json` |
| T6 measurements | `metrics.json`; original observations and confidence intervals under `results/` |
| Five-page assessment report | `report/TKH M1 Report.pdf`; editable source `report/TKH M1 Report.tex` |
| Illustrated report with every figure | `report.pdf` (nine pages); canonical source `report/TKH M1 Illustrated Report.tex` |
| Full formalism and algorithm (supplements) | `report/TKH M1 Mathematical Formalism.pdf`, `report/TKH M1 Algorithm.pdf`, and editable TeX |
| AI usage | `AI_USAGE.md` (major reconstructed examples labelled honestly, actual recent instruction, work and verification scope) |
| Optional static visualization | `visualization/levels_0_1_2.png` and `.svg` |

The short-path JSON files and `report.pdf` (the illustrated report) are exact byte copies, with source paths and SHA-256 values in `release/deliverables_audit.json`. Cluster IDs, original member IDs, labels, glosses and parent IDs are not replaced. L0 = coarse, L1 = fine, L2 = original singletons. Each selected L0 has four L1 children. Colors/slots in the static figure are local display choices, not persistent identity; the JSON and temporal log contain that identity.

## Exact reproduction steps

Supported strict replay: **Python 3.12 on macOS arm64**, using all versions in `requirements.lock`. The pins and cached inputs do not establish universal Linux/Windows or cross-architecture byte equality. Installation can require network access or compatible wheels. Scientific cached replay needs no network, model weights, API key or full-paper archive. Full neural inference and source reacquisition are outside this cached-replay contract.

After extracting the ZIP, open a terminal in `TKH_Method_I_Submission/`. Verify it **before** installation or execution (the verifier uses the standard library):

```bash
PYTHONDONTWRITEBYTECODE=1 python3.12 tools/verify_package.py
```

Successful output includes `passed: true`. Preserve that extraction. The execution commands write logs, build metadata and some results into their working root. Make a separate working copy and environment; the three destinations below must not already exist:

```bash
set -eu
test ! -e ../TKH_Method_I_working
test ! -e ../tkh-env
test ! -e ../tkh-replay
cp -R . ../TKH_Method_I_working
cd ../TKH_Method_I_working
python3.12 -m venv ../tkh-env
../tkh-env/bin/python -m pip install -r requirements.lock
../tkh-env/bin/python -m pip install --no-deps --no-build-isolation .
export PYTHONDONTWRITEBYTECODE=1
export OMP_NUM_THREADS=1
export OPENBLAS_NUM_THREADS=1
export MKL_NUM_THREADS=1
export PYTHONPATH="$PWD/src"
../tkh-env/bin/python -m pip check
../tkh-env/bin/python tools/preflight_assets.py
../tkh-env/bin/python -m pytest -q -p no:cacheprovider
../tkh-env/bin/python tools/replay_assessment.py --target ../tkh-replay
```

Execute the commands in order and stop if any fails. The fresh replay excludes saved final fits, metrics and reports. It reconstructs **150 main + 5 diagnostic fits** from the declared inputs, regenerates labels/evaluation, and compares **930 fit-artifact references**, selected hierarchy/ancestry records and deterministic metric bytes. Success prints `passed: True`, `difference_count: 0`. Inspect `results/reproduction/output_comparison.json`, `results/reproduction/clean_run.json` and `work/logs/clean_reproduction.log` in the working copy. Timing, timestamps and process logs are volatile exclusions, not metric tolerances. The original shipped scientific results remain in the pristine extraction.

The current package's `release/payload_acceptance.json` indexes the executed document checks and explicitly links the prior static release's 201-test and fresh 155-fit cached-replay evidence under `docs/illustrated_report_revision/previous_static_release/`. Those scientific runs were not repeated for this document-only revision. The existing environment was reused; no new dependency installation is claimed. The selected release's earlier installation receipt is retained under `docs/submission_packaging/original_release/release/payload_acceptance.json`.

Optional independent arithmetic checks (in the working copy) recompute quantities from submitted records using separate audit code; they are AI-authored checks, not independent human review:

```bash
../tkh-env/bin/python tools/independent_audit_science.py
../tkh-env/bin/python tools/independent_audit_evaluation.py
```

## Rebuild the report and static deliverables

The supplied PDFs are ready to read. Rebuilding additionally requires TeX Live with `latexmk`, pdfLaTeX and BibTeX on `PATH`; the actual tested versions are in `report/build_manifest.json`. See `report/README_BUILD.md` for the LaTeX package list. In the working copy:

```bash
../tkh-env/bin/python tools/build_report.py
../tkh-env/bin/python tools/export_submission.py
../tkh-env/bin/python tools/build_static_hierarchy.py
../tkh-env/bin/python tools/build_presentation.py
../tkh-env/bin/python tools/check_documents.py
../tkh-env/bin/python tools/check_illustrated_report.py
../tkh-env/bin/python tools/check_publication.py
```

These commands use the saved v1.2.1 results in the working copy. To inspect fresh replay outputs, use the complete comparison record or copy a result into a separate analysis location; do not overwrite the certified extraction. The report builder exports numbers from saved measurements, compiles the three assessment documents plus the illustrated report, and checks that the assessment report is exactly five pages and the illustrated report exactly nine pages. `export_submission.py` refreshes the convenient aliases after a build. PDF text/numeric parity is supported; PDF bytes can vary by TeX toolchain. Rebuilding invalidates the old package manifest in the working copy by design. Verify the original extraction, not a modified execution tree, against the shipped manifest.

## Scientific interpretation

Artifact completeness is not proof of retrieval improvement. In this selected v1.2.1 release, all measured top-1/5/10/20 recalls are zero. A larger inspection-budget evidence comparison is reported with its four-question, exposed-test and partial-gold limitations. Do not substitute later versions' results.

Coherence uses MPNet withheld from fitting against a size/evaluability-preserving assignment null, while construction uses MiniLM. Shared pretraining and lack of expert domain truth remain circularity risks. Stability intervals are conditional on five optimizer trajectories. The reported over-claim quantity is an **uncalibrated automated NLI nonsupport proxy**, not an expert-adjudicated error rate. No human validation is invented to meet a deliverable label.

The five-page report contains the formal statement (Deliverable 0), literature positioning, T4 native coarsening and an actual figure, evaluation/circularity discussion, negative results and a four-week research plan. The 39-page mathematical formalism and 26-page algorithm are supplements, not the page-limited report. Their prior interactive-traversal descriptions document the selected release's data interface; the application itself is excluded. Historical reviews, old receipts and original packaging instructions under `docs/` are evidence, not current commands or certification of this package.

No external submission has been made.

## Figure-integration revision

This is a document-only revision of the verified static submission ZIP with SHA-256 `87ad308d83643880840f08acb00965a35bae84e0abec9d665cb3349da156338c`. The backend, scientific results, source images and original five-page report are preserved. Current figure coverage/pixel checks and PDF layout review are recorded in `report/figure_coverage.json` and `report/layout_validation.json`. The earlier 201-test and 155-fit replay evidence is retained and inherited only for byte-identical scientific files; it is not presented as a new scientific run.
