# GitHub publication report

Verification snapshot: 2026-10-21T13:27:16.782025+00:00. The owner explicitly approved all nine public repositories, Git push and the prepared profile settings. Pitomo and MicroBrain remain without a project license, as chosen by the owner.

## Published source

| Repository | Verified commit | Hosted CI at this commit |
|---|---|---|
| [route-lab](https://github.com/susmogus228/route-lab) | [`9f48eb1e7209`](https://github.com/susmogus228/route-lab/commit/9f48eb1e720948bc9dacc220a515494bb0977fed) | [success](https://github.com/susmogus228/route-lab/actions/runs/39603217192) |
| [demand-forecast](https://github.com/susmogus228/demand-forecast) | [`352f5c7674ac`](https://github.com/susmogus228/demand-forecast/commit/352f5c7674ac3e999b691e2842fb2120b77c5e68) | [success](https://github.com/susmogus228/demand-forecast/actions/runs/39603257442) |
| [unknown-vision](https://github.com/susmogus228/unknown-vision) | [`7fc066823319`](https://github.com/susmogus228/unknown-vision/commit/7fc066823319cf0754fe80ab9ac7b2ef06990d98) | [success](https://github.com/susmogus228/unknown-vision/actions/runs/39603419253) |
| [reliable-text-classifier](https://github.com/susmogus228/reliable-text-classifier) | [`7c3441d8e027`](https://github.com/susmogus228/reliable-text-classifier/commit/7c3441d8e027e30e376f5411b812f525c297d228) | [success](https://github.com/susmogus228/reliable-text-classifier/actions/runs/39603455220) |
| [near-duplicate-search](https://github.com/susmogus228/near-duplicate-search) | [`99d32f138dc2`](https://github.com/susmogus228/near-duplicate-search/commit/99d32f138dc2a3377ce73b71383d82bde78ae278) | [success](https://github.com/susmogus228/near-duplicate-search/actions/runs/39603491070) |
| [duplicate-leakage-study](https://github.com/susmogus228/duplicate-leakage-study) | [`e30d45208007`](https://github.com/susmogus228/duplicate-leakage-study/commit/e30d4520800763fa47feae067b71984a3aac307d) | [success](https://github.com/susmogus228/duplicate-leakage-study/actions/runs/39603533119) |
| [pitomo](https://github.com/susmogus228/pitomo) | [`dea9b5e5e230`](https://github.com/susmogus228/pitomo/commit/dea9b5e5e23028a2c6d37296214656f5fcef4f77) | [success](https://github.com/susmogus228/pitomo/actions/runs/39607322979) |
| [microbrain-pocket](https://github.com/susmogus228/microbrain-pocket) | [`8df607790665`](https://github.com/susmogus228/microbrain-pocket/commit/8df607790665c3865c4ea7a5a0fd4378ade76c3e) | No workflow configured |
| [susmogus228](https://github.com/susmogus228/susmogus228) | [`ed424a4a0474`](https://github.com/susmogus228/susmogus228/commit/ed424a4a04745b920f232fd49eb80c1a480559e6) | No workflow configured |

All nine repositories were public and their remote heads matched the local publication state at this snapshot. A subsequent profile-documentation commit may include this report; it does not change application source. Original local source checkouts did not receive Git history changes.

## Profile and media

The public [profile](https://github.com/susmogus228) shows Kirill Sotnikov, the approved English bio and KS avatar. Six pins were saved in this order and checked after reload: MicroBrain Pocket, Pitomo, DemandForecast, RouteLab, UnknownVision and Reliable Text Classifier. Login, email, account security and unrelated repositories remain unchanged.

Seven separately generated cover masters have static PNG and animated GIF variants. All seven public profile GIFs loaded at their native width of 1600 pixels. Motion verification decodes 72 frames per six-second loop and checks stationary titles. Native GitHub controls and static links provide motion alternatives. A 390-pixel viewport check showed no horizontal overflow; the temporary viewport override was cleared.

The [eight galleries](GALLERIES.md) contain 70 actual annotated captures. The published UnknownVision gallery was opened on GitHub: all 20 images loaded with their 20 explanations. Each gallery identifies unexercised functions and model limits. Screenshots are presentation evidence rather than a fresh complete application-test verdict.

## Pitomo CI repair

The first hosted run exposed an unavailable Windows Python patch and vulnerable locked dependencies. A subsequent Windows run exposed conflicts with the runner's preinstalled pipx, so Python jobs now create and verify an isolated virtual environment. The repair keeps Python 3.12, hash-checked installation and both audits. Only Pillow and development-only certifi changed versions. Fresh local installs, pip checks and audits passed; Ruff and seven operational tests passed; backend/SQLite/media tests returned 385 passed and 35 PostgreSQL tests deselected. The table above records the separate hosted result, including PostgreSQL, Windows and disposable containers.

The detailed repair report is in [Pitomo](https://github.com/susmogus228/pitomo/blob/main/docs/CI_DEPENDENCY_FIX_2026-10-21.md). Existing local Docker images, databases and volumes were not rebuilt or migrated for this dependency repair.

## Running and licensing

The web applications require their own local Python or Docker backend. No GitHub Pages or permanent backend hosting was configured. MicroBrain includes a downloadable debug APK for local Android testing; this is not an app-store release. Its repository has no hosted workflow, and the profile repository is documentation only.

The six AI repositories retain MIT licenses and their data/model notices. Pitomo and MicroBrain have no project license; public visibility does not grant a general reuse license. Their current UI and legacy documents remain Russian, with English public entry guides.
