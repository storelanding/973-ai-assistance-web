# Ai Asistance — website

Static website for the Ai Asistance Android app (Google Play). Plain HTML + CSS, no build step.

| File | Purpose |
| --- | --- |
| `index.html` | App landing page |
| `policies.html` | Privacy Policy |
| `terms.html` | Terms of Use |
| `app-ads.txt` | app-ads.txt |
| `404.html` | Not-found page |
| `robots.txt`, `sitemap.xml` | Crawler rules and sitemap (absolute URLs use the site URL) |
| `assets/` | CSS, icon, images |
| `site.json` | Metadata used to generate the site (for future updates) |

## Deploy

**Cloudflare Pages:** Workers & Pages → Create → Pages → Connect to Git → choose this repo.
Framework preset **None**, build command empty, output directory `/`. Add your domain under Custom domains.

**Vercel:** Add New → Project → import this repo. Framework **Other**, no build command, output directory `.`.
Add your domain under Settings → Domains.

## After deploying

Site URL (hosted on Vercel): https://supper-assistance.vercel.app

- app-ads.txt: https://supper-assistance.vercel.app/app-ads.txt
- Privacy Policy: https://supper-assistance.vercel.app/policies.html

If the domain changes, update the absolute URLs in `sitemap.xml`, `robots.txt`, `site.json` and the
`canonical` / `og:url` / `og:image` tags in the HTML pages.

- `app-ads.txt` must be reachable at `https://<your-domain>/app-ads.txt`, and that domain must match the developer
  website declared on Google Play.
- Privacy Policy URL to declare on Google Play: `https://<your-domain>/policies.html`.

## Local preview

Open `index.html` in a browser — all paths are relative.
