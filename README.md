# FORGE — *Forge the self*

A Progressive Web App for building an unbreakable daily routine around training, eating well, and steadying your mind. It combines **identity-based habit design**, **Stoic philosophy**, and the **3·3·3 eating framework** into a single, offline-capable app you can install on your phone.

> You do not rise to your goals. You fall to your systems. FORGE is the system.

---

## What it is

FORGE is a single, self-contained web app (no accounts, no server, no tracking). All your data lives privately on your own device. Install it to your home screen and it behaves like a native app — it opens full-screen, works offline, and can send you reminders.

The design language is **"neon dusk"**: a deep indigo base with electric violet, hot pink, and cyan accents, a literary serif (Fraunces) for the Stoic voice, and a clean grotesque (Hanken Grotesk) for the interface.

---

## The idea

Motivation is unreliable, so FORGE is built on systems instead:

- **Identity over outcomes.** You don't chase "lose weight"; you become *"someone who trains daily and eats with intention."* Every completed action is logged as a vote for that identity.
- **Stoic discipline.** Focus on what you control (showing up, your effort, your meals) and accept what you don't (the scale, soreness, other people). Embrace the hard thing on purpose.
- **Start ridiculously small.** The keystone habit is just *showing up* for ten minutes. Master that, and intensity follows.
- **Design the environment.** Make the good choice easy and the bad choice hard.

---

## Features

### Today
- **Identity banner** — who you're becoming, and your *why*.
- **Maxim of the Day** — a daily Latin maxim with translation, source, and a psychology/philosophy note, drawn from a library of **130 sourced maxims** (Seneca, Horace, Ovid, Cicero, Virgil, Publilius Syrus, and classical proverbs). New one each day, no repeat for ~4 months. Tap **★** to save it; tap **↻ Another** for more.
- **Streak strip** — day streak, identity votes, and best run.
- **Rank bar** — your current Roman rank and progress to the next.
- **The keystone** — one tap: *"I showed up · 10 min."*
- **Show-up timer** — 2 / 10 / 20 / 30-minute countdown; finishing it auto-logs the session.
- **"I don't feel like it"** — surfaces your identity, your why, a Stoic reframe, and a 2-minute timer to break the inertia.
- **The 3·3·3 Plate** — three balanced meals, each marked for protein, healthy fat, and fibre/complex carb.
- **3 litres by 3 PM** — a tap-to-fill hydration tracker.
- **Today's cues** — your implementation intentions, habit stacks, and temptation bundles.
- **Tonight's prep** — a nightly environment-design checklist that resets each day.
- **Never miss twice** — a recovery banner that appears only after a missed day, with a stronger nudge after two ("this is where habits die"). It disappears the moment you show up.

### System
- Set your **identity** and **why**.
- **Implementation intentions** — *"I will [behaviour] at [time] in [place]."*
- **Habit stacks** — *"After I [existing habit], I will [new habit]."*
- **Temptation bundling** — pair a should-do with a want-to-do.
- **Environment prep** — your editable nightly checklist.
- **Reminders & alarms** — editable times with on/off toggles; in-app nudges, plus per-reminder **calendar (.ics) export** for alarms that fire even when the app is closed.
- **Commitment contract** — sign a promise to your future self.
- **Data & memory** — export a backup, restore from one, or reset.

### Reflect
- **Morning premeditation** — what's in your control today.
- **Discomfort training** — a daily voluntary-hardship challenge.
- **Evening reflection** — where you acted on your values, and where you fell short.

### Progress
- **Don't break the chain** — a 35-day heatmap coloured by how many pillars you hit.
- **The Ledger** — totals: days shown up, current streak, full-plate days, hydrated days, total minutes, hard things done.
- **The Cursus · Ranks** — a cumulative rank ladder (Tiro → Miles → Legionarius → Decanus → Optio → Centurio → Primus Pilus → Tribunus → Legatus → Imperator). Rank only ever rises.
- **Trends** — weekly minutes vs. the 180-min goal, pillars hit over 14 days, 30-day consistency, and an automatic behavioural insight when there's enough data.
- **The Memory** — your full journal of past reflections and wins.
- **Saved Maxims** — the maxims you've starred.

### Anchor
A section for the hard days — when you can't see your own worth:
- A grounding **box-breathing** exercise (in 4, hold 4, out 4, hold 4).
- **The kinder, truer voice** — reframe the harsh thought as you would for a friend.
- **The Worth Ledger** — log small, real evidence of your value and read it back when the low voice lies.
- **One small, kind thing** — a single tiny action to create momentum.
- **Reach out** — save a trusted person one tap away, plus signposting to support.

### Codex
A reading library (opened from the book icon in the header) for long-form pieces on strategy and philosophy.

---

## The psychology, mapped

| Technique | Where it lives in FORGE |
|---|---|
| Identity-based habits (James Clear) | Identity banner, "identity votes", ranks |
| Implementation intentions | System → Intentions, surfaced as Today's cues |
| Habit stacking | System → Habit stacks |
| Temptation bundling | System → Temptation bundling |
| Environment design | Tonight's prep checklist |
| Start ridiculously small | The keystone (10-min show-up), show-up timer |
| Never miss twice | Recovery banner |
| Stoic dichotomy of control | Morning premeditation, daily Stoic card |
| Amor fati / voluntary hardship | Discomfort training |
| Self-compassion & cognitive reframing | Anchor section |
| 3·3·3 eating & hydration | The Plate, 3 litres by 3 PM |

---

## Install & run

A PWA must be served over **HTTPS** (or `localhost`) for install and offline features to work.

**Deploy (recommended):**
1. Create a free account on **Netlify** (or Vercel / Cloudflare Pages / GitHub Pages).
2. Drag this whole folder onto the deploy drop-zone.
3. Open the URL it gives you on your phone.
   - **iPhone (Safari):** Share → *Add to Home Screen*.
   - **Android (Chrome):** tap the *Install* prompt, or ⋮ → *Install app*.

**Test locally:**
```bash
cd forge
python3 -m http.server 8080
# open http://localhost:8080
```

---

## Quick start

1. **System** → name your identity and *why*, add one implementation intention and one habit stack.
2. **Today** → read the maxim, then tap *I showed up* (or run the timer). Tick the plate, fill the water drops.
3. **Reflect** → two lines in the morning, two at night.
4. **Progress / Anchor** → check your trends, or steady yourself on a hard day.

---

## Privacy & data

- No accounts, no analytics, no servers. Everything is stored locally in your browser (`localStorage`).
- Use **System → Export** to back up your data as a file, and **Restore** to move it to a new device.
- Reminders are scheduled on-device; nothing leaves your phone.

---

## A note on alarms

Phone browsers — especially iOS Safari — **cannot reliably wake a closed web app to ring an alarm on time.** That's an operating-system limitation, not a fault in FORGE. So reminders work in two layers:

- **In-app nudges** fire at your chosen times while FORGE is open (and, on supported browsers like installed Chrome/Edge, when it's closed too).
- **Calendar (.ics) alarms** — tap **＋cal** on any reminder to drop a repeating alarm into your phone's Calendar/Clock, which *will* fire when the app is closed.

Use both for full coverage. The **morning reminder** also delivers that day's Latin maxim in the notification.

---

## Tech notes

- Vanilla HTML, CSS, and JavaScript — **no build step, no dependencies**.
- Files:
  - `index.html` — the entire app (markup, styles, logic).
  - `manifest.json` — PWA metadata for installability.
  - `sw.js` — service worker (offline caching + notifications).
  - `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` — app icons.
- Theming is driven by CSS custom properties, so the whole palette can be re-skinned from one place.

---

## If something looks off

This is a self-contained app; the most reliable way to capture or share a screen is to open it on your own device and screenshot it. If a reminder doesn't fire while the app is closed, that's the OS limitation above — use the calendar alarm.

*Per aspera ad astra.*
