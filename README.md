# Jukebox Download Wizard for ALU

Release binaries and signed update information for the AtGames Legends edition
of JDW. Private development sources and signing credentials are not stored here.

The 0.1.0-beta.7 prerelease is an **application-only update** for the existing
beta.5/beta.6 split prototype. It is not a fresh-install ZIP and cannot update
older embedded beta.2/beta.3/beta.4 carts. See the release's READ-ME-FIRST.md.

The stable UCE contains the launcher, graphics runtime and BYOG artwork.
Jukebox Download Wizard/.app/JDW.app contains the native app and download tools.
Normal updates replace the app image while leaving the UCE/bootstrap and user
data in place. These packages are not encryption. Runtime notices ship in-app.

The beta.5 -> beta.6 local signed update/restart passed on HA8801/RK3328,
kernel 4.4.159. Beta.7 GitHub delivery and hardware acceptance are pending;
other models/firmware are unverified and not enabled by this manifest.

The beta.6 diagnostic install checks GitHub after its one-time
settings/update-test-mode marker is removed. Public-feed beta.7 disables
local-test mode. Startup offers A to install or B to continue; signatures,
compatibility, space, hashes, health and rollback are checked. Draft releases
are invisible to the anonymous ALU feed. See UPDATE-FORMAT.md for protocol 2.
