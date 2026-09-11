# Source-grounded document workflow

Use for long reports, operational histories, specifications, or systems that change over time. Apply only the steps relevant to the user's question.

## Extract before illustrating

1. Establish coverage: document identity/revision, available pages or date range, and the question being answered. For a whole-document overview, inspect its full structure and major phases before choosing details. Do not imply complete coverage from a few retrieved passages.
2. Build a compact working record of the important entities, relationships, events, and values. Retain source locations and original expressions. Use structured data when needed for many linked views, not as a mandatory extra deliverable.
3. Separate observations, operator actions, proposed explanations, and recorded outcomes. Read relevant later entries for confirmation or correction. Preserve competing explanations when the evidence does not resolve them.
4. Select a few explanatory views: an overview of phases, a system/section view, and focused event or mechanism views. Expand only the operations needed to understand the story; compress routine repetitions without hiding important failures or configuration changes.

A useful record shape is:

```text
source location | event time/order | entity/action | before -> after
value + unit + reference basis | evidence status | unresolved issue
```

## Reconstruct states, not a single timeless picture

- Track installation, removal, replacement, open/closed states, connections, and verified outcomes. Draw the configuration for the selected time; do not combine equipment from different campaigns into one supposed actual arrangement.
- Preserve unknowns. An absent component in the record is not proof it was absent in reality. A successful pressure test is evidence about the stated test, not proof of every possible barrier or load case.
- For an event, show **observation -> recorded response -> recorded outcome**. Add an explanatory mechanism separately and label it when inferred. A generic teaching animation is not a historical replay.
- Keep measured samples separate from interpolated transitions. Mark compressed time and gaps. Do not manufacture a continuous pressure/temperature trace from occasional readings, or infer exact task durations from coarse daily entries.

## Keep measurements comparable

Retain the measurement basis, not just the number. Examples include measured versus true vertical depth; pipe, wireline, or coiled-tubing measurements; depth below mudline versus a rig datum; gauge versus absolute pressure; test pressure versus equipment rating; nominal diameter versus bore.

Do not convert between reference systems without a supported relationship. Keep the original alongside any justified conversion. For suspected typos, retain the reported value and flag it; label a proposed correction rather than silently using it as fact.

## Teach from the source

Use a source figure with annotations when it is clearer than a redraw. Simplify only what does not change the relevant physical relationships. Link key events and components to their page, figure, table, dated entry, or line range; preserve these references in exported files, not only in chat.

Use a compact legend for reported/calculated/inferred/illustrative content where the distinction matters. Explain abbreviations in context instead of front-loading a large glossary. Do not invent an expansion merely because it fits a familiar domain.

If a drawing or page is unreadable, inspect its image. Use OCR only when necessary and verify critical values visually. Missing evidence can justify a qualitative explanation, a marked gap, or a targeted request for the source—not a fabricated reconstruction.
