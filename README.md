# Jukebox Download Wizard for ALU

# JDW ALU beta.11 - controlled update-handoff diagnostic

HA8801/RK3328 diagnostic; cabinet acceptance pending. This is not a confirmed graphics fix. Beta.9 remains withdrawn. Beta.8 remains the accepted community baseline. Three local beta.10 restarts passed; the real downloaded-update handoff is the remaining test.

IMPORTANT: existing installations must have recovery-r2 Jukebox Download Wizard.uce before accepting this update. Replace only the root UCE using JDW-ALU-UCE-Recovery-Fix-r2.zip. Old beta.8 UCEs cannot execute rollback commands correctly on tested firmware; app-only updates cannot repair this and old beta.8 updaters cannot enforce the prerequisite. The complete Installer ZIP includes the repaired UCE. This diagnostic is for the owner's controlled test; other models are not enabled.

1. Restore J: to beta.8 with the supplied restore journal if beta.10 is installed. Keep the repaired UCE and all other files.
2. Accept beta.11 from the ALU GitHub update prompt. Signature and SHA-256 verification, backup, installation and restart are handled by JDW.
3. If it opens, visit all tabs, leave it open 30 seconds, then exit normally to accept the trial. Relaunch and confirm beta.11. Test P1 Restart JDW twice.
4. If it crashes or loses HDMI signal, stop and return the drive for log capture before further launches or testing the main SSD. Preserve the logs even if automatic recovery restores beta.8.
5. Before repeating on the main SSD, verify that SSD also has recovery-r2. Save its prior logs separately.

The normal automatic update check and preview warm-up are restored on ordinary launches. The existing first-boot trial still defers them. Diagnostics record exact render stage, frame counters, ARM registers, first presents, startup/cleanup timing and resource limits. Graphics libraries, rendering call order, audio/video decoder and solver cache implementation are retained. No raw cookies, account details or webpage contents are added to diagnostics.

Settings includes cookie status and Test YouTube Access. No One Sauce or cookies are needed for startup, local library or GitHub updates. Online video functions require your own Netscape cookie file at Jukebox Download Wizard/settings/ytcookies.txt. Cookies, settings, queue, library and persistent solver cache are preserved by app updates.

The trial requires 20 seconds, 120 frames and clean exit for acceptance. Later ordinary restarts are not themselves new first-boot trials.

Feedback: share logs/support-report.txt, logs/player.log, logs/entry.log, logs/display.log and root scripter.log for startup failure. Include model/firmware if known, port/hub, steps and symptoms. Review logs before posting. Never share cookies, credentials, settings/cache directories or media.

Accepted community baseline: [beta.8](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/tag/v0.1.0-beta.8).
Controlled diagnostic: [beta.11](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/tag/v0.1.0-beta.11).

Private source and signing credentials are not published. Third-party notices are bundled.
