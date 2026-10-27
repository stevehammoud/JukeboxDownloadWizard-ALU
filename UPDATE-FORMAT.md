# JDW ALU signed updates - community installer generation 5

Protocol 2 stages a signed app-only ZIP, verifies Ed25519 metadata with the
existing pinned public key, checks SHA-256, retains previous app/bootstrap,
and commits by rename. User confirmation is required. The live UCE is not
replaced by the app updater. Userdata and persistent solver cache stay outside
.app/JDW.app. Health requires 20 seconds, 120 frames and clean exit; a failed
first-boot trial restores the verified backup through the stable supervisor.

Beta.12 requires minimum_bootstrap_revision=5. Legacy beta.8/beta.11 build-info
revision 4 fails this authentication check and cannot install the app-only
community release. Use the COMPLETE installer once, merging all three program
files. Generation-5 00_start.sh verifies the exact repaired recovery script in
the mounted root UCE before entering the privileged session. Unknown/old UCEs
are refused before recovery/app execution. No data-directory marker can bypass
this check. New complete installers include the repaired UCE.

Manual initial/migration copies do not themselves create updater transactions.
After migration, future signed eligible updates continue normally. Only signed
explicit model allowlists enable experimental devices on the beta channel;
stable does not. Unknown models/SoCs are not treated as universally supported.
GPU profile selection and signed update eligibility are separate decisions.
Signing identity unchanged; private key never published. See MIGRATION.md.
