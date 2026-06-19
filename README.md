# Shiksha Alochana — Website

The official website for **Shiksha Alochana (শিক্ষা আলোচনা)**, a non-profit organisation of primary school teachers in West Bengal.

Built with [Jekyll](https://jekyllrb.com/) + [GitHub Pages](https://pages.github.com/) (free hosting) + [Decap CMS](https://decapcms.org/) (browser-based editing).

---

## Quickstart — Publishing the Site (One Time)

### Step 1 — Create a GitHub account

Go to [github.com](https://github.com) and sign up for a free account if you don't already have one.

### Step 2 — Create a new repository

1. On GitHub, click the **+** icon → **New repository**
2. Name it `shiksha-alochana` (or any name you like)
3. Set it to **Public**
4. Do **not** tick "Add a README" (we already have one)
5. Click **Create repository**

### Step 3 — Upload the website files

**Option A — Using GitHub's web interface (no technical knowledge needed):**
1. On your new empty repository page, click **uploading an existing file**
2. Drag and drop all the files and folders from this folder
3. At the bottom, click **Commit changes**

**Option B — Using Git (for developers):**
```bash
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/shiksha-alochana.git
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Go to your repository → **Settings** → **Pages** (in the left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: **main**, folder: **/ (root)**
4. Click **Save**

Your site will be live at `https://YOUR-USERNAME.github.io/shiksha-alochana/` within a few minutes.

### Step 5 — Update your site URL in `_config.yml`

Open `_config.yml` and replace:
```yaml
url: "https://YOUR-USERNAME.github.io"
```
with your actual GitHub username.

---

## Editing Content from the Browser (Decap CMS)

This lets anyone with a GitHub account edit the website from a browser — no coding needed.

### One-time setup

**1. Create a GitHub OAuth App**

1. Go to [github.com/settings/developers](https://github.com/settings/developers)
2. Click **New OAuth App**
3. Fill in:
   - **Application name:** Shiksha Alochana CMS
   - **Homepage URL:** `https://YOUR-USERNAME.github.io/shiksha-alochana`
   - **Authorization callback URL:** `https://YOUR-USERNAME.github.io/shiksha-alochana`
4. Click **Register application**
5. Copy the **Client ID** shown on the next page

**2. Update `admin/config.yml`**

Open `admin/config.yml` and replace:
- `OWNER/REPO-NAME` → your GitHub username and repository name (e.g. `shikshaalochana/shiksha-alochana`)
- `YOUR-GITHUB-OAUTH-APP-CLIENT-ID` → the Client ID you just copied

**3. Push the change to GitHub** and wait a minute for the site to rebuild.

### Using the CMS

1. Visit `https://YOUR-USERNAME.github.io/shiksha-alochana/admin/`
2. Click **Login with GitHub**
3. Authorise the app
4. You will see a dashboard where you can:
   - **Add / edit News posts** — write announcements, event reports, updates
   - **Edit Pages** — update the About, Activities, Resources, and Wall Magazine pages
5. Click **Publish** when done — the site rebuilds automatically in about 1-2 minutes

---

## Simpler Alternative — Edit Directly on GitHub

You don't need the CMS to make edits. For any file:
1. Go to your repository on GitHub
2. Click on the file you want to edit (e.g. `about.md`)
3. Click the **pencil icon** (Edit this file)
4. Make your changes
5. Click **Commit changes**

The site rebuilds automatically within 1-2 minutes.

---

## Site Structure

```
/
├── _config.yml          # Site settings (title, contact info, etc.)
├── _layouts/            # Page templates
├── _includes/           # Header & footer
├── _posts/              # News articles (add new .md files here)
├── assets/css/          # Stylesheet
├── admin/               # Decap CMS browser editor
├── index.html           # Home page
├── about.md             # About Us page
├── activities.md        # Activities page
├── resources.md         # Resources page
├── wall-magazine.md     # Wall Magazine page
├── news.html            # News listing page
└── contact.md           # Contact page
```

## Adding a News Post

Create a new file in `_posts/` named `YYYY-MM-DD-title-here.md` with this format:

```markdown
---
layout: post
title: "Your Post Title"
date: 2025-06-15 10:00:00 +0530
author: Shiksha Alochana
categories: [news]
excerpt: "A short one-sentence summary."
---

Write your full post content here in Markdown.
```

---

## Updating Contact Information

All contact details are in `_config.yml`. Edit these fields:

```yaml
email: shikshaalochana2021@gmail.com
phone_primary: "+91 9831068201"
phone_secondary: "+91 9734805117"
phone_tertiary: "+91 9339493271"
address_line1: "Narayanpur, Lakshmipul"
address_line2: "North 24 Parganas, 743234"
address_line3: "West Bengal, India"
```

---

## Contact Form Setup

The contact form uses [Formspree](https://formspree.io) (free for up to 50 submissions/month).

1. Sign up at [formspree.io](https://formspree.io)
2. Create a new form and copy your form ID
3. In `contact.md`, replace `YOUR-FORM-ID` with your actual form ID:
   ```
   action="https://formspree.io/f/YOUR-FORM-ID"
   ```

---

## Custom Domain (Optional)

To use a custom domain like `www.shikshaalochana.org`:

1. Buy a domain from a registrar (e.g. GoDaddy, Namecheap)
2. In your registrar's DNS settings, add a CNAME record pointing to `YOUR-USERNAME.github.io`
3. In GitHub Pages settings, enter your custom domain
4. Update `url:` in `_config.yml` to your custom domain

---

## Technology Stack

| Component | Tool | Cost |
|-----------|------|------|
| Static site generator | Jekyll | Free |
| Hosting | GitHub Pages | Free |
| Browser CMS | Decap CMS | Free |
| Contact form | Formspree (free tier) | Free |
| Fonts | Google Fonts | Free |
| Total | | **₹0 / month** |
