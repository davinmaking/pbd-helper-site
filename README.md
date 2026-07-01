# PBD Helper Site

Public landing + privacy policy for the **PBD Helper** Chrome extension.
Static HTML, no build step. Mirrors `smis-helper-site`.

- `index.html` — landing (lean v1; iterate later)
- `privacy.html` — privacy policy (CWS requires this URL live)
- `icon128.png` / `favicon.png` — teal brand mark (copied from the extension)
- `_headers`, `robots.txt`, `sitemap.xml`

## Deploy (Cloudflare Pages — one-time setup)
1. Push this repo to GitHub: `davinmaking/pbd-helper-site`.
2. Cloudflare dashboard → Pages → **Create project** → connect that repo → framework
   preset **None**, build command empty, output dir `/`.
3. Custom domain: add `pbd.davinhub.com` (Pages auto-creates the CNAME in the
   `davinhub.com` zone).
4. Verify: `https://pbd.davinhub.com/privacy` resolves (Pages serves `privacy.html`
   at the clean `/privacy` path).

After step 1, every push to `main` auto-deploys in ~1 minute.

## CWS
Live listing: `https://chromewebstore.google.com/detail/pbd-helper/hpjmhpolokbbhnjbnkddbjnomahanpoc`
(approved 2026-07-01). Privacy Policy URL is `https://pbd.davinhub.com/privacy`. The install
CTAs in `index.html` + `panduan.html` point at the live listing (`target="_blank"`).
