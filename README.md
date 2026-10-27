# Jukebox Download Wizard for ALU

Cookie setup and access-test beta for Jukebox Download Wizard ALU.

Settings now shows Missing, Present (not tested), Authenticated or Authentication
Failed, with Test YouTube Access and cookie placement instructions. Network,
timeout or unknown responses are inconclusive. The bounded, cancellable test
checks YouTube's reported sign-in state without downloading video or starting
Node. It runs only while playback/search/download work is idle.

Existing beta.8 installations update only the app through the ALU GitHub prompt;
new users use the complete Installer ZIP. Stable UCE/bootstrap, cookies,
settings, queue, library and persistent solver cache are preserved. One Sauce
or One Saucier is not required. No cookie file is bundled.

HA8801/RK3328 passed beta.8 GitHub updates and media tests. Beta.9 hardware,
fresh-install and GitHub-to-ALU acceptance remain pending. Other listed models
remain experimental. Read READ-ME-FIRST.md, TEST-CASES.md and COMPATIBILITY.md.


Download the release Installer ZIP for a new installation. Existing split
installations use the built-in signed update. See the release test cases and
feedback instructions. Never share your cookie file. Private development
sources and signing credentials are not published; third-party notices remain
inside the app. See UPDATE-FORMAT.md for protocol-2 app updates.
