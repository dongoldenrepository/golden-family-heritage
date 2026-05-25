# Golden Family Heritage — GitHub Pages Deployment

## What's in this folder

| File/Folder | Purpose |
|---|---|
| `index.html` | The website (single page app) |
| `data.js` | All family data (~135 people, 39+ families) |
| `charts/` | 39 scanned chart images (JPEG) |
| `DEPLOY.md` | This file |

---

## Step-by-step: Publish to GitHub Pages

### 1. Create a GitHub account (if you don't have one)
Go to [github.com](https://github.com) → Sign up (free).

### 2. Create a new repository
- Click the **+** button (top right) → **New repository**
- Name it something like: `golden-family-heritage`
- Set it to **Private** (only people with the link can see it via Pages)
  - Note: GitHub Pages on free accounts requires the repo to be **Public** for sharing.
  - For a truly private site, use Cloudflare Pages (see below).
- Click **Create repository**

### 3. Upload the files
**Option A — via GitHub website (easiest):**
1. In your new repo, click **uploading an existing file**
2. Drag and drop everything inside this `site/` folder:
   - `index.html`
   - `data.js`
   - The entire `charts/` folder
3. Click **Commit changes**

**Option B — via command line (if you have Git installed):**
```bash
cd "/Users/dongolden/Documents/Claude/Projects/Ancestry Website/site"
git init
git add .
git commit -m "Golden Family Heritage website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/golden-family-heritage.git
git push -u origin main
```

### 4. Enable GitHub Pages
1. In your repo, go to **Settings** → **Pages** (left sidebar)
2. Under "Source", select **Deploy from a branch**
3. Branch: **main** · Folder: **/ (root)**
4. Click **Save**
5. Wait ~2 minutes, then your site will be live at:
   `https://YOUR_USERNAME.github.io/golden-family-heritage/`

### 5. Share the link
Send that URL to family members — anyone with the link can view it!

---

## Alternative: Cloudflare Pages (truly private with password)

1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Connect your GitHub account and select your repo
3. Build settings: **None** (static site, no build command needed)
4. Deploy — you get a URL like `https://golden-family-heritage.pages.dev`
5. To add password protection: Cloudflare Pages → Access → Add a policy

---

## Updating the site later

To add corrections or new people:
1. Edit `data.js` — find the person's entry and update their fields
2. Re-upload (or `git push`) the updated file
3. GitHub Pages will automatically refresh within a minute or two

---

## Notes on the data

- Dates marked with `c.` mean "circa" (approximate)
- Names in `[brackets]` indicate uncertain readings from the handwritten forms
- All 39 original chart images are in the `charts/` folder for reference
- The tree is centered on **James Edward Golden** by default; use the dropdown to change the starting person
