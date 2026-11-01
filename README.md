# Logistics Order Tracker

A static single-page app (no build step, no dependencies).

- `index.html` is the whole app.
- `vercel.json` adds clean URLs and basic security headers. It is optional.

## Deploy to Vercel

1. Install the CLI: `npm i -g vercel`
2. From this folder run `vercel` (preview) or `vercel --prod`.
   Framework preset: "Other". Build command and output directory: leave empty.

Or push this folder to a Git repo and import it at vercel.com/new.

## Notes

- Orders are saved in the browser's localStorage, per device. There is no backend yet.
- Flow: New, Picking, Packed, Dispatched, Delivered. "Confirm delivery" on a dispatched order asks who received and endorsed it.
- Sample orders load on first visit; use "Clear sample orders" to remove them.
- Fonts load from Google Fonts. No other network requests are made.
