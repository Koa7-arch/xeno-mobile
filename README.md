# XENO Mobile v0.2

Static PWA frontend for GitHub Pages plus a separate Cloudflare Worker gateway.

## Deploy
1. Upload `index.html`, `manifest.webmanifest`, `icon.svg`, `sw.js` to your GitHub Pages repository root. Do NOT upload API keys.
2. In Cloudflare Workers & Pages create a Worker and replace its code with `worker.js`. Deploy.
3. Add Worker secrets/variables: `GROQ_API_KEY` (Secret) and `ALLOWED_ORIGIN` (plain text variable, exact `https://YOUR-USERNAME.github.io`, without trailing slash).
4. In XENO Settings, paste the Worker URL and save.

## Security
Origin checks and CORS do NOT authenticate a public Worker endpoint; scripts can spoof Origin outside browsers. Add Cloudflare rate limiting and authentication before sustained use. Do not send sensitive information in this prototype. Never put a Groq key in GitHub or the PWA. Cloudflare Workers free usage and Groq API limits apply.

## Future providers
Add an adapter to PROVIDERS in worker.js, select provider server-side, and keep frontend request schema unchanged.
