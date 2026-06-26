# Loomrift Design Tokens

## Colors — Background Scale
| Token | Value | Usage |
|-------|-------|-------|
| `--bg` | `#090B12` | Page background, deepest layer |
| `--canvas` | `#0B0F17` | Graph canvas area |
| `--surface` | `#10151E` | Sidebar, panels, cards |
| `--elevated` | `#151B26` | Modals, dropdowns, context menus |
| `--hover` | `#1A2230` | Interactive hover state |
| `--selected` | `#202A3B` | Active/selected items |

## Colors — Border
| Token | Value | Usage |
|-------|-------|-------|
| `--border` | `#222B38` | Default borders |
| `--hairline` | `rgba(255,255,255,0.05)` | Subtle dividers |

## Colors — Text
| Token | Value | Usage |
|-------|-------|-------|
| `--fg` | `#F5F7FB` | Primary text |
| `--fg2` | `#8F99AB` | Secondary text, descriptions |
| `--fg3` | `#5A6373` | Tertiary, labels |
| `--fg4` | `#3A4250` | Disabled, muted |

## Colors — Accent
| Token | Value | Usage |
|-------|-------|-------|
| `--green` | `#75FF52` | Active, success, online |
| `--blue` | `#4FA7FF` | Primary accent, links, focus |
| `--orange` | `#FFC34D` | Warning, attention markers |
| `--purple` | `#8B5CF6` | Groups, creative |
| `--danger` | `#FF5B73` | Error, delete, critical |

## Typography
| Property | Value |
|----------|-------|
| Font | Inter |
| Weights | 400 (body), 500 (medium), 600 (semibold), 700 (bold) |
| Body | 13px / 20px |
| Label | 11px / 16px, letter-spacing 0.06em, uppercase |
| Heading | 16-17px / 24px, weight 600 |
| Caption | 11-12px / 16px |

## Spacing (8px grid)
`4 · 8 · 12 · 16 · 24 · 32 · 40 · 48 · 64 · 96`

## Radius
| Element | Value |
|---------|-------|
| Buttons | 8px |
| Cards | 12px |
| Panels | 16px |
| Floating/Modals | 20px |

## Shadows
| Level | Value |
|-------|-------|
| Soft | `0 1px 3px rgba(0,0,0,0.3)` |
| Medium | `0 4px 12px rgba(0,0,0,0.4)` |
| Strong | `0 10px 30px rgba(0,0,0,0.5)` |
| XL | `0 20px 60px rgba(0,0,0,0.6)` |

## Z-Index
| Layer | Value |
|-------|-------|
| Canvas (lc) | 1 |
| Three.js (c) | 2 |
| Hint | 10 |
| Sidebar/Panel | 15 |
| Topbar | 20 |
| UI Rail | 26 |
| Tooltip | 30 |
| Alert tip | 40 |
| Modal overlay | 60 |
| Crop overlay | 80 |
| Context menu | 100 |

## Motion
| Property | Value |
|----------|-------|
| Duration | 150-220ms |
| Easing | `cubic-bezier(0.16, 1, 0.3, 1)` |
| Fast | 150ms (hover, active) |
| Normal | 200ms (transitions) |
| Panels | 280ms (slide in/out) |
