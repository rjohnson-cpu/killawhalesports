# Killa Whale (KW) Sports — Website

Static brand site for **killawhalesports.com**, built to host free on GitHub Pages with the domain staying at Namecheap.

## Files
- `index.html` — single-scroll home page (Hero, Why an orca, Three Pillars, Mental Game, Follow + Join, Footer)
- `connect.html` — quiet partner / press page
- `404.html` — redirects stray URLs back to home
- `CNAME` — binds the custom domain (killawhalesports.com). Do not delete.
- `.nojekyll` — tells GitHub Pages to serve files as-is
- `assets/` — orca icon, wordmark, favicons (white art on transparent, navy-disc favicons)

---

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `kwsports`). Public.
2. Upload everything in this folder to the repo root (keep the `assets/` folder and the `CNAME` file).
3. Repo **Settings → Pages**: set Source to **Deploy from a branch**, branch **main**, folder **/(root)**. Save.
4. Under **Custom domain**, it should already read `killawhalesports.com` (from the CNAME file). If not, type it and Save.
5. Wait for DNS (below) to resolve, then check **Enforce HTTPS**.

## Point the domain at GitHub (Namecheap → Advanced DNS)

Delete Namecheap's default parking records, then add:

**A records — Host `@`:**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```
**CNAME — Host `www`, Value:** `YOURUSERNAME.github.io.`

Replace `YOURUSERNAME` with your GitHub username. Propagation: 30 min to a few hours.

### Redirect the other domains
For `killawhalesports.com` and `kwsports.co`, use Namecheap's **Redirect Domain** (URL Redirect / unmasked, 301) pointing to `https://killawhalesports.com`.

---

## Email capture

The "Email to join" button on the home page opens the visitor's mail app with a message
to **kwsportsnj@gmail.com**. The partner/press links on the footer and Connect page use the
same address. No setup needed; these work the moment the site is live.

## Edit copy later
All text is plain HTML inside `index.html` / `connect.html`. Change wording directly, commit, and Pages redeploys automatically.
