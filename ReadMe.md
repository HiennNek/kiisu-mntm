# Kiisu-MNTM
### Momentum firmware fork for Kiisu v4b/v4br - with U2F and rolling code support

> **Note:** Kiisu-MNTM is **not** an official Momentum branch. It is a separate community fork of [Momentum FW](https://github.com/Next-Flip/Momentum-Firmware) for Kiisu.

## Why choose this over other forks?

- **Up-to-date** - Actively maintained and always in sync with upstream Momentum, plus the latest tweaks and apps from upstream Kiisu FW.

- **Rolling code & U2F support** - Includes rolling code and U2F support for Kiisu. The firmware covers most rolling code manufacturers from upstream Momentum, but not all. If you find a missing manufacturer key, please [contribute here](https://github.com/HiennNek/non-flipper-rolling-code-support).

- **Kiisu assets** - Replaces all Flipper assets with Kiisu branding, unlike the Momentum Kiisu branch or stock Kiisu FW. The original Kiisu assets had minor visual issues (noise, low-res images); this firmware ships with fixed assets redrawn by hand. Found something missing? [Open an issue](https://github.com/HiennNek/kiisu-mntm/issues).

## How to install

1. Download **`flipper-z-f7-update-mntm-dev-XXXXXXXX.tgz`** from [Releases](https://github.com/HiennNek/kiisu-mntm/releases)
2. Open **qFlipper** or visit [lab.flipper.net](https://lab.flipper.net/)
3. Select **Install from file** and choose the downloaded file

## How to build

Clone the repository:

```bash
git clone --recursive --jobs 8 https://github.com/Next-Flip/Momentum-Firmware.git
cd Momentum-Firmware/
```

Flash directly to the Flipper (device must be connected via USB with qFlipper closed):

```bash
./fbt flash_usb_full
```

Compile a TGZ package:

```bash
./fbt updater_package
```

Build and launch a single app:

```bash
./fbt launch APPSRC=your_appid
```
