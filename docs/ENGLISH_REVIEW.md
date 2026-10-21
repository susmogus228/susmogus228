# Public language and evidence review

Reviewed locally on 2026-10-21. This independent pass checks the current six AI repository trees after `work/english_cleanup.py`, plus the eight project READMEs for presentation boundaries. It does not modify application sources, train models, run full test suites, inspect private configuration or publish files.

## Verdict

**PASS for the six AI repositories' public English prose, with documented source and regression-test exceptions. WARN for any claim that all eight projects have English internal files or an English UI.** Pitomo and MicroBrain Pocket retain Russian source documentation and the current Russian application locale. Their new English guides explain the existing product; they do not translate its interface.

The reviewed six AI source trees can enter an English public source package when its exclusions preserve the existing boundary around `work/`, local data, environments, build output and raw downloaded corpora. Keep originals and owner backups outside that package. This verdict addresses language and evidence presentation, not security certification, remote GitHub rendering, publication or overall product acceptance. This pass did not inspect the final staging tree or archive.

## Eight agreed document corrections

For each row below, the current file matches the cleanup ledger's `after_sha256`; the preserved local original matches its `before_sha256`. The ledger records eight corrections. Original copies remain under `D:/Projects/applied-ai-portfolio/unknown-vision/work/language-audit-2026-10-21/originals/`.

| Current path under `D:/Projects/` | Fresh result |
|---|---|
| `applied-ai-portfolio/unknown-vision/THIRD_PARTY_NOTICES.md` | Line 5 uses `8×8`; the corrupted multiplication sign is gone. |
| `applied-ai-portfolio/unknown-vision/SOURCES.md` | Line 5 uses `8×8`; the source attribution remains. |
| `applied-ai-portfolio/unknown-vision/docs/API.md` | Lines 69 and 82 use `8×8` and `0–7`; the corrupted symbols are gone. |
| `applied-ai-portfolio/unknown-vision/docs/REQUIREMENTS.md` | The source table uses English translations and labels them as translations from Russian. Source IDs and approval boundaries remain explicit. |
| `applied-ai-portfolio/unknown-vision/docs/verification/local-history.json` | JSON parses. The authorization has an English translation and a dated translation note. Every original value other than the translated authorization remains equal to the preserved original. |
| `applied-ai-portfolio/docs/superpowers/plans/2026-10-20-audit-corrections.md` | The authorization excerpt uses an English translation label. |
| `reliable-text-lab/docs/superpowers/plans/2026-10-19-audit-fixes-v2.md` | The authorization excerpt uses an English translation label. |
| `reliable-text-lab/docs/GITHUB_PUBLICATION.md` | The English edition replaces the previous `_RU` filename. It distinguishes local evidence from remote publication and successful GitHub Actions. |

No Cyrillic prose, replacement character `U+FFFD`, or the identified mojibake sequences remain in those eight documents. The parent publication guide and execution plans are preparation records, not mandatory contents of each application repository.

## Fresh six-repository pass

The recursive file pass pruned `.git`, `.venv`, `work`, `outputs`, `dist`, `build`, dependency/build caches, `node_modules`, `.local-data` and package metadata directories. It inspected text source, configuration, docs, CSV metadata, JSON and notebooks. It found no Russian filenames in the six included trees.

| Repository | Text files inspected | JSON/notebook files parsed | Remaining language exception |
|---|---:|---:|---|
| RouteLab | 115 | 65 | None found in the inspected text. |
| DemandForecast | 56 | 12 | None found in the inspected text. |
| UnknownVision | 122 | 36 | Intentional Unicode regression inputs and historical source descriptions. |
| Reliable Text Classifier | 58 | 11 | Original UCI notice encoding and an intentional Chinese regression input. |
| Near-Duplicate Search | 42 | 4 | None found in the inspected text. |
| Duplicate Leakage Study | 37 | 3 | Original UCI notice encoding. |
| **Total** | **430** | **131** | No unexpected Cyrillic prose or identified encoding corruption found. |

The counts reflect this pass's selected text extensions, not every binary resource or image. JSON parsing also covered the two executed notebooks. The pass checks source text and structure; it does not OCR screenshots, review every generated image label or establish browser behavior.

### Preserve these exceptions

- UnknownVision `tests/photo-review.test.cjs:19–20`, `tests/photo-browser.cjs:36–41,84–85`, `tests/history-browser.cjs:12,23,29` and `tests/generate_upload_fixtures.py:16` retain `сова / owl` and `снимок.jpg`. These inputs exercise Unicode corrections, persistence, exports and upload filenames. Their surrounding test descriptions are English.
- Classifier `tests/test_core.py:108` retains `你好` as an unsupported-input regression case. Translating that input would change what the test checks.
- UnknownVision `results/photo-probe-2026-10-20/search.json:118,168` and `search-exact-title.json:118,168` retain source descriptions containing Nahuatl names, IPA and Japanese characters. These are historical retrieval records, not untranslated product prose.
- Classifier and Leakage `docs/UCI-original-readme.txt` remain byte-identical original English notices in legacy encoding. Both SHA-256 values equal `8753cd2d3cab68f80c8257851b8c2037778c267f55accb6fd1b5a2e32d36a84e`. Both repositories' `docs/sources.md:17` promise verbatim preservation. Do not silently re-encode or replace those originals; provide a separate reader-friendly edition if needed.

## Claims a screenshot cannot establish

The following functions and limits come from the current project READMEs and linked guides. A screenshot shows a particular state. Use executable checks, recorded exports or reproduction evidence to support the behavior below.

| Project | Important behavior requiring evidence beyond a screenshot |
|---|---|
| Reliable Text Classifier | Group-separated train/validation/test partitions; vocabulary fitting without test leakage; unsupported-input refusal; the recorded 1114/1115 coverage with 13 wrong predictions; matching API behavior and diagnostic provenance. Verify split IDs, test cases, prediction rows and the actual API contract. |
| Near-Duplicate Search | Complete exact cross-file comparison, deterministic MinHash, candidate verification against original shingle sets, approximate-search misses and source-preserving exports. Use oracle agreement, real CLI JSON/CSV and input hashes. A small example does not establish a general LSH speed advantage. |
| Duplicate Leakage Study | Thirty recorded development runs; exclusion of final-test IDs; controlled injection membership; reproducible per-seed means and honest causal limits. Use the CSV, split and membership records, notebook and checksums. A chart cannot establish scientific novelty, population uncertainty or a causal interpretation of the natural split comparison. |
| DemandForecast | Chronological selection, exact timestamp lags, training-only fallback statistics, custom-history isolation and paired diagnostics over identical observed targets. Verify timestamp/split tests, per-hour predictions, hashes and recomputation; a forecast chart does not establish future-city performance or uncertainty coverage. |
| RouteLab | Optimal route costs, unreachable cases, agreement with an independent oracle, current-map experiments and protection against late imports overwriting newer state. Verify path contracts, solver/oracle checks, async browser tests and exported analyses. A closure map does not prove resilience to simultaneous failures or real-road suitability. |
| UnknownVision | Bounded image decoding, stale-result prevention, explicit local save/delete across restarts, unchanged model predictions after human corrections, and bounded candidate-search failure handling. Use upload/API/storage/browser checks and result manifests. A selected confident mistake or candidate article cannot establish personal-photo recognition reliability or correct object identification. |
| Pitomo 0.14.0 | Account isolation, concurrent cart/stock behavior, guest-cart merge and checkout/reorder retry safety, current-price validation, verified-purchase rules, review visibility and moderation audit integrity. Use backend/database tests and transaction/API evidence. Screenshot language is Russian; payment and delivery integrations remain test/manual behavior as described in the README. |
| MicroBrain Pocket 0.2.0 | Memory-budget enforcement, forgetting with evidence, approval-only expansion, atomic persistence, checkpoint/import limits, bounded inference, background research constraints and recovery after restart. Use JVM/instrumentation tests, measured storage and scheduler/restart records. Screenshot language is Russian; a chat screen does not demonstrate an LLM inside 1 MiB or autonomous understanding of arbitrary articles. |

## Current presentation limits

Pitomo's English guide must retain the test-payment and local-hosting boundaries. The source README and current UI remain Russian. This review does not attest to a fresh shopping session, live payment integration, production deployment or current remote CI.

MicroBrain Pocket's English guide must identify its bounded symbolic inference and structured Wikidata research. The current source README, command examples and UI remain Russian. The persistent brain budget does not include the APK, Android runtime or scheduler database; no language model inside 1 MiB is claimed. This review does not execute the Android application or refresh previous device tests.

The six AI projects retain their documented scope. In particular, UnknownVision's locally verified implementation does not establish complete product acceptance or useful arbitrary personal-photo recognition. English cleanup and screenshots do not close those separate questions.

The CLI transcript and research evidence pages are labeled presentations of actual executed output and recorded measurements. They are not invented graphical applications. Root owns their browser rendering, final gallery coverage, staging exclusions and GitHub publication checks.
