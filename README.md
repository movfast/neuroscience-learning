# NeuroExplorer — Interactive 3D Brain Dashboard

An interactive web-based neuroscience learning dashboard with 3D brain visualization, animated neural activity, and comprehensive educational content about how the brain works and how we learn.

## Features

### Brain Atlas
- **10 brain regions** rendered as 3D translucent ellipsoids with anatomically accurate positioning
- Click any region to see detailed information: description, key functions, fun facts, and related regions
- Smooth camera transitions and highlight animations on selection
- Auto-rotating 3D model with orbit controls (drag to rotate, scroll to zoom)

### How We Learn
Six interactive topics explaining the neuroscience of learning:
- **Synaptic Plasticity** — how neural connections strengthen with use
- **Long-Term Potentiation** — the molecular mechanism of memory
- **Memory Consolidation** — how short-term memories become permanent
- **The Role of Sleep** — why sleep is essential for learning
- **Spaced Repetition** — optimal review timing for retention
- **Neurogenesis** — growing new neurons in the adult brain

Each topic includes animated 3D diagrams showing the underlying processes.

### Neural Activity
- Detailed 3D neuron model with cell body, dendrites, axon, and myelin sheaths
- Animated signal propagation demonstrating saltatory conduction
- Neurotransmitter particle burst at axon terminals
- Continuous 2D neural chain animation in the bottom strip

## Tech Stack
- **Three.js** — 3D rendering and animation
- **OrbitControls** — interactive camera control
- **Canvas 2D** — bottom-panel neural activity strip
- **Vanilla JavaScript** — no frameworks, no build tools
- **CSS Grid** — responsive dashboard layout

## Getting Started

Just open `index.html` in a modern browser. No installation or build step required.

```bash
# Clone and open
git clone https://github.com/movfast/neuroscience-learning.git
cd neuroscience-learning
open index.html
```

## Controls
| Action | Control |
|---|---|
| Rotate brain | Click + drag |
| Zoom | Scroll wheel |
| Select region | Click on region or sidebar card |
| Switch tabs | Click tab or press 1/2/3 |
| Deselect | Press Escape |
| Animation speed | Bottom-right slider |

## Live Demo

[https://movfast.github.io/neuroscience-learning/](https://movfast.github.io/neuroscience-learning/)

## License

MIT
