# CalciTape PWA starter

This package preserves the supplied CalciTape HTML and adds:
- PWA manifest and app icons
- Service worker and app-shell caching
- CalciTape branding in the page title and worksheet heading

## Test locally
Service workers require HTTPS or localhost. Opening index.html directly as a file will not enable PWA installation.

## Publish
Upload the contents of this folder to an HTTPS static host (for example GitHub Pages).
Then open the hosted URL in Chrome on Android and choose Install app / Add to Home screen.

## Offline note
Open the hosted app once while online so the service worker can cache the app shell and external assets. The current HTML loads Tailwind CSS, Google Fonts and html2pdf.js from CDNs; the service worker caches those assets as they are requested. A fully self-contained offline build can be prepared later by bundling these dependencies locally.

## Play Store note
This PWA package is not yet an Android APK/AAB and is not Play Store-ready by itself. A later Android packaging and Play Billing stage will be needed.
