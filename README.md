# Asher — 8 Week Program Tracker

Adaptive calisthenics + running + diet tracker. Works as a home screen app on Android.

## Deploy to GitHub Pages (5 min)

### Step 1 — Create a new repository
1. Go to github.com and log in
2. Click the **+** icon (top right) → **New repository**
3. Name it: `asher-tracker`
4. Set to **Public**
5. Click **Create repository**

### Step 2 — Upload the files
1. On the new repo page, click **uploading an existing file**
2. Drag and drop ALL 4 files at once:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon.png` (optional — add any square PNG image as your app icon)
3. Scroll down, click **Commit changes**

### Step 3 — Enable GitHub Pages
1. Click **Settings** (top of your repo)
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select **main** → **/root**
5. Click **Save**
6. Wait 1–2 minutes

### Step 4 — Get your URL
Your app will be live at:
```
https://YOUR_GITHUB_USERNAME.github.io/asher-tracker
```
GitHub will show this URL in the Pages settings section.

### Step 5 — Add to Android home screen
1. Open Chrome on your Android phone
2. Navigate to your URL above
3. Tap the **three dot menu** (top right)
4. Tap **Add to Home screen**
5. Tap **Add**

The app now lives on your home screen, opens fullscreen, and works offline.

---

## Data
All data is saved in your phone's localStorage — it persists between sessions and survives closing the browser. It is stored locally on your device only.

## App features
- **Plan tab** — adaptive workout for the week. Exercises, sets, reps, and rest times update automatically based on what you logged last week
- **Log tab** — weekly check-in. Log weight, chin-ups, push-ups, run distance/time/effort, shin pain flag
- **Progress tab** — weight chart vs target line, run pace trend, strength benchmarks

## How the adaptive logic works
| What you logged | What changes next week |
|---|---|
| Push-ups ≥ 20 | Flat push-up gets a 4th set. Diamond push-ups progress to 3×8–10 |
| Chin-ups ≥ 6 | Chin-up and negative pull-up get a 4th set |
| Run effort ≤ 4/10 | Progresses to next run level early |
| Run effort ≥ 8/10 | Holds current run level another week |
| Shin pain = Yes | Drops back to run/walk regardless of effort |
| Weight stalled 2 weeks | Calories drop to 1700, carbs reduced by 35g |
| Week 5 | Pike push-ups move to feet-elevated. Run adds Saturday intervals |
