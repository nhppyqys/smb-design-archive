# SMB Design Archive

A collection of Claude Code skill packs for building Nod-aligned web surfaces.

---

## Skill Packs

| Skill | What it does |
|---|---|
| [`nod-surface-design`](./nod-surface-design/) | Design and build Nod-aligned web surfaces: SEO utility pages, app UIs, multilingual acquisition pages |

---

## `nod-surface-design`

> Design, build, refactor, or visually QA web surfaces using the Nod compact-professional system.

### What it covers

- **Surface routing** — classifies the page before styling into one of three types
- **Content model** — task-first structure, concrete use cases, accurate free/privacy/limit claims, practical FAQ
- **Nod visual system** — design tokens, typography scale per surface type, component and state rules
- **All interaction states** — empty, loading, success, error, disabled, drag-active, confirmation
- **SEO built into the page** — canonical, hreflang, JSON-LD, sitemap, robots.txt, Open Graph
- **Localization as layout** — RTL, logical CSS properties, language detection, long-copy wrapping
- **Browser verification** — 1440 / 1024 / 390 px and RTL visual QA matrix

### The three surface types

| Surface | Primary job | Type scale |
|---|---|---|
| **Application UI** | Repeated operational work — diagnosis, editing, monitoring | 11–14 px working UI; 18–24 px titles |
| **Marketing / SEO page** | Explain value, match search intent, earn trust, convert | 14–16 px body; 42–66 px hero H1 |
| **SEO utility hybrid** | Acquire through search + let the visitor complete a task immediately | Marketing type outside; app density inside the tool |

Use the **SEO utility hybrid** route for any page that embeds a converter, checker, generator, calculator, analyzer, or uploader that needs to rank in search.

Content order for an SEO utility page:

```
exact task/value → free/trust qualifiers → usable tool → why it matters
→ use cases → workflow → practical FAQ → product bridge
```

### Nod design tokens (quick reference)

```css
--nod-brand:          #7F22FE;
--nod-brand-hover:    #6817DC;
--nod-brand-soft:     #F5EBFF;
--nod-brand-tint:     #F6F0FD;
--nod-text-strong:    #161A26;
--nod-text-primary:   #2B3142;
--nod-text-secondary: #6B7489;
--nod-canvas:         #F6F7FB;
--nod-surface:        #FFFFFF;
--nod-border:         #E4E7F2;
--nod-radius-control: 6px;
--nod-radius-card:    8px;
--nod-radius-shell:   12px;
```

Full token set with spacing rhythm, elevation, and responsive rules in [`nod-surface-design/references/foundations-and-tokens.md`](./nod-surface-design/references/foundations-and-tokens.md).

---

## Installation

### Option A — Project skill (recommended)

```bash
cp -r nod-surface-design /your-project/.claude/skills/
```

Trigger in Claude Code:

```
/nod-surface-design
```

### Option B — Global skill

```bash
cp -r nod-surface-design ~/.claude/skills/
```

### Option C — Manual reference

```
Read nod-surface-design/SKILL.md and the files in nod-surface-design/references/,
then redesign this page.
```

---

## Skill pack structure

```
nod-surface-design/
├── SKILL.md                         # Entrypoint — 10-step workflow and quality gate
└── references/
    ├── foundations-and-tokens.md    # Design tokens, typography, spacing, borders, color rules
    ├── application-patterns.md      # App UI patterns: shell types, info patterns, state requirements
    └── seo-utility-pages.md         # SEO page structure, content rules, crawl/index checklist
```

---

## Example prompt

```
/nod-surface-design

Building a free browser-based video-to-depth-map converter that needs to rank
for "video depth map seedance" queries. 20 locales including Arabic RTL.
Stack: Astro + React, static output.
```

Claude classifies this as an SEO utility hybrid, plans the content model, applies Nod tokens to both the marketing shell and the tool workspace, covers all interaction states, and implements canonical, hreflang, JSON-LD, sitemap, and robots.txt.

---

## Quality gate

The skill does not sign off until every applicable question is yes:

- Did the surface route match the user's job?
- Is the value clearer than the implementation?
- Is the tool usable without reading the SEO content first?
- Are free, privacy, account, and external-cost claims accurate?
- Is content density appropriate rather than merely spacious?
- Are app UI and marketing typography separated correctly?
- Are all interaction, error, mobile, long-copy, and RTL states designed?
- Can search engines discover, crawl, and index every intended locale?
- Did browser screenshots confirm the result?

---

## Contributing

Add a skill pack by creating a folder with a `SKILL.md` (YAML frontmatter with `name` and `description`), any reference files it needs, and updating the skill table above.

---

## License

MIT
