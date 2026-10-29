# Jukebox Download Wizard for ALU

## Community testing beta.13

**[Download the complete beta.13 installer](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.13/JukeboxDownloadWizard-ALU-Installer-0.1.0-beta.13.zip)**

[Release notes](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/tag/v0.1.0-beta.13) | [Installation guide](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.13/READ-ME-FIRST.md) | [Test checklist](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.13/TEST-CASES.md) | [SHA-256 checksum](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.13/SHA256SUMS.txt)

Search YouTube, preview videos, download them to your ALU jukebox library, and manage saved videos from your cabinet. Downloads go directly to `ha8800_screensaver`, which JDW creates when needed. No One Sauce, One Saucier or URL-list text file is required to run JDW. Online features need your own cookie file; local library playback works without it.

### Install or update to beta.13

1. Download **JukeboxDownloadWizard-ALU-Installer-0.1.0-beta.13.zip** using the link above. It is the only installation package needed. GitHub's automatic **Source code** archives are not the installer.
2. Exit JDW cleanly and connect your USB/SSD to a PC. Keep a PC backup of your existing program files if you want a manual rollback.
3. Extract the ZIP to the drive root. **Merge folders and replace program files; do not delete your existing JDW folder first.** The matched program files are `Jukebox Download Wizard.uce`, `Jukebox Download Wizard/00_start.sh` and `Jukebox Download Wizard/.app/JDW.app`.
4. Keep your cookies, settings, queue, library, backups and solver cache. The installer does not supply or clear active user data. Your videos remain in drive-root `ha8800_screensaver`.
5. Put your Netscape-format cookie file at `Jukebox Download Wizard/settings/ytcookies.txt`. The cookie-export PDF and setup/test/compatibility guides are inside `Jukebox Download Wizard/docs/` in the ZIP. Use **Settings > Test YouTube Access** to check online access.
6. Launch JDW from BYOG. The installed version is **0.1.0-beta.13**.

**Beta.13 requires this manual installer, including when upgrading from beta.12.** It includes the generation-6 startup script and existing repaired UCE. This beta.13 release has no automatic-update manifest, so an older app may report no eligible update even though beta.13 is available here. See [UPDATE-FORMAT.md](UPDATE-FORMAT.md).

If you installed an earlier beta.13 copy before the latest corrections or artwork addition, download the current installer again. The version remains beta.13; the current app contains the r8 trackball confirmation fix and the installer includes the BitLCD files below.

### Included BitLCD marquee artwork

The installer includes the matching static JPG and 20-second animated MP4:

```text
Jukebox Download Wizard/bitlcd_marquee/
  Jukebox Download Wizard.jpg
  Jukebox Download Wizard.mp4
```

Extraction places both files in that folder on your app drive. To use them with BitLCD, copy **both files** to the BitLCD USB drive's `bitlcd/thirdparty/byog/` folder, preserving their filenames. Keep a PC backup before replacing existing artwork. These are the supplied matched artwork files; extraction does not automatically configure a separate BitLCD drive. BitLCD is optional and is not needed to run JDW.

### Beta.13 fixes and features

- Direct startup from BYOG without first opening One Saucier.
- Clean optional exit to an installed One Sauce, plus Restart JDW and exit to stock firmware.
- A transparent, animated logo screensaver replaces automatic idle exit.
- Manage Library provides **Preview, Delete and Rename**. Lists update automatically.
- **Delete Permanently** works with trackball/A and joystick confirmation. Cancel remains the default and deletion still requires confirmation.
- Automatic lightweight previews; video details show the available download resolution up to 1080p. Download Resolution remains separate from preview playback.
- Optional static and animated **BitLCD marquee artwork included in the installer**.

The original affected community tester confirmed the startup, One Sauce handoff and trackball deletion corrections. Owner tests also cover library actions, playback and clean exits. The subsequent artwork packaging change leaves the tested app, startup script and UCE unchanged. [Validation details](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.13/VALIDATION.json) distinguish tested behavior from pending device acceptance.

### Hardware and testing scope

HA8801/RK3328 has owner and community testing. Other included profiles remain experimental: HA8800/HA8802 (RK3328), HA8818/HA8819/HA2818/HA2819 (RK3399), and HA9901 (RK3588). This is a community prerelease, not universal model/firmware/display acceptance. See `Jukebox Download Wizard/docs/COMPATIBILITY.md` after extracting the installer. A suitable SSD and powered USB hub are recommended.

### Feedback

Follow the included test checklist and report your model/firmware if known, USB/hub/display/control setup, steps, expected/actual result and approximate time. Share these five files privately for analysis:

- `Jukebox Download Wizard/logs/entry.log`
- `Jukebox Download Wizard/logs/player.log`
- `Jukebox Download Wizard/logs/display.log`
- `Jukebox Download Wizard/logs/support-report.txt`
- Drive-root `scripter.log`

After a failed launch, copy `scripter.log` before opening another UCE, which can replace it. Review and redact private log data before any public attachment. Never upload cookies, credentials, cache folders or media/library files.

This repository publishes release downloads and documentation. Private development source and signing credentials are not published. Third-party notices are bundled with the application.
