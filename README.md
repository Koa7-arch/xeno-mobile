# XENO Mobile v0.1

A zero-build, iPhone-first Progressive Web App foundation. No dependencies or API keys.

## Deploy from an iPhone
1. Create a GitHub repository.
2. Upload the four files `index.html`, `manifest.webmanifest`, `icon.svg`, and `sw.js` to the repository root. You may also upload this README.
3. In GitHub repository **Settings → Pages**, select **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
4. Wait for GitHub Pages to publish. Visit the HTTPS URL shown in Pages settings in Safari.
5. In Safari, tap Share → Add to Home Screen → Add.

## Limitations
This is a UI prototype, not a live AI assistant. Chat messages are stored in browser localStorage on this device, not synchronized. Offline shell support depends on the service worker being installed and cached after the first online visit. SVG Home Screen icon support can vary across iOS versions; a PNG icon can be added later.

## Next
Add secure AI calls through a serverless backend, then authentication and cloud memory.
