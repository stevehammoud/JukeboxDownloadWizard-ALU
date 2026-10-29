# JDW ALU updates and complete installers

## Current community release: 0.1.0-beta.13

**Install beta.13 manually using the [complete installer](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/download/v0.1.0-beta.13/JukeboxDownloadWizard-ALU-Installer-0.1.0-beta.13.zip).** This applies to new installations and migration from earlier betas, including beta.12. Merge the existing folders and replace the matched UCE, external `00_start.sh` and `.app/JDW.app`; preserve saved data.

Beta.13 includes bootstrap revision 6 and the existing recovery-r2 UCE. Its startup script verifies the expected recovery script and binds the correctly decoded helper from JDW's own cart before entering the privileged session. This fixes startup paths containing spaces without requiring One Saucier.

**The beta.13 release has no automatic-update manifest.** Publishing the installer does not make it an eligible app-only update. An older app may correctly show no eligible update; use the installer link above. The existing beta.12 signed metadata and signing identity have not been replaced or changed by beta.13 documentation/installer refreshes.

The installer also bundles `Jukebox Download Wizard/bitlcd_marquee/Jukebox Download Wizard.jpg` and `.mp4`. These optional files are outside the application image. Copy the matched pair to the BitLCD USB drive as described in the README. They do not require an application rebuild or configure a separate drive automatically.

## Signed application-update protocol

Protocol 2 applies to eligible signed app-only releases. It verifies Ed25519 metadata with the existing pinned public key, checks SHA-256, stages the application update and retains a verified rollback copy. User confirmation is required. The app updater does not replace the live UCE or external startup script; a release requiring those files must use a complete installer.

User data and persistent solver cache stay outside `.app/JDW.app`. Compatibility and minimum-bootstrap requirements in a signed manifest must pass before installation. A failed first-boot trial can restore the verified prior application through the stable supervisor. Manual initial/migration copies do not themselves create updater transactions.

Only explicit signed model allowlists enable experimental devices on the beta channel. Unknown models/SoCs are not treated as universally supported. GPU profile selection and signed update eligibility are separate checks. The included profiles do not constitute hardware acceptance for every model or firmware.

For historical context, beta.12 required `minimum_bootstrap_revision=5`; older generation-4 installations could not install that app-only release and needed its complete installer. That historical manifest requirement is not a beta.13 automatic-update feed.

Signing identity is unchanged; the private signing key is never published. For current downloads and migration instructions, use the repository [README](README.md) and [beta.13 release notes](https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/tag/v0.1.0-beta.13).
