# Loomrift Frontend Architecture

## Stack
- **Runtime**: Vanilla JS (no framework, no build step)
- **3D**: Three.js r128 via CDN
- **Rendering**: Two-canvas architecture (2D overlay + WebGL)
- **Persistence**: localStorage with versioned key
- **Deploy**: GitHub Pages via Contents API

## File Structure
```
index.html          — Single file, ~110KB
build2.py           — Python build script (source of truth)
working_js.txt      — Extracted verified JS
docs/               — Documentation
```

## Build Process
1. `build2.py` loads SVG assets from `/mnt/user-data/uploads/`
2. Base64-encodes them into JS `ICONS` object
3. Generates complete HTML with embedded CSS + JS
4. Output: `loomrift_clean.html` (~110KB)

## Deploy Process
1. `GET /repos/{owner}/{repo}/contents/index.html` → get SHA
2. `PUT` with base64 content + SHA → update file
3. GitHub Pages serves updated version

## Key Data Structures
- `nodeMap{}` — all nodes by ID
- `visN` Set — currently visible node IDs
- `expN` Set — expanded node IDs
- `effCol{}` — effective color per node (changes with mode)
- `sprO{}` — Three.js Sprite per node
- `hitO{}` — invisible hit-test Mesh per node
- `edgeData[]` — visible edges for current frame

## Rendering Pipeline (per frame)
1. Update camera position (spherical lerp)
2. Update node positions (lerp to target)
3. Update sprite scales/opacity
4. Three.js render (sprites)
5. `drawFrame()`: clear 2D canvas → draw grid → edges → path animation → alert badges → labels

## State Management
- Global variables (no store/reducer)
- `curMode` (1-4), `is2D`, `selId`, `hovId`, `alertFilter`
- Auto-save via `scheduleSave()` (debounced 800ms)
