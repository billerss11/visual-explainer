---
name: visual-explainer
description: Teach technical and scientific concepts through schematics, interactive demonstrations, or animations, including requested image/video exports. Use for visual explanations of mechanisms, processes, and quantitative relationships; not decorative art, general websites, or business dashboards.
---

# Visual Explainer

Choose the simplest visual that makes the concept clear. Infer audience and format; clarify only consequential gaps. Deliver the explanation unless the user asks only for advice.

## Delivery

- **Inline:** Load `visualize` when available; it owns rendering, styling, resource restrictions, controls, and validation. Keep host-specific code out of standalone files.
- **Standalone:** Use compact HTML/CSS/vanilla JavaScript, or the existing project's stack. Default to HTML if inline rendering is unavailable.
- **Static:** Export editable SVG or the requested raster format. Use standard plotting tools for publication-quality figures and image generation for illustrative bitmap art.
- **Video:** Export the actual requested file using existing tools or, when justified, Remotion with deterministic frame-based animation. HTML animation does not fulfill an MP4 request.

Publish or package for offline use only when requested.

## Technology selection

Combine only necessary layers; do not load this entire list.

| Need | Choice |
| --- | --- |
| Physical schematics, cross-sections, forces | SVG by default |
| Simple motion | CSS/native animation or requestAnimationFrame |
| Coordinated teaching sequences | GSAP |
| Dense particles, traces, fields | Canvas 2D; keep labels and controls accessible |
| Data-rich or linked plots | D3 + SVG/Canvas; plain SVG for simple values |
| Complex equations | Host math rendering or KaTeX; no dependency for simple expressions |
| Logic, workflows, state transitions | Mermaid; use SVG for physical geometry |
| Inspect an existing 3D asset | model-viewer + GLB/glTF; no automatic exploded-view assumption |
| Spatial relationships or assembly motion requiring 3D | Three.js + GLB/glTF rather than raw WebGL |
| Rigid-body dynamics | Rapier + renderer; not a CFD or stress solver |

## CDN-first policy

Assume internet access. Prefer native browser features, then version-pinned CDNs; reuse existing tools and dependencies. No new installations, environments, or build tools by default.

If existing tools/CDNs cannot satisfy the deliverable, explain the required installation and ask permission unless already explicitly authorized. This includes project-local packages and automatic downloads/installations through npx. Continue independent work while waiting.

Respect host CDN, CSP, and WebAssembly restrictions; use standalone output if necessary without weakening security. CDN resources still download/cache and are not guaranteed offline.

Verify unfamiliar/changing APIs in official documentation. Match Three.js core/addon versions and source. For Rapier without a bundler, use a pinned compatibility package with precompiled WebAssembly and await initialization; no Rust toolchain is required.

## Teaching and accuracy

- Use one dominant visual. For mechanisms, show input, relevant parts, transfer path, and outcome. Add only interactions that teach; omit decorative motion and unrelated metrics.
- Distinguish illustration, calculation, and validated simulation. Label consequential assumptions, illustrative values, non-scale geometry, and exaggerated motion. Use qualitative explanations when evidence is insufficient; verify uncertain claims with primary sources.
- Define units/signs and check governing relationships. Drive geometry, equations, and plots from shared state. Do not invent thresholds, material properties, or validation.
- For CAD, check available importers/converters and distinguish approximate reconstructions from supplied geometry.
- Keep labels direct, readable at narrow widths, and consistent across states. Pair color with text/shape; provide keyboard access, reduced-motion behavior, accessible descriptions, and readable fallbacks when rendering fails. Keep essentials visible without hover.

## Verify and deliver

For standalone interactive output, use an available browser tool to inspect normal/narrow layouts, exercise the main interaction, and check asset/script errors. For calculations, check a representative result and relevant boundaries. Avoid new test frameworks for one-off visuals.

Follow `visualize` for inline validation. Inspect exported images; check video duration, dimensions, representative frames, and playback when possible. Disclose unperformed checks.

Deliver the requested format with a brief explanation of what to notice. Link standalone files with necessary launch instructions; mention material assumptions and network requirements when relevant.
