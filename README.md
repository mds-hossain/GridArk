<div align="center">

# ▦ GridArk

**Instant Excel & CSV analytics dashboard - right in your browser.**

Drop any spreadsheet and get KPIs, charts, filters and a searchable table in seconds.
No backend. No upload. No tracking. Your data never leaves your device.

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-GitHub_Pages-6366f1)](https://mds-hossain.github.io/gridark/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e)](LICENSE)
[![No Build](https://img.shields.io/badge/Build-None_needed-f59e0b)](#)
[![Client--Side](https://img.shields.io/badge/100%25-Client--Side-06b6d4)](#-privacy)

</div>

---

## ✨ Features

### 📦 Broad format support & VBA macro preservation
Open **XLSX, XLSM, XLSB, XLS, XLTX, XLTM, CSV, TSV, ODS, FODS, Numbers, XML, TXT, DIF** and **SLK** files.

Macro-enabled workbooks (`.xlsm`, `.xltm`, `.xlsb`) are read with the raw VBA project attached (`bookVBA`). GridArk shows a banner when macros are detected and can export filtered data back to `.xlsm` with the macro blob preserved. Macros are never executed in the browser.

### 🧠 Smart column detection
GridArk analyzes your file and automatically recognizes:

| Type | Detection | What you get |
|---|---|---|
| **Categories** | Country, sector, status... | Filter dropdowns + bar charts |
| **Status** | Column name contains *status* | Color-coded pills + donut chart |
| **Dates** | `dd.mm.yyyy`, ISO, Excel dates | Activity timeline chart |
| **Numbers / Ratings** | Numeric values | Average KPI + distribution histogram |
| **URLs** | `http(s)://...` | One-click links (domain preview) |
| **Emails** | `name@domain.tld` | `mailto:` links + coverage KPI |
| **Phones** | International formats | `tel:` links + coverage KPI |

Works with lead lists, CRM exports, inventory, finance trackers, survey results and more. If your file structure changes, GridArk adapts automatically.

### 📊 Auto-generated dashboard
- **KPI cards** - totals, top status, positive-reply rate, unique counts, averages, contact-data coverage
- **Charts** - status donut, category distributions, date timeline, numeric histogram (Chart.js)
- **Data table** - global search, per-column filters, click-to-sort headers, pagination (25/50/100), sticky header, sleek minimal scrollbars
- **Export** - download your filtered view as CSV, XLSX or macro-preserving XLSM
- **Multi-sheet** - picker appears automatically for workbooks with several sheets

### 🎨 Make it yours (⚙️ settings panel)
- **8 themes** - 4 light (Light, Cream, Mint, Rose) + 4 dark (Dark, Midnight, OLED, Forest), with live swatch previews
- **11 fonts** - Inter, Poppins, Nunito, Roboto, Open Sans, Lato, Montserrat, Trebuchet MS, Tahoma, Verdana, Georgia
- **Font size slider** - 85 % to 130 %
- Charts re-color instantly to match your theme

### 🔍 Comfort tools
- **Zoom** 50 % to 150 % (magnifier controls in header, click % to reset)
- **Fullscreen mode** - expands the layout to the whole screen; wide tables breathe
- **Logo click** - returns to the homepage from anywhere
- **Persistent preferences** - theme, font, size & zoom are saved locally
- **Mobile responsive** - compact one-line header, icon-only buttons, full-width settings sheet

---

## 🚀 How to use

1. **Open** `index.html` in any modern browser (or visit the [live demo](https://mds-hossain.github.io/gridark/)).
2. **Drop** your spreadsheet file onto the dropzone - or click **📂 Choose file** / **✨ Try sample data**.
3. **Explore**:
   - Read KPIs & charts at a glance
   - Use dropdown filters + the search box to slice data - everything updates live
   - Click any column header to sort
   - Click website / email / phone cells to act on them
4. **Export** the filtered result as CSV, XLSX or macro-preserving XLSM when done.

> 💡 First load needs internet (Chart.js, SheetJS & fonts load from CDN). Everything after that runs locally.

---

## ⚙️ How it works

```
your-file.xlsm
      |
      v
SheetJS (in-browser parser, bookVBA) --> rows + headers + vbaraw
      |
      v
Column profiler --> type heuristics (url / email / phone / date / number / category / text)
      |             + name hints (status, country, sector, rating, company...)
      v
Dashboard engine --> KPIs + Chart.js visualizations + filterable/sortable table
      |
      v
Export --> CSV / XLSX / XLSM (vbaraw reattached, macros preserved)
```

- **Single file** - the whole app is one self-contained `index.html` (HTML + CSS + vanilla JS). No build step, no framework, no server.
- **Libraries via CDN** - [SheetJS](https://sheetjs.com/) for spreadsheet parsing, [Chart.js](https://www.chartjs.org/) for visualization, Google Fonts for typography.
- **State** - filters, sorting and preferences are held in memory / `localStorage`; nothing is transmitted anywhere.

---

## 🌐 Deploy on GitHub Pages

1. Push this repo (with `index.html` at the root).
2. Go to **Settings → Pages**.
3. Source: **Deploy from a branch** → Branch: `main` → folder: `/ (root)` → Save.
4. Your dashboard is live at `https://mds-hossain.github.io/gridark/` within a minute.

It also works on Netlify, Vercel, Cloudflare Pages - or just by double-clicking the file locally.

---

## 🔒 Privacy

GridArk is **100% client-side**:

- Files are parsed in your browser with the FileReader API
- VBA macros are preserved as inert data and never executed
- No server, no database, no analytics, no cookies
- Preferences are stored only in your browser's `localStorage`
- Safe for confidential lead lists, financial data and internal exports

---

## 📁 Project structure

```
gridark/
├── index.html   # the entire app (UI + logic)
├── README.md    # you are here
└── LICENSE      # MIT
```

---

## 🤝 Contributing

Issues and PRs are welcome. Ideas on the roadmap: editable cells with save-back to Excel, map view for location links, follow-up reminder rules, PWA offline bundle.

---

## 📜 License & Credits

Released under the [MIT License](LICENSE).

**Designed by Shakhawat H.**
© ShuvoniX 2026 · GridArk - Runs fully client-side · No cloud · No tracking
