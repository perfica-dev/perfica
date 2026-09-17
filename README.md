# LoopCoder

**Downloads and updates live here.** → **[Releases](https://github.com/UezarDev/LoopCoder/releases)**

This repository holds nothing but LoopCoder's installers and the metadata the app reads to find out
that a newer one exists. There is no source code here. The source is developed privately, and every
file in this repository is published by an automated release workflow from a version tag.

## What is LoopCoder

A desktop app for building multi-agent coding workflows as **rings** rather than DAGs. Agents are
seated on a circular track and hand work to their neighbour; a ring runs until it converges or trips
a circuit breaker, and rings nest — a security checker that finds a vulnerability routes into a
sub-ring that fixes it, then returns to the parent where it left off.

## Installing

Take the newest release and the file for your platform:

| Platform | File | Notes |
|---|---|---|
| Windows | `LoopCoder-Setup-<version>.exe` | x64 |
| macOS | `LoopCoder-<version>-{x64,arm64}.dmg` | Apple Silicon and Intel builds are separate |
| Linux | `LoopCoder-<version>-{x86_64,arm64}.AppImage` | `chmod +x` it, then run it |

### These builds are not code-signed

Nothing here carries a code-signing certificate yet, and you should know what that means before you
run it:

- **Windows** shows *"Windows protected your PC"*. Getting past it is *More info* → *Run anyway*.
- **macOS** is blocked by Gatekeeper. Additionally, **an unsigned macOS app cannot update itself** —
  the updater refuses to install over one. On macOS, updating means downloading the new release by
  hand until this changes.
- **Linux** AppImages have no platform signing requirement and just run.

Every download's SHA-512 is recorded in the `latest*.yml` file beside it, and the app checks that
hash before installing an update, so the downloads are integrity-checked even though they are not
signed.

## The files that are not installers

`latest.yml`, `latest-mac.yml` and `latest-linux.yml` are the update feed. An installed copy fetches
the one for its platform, compares the version with its own, and offers the update. They are not
useful to download by hand; deleting one from a release breaks updates for everyone already on that
platform.

## Issues

Bug reports and feature requests are welcome in this repository's issue tracker. Pull requests are
not — there is no source here to change.

## Licence

LoopCoder is proprietary software, © 2026 UezarDev. See [LICENSE](LICENSE). Downloading a release
does not grant any rights over the source code.
