# Perfica

**Loops of AI agents that build your app, and finish it.**

**Download:** [perfica.dev](https://perfica.dev) · **[Releases](https://github.com/perfica-dev/perfica/releases)** · **Docs:** [perfica.dev/docs](https://perfica.dev/docs/)

Perfica is a desktop app for Windows, macOS and Linux. Loops of AI agents plan, build, review and test
an app on your own machine, then hand it over with a finish report and a live preview. You bring your
own model keys, and the agents work only in the folders you give them.

This repository holds Perfica's installers and the metadata the app reads to learn that a newer one
exists. There's no source code here. The source is developed privately, and a release workflow
publishes every file here from a version tag.

## Installing

Take the newest release and the file for your platform:

| Platform | File | Notes |
|---|---|---|
| Windows | `Perfica-Setup-<version>.exe` | x64 |
| macOS | `Perfica-<version>-{x64,arm64}.dmg` | Apple Silicon and Intel builds are separate |
| Linux | `Perfica-<version>-{x86_64,arm64}.AppImage` | `chmod +x` it, then run it |

Upgrading from LoopCoder: Perfica installs as a new app beside it. Uninstall LoopCoder afterwards.
Nothing carries over.

### These builds aren't code-signed

None of these installers carries a code-signing certificate yet. Here's what that means before you run
one:

- **Windows** shows *"Windows protected your PC"*. To get past it, choose *More info*, then *Run anyway*.
- **macOS** blocks the app with Gatekeeper. Also, **an unsigned macOS app can't update itself**, so on
  macOS updating means downloading the new release by hand until this changes.
- **Linux** AppImages have no signing requirement and just run.

Every download's SHA-512 is recorded in the `latest*.yml` file beside it, and the app checks that hash
before it installs an update. So downloads are integrity-checked even though they aren't signed.

## The files that aren't installers

`latest.yml`, `latest-mac.yml` and `latest-linux.yml` are the update feed. An installed copy fetches the
one for its platform, compares that version with its own, and offers the update. They aren't useful to
download by hand, and deleting one from a release breaks updates for everyone on that platform.

## Issues

Bug reports and feature requests are welcome in this repository's issue tracker. The app can file a
report here for you, from *Report a bug* in its top bar. Pull requests aren't accepted, since there's no source
here to change.

## Terms

Using Perfica is governed by its [terms of use](https://perfica.dev/terms/),
[privacy policy](https://perfica.dev/privacy/) and [refund policy](https://perfica.dev/refunds/), in
English and [Spanish](https://perfica.dev/es/terms/). Perfica runs agents that execute commands and
change files on your computer. Review what runs, and keep backups.

## Licence

Perfica is proprietary software. See [LICENSE](LICENSE). Downloading a release grants no rights over the
source code.
