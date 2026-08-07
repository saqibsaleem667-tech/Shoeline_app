# Shoeline App — speed update

Catalog is now cached in the browser (localStorage) after the first load,
so repeat visits show instantly while a fresh copy loads quietly in the
background. Images now use loading="lazy" so only visible ones load first.

Replace src/App.jsx in your GitHub repo — Vercel redeploys automatically.
