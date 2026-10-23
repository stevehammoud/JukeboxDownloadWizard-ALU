# Update format, protocol 1

Release assets include the install ZIP, UCE, SHA256SUMS.txt, update-manifest.json,
its raw 64-byte Ed25519 detached signature, and the public signing key.

The manifest is UTF-8 JSON. Verify the signature over its exact downloaded
bytes using the public key already trusted by the installed application.
Do not bootstrap trust by accepting a key downloaded beside an update.
The release's public-key copy is for inspection; it is not a trust decision.

Reject unknown schema/protocol, wrong product, unsupported architecture/profile,
ineligible releases, invalid signatures, incorrect hashes/sizes and archive
paths outside their permitted locations. Draft releases are not an update feed.
Stable and beta channels must be selected explicitly; do not compare version
strings lexicographically or silently switch a stable user to a beta.

The future updater must stage downloads on disk, verify available space for
staging plus rollback, preserve user state, quiesce all player/download/lookup
processes, and replace the UCE only through the tested ALU launcher sequence.
An interrupted operation must retain a working version and recover on launch.
These requirements are a protocol plan, not a shipped updater implementation.

Signing keys are maintained separately and are never committed to this repo.
