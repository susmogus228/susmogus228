# Publication handoff

## Current state

This package prepares nine repository folders under `outputs/github-staging/`: the `susmogus228` profile repository and eight application/research repositories. It does not push Git commits, create public repositories, upload an avatar or edit account settings. The account was verified as `susmogus228` during preparation.

Review `index.html`, the annotated galleries and the independent English review before publication. The source inventory names the actual local roots and source file hashes. Working state, private uploads, environments, dependency caches, Docker volumes and local configuration remain outside the staging folders.

Proposed native profile settings: display name **Kirill Sotnikov**; bio **Software student exploring data, algorithms and systems. AI-assisted projects with reproducible experiments.**; avatar `assets/avatar/ks-512.png`. Retain the login, email and account security settings.

## Proposed repository names

| Name | Purpose |
|---|---|
| `susmogus228` | GitHub profile README and native image assets |
| `microbrain-pocket` | Current Android symbolic-agent source and debug APK |
| `pitomo` | Pet-store frontend, Python API and database setup |
| `demand-forecast` | Machine-learning/time-series project |
| `route-lab` | Algorithms and closure experiments |
| `unknown-vision` | Image-classification reliability research pilot |
| `reliable-text-classifier` | Duplicate-aware spam classification and local lab |
| `near-duplicate-search` | Exact and MinHash/LSH duplicate audit |
| `duplicate-leakage-study` | Controlled data-leakage study |

Recommended six pinned repositories: `microbrain-pocket`, `pitomo`, `demand-forecast`, `route-lab`, `unknown-vision`, `reliable-text-classifier`. The classifier README and profile table link the two companion text repositories. GitHub supports at most six pins.

## Final publication steps

1. Obtain the user authorization required by their AGENTS.md for Git push and these named public repositories. Existing unrelated repositories remain untouched.
2. Recheck name collisions and authenticated account, then create/push the approved staged repositories. Record remote URLs and commit IDs.
3. Replace the profile's local-preparation note after every linked repository exists. Verify relative image/gallery links on the actual GitHub render.
4. Set the approved public bio if requested; retain the existing login. Pin six repositories through the account UI.
5. Check GIF playback and the static alternatives on GitHub. Do not present a local preview as proof of remote rendering.

The web applications require a local server. No GitHub Pages deployment or paid hosting is included. The MicroBrain debug APK is for local testing; it is not a signed app-store release. Preserve model/data notices and AI-assistance disclosures.

## License decision

The six AI repositories already include MIT licenses. Pitomo and MicroBrain currently have no project LICENSE. Their dependency notices do not license the user's own project. Before presenting those two as freely reusable open-source projects, ask the owner to approve a project license. Do not silently add legal permissions as a formatting change. Source publication itself does not imply that permission.
