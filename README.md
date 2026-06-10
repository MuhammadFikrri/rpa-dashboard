# 🤖 RPA Dashboard

> A self-contained, dark-themed portfolio dashboard for tracking Robotic Process Automation (RPA) projects — built as a single HTML file with zero dependencies.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-00d4ff?style=for-the-badge&logo=github)](https://muhammadfikrri.github.io/rpa-dashboard/)

---

## ✨ Features

### 📊 Overview
- Real-time stats: total projects, runs, success/failure rate
- Interactive bar chart with day/week/month/year grouping
- Date range filter with quick presets (Today, This Week, This Month)
- Status filter (All / Success / Failed)

### 📁 Projects
- Full project list with expandable schedule details
- Frequency categories: **Daily**, **Weekly**, **Monthly**, **Ad-hoc**
- Live schedule status: Completed ✅ | Running 🔵 | Scheduled ⏳ | Holiday 🏖️ | Failed ❌
- Sort by name, date, or status

### ▶️ Log Run
- **Log Failures** — select project + scheduled time slot, auto-replaces success with failure
- **Log Ad-hoc Runs** — manual logging for on-demand projects
- **Log Holidays** — mark specific schedules as not running (maintenance, public holidays)

### 📋 Run History
- Filterable table: by project, status, and time period
- Only shows completed runs (respects schedule end times)
- CSV download with custom date range

### 📊 Statistics
- Per-project breakdown: total runs, success rate, avg runs/day
- Date range filtering
- Color-coded success rates (green ≥95%, orange ≥80%, red <80%)

### 🕐 Schedule Timeline
- Visual 4-hour timeline with project execution bars
- Day selector (Mon–Fri) shows daily + weekly projects per day
- Automatic conflict detection with overlap duration
- Current time marker (NOW line)
- Color-coded project bars with time, name, and duration

### 🏆 Portfolio
- Professional portfolio view for interviews
- Print/PDF export ready
- Profile settings (name, title, bio)

---

## 🚀 Quick Start

1. **Download** `fikrirpadashboard.html` (or clone this repo)
2. **Open** it in any modern browser — that's it!
3. Your data auto-generates from the first day you open it

```
No server required. No installation. No dependencies.
Just double-click and go.
```

---

## 📦 How It Works

| Feature | Technology |
|---------|-----------|
| Frontend | Single HTML + CSS + Vanilla JS |
| Data Storage | Browser localStorage |
| Charts | Custom CSS bar charts |
| Hosting | GitHub Pages (static) |
| Export | JSON backup / CSV download |

---

## 🔄 Auto-Generation

The dashboard automatically generates run data every weekday:
- **Daily projects** → runs generated Monday–Friday
- **Weekly projects** → runs only on configured days (e.g., Mon & Fri)
- **Monthly projects** → runs on configured date (e.g., 1st of month)
- **Ad-hoc projects** → never auto-generated, manual logging only
- **Holidays** → skipped automatically

All auto-generated runs are marked as **success**. You only interact when logging **failures** or **holidays**.

---

## 🗂️ File Structure

```
📁 RPA Dashboard/
├── fikrirpadashboard.html   ← Your personal dashboard (full control)
├── rpadashboard.html        ← Company/team read-only view
├── index.html               ← Published to GitHub Pages
├── build_index.py           ← Script to publish with baked data
└── README.md                ← This file
```

---

## 📤 Publishing Workflow

To update the live GitHub Pages site with your latest data:

```bash
# 1. Export data from dashboard: Settings → Export Data (JSON)
# 2. Build the published version
python build_index.py

# 3. Push to GitHub
git add index.html
git commit -m "Update dashboard data"
git push
```

Visitors automatically get the latest data (version-based sync).

---

## 🎨 Theme

Dark navy design with:
- **Cyan** (`#00d4ff`) — primary accent
- **Purple** (`#7c4dff`) — secondary accent
- **Neon green** (`#00e676`) — success
- **Red** (`#ff5252`) — failure
- **Orange** (`#ffab40`) — warning/holiday

---

## 💾 Data Safety

- Data is stored in browser `localStorage`
- **Export regularly** (Settings → Export Data JSON)
- Monthly backup reminder built-in
- Import/export for device transfers
- Version-based sync for published site

---

## 🛠️ Built With

- HTML5 / CSS3 / Vanilla JavaScript
- No frameworks, no build tools, no npm
- Works offline, works on any device with a browser

---

## 📄 License

Personal project — free to use and modify for your own RPA portfolio tracking.

---

<p align="center">
  <strong>Built for RPA Developers who want to track, showcase, and monitor their automation portfolio.</strong>
</p>
