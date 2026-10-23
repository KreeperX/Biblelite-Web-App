# Biblelite-Web-App
Biblelite, Prayer sharing.

Static pages for the Biblelite app, served by GitHub Pages at https://kreeperx.github.io/.

- `p/index.html` shows a written prayer shared from Biblelite as a Biblelite link. The prayer travels inside the link's `#fragment`, which browsers never send to a server, so nothing about it is stored here.
- `.well-known/assetlinks.json` lets Android open those links straight in the Biblelite app (App Links). It lists the app's signing-key fingerprints; add Google's app-signing key fingerprint when the app moves to Play App Signing.
- `.nojekyll` makes GitHub Pages serve the `.well-known` folder.

For links to open the app, this repository must be named `KreeperX.github.io` so the site sits at the domain root.
