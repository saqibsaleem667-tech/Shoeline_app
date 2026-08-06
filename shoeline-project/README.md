# Shoeline App — Deployment Guide

## Updating your live site
1. Replace `src/App.jsx` in your GitHub repo with the new one from this zip.
2. Vercel redeploys automatically within a minute.

## This update fixes
- Catalog edits (season, hide/unhide, add/edit article) now save to your Google
  Sheet's linked Drive file, not just your own phone — every device sees the
  same catalog after a page refresh.
  IMPORTANT: paste the updated `google-sheets-backend-v3.gs` into your Apps
  Script (Extensions > Apps Script), then Deploy > Manage deployments > Edit
  > New version > Deploy. The first time you save, Google will ask you to
  authorize Drive access — allow it.
- Season buttons (Summer/Winter) in the admin add/edit form now deselect if
  you tap the already-selected one again.
