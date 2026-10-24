# Signed application updates: protocol 2

The feed is the public GitHub releases API for this repository. Beta builds
consider published stable/prerelease tags; stable builds consider stable tags.
Drafts are excluded. Versions are compared numerically with prerelease ordering.
Only newer eligible compatible versions are offered, with A/B user confirmation.

Assets: JukeboxDownloadWizard-ALU-VERSION.zip, JDW-ALU-VERSION.squashfs, update-manifest.json,
update-manifest.json.sig, update-public-key.pem, SHA256SUMS.txt and README.
The signature is raw 64-byte Ed25519 over the exact UTF-8 manifest bytes.
The trusted public key is pinned in the installed app, not accepted from the
same download. The public-key asset is for inspection/recovery only.

Manifest schema_version is 1; minimum_updater_protocol is 2 and
minimum_bootstrap_revision is 4. Product, release tag, architecture, cabinet
model, channel, eligibility and exact repository download URLs must match.
The application section identifies the hosted .squashfs image, its size/SHA-256
and URL. The install_filename remains JDW.app; GitHub rejects .app uploads. The
install_bundle section identifies the ZIP, its size/SHA-256 and URL.
Public mode rejects test_only metadata. Beta.7 disables local diagnostic mode.

The ZIP may contain only Jukebox Download Wizard/.app/JDW.app and optional
READ-ME-FIRST.md; UCE/bootstrap/userdata paths, duplicates and symlinks fail.
Downloads stream to .app-updates/bundle.part, with free-space checks including
staging, backup and reserve. ZIP and extracted app hashes are verified before
installation. Current app/launcher identity is rechecked at commit.

The updater keeps previous.app, journals the transition, atomically replaces
only .app/JDW.app, and requests exit 43. The stable UCE supervisor remounts the
app but retains the SAME graphics mount through restart. It accepts a trial
only after at least 20 seconds/120 frames followed by clean exit. Incomplete
or failed first trials restore the verified old app; an invalid backup is not
restored. Final exit stops helpers and releases app/graphics/Node mounts.

Settings, cookies, queue, library and caches are outside the bundle. UCE and
bootstrap upgrades remain separate/manual; protocol 1 UCE-update archives
are incompatible. Signing credentials are maintained separately from this repo.


Beta.8 adds a separate fresh_installer asset; normal updates MUST continue to
use install_bundle (app-only). experimental_models_for_this_package is a signed
allowlist accepted only by beta.8+ beta-channel builds with experimental support
enabled. It is never a substitute for tested_models_for_this_package on stable.
An unknown model is not implicitly allowed merely because a SoC is recognized.
All beta.8 hardware acceptance is pending; HA8801 has beta.7 baseline evidence.
