# Respectful Emoji Tool

This modified version of
[neutral-face-emoji-tools](https://github.com/Fauntleroy/neutral-face-emoji-tools)
respects the [rate limits imposed by
Slack](https://api.slack.com/docs/rate-limits#overview), allowing you to queue
hundreds of emoji to upload!

### Installation

To use this extension, you will need to manually build and add it
since the [official
version](https://chrome.google.com/webstore/detail/neutral-face-emoji-tools/anchoacphlfbdomdlomnbbfhcmcdmjej)
does not respect Slack's rate limit.

1. Install [nvm (Node version
   manager)](https://github.com/nvm-sh/nvm#node-version-manager---)
1. `cd` into the local repo and run `nvm use` to change your Node version to
   `10.16.0` (as the [current version of gulp will not work with higher versions
   of
   Node](https://stackoverflow.com/questions/55921442/how-to-fix-referenceerror-primordials-is-not-defined-in-node))
1. Run `npm install` to download dependencies (_ignore security warnings_)
1. Run `npm run build` which will produce a `/dist` folder containing all of the
   files to upload in Chrome
1. Open Chrome and browse to `chrome://extensions/`
1. Click on `Load unpacked` and select the `/dist` folder on your local file
   system
1. You are now ready to upload emoji by navigating to
   `mySlackWorkspaceURL/customize/emoji`, where `mySlackWorkspaceURL` is the
   URL of your Slack workspace!

**Note**: Run `nvm use system` when you no longer need to keep your version of Node
set to `10.16.0`!
