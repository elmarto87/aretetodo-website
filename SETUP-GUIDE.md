# Hosting Legal Docs on GitHub Pages — Setup Guide

## Overview

Host your Privacy Policy and Terms of Service at:
- `aretetodo.com/privacy`
- `aretetodo.com/terms`

Free. Custom domain. HTTPS included.

---

## Step 1: Create a new GitHub repo

1. Go to https://github.com/new
2. Name it `aretetodo.com` (or any name you like, e.g. `arete-legal`)
3. Set it to **Public**
4. Check "Add a README file"
5. Click **Create repository**

---

## Step 2: Add the legal pages

Create the following file structure in the repo:

```
/
├── index.html          ← Simple landing/redirect page
├── privacy/
│   └── index.html      ← Privacy Policy
├── terms/
│   └── index.html      ← Terms of Service
└── CNAME               ← Custom domain config
```

### 2a. Create `CNAME` file

Create a file called `CNAME` (no extension) in the repo root with just:

```
aretetodo.com
```

### 2b. Create `index.html` (landing page)

Create `index.html` in the repo root — a simple page that links to both docs:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ARETE</title>
  <style>
    body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; max-width: 600px; margin: 60px auto; padding: 0 24px; color: #111418; background: #FAFBFC; }
    h1 { font-size: 28px; font-weight: 800; letter-spacing: 3px; color: #2B4AFF; }
    p { font-size: 16px; color: #64748B; line-height: 1.6; }
    a { color: #2B4AFF; text-decoration: none; font-weight: 600; }
    a:hover { text-decoration: underline; }
    .links { margin-top: 32px; }
    .links a { display: block; margin-bottom: 12px; font-size: 17px; }
  </style>
</head>
<body>
  <h1>ARETE</h1>
  <p>The to-do list that actually gets done.</p>
  <div class="links">
    <a href="/privacy">Privacy Policy</a>
    <a href="/terms">Terms of Service</a>
  </div>
</body>
</html>
```

### 2c. Create `privacy/index.html`

Create the folder `privacy/` and add `index.html` inside it. Copy the content of `legal/privacy-policy.md` and wrap it in a simple HTML template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Privacy Policy — ARETE</title>
  <style>
    body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; max-width: 720px; margin: 40px auto; padding: 0 24px; color: #111418; background: #FAFBFC; line-height: 1.7; }
    h1 { font-size: 28px; color: #2B4AFF; }
    h2 { font-size: 20px; margin-top: 32px; border-bottom: 1px solid #E8EAED; padding-bottom: 8px; }
    h3 { font-size: 17px; margin-top: 24px; }
    p, li { font-size: 15px; color: #374151; }
    a { color: #2B4AFF; }
    table { width: 100%; border-collapse: collapse; margin: 16px 0; font-size: 14px; }
    th, td { border: 1px solid #E8EAED; padding: 10px 12px; text-align: left; }
    th { background: #F8FAFC; font-weight: 600; }
    hr { border: none; border-top: 1px solid #E8EAED; margin: 32px 0; }
    .back { display: inline-block; margin-bottom: 24px; font-size: 14px; color: #64748B; text-decoration: none; }
    .back:hover { color: #2B4AFF; }
  </style>
</head>
<body>
  <a class="back" href="/">← Back to ARETE</a>

  <!-- Paste the privacy policy content here as HTML -->
  <!-- Convert the markdown to HTML using any markdown-to-HTML tool -->
  <!-- Or use the raw markdown content from legal/privacy-policy.md -->

</body>
</html>
```

### 2d. Create `terms/index.html`

Same structure — create `terms/` folder with `index.html`. Use the same HTML template above but with the Terms of Service content and update the `<title>` to "Terms of Service — ARETE".

### Tip: Convert Markdown to HTML easily

Paste the markdown content from `legal/privacy-policy.md` and `legal/terms-of-service.md` into any of these free converters:
- https://markdowntohtml.com
- https://pandoc.org/try (select "from Markdown" → "to HTML")

Then paste the HTML output into the `<body>` of each template.

---

## Step 3: Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under "Source", select **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**
4. Click **Save**
5. GitHub will show: "Your site is live at https://yourusername.github.io/repo-name"

---

## Step 4: Connect your custom domain

### 4a. In GitHub

1. Still in **Settings → Pages**
2. Under "Custom domain", enter: `aretetodo.com`
3. Click **Save**
4. Check **Enforce HTTPS** (may take a few minutes to become available)

### 4b. In your DNS provider (Namecheap, Cloudflare, etc.)

Add these DNS records:

**For apex domain (`aretetodo.com`):**

| Type | Host | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**For www subdomain (optional):**

| Type | Host | Value |
|------|------|-------|
| CNAME | www | yourusername.github.io |

### 4c. Wait for DNS propagation

- Usually takes 5-30 minutes, sometimes up to 24 hours
- HTTPS certificate is provisioned automatically by GitHub (Let's Encrypt)
- You can check status in Settings → Pages

---

## Step 5: Verify

Once DNS propagates, verify these URLs work:
- `https://aretetodo.com` → landing page
- `https://aretetodo.com/privacy` → Privacy Policy
- `https://aretetodo.com/terms` → Terms of Service

---

## Step 6: Update app URLs

The app already points to these URLs in:
- `app/privacy-settings.tsx` → `https://aretetodo.com/privacy` and `https://aretetodo.com/terms`
- `app/signup.tsx` → same URLs

No code changes needed — they'll work as soon as the site is live.

---

## Summary

| What | Cost |
|------|------|
| GitHub Pages hosting | Free |
| Custom domain (aretetodo.com) | Already owned |
| HTTPS certificate | Free (GitHub/Let's Encrypt) |
| **Total** | **$0** |
