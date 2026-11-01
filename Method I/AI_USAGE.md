# AI usage and provenance — final unified release

Codex substantially authored and revised the code, tests, mathematical prose, reports, interactive explorer, static reader and release tooling. The exact conversational backend revision is not asserted. This closure used filesystem/shell tools, Python/NumPy/SciPy/Numba/PyTorch, pytest, pinned local model assets where needed, Matplotlib, pdfLaTeX/BibTeX/latexmk, PDF rendering/text extraction and browser inspection. Historical PDFs used ReportLab; the current three documents are actual LaTeX builds. No subagents, human raters, paid model API calls, third-party messages, deployment or external submission are claimed.

## Work surfaces and evidence boundaries

- Codex: production inspection, targeted implementation, real commands/tests, model-cache validation, report/frontend generation and packaging. Actual scope is supported by receipts and logs.
- ChatGPT Chat / GPT review: mathematical explanation and AI-assisted review of supplied artifacts. This is not independent human peer review.
- ChatGPT Work: the historical operator guide assigns scoped source/document assistance through explicit handoffs. That intended role does not prove every Work action occurred.
- Applicant: determines scope, reviews outputs and decides whether/when to submit. This does not imply personal execution of every AI-produced step.

There is no assumed automatic cross-chat file sharing. The guide's “Close Sxx” convention is a human instruction, not a software command. No private unrelated conversation history is bundled.

## Models, inference and exposure

`work/model_acquisition.json` records pinned revisions. MiniLM provides surface-form construction and retrieval vectors; MPNet is held out of fitting and measures coherence/description alignment; the NLI cross-encoder classifies exact source/claim pairs. None is fine-tuned. The v5 labeller is deterministic lexical/extractive code, not a hidden generative prompt. Its sole-substantive-member wording and independent verified-source predicate extend the preceding v4 exact-frequency correction.

Current inference/reuse accounting is generated from exact old/new input identities in `results/revision_preservation_final.json`. The author campaign may generate required new MPNet text-list caches using pinned local assets. Exact NLI premise/hypothesis outputs are reused only after matching identity. Recipient cached replay consumes frozen vectors/annotations and does not claim fresh neural inference or complete original-paper extraction. Existing model/source acquisition timings remain historical. The new code/run identities and 155-condition membership comparison are explicit.

All benchmark questions/answers were exposed before final scoring; they are diagnostic, not an untouched blind test. No human ratings, expert calibration, unseen benchmark, prospective preregistration, global optimum or universally meaningful taxonomy is invented. Some original workflow receipts were retrospective and remain labelled historical. Negative retrieval, limited coverage and uncalibrated NLI outcomes remain in the reports. Recorded installation, cached replay, independent arithmetic, report compilation and artifact checks are separate evidence categories.

## Representative prompts — retrospective reconstructions

These ten prompts are retrospective reconstructions of the task stages and verification standards, not a verbatim execution transcript. Actual execution is evidenced separately by the supplied code, input/output identities, command logs, and test results.

## RP01 — Establish the actual task, sources, and acceptance boundary

```text
I need you to establish the actual assessment contract before writing code. Work on
Option A only and inspect the supplied brief, article metadata, hypergraph, questions,
and answer key. Report your actual project directory, all relevant input paths and
hashes, and any missing or inconsistent files. Preserve original bytes and IDs.

Map P1–P6, T1–T7, Deliverable 0, the report page limit, and AI-use requirements to
specific outputs and acceptance tests. Distinguish the original task from historical
plans and conversational suggestions. Do not infer a gold scientific taxonomy from
the answer key, invent a deadline, introduce another corpus, fine-tune a model, build
an interactive application, or submit anything externally.

Create a scoped evidence ledger and an explicit plan with prerequisites, outputs,
and pending verification states. Mark the supplied questions as exposed. Codex is
the production writer; export review handoffs for Chat and source/document tasks for
Work without assuming shared access. A planned test is not a passed test. Return the
requirements map, input inventory, risks, and the first safe implementation stage.
```

## RP02 — Audit records and construct defensible temporal snapshots

```text
Implement the data and chronology layer from the actual Option A records. Preserve
distinct assertion IDs even when endpoint sets coincide. Audit node/edge types,
arity, degrees, repeated IDs, endpoint validity, provenance, and the different date
fields. Distinguish origin date, source availability, and ingestion rather than
using a convenient year indiscriminately.

Implement the chosen nodes-first eligible snapshot policy with explicit endpoint
checks for admitted edges. Use the recorded conservative availability intervals and
retain every quarantine/unresolved decision with its reason. Do not silently rename
candidate conflations or fabricate missing source text. Names, source occurrences,
export-attributed assertions, and source-entailment judgments must remain distinct.

Produce the three declared primary snapshots and their actual counts, node order,
source coverage, and digests. Test date boundaries, uncertain intervals, dangling
references, isolated nodes, future-record noninterference, and preservation of raw
IDs. Construct only permitted surface-form encoder inputs under the declared policy.
Keep external evaluation information outside this layer and return inspectable
code, examples, and test logs before proceeding to numerical fitting.
```

## RP03 — Implement and independently verify the mathematical kernels

```text
Implement TKH Method I's actual per-level criterion:
J=(1-alpha)S+alpha F+beta T. Use weighted Euclidean within-cluster distortion,
original-arity-normalized native connectivity (lambda_e-1)/(r_e-1), and optimal
one-to-one common-node overlap disagreement. Keep reference relation balancing and
general positive-mass support explicit. Do not normalize arithmetic centroids into
a different fitting loss or replace original arities by coarse occupancies.

Build the original incidence interface, multiplicity-preserving quotient, full
objective oracle, matching adapter, and legal single-node deltas. Distinguish the
edge-by-cluster storage orientation from the mathematical S-transpose times B form.
Preserve internal edges, duplicate-support record identities, evidence references,
and direct-versus-staged coarsening.

Write an independently expressed numerical checker, not two wrappers around the
same function. Test unequal masses, singleton edges, empty persistent sets, newly
admitted nodes, forbidden empty-cluster moves, coincident endpoint sets, partial
collapse, and a correctly scoped pair-projection counterexample. Enumerate tiny
matching/partition examples where feasible. Return derivations, actual tests and
limits; passing finite cases is not a global-optimality theorem.
```

## RP04 — Construct the real hierarchy and fixed-matching local solver

```text
Build the implemented 12 / up-to-48 / singleton hierarchy. Fit the coarse partition
first, then hold it fixed while refining up to four nonempty children inside each
parent. Keep all original edges in the child-level structural score, including
cross-parent edges. Use the actual semantic and incidence initializers with explicit
count repair; score only completely assigned states.

Implement seeded feasible single-node sweeps over maintained endpoint counts and
semantic moments. At each sweep start obtain an optimal temporal matching, hold it
fixed for candidate gains, and recompute the full rematched objective at the boundary.
Verify the fixed-surrogate delta sum, sweep-boundary nonincrease, quotient counts,
moments, and parent constraints with explicit errors. Keep random-stream consumption,
move tolerance, maximum sweeps and stop reasons in the run record.

Return only the stationarity claim the algorithm actually supports. A capped run is
not converged, and sequential level fitting is not global hierarchy optimization.
Test repeatability, empty-source rejection, stale matching, invalid vectors and
shared-edge updates. Preserve the production/checking distinction and expose a
small genuine smoke command without substituting it for real corpus execution.
```

## RP05 — Add chronological trajectories, persistent identity, and locality

```text
Implement the chronological sequence using each run's actual preceding output.
Align persistent raw node IDs, initialize newcomers from current eligible numerical
information, and repair the complete hierarchy before scoring. Keep warm-start
memory separate from the explicit beta penalty and provide a warm beta-zero control.
Never use a future snapshot or another variant's predecessor to initialize a run.

After fitting, compute reporting identity and full many-to-many ancestry from the
declared common-count/Jaccard/containment rule, including the identical-singleton
exception. These reporting thresholds must not enter the optimization matching.
Retain full overlaps and clearly label births, retirements, splits, merges, and
growth as partition conventions rather than scientific discovery or extinction.

Define and measure the actual source-change and effective-input-change locality
regions, including global weight-normalizer effects; report empty denominators as
unavailable. Test additions, removals, tiny clusters, crossed memberships, parent
changes, deterministic identity handling, and temporal prefix consistency. Store
immutable predecessor references and return a reviewable real sequence as well as
synthetic edge cases. Do not manufacture meaningful continuity from renamed IDs.
```

## RP06 — Freeze development, execute controls, and retain negative results

```text
Establish the actual coefficient-selection protocol before using final evaluators.
Use the construction-side alpha development and the declared synthetic nuisance/
changed-truth beta calibration. Keep final MPNet scores, judged labels, retrieval
targets, and answer text outside selection. Preserve all candidates, criteria, and
selected values rather than keeping only the winner.

Execute the complete registered matrix: 75 base conditions, 45 paired current-edge
perturbations, 15 uniform-weight conditions, and 15 warm beta-zero controls, plus
five separately identified latest-view diagnostics. Do not count the selected
trajectory twice. Retain the same node universe after edge removal and use the
specified unperturbed predecessor in the conditional perturbation experiment.

For every real fit, record data/vector/config/code identities, masks, named streams,
predecessor references, objective components, quotas, stop status and measured work.
Verify immutable reuse rather than silently recomputing under the same ID. Negative
coherence, imbalance, cap exits, or retrieval results are not reasons to edit the
protocol. Return the complete manifests and actual execution logs, separating cached
reuse, physical computation, development, and final measured conditions.
```

## RP07 — Generate supported descriptions without fabricating cluster meaning

```text
Implement a versioned deterministic description layer on frozen fitted memberships.
Use only permitted member names/types, construction-vector representatives, and
eligible bundled source windows. Generate lexical theme candidates from the declared
snapshot vocabulary, but require the final exact original-name member threshold,
including its explicit small-population rule, and actual dated source support.
Stop-word removal must not create a second exact occurrence that the original name
never contained.

Describe mixed and bibliography-dominated groups honestly. Keep source-sentence
quotations attributed, bounded, and connected to exact evidence IDs and field spans.
Do not create a hand-written twelve-topic taxonomy, use evaluation vectors to choose
labels, or infer causality, superiority, or universality from shared membership.
Evidence-limited fallbacks must remain visible rather than be counted as success.

Preserve complete packets, ranking/coverage diagnostics and the previous description
baseline. Independently recompute member/source checks and validate thresholds rather
than trusting generator flags. Separate quotation occurrence, NLI classification,
and description informativeness. Freeze actual final text before its evaluation and
regenerate only valid input-matched caches. Return all outputs, including awkward
or weak cases, with the policy version and provenance of every asserted sentence.
```

## RP08 — Evaluate independently and account for actual retrieval work

```text
Run the declared independent evaluation without sending its results back into fitting
or description selection. Compute MPNet coherence with exact evaluable populations,
macro and pair-weighted names intact, and the registered assignment null that retains
hierarchy/size constraints. Report all seeds and actual uncertainty assumptions.
Measure current-edge perturbation agreement separately from genuine cross-snapshot
agreement, excluding trivial singleton agreement from success claims.

Evaluate the actual description population using exact support checks, lexical
coverage, paired description alignment, and the frozen NLI instrument. State claim
and sampling denominators and never call a model nonsupport fraction scientific
falsehood. Use real model metadata for class order, and never invent human ratings.

Implement gold-free retrieval requests, shared pre-routing target/candidate eligibility,
explicit node/evidence answer units and deduplication, fixed beams and threshold,
and every registered inspection budget. Record routing and vector-scoring work
separately. Preserve the February-2026 scope and unavailable primary cells instead
of backdating answers. Report top-k failures and any qualified budget benefit together.
Return raw observations, independent arithmetic checks, intervals, and exposed-test
limitations; no cherry-picked metric may replace the registered endpoint.
```

## RP09 — Resolve the final audit and produce source-faithful LaTeX reports

```text
Read the final TKH Method I review and inspect every cited active source range before
editing. Correct the exact-theme-frequency mismatch and its independent validator,
make the small-population exception explicit, and add the adversarial regression
cases. Preserve the numerical method, inputs, selected coefficients and observed
negative outcomes. Address package membership verification, effective-input wording,
report parity, and honest reproducibility scope without suppressing failures.

Finalize code versions before rebuilding run identities. Because the code manifest
covers the package and schemas, do not attach new code to old execution hashes.
Execute the required frozen-input fits and downstream annotation/evaluation pipeline,
verify membership preservation, and regenerate any genuinely changed model-input
caches. Record actual reuse and inference separately.

Create a canonical validated JSON-to-TeX data exporter. Compile a 3–5-page main report
and a separately detailed technical supplement, with all symbols, losses, matching,
coarsening, update formulas, guarantees, complexity, estimands, real tables and limits
explicit. Keep the actual bibliography and one report build path. Inspect every PDF
page, resolve citations and layout defects, and produce machine-readable evidence
for each correction. Do not declare submission readiness while a required gate is
pending or while a new artifact exists only as a plan.
```

## RP10 — Seal one complete archive and preserve honest AI provenance

```text
Prepare one recipient-facing TKH Method I archive from the final accepted payload.
Include the complete backend, tests, schemas, fixed configuration, original and cached
required inputs, exact evidence/judge packets, active outputs, LaTeX sources/PDFs,
static reviewer pages, build tools, and scoped acceptance records. Preserve relative
paths; include current HTML explicitly despite the old global HTML exclusion. Do not
build an interactive app or include secrets, environments, font binaries, private
chat history, stale ZIPs, or optional large model/paper caches as hidden prerequisites.

Use exact-member manifests and negative tests for extra/missing/changed/unsafe files.
Bind a fresh recipient-style installation, test, replay and report-build receipt to
an immutable payload manifest, then include that receipt in the final package manifest.
Avoid circular self-hashes. Extract the final ZIP again, verify all bytes and links,
and report its real full SHA-256, byte size, supported environment and remaining
scientific limitations. Do not submit externally without my separate instruction.

Update AI_USAGE.md truthfully: retain recorded prompts, separate these ten reconstructed
representative examples from historical transcripts, describe Codex/Chat/Work roles
with evidence limits, and record actual modifications and verification. Do not invent
backend versions, timestamps, human reviewers, preregistration, or successful commands.
Return the single archive and a final gate table with real evidence, not a success slogan.
```

## Final errata and interactive integration — 11 October 2026

Codex read the supplied final audit narratives and JSON evidence, reconciled all 5,403 inventory rows and 9,645 line-numbered source-browser lines with the named preceding ZIP, implemented FR01–FR05, and rebuilt the existing interactive explorer from the final backend artifacts. The explorer layout is reused only as a display aid; all scientific content and its input hashes are regenerated. Additional tests, actual cached assessment runs, independent artifact/field checks and browser/PDF inspection are recorded in the current internal acceptance receipt. No new model inference, Linux run, human raters, subagents or external submission are claimed for this patch. Historical Linux comparison failures remain preserved. Representative prompt examples above remain retrospective reconstructions, not verbatim execution history.

## Hierarchy navigation and document consolidation — 11 October 2026

Codex added snapshot-specific L0-to-L1 traversal using saved parent IDs, complete original-member lists and child/entity links; it consolidated the full mathematical foundations and technical supplement, prepared a separate algorithm document and retained an exactly five-page report. It updated current documentation from policy v4 to the implemented v5 and portability contract v2. Pandoc converted supplied source material into editable LaTeX; TeX Live compiled PDFs and Poppler rendered pages for inspection. The mathematical expressions and technical supplement were retained; source changes affect presentation/tools/tests/documentation, not the backend numerical modules, frozen configuration, input arrays or fitted results. The current acceptance receipt states the actual verification and cached replay scope. No new model inference, Linux run, subagents, independent human certification or external submission is claimed. Reconstructed prompt examples above remain expressly retrospective, not verbatim execution history.

## Static submission packaging — 12 October 2026

Actual user instruction (verbatim excerpt):

> I am gonna stick to this version for the final submission make sure all the deliverables are there

The user selected `TKH_Method_I_Unified_v1.2.1_Hierarchy_20261011_d09b3b102633.zip` and provided the six-deliverable assessment list, including:

> Optional: a static visualisation of levels 0-2 across snapshots (a screenshot is enough). Do not build an interactive frontend.

Codex audited that archive and prepared a separate static submission package. It removed the interactive application and its dedicated builders/test, added byte-identical conveniently named exports of selected hierarchies, metrics and temporal events, created a static hierarchy figure, clarified reproduction in a working copy, and corrected presentation-only report wording. The numerical backend, schemas, frozen configurations, original data, cached inputs and scientific result tree are preserved. Historical mentions of the interactive work above and in supplemental documents describe the earlier release; no interactive application is delivered here. Later v1.3.0 and follow-up scientific experiments were not merged into this selected v1.2.1 release.

Verification is recorded in `release/payload_acceptance.json` and `release/acceptance_logs/`: archive/content hashes, hierarchy/metric schema and membership checks, dependency versions, tests, fresh cached scientific replay, independent arithmetic, PDF compilation/layout and static links/fields. The interpreter is a reused pinned environment, not a newly installed environment. The original release's fresh-install receipt is retained as historical evidence. Cached replay does not constitute new neural inference, new evidence acquisition, expert validation or a blind retrieval test. Major reconstructed prompts above remain explicitly reconstructed; no missing historical transcript is invented. No external submission was made.

## Illustrated report integration — 12 October 2026

Actual user instruction (verbatim):

> Put all the pictures in visualisation and figure(in the report folder)  folders in the report pdf  cleanly. Where is the final ZIP file saved? Give me its full path and a working download link.

Codex inventoried eight PNG/SVG files representing four distinct pictures. It added a nine-page illustrated edition: the unchanged five assessment pages followed by four landscape figure plates with source-specific captions and the existing scientific limitations. The five-page assessment report remains separately available for the assessment page limit. Codex updated the reproducible document builders, alias/export checks, figure pixel-coverage verification, reader links and archive manifests; rendered and inspected the new pages; and verified preservation of the scientific payload. The prior 201 tests and exact 155-fit cached replay remain prior evidence for unchanged science, not newly executed experiments. No new inference, data acquisition, expert validation or interactive frontend was added.
