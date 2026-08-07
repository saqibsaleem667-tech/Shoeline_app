# Shoeline App — instant load fix

The app no longer shows a blank "Loading catalog..." screen while waiting on
a network request. It now renders immediately using the built-in catalog
data (already inside the app bundle), and quietly fetches the latest
version from Google in the background — updating in place if anything
changed. This makes opening the app feel instant every time.

Replace src/App.jsx in your GitHub repo — Vercel redeploys automatically.
