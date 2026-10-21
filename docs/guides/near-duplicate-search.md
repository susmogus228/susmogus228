# Near-Duplicate Search 0.2.0

Find copied and edited messages across a training file and a test file. You receive matching row IDs, exact word-shingle Jaccard scores and input fingerprints; the audit leaves your input files unchanged.

## Try the included example

Run from the `near-duplicate-search` repository after installing the package with Python 3.11 or newer:

```powershell
python -m near_duplicate_search audit --train examples/train.txt --test examples/test.txt --method exact --threshold 0.6
python -m near_duplicate_search audit --train examples/train.txt --test examples/test.txt --method minhash --threshold 0.6
```

These synthetic examples include a one-word edit: pickup **today** versus pickup **tomorrow**. Their exact word 3-gram Jaccard is 4/6, or 0.667. The audit distinguishes normalized exact matches from other above-threshold pairs. JSON output identifies rows without copying message bodies; optional JSON/CSV file exports support a later review.

The exact method checks every cross-file pair. MinHash/LSH generates candidates, then verifies their original shingle sets with exact Jaccard. Both methods check normalized exact overlap completely. Approximate search can miss qualifying near-duplicate pairs, so an empty report does not certify a clean split. Lexical similarity also does not establish semantic equivalence or quantify model-score inflation.

## Evidence and screenshot coverage

Open [the executed CLI transcript](../../outputs/cli-evidence/near-duplicate-search/index.html). It presents actual stdout from both commands against the included fixtures, with exit codes and input hashes recorded alongside the output. This page presents a CLI tool; it is not a separate application UI.

Capture these distinct points:

1. The synthetic today/tomorrow pair and its calculated 0.667 score.
2. Exact audit summary, returned row pairs and complete-comparison coverage.
3. MinHash candidate counts, verified scores and the approximate-coverage warning.
4. The repository's existing recall, time and memory figures, each with its own caption. Recorded 1,000-document measurements show candidate reduction with comparable or slower total execution; do not label them a proven speedup.

Source: current repository README, public CLI and `pyproject.toml`; local transcript generated on 2026-10-21. Full command arguments, cwd, source input hashes, stdout and stderr appear in `work/cli-evidence/near-provenance.json` and adjacent files.
