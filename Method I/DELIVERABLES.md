# Assessment deliverable audit — selected v1.2.1

This package supplies all six listed artifact categories, with item 6 implemented as static figures. `report.pdf` is the requested nine-page illustrated edition (five assessment pages plus four figure plates); use `report/TKH M1 Report.pdf` for the strict five-page assessment requirement. It preserves the selected release's scientific evidence and limitations; no improvement in its measured scientific performance is claimed.

| Item | Included artifact | Verification and scope |
|---|---|---|
| 1. Runnable repo/ZIP, README, pins | `src/`, `tests/`, `schemas/`, `configs/`, `README.md`, `requirements.lock` | Exact reproduction commands; 65 version pins; current tests, cache preflight and fresh 155-fit replay indexed in `release/payload_acceptance.json`. Installation and platform limits are explicit. |
| 2. Snapshot hierarchy and event log | `hierarchies/{2020,2022,2024}/hierarchy.json`, `temporal_events.json` | Every cluster has `id`, `level`, `parent_id`, `member_ids`, `label`, `gloss`; IDs/parent containment, disjoint coverage at each level and child unions checked. Direct exports are byte-identical to their authoritative originals. |
| 3. T6 metrics | `metrics.json` | 2,631 schema-validated metric records, including coherence/null comparisons, stability with CIs, over-claim proxy and flat/hierarchical extrinsic scores; raw observations retained. Unavailable is distinct from zero. |
| 4. 3–5-page report | `report/TKH M1 Report.pdf` | Exactly five pages, with formal statement, method/literature, T4 incidence coarsening and figure, evaluation including circularity, limits and a four-week plan. TeX and bibliography included. |
| 5. AI disclosure | `AI_USAGE.md` | Major reconstructed prompts are explicitly labelled; actual recent instruction, AI-assisted work and verification are recorded. No fabricated verbatim history or human validation. |
| 6. Optional static visualization | `visualization/levels_0_1_2.png`, `.svg` | L0/L1 nesting across all three snapshots and explicitly aggregated counts of L2 singletons. No interactive application, dedicated frontend builder or server. |

## Snapshot counts and semantics

| Snapshot | L0 | L1 | L2 original-node singletons | Admitted hyperedges |
|---|---:|---:|---:|---:|
| 2020 | 12 | 48 | 1,424 | 352 |
| 2022 | 12 | 48 | 2,093 | 504 |
| 2024 | 12 | 48 | 4,046 | 912 |

Every selected L0 group has exactly four L1 children; every L2 singleton has exactly one L1 parent. `member_ids` always identify original entities. `parent_id: null` is correct for L0. Persistent IDs and saved parent IDs, not plot colors or construction slot numbers, determine identity.

The temporal log contains **178 events**: 67 births, 82 growth events, 23 continuations, 3 reorganizations, 1 death and 2 merges. **Zero splits were observed** in the selected trajectory; the event schema and temporal implementation support split events. These are partition-ancestry conventions, not claims of scientific discovery or extinction.

## Qualification of T6

- Coherence measurements and the assignment null are present. Evaluator/model separation reduces direct circularity, but shared pretraining and absence of expert semantic ground truth remain.
- Stability CIs are present with their conditional seed-based estimands. They are not population-level scientific uncertainty.
- The over-claim field is populated by an uncalibrated automated NLI nonsupport estimate. Expert-calibrated false-claim assessment is **not available** in v1.2.1.
- Extrinsic scores are present, including negative results. All measured top-1/5/10/20 recalls are zero; larger-budget evidence comparisons do not establish general retrieval superiority.

## Verification trail

`release/deliverables_audit.json` gives schemas, counts and exact alias hashes. `docs/submission_packaging/change_audit.json` lists changes and verifies preservation of scientific trees against the selected original ZIP. `release/payload_acceptance.json` binds the current verification logs to the immutable payload; `PACKAGE_MANIFEST.json` binds the whole archive including that receipt. The original archive hash and its historical receipt remain available under `docs/submission_packaging/original_release/` and `release/archive_policy.json`.

The full formalism and algorithm PDFs are clearly separated supplemental documents. The original interactive application is retained only in the user's untouched original ZIP, not in this submission package.

## All-picture coverage

The illustrated report includes the hierarchy across snapshots (page 6), native coarsening at full size (page 7, also in the assessment on page 2), stability intervals (page 8), and temporal event counts (page 9). These are the four distinct images stored in eight PNG/SVG files. `report/figure_coverage.json` checks that the original PNG pixels are embedded and that the original assessment text is preserved. The source images remain included without modification.
