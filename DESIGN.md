<!-- Colors and typography direction are read from the Kawlopsia Instagram profile screenshot (visual approximation), not from an original brand file. Re-run /impeccable document once real components exist in code to capture exact computed values. -->

---
name: Kawlopsia
description: Bold, high-contrast bureau identity — near-black surfaces cut by voltage-lime accents and heavy slab-serif headlines.
colors:
  void-black: "#0A0A0A"
  charcoal-surface: "#141410"
  voltage-lime: "#D6FF3D"
  lime-deep: "#A8CC2E"
  bone-white: "#F5F5F0"
  ash-gray: "#A0A0A0"
  error-red: "#8F3A3A"
  line: "rgba(245,245,240,0.14)"
typography:
  display:
    fontFamily: "Roboto Slab, Georgia, serif"
    fontSize: "clamp(2.75rem, 6vw, 5.5rem)"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Roboto Slab, Georgia, serif"
    fontSize: "clamp(1.75rem, 3.2vw, 2.75rem)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.8rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "0.01em"
rounded:
  none: "0px"
  sm: "2px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "32px"
  lg: "64px"
  xl: "112px"
components:
  button-primary:
    backgroundColor: "{colors.voltage-lime}"
    textColor: "{colors.void-black}"
    rounded: "{rounded.none}"
    padding: "18px 40px"
  button-primary-hover:
    backgroundColor: "{colors.lime-deep}"
    textColor: "{colors.void-black}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.bone-white}"
    rounded: "{rounded.none}"
    padding: "18px 40px"
  button-ghost-hover:
    backgroundColor: "{colors.void-black}"
    textColor: "{colors.voltage-lime}"
---

# Design System: Kawlopsia

## 1. Overview

**Creative North Star: "The Access List"**

Kawlopsia's surface reads like a door with a list behind it: void-black rooms cut open by sheets of voltage lime, the same way the brand's own Instagram grid alternates full-black and full-lime panels like a stamped "in / not yet" ledger. Nothing here is soft-edged or apologetic — corners are cut square, type sits heavy and close, and the lime is used at full saturation rather than diluted into a tasteful tint. This is the visual expression of PRODUCT.md's core line: *access is earned, not browsed*. The palette itself performs the gate: you are either standing in the black room, or you have been let onto the lime page.

The system explicitly rejects the generic SaaS/AI grammar named in PRODUCT.md — no gradient text, no hero-metric-card clichés, no uniform icon grids, no tiny tracked eyebrow sitting above every section out of habit. It also rejects the open-marketplace feel: no dense grids of interchangeable "browse" cards that would read as Upwork/Fiverr. Density stays low and deliberate; every block of lime is a decision, not decoration.

**Key Characteristics:**
- Three surfaces — void-black, voltage-lime, and charcoal-surface as a deliberate "third room" — used as full panels, not gradients or tints between them.
- Heavy slab-serif display type set tight and large, functioning like poster headlines, not app copy.
- Flat, hard-edged geometry at rest, with ambient glow permitted at rest only on elevated cards that need to signal weight; interactive elements still earn their glow through hover/focus.
- Restraint in ornament: no card borders-as-decoration, no side-stripes, no soft shadows.

**Revision note (2026-07-08):** the three rules below were loosened after real build experience showed the original all-or-nothing versions were already being quietly worked around in shipped code. Each change is scoped narrowly — the core "bold, tegas, two rooms" identity is untouched; see [Do's and Don'ts](#6-dos-and-donts) for what still holds firm.

## 2. Colors

Two saturated surfaces carry the identity; everything else is in service of legibility against them.

### Primary
- **Voltage Lime** (#D6FF3D): The signal color. Used for primary CTAs, key headline words, full-bleed section panels that mark a "you've been let in" moment (proof points, the access-request CTA), and the hover glow. Never diluted or tinted — always full saturation.

### Neutral
- **Void Black** (#0A0A0A): The default body surface — most of the page lives here. Reads as the "waiting room" before access.
- **Charcoal Surface** (#141410): One step up from Void Black. Originally card-only; now also a valid full-section background (see The Three-Room Rule) for a moment that needs to read as distinct from the surrounding waiting-room black without earning a full lime "you're in" panel — e.g. a trust/security beat like fee protection. Still never used as a card background on a lime section, and never blended with either brand color.
- **Bone White** (#F5F5F0): Primary text and headline color on black surfaces. Never pure #FFFFFF — keeps the page from feeling clinical.
- **Ash Gray** (#A0A0A0): Secondary/muted text (captions, metadata, timestamps) on black surfaces only — 7.6:1 against Void Black, never used at body-copy size on Voltage Lime.
- **Lime Deep** (#A8CC2E): Hover/active state for lime surfaces — a shade down in lightness, never a different hue, so state changes read as "pressed," not "recolored."
- **Error Red** (#8F3A3A): Utility color, scoped strictly to form-validation and inline-notification states (field borders, error text). Never used for section backgrounds, decoration, or anything outside error/warning feedback — this is a functional exception to the two brand hues, not a third brand color.

### Named Rules
**The Three-Room Rule** *(formerly the Two-Room Rule)*. A given section is void-black, voltage-lime, or charcoal-surface at full strength — never a gradient between any of them, never a tint applied "for accent." Charcoal-surface is the deliberate middle room: reach for it when a section needs more weight than the waiting-room black but hasn't earned the lime "you're in" moment yet. It should stay rare — if more than one section in a row uses it, the specialness is gone and it's becoming a fourth default, not a considered exception.

## 3. Typography

**Display Font:** Roboto Slab (with Georgia, serif fallback)
**Body Font:** Inter (with ui-sans-serif, system-ui fallback)

**Character:** A heavy, close-set slab serif for anything meant to be read as a headline or poster line, paired with a plain, quiet grotesque for everything meant to be read as running text — the same split the brand's own Instagram carousels use between bold statement lines and small caption copy.

### Hierarchy
- **Display** (800, clamp(2.75rem, 6vw, 5.5rem), 1.02 line-height, -0.02em tracking): Hero headline only, one per page.
- **Headline** (700, clamp(1.75rem, 3.2vw, 2.75rem), 1.1 line-height, -0.01em tracking): Section headers ("Cara Kerja Kurasi", "Untuk Founder & Perusahaan").
- **Body** (400, 1.05rem, 1.6 line-height): Paragraph copy, max 70ch measure.
- **Label** (600, 0.8rem, 0.01em tracking): Form labels, button text (uppercase), chip/tag text. Not a decorative eyebrow — only used where it labels an actual interactive element or data point.

### Named Rules
**The No-Eyebrow Rule.** Label-style type never sits alone above a heading purely as rhythm ("ABOUT" / "01 — PROCESS"). It is reserved for things that are genuinely labels: a button, a form field, a status chip.

## 4. Elevation

Flat by default — surfaces are solid color blocks with no ambient shadow, matching the poster-like flatness of the source material. Two distinct kinds of depth exist, and they mean different things:
- **Earned glow** — a *response to interaction*. Primary CTAs and key interactive elements carry a lime glow on hover/focus only. This is the one that matters most: the interaction that drives the page's single conversion path gets a distinct, earned lift.
- **Ambient glow** — a *resting-state signal of weight*, permitted on a small, named set of elevated cards (see below) that need to read as important the moment they appear, not just on interaction.

### Shadow Vocabulary
- **glow-cta** (`box-shadow: 0 0 32px rgba(214,255,61,0.45)`): Hover/focus state on the primary CTA button and any lime-surfaced link. Signals "this is the way through." Interaction-only, no exceptions.
- **glow-focus** (`box-shadow: 0 0 0 2px rgba(214,255,61,0.9)`): Keyboard focus ring on all interactive elements — a lime ring, not a browser-default blue.
- **glow-ambient** (`box-shadow: 0 0 28px rgba(214,255,61,0.12)`): Permitted at rest on elevated content cards — process/flow cards, testimonial/quote cards — where the card needs to feel present against a black section without waiting for a hover. Not for buttons, inputs, or anything already covered by glow-cta/glow-focus.

### Named Rules
**The Earned-Glow Rule, revised.** `glow-cta` and `glow-focus` still only appear on `:hover` / `:focus-visible` — that discipline is what makes the CTA's glow mean something. `glow-ambient` is the one named, deliberate exception: it may sit at rest on elevated cards, and should intensify to `glow-cta` on hover/focus for that "earned" lift on top of the ambient base. If a component isn't on the short list above, it stays flat until interaction — the rule still exists to be broken rarely, not ignored.

## 5. Components

### Buttons
- **Shape:** Square corners, 0px radius (or 2px maximum for accessibility of tap targets on very small text buttons) — cut, not softened.
- **Primary:** Voltage Lime background, Void Black text, 18px/40px padding, Label typography in uppercase, no border.
- **Hover / Focus:** Background shifts to Lime Deep; `glow-cta` shadow appears; focus-visible adds `glow-focus` ring.
- **Ghost/Secondary:** Transparent background, Bone White text, 2px solid Bone White border, same padding. On hover, inverts to Void Black background with Voltage Lime text — the "you've stepped through" moment in miniature.

### Cards / Containers
- **Corner Style:** 0px radius, matching buttons.
- **Background:** Charcoal Surface on black sections; never a lime-tinted card.
- **Shadow Strategy:** None at rest (see Elevation). A 1px `line` border (rgba(245,245,240,0.14)) substitutes for shadow-based separation.
- **Internal Padding:** `spacing.md` (32px) minimum; testimonial/quote cards use `spacing.lg` (64px) to read as spacious, not cramped.

### Inputs / Fields
- **Style:** Void Black or Charcoal Surface background, 1px `line` border, Bone White text, 0px radius.
- **Focus:** Border color shifts to Voltage Lime, `glow-focus` ring appears.
- **Error:** Border and label shift to Error Red (#8F3A3A) — tokenized, scoped to form/notification states only (see Colors).

### Navigation
- Void Black bar, Bone White wordmark/logo, Label-style nav links (uppercase, 600 weight). Active/hover link underlines in Voltage Lime — a 2px solid underline, not a border-left stripe. Mobile: full-black overlay menu, links set in Headline size for thumb-friendly tap targets.

## 6. Do's and Don'ts

### Do:
- **Do** keep every section Void Black, Voltage Lime, or Charcoal Surface at full strength — no in-between tints, no blending (The Three-Room Rule). Charcoal-surface sections stay rare and deliberate.
- **Do** cut every corner square (0px radius) on buttons, cards, and inputs — the flat, print-poster geometry is the point.
- **Do** reserve `glow-cta` and `glow-focus` for hover/focus states only — `glow-ambient` is the sole named at-rest exception, and only on the elevated-card short list (see Elevation).
- **Do** frame every CTA as an application/request action ("Ajukan Akses", "Jadwalkan Panggilan"), never a generic "Sign Up" or "Get Started."
- **Do** keep Error Red scoped to form/notification states only — it is a functional utility color, not a third brand hue.

### Don't:
- **Don't** use gradient text or a gradient background anywhere — the brand is flat color blocks, not a blend.
- **Don't** add a tiny uppercase tracked eyebrow above every section out of habit (The No-Eyebrow Rule) — label type only labels real interactive elements.
- **Don't** use numbered 01/02/03 section markers unless the content is a genuine ordered sequence (the login/onboarding flows qualify; generic marketing sections do not).
- **Don't** build dense, uniform card grids that read like an open talent directory — the page should feel curated and sparse, not like a marketplace listing.
- **Don't** use `border-left`/`border-right` colored stripes as an accent on any card, alert, or list item.
- **Don't** reach for charcoal-surface as a default "safe middle ground" — it exists for the rare section that needs more weight than black but hasn't earned lime, not as a way to avoid committing to a room.
