# Jukebox Download Wizard for ALU

## Community testing beta.12

**Start here:** [Download the complete installer](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.12/JukeboxDownloadWizard-ALU-Installer-0.1.0-beta.12.zip).

New users and existing split-beta users use this same installer once. Extract
to the USB/SSD root and merge existing folders, replacing the UCE, 00_start.sh
and .app/JDW.app as a matched set. Keep cookies, settings, queue, library,
backups and solver cache. Documentation is in Jukebox Download Wizard/docs.

- [Cookie export guide](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.12/Cookie-Export-Guide.pdf)
- [Installation guide](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.12/READ-ME-FIRST.md)
- [One-time migration](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.12/MIGRATION.md)
- [Compatibility and experimental models](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.12/COMPATIBILITY.md)
- [Test checklist and feedback logs](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.12/TEST-CASES.md)

Download **JukeboxDownloadWizard-ALU-Installer-0.1.0-beta.12.zip** for a new
installation OR the one-time migration from earlier beta builds. It includes
the repaired UCE, generation-5 launcher, application, cookie-export PDF and
setup/test/compatibility guides. Extract to the USB/SSD root; merge existing
folders and replace all three program files. Keep cookies, settings, queue,
media, backups and solver cache. See MIGRATION.md before updating an old beta.

Older apps do not offer beta.12 automatically: the signed manifest requires
installer generation 5 so an app-only update cannot leave the faulty old UCE
in use. The new launcher verifies recovery-r2 before running JDW. Once migrated,
future eligible signed app updates continue through the built-in ALU updater.

HA8801/RK3328 has owner beta.11 update/media acceptance. HA8800/HA8802 (RK3328),
HA8818/HA8819/HA2818/HA2819 (RK3399), and HA9901 (RK3588) have experimental
profiles and need community hardware testing. Beta.12 final owner checks passed
on HA8801: generation-5 recovery verification, five launches, two in-app
restarts, local playback/fullscreen and three clean exits. Cookie/search/download
acceptance is from the unchanged beta.11 baseline. No universal
firmware or display compatibility is claimed. See COMPATIBILITY.md.

The player, audio/video pacing, GPU libraries and solver cache implementation
are retained from beta.11. Support-report version is corrected, experimental
update eligibility restored, and migration is now enforced. Earlier beta.9 Mali
failure did not recur in beta.11 tests; its root cause remains unconfirmed.
Three temporary streamed underruns around button actions on slow USB remain a
follow-up; saved-library playback had none. SSD with powered hub is recommended.
No One Sauce/One Saucier or URL-list file is required. Online video functions
need the user's own cookie file; local playback/startup/updates do not.

### Setup and feedback

Installer documentation is in Jukebox Download Wizard/docs. Read READ-ME-FIRST.md,
MIGRATION.md, Cookie-Export-Guide.pdf and TEST-CASES.md.
Share model/firmware if known, port/hub/display/controls, test case and steps,
expected/actual result, plus logs/support-report.txt, player.log, entry.log,
display.log; add root scripter.log for startup failure. Review logs before
posting. Never upload cookies, credentials, settings/cache folders or media.
Stop and capture logs after a crash before repeated launches.

Private development source and signing credentials are not published.
Third-party notices are bundled. See UPDATE-FORMAT.md for the signed updater.
