# Application surface patterns

Use these patterns for authenticated or repeated operational work.

## Shell selection

### Full application shell

Use a 76 px desktop rail only when global application navigation is necessary. Put the main panel on the cool-gray canvas with a white surface, fine border, and 12 px radius.

Do not use the rail for a standalone public utility page, campaign landing page, or a page whose primary navigation is browser/search driven.

### Master-detail

Use `76 rail | 250–300 list/tree | flexible detail` for recurring task inboxes or large entity collections. Keep the main decision or reading column near 720 px when possible.

### Creative/editor workspace

Use a two-pane workspace when configuration and result must remain visible together:

`source/diagnosis/configuration | preview/result/versions/actions`

Stack configuration above result on tablet/mobile. Preserve the main preview and final action.

### Contextual drawer

Use a roughly 360 px push/overlay panel for discussion, inspection, or reversible secondary edits. Closing it must preserve the primary task state. Do not put the main multistep workflow in the drawer.

## Information patterns

### AI task

Use the closed loop:

`discover → diagnose → recommend → confirm → execute → verify`

Every recommendation needs evidence, an explicit action, an execution state, and verification when the result can be observed. Keep chat secondary to the action.

### Diagnosis

Show current value, expected value or benchmark, gap, likely cause, and an available change. Prefer a compact comparison table for several related issues.

### Recommendation row

Lead with the verb and target, then expected effect, then one right-aligned action. Use one recommendation per row. Show `modified`, `executing`, `success`, or `failed` explicitly.

### Operational records

Use a table for comparable logs and records. Keep row height 40–48 px, align numeric columns, use tags for state, and scroll horizontally instead of shrinking text below 11 px.

## State requirements

- Loading: mirror the final geometry with a skeleton or local progress state.
- Empty: explain why and offer the relevant next action.
- Failure: state what failed, preserve input, disclose partial application, and offer recovery.
- Consequential change: show scope and values before confirmation.
- Success: keep evidence near the action; do not rely only on a toast.
- Verification: show baseline, observation period, and before/after outcome.

## Compactness checks

- Keep default app controls at 32–36 px high.
- Keep body copy at 14 px and metadata at 12 px; use 11 px only for genuinely compact annotations.
- Keep card padding 16–20 px.
- Remove decorative whitespace before reducing readability.
- Use dividers and alignment rather than a grid of generic dashboard cards.
- Do not make every AI result a large vertical card or a chatbot destination.

## Application QA

- Can the user identify the current entity/task and next action within five seconds?
- Is evidence visible before the recommendation?
- Are analysis and execution visually distinct?
- Are all consequential actions confirmed and stateful?
- Does a failure preserve the user's work?
- Does tablet/mobile change the flow rather than merely shrink it?

