---
name: nod-surface-design
description: Design, build, refactor, or visually QA Nod-aligned web surfaces using a compact-professional system. Use for authenticated application UI, AI/commerce operations screens, dashboards, creative workspaces, SEO utility landing pages, multilingual acquisition pages, or requests to apply the Nod/SMB_DESIGN visual scale without blindly reusing an application rail, tiny type, or dashboard density.
---

# Nod Surface Design

Preserve Nod's calm, compact, professional character while adapting the shell, typography, density, and content structure to the page's actual job.

## Load the relevant references

- Read [foundations-and-tokens.md](references/foundations-and-tokens.md) for every task that changes visual styling or components.
- Read [application-patterns.md](references/application-patterns.md) for authenticated product, operations, dashboard, editor, table, onboarding, or AI workflow surfaces.
- Read [seo-utility-pages.md](references/seo-utility-pages.md) for public tools, product-led SEO pages, multilingual acquisition pages, or any page expected to rank and convert.

## Route the surface before styling

Classify the page first. Do not infer the shell from the design tokens.

| Surface | Primary job | Default shell | Typical type scale |
|---|---|---|---|
| Application UI | Repeated operational work, diagnosis, editing, execution, monitoring | Compact app shell; rail/split panes only when they improve task flow | 11–14 px working UI; 18–24 px titles |
| Marketing / SEO page | Explain value, match search intent, earn trust, lead to a tool or product | Public header, readable hero, crawlable content sections | 14–16 px body; 28–42 px section titles; 42–66 px hero |
| SEO utility hybrid | Acquire through search and let the visitor complete a focused task | Marketing shell around a compact professional tool workspace | Marketing type outside; application density inside the tool |

Use the hybrid route when a public page contains an interactive converter, checker, generator, calculator, analyzer, or uploader. Never force the 76 px application rail onto this route unless the user explicitly asks for an authenticated app shell.

If uncertain, write these two sentences internally:

1. `The visitor comes here to _______.`
2. `The visitor searched for _______ because they want to _______.`

If the first answer is a repeated business operation, route to application UI. If the second answer controls discovery and the page has a self-contained task, route to the SEO utility hybrid.

## Follow this workflow

### 1. Inspect before changing

- Inspect the current page, content, routes, data states, localization system, and target brand references.
- Open the page in a browser when a runnable implementation exists.
- Record the current information order, viewport behavior, overflow, empty space, interaction failures, and implementation leakage.
- Preserve intentional product behavior and unrelated user changes.

### 2. Define the task and promise

Write one primary user task and one primary value promise. Allow one dominant CTA per action region.

For application UI, order information as:

`context → issue/outcome → evidence → interpretation → action → state/verification`

For an SEO utility page, order the experience as:

`exact task/value → free/trust qualifiers → usable tool → why it matters → use cases → workflow → practical FAQ → product bridge`

Do not begin with the implementation, the model, or the company's SEO goal.

### 3. Build the content model before decoration

- Lead with what the user can accomplish, for whom, and with what output.
- Explain why the output is useful before explaining the workflow.
- Name concrete use cases with an input, an action, and an outcome.
- State `free`, privacy, limits, account requirements, and external-service costs accurately and close to the relevant action.
- Use comparisons, before/after examples, recipes, or diagrams when they explain the task faster than prose.
- Derive FAQ items from real selection, compatibility, workflow, output, price, privacy, and failure questions.

Remove content that makes the product feel unfinished or inward-looking unless it changes the user's decision:

- internal model, library, runtime, or infrastructure names;
- engineering implementation notes and roadmap promises;
- weak defensive explanations such as why sign-in exists;
- low-value `Is this official?` questions when no genuine ambiguity or compliance issue exists;
- claims about SEO, activation, or internal acquisition strategy;
- speculative precision or guarantees the tool cannot support.

### 4. Compose the correct shell

For application surfaces, use the smallest sufficient application pattern from [application-patterns.md](references/application-patterns.md).

For SEO utility hybrids:

- Use a public header, a direct hero, and a clearly visible tool above or near the fold.
- Present the interactive tool as a compact editor/workspace with clear input, controls, progress, result, and recovery states.
- Return to readable marketing typography outside the tool. Do not apply the 11–14 px application scale to the entire page.
- Keep content sections visually calm but distinct with spacing, fine borders, quiet tints, and limited brand emphasis.
- Use 16–20 px card padding by default. Increase only when content density justifies it.
- If a card contains more empty space than meaningful content, reduce padding, change the grid, add a useful visual, or remove the card.

### 5. Apply the Nod visual character

- Use white surfaces on a light cool-gray canvas.
- Use fine neutral borders and spacing for structure; reserve shadows for floating layers or one prominent tool shell.
- Reserve purple for brand, selected states, and high-value forward actions.
- Prefer control radii of 6 px, card radii of 8 px, and shell radii of 12 px.
- Use deliberate whitespace without turning the page into sparse oversized cards.
- Use clear, appropriately sized icons. Prefer a coherent icon set; use emoji only when their visual weight and cross-platform rendering are acceptable.
- Keep one strongest title and one dominant CTA per action region.

### 6. Make visuals correspond to the claim

- Put input/output comparisons beside the explanation they support.
- Put workflow diagrams beside workflow copy, not in an unrelated section.
- For page audits or recommendations, cite the exact page URL and show a screenshot or crop so the reader can identify the target.
- Give every meaningful image localized alt text; use empty alt text only for decoration.
- Avoid generic stock imagery, decorative diagrams, and screenshots with no referenced conclusion.

### 7. Design all meaningful states

Cover at least:

- default and empty;
- hover and visible keyboard focus;
- input selected / drag active where relevant;
- loading or processing with stable geometry;
- success with an obvious next action;
- error with preserved input and recovery;
- disabled or unsupported conditions;
- confirmation and verification for consequential actions.

Do not leave an empty toolbar, numbered section, or blank card after content is removed.

### 8. Treat localization as layout and SEO

- Use real localized routes and server-rendered/static localized text for indexable pages; do not rely only on client-side string replacement.
- Set valid `lang` and `dir`; use logical CSS properties for bidirectional layout.
- Add canonical and complete reciprocal `hreflang` links, including `x-default` where an intentional language selector exists.
- Test the longest supported labels and at least one RTL locale.
- Let headings wrap; do not shrink important copy to fit.
- Keep operators, icons, numbers, media controls, and directional arrows semantically correct in RTL.
- Never show a language suggestion where the detected source and target are identical.
- Let popovers close by outside click and Escape; preserve focus behavior.

### 9. Build SEO into the page, not only the head

For indexable utility pages, verify all of the following:

- one localized, intent-matching `title`, meta description, and H1;
- canonical URL and valid status code;
- crawlable descriptive content and internal links in rendered HTML;
- clean, stable locale URLs without query-only localization;
- reciprocal `hreflang` plus an intentional `x-default` entry;
- `robots.txt` and an XML sitemap containing canonical localized URLs;
- applicable JSON-LD that matches visible content and does not invent capabilities;
- useful Open Graph and Twitter metadata, including a share image when available;
- descriptive links, image dimensions, alt text, and reasonable performance;
- no accidental `noindex`, blocked assets, redirect loops, duplicate canonicals, or soft-404 locale pages.

Do not create thin translated pages by swapping keywords into identical filler. Each locale must retain useful, natural task explanation. See [seo-utility-pages.md](references/seo-utility-pages.md) for the implementation and QA checklist.

### 10. Verify in a real browser

Run proportional automated checks, then inspect the rendered page.

At minimum, verify:

- full desktop around 1440 px;
- compact desktop or tablet around 1024 px;
- mobile around 390 px;
- one RTL locale and one long-text locale;
- no horizontal overflow, clipped controls, tiny critical text, empty regions, or excessive card padding;
- primary task and value understood within five seconds;
- language menu, outside click, Escape, anchors, upload/process/result, and failure recovery as applicable;
- headings, canonical, alternates, JSON-LD, robots, and sitemap in the built output;
- no console errors or broken assets.

Capture full-page and task-critical screenshots. Inspect the screenshots rather than treating a successful build as visual proof.

## Quality gate

Do not finish until the answer to each applicable question is yes:

- Did the surface route match the user's job?
- Is the value clearer than the implementation?
- Is the tool usable without reading the SEO content first?
- Do the use cases explain why the output matters?
- Are free, privacy, account, and external-cost claims accurate?
- Is content density appropriate rather than merely spacious?
- Are app UI and marketing typography separated correctly?
- Are visuals adjacent to the claims they explain?
- Are interaction, error, mobile, long-copy, and RTL states designed?
- Can search engines discover, crawl, understand, and index every intended locale?
- Did browser screenshots confirm the result?
