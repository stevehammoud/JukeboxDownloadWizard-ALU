# Jukebox Download Wizard for ALU

The current public community test release is **0.1.0-beta.8**:
https://github.com/stevehammoud/JukeboxDownloadWizard-ALU/releases/tag/v0.1.0-beta.8

Beta.9 has been withdrawn after an HA8801 startup failure and a failed automatic
rollback. Its assets are retained privately as a draft for investigation.
Please use beta.8 while a corrected candidate is tested. Beta.8 fresh startup
without One Sauce/cookies and clean exit passed on the maintainer's HA8801.
Other cabinet/display/controller combinations remain experimental.

For a new installation, use the complete Installer ZIP from the beta.8 release.
It includes the stable UCE and separate opaque application image. No One Sauce,
One Saucier or old JDW test/player folders are required. Existing split installs
normally use the signed app-only updater; user settings, cookies, queue, library
and persistent solver cache remain outside the application image.

YouTube search, previews and downloads require your own Netscape-format cookie
file at Jukebox Download Wizard/settings/ytcookies.txt. Local library use and
GitHub update checks do not require cookies. Never share your cookie file.

Read the release README, TEST-CASES.md, COMPATIBILITY.md and feedback instructions.
Report results through GitHub Issues and attach only reviewed diagnostic logs.
Private development sources and signing credentials are not published.
Third-party notices remain inside the application. See UPDATE-FORMAT.md for the
signed application update format.
