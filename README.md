# Logistics Order Tracker

A static single-page app. No build step, no dependencies to install.

## Files

- `index.html` is the whole app (HTML, CSS and JavaScript).
- `vercel.json` adds clean URLs and basic security headers. Optional.
- `sample-orders.xlsx` is an example file for the Upload Excel feature.
- `.gitignore` keeps Vercel CLI and OS files out of the repo.

## Deploy to Vercel

**From GitHub (recommended, redeploys on every push to `main`)**

1. Go to https://vercel.com/new and import this repository.
2. Framework Preset: **Other**. Leave Build Command, Output Directory and Install Command empty (Root Directory stays `./`).
3. Click Deploy.

To connect an existing Vercel project instead: Project Settings, Git, Connect Git Repository, choose this repo and set the production branch to `main`.

**From the CLI**

```
npm i -g vercel
vercel --prod
```

## How it works

- Flow: New, Picking, Packed, Dispatched, Delivered. "Confirm delivery" on a dispatched order asks who received and endorsed it.
- Add orders one at a time, or use Upload Excel for `.xlsx`, `.xls` or `.csv`. Row one needs `Order ID` and `Customer name` headers; `Priority` is optional.
- Orders are saved in each browser's localStorage. There is no backend, so data does not sync between devices.
- Sample orders load on first visit; use the bin icon to clear them.
- External requests: Google Fonts, and the spreadsheet reader (SheetJS 0.18.5) from cdnjs, used only when uploading a file.
