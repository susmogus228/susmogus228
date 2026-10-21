# DemandForecast: annotated walkthrough

Current source version: **0.1.1**. Capture date: **2026-10-21**.

Fresh screens cover historical replay, mobile, paired holdout diagnostics, API and custom-history fallbacks. A forecast screen does not prove chronology or leakage prevention; retain the timestamp/split tests and recorded prediction rows. Future-city accuracy and prediction intervals remain unestablished.

[Image hashes and timestamp basis](../screenshot-manifest.json). Captions distinguish current calculation, retained state and recorded research.

## 01. Replay a historical day

Generate 24 hourly predictions from the 2012-11-01 origin. Compare the model, seasonal baseline and observed demand; the displayed day has MAE 31.30.

![Replay a historical day](../../outputs/screenshots/demandforecast/forecast-desktop.jpg)

<sub>1265 × 1284 px · actual browser screenshot · source 0.1.1</sub>

## 02. Read the hourly forecast on mobile

Open the same replay in a narrow browser viewport. The chart and controls remain part of the real local application.

![Read the hourly forecast on mobile](../../outputs/screenshots/demandforecast/forecast-mobile.jpg)

<sub>375 × 812 px · actual browser screenshot · source 0.1.1</sub>

## 03. Judge the entire holdout

Inspect paired errors over 3,488 observed targets. Model MAE is 60.29 versus baseline 64.83; the model still loses in two of five months.

![Judge the entire holdout](../../outputs/screenshots/demandforecast/evaluation-overview.jpg)

<sub>1265 × 712 px · actual browser screenshot · source 0.1.1</sub>

## 04. Locate losses hidden by the mean

Open the final-test monthly/hourly slices. Positive model-minus-baseline error means the model did worse. These comparisons use the same observed targets.

![Locate losses hidden by the mean](../../outputs/screenshots/demandforecast/failure-slices.jpg)

<sub>1265 × 712 px · actual browser screenshot · source 0.1.1</sub>

## 05. Request a forecast from code

Send POST /api/forecast to the running Python service. The response contains 24 real predictions and their input provenance.

![Request a forecast from code](../../outputs/screenshots/demandforecast/api-success.jpg)

<sub>1265 × 712 px · actual browser screenshot · source 0.1.1</sub>

## 06. Disclose missing custom-history lags

Send an explicit empty history array. The API returns HTTP 200, marks custom_history, uses training medians with warnings and leaves actual values null. It does not borrow hidden archive observations.

![Disclose missing custom-history lags](../../outputs/screenshots/demandforecast/custom-history-fallback.jpg)

<sub>1265 × 712 px · actual browser screenshot · source 0.1.1</sub>

## 07. Reject a wrong history type

Send history: null. The API returns HTTP 400 because an explicit history must be an array. This differs from the allowed empty-array fallback.

![Reject a wrong history type](../../outputs/screenshots/demandforecast/api-validation.jpg)

<sub>1265 × 712 px · actual browser screenshot · source 0.1.1</sub>
