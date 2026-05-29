# FORGE — install guide

A Progressive Web App for forging a daily eat-right + gym routine using Stoic discipline and behavioral-psychology habit design.

## Files
- `index.html` — the whole app (works offline, no build step)
- `manifest.json` — makes it installable
- `sw.js` — service worker (offline + caching)
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` — app icons

A PWA must be served over **https** (or `localhost`) for install + offline to work. Pick one:

### Option A — Free hosting (easiest, gets you a real installable app)
1. Make a free account at **Netlify** (or Vercel / Cloudflare Pages / GitHub Pages).
2. Drag this whole folder onto Netlify's "deploy" drop zone.
3. Open the URL it gives you on your phone.
4. **iPhone (Safari):** Share → *Add to Home Screen*.
   **Android (Chrome):** tap the *Install* banner / ⋮ menu → *Install app*.

### Option B — Test locally first
```bash
cd forge
python3 -m http.server 8080
# then open http://localhost:8080 on the same machine
```

## How to use it
1. **System tab** — set your *identity* ("I am someone who…"), then add Implementation Intentions, Habit Stacks, Temptation Bundles, and your nightly Environment prep.
2. **Today tab** — tap *I showed up* (the keystone), tick the 3·3·3 plate, fill the water drops before 3 PM, and your cues + prep show here.
3. **Reflect tab** — morning premeditation, the daily discomfort challenge, evening reflection.
4. **Progress tab** — your don't-break-the-chain heatmap and the ledger of votes for your identity.

All data is stored privately on your own device. Use **System → Export** to back it up.

## Motivation & discipline tools built in
- **Show-up timer** (2 / 10 / 20 / 30 min) on the Today screen — finishing it auto-logs your session. Master the art of *beginning*.
- **"I don't feel like it"** button — opens your identity, your why, a Stoic line and a reframe, then offers to start a 2-minute timer. Use it the moment you waver.
- **Reminders & alarms** (System tab):
  - In-app notifications fire at your chosen times while FORGE is open (default nudges for morning intention, hydration, training, evening reflection — all editable).
  - On supported browsers (Chrome/Edge, installed) they can also fire when the app is closed.
  - **＋cal** on any reminder downloads a repeating **calendar alarm (.ics)** — the reliable way to get an alarm that rings even when the app is closed (works on iPhone too).
- **Commitment contract** — sign a promise to your future self; reading it back is its own discipline tool.
- **The Memory (journal)** in Progress — every reflection and win, kept and scrollable.
- **Backup & restore** — export your data and import it onto a new phone.

### Why the calendar alarm matters
Phone browsers (especially iOS Safari) **cannot reliably wake a closed web app to fire an alarm on time** — that's an OS limitation, not a bug in FORGE. The in-app nudges cover you while the app is open; the **＋cal alarms** cover you when it's closed. Use both.

## Maxim of the Day
The top of the Today screen shows a **daily Latin maxim** — the Latin, a translation, the source, and a short psychology/philosophy gloss. There are **130 genuine, sourced maxims** (Seneca, Horace, Ovid, Cicero, Virgil, Publilius Syrus, classical proverbs and mottos). They rotate so every day shows a different one, with **no repeat for ~4 months** straight. Tap **Another** for extra firepower on any given day.

The **morning reminder** (06:30 by default) delivers that day's maxim right in the notification, so your first nudge of the day is a line of Latin firepower plus your intention prompt.


