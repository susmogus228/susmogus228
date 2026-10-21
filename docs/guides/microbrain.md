# MicroBrain Pocket 0.2.0

Try an experimental Android symbolic agent that stores explicit facts, rules and evidence within a limited persistent budget. You can ask for a rule-based inference or request structured Wikidata research on a topic. The current application and its screenshots use the **Russian locale**. This English guide does not imply an English UI.

## Use the local reasoning and research

Install the project's debug APK on Android 8.0 or newer when you intend to test it. The Pocket package is `org.microbrain.pocket`, separate from the preserved 0.1 application.

In the current Russian command interface, you add a fact, add a rule, then ask an explicit “A is B?” question. The included example identifies a sparrow as a bird and a bird as an animal, then asks whether a sparrow is an animal. You can inspect the inference chain and its retained evidence. No language-model provider or API key is required for this local path.

For research, you supply a topic or Wikidata Q-ID. Pocket reads bounded P31 (instance of) and P279 (subclass of) relations. You can inspect the source journal, pause or resume research, and select network/charging conditions. WorkManager schedules persistent work, while Android controls actual timing. Research waits without suitable network or power conditions; after a force-stop you must open the app again.

## Inspect the memory boundary

The initial persistent brain budget is 1 MiB across facts, rules, chat events, research topics, queue, evidence and one checkpoint. The app and Android runtime sit outside that budget. Current state and checkpoint share the persistent allowance; temporary atomic writes can briefly require extra storage.

The app can request 2, 4 or 8 MiB. Only an explicit approval changes that limit. Without expansion, the agent can forget lower-priority records with their evidence. Export/import and a bounded checkpoint help inspect or restore retained state. Increasing persistent storage does not increase the 1 MiB Active Self boundary.

## Screenshot coverage

1. An explicit fact/rule/question sequence with the inference chain visible.
2. Research topics and a user-supplied Q-ID, showing start/pause/resume state.
3. Source journal: source URL, retained evidence and qualifiers that were skipped.
4. Memory settings: used budget and an expansion request before approval.
5. Export/checkpoint/import controls and their stated storage limits.

Use disposable demonstration state. Mark the screenshots as the current Russian Android UI. A single chat screenshot does not demonstrate background persistence, budget enforcement or restart recovery; those require the corresponding recorded tests.

## Limits

Pocket uses bounded symbolic reasoning, with a chain depth of eight and up to 256 checks. It does not interpret arbitrary article prose or include a general language model inside 1 MiB. Wikidata claims with qualifiers do not become unconditional inference rules. External evidence keeps a source URL and digest; a digest checks retained content integrity rather than truth. A separately enabled manual provider can send the selected chat context to a configured HTTPS service after interface consent; the research worker does not call that provider.

Source: current README, `docs/POCKET_GUIDE.md`, `docs/RESOURCE_SOURCES.md` and `app/build.gradle.kts`, read on 2026-10-21. The source version is 0.2.0. This guide is not a fresh Android execution verdict and does not establish AI novelty.
