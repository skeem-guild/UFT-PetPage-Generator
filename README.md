# Neopets Petpage Generator

A single-page, static website that turns a **template CSV** into ready-to-copy
Neopets petpage HTML. Everything runs in the browser — no server needed, so it
works on GitHub Pages for free.

## Use it
1. Open the site.
2. Upload your CSV **or** paste it into the box (a sample is preloaded).
3. Adjust the page title / subtitle if you want.
4. Click **Copy HTML** (or **Download .html**) and paste it into your petpage.

## CSV format
- **Row 1** is treated as a header and skipped if its first cell is `Pet Name`.
- A **blank row** starts a new section; the **next row** becomes that section's
  heading (e.g. `UC P2`, `ANCIENT`, `RW`, `RN`).
- **Column 1** = pet username, **Column 2** = info line shown under the name.

Pets are laid out 3 per row in the same style as the original petpage.

## Deploy to GitHub Pages
1. Create a new GitHub repo and add `index.html` (and this README) to it.
2. Push:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Petpage generator"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
3. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   pick `main` / `/ (root)`, save.
4. Your site goes live at `https://<you>.github.io/<repo>/`.
