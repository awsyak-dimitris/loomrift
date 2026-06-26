# Loomrift UX Rules

## Core
1. **Graph is the hero** — always visible, never hidden behind modals
2. **Prefer Inspector over dialogs** — use right panel for viewing/editing
3. **Prefer inline editing** — minimize modal workflows
4. **Keep users inside the graph** — reduce context switches
5. **Fast interactions** — everything responds within 200ms

## Navigation
- Click node → expand children, center camera, open inspector
- Right-click → context menu at cursor
- Sidebar tree → navigate structure, auto-reveal on click
- Camera auto-centers on clicked node

## Visual Hierarchy
- Root nodes: largest, most prominent
- Each level smaller: 32 → 20 → 16 → 14 → 11 → 9 → 8
- Depth shown by size, not just position

## Feedback
- Pulse ring on selected node
- Path animation shows traversal
- Save indicator confirms persistence
- Spawn animation for new nodes

## Mobile
- 1-finger: rotate (3D) / pan (2D)
- 2-finger: pinch zoom
- Long press: context menu
- Double tap: context menu on same node

## Avoid
- Modal-heavy workflows
- Blocking confirmations (use inline instead)
- Visual noise (no unnecessary glow, animation, or decoration)
- Generic dashboard patterns (cards with KPIs, data tables)
