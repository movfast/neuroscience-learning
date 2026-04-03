# NeuroExplorer — Interactive 3D Brain Dashboard

## Overview
A single-page interactive neuroscience dashboard built with Three.js. Everything lives in one `index.html` file — no build tools, no dependencies to install.

## Project Structure
```
neuroscience_learning/
├── index.html    — the entire application (HTML + CSS + JS)
├── README.md     — project documentation
└── CLAUDE.md     — this file
```

## Architecture
The app is a single HTML file with three internal sections:
- `<style>` — CSS Grid dark-theme dashboard layout
- `<body>` — HTML structure (header, sidebar, viewport, bottom panel)
- `<script type="module">` — all JavaScript (Three.js scene, brain model, animations, interactivity)

Three.js is loaded via ES module import map from CDN (no local dependencies).

## Key Components

### Data
- `BRAIN_REGIONS` array — 10 regions with id, color, position, scale, descriptions, functions, fun facts, related regions
- `LEARNING_TOPICS` array — 6 topics with HTML content about learning neuroscience

### 3D Scenes
- **Brain Atlas** (`brainGroup`) — 10 ellipsoid meshes + translucent outer shell + background particles
- **Neural Activity** (`neuronGroup`) — cell body, axon (TubeGeometry), myelin sheaths, dendrites (recursive), signal sphere, neurotransmitter particles
- **How We Learn** (`learnGroup`) — two simplified neurons with animated signal pulse and synapse glow

### State
Plain JS object (`state`) manages active tab, selected region, hovered region, learning topic, animation speed, and mesh references.

### Interaction
- Raycasting for click/hover on brain regions
- OrbitControls for camera rotation/zoom
- Tab switching between three views
- Sidebar panels with detail content
- Keyboard shortcuts (1/2/3 for tabs, Escape to deselect)

### Animation
Single `requestAnimationFrame` loop handles:
- Region highlight animations (lerp opacity, emissive, scale)
- Camera target smooth transitions
- Neural signal propagation along axon curve
- Neurotransmitter particle physics
- Learning scene pulse animations
- 2D bottom-strip neural chain rendering
- HTML label projection from 3D to 2D

## Design System
- Background: `#0a0a1a` (deep navy)
- Primary: `#6c63ff` (indigo-violet)
- Secondary: `#00e5ff` (cyan)
- Tertiary: `#ff6b9d` (pink)
- Glassmorphism sidebar with backdrop blur

## Guidelines
- Keep everything in a single `index.html` — no external files except CDN
- Use Three.js MeshPhysicalMaterial for brain regions (organic look)
- All brain regions defined in `BRAIN_REGIONS` data array
- Labels are HTML overlays projected from 3D coordinates
- Responsive: CSS Grid collapses to single column on mobile
