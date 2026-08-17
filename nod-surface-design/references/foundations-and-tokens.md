# Nod foundations and tokens

Use this reference for visual implementation. The values come from the Nod compact-professional system; the application and marketing scales intentionally differ.

## Design character

Optimize for:

- fast comprehension;
- trust through visible evidence and state;
- an obvious next action;
- calm, neutral structure;
- compact controls without cramped reading copy.

Avoid decorative AI styling, gratuitous gradients, glass, glow, excessive cards, repeated shadows, and purple used as general decoration.

Marketing may use a restrained gradient or richer hero surface. Keep the embedded tool itself precise and professional.

## Core tokens

```css
:root {
  --nod-brand: #7F22FE;
  --nod-brand-hover: #6817DC;
  --nod-brand-soft: #F5EBFF;
  --nod-brand-tint: #F6F0FD;
  --nod-brand-border: #D6BBF5;

  --nod-text-strong: #161A26;
  --nod-text-primary: #2B3142;
  --nod-text-secondary: #6B7489;
  --nod-text-tertiary: #9BA3BA;
  --nod-text-disabled: #CBD1E0;

  --nod-canvas: #F6F7FB;
  --nod-surface: #FFFFFF;
  --nod-surface-subtle: #F2F4FA;
  --nod-surface-quiet: #FAFBFE;
  --nod-border: #E4E7F2;
  --nod-border-strong: #CBD1E0;

  --nod-success: #00B42A;
  --nod-success-strong: #009622;
  --nod-success-soft: #E6F9EC;
  --nod-warning: #FF7D00;
  --nod-danger: #F53F3F;
  --nod-info: #3491FA;

  --nod-radius-control: 6px;
  --nod-radius-card: 8px;
  --nod-radius-shell: 12px;
  --nod-radius-large: 16px;
  --nod-shadow-popover: 0 4px 12px rgba(0,0,0,.08);
  --nod-shadow-modal: 0 8px 24px rgba(0,0,0,.12);
}
```

Use a 4 px rhythm normalized to `4, 6, 8, 12, 16, 20, 24, 32, 40, 48`.

## Typography by surface

### Application working scale

| Role | Size / line-height | Weight |
|---|---:|---|
| Page title | 24 / 36 | 600 |
| Detail title | 18 / 26 | 600 |
| Section title | 14 / 22 | 600 |
| Body | 14 / 22 | 400 |
| Metadata | 12 / 20 | 400 |
| Compact annotation | 11 / 16 | 400 |
| Metric | 20 / 28 | 700 |

### Marketing / SEO reading scale

| Role | Size / line-height | Guidance |
|---|---:|---|
| Hero H1 | 42–66 / 1.1–1.18 | Balance to two lines where possible |
| Hero lead | 16–18 / 1.6–1.75 | Keep roughly 55–75 characters per line |
| Section H2 | 28–42 / 1.18–1.3 | Use natural wrapping |
| Card H3 | 17–20 / 1.35–1.5 | Keep concise |
| Reading body | 14–16 / 1.65–1.8 | Do not demote core value copy |
| Kicker / metadata | 12–13 / 1.4–1.6 | Never carry the only important meaning |

Use the application scale inside the interactive utility workspace, not across the whole public page.

## Geometry and density

- Public content max width: about 1120–1200 px with 24–32 px desktop gutters.
- Application reading column: about 680–720 px when prose or decisions dominate.
- Standard card padding: 16–20 px.
- Tool workspace panel padding: 16–24 px.
- Major content section gap: 24–40 px inside; 44–72 px between public sections.
- Button heights: 28 px compact, 32 px default app, 36–44 px prominent or touch-facing.
- Frequent touch targets on mobile: at least 44 px.

Do not fill space by inflating padding. When content is short, use a tighter card, a comparison row, or no card.

## Borders and elevation

- Use `1px solid var(--nod-border)` for normal structure.
- Use `--nod-border-strong` for inputs and stronger affordances.
- Use no shadow on ordinary cards.
- Use popover/modal shadows only on floating UI.
- Allow one restrained shadow on a prominent public tool shell when it clarifies foreground hierarchy.

## Color discipline

- Use purple for active navigation, selected controls, important links, and primary forward actions.
- Use semantic colors only for semantic state.
- Keep most surfaces white or quiet neutral.
- Pair semantic color with an icon, label, sign, or text; never rely on color alone.

## Components

- Prefer one primary action per action group.
- Use explicit verbs instead of `Submit`, `Confirm`, or `Next` when the consequence can be named.
- Use tags for state, not as substitute buttons.
- Use borders and alignment before creating another card.
- Do not nest cards unless the inner object has an independent interaction boundary.
- Use a consistent line-icon set. Avoid tiny icons floating in oversized boxes.
- Keep focus rings visible with a 2 px brand-tinted outline.

## Responsive priority

When space contracts, remove or collapse in this order:

1. decorative whitespace;
2. secondary metadata;
3. auxiliary navigation;
4. nonessential columns;
5. secondary actions into overflow.

Do not remove the primary task, evidence, output, or action first.

