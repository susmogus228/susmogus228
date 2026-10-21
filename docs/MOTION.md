# Banner motion

Seven independently generated PNG masters are kept in `assets/masters/`. They are immutable source artwork. The generator creates a 1600-pixel-wide PNG fallback and a separate animated GIF for each banner. The master files retain their original full resolution.

These are decorative illustrations of each project's topic. Their paths, pulses, charts and highlights do not represent application execution, measurements, model confidence or live traffic.

## GitHub compatibility

GitHub supports GIF images in repository files and Markdown. A README cannot run an animation library or arbitrary JavaScript. Scripted or animated SVG is not a dependable substitute for a GIF in GitHub's sanitized image pipeline.

Use a repository-relative GIF reference, for example:

```markdown
![RouteLab: algorithm experiments](assets/animated/route.gif)
```

Also provide an explicit still-image link, for example `[Static banner](assets/static/route.png)`. Readers can use GitHub's **Settings → Accessibility → Autoplay animated images** control. A README image cannot enforce a CSS `prefers-reduced-motion` media query itself. Prefer the PNG as the default for a motion-free profile; link the GIF as an optional animated version. GitHub's treatment of a specific uploaded README must be checked after publication.

Official references checked for this implementation:

- [Working with non-code files](https://docs.github.com/en/repositories/working-with-files/using-files/working-with-non-code-files)
- [Managing accessibility settings](https://docs.github.com/en/account-and-profile/how-tos/account-settings/managing-accessibility-settings)
- [FFmpeg palettegen and paletteuse filters](https://ffmpeg.org/ffmpeg-filters.html#palettegen)
- [FFmpeg GIF encoder](https://ffmpeg.org/ffmpeg-formats.html#gif-2)

## Motion design

| Banner | Motion on existing artwork |
| --- | --- |
| Hero | Signal traces along the systems cube and existing network connections |
| MicroBrain Pocket | Memory layer outline and pulses at connected memory nodes |
| Pitomo | Product-to-cart-to-order transit along the existing arrows |
| DemandForecast | A highlight follows the illustrated forecast segment |
| RouteLab | Successive segments highlight the route drawn across the grid |
| UnknownVision | Review brackets and the connection to the secondary image |
| Reliable Text Lab | Document line, fingerprint comparison and dataset split connection |

The titles and subtitles remain still. Each loop contains 72 frames, nominally 12 fps, over six seconds. GIF time uses hundredths of a second, so encoded frame delays alternate between 80 and 90 ms. There is no full-image zoom, flashing background, camera motion or moving text. Highlights are limited to the illustration region. Node pulse functions and dash offsets are periodic for a continuous loop.

## Reproduction

The build uses the existing `sharp` installation and FFmpeg, without installing dependencies. `scripts/render-motion.cjs` records the exact output hashes and verifies that master hashes remain unchanged.

```powershell
& 'C:\Users\s.kirill\.cache\codex-runtimes\codex-primary-runtime\dependencies\node\bin\node.exe' scripts/render-motion.cjs
```

On another computer, make `sharp` resolvable and update its require path in the script. FFmpeg must be on `PATH`. Temporary PNG frames and decoded proof frames go under `work/motion/`, not the public assets directory. A single palette is generated across the full sequence with `stats_mode=diff`; Bayer dithering and rectangle updates keep GIF size bounded and static pixels stable.

## Verification

`motion-verification.json` contains dimensions, file sizes, duration, frame count, loop metadata and SHA-256 hashes for all outputs. The generator decodes the finished GIF and compares frames 0 and 36: every pixel in the protected title region must remain identical, while pixels in the illustration region must differ. It also rejects a file larger than 3 MiB or a duration/frame count other than six seconds / 72 frames. Run `scripts/verify-motion.cjs` afterward to decode all 72 frames: the title crop must have one identical hash across the sequence, while full frames must have at least 36 distinct hashes. All seven final GIFs have 72 distinct decoded frames and a single unchanged title-region hash.

This proves the files contain animation and the protected titles stay frozen across all decoded frames. It does not substitute for checking the final published README, the account's autoplay preference or every browser's GIF timing.
