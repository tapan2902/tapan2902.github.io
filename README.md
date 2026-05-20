# Portfolio — Robotics & Mechatronics Engineering

A single-page portfolio site showcasing 17 robotics, mechatronics, and embedded systems projects. Built as a static site with zero dependencies — just HTML, CSS, and a touch of vanilla JS. Hosts on GitHub Pages with no build step.

## What's in here

```
.
├── index.html       # The whole site — one file, no frameworks
├── images/          # 28 project photos extracted from the source PDF
├── .nojekyll        # Tells GitHub Pages to serve files as-is
└── README.md        # This file
```

## Deploy to GitHub Pages

### 1. Create the repository

On GitHub, create a new repository. Two naming options:

- **Personal site:** name the repo exactly `yourusername.github.io` — the site will live at `https://yourusername.github.io`
- **Project site:** name it whatever you like (e.g. `portfolio`) — the site will live at `https://yourusername.github.io/portfolio`

### 2. Push the files

From this folder, run:

```bash
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/REPONAME.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Open your repo on GitHub
2. Go to **Settings → Pages**
3. Under **Source**, choose **Deploy from a branch**
4. Select branch **`main`** and folder **`/ (root)`**
5. Click **Save**

GitHub will publish the site within a minute or two. The Pages settings page shows the live URL once it's ready.

## Before you publish — things to update

Open `index.html` and edit:

1. **Your name** — the site currently has no name on it. Search for `<title>` and the nav `.brand` text. You may also want to add your name to the hero title.
2. **Contact info** in the footer (search for `your.email@example.com`):
   - Email
   - LinkedIn URL
   - GitHub URL
   - Location (currently set to Boston, MA based on your location data)
3. **Dates** in the hero meta (currently `2019 — 2026` as a guess)
4. **ABU ROBOCON** — this project has no photo in the source PDF, so it shows a placeholder card. Drop a photo into `images/abu-robocon.jpg` and swap the placeholder for a real `<figure>` if you have one.

## Custom domain (optional)

If you own a domain (e.g. `yourname.com`):

1. Add a file called `CNAME` to the repo root containing just your domain name
2. In your DNS provider, add a `CNAME` record pointing your domain (or subdomain) to `yourusername.github.io`
3. GitHub Pages will pick it up automatically — HTTPS is provisioned for free via Let's Encrypt

## Tech notes

- No build step, no npm, no dependencies — open `index.html` in a browser to preview locally
- Fonts loaded from Google Fonts: Fraunces (display), Inter Tight (body), JetBrains Mono (UI/code)
- All images are optimized to max 1600px wide, JPEG quality 85
- Total site weight: ~3.4 MB (mostly images)
- Responsive down to 360px wide
- The scroll-reveal animation uses IntersectionObserver — supported in all modern browsers
