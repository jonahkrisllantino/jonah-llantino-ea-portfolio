# Jonah Kris Llantino — VA/EA Portfolio Site

A single-page portfolio site (static HTML/CSS/JS, no build step, no dependencies).

## What's in this folder
- `index.html` — the entire site (all pages/tabs are rendered client-side via hash routing, e.g. `#offer`, `#work`, `#about`, `#write`)
- `img/` — every image the site references (30 files)
- `vercel.json` — minimal config (clean URLs)

## Deploy: GitHub → Vercel

### 1. Push to GitHub
```bash
cd jonah-site
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
(Create the empty repo on GitHub first — no README/license, so it doesn't conflict with this commit.)

### 2. Import into Vercel
1. Go to vercel.com → **Add New... → Project**
2. Select your GitHub repo
3. Framework preset: choose **Other** (it's a static site, no build command needed)
4. Build command: leave blank
5. Output directory: leave blank (root)
6. Click **Deploy**

Vercel will serve `index.html` at your root domain automatically — no further config needed.

### 3. Custom domain (optional)
In the Vercel project → **Settings → Domains**, add your own domain if you have one and point its DNS as instructed there.

## Updating later
Any time you want to change the site:
1. Edit `index.html` (or ask Claude to re-export the latest version)
2. `git add -A && git commit -m "update" && git push`
3. Vercel redeploys automatically on every push to `main`
