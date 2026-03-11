# 🚀 LUNAR LANDER 3D — VECTREX

> A 3D wireframe lunar lander built in a single HTML file, rendered in authentic Vectrex phosphor-glow vector style.

> A 3D wireframe lunar lander game with Vectrex like phosphor-glow vector graphics. Full 6DOF physics with gravity, thrust and auto-leveling. Left stick tilts the lander, right stick orbits the camera freely, R3 provides smooth overhead view. Procedurally generated terrain. GPWS proximity system with color-coded blinking warnings. Claude generated.


**Built entirely by [Claude Sonnet 4.5](https://www.anthropic.com/claude) (Anthropic)**

---

## Play

Open `lunar-lander-3d.html` in any modern browser. No build step, no dependencies, no install.

---

## Controls

### Gamepad (recommended)

| Input | Action |
|---|---|
| **Left stick** | Tilt the lander (pitch / roll) |
| **Right stick** | Orbit camera freely |
| **R3** (right stick click, hold) | Smooth transition to overhead view |
| **L3** (left stick click) | Snap lander back to upright + RCS brake |
| **RT / R2** | Main engine thrust (analog) |
| **A / Cross** | Thrust (digital) / Start game |

### Keyboard (fallback)

| Key | Action |
|---|---|
| `← → ↑ ↓` | Tilt lander |
| `W A S D` | Orbit camera |
| `V` (hold) | Overhead view |
| `R` | Level the lander |
| `Space` | Thrust / Start |

---

## Gameplay

- You spawn above a procedurally generated lunar surface and must land on one of the **glowing cyan pads**
- Safe landing requires: low vertical speed, low horizontal speed, and a near-upright angle
- Fuel is limited — use thrust efficiently
- Score is based on fuel remaining and landing precision

### Difficulty (1–9)

The main difficulty lever is **terrain roughness**:

- **1–3** — gently rolling hills, two wide landing pads, generous fuel
- **4–6** — moderate ridges, medium pads
- **7–9** — jagged mountain ranges, one narrow pad, scarce fuel

Physics (gravity, thrust power, landing tolerances) also tighten slightly at higher difficulties, but terrain is the real challenge.

---

## GPWS — Ground Proximity Warning System

Altitude callouts every 10 metres from **100** down to **TERRAIN**, displayed below the attitude indicator. Colour transitions green → amber → red. Warnings below 30m blink with increasing urgency. A full red border flash triggers at ≤5m.

---

## HUD

| Element | Location | Description |
|---|---|---|
| **ATT** | Top centre | Artificial horizon — shows pitch and roll, pitch ladder, roll tick |
| **GPWS** | Below ATT | Altitude callout with chevrons |
| **Telemetry** | Left side | ALT, VY, SPD, score, difficulty |
| **Fuel bar** | Right side | Segmented bar, colour-coded by level |
| **Overhead bar** | Bottom centre | Progress indicator while R3 is held |

---

## Technical

- Pure HTML + CSS + JS, single file, ~1100 lines
- Custom software 3D renderer (no WebGL, no Three.js) with perspective projection
- Triple-pass phosphor glow on every vector line (outer bloom → mid glow → bright core)
- CRT scanline and vignette overlays
- Procedural terrain via layered sine waves, amplitude and frequency scaled by difficulty
- Particle systems for thrust, explosion, and landing sparks
- Full gamepad API support (standard mapping)

---

## Credits

Designed and coded by **Claude Sonnet 4.5** by [Anthropic](https://www.anthropic.com), through an iterative conversation — from a 2D Vectrex prototype to a full 3D game, one feature at a time.

---

*"TERRAIN. TERRAIN."*
