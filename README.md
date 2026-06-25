# VOID RUNNER 🚀

> *How long can you survive?*

A browser-based sci-fi survival game built entirely in a **single HTML file** — no dependencies, no build step, no installs. Open it and play.

---

## Gameplay

You are a glowing cyan ship on the left side of the screen. Obstacles fly in from the right at increasing speed. Don't touch them. Survive as long as possible.

| Control | Action |
|---|---|
| `↑` / `W` | Move up |
| `↓` / `S` | Move down |
| `Space` | Start / Restart |

---

## Features

### Obstacle Types
| Color | Type | Behavior |
|---|---|---|
| 🔴 Red/Orange | Normal | Standard wall pair |
| 🔵 Blue/Cyan | Moving | Oscillates up and down |
| 🟣 Purple | Gap | Three-piece column with two 80px gaps |
| 🟡 Gold | Fast | 2× speed, thinner, preceded by a WARNING flash |

### Scoring System
- Score increases every frame, scaled by your **score multiplier**
- **Score multiplier** starts at 1x and gains +0.5x every 15 seconds
- **Close Call Bonus** — pass within 10px of an obstacle without dying: `+50 × multiplier`
- **Level Up** every 500 points — background tint shifts and an animation fires
- **High score** saved to localStorage and displayed on the menu

### Progression
- Obstacles speed up every 10 seconds
- Engine drone pitch rises with speed — the game *sounds* more tense as it gets harder
- Speed lines appear after 30 seconds of survival

### Visual Effects
- Pulsing cyan player with motion trail
- Particle explosion on death (cyan fragments)
- Screen shake on death
- 100 drifting parallax stars
- CRT scanlines + radial vignette
- Animated neon title on the menu with decorative background obstacles

### Audio (Web Audio API — no external files)
- **Engine drone** — triangle wave power chord at 90+135Hz with sub-bass, LFO heartbeat pulse, pitches up as speed increases
- **Obstacle approach** — low doppler rumble every time an obstacle spawns
- **Close call whoosh** — air-tear sound on near misses
- **Death explosion** — filtered noise burst
- **Level up** — ascending four-note chime

---

## How to Run

Just open `void-runner.html` in any modern browser. That's it.

```bash
# Or serve locally if you prefer
npx serve .
```

---

## Share

On the game over screen, hit **📋 Share Score** to copy:
> *"I survived Xs in VOID RUNNER and scored N! Can you beat me? Play at vcac-app.vercel.app 🎮"*

---

## Built With

- Vanilla HTML/CSS/JS — zero frameworks
- Canvas 2D API for rendering
- Web Audio API for all sound design
- localStorage for high score persistence

---

*Built with AI — Submit yours at [vcac-app.vercel.app](https://vcac-app.vercel.app)*
