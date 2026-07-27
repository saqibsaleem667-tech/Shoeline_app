# Shoeline App — Deployment Guide

## What's inside
- `src/App.jsx` — the full app (catalog + admin panel), with all 187 articles baked in
- `src/main.jsx` — entry point
- `index.html`, `vite.config.js`, `package.json` — standard Vite + React setup

## Before deploying: connect your Google Sheet
Open `src/App.jsx`, find this line near the top:

```
const ORDERS_ENDPOINT = "https://script.google.com/macros/s/AKfycbxu.../exec";
```

This is already set to the Google Apps Script Web App you created earlier. If you ever redeploy that script and get a new URL, update it here.

## Deploy to Vercel (free, ~5 minutes)

1. **Create a GitHub account** if you don't have one (github.com — free).
2. **Create a new repository** (e.g. "shoeline-app") and upload this whole folder to it.
   - Easiest way: on the GitHub repo page, click "Add file" → "Upload files", then drag in every file/folder here.
3. Go to **vercel.com** → Sign up using your GitHub account.
4. Click **"Add New Project"** → select your `shoeline-app` repository → click **Deploy**.
5. Vercel will detect it's a Vite project automatically. Wait ~1 minute.
6. You'll get a live URL like `https://shoeline-app.vercel.app` — this is your real, public website.

## After deploying
- Generate a QR code for that URL (any free QR generator online, e.g. qr-code-generator.com) and share it at the Shoeline event.
- Every order a customer submits will go straight into your Google Sheet.
- Admin panel: tap the small gear icon (bottom-right) on the site, passcode `1234` (change this in `App.jsx` — search for `ADMIN_PASSCODE`).

## Updating the catalog for the next Shoeline
1. Send me the new Excel file — I'll rebuild `src/App.jsx` with the new articles/images.
2. Replace the file in your GitHub repo (or ask me to prepare the updated project again).
3. Vercel automatically redeploys within a minute of any update to your repo.
