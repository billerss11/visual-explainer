# Browser implementation notes

Read only the relevant sections. Verify current official documentation for the chosen version before copying API patterns. No library below is required merely because it appears here.

## Loading and launch

Prefer the library's documented browser build: a classic script bundle or an ES module. Use an import map for bare module names. Avoid mixing global-script examples, CommonJS `require`, and ES-module exports. Pin library/plugin versions and check transitive imports, CSS, fonts, workers, WASM, and asset paths as needed.

Test from the same launch mode being handed to the user. Modules or local asset loading may need HTTP even in a no-build project. Prefer the existing host preview. If Python is already installed, its standard-library server is a no-package-install option: run `python -m http.server 8000 --bind 127.0.0.1` from the artifact's directory, then open `http://127.0.0.1:8000/`. Do not require a new runtime just to preview a simple diagram.

When loading fails, retain the explanation/static view and show a useful error. Do not endlessly swap CDNs or weaken CSP/CORS. Escape source text before inserting it into HTML; do not execute document content.

Official reference: [MDN JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules).

## Three.js and model-viewer

Use one exact Three.js version and CDN for core and addons. Resolve `three` and `three/addons/` consistently; import loaders and controls explicitly. Fit the camera to the subject, resize with the container, and provide a reset viewpoint. Use basic geometry for an openly labeled schematic; use supplied GLB/glTF when asset fidelity matters.

For inspecting an existing model, prefer model-viewer when its controls and annotations suffice. An exploded view requires separable parts and meaningful transforms; a flattened mesh does not supply them automatically. STEP/IGES/SolidWorks files are not GLB/glTF: check available importers/converters and obtain approval for any installation or external upload.

Official references: [Three.js manual](https://threejs.org/manual/), [model-viewer](https://modelviewer.dev/).

## Rapier

For a no-bundler browser setup, use a version-pinned `@dimforge/rapier2d-compat` or `@dimforge/rapier3d-compat` browser import. These packages embed precompiled WASM; await `RAPIER.init()` before creating the world. No Rust compilation is needed for this path.

Separate physics units from display scale. Use a fixed simulation timestep and synchronize rendered transforms from physics bodies. Keep stepping independent of display refresh rate; reset the world, accumulated time, and plots together. Check collider dimensions, masses, gravity, and joint constraints against the intended model.

For a scrubbed sequence, use saved states or reproducible replay rather than pretending a rigid-body world can jump arbitrarily in time. For buoyancy, drag, or other forces outside the contact model, supply and disclose the governing equations; water-looking graphics do not create fluid physics. Browser dynamics are not evidence of stress capacity or failure thresholds.

Official references: [Rapier JavaScript setup](https://rapier.rs/docs/user_guides/javascript/getting_started_js/), [common mistakes](https://rapier.rs/docs/user_guides/javascript/common_mistakes/).

## Charts, motion, logic, and equations

| Tool | Use it when | Avoid |
| --- | --- | --- |
| [Plotly](https://plotly.com/javascript/getting-started/) | Standard interactive scientific plots reduce custom code | Invented readings, unlabeled axes, misleading interpolation |
| [D3](https://d3js.org/getting-started) | Custom scales, geometry, or linked selections are central | A bespoke charting system for three simple values |
| [GSAP](https://gsap.com/docs/v3/Installation/) | Several explanatory elements must move in coordination | Multiple independent clocks fighting shared state |
| [Mermaid](https://mermaid.js.org/intro/getting-started.html) | Logical flows, sequences, and state relationships | Equipment geometry, physical dimensions, unlabeled relationships |
| [KaTeX](https://katex.org/docs/browser) | Complex notation needs mathematical typesetting | Missing matching CSS/fonts or treating typesetting as calculation |

Use native animation for simple transitions. For dense Canvas graphics, keep labels/controls in HTML or SVG, and separate pixel resolution from physical coordinates. Reuse chart instances rather than recreating them every frame.

## Images and video

Inspect generated images for incorrect connections, impossible geometry, labels, and misleading scale. Use precise overlays where needed; use an available image-generation tool rather than returning only a prompt. Generated imagery remains illustrative even when photorealistic.

Prefer existing export tools. For exact motion, define each frame from time/frame index; avoid wall-clock animation in a frame renderer. Remotion is an option for an existing or authorized React/video toolchain, not a default CDN-only MP4 exporter. Verify the encoded output; do not rename WebM to MP4 or claim that browser playback proves video export.

Official reference: [Remotion fundamentals](https://www.remotion.dev/docs/the-fundamentals).
