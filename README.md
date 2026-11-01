# LinguaFlow Web Beta

A mobile-first PWA prototype for iPhone. It supports pasted text, bidirectional language selection, OCR from a selected screenshot, copy/share, and translation via the public MyMemory translation endpoint.

## Publish so it can be added to iPhone Home Screen
A PWA must be served over HTTPS for reliable installation and service-worker support. This ZIP is a static website; it is not yet hosted.

Simple publishing options:
1. Create a GitHub repository and upload `index.html`, `manifest.webmanifest`, and `sw.js`.
2. In repository Settings → Pages, deploy from the main branch/root.
3. Open the HTTPS Pages URL in Safari on iPhone.
4. Tap Share → Add to Home Screen.

You can also use any static HTTPS hosting provider. Do not put API secrets in the client. This prototype uses a public translation endpoint and has no private API key.

## Limits
- Cannot read or overlay other apps' live screens.
- Copy/paste and screenshot selection are required.
- Public translation endpoint has quotas/availability/quality limits.
- OCR downloads Tesseract.js and language data from a CDN; first use requires internet.
- For production, replace public translation service with a controlled backend, add a privacy policy, rate limiting, and stronger error handling.
