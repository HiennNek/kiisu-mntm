# Kiisu-MNTM
### Momentum firmware fork for Kiisu v4b/v4br - with U2F and rolling code support

> **Note:** Kiisu-MNTM is **not** an official Momentum branch. It is a separate community fork of [Momentum FW](https://github.com/Next-Flip/Momentum-Firmware) for Kiisu.

## Why choose this over other forks?

- **Up-to-date** - Actively maintained and always in sync with upstream Momentum, plus the latest tweaks and apps from upstream Kiisu FW.

- **Rolling code & U2F support** - Includes rolling code and U2F support for Kiisu. The firmware covers most rolling code manufacturers from upstream Momentum, but not all. If you find a missing manufacturer key, please [contribute here](https://github.com/HiennNek/non-flipper-rolling-code-support#-missing-keys).

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

## FAQ

> Don't see your question answered here? [Open an issue](https://github.com/HiennNek/kiisu-mntm/issues).

### General

<details>
<summary><b>What is Kiisu-MNTM?</b></summary>

Kiisu-MNTM is a community-maintained fork of [Momentum Firmware](https://github.com/Next-Flip/Momentum-Firmware) built specifically for the Kiisu device. It adds rolling code and U2F support that aren't available in official Flipper firmware on Kiisu hardware, ships hand-redrawn Kiisu-branded assets, and stays continuously synced with upstream Momentum plus the latest Kiisu-specific tweaks and apps.

</details>

<details>
<summary><b>Is this an official Momentum or Kiisu firmware?</b></summary>

No. Kiisu-MNTM is **not** an official Momentum branch, and it isn't the stock Kiisu firmware either - it's a separate, independently maintained community fork.

</details>

### Installation & Updates

<details>
<summary><b>How do I install Kiisu-MNTM?</b></summary>

Download the latest `flipper-z-f7-update-mntm-dev-XXXXXXXX.tgz` from the [Releases](https://github.com/HiennNek/kiisu-mntm/releases) page, then open **qFlipper** or [lab.flipper.net](https://lab.flipper.net/), choose **Install from file**, and select the downloaded file.

</details>

<details>
<summary><b>Can I switch back to stock firmware or another fork later?</b></summary>

Yes - switching is just a matter of flashing a different firmware file the same way, via qFlipper or lab.flipper.net.

</details>

<details>
<summary><b>How often is it updated?</b></summary>

It's actively maintained and kept in sync with upstream Momentum Firmware. Check the [Releases](https://github.com/HiennNek/kiisu-mntm/releases) page for the latest build.

</details>

### Features

<details>
<summary><b>What is rolling code support, and why does it matter for Kiisu?</b></summary>

Rolling code is the security scheme used by many garage door openers, gate remotes, and car key fobs, where each transmission uses a new code instead of a static one. Official Flipper firmware needs factory-provisioned keys to handle certain rolling-code protocols - and since Kiisu hardware isn't produced by Flipper Labs, it doesn't ship with those keys. Kiisu-MNTM implements its own support so these protocols work on Kiisu anyway.

</details>

<details>
<summary><b>Which rolling code manufacturers are supported?</b></summary>

Most of the manufacturers covered by upstream Momentum Firmware, though not all of them.

</details>

<details>
<summary><b>What if my remote/manufacturer isn't supported?</b></summary>

You can contribute the missing manufacturer key at the companion repo: [non-flipper-rolling-code-support](https://github.com/HiennNek/non-flipper-rolling-code-support#-missing-keys).

</details>

<details>
<summary><b>What is U2F, and why didn't it work before?</b></summary>

U2F (Universal 2nd Factor) is a hardware authentication standard used for two-factor login. Like rolling code, some U2F functionality needs factory keys that Kiisu hardware lacks - Kiisu-MNTM adds its own support so U2F works on Kiisu.

</details>

<details>
<summary><b>What's different about the Kiisu-themed assets in this fork?</b></summary>

All visuals are Kiisu-branded rather than Flipper-branded, and the original Kiisu asset set - which had some noise and low-resolution artifacts - has been redrawn by hand to fix those issues.

</details>

### Kiisu-MNTM vs. Other Firmware

<details>
<summary><b>How is this different from stock Kiisu firmware?</b></summary>

Kiisu-MNTM brings Momentum's broader feature set on top of Kiisu, stays actively synced with upstream, and includes the hand-corrected assets - none of which are part of stock Kiisu firmware.

</details>

<details>
<summary><b>How is this different from the official Momentum Kiisu branch?</b></summary>

The official Momentum Kiisu branch doesn't include the hand-redrawn Kiisu assets that Kiisu-MNTM ships with - it still has the original assets' minor visual issues (noise, low-res). Kiisu-MNTM also tracks upstream Momentum closely to stay current.

</details>
