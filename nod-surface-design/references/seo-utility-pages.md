# SEO utility page pattern

Use this reference for public tools that must rank, explain value, and convert visitors into product users.

## Canonical page structure

Use this as a starting grammar, then remove sections that do not answer real intent:

```text
Public header
Hero
  exact task-oriented H1
  outcome-oriented lead
  free / privacy / compatibility qualifiers
  primary CTA to tool
Interactive tool workspace
  input / configuration / progress / result / recovery
  one-sentence next-step instruction
Why this output matters
  source-versus-output or before-versus-after comparison
Use cases
  concrete audience + input + desired outcome
Workflow
  3–4 steps and an actionable recipe
Free / privacy / limitations
Practical FAQ
Product bridge
Footer
```

Place `Why this output matters` before `Workflow` when visitors may understand how to click but not why they should care.

## Content rules

### Hero

- Match the main query in natural language.
- Say what input becomes what output and what that output enables.
- Keep the headline specific enough to disqualify irrelevant traffic.
- Put accurate free, privacy, platform, and compatibility qualifiers near the CTA.
- Do not mention the internal SEO strategy.

### Tool

- Make the first input obvious without requiring the visitor to read the rest of the page.
- Show accepted input, relevant constraints, and the output format close to the control.
- Keep controls compact and results visually dominant.
- Preserve geometry while processing.
- After success, explain the next real-world step, not only `Download complete`.

### Value and use cases

- Explain what information the output preserves, emphasizes, removes, or enables.
- Use direct comparisons when the distinction is visual.
- Use cases must name the audience/task and why this output is preferable to the original input.
- Avoid generic cards such as `Fast`, `Smart`, and `Powerful` unless supported by specific outcomes.

### Workflow

- Use an actionable sequence, not a restatement of features.
- Show the output's place in the downstream workflow.
- Add a concise recipe such as `output A + reference B + instruction C → desired result` when it reduces ambiguity.

### FAQ

Prioritize:

- what the output is;
- how to use it downstream;
- source selection and compatibility;
- free versus separately charged external services;
- privacy and upload behavior;
- formats, duration, limits, and failure recovery;
- whether the result is approximate where precision matters.

Do not add `Is this official?`, internal model questions, or generic copyright boilerplate unless search evidence or user risk makes them important.

## Crawl and index implementation checklist

### Every intended locale route

- Return a stable 200 URL with a self-referencing canonical.
- Render localized title, description, H1, headings, body, links, and FAQ in the initial HTML.
- Set the correct HTML `lang` and `dir`.
- Include reciprocal alternates for all equivalent locales.
- Include `x-default` pointing to a neutral selector or chosen global default.
- Avoid query-parameter-only localization.

### Site-level discovery

- Link the tool from an indexable hub or relevant product page.
- Generate an XML sitemap containing canonical localized URLs and update timestamps only when meaningful.
- Reference the sitemap from `robots.txt`.
- Ensure `robots.txt` does not block rendered assets required to understand the page.
- Avoid orphan pages that only exist in a sitemap.

### Page-level signals

- Use one intent-matching H1 and a logical H2/H3 hierarchy.
- Keep the canonical host, protocol, trailing-slash policy, and sitemap URLs consistent.
- Add `WebApplication` or `SoftwareApplication` structured data when the page exposes a real tool.
- Add `FAQPage` only when the questions and answers are visible and accurately represented; do not promise a rich result.
- Keep schema offers, features, supported platform, and pricing consistent with the visible page.
- Add an OG/Twitter share image when a meaningful preview exists.
- Use descriptive anchors instead of `click here`.
- Set image width/height and meaningful localized alt text.

### Quality and duplication

- Do not create twenty mechanically translated thin pages with incorrect keyword phrasing.
- Keep content naturally useful in each locale; validate high-value markets with native or professional review.
- Avoid multiple pages targeting the same intent with only minor wording changes.
- Give variant pages a distinct user task or consolidate with canonical redirects.
- Do not index empty, failed, or unsupported tool states.

## Multilingual interaction checks

- Test language names, navigation, title, chips, card headings, and CTA wrapping.
- Test Arabic or another RTL locale using logical properties.
- Keep formulas, media controls, file names, and numeric values directionally stable.
- Prevent `current language → current language` suggestions.
- Close language menus by outside click and Escape.
- Prefer a suggestion or explicit user choice over an unexpected automatic redirect that prevents access to another locale.

## Visual QA matrix

Capture and inspect these states:

| View | What to inspect |
|---|---|
| 1440 px default locale | hierarchy, max width, content density, full tool |
| 1024 px | header collisions, tool pane collapse, text measures |
| 390 px | touch targets, upload/result controls, card stacking, overflow |
| RTL mobile | logical borders/padding, order, operators, alignment |
| Long-copy locale | heading wrap, chip wrap, navigation and buttons |
| Tool loading/result/error | stable layout, recovery, obvious next step |
| Language menu/suggestion | outside click, Escape, correct source and target |

Check built HTML or rendered DOM for title, canonical, alternates, JSON-LD, crawlable text, internal links, and sitemap entries. A green build alone does not prove indexability or visual quality.
