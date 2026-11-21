# Lake Nacimiento Water Ski & Conditions Dashboard

A single-file, dark-themed live conditions dashboard for **Lake Nacimiento, California**, built for water skiing, wakeboarding, and boating.

**Live Site:** https://gomce62.github.io/Lake-Nacimiento-Waterski-Conditions/

---

## What This Site Does

The dashboard aggregates real-time weather, wind, water level, and webcam feeds into one view:

- **Water-Ski & Glass Conditions Overview:** Displays current wind speed, gusts, wind direction, air temperature, and skiability conditions for the lake.
- **Dual-Source Weather & Hourly Wind Forecast:** Fetches live hourly and 7-day forecasts for Lake Nacimiento (`35.7289° N, 120.8844° W`) using **Open-Meteo** and **NOAA / National Weather Service (`api.weather.gov`)**.
- **Live Lake Level & Water Data:** Tracks reservoir elevation, capacity, and 7-day trends from **USGS Monitoring Location `11149300`** and **LakeMonster**.
- **Live Lake Webcams:** Embeds auto-refreshing snapshots with fallback handling from **805Webcams**:
  - LandsEnd Mid-Lake (Main Channel & Jumping Rock)
  - Lake Nacimiento Marina
  - Oak Shores
- **Zero-Backend Architecture:** Runs entirely in the browser using HTML, vanilla JavaScript, Tailwind CSS (CDN), Lucide Icons, and Google Fonts.

---

## How to Install & Run Locally

Because this is a static single-page HTML application, there is **no build step, package manager, or backend server required**.

### 1. Clone the repository

```bash
git clone https://github.com/gomce62/Lake-Nacimiento-Waterski-Conditions.git
cd Lake-Nacimiento-Waterski-Conditions
```

### 2. Run locally

**Option A — Open directly in a browser**
Double-click `index.html` (or open it via `File > Open File` in Chrome, Safari, Edge, or Firefox).

**Option B — Serve via a local HTTP server (recommended)**
Using Python:
```bash
python3 -m http.server 8000
```
Or using Node.js:
```bash
npx serve .
```
Then visit `http://localhost:8000` in your browser.

---

## Deployment

### GitHub Pages
This repository is configured to deploy automatically via **GitHub Pages** from the `gh-pages` branch:

- **Primary URL:** `https://gomce62.github.io/Lake-Nacimiento-Waterski-Conditions/`
- **Main file:** `index.html` (also mirrored as `lake_nacimiento_dashboard.html`)

To publish updates:
1. Edit `index.html` on `main` (and keep `lake_nacimiento_dashboard.html` synced if needed).
2. Commit and push to `main`, then merge/push to `gh-pages`:
   ```bash
   git checkout gh-pages
   git merge main
   git push origin gh-pages
   git checkout main
   ```

### Embedding in Google Sites
1. Open your Google Site editor (`sites.google.com`).
2. Select **Insert → Embed → By URL**.
3. Paste:
   ```text
   https://gomce62.github.io/Lake-Nacimiento-Waterski-Conditions/
   ```
4. Choose **Whole page** and resize the embed container as needed, then click **Publish**.
