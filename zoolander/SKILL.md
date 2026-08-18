---
name: zoolander
description: >-
  Guardrail UI against vibe-coded AI slop: the fashionified, statistical-average look
  (Blue Steel) models emit without intention. Use when generating, editing, or reviewing
  frontend UI, landing pages, dashboards, Tailwind/shadcn, or when the user says vibe
  coding, AI slop, generic SaaS, or zoolander. Do not use for accessibility, performance,
  component APIs, or general UX quality.
---

# Zoolander

Satire of fashionified software UI: the industry mistakes the pose for the work.

**Rule:** If the screen could wear another product's wordmark, do not ship it. Lock to this repo's tokens, or stop.

This skill only refuses vibe-coded slop. It does not invent a brand, run an a11y audit, or teach layout.

## Scope

**In.** Visual, copy, and class-name tells of generated-UI mode-seeking (Tailwind defaults, unthemed shadcn, v0/Lovable, Dribbble 2022).

**Out.** WCAG, keyboard, performance, i18n, form composition, empty/error/focus as quality (those are other skills). Using shadcn/ui is fine; shipping it unthemed is slop.

## When

Generating or reviewing screens, components, tokens, or marketing UI. User names slop, vibe coding, or zoolander.

## When not

Backend, data, tests with no UI. "Is this usable?" without a slop question. A brief that *names* a look that happens to match a signal (then it is a choice).

## Gate

Before markup, and again before calling the UI done:

```
MUST-STOP unless all are true:
1. Palette and type come from this repo (or from a constraint you wrote down first).
2. You can name what is not a card.
3. Wordmark off, this still cannot be any other 2025–2026 AI product.
```

If the first pass looks like v0: do not polish. Change type, color, or structure — one move. Do not escape into the *next* default (see [signals.md](signals.md) § Modes).

## Excuses

| The model says | Counter |
| --- | --- |
| It's just a prototype | Slop trains the next pass. Same gate. |
| I'll differentiate later | The first pass is what ships. |
| The brief said modern / premium / clean / SaaS | Those words *are* the mode. Name hexes, faces, density. |
| I used shadcn, that's the system | Unthemed shadcn is the average. Theme it or don't pretend it's a look. |
| I avoided purple | Cream+serif+terracotta, acid-green-on-black, and broadsheet-zero-radius are the next modes. |
| I picked a unique font | One face plus icon-tile cards plus indigo is still a fail. |
| Locally each block looks fine | Globally it is chaos. Color and cards are a page budget. |
| Make it pop / add hierarchy | That is how left-bars, dots, and glow orbs get in. Remove, don't decorate. |

## Warning signs (own reasoning)

- "polished", "premium", "modern", "clean SaaS", "delightful"
- Reaching for Inter, Geist, indigo, purple, `bg-indigo-500` without opening tokens
- Next block wrapped in a card by habit
- Three-column icon tiles; eyebrow pill over the H1
- New palette invented while the repo already has one

## Practice

1. Read existing tokens, fonts, copy in the app. Do not add a second aesthetic.
2. Ban the reflex list in [signals.md](signals.md). Four signals together = fail. One named in the brief may stand.
3. Spend one accent, rarely. Group with type and space, not boxes. A card is for something independently actionable.
4. Chrome (dots, glows, motion, emoji, sparkle) must mean a state, a layer, or an action — else remove.
5. Write the product: specific nouns and verbs. Cut the sentence that restates the last.

## Review

Only report slop. Format: `path` — signal — cut or lock-to-token.

Do not file taste essays, a11y notes, or "while you're here" refactors.

## Before you ship

- [ ] Gate passed
- [ ] Not four signals
- [ ] Copy would sound wrong on a competitor
- [ ] You did not swap one template for the opposite template
