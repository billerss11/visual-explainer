# Visual Explainer

A reusable agent skill for understanding concepts and documents through visuals. Rewritten from the user's original skill and requirements, with online research checked on September 11, 2026.

## Files

```text
visual-explainer/
  SKILL.md                         Core instructions
  references/
    document-workflow.md           Long reports and changing systems
    browser-notes.md               CDN, 3D, physics, and export details
  evals/
    CASES.md                        Prompts and expected behaviors
  README.md                        This guide and research notes
```

`SKILL.md` contains the essential workflow and constraints. The two references are loaded only for relevant tasks. The core also works without them; the complete folder supplies extra implementation and source-handling guidance. The README and behavior checks are for maintenance, not required reading on each invocation.

## Use

Keep the folder name `visual-explainer` and the file name `SKILL.md`. Add this folder through the skill mechanism supported by your agent, or provide `SKILL.md` as instructions in a host that does not support skill folders. Host-specific registration is not performed by this download.

Example requests:

> Use visual-explainer to help me understand this operation report. Start with the overall sequence, then explain the main events visually.

> Use visual-explainer to explain buoyancy with Three.js and Rapier through CDN. Do not install anything.

> Use visual-explainer to show how a television displays an image. Choose the visual format that explains it best.

The skill does not add tools to an agent. Browser inspection, file creation, image generation, and video export depend on capabilities already available in the host. A host-specific `visualize` skill is optional, not a package to install.

## Setup policy

The default is native browser functionality or browser-ready libraries loaded from version-pinned CDNs. No package manager, framework scaffold, Rust toolchain, converter, or new runtime is required merely to adopt the skill. Existing project dependencies remain usable.

CDN loading still downloads code and normally needs internet access. A no-build page may need an existing local server because of module/asset security rules. A request for a library or video format is not blanket permission to install software. The skill requires an explicit explanation and approval for an otherwise unavoidable installation.

## Research and design choices

| Research source | What informed this rewrite |
| --- | --- |
| [Agent Skills specification](https://agentskills.io/specification) | Standard YAML frontmatter, a matching folder/name, and shallow optional references. |
| [Agent Skills creator guidance](https://agentskills.io/skill-creation/best-practices) | Clear defaults, limited scope per instruction, and task-specific details instead of an exhaustive manual. |
| [Anthropic authoring guidance](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) | Discoverable descriptions, concise instructions, and conditional resource loading. |
| [Anthropic skill-creator example](https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md) | Concrete behavior checks, evaluation against real requests, and refinement rather than assuming a first draft is validated. |
| [nicobailon's visual-explainer](https://github.com/nicobailon/visual-explainer/blob/main/plugins/visual-explainer/SKILL.md) | A real visual-explanation skill with HTML delivery and representation/reference routing. This rewrite does not adopt its host-specific integrations, branding rules, or automatic table-to-page threshold. |
| [Three.js manual](https://threejs.org/manual/), [Rapier JavaScript setup](https://rapier.rs/docs/user_guides/javascript/getting_started_js/), and [MDN modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) | Browser loading constraints, consistent imports, no-bundler Rapier initialization, and honest launch requirements. |

This is newly written guidance, not a copy of another skill. The user's original no-install preference, broad teaching objective, and supplied well-activity report determine the substance. Library-specific notes include further official documentation links; they are not frozen API recipes or claims about the latest package versions.

The report informed safeguards for changing configurations, mixed measurement bases, and the difference between attempted work and confirmed results. The original report and its full contents are not included in the package.

## Validation status

Package checks cover YAML/name/description validity, relative reference targets, Markdown structure, and archive integrity. The behavior prompts are supplied for evaluation in the intended host. No independent agent benchmark, host installation test, or generated HTML/image/video runtime suite has been completed as part of this rewrite. These are skill instructions, not a prebuilt simulation.
