# 🌎 PLANET ZERO — Retro Edition

A single-file, retro pixel-art planet simulator built with plain HTML, CSS, and JavaScript. Name your planet, manage its resources across five sectors, and survive random asteroid attacks.

No frameworks, no build step, no dependencies to install — just open the file and play.

---

## ▶️ How to Run

1. Download `planet-zero.html`.
2. Double-click it (or right-click → **Open with** → your browser).
3. It should open as a `file:///.../planet-zero.html` address — that's correct, you do **not** need a local server.
4. Type a planet name and click **▶ START ADVENTURE**.

Requires a modern browser (Chrome, Edge, Firefox, Safari). An internet connection is only needed to load the retro Google Font (`Press Start 2P`); everything else works fully offline.

---

## 🎮 How to Play

### The Planet View
Click the glowing planet to make it "come alive" (animation + sound). Below it are five **sector buttons**:

| Sector | Focus |
|---|---|
| 🏙️ CITY | Population, happiness, credits |
| 🌾 FARM | Food, environment |
| ⛏️ MINE | Minerals, credits |
| 🧪 LAB | Science |
| 🛡️ BASE | Defense, science |

### Inside a Sector
Each sector has 4 clickable buildings. Click one to open an action popup, then hit **DO ACTION** to:
- Trigger a big centered animated icon + a unique sound effect for that building (e.g. the Burger Shop shows a chomping burger with a crunch sound).
- Apply that building's effect to your stats (population, happiness, environment, science, credits, food, minerals, energy).
- Show floating `+`/`−` indicators for every stat that changed.

Click **◀ PLANET** to return to the main planet view.

### HUD
Top of the screen shows your planet name, current year, and live stats (population, happiness, environment, science, credits, food, minerals, energy).

### Day / Night Cycle
The sky automatically cycles between day and night, and a new "year" begins periodically — all shown in the HUD.

### ☄️ Asteroid Events
Random asteroid attacks can occur while you play (guaranteed once shortly after you start, and roughly a 55% chance each time you open a sector after that). When one hits:

1. A siren sounds and a red alert flashes as an asteroid animates toward the center of the screen.
2. You get **5 seconds** to complete a random quick-time challenge:
   - **PRESS [ X ]** — press the shown key, or
   - **TYPE "WORD"** — type the shown word into the box.
3. **Success** → shield animation deploys, asteroid is destroyed, and you gain `+5 happiness` / `+5 science`.
4. **Failure** (time runs out) → impact flash, screen shake, and you lose `-8 population`, `-10 happiness`, `-8 environment`.

### Keyboard Shortcuts
- **Enter** — start the game from the title screen.
- **Escape** — close the action popup.
- Any letter key or typed word — respond to an active asteroid challenge.

---

## 📁 Project Structure

This is a single self-contained file:

```
planet-zero.html   → HTML + CSS + JavaScript, all in one
```

If you'd rather split it into separate files for a larger project (e.g. `index.html`, `style.css`, `script.js`), just ask — but keep all three in the same folder if you do, since the HTML links to the other two by relative path.

---

## 🛠️ Tech Notes

- Pure vanilla HTML/CSS/JS — no libraries, no build tools.
- All sound effects are generated live with the Web Audio API (no audio files).
- All visuals are CSS gradients, box-shadows, and keyframe animations — no images.
- Game state lives entirely in memory (a single `state` object); refreshing the page resets progress.

---

## 🙌 Credits

- Font: [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) via Google Fonts.
- Built as a fun retro pixel-art sim — extend it with more sectors, buildings, or events as you like.
