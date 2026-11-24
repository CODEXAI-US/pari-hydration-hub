# Pari Hydration Hub

A simple, responsive informational website about **Kangen Water®** and Enagic's LeveLuk water ionizers. Built as a static site (plain HTML, CSS and JavaScript) — no build tools, no dependencies.

## Pages / Tabs

| Page | File | What's on it |
|------|------|--------------|
| Home | `index.html` | Intro, five water types, highlights, machine spotlight |
| About | `about.html` | What Kangen Water is, how the machine works, heritage |
| Benefits | `benefits.html` | Why people love it, beauty water, family lifestyle |
| Uses | `uses.html` | The five water types (seven pH settings) and what each is used for |
| FAQ | `faq.html` | Common questions and answers |
| Contact | `contact.html` | Email contact + a message form (opens your email app) |

## Project structure

```
.
├── index.html, about.html, benefits.html, uses.html, faq.html, contact.html
├── css/styles.css      # all styling
├── js/main.js          # mobile menu + footer year
├── img/                # website images (cleaned-up copies)
├── Images/             # original source images (not used by the site directly)
├── render.yaml         # Render deployment blueprint
└── README.md
```

## Run it locally

Just open `index.html` in a browser. Or serve the folder:

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000
```

## Contact / editing tips

- **Email:** the contact address is `pervinabdul@yahoo.com`. To change it, search-and-replace that string across the `.html` files.
- **Text:** all copy lives directly in the HTML — edit any page in a text editor.
- **Images:** swap files in `img/` (keep the same filenames), or point the `<img src="...">` tags at new ones.
- **Colors/fonts:** edit the variables at the top of `css/styles.css`.

---

## Deploy to GitHub

From this folder:

```bash
git init
git add .
git commit -m "Initial commit: Pari Hydration Hub website"
git branch -M main
# create an empty repo on github.com first, then:
git remote add origin https://github.com/<your-username>/pari-hydration-hub.git
git push -u origin main
```

## Deploy to Render (free static site)

**Option A — one click with the blueprint (`render.yaml`):**
1. Push this repo to GitHub (above).
2. In the [Render dashboard](https://dashboard.render.com), click **New → Blueprint**.
3. Connect the GitHub repo. Render reads `render.yaml` and creates the static site automatically.
4. Click **Apply** and wait for it to go live.

**Option B — manual static site:**
1. Push to GitHub.
2. Render dashboard → **New → Static Site** → connect the repo.
3. Settings:
   - **Build Command:** *(leave blank)*
   - **Publish Directory:** `.`
4. Click **Create Static Site**. Every push to `main` auto-deploys.

---

### Disclaimer
Kangen Water®, Enagic® and LeveLuk® are registered trademarks of Enagic Co., Ltd. This is an independent informational website, not the official Enagic site. Content is for general educational purposes only and is not medical advice.
