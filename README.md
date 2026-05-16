# 🎯 GATE 2027 Tracker

A comprehensive self-hosted study tracker built for GATE CSE preparation. Tracks progress across subjects, mock tests, revision schedules, study hours, and weekly goals — all stored locally in the browser with no backend required.

---

## 🚀 Getting Started

### Prerequisites
- Python 3 (for local server) or any static file server
- A modern browser (Chrome / Firefox / Edge)

### Running Locally

```bash
# Place files in a folder
mkdir gate-tracker && cd gate-tracker

# Put index.html and assets/index-modified.js inside
# Then serve with Python
python3 -m http.server 8080

# Open in browser
http://localhost:8080
```

### File Structure
```
gate-tracker/
├── index.html
└── assets/
    └── index-modified.js
```

> **Note:** All data is saved in browser storage automatically. No login, no backend.

---

## 📦 Features Overview

### 🗺️ Roadmap Tab
Visual phase-by-phase subject roadmap. Click any card to expand.

- Phase 1 → 2 → 3 layout with connector arrows
- Each card: subject name, progress %, phase color
- **Expand panel** — all topics with checkboxes, prerequisites, unlocks
- ✅ Click row to toggle topic complete
- **Revise** button per topic — stamps last-studied date
- Bottom banner shows days remaining (dynamic from your exam date)

---

### 📊 Dashboard Tab
Full prep overview at a glance.

- 4 stat cards — Days left · Streak · Latest mock · Completed subjects
- Phase progress grid
- All subjects mini list

**⏱ Study Time Tracker:**
- 5 cards: Today · This Week · 7-Day Avg · Total Hours · Streak 🔥
- **✓ Log hours** + **− Subtract** buttons
- Weekly target input with live progress bar
- `X hrs remaining` or `🎉 Weekly goal met!`
- Last 7 days bar chart (today in purple)
- **↓ Export CSV** · **↑ Import CSV**

---

### 📚 Subjects Tab
All 13 subjects organised by phase.

| Phase | Subjects |
|-------|----------|
| 1 (Apr–May) | Discrete Maths · Linear Algebra + Calculus · Probability & Stats · General Aptitude · C Programming |
| 2 (Jun–Aug) | Data Structures · Algorithms · OS · DBMS · Computer Networks |
| 3 (Sep–Jan) | Digital Logic · Computer Organisation · Theory of Computation · Compiler Design |

Each card shows progress bar, revised count, last studied date.  
Topics have ✅ checkbox + **Revise** button.

---

### 🔗 Resources Tab
Curated videos, notes, PYQ links per subject.

---

### 📝 Mocks Tab
Complete mock test tracking and analysis.

**Log a mock:** Name · Score/100 · Date · Link · **Weak subjects** (tag pills)

**Stat cards:** Best · Average · Taken · Avg L10

**Bar chart** — scrollable, color coded:
🟢 ≥80 · 🔵 ≥50 · 🔴 <50

**🔥 Weak Area Trend** (auto-appears after tagging):
- Frequency bar per subject
- ⚠ Recurring badge at 3+ mocks
- 🔵 1 · 🟠 2 · 🔴 3+ mock appearances

**All Mocks list:** Name → Weak tags → Score → Date → ✕

---

### 📈 Scores Tab
Subject-wise test score tracker (separate from full mocks).

- Add: Test name · Score · Max marks · Link · Subject selector
- Per-subject cards with Best %, Avg %, all entries
- **⚠ Weak <50%** badge auto-appears
- Score colors: 🟢 ≥80% · 🔵 ≥50% · 🔴 <50%

---

### 📖 Plan Tab — Revision Tracker
All 13 subjects with full revision history.

Each subject has **4 cards:**

| Card | Info |
|------|------|
| Revisions | Total count with gradient |
| Last Revision | Date · "Today ✓" · days ago |
| Next Revision | Auto (7 days) or custom date picker · Overdue/Today/in Xd |
| Done Today | Purple → green on click · undo last |

Border: 🔴 Overdue · 🟢 Due today

---

### 📅 Weekly Tab
Weekly review and snapshot archive.

**This week stats:** Hours · Mocks · **Avg L7** (last 7 mocks) · Streak · Topics · Revised

**📸 Save this week** — archives snapshot with all stats  
Past snapshots shown in reverse order, color-coded avg mock scores.

---

### 💡 Tips & 🗒️ Notes Tabs
Built-in strategy tips and free-form subject notes.

---

## ⚙️ Settings

| Setting | Location |
|---------|----------|
| Exam date | Header date picker (updates countdown everywhere) |
| Dark / Light mode | ☀️/🌙 button top-right |
| Weekly hour target | Dashboard time tracker card |

---

## 💾 Data

- Auto-saved in browser storage after every action
- **Export CSV** → `gate_tracker_export.csv` (mock + subject scores)
- **Import CSV** → merges data back without overwriting existing entries
- Recommended: export every Sunday before saving weekly snapshot

---

## 🎨 Score Colors (used everywhere)

| Score | Color |
|-------|-------|
| ≥ 80% | 🟢 Green |
| ≥ 50% | 🔵 Blue |
| < 50% | 🔴 Red |

---

## 📅 Recommended Daily Workflow

**Every day:**
1. Dashboard → log study hours (✓ Log hours)
2. Roadmap / Subjects → mark topics complete
3. After revising a subject → hit **Revise** on covered topics

**After every mock:**
1. Mocks tab → add score, name, link
2. Tag weak subjects with **Weak in:** pills
3. Check Weak Area Trend for patterns

**Every Sunday:**
1. Weekly tab → review stats
2. **📸 Save this week**
3. Export CSV as backup

---

## 🛠️ Tech

- React (no build step) · Vanilla JS · Browser Storage API
- Single compiled JS file — just serve `index.html` + `assets/` folder
