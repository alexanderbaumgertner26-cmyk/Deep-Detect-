# Deep Detect (Static React App)

This repository hosts the **Deep Detect** single-page app as a static site. It runs from a single `index.html` that imports React via CDN and renders into `#root`.

## Project Structure
```
deep-detect/
├─ index.html       # your app (copied from DeepDetect.html)
├─ README.md
├─ LICENSE
├─ .gitignore
├─ netlify.toml     # optional, for one-click Netlify deploys
└─ vercel.json      # optional, for zero-config Vercel deploys
```

## Quick Start (local preview)
You don't need Node or a bundler—it's a single file.
```bash
# from the repo root
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy Options

### 1) GitHub Pages (free)
1. Create a new GitHub repo and push this folder.
2. In **Settings → Pages**, choose **Deploy from branch** → `main` and **root** (`/`).
3. Your site will appear at `https://<username>.github.io/<repo>/`.

> If you want it served at the repo root automatically, keep the file name as `index.html` (already done).

### 2) Vercel (recommended for custom domains)
1. Go to Vercel → **New Project** → Import this GitHub repo.
2. **Framework Preset**: *Other*
3. **Build Command**: *(leave empty)*  
   **Output Directory**: `/`
4. Deploy. Add your custom domain in **Settings → Domains**.

### 3) Netlify (drag & drop or Git)
**Drag & drop**: zip the project and drop it on `app.netlify.com/drop` (it will serve `index.html` at `/`).  
**Git**: connect your repo; set **Build command**: *(none)* and **Publish directory**: `/`.

## Custom Domain + HTTPS
Point your DNS to your chosen host (Vercel/Netlify/GitHub Pages). Most providers issue SSL automatically.

## Next Steps (optional modernization)
If you later want a dev setup with bundling and hot reload, migrate to Vite:
```bash
npm create vite@latest deep-detect -- --template react
cd deep-detect
npm i
# move JSX/state into src/App.jsx and run:
npm run dev
```
Then deploy the `dist/` folder to Vercel/Netlify.

---

**Enjoy!** If you want me to also add CI/CD or convert this to a Vite/Next.js repo, say the word.