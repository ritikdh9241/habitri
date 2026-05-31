# ✦ Habit OS

> Ultimate Habit Tracker — built with React + Vite. Track daily habits, set goals across 4 timeframes, earn XP, unlock achievements, and visualize your consistency.

![Habit OS Preview](https://img.shields.io/badge/React-18-61DAFB?style=flat&logo=react) ![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=flat&logo=vite) ![License](https://img.shields.io/badge/license-MIT-green)

---

## ✨ Features

### 📋 Habits
- 7-day weekly grid with per-day checkboxes
- Difficulty levels: Easy · Medium · Hard · Legendary
- Categories: Health · Fitness · Mind · Work · General
- Daily completion % with fill-circle indicators
- Drag handle to reorder habits
- Consistency heatmap (last 13 weeks)

### 🎯 Goals
- **Today** — daily to-do list
- **This Week** — weekly targets
- **This Month** — monthly milestones
- **This Year** — big annual goals
- Priority tags: High · Medium · Low
- Collapsible sections, sorted (done → bottom)

### 📊 Analytics
- Weekly completion line chart (Recharts)
- Per-habit XP & progress breakdown
- Level system (100 XP = 1 level)

### 🏆 Achievements
- 10 unlockable badges (First Step, Week Warrior, Level 10, Perfect Week, Year Planner, and more)

### 💅 Design
- Glassmorphism UI with `backdrop-filter: blur`
- Deep space gradient (dark) / soft blue (light)
- Dark/Light mode toggle
- Pure CSS confetti on habit completion
- Full confetti + banner on perfect day
- Smooth hover animations throughout
- localStorage persistence

### 📲 PWA Ready
- Installable on iPad, iPhone, Android, Desktop
- Service worker for offline support
- Web app manifest included

---

## 🚀 Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/habit-os.git
cd habit-os
```

### 2. Install dependencies
```bash
npm install
```

### 3. Run locally
```bash
npm run dev
```
Opens at `http://localhost:3000`

### 4. Build for production
```bash
npm run build
```
Output goes to `/dist` — ready to deploy.

---

## 📁 Project Structure

```
habit-os/
├── public/
│   ├── favicon.svg        # App icon
│   ├── manifest.json      # PWA manifest
│   └── sw.js              # Service worker (offline)
├── src/
│   ├── App.jsx            # Main app (all components)
│   └── main.jsx           # React entry point
├── index.html             # HTML shell
├── vite.config.js         # Vite config
├── package.json           # Dependencies
└── README.md
```

---

## 🌐 Deploy to GitHub Pages

```bash
# 1. Install gh-pages
npm install --save-dev gh-pages

# 2. Add to package.json scripts:
#    "predeploy": "npm run build",
#    "deploy": "gh-pages -d dist"

# 3. Add homepage to package.json:
#    "homepage": "https://YOUR_USERNAME.github.io/habit-os"

# 4. Deploy
npm run deploy
```

## 🌐 Deploy to Vercel (easiest)
1. Push to GitHub
2. Go to [vercel.com](https://vercel.com) → Import project
3. Select your repo → Deploy ✅

## 🌐 Deploy to Netlify
1. Push to GitHub
2. Go to [netlify.com](https://netlify.com) → New site from Git
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Deploy ✅

---

## 📱 Install as App on iPad / iPhone
1. Deploy to any URL (Vercel, Netlify, GitHub Pages)
2. Open the URL in **Safari**
3. Tap the **Share** button → **Add to Home Screen**
4. Tap **Add** — it's now a full-screen app! ✅

---

## 🛠 Customization

### Change default habits
Edit `INITIAL_STATE.habits` in `src/App.jsx`:
```js
const INITIAL_STATE = {
  habits: [
    { id: 1, label: 'Your habit', emoji: '🌟', category: 'Health', difficulty: 'Easy' },
    // ...
  ],
  checks: {},
};
```

### Change default goals
Edit `INITIAL_GOALS` in `src/App.jsx`:
```js
const INITIAL_GOALS = {
  today: [{ id: 't1', label: 'Your goal', priority: 'High', done: false }],
  week:  [...],
  month: [...],
  year:  [...],
};
```

### Add new categories or difficulties
Update the color maps near the top of `App.jsx`:
```js
const CAT_COLOR  = { Health: '#06b6d4', YourCategory: '#yourcolor', ... };
const DIFF_COLOR = { Easy: '#22c55e', YourDifficulty: '#yourcolor', ... };
```

---

## 📦 Tech Stack

| Tool | Purpose |
|------|---------|
| [React 18](https://react.dev) | UI framework |
| [Vite 5](https://vitejs.dev) | Build tool & dev server |
| [Recharts](https://recharts.org) | Analytics line chart |
| localStorage | Data persistence |
| Pure CSS | Confetti animation |
| CSS `backdrop-filter` | Glassmorphism |

---

## 📄 License

MIT © 2026 — free to use, modify, and distribute.

---

## 🙌 Credits

Built with [Claude](https://claude.ai) by Anthropic.
