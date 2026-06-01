# Solar System Explorer

An interactive, single-file 3D planetarium built with Three.js. It now leans into a calm lofi observatory mood: slower orbital pacing, soft glass panels, cinematic drift, safe outside-body camera following, realistic planet tints, atmospheric glows, comet coma/tails, ambient dust, guided tours, search, snapshots, adaptive rendering, realistic light-travel visualization, true-scale mode, textured worlds, moons, an asteroid belt, and Halley's Comet.

## Highlights

- **Interactive 3D simulation** — Explore all 8 planets, Pluto, key moons, Halley's Comet, Saturn's rings, and a 3,000-particle asteroid belt.
- **Lofi observatory cockpit** — Live focus, scale, camera distance, FPS, adaptive quality status, and responsive glass UI designed to stay calm and unobtrusive.
- **Multilingual cockpit** — Switch instantly between English, Italian, and Spanish for primary controls, science copy, command search, tour narration, and alerts.
- **Discovery Dossier** — Selecting a world now opens a companion science brief with habitability/exploration meters, mission badges, translated facts, and historical milestones.
- **Slow guided Grand Tour** — Press **T** or use the **◎ TOUR** button for a curated story-driven flythrough across the solar system with gentle outside-body camera tracking.
- **Command palette** — Press **Ctrl/⌘ + K** to search bodies, jump camera presets, launch science modes, or export a snapshot.
- **Togglable lofi radio** — Open **♫ RADIO** for low-volume SomaFM downtempo, space ambient, and drone streams with backup URLs.
- **Comfort submenu** — Open **☰ QOL** for follow-after-close, idle drift, UI dimming, release focus, home view, and quick overlay controls.
- **Camera presets** — Keys **1–5** jump between inner-system, outer-system, top-down, ecliptic, and hero flyby views.
- **Planet intelligence panels** — Click any body for diameter, distance, day/year length, moons, gravity, temperature, orbital speed, mission history, facts, and a slowly orbiting camera that keeps you safely outside the world.
- **Realistic visual treatment** — Texture color management, calmer true-to-body tints, atmosphere glows, Earth day/night/cloud layers, Saturn rings, and a dark Halley nucleus with separate blue ion and golden dust tails.
- **Light-travel mode** — Visualize sunlight expanding outward and compare arrival times at each world.
- **True-scale mode** — Morph from presentation scale into astronomical spacing and relative radii.
- **Snapshot export** — Capture the current view as a PNG from the cockpit.
- **Relaxation-first polish** — Reduced-motion support, responsive controls, keyboard shortcuts, live UI readouts, fixed high-DPI text sprites, and slower default motion.

## Controls

| Action | Control |
| --- | --- |
| Orbit / pan / zoom | Mouse left / right / scroll |
| Select body | Click a planet, moon, comet, or star |
| Command palette | **Ctrl/⌘ + K** |
| Guided tour | **T** or **◎ TOUR** |
| Lofi radio | **♫ RADIO** button |
| Comfort menu | **☰ QOL** button |
| Camera presets | **1**, **2**, **3**, **4**, **5** |
| Play / pause | **Space** |
| Slow cinematic follow | Click any planet, moon, comet, or star |
| Labels | **L** |
| Orbit lines | **O** |
| Fullscreen | **F** |
| Snapshot | **📷 SNAP** |
| Language | **EN / IT / ES** selector |

## Running locally

This is a standalone static site. Any simple HTTP server is enough:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

> A local server is recommended because browser security policies are stricter when opening `index.html` directly from disk.

## Technical Details

- **Engine**: Three.js r134 via CDN
- **Controls**: `THREE.OrbitControls`
- **Rendering**: WebGL with logarithmic depth buffer, ACES tone mapping, adaptive pixel ratio, and responsive HUD overlays
- **Localization**: In-file i18n dictionary for English, Italian, and Spanish with persisted language preference
- **Textures**: Solar System Scope maps are loaded without forced CORS and backed by self-contained procedural fallbacks
- **Audio**: Optional user-started SomaFM direct MP3 radio streams with backup URLs
- **Deployment**: Static-site ready, including GitHub Pages

## Credits

Primary texture maps are provided by [Solar System Scope](https://www.solarsystemscope.com/textures/) under the Creative Commons Attribution 4.0 license. The app also generates procedural fallback textures in-browser so the scene remains visible if remote images are unavailable.
