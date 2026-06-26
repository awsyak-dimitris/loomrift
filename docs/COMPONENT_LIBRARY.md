# Loomrift Component Library

## App Shell
- Full viewport, no scroll on body
- Topbar (48px) + content area
- Sidebar slides from left (260px)
- Inspector panel slides from right (300px)

## Topbar
- Height: 48px
- Glass effect: `backdrop-filter: blur(16px)`
- Contains: burger, logo, mode buttons, view toggle
- Buttons: `.btn` outline style, `.btn.active` with accent tint

## Sidebar (Tree)
- VSCode-inspired file tree
- Collapsible sections
- Row height: 28px
- Indent: 16px per level
- Shows: arrow, icon, status dot, name, role, alert badge

## Inspector Panel (Right)
- Width: 300px
- Sections: avatar, name/role, status rows, entity fields, AI summary, actions
- Entity-aware: shows person fields (phone, email, socials) or org fields (website, industry)
- Actions: Edit, Add child, Delete

## Graph Canvas
- Two layers: 2D canvas (grid, lines, labels) + Three.js (sprites)
- Node shapes: circle, triangle, star, square, hexagon, main
- SVG icons with color compositing (`source-in`)
- 30% opacity color fill inside shapes

## Context Menu
- Right-click or long-press
- Dropdown style with animation
- Contains: toggle, edit, add, alert markers, delete
- Alert buttons: `!` (orange), `?` (blue), `★` (green), `✕` (clear)

## Modal / Dialog
- Centered overlay with backdrop blur
- Animation: scale 0.95→1, translateY 8→0
- Form fields: name, role, shape, status, avatar, parent
- Radius: 20px (floating panel)

## Avatar Crop Modal
- Drag-to-pan, zoom controls
- Circle crop ring (210px)
- Touch support

## FAB (Floating Action Button)
- Bottom-left rail, fixed position
- Creates new root node
- Accent color, 44px circle

## Toast / Save Indicator
- Fixed bottom-left
- Shows "✓ Сохранено" briefly after save
