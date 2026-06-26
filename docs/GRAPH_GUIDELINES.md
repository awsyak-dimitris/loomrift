# Loomrift Graph Guidelines

## Node Types
- **Root nodes**: parentId=null, largest size (28-32), independent subtrees
- **Level 2**: departments/projects (16-20)
- **Level 3-4**: teams/roles (11-14)
- **Level 5-6**: individuals (8-9)

## Layout
- `placeTree()`: recursive radial layout from each root
- `resolveCollisions()`: spring-based push-apart (5 iterations)
- Multiple roots arranged in arc around center
- 2D mode: horizontal layout with vertical drop

## Node Rendering
1. SVG icon loaded and cached in `imgC[]`
2. `mkTex()` draws on 128x128 canvas
3. Avatar path: clip circle → draw image → stroke border
4. Icon path: drawImage → source-in composite → color fill → 30% overlay
5. Result → `THREE.CanvasTexture` → `THREE.Sprite`

## Edges
- Drawn on 2D canvas overlay each frame
- Shortened by node radius at both ends
- Level 4+ edges use dashed lines
- Color matches child node color

## Labels
- Drawn on 2D canvas (not 3D sprites)
- Role above, name below
- Scale with screen radius
- Fade when node < 8px screen size
- Text shadow for readability

## Interactions
- Click: expand/collapse children + center camera
- Right-click: context menu
- Hover: show tooltip, highlight node
- Touch: 1-finger rotate, 2-finger zoom, long-press = context menu

## Color Modes
1. **Статус**: nodes colored by status (green/yellow/red/gray)
2. **Фокус**: clicked node + ancestors + descendants colored, rest dimmed
3. **Группы**: colored by group, click group to highlight
4. **Все**: monochrome

## Alert Markers
- `!` (orange), `?` (blue), `★` (green)
- Drawn as canvas badges outside node edge
- Filter button cycles through types

## Path Animation
- Running dot along path from root to clicked leaf
- Dashed trail with flicker effect
- Repeats every 3.5 seconds

## Camera
- Spherical coordinates: theta, phi, r
- Smooth lerp (0.07-0.09)
- Click on node → camera pans to center on it
