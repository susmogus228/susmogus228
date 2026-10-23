# Presentation sources

Checked on 2026-10-21. Current local source versions and SHA-256 inventories accompany this package. Dates identify the review, not a guarantee that upstream documentation will remain unchanged.

## GitHub constraints

- [Profile README requirements](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme): a public repository matching the account name, with a nonempty root README.
- [Pinned profile items](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/pinning-items-to-your-profile): up to six repositories or gists. Eight source repositories can exist while the profile pins six selected entries.
- [Non-code files](https://docs.github.com/en/repositories/working-with-files/using-files/working-with-non-code-files): GIF support; SVG scripts and animation do not run in the supported image display.
- [Accessibility settings](https://docs.github.com/en/account-and-profile/how-tos/account-settings/managing-accessibility-settings): animated-image autoplay settings, including system reduced-motion behavior.
- [GitHub CLI reference](https://cli.github.com/manual/): installed CLI 2.96.0; authentication checked without disclosing credentials. This preparation makes no remote write.
- [Large-file limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github): regular Git rejects files larger than 100 MiB; browser uploads have a lower limit. The largest included model is about 37 MB and requires Git/CLI upload, not the browser's 25 MiB upload path.
- [Repository licensing](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository): public visibility and an open-source license are different decisions. The six AI repositories supply MIT files. Pitomo and MicroBrain currently supply no project LICENSE; a user decision remains before claiming reuse permissions for those two projects.

## Animation implementation

The build uses existing FFmpeg 8.1.1 and sharp 0.35.5. [FFmpeg filters](https://ffmpeg.org/ffmpeg-filters.html#palettegen) and [GIF format options](https://ffmpeg.org/ffmpeg-formats.html#gif-2) describe palette generation, palette use and looping. Context7 supplied the matching GitHub CLI and FFmpeg documentation. `MOTION.md` records exact output dimensions, duration and proof boundaries.

## Original cover artwork

Seven image-generation calls produced independent PNG masters for this package: personal hero, MicroBrain Pocket, Pitomo, DemandForecast, RouteLab, UnknownVision and Reliable Text Lab. The generated artwork uses graphite backgrounds, stationary English titles, cobalt accents and geometric project diagrams. It contains no measured performance values or application screenshots. `assets/masters/` retains each full-resolution original; the derived GIF/PNG hashes appear in `motion-verification.json`.

The user approved the earlier graphite/cobalt GitHub-native profile direction. This package retains its stacked covers, restrained English and native Markdown structure. No external stock photos or third-party brand logos enter the cover artwork.

A separate image-generation call produced `assets/avatar/ks.png`, an original KS monogram with a cobalt accent. `AVATAR_PROMPT.txt` retains its full prompt. This file prepares the native account-avatar upload; creating it does not change the GitHub account.

[GitHub's profile reference](https://docs.github.com/en/account-and-profile/reference/profile-reference) requires avatar files below 1 MB and 3000 × 3000 pixels, and recommends about 500 × 500. `assets/avatar/ks-512.png` is a resized PNG for that upload; the original remains unchanged. `avatar-verification.json` records its exact size and hashes.

## IntentProbe cover addition

On 2026-10-23, the user approved a separate static IntentProbe banner generated with the built-in image_gen tool. The existing RouteLab artwork supplied the portfolio style reference. The original 2172 x 724 PNG is included as `assets/static/intentprobe.png`; no resize or animation was applied. Its question-selection diagram is conceptual and contains no measured values. The profile links the project's current screenshot guide and states the synthetic evaluation limit of 84.6% (22/26) no-feasible detection, below the 95% target.

## Uploaded photo demonstration

The upload walkthrough uses [The Blue Marble](https://science.nasa.gov/resource/the-blue-marble/), Apollo 17, AS17-148-22727. Credit: NASA / Johnson Space Center. Downloaded from NASA's image asset endpoint at a requested 1024-pixel size. NASA identifies this as an Apollo photograph; it is a public US government work. Preserve the credit and avoid implying NASA endorsement. The local app reduces the validated input to 512 pixels. The upload tests file handling and inference, not measured benchmark accuracy.

## Project evidence

Each repository keeps its own model, data, dependency and license records. The presentation preserves them. CLI evidence comes from two actual local executions against included synthetic files. The research summary recomputes the existing 30-row CSV and uses three unchanged figures. The screenshot manifest records image hashes and distinguishes capture-log timestamps from file modification times when exact capture metadata was not retained.

Pitomo and MicroBrain current interfaces use Russian. Their English guides describe those existing controls. Source publication does not provide a permanently running backend or prove successful remote CI.
