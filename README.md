![Kirill Sotnikov: software, data and systems](assets/animated/hero.gif)

[Static hero](assets/static/hero.png) · [All annotated application galleries](docs/GALLERIES.md)

I study software and build experiments around data quality, algorithms and system behavior. I use AI assistance for implementation and documentation, then inspect the resulting code, tests and evidence.

You can explore the source, run the applications on your own machine and inspect their recorded results. The web applications require their Python or Docker server; this profile does not host their backends.

## IntentProbe

![IntentProbe project cover](assets/static/intentprobe.png)

A machine-learning experiment that selects clarification questions before recommending a project, with explicit constraint checks and outcomes for insufficient information.

Python · scikit-learn · FastAPI · React

**Evaluation limit:** no-feasible detection reached **84.6% (22/26)** on a synthetic audit, below the 95% target. This is not overall model accuracy or evidence of usefulness for real users.

[Source and run instructions](https://github.com/susmogus228/intent-probe) · [Application walkthrough](https://github.com/susmogus228/intent-probe/blob/main/docs/images/README.md) · [Static cover](assets/static/intentprobe.png)

## MicroBrain Pocket

![MicroBrain Pocket project cover](assets/animated/microbrain.gif)

An Android symbolic agent with explicit facts, source evidence and a bounded persistent store.

Kotlin · Jetpack Compose · WorkManager

[Source and run instructions](https://github.com/susmogus228/microbrain-pocket) · [Application walkthrough](docs/galleries/microbrain.md) · [Static cover](assets/static/microbrain.png)

## Pitomo

![Pitomo project cover](assets/animated/pitomo.gif)

A pet-store application with a React storefront, Python API and PostgreSQL transactions.

React / TypeScript · FastAPI · PostgreSQL

[Source and run instructions](https://github.com/susmogus228/pitomo) · [Application walkthrough](docs/galleries/pitomo.md) · [Static cover](assets/static/pitomo.png)

## DemandForecast

![DemandForecast project cover](assets/animated/demand.gif)

An hourly-demand experiment with chronological evaluation and comparisons against a seasonal baseline.

Python · scikit-learn · time-series evaluation

[Source and run instructions](https://github.com/susmogus228/demand-forecast) · [Application walkthrough](docs/galleries/demandforecast.md) · [Static cover](assets/static/demand.png)

## RouteLab

![RouteLab project cover](assets/animated/route.gif)

A weighted-grid laboratory for optimal paths and the consequences of closing a crossing.

Python · A* / Dijkstra · resilience experiments

[Source and run instructions](https://github.com/susmogus228/route-lab) · [Application walkthrough](docs/galleries/routelab.md) · [Static cover](assets/static/route.png)

## UnknownVision

![UnknownVision project cover](assets/animated/vision.gif)

An image-classification reliability pilot: confident errors, unfamiliar inputs and human review.

ONNX Runtime · open-set detection · local Python API

[Source and run instructions](https://github.com/susmogus228/unknown-vision) · [Application walkthrough](docs/galleries/unknownvision.md) · [Static cover](assets/static/vision.png)

## Reliable Text Lab

![Reliable Text Lab project cover](assets/animated/text.gif)

Three connected repositories: spam classification, duplicate-search algorithms and a controlled leakage study.

Python · TF-IDF / SVM · MinHash / LSH · reproducible research

[Source and run instructions](https://github.com/susmogus228/reliable-text-classifier) · [Application walkthrough](docs/galleries/reliable-text.md) · [Static cover](assets/static/text.png)

## Repositories and current limits

| Repository | Explore |
|---|---|
| [intent-probe](https://github.com/susmogus228/intent-probe) | [Screens and explanations](https://github.com/susmogus228/intent-probe/blob/main/docs/images/README.md) |
| [route-lab](https://github.com/susmogus228/route-lab) | [Screens and explanations](docs/galleries/routelab.md) |
| [demand-forecast](https://github.com/susmogus228/demand-forecast) | [Screens and explanations](docs/galleries/demandforecast.md) |
| [unknown-vision](https://github.com/susmogus228/unknown-vision) | [Screens and explanations](docs/galleries/unknownvision.md) |
| [reliable-text-classifier](https://github.com/susmogus228/reliable-text-classifier) | [Screens and explanations](docs/galleries/reliable-text.md) |
| [near-duplicate-search](https://github.com/susmogus228/near-duplicate-search) | [Screens and explanations](docs/galleries/near-duplicate-search.md) |
| [duplicate-leakage-study](https://github.com/susmogus228/duplicate-leakage-study) | [Screens and explanations](docs/galleries/duplicate-leakage-study.md) |
| [pitomo](https://github.com/susmogus228/pitomo) | [Screens and explanations](docs/galleries/pitomo.md) |
| [microbrain-pocket](https://github.com/susmogus228/microbrain-pocket) | [Screens and explanations](docs/galleries/microbrain.md) |

Follow each repository's README to run it locally. Published source does not provide a permanently running backend.

Pitomo and MicroBrain currently use a Russian interface; their English guides explain the controls. The AI projects use English. UnknownVision exposes substantial reliability failures on larger photos, so its gallery includes unsuccessful results. The generated banners illustrate project themes and contain no measured results.

[Motion / accessibility](docs/MOTION.md) · [Sources](docs/SOURCES.md) · [Coverage and language review](docs/ENGLISH_REVIEW.md)
