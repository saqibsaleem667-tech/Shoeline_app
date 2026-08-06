# Shoeline App — Deployment Guide

## What's inside
- `src/App.jsx` — the full app (catalog + admin panel), with all articles baked in
- `src/main.jsx` — entry point
- `index.html`, `vite.config.js`, `package.json` — standard Vite + React setup

## Updating your live site (already deployed on Vercel)
1. Replace `src/App.jsx` in your GitHub repo with the new one from this zip.
2. Vercel redeploys automatically within a minute.

## New in this update
- Customer side: "All Articles / Summer / Winter" tabs to filter the catalog.
- Admin: choose Summer or Winter when adding/editing an article. Existing articles
  (from your original Excel) have no season set yet, so they only show under
  "All Articles" until you edit each one and pick a season.
- Admin: an eye icon next to each article — tap to hide/unhide it from customers
  (hidden articles disappear from every customer-facing tab, but stay visible
  and editable in the admin list).
