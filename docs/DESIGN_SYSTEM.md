# LOOMRIFT DESIGN SYSTEM v2.0

## Design Philosophy

Loomrift is not a dashboard. Loomrift is a visual operating system.

Every screen should feel like a professional desktop application used
daily by designers, developers and technical teams.

References: - Linear - Cursor IDE - Arc Browser - Figma - Unreal Engine
Editor - Obsidian Graph - Raycast

Avoid Bootstrap, Material Design and generic SaaS dashboards.

## Core Principles

-   Graph First
-   Calm Interface
-   Premium Desktop Feeling

## Visual Identity

Dark technical workspace. Large negative space. Thin borders. Soft
shadows. Restrained glow.

## Colors

Background #090B12 Canvas #0B0F17 Surface #10151E Elevated #151B26 Hover
#1A2230 Selected #202A3B Border #222B38 Hairline rgba(255,255,255,0.05)

Accent: Green #75FF52 Blue #4FA7FF Orange #FFC34D Purple #8B5CF6 Danger
#FF5B73

## Typography

Font: Inter Weights: 400,500,600,700

## Spacing

8px grid: 4,8,12,16,24,32,40,48,64,96

## Radius

Buttons 8 Cards 12 Panels 16 Floating Panels 20 Inspector 20

## Shadows

Layered shadows only. Glow only for active objects.

## Components

Sidebar: - VSCode inspired - Quiet hierarchy - Lucide icons

Top Navigation: - Compact - Search centered - Minimal

Graph: - Main hero - Readable at every zoom - Calm idle state

Inspector: - Docked right - Figma-like properties panel

Floating Toolbar: - Glass - Blur - Rounded

## Motion

Framer Motion 150-220ms Spring animations No bounce.

## Libraries

Base: shadcn/ui Motion: Framer Motion Graph: React Flow Enhancement:
Magic UI Accent: Aceternity UI

Adapt libraries to Loomrift style instead of default appearance.

## UX Rules

-   Graph is always the hero.
-   Prefer Inspector over dialogs.
-   Prefer inline editing.
-   Keep users inside graph.

## Accessibility

AA contrast. Keyboard navigation. Command palette.

## Performance

Avoid unnecessary rerenders. Animations never block interaction.

## Vision

Loomrift should feel comparable in quality to: - Linear - Cursor -
Figma - Arc - Unreal Engine
