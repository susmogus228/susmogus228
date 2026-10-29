![Kirill Sotnikov: software, data and systems](assets/animated/hero.gif)

[Static hero](assets/static/hero.png) · [All annotated application galleries](docs/GALLERIES.md)

I study software and build experiments around data quality, algorithms and system behavior. I use AI assistance for implementation and documentation, then inspect the resulting code, tests and evidence.

You can explore the source, run the applications on your own machine and inspect their recorded results. The web applications require their Python or Docker server; this profile does not host their backends.

## SleepScope

![SleepScope project cover: illustrated sleep and EEG](assets/static/sleepscope.png)

An EEG sleep-stage research workbench for comparing expert annotations, model predictions and errors across recordings.

Python · scikit-learn · FastAPI · React

**Evaluation limit:** V8 reached 87.59% accuracy on five held-out people from Sleep-EDF and 69.86% on another five from the same cohort. These are not external or clinical validation.

[Source and run instructions](https://github.com/susmogus228/sleep-scope) · [Application screenshots](https://github.com/susmogus228/sleep-scope#explore-the-workbench) · [Research results](https://github.com/susmogus228/sleep-scope#measured-results-at-a-glance)

## HeatTrace

![HeatTrace project cover: satellite and urban surface temperature illustration](assets/static/heattrace.png)

A Wuhan urban heat research workbench comparing Landsat surface-temperature observations, a trained model and its errors.

Python · scikit-learn · satellite imagery · spatial evaluation

**Study limit:** estimates surface temperature for a satellite scene; it is not a live weather service or air-temperature forecast.

[Source and run instructions](https://github.com/susmogus228/heat-trace) · [Application screenshots](https://github.com/susmogus228/heat-trace#explore-the-workbench) · [Results and methodology](https://github.com/susmogus228/heat-trace/blob/main/docs/RESULTS.md)

## SignalWatch

![SignalWatch project cover: sensor-anomaly research illustration](assets/static/signalwatch.png)

A sensor-anomaly research workbench for inspecting detections, false alerts and delay across model versions and baselines.

Python · scikit-learn · time-series analysis · FastAPI

**Evaluation limit:** the active model detected 26 of 28 annotated events in a retrospective audit, with 11.072 false starts per normal hour. False-alert control remains unresolved.

[Source and run instructions](https://github.com/susmogus228/signal-watch) · [Application screenshots](https://github.com/susmogus228/signal-watch/blob/main/docs/SCREENSHOTS.md) · [Research history](https://github.com/susmogus228/signal-watch/blob/main/docs/RESEARCH_LOG.md)

## QueueCraft

![QueueCraft project cover: learned dispatch and scheduling trade-offs](assets/static/queuecraft.svg)

A job-shop scheduling workbench comparing a trained dispatch scorer with heuristic rules and a constraint solver.

Python · scikit-learn · OR-Tools CP-SAT · React

**Evaluation limit:** synthetic test instances do not establish an advantage over every baseline; CP-SAT produced better schedules on the tested small cases.

[Source and run instructions](https://github.com/susmogus228/queue-craft) · [Application screenshots](https://github.com/susmogus228/queue-craft#try-the-workbench) · [Results](https://github.com/susmogus228/queue-craft/blob/main/docs/RESULTS.md)

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
| [sleep-scope](https://github.com/susmogus228/sleep-scope) | [Screens and explanations](https://github.com/susmogus228/sleep-scope#explore-the-workbench) |
| [heat-trace](https://github.com/susmogus228/heat-trace) | [Screens and explanations](https://github.com/susmogus228/heat-trace#explore-the-workbench) |
| [signal-watch](https://github.com/susmogus228/signal-watch) | [Screens and explanations](https://github.com/susmogus228/signal-watch/blob/main/docs/SCREENSHOTS.md) |
| [queue-craft](https://github.com/susmogus228/queue-craft) | [Screens and explanations](https://github.com/susmogus228/queue-craft#try-the-workbench) |
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
