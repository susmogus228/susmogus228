# Duplicate Leakage Study 0.1.1

Inspect how copied validation messages can distort a spam classifier's evaluation. The fixed study contains 30 development runs: five split seeds and six conditions using one TF-IDF/logistic-regression pipeline on the historical English UCI SMS Spam Collection.

## Read the result

You can inspect the recorded CSV, split IDs and executed notebook without training a model. The [research evidence page](../../outputs/cli-evidence/research/index.html) recomputes the summary from the 30 existing score rows and displays unchanged copies of the repository's figures.

| Recorded comparison | Mean spam F1 |
|---|---:|
| Random validation | 0.799333 |
| Exact-group validation | 0.796205 |
| Grouped validation with all validation rows copied into training | 0.849876 |

The natural random-minus-grouped mean difference is +0.003127 F1, with negative differences for two seeds. The two methods use different validation memberships, which prevents a causal interpretation. The controlled full-copy minus zero-copy difference averages +0.053671 F1. Full copying is a deliberate positive control; its score is invalid as a generalization estimate. Seed 33 decreases at intermediate copy doses.

For a local figure redraw after installing the locked dependencies, run from the study repository:

```powershell
python -m duplicate_leakage_study --plots-only --output results
```

That documented command redraws the recorded figures. The evidence preparation for this guide only reads CSV and copies existing PNGs; it does not execute training or change results.

## Scope and screenshot coverage

Capture the summary table, positive-control figure with its zoomed axis, natural split comparison, and per-seed differences. Include the actual conditions and the distinction between injected-row fraction and observed group overlap. The evidence page is a presentation of recorded research, not a live model application.

The study measures exact normalized duplicates on one English-heavy corpus. It leaves fuzzy duplicates, paraphrases, Chinese-language performance and deployment drift unmeasured. Five seeds reuse one corpus and do not establish population uncertainty. The 1,115 companion-classifier final-test rows do not enter these development experiments. The project claims neither scientific novelty nor peer review; development was AI-assisted.

Source: current README, fixed protocol, `pyproject.toml` and `results/scores.csv`. Independent recomputation and copied-figure SHA-256 records accompany the evidence page, dated 2026-10-21.
