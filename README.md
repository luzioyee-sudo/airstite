# Airsite — Web Designer & UI/UX Developer

Bilingual (English / Arabic) portfolio site. The whole site is a single static file: `index.html` (HTML, CSS, JS and images are all embedded). No build step.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Push to GitHub

```bash
cd airsite
git init -b main
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Deploy

### GitHub Pages (automatic)
1. In the repo go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. Push to `main`. The workflow in `.github/workflows/deploy.yml` publishes the site.
4. Your site will be at `https://<your-username>.github.io/<repo-name>/`.

### Netlify
Import the repo at app.netlify.com. Leave the build command empty and set the publish directory to `.` (already in `netlify.toml`).

### Vercel
Import the repo at vercel.com. Framework preset: **Other**, no build command. `vercel.json` is included.

## Notes
- `index.html` is about 16 MB because images are embedded. GitHub accepts files up to 100 MB, but loading is faster if the images are compressed.
- Edits made inside the site's built-in editor are saved in the visitor's browser (localStorage); to change the live site for everyone, edit `index.html` and push.
