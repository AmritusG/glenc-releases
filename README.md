# GlEnc — Releases

Native macOS multi-format video encoder for Resolume Arena workflows.

This repository hosts signed, notarized DMG releases of GlEnc.
The source code is private. Bug reports and feature requests are welcome via the [Issues tab](../../issues).

## Download

Latest release: **[Releases page](../../releases/latest)** — GlEnc 1.7.1 (the loop-off preview with sound stops at the end; a faster build).

All previous versions are available on the [Releases tab](../../releases).

## What it is

A fast macOS encoder that converts video into the formats VJs actually deliver. Drop in
any source — DXV, HAP, ProRes, H.264, HEVC, MJPEG, or anything macOS can decode — and
encode it to:

- **DXV3** — DXT1, DXT5, YCG6, and YG10 (the Resolume-native codecs, including alpha)
- **HAP** — Hap1, Hap5, HapY, and HapM (HAP + alpha)
- **ProRes** — 422, 422 HQ, 422 LT, 422 Proxy, and 4444 (with alpha)
- **H.264** and **HEVC** — broad delivery in `.mp4` or `.mov`
- **Motion JPEG**

Audio is carried through, resampled, or stripped per job, with per-job trim, resize, and
crop. Built for VJs and content creators who prep clips for Resolume Arena daily.

Since 1.7.0 GlEnc is built in Rust on the same core as Glance and CueGlance: the same window,
menus and settings as 1.6.2, and DXV / HAP files byte for byte the ones 1.6.2 writes (HAP Q
sources aside: see the 1.7.0 notes).

## Installing

1. Download the latest `.dmg`
2. Double-click to mount
3. Drag `GlEnc.app` into your Applications folder
4. First launch: macOS verifies the signature and notarization (~2 seconds), then opens

## Verifying the download

Each release includes a `.sha256` checksum file. To confirm the DMG is intact:

    shasum -a 256 GlEnc-vX.Y.Z.dmg

Compare the output against the `GlEnc-vX.Y.Z.dmg.sha256` file in the release.

## Requirements

- macOS 14 (Sonoma) or later
- Apple Silicon or Intel (universal since 1.7.0)

## Known issues

Open known issues are listed in the [Issues tab](../../issues) and in each release's notes.

## Reporting issues

Please open an [Issue](../../issues) with:

- macOS version (`sw_vers`)
- GlEnc version (visible in the About menu)
- Steps to reproduce
- Screenshot or screen recording if visual

## License

GlEnc binaries are distributed for personal and commercial use.
