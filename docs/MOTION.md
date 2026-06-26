# Loomrift Motion Guidelines

## Principles
- Subtle, never distracting
- 150-220ms duration
- ease-out curve: `cubic-bezier(0.16, 1, 0.3, 1)`
- No bounce, no overshoot
- Animations never block interaction

## Durations
| Context | Duration |
|---------|----------|
| Hover states | 150ms |
| Button press | 150ms |
| Panel slide | 280ms |
| Modal appear | 250ms |
| Context menu | 150ms |
| Node spawn | 400ms |
| Camera move | lerp 0.07-0.09/frame |

## Easing
- Default: `cubic-bezier(0.16, 1, 0.3, 1)` (spring-like)
- Hover/Active: `ease-out`
- Camera: linear lerp

## Node Animations
- Spawn: scale 0→1 with bounce overshoot (`sv=1.7`)
- Fade: opacity lerp
- Position: `pos.lerp(targetPos, 0.09)`
- Pulse ring: on selected node, repeating

## Path Animation
- Dot travels along edges root→leaf
- Duration: 1.2s travel, 3.5s cycle
- Flicker: `0.7 + sin(t*0.018) * 0.3`
- Dashed trail with animated offset

## UI Animations
- Panels: `transform: translateX(±100%)` → `0`
- Modals: `scale(0.95) translateY(8px)` → `scale(1) translateY(0)`
- Context menu: `scale(0.95) translateY(-4px)` → `none`
- Save indicator: opacity 0→1→0
