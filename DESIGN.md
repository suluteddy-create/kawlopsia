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
- Two dominant surfaces only — void-black and voltage-lime — used as full panels, not gradients or tints between them.
- Heavy slab-serif display type set tight and large, functioning like poster headlines, not app copy.
- Flat, hard-edged geometry at rest; glow is reserved as a live, earned response to interaction.
- Restraint in ornament: no card borders-as-decoration, no side-stripes, no soft shadows.

## 2. Colors

Two saturated surfaces carry the identity; everything else is in service of legibility against them.

### Primary
- **Voltage Lime** (#D6FF3D): The signal color. Used for primary CTAs, key headline words, full-bleed section panels that mark a "you've been let in" moment (proof points, the access-request CTA), and the hover glow. Never diluted or tinted — always full saturation.

### Neutral
- **Void Black** (#0A0A0A): The default body surface — most of the page lives here. Reads as the "waiting room" before access.
- **Charcoal Surface** (#141410): One step up from Void Black, used only for a card/panel that needs to sit slightly forward on a black section (e.g. a testimonial block) without introducing a second hue.
- **Bone White** (#F5F5F0): Primary text and headline color on black surfaces. Never pure #FFFFFF — keeps the page from feeling clinical.
- **Ash Gray** (#A0A0A0): Secondary/muted text (captions, metadata, timestamps) on black surfaces only — 7.6:1 against Void Black, never used at body-copy size on Voltage Lime.
- **Lime Deep** (#A8CC2E): Hover/active state for lime surfaces — a shade down in lightness, never a different hue, so state changes read as "pressed," not "recolored."

### Named Rules
**The Two-Room Rule.** A given section is either a black room or a lime room — never a gradient between them, never a lime tint applied to a black background "for accent." If a section needs a third value, use Charcoal Surface, not a blend of the two brand colors.

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

Flat by default — surfaces are solid color blocks with no ambient shadow, matching the poster-like flatness of the source material. Depth is introduced only as a *response to interaction*: primary CTAs and key interactive elements carry a lime glow on hover/focus, never at rest. This keeps the resting page graphic and print-like while giving the one interaction that matters (booking a call, requesting access) a distinct, earned lift.

### Shadow Vocabulary
- **glow-cta** (`box-shadow: 0 0 32px rgba(214,255,61,0.45)`): Hover/focus state on the primary CTA button and any lime-surfaced link. Signals "this is the way through."
- **glow-focus** (`box-shadow: 0 0 0 2px rgba(214,255,61,0.9)`): Keyboard focus ring on all interactive elements — a lime ring, not a browser-default blue.

### Named Rules
**The Earned-Glow Rule.** Glow only appears on `:hover` / `:focus-visible`, never at rest. A page with everything glowing has nothing glowing.

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
- **Error:** Border and label shift to a desaturated red-orange (not yet tokenized — resolve alongside form-validation build).

### Navigation
- Void Black bar, Bone White wordmark/logo, Label-style nav links (uppercase, 600 weight). Active/hover link underlines in Voltage Lime — a 2px solid underline, not a border-left stripe. Mobile: full-black overlay menu, links set in Headline size for thumb-friendly tap targets.

## 6. Do's and Don'ts

### Do:
- **Do** keep every section either Void Black or Voltage Lime at full strength — no in-between tints (The Two-Room Rule).
- **Do** cut every corner square (0px radius) on buttons, cards, and inputs — the flat, print-poster geometry is the point.
- **Do** reserve the lime glow (`glow-cta`) for hover/focus states only, never at rest.
- **Do** frame every CTA as an application/request action ("Ajukan Akses", "Jadwalkan Panggilan"), never a generic "Sign Up" or "Get Started."

### Don't:
- **Don't** use gradient text or a gradient background anywhere — the brand is two flat colors, not a blend.
- **Don't** add a tiny uppercase tracked eyebrow above every section out of habit (The No-Eyebrow Rule) — label type only labels real interactive elements.
- **Don't** use numbered 01/02/03 section markers unless the content is a genuine ordered sequence (the login/onboarding flows qualify; generic marketing sections do not).
- **Don't** build dense, uniform card grids that read like an open talent directory — the page should feel curated and sparse, not like a marketplace listing.
- **Don't** use `border-left`/`border-right` colored stripes as an accent on any card, alert, or list item.
