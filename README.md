# Biblelite-Web-App
Biblelite, Prayer sharing.

Static pages for the Biblelite app, hosted on Vercel at https://biblelite.vamillion.net/.

- `p/index.html` shows a written prayer shared from Biblelite as a Biblelite link. The prayer travels inside the link's `#fragment`, which browsers never send to a server, so nothing about it is stored here.
- `.well-known/assetlinks.json` lets Android open those links straight in the Biblelite app (App Links). It lists the app's signing-key fingerprints; add Google's app-signing key fingerprint when the app moves to Play App Signing.
- `vercel.json` serves `/p` without a redirect and gives `assetlinks.json` the JSON content type Android expects.

The app builds links as `https://biblelite.vamillion.net/p#1.<payload>`; changing the domain means changing `lib/prayer_codec.dart` and `AndroidManifest.xml` in the app too.
