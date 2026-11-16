# Well Struck — Podcast Landing Page

Static marketing site for **wellstruckpod.com**: a clean modern landing page for the Well Struck football podcast, presented by Two Footed Media.

## Stack

- Vite (vanilla HTML/CSS/JS)
- Brand assets under `public/branding/`
- Build output: `dist/`

## Local development

```bash
npm install
npm run dev
```

Production build:

```bash
npm run build
npm run preview
```

## Deploy on Render (Static Site)

1. Push this repo to GitHub (or connect the existing remote).
2. In [Render](https://dashboard.render.com/) → **New** → **Static Site**.
3. Connect the GitHub repo and branch (usually `main`).
4. Settings:
   - **Build Command:** `npm install && npm run build`
   - **Publish Directory:** `dist`
   - **Node version:** 20+ (Render’s default is fine)
5. Deploy. Confirm the site loads on the `onrender.com` URL.

### Custom domain: wellstruckpod.com

1. In the Render Static Site → **Settings** → **Custom Domains** → add `wellstruckpod.com` (and optionally `www.wellstruckpod.com`).
2. At your DNS provider, create the records Render shows (typically):
   - **Apex (`wellstruckpod.com`):** A record to Render’s IP, *or* ALIAS/ANAME if your DNS supports it
   - **`www`:** CNAME to `your-service.onrender.com`
3. Wait for DNS + TLS provisioning (Render issues certificates automatically).
4. Prefer redirecting `www` → apex (or the reverse) so one canonical host wins.

No server runtime or environment variables are required for this static build.

## Content / links

Source copy and URLs live in the Project store at `docs/site-content.md`. Platform links on the page: Spotify, beehiiv newsletter, YouTube, Instagram, Threads, TikTok. Contact is `mailto:kevin@twofootedmedia.com`.
