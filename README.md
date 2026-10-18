# Thawamine (iPhone 8 Plus)

> **R4.2 targets only iPhone 8 Plus (`iPhone10,5`) on iOS 16.7.10 (`20H350`) or iOS 16.7.16 (`20H392`). R4.2 has been tested and is working on iOS 16.7.16 with ElleKit and a third-party replacement screen; the same screen fix was previously validated on iOS 16.7.10 with R4.1. Other devices and iOS versions are unsupported.**

Thawamine is the PrivacyPortal project for the replacement-screen touch freeze fix. The installed app is named **Thawamine**; R4.2 identifies the release.

This branding update uses build **2026.10.77** and retains the tested R4.2 runtime, **3.0.10-s4.2**. The renamed build is compiled and checked before publication, but has not been separately tested on a phone.

Maintained by [PrivacyPortal](https://PrivacyPortal.co.uk).

**A jailbreak with a fix for the frozen or unresponsive touchscreen glitch after jailbreaking or restarting jailbreak services on an iPhone with a third-party replacement screen. Tested on iPhone 8 Plus with a third-party replacement screen: iOS 16.7.10 with R4.1, and iOS 16.7.16 with R4.2 and ElleKit.**

Built on [Dopamine 3.0.10 by opa334 and contributors](https://github.com/opa334/Dopamine) and [Cheapamine by wumbomumbo and contributors](https://github.com/wumbomumbo/Cheapamine), including its selective restart approach. PrivacyPortal maintains the iPhone 8 Plus build, restart routing and automatic Sileo and Zebra registration.

## Replacement-screen freeze fix

Some replacement screens can lose touch input when jailbreak services restart. Thawamine uses Cheapamine's selective restart approach to address the freeze encountered on the tested iPhone 8 Plus, while retaining package-manager and tweak support.

On the test iPhone 8 Plus (`iPhone10,5`) with a reported third-party replacement screen:

- **iOS 16.7.16 (`20H392`), R4.2:** jailbreak and ElleKit installation through Sileo succeeded, and touch remained responsive after the package restart. A follow-up USB diagnostic capture found successful app registration and restart, unchanged touch reset counters, stable SpringBoard/backboardd processes, and no relevant crash reports or kernel panics during the observation.
- **iOS 16.7.10 (`20H350`), R4.1:** the same replacement-screen fix was previously confirmed working after jailbreak, tweak installation and respring. R4.2 retains this support, but has not been separately retested on 16.7.10.

Earlier touch-driver errors recovered before the R4.2 observation. These results cover this device and screen; other replacement-screen variants have not been verified.

## Download R4.2

- [Thawamine-R4.2.ipa](https://github.com/privacyportalUK/Thawamine/releases/download/thawamine-r4.2/Thawamine-R4.2.ipa)
- [Thawamine-R4.2-source.zip](https://github.com/privacyportalUK/Thawamine/releases/download/thawamine-r4.2/Thawamine-R4.2-source.zip)
- [Release notes](https://github.com/privacyportalUK/Thawamine/releases/tag/thawamine-r4.2)

## Supported device

R4.2 permits **only iPhone 8 Plus (`iPhone10,5`) on iOS 16.7.10 (`20H350`) or iOS 16.7.16 (`20H392`)**. The app and restart helpers enforce the same exact model/build allowlist. Other devices and iOS versions are unsupported; compatibility must not be assumed.

R4.2 is tested and working on iOS 16.7.16 with ElleKit and the replacement screen described above. It retains support for the previously tested iOS 16.7.10 configuration. **This is not a continuous 16.7.10–16.7.16 compatibility range:** intermediate iOS builds are not enabled or tested.

## Install

### 1. Check your device and download the app

Check your model and iOS version in **Settings → General → About**. R4.2 is limited to **iPhone 8 Plus (`iPhone10,5`), iOS 16.7.10 (`20H350`) or iOS 16.7.16 (`20H392`)**. Other devices and iOS versions, including intermediate 16.7.x builds, are unsupported.

Download [Thawamine-R4.2.ipa](https://github.com/privacyportalUK/Thawamine/releases/download/thawamine-r4.2/Thawamine-R4.2.ipa) to your computer. The **IPA is the installable app**; the source ZIP is for building it yourself. You will need a Mac or Windows PC, a USB cable, and an Apple account for signing.

### 2. Install the IPA

One option is [Sideloadly for macOS or Windows](https://sideloadly.io/):

1. Install Sideloadly from its official website. Windows users should follow its Apple iTunes/iCloud dependency instructions.
2. Connect the iPhone by USB, unlock it, and accept **Trust This Computer** if prompted.
3. Select the connected iPhone in Sideloadly and drag the downloaded **IPA** into the app.
4. Enter your Apple account in Sideloadly, start installation, and complete any authentication prompts. Wait for installation to finish.

If you already have a working IPA signing tool, you can use it instead. Downloading the IPA in Safari alone does not install it.

### 3. Open the app and jailbreak

1. If iOS asks you to trust the signing account, open **Settings → General → VPN & Device Management**, select that account's developer profile, and follow the trust prompt.
2. If iOS requests **Developer Mode**, open **Settings → Privacy & Security → Developer Mode** and follow the restart and confirmation prompts. See [Apple's Developer Mode guide](https://developer.apple.com/documentation/xcode/enabling-developer-mode-on-a-device).
3. Open the installed jailbreak app and tap **Jailbreak**. Allow setup and the service restart to finish.
4. Unlock the phone and open **Sileo** or **Zebra**. R4.2 registers the package-manager apps automatically. Let the package manager refresh before installing packages.

### After restarting and refreshing the app

After a full power-off or device restart, open the jailbreak app and tap **Jailbreak** again. A respring is different from a full device restart.

With a free Apple account, Sideloadly-signed apps normally need refreshing every **7 days**. Use Sideloadly's refresh feature or re-sign the IPA before it expires. If the jailbreak app stops opening, check its signing status first.

### Troubleshooting

| What you see | What to do |
| --- | --- |
| Sileo or Zebra is missing after a successful jailbreak | Open the jailbreak app's settings and use **Refresh Jailbreak Apps**, then check the Home Screen again. |
| Setup stops with an error | Save the exact error message, restart the phone normally, and try again. If it repeats, include the log when reporting the problem. |
| The app will not open | Check the developer profile, Developer Mode prompt, and signing expiry. Re-sign using the same account and bundle identifier if needed. |
| Touch becomes unresponsive | On iPhone 8 Plus, quickly press Volume Up, quickly press Volume Down, then hold Side until the Apple logo appears. After it restarts, check touch before jailbreaking again. Record which action caused the freeze. |

For PrivacyPortal information and contact options, visit **[PrivacyPortal.co.uk](https://PrivacyPortal.co.uk)**. When reporting a problem, include the device model, iOS version, release version, exact error, and what happened immediately before it. Remove account details and device identifiers from any shared logs.

## Build from source (developers only)

**R4.2 targets iOS 16.7.10 and iOS 16.7.16 on the device listed above.** To install it, use the IPA and the installation steps above; Xcode and an SDK are not needed.

To compile the source, use macOS with full Xcode, Theos, GNU make, Procursus ldid, trustcache, dpkg, libarchive, OpenSSL and zstd. The build scripts require **iPhoneOS16.5.sdk** in Theos: this is the compiler SDK used to build the app, not the iOS version required on your phone. The SDK version does not require changing the iOS version on your phone.

Set `THEOS` to your Theos installation, then run:

```sh
git clone --recursive --branch thawamine-r4.2 https://github.com/privacyportalUK/Thawamine.git
cd Thawamine
bash scripts/build-package-ipa.sh
```

The script builds and verifies the IPA. The release source ZIP includes recursive submodules, dependency sources and build records.

## Credits and licenses

- [Dopamine](https://github.com/opa334/Dopamine) — opa334 and contributors.
- [Cheapamine](https://github.com/wumbomumbo/Cheapamine) — wumbomumbo and contributors; the basis for selective restart support.
- Sileo Team, Zebra Team, Procursus Team, ElleKit, and the upstream component authors listed in the [app credits](Application/Dopamine/UI/Settings/Credits.plist).

Original copyrights and licenses are retained in [LICENSE.md](LICENSE.md) and the [component license files](Application/Dopamine/Resources).

**This product includes software developed by the Sileo Team.**
