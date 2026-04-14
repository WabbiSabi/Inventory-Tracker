# RFID Inventory Tracker

A client-side web app for tracking RFID-scanned inventory across warehouse and event sites. Built for GitHub Pages — no backend required.

## How It Works

1. **Warehouse Scan** — Upload a CSV from your RFID scanner with the baseline inventory
2. **Event Site Scan** — Upload a second CSV confirming what arrived on-site
3. **Reconcile** — Dashboard auto-compares and shows confirmed, missing items
4. **Adjust** — Upload CSVs throughout the day to add or remove items as merchandise moves between sites
5. **Export** — Download the final reconciled inventory as a CSV

## Features

- CSV column mapping preview (works with any CSV format)
- Auto-detects delimiters (comma, tab, semicolon)
- Bulk add/remove via CSV with reason tracking
- Timestamped adjustment log
- Search and filter by status
- Data persists in browser localStorage
- Fully responsive

## Deploy to GitHub Pages

1. Create a new GitHub repository
2. Push this folder as the repo root
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch**, select `main` and `/ (root)`
5. Your site will be live at `https://<username>.github.io/<repo-name>/`

## Project Structure

```
rfid-inventory-tracker/
├── index.html          # Main page
├── css/
│   └── styles.css      # All styles
├── js/
│   ├── csv-parser.js   # CSV parsing utilities
│   └── app.js          # Application logic
└── README.md
```

## CSV Format

The app works with any CSV. On upload, you pick which column is the RFID tag and which is the description. Common scanner formats are auto-detected by header names like `tag`, `rfid`, `epc`, `id`, `sku`, `barcode`.
