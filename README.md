# TKH Method I — v1.2.1

Reproducible temporal knowledge-hypergraph assessment and its complete offline interactive frontend. This repository preserves the user's selected v1.2.1 scientific implementation. It combines two exact release trees without changing their files:

| Directory | Purpose | Original archive SHA-256 |
|---|---|---|
| `backend/` | Scientific code, pinned dependencies, tests, data, frozen results, assessment reports and evidence | `074ed09f9434d241cc50f61d4c7fcb1019b8c0bc4c6dfd552b0d7e26eaab4ac3` |
| `frontend/` | Offline interactive hypergraph, its sources, matching data, reports and verification tools | `30bad8993466ae9a2fc403def9cd340baa008212ffed0b5ee848333cfe46555b` |

[Exact archive identities](release/source_archives.json), [publication audit](PUBLICATION_AUDIT.md), and [third-party material notice](THIRD_PARTY_NOTICES.md). This is a local release candidate. No GitHub repository, remote, publication or license grant has been created. Publication needs the owner's authorization and resolution of the recorded rights/privacy review items.

## Open the frontend

Open [frontend/START_HERE.html](frontend/START_HERE.html) in a browser, or open [the interactive hypergraph](frontend/interactive/TKH%20Method%20I%20Hypergraph.html) directly. Download or clone the repository first; GitHub's source viewer does not run the explorer.

No installation, server, API key or internet connection is needed. Select 2020, 2022 or 2024. Each snapshot has 12 coarse L0 groups and 48 fine L1 groups. Click a coarse group to inspect its four fine children and their original members. The raw **All data** view has no fitted hierarchy. Diamonds preserve original indexed hyperedges and their incidence multiplicities. See the [frontend instructions](frontend/README.md).

## Verify the pristine release

Run from the repository root before installing or executing anything inside the frozen directories:

```sh
PYTHONDONTWRITEBYTECODE=1 python3 tools/verify_repository.py
PYTHONDONTWRITEBYTECODE=1 python3 backend/tools/verify_package.py
PYTHONDONTWRITEBYTECODE=1 python3 frontend/tools/verify_package.py
PYTHONDONTWRITEBYTECODE=1 python3 frontend/tools/build_frontend.py --check
```

These checks use the standard library and should report success. The repository verifier checks all 5,861 original release files, exact nested membership and manifest hashes. The frontend rebuild comparison is byte-for-byte. Keep `backend/` and `frontend/` pristine; many scientific and report commands intentionally write outputs in their execution tree. Use the separate working copy below.

## Reproduce the scientific assessment

The strict recorded replay environment is **Python 3.12 on macOS arm64**, with all **65 exact dependency pins** in [backend/requirements.lock](backend/requirements.lock). Other platforms are not certified for exact output identity. Installing dependencies may require network access or compatible wheels. After installation, cached scientific replay requires no network, model weights, API key or original full-paper archive. Frozen feature vectors, exact-excerpt inputs and recorded model annotations are necessary replay inputs and remain tracked.

From the repository root, execute the following in order. The three sibling destinations must not already exist; the commands stop rather than overwrite them:

```sh
set -eu
test ! -e ../TKH_Method_I_working
test ! -e ../tkh-env
test ! -e ../tkh-replay
cp -R backend ../TKH_Method_I_working
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

The asset preflight must report no missing or changed inputs. The selected static backend has 201 tests. Replay reconstructs **150 main plus 5 diagnostic fits**, regenerates descriptions/evaluation and compares **930 fitted-artifact references** and deterministic output records. It must report `passed: True` and `difference_count: 0`. Check `results/reproduction/output_comparison.json`, `results/reproduction/clean_run.json` and `work/logs/clean_reproduction.log` in the working copy. Timing and process-log variability is excluded explicitly, not treated as numerical tolerance.

The earlier executed 201-test and 155-fit replay evidence is retained under `backend/docs/illustrated_report_revision/previous_static_release/release/`. New repository-preparation checks are recorded separately in `release/verification.json`; they do not relabel historical scientific runs as new runs.

Optional independent arithmetic checks, from the same working copy:

```sh
../tkh-env/bin/python tools/independent_audit_science.py
../tkh-env/bin/python tools/independent_audit_evaluation.py
```

These are separate audit implementations, not human scientific adjudication. Full neural inference and original-source reacquisition are optional regeneration tasks outside the cached replay contract.

## Rebuild reports and figures

Precompiled documents are included. To rebuild, install TeX Live with `latexmk`, pdfLaTeX and BibTeX and put them on `PATH`. The complete TeX package list and tested engine versions are in [backend/report/README_BUILD.md](backend/report/README_BUILD.md) and [backend/report/build_manifest.json](backend/report/build_manifest.json). From the scientific working copy with the installed environment:

```sh
../tkh-env/bin/python tools/build_report.py
../tkh-env/bin/python tools/export_submission.py
../tkh-env/bin/python tools/build_static_hierarchy.py
../tkh-env/bin/python tools/build_presentation.py
../tkh-env/bin/python tools/check_documents.py
../tkh-env/bin/python tools/check_illustrated_report.py
../tkh-env/bin/python tools/check_publication.py
```

The assessment report remains five pages. The illustrated reading edition has nine pages, including all four distinct source figures. PDF text and numerical parity are the documented portable build contract; PDF binary identity depends on the TeX toolchain. Rebuild only in a working copy, then inspect the rendered output. Do not replace frozen files to make a check pass.

## Rebuild or validate the frontend

Viewing needs only a browser. Rebuilding and data checks use Python's standard library. From the repository root, make a separate frontend working copy:

```sh
test ! -e ../TKH_Method_I_frontend_working
cp -R frontend ../TKH_Method_I_frontend_working
cd ../TKH_Method_I_frontend_working
PYTHONDONTWRITEBYTECODE=1 python3 tools/build_frontend.py
PYTHONDONTWRITEBYTECODE=1 python3 tools/check_frontend.py
```

This rebuilds the exact selected HTML and checks all parent-child memberships, evidence packets, native quotient multiplicities and local links. It does not fit new clusters. The original browser-validation receipts are explicitly historical and correspond to the byte-identical HTML.

## Assessment deliverables

| Deliverable | Location |
|---|---|
| Runnable code, tests and pinned dependencies | `backend/src/`, `backend/tests/`, `backend/requirements.lock` |
| Per-snapshot hierarchy with IDs, levels, parents, members, labels and glosses | `backend/hierarchies/{2020,2022,2024}/hierarchy.json` |
| Birth/merge/split/death and related temporal log | `backend/temporal_events.json` |
| T6 measurements, null comparisons, stability intervals and retrieval results | `backend/metrics.json`, `backend/results/` |
| Five-page assessment report | [TKH M1 Report](backend/report/TKH%20M1%20Report.pdf) |
| Illustrated report with all figures | [Nine-page reading edition](backend/report.pdf) |
| Complete formalism and algorithm | [Formalism](backend/report/TKH%20M1%20Mathematical%20Formalism.pdf), [Algorithm](backend/report/TKH%20M1%20Algorithm.pdf) |
| AI-use disclosure | [Backend AI usage](backend/AI_USAGE.md), [frontend packaging note](frontend/provenance/PACKAGING_NOTE.md) |
| Static visualization | `backend/visualization/` and `backend/report/figures/` |
| Optional interactive companion | `frontend/interactive/TKH Method I Hypergraph.html` |

## Interpretation and publication scope

This preserves v1.2.1, including its negative findings. All measured top-1/5/10/20 recalls in this selected version are zero. Coherence, stability and NLI-based nonsupport are qualified in the report; the NLI quantity is not an expert-adjudicated overclaim rate. Do not substitute later experimental versions' results. Five seeds, exposed questions, partial gold data and unresolved source/identity issues limit the scientific conclusions.

Required reproducibility assets are intentionally tracked even when they are named `cache`, `work` or `generated`. Virtual environments, runtime caches, credentials and scratch output are ignored. The frozen archives' recorded logs and audit history are retained for provenance and may contain the author's name and historical local paths. The source license inventory contains unresolved redistribution information. No project-wide license has been invented. See [PUBLICATION_AUDIT.md](PUBLICATION_AUDIT.md) before any public push.
