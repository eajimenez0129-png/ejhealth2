# EJ's Health Tracker — PWA

Neon green · Neon purple · Black & white.
Training, nutrition, and daily goals — all in one place.

---

## Deploy in 5 minutes (free)

### Step 1 — Install dependencies
```bash
npm install
```

### Step 2 — Test locally
```bash
npm run dev
```
Open http://localhost:5173 in your browser to verify everything looks right.

### Step 3 — Deploy to Vercel (recommended, free)

**Option A — Vercel CLI**
```bash
npm install -g vercel
vercel
```
Follow the prompts. Vercel auto-detects Vite. Your app will be live at a URL like:
`https://ej-health-tracker.vercel.app`

**Option B — Vercel Dashboard**
1. Push this folder to a GitHub repo
2. Go to vercel.com → New Project → Import your repo
3. Framework preset: Vite → Deploy
4. Done. Vercel handles builds automatically on every push.

---

## Add to iPhone home screen

1. Open your Vercel URL in **Safari** (must be Safari — Chrome doesn't support iOS PWA install)
2. Tap the **Share** button (box with upward arrow, bottom of screen)
3. Scroll down and tap **"Add to Home Screen"**
4. Name it **"EJ Health"** → tap **Add**

The app will appear on your home screen with the neon EJ icon.
It opens full-screen with no browser chrome, like a native app.
It works offline (service worker caches the app shell).

---

## Add to Android home screen

1. Open your Vercel URL in **Chrome**
2. Tap the three-dot menu → **"Add to Home screen"** or **"Install app"**
3. Tap **Add**

Android Chrome shows a proper install banner automatically after a few visits.

---

## Project structure

```
ej-pwa/
├── index.html              # PWA entry point (all meta tags)
├── vite.config.js
├── package.json
├── public/
│   ├── manifest.json       # PWA manifest (name, icons, colors)
│   ├── sw.js               # Service worker (offline caching)
│   └── icons/
│       ├── icon.svg        # Vector icon
│       ├── icon-180.png    # iOS home screen icon
│       ├── icon-192.png    # Android home screen icon
│       └── icon-512.png    # Android splash / store
└── src/
    ├── main.jsx            # React entry + service worker registration
    └── App.jsx             # Full app (all tabs, all logic)
```

---

## Updating the app

Edit `src/App.jsx` and push to GitHub. Vercel auto-deploys.
Your localStorage data on device persists across updates.

---

## Customising macro targets

On the **Dashboard** tab, tap **+ Log** under Weight Log.
Enter your new weight (and optionally body fat %).
The app recalculates your TDEE and all macro targets automatically.
