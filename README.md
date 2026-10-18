<div align="center">

# Thawamine

**Replacement-screen touch freeze fix · iPhone 8 Plus**

<img src="https://cdn.shopify.com/s/files/1/0768/2372/4345/files/thawamine-r4-2-iphone-8-plus-ios-16-7-16.png?v=1792358260" alt="Thawamine — replacement-screen touch freeze fix for iPhone 8 Plus" width="900">

<br>

[![Release](https://img.shields.io/badge/release-current-08b8d1?style=flat-square)](https://github.com/privacyportalUK/Thawamine/releases/latest)
![Device](https://img.shields.io/badge/device-iPhone_8_Plus-313b4a?style=flat-square)
![iOS](https://img.shields.io/badge/iOS-16.7.16-313b4a?style=flat-square)

[![Download IPA](https://img.shields.io/badge/Download-IPA-08b8d1?style=for-the-badge)](https://github.com/privacyportalUK/Thawamine/releases/latest/download/Thawamine.ipa)
[![Source ZIP](https://img.shields.io/badge/Download-source-313b4a?style=for-the-badge)](https://github.com/privacyportalUK/Thawamine/releases/latest/download/Thawamine-source.zip)

[Installation](#install) · [Compatibility](#supported-device) · [Release notes](https://github.com/privacyportalUK/Thawamine/releases/latest) · [PrivacyPortal guide](https://www.privacyportal.co.uk/blogs/free-rooting-tips-and-tricks/thawamine)

</div>

---

## What is Thawamine?

Thawamine is [PrivacyPortal](https://PrivacyPortal.co.uk)'s jailbreak build for the frozen or unresponsive touchscreen issue encountered on an iPhone 8 Plus with a third-party replacement screen.

Built on **[Dopamine by opa334](https://github.com/opa334/Dopamine)** and **[Cheapamine by wumbomumbo](https://github.com/wumbomumbo/Cheapamine)**, including Cheapamine's selective restart approach.

| Feature | What it does |
| :--- | :--- |
| **Replacement-screen handling** | Uses selective restarts to address the touch freeze seen on the tested iPhone 8 Plus. |
| **Sileo & Zebra** | Registers both package-manager apps automatically. |
| **Tweak support** | Retains package-manager and tweak support; ElleKit installation through Sileo was tested successfully. |
| **Device checks** | The app and restart helpers enforce the same exact model and iOS-build allowlist. |

## Supported device

> [!IMPORTANT]
> **Only iPhone 8 Plus with model identifier `iPhone10,5` is supported.** Only iOS 16.7.16 (build `20H392`) is supported. Other iOS versions, iPhone models and replacement-screen variants are outside the verified support scope.

| iOS | Build | Testing status |
| :--- | :--- | :--- |
| **16.7.16** | `20H392` | Jailbreak, ElleKit installation through Sileo and the package restart completed with responsive touch. |

**Check your exact model, version and build before installing.**

<details>
<summary><strong>Testing and build details</strong></summary>

The test device was an iPhone 8 Plus (`iPhone10,5`) with a reported third-party replacement screen.

On iOS 16.7.16, a follow-up USB diagnostic capture found successful app registration and restart, unchanged touch reset counters, stable SpringBoard/backboardd processes, and no relevant crash reports or kernel panics during the observation. Earlier touch-driver errors had recovered. These results cover that device and screen; they do not establish compatibility with every panel or tweak.

| App information | Value |
| :--- | :--- |
| Installed app name | **Thawamine** |
| Build | `2026.10.77` |

The packaged Thawamine app passed compilation, regression and packaging checks. Its underlying jailbreak runtime was tested as described above; the renamed app has not been separately tested on a phone.

</details>

## Install

### ① Check & download

Check **Settings → General → About** against the [compatibility table](#supported-device).

| You need | Download |
| :--- | :--- |
| A Mac or Windows PC, USB cable and Apple account for signing | **[Download Thawamine IPA](https://github.com/privacyportalUK/Thawamine/releases/latest/download/Thawamine.ipa)** |
| Building it yourself | [Source ZIP](https://github.com/privacyportalUK/Thawamine/releases/latest/download/Thawamine-source.zip) · [Build instructions](#build-from-source) |

The **IPA is the installable app**. Downloading it in Safari alone does not install it.

### ② Sign & install

One option is **[Sideloadly for macOS or Windows](https://sideloadly.io/)**. You can also use your existing working IPA signing tool.

1. Install Sideloadly from its official website. Windows users should follow its iTunes/iCloud dependency instructions.
2. Connect the iPhone by USB, unlock it and accept **Trust This Computer** if prompted.
3. Select the phone in Sideloadly and drag the **IPA** into the app.
4. Enter your Apple account, start installation and complete any authentication prompts. Wait for it to finish.

### ③ Open & jailbreak

1. If prompted, trust the signing account under **Settings → General → VPN & Device Management**.
2. If iOS requests **Developer Mode**, follow **Settings → Privacy & Security → Developer Mode** and the restart prompts. [Apple's guide →](https://developer.apple.com/documentation/xcode/enabling-developer-mode-on-a-device)
3. Open **Thawamine**, tap **Jailbreak** and allow setup and the service restart to finish.
4. Unlock the phone, open **Sileo** or **Zebra**, and let the package lists refresh before installing packages.

> [!TIP]
> After a full device restart, reopen **Thawamine** and tap **Jailbreak** again. A respring is different from restarting the phone.
>
> With a free Apple account, Sideloadly-signed apps normally need refreshing every **7 days**. Refresh or re-sign before expiry, retaining the same signing account and bundle identifier when updating.

## Troubleshooting

<details>
<summary><strong>Sileo or Zebra is missing</strong></summary>

Open Thawamine's settings and use **Refresh Jailbreak Apps**, then check the Home Screen again.

</details>

<details>
<summary><strong>The app will not open, or setup stops with an error</strong></summary>

- **App will not open:** check the developer profile, any Developer Mode prompt and signing expiry. Re-sign using the same account and bundle identifier if needed.
- **Setup error:** save the exact message, restart the phone and try again. If it repeats, include the log when reporting the problem.

</details>

<details>
<summary><strong>Touch becomes unresponsive</strong></summary>

Quickly press **Volume Up**, quickly press **Volume Down**, then hold **Side** until the Apple logo appears. After restarting, check touch before jailbreaking again. Record which action triggered the freeze.

</details>

Need help? **[Contact PrivacyPortal](https://www.privacyportal.co.uk/pages/contact-us)** with your model identifier, iOS build, release, exact error and the steps that caused it. Remove account details and unique device identifiers from shared logs.

## Build from source

<details>
<summary><strong>Developer toolchain & build commands</strong></summary>

To install Thawamine, use the IPA and [installation steps](#install). Xcode and an SDK are needed only to compile the source.

| Requirement | Details |
| :--- | :--- |
| Host | macOS with full Xcode |
| Toolchain | Theos, GNU make, Procursus ldid, trustcache, dpkg, libarchive, OpenSSL and zstd |
| Compiler SDK | `iPhoneOS16.5.sdk` in Theos |
| Device target | iPhone 8 Plus (`iPhone10,5`), iOS 16.7.16 (`20H392`) |

**The compiler SDK version is separate from the iOS version on your phone.** It does not require changing the phone's iOS version.

Set `THEOS` to your Theos installation, then run:

```sh
git clone --recursive https://github.com/privacyportalUK/Thawamine.git
cd Thawamine
bash scripts/build-package-ipa.sh
```

The script builds and verifies the IPA. The release source ZIP includes recursive submodules, dependency sources and build records.

</details>

## Credits & licences

| Project | Credit |
| :--- | :--- |
| **[Dopamine](https://github.com/opa334/Dopamine)** | **opa334 and contributors** — upstream jailbreak, based on Dopamine 3.0.10. |
| **[Cheapamine](https://github.com/wumbomumbo/Cheapamine)** | **wumbomumbo and contributors** — the basis for selective restart support. |
| **Sileo · Zebra · Procursus · ElleKit** | Their teams and the upstream component authors listed in the [app credits](Application/Dopamine/UI/Settings/Credits.plist). |
| **[PrivacyPortal](https://PrivacyPortal.co.uk)** | Maintains this iPhone 8 Plus build, restart routing and automatic Sileo/Zebra registration. |

Original copyrights and licences are retained in [LICENSE.md](LICENSE.md) and the [component licence files](Application/Dopamine/Resources).

**This product includes software developed by the Sileo Team.**

---

<div align="center">

**[PrivacyPortal.co.uk](https://PrivacyPortal.co.uk)** · [Full guide](https://www.privacyportal.co.uk/blogs/free-rooting-tips-and-tricks/thawamine) · [Releases](https://github.com/privacyportalUK/Thawamine/releases)

</div>
