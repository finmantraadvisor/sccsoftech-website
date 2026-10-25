# SCC Softech website

Single-page website for SCC Softech IT Solutions (Sanvi Computers & Cloud): IT courses, laptop and desktop rental, and IT services.

Plain HTML, no build step. It is ready to host free on GitHub Pages.

## Files

| File | Purpose |
|---|---|
| `index.html` | The website |
| `404.html` | Shown when an old WordPress link (e.g. /about-us/) is opened; sends visitors to the home page |
| `favicon.svg` | Browser tab icon |
| `robots.txt`, `sitemap.xml` | Help Google find and index the site |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Deploy on GitHub Pages

1. Create a new repository on GitHub, for example `sccsoftech-website` (Public).
2. Upload all files from this folder (Add file → Upload files), including `.nojekyll`. Commit.
3. Go to **Settings → Pages**.
   - Source: **Deploy from a branch**
   - Branch: **main**, folder: **/ (root)** → Save.
4. Wait 1–2 minutes. The site is live at `https://<your-username>.github.io/sccsoftech-website/`. Check it there first.

## Connect the domain sccsoftech.com

Do this only after you have checked the github.io version. Until the DNS change, the old WordPress site stays live.

1. In **Settings → Pages → Custom domain**, enter `sccsoftech.com` and save. (GitHub adds a `CNAME` file to the repo.)
2. At your domain registrar (where sccsoftech.com was bought), edit DNS:
   - Delete the existing **A** records for `@` that point to the WordPress host.
   - Add four **A** records for `@`:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Add a **CNAME** record: `www` → `<your-username>.github.io`
3. Wait for DNS to update (from a few minutes up to 24 hours), then tick **Enforce HTTPS** in Settings → Pages.

**Before changing DNS:** if the domain's email (MX records) is with the same host, leave the MX records untouched so email keeps working. Also take a backup of the WordPress site.

## Making changes later

Edit `index.html` on GitHub (pencil icon) and commit. The live site updates in about a minute.

Things to fill in when available: course fees, rental rates, real student testimonials, and the trainer's experience and certifications.
