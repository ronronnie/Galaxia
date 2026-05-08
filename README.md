# Galaxia

A procedural spiral galaxy rendered in real time — 159,000 stars, 5 spiral arms, music sync, warp travel, and a wormhole effect. All in a single HTML file.

**[Live Demo](https://ronronnie.github.io/Galaxia)**

---

## Features

### Galaxy
- 159,000 procedurally generated stars across 5 spiral arms
- Differential orbital speeds — inner stars orbit faster than outer ones
- Cinematic formation reveal on load
- Real-time 60fps WebGL rendering via Three.js and custom GLSL shaders

### Navigation
- **Drag** to orbit the galaxy
- **Scroll** to zoom in/out
- **Click** anywhere to travel to that point
- **Camera presets** — Top-down, Equatorial, and Dive views
- **Hold W** for warp speed (lightspeed streak effect)
- Auto-rotate with idle resume

### Music Sync
Beat-reactive visuals powered by the Web Audio API:
- **Stars pulse** and swell on every beat
- **Bloom flares** spike on downbeats
- **Color tint** shifts warm on bass, cool on treble
- **Rotation speed** rises with musical energy

Built-in genres (simulated audio):

| Genre | BPM |
|-------|-----|
| Lofi | 80 |
| Space / Ambient | 60 |
| Synthwave | 130 |
| Focus | 100 |
| Jazz | 120 |
| Classical | 72 |

Also supports **local file upload** (any audio file) with real FFT analysis via the Web Audio API.

### Themes
10 color themes with smooth tint transitions:

| Theme | Style |
|-------|-------|
| Milky Way | Warm white (default) |
| Andromeda Neon | Cyan-green |
| Synthwave | Magenta-purple |
| Monochrome | Desaturated blue |
| Solar Flare | Deep orange |
| Arctic | Pale blue |
| Golden Hour | Amber |
| Infrared | Red |
| Ultraviolet | Indigo |
| Copper | Warm copper |

### Effects
- **Wormhole** — cinematic dive-through with a lightspeed tunnel
- **Warp streaks** — star trails while holding W
- **Travel ripple** — click-to-travel with an expanding ring
- **Grain & vignette** — subtle film grain post-processing
- **Frequency visualizer** — FFT bars (real audio) or animated waveform (simulated)

### HUD
- Live FPS, star count, arm count, camera distance, simulation time
- Toast notifications
- Screenshot capture
- Fullscreen toggle

---

## Tech Stack

- [Three.js](https://threejs.org/) — 3D scene, camera, controls
- **WebGL / GLSL** — custom vertex + fragment shaders for stars, warp streaks, and the lightspeed tunnel
- **Web Audio API** — real FFT analysis for uploaded tracks
- YouTube IFrame API — genre radio streams

---

## Running Locally

No build step required. Just serve the folder:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

Or use any static file server.

---

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `W` (hold) | Warp speed |
| `T` | Cycle theme |
| `M` | Toggle music player |
| `F` | Fullscreen |
| `S` | Screenshot |
| `?` | Show all shortcuts |

---

Built by **Ron Anthony** · Three.js / WebGL / GLSL
