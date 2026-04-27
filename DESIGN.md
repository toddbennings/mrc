---
name: Carmichael Portfolio
description: London Carmichael's creative portfolio — brand, graphic, photo, video.
colors:
  gold: "#C5A120"
  near-black: "#18150E"
  charcoal: "#2D2920"
  warm-white: "#F8F7F3"
  card-surface-light: "#FEFDF9"
  card-surface-dark: "#1F1C14"
  off-white: "#DEDAD3"
  warm-mid-light: "#7A7569"
  warm-mid-dark: "#9D9890"
  placeholder-light: "#DEDAD3"
  placeholder-dark: "#242018"
  border-light: "#E8E5DF"
  border-dark: "#2A2720"
typography:
  display:
    fontFamily: "'Barlow Condensed', Impact, sans-serif"
    fontSize: "clamp(4rem, 12vw, 9rem)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "'Barlow Condensed', Impact, sans-serif"
    fontSize: "clamp(2rem, 6vw, 4.5rem)"
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: "-0.01em"
  title:
    fontFamily: "'Inter', sans-serif"
    fontSize: "1.125rem"
    fontWeight: 500
    lineHeight: 1.3
  body:
    fontFamily: "'Inter', sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "'Inter', sans-serif"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: "0.08em"
rounded:
  sm: "8px"
  md: "16px"
  lg: "24px"
  full: "9999px"
spacing:
  xs: "16px"
  sm: "24px"
  md: "40px"
  lg: "48px"
  xl: "64px"
  2xl: "80px"
components:
  case-study-card:
    backgroundColor: "{colors.card-surface-light}"
    rounded: "{rounded.lg}"
    padding: "48px"
  case-study-card-dark:
    backgroundColor: "{colors.card-surface-dark}"
    rounded: "{rounded.lg}"
    padding: "48px"
  theme-toggle:
    backgroundColor: "{colors.card-surface-light}"
    textColor: "{colors.charcoal}"
    rounded: "{rounded.full}"
    padding: "8px 14px"
  btn-primary:
    backgroundColor: "{colors.charcoal}"
    textColor: "{colors.warm-white}"
    rounded: "0px"
    padding: "16px 40px"
  btn-primary-hover:
    backgroundColor: "{colors.charcoal}"
    textColor: "{colors.warm-white}"
    rounded: "0px"
    padding: "16px 40px"
---

# Design System: Carmichael Portfolio

## 1. Overview

**Creative North Star: "The Athletic Edit"**

London Carmichael's portfolio operates like a Nike campaign page, not a case study archive. The dominant visual instrument is maximum contrast — near-black against warm-white, with the Carmichael gold appearing only as the brand mark. Nothing decorates. Every element either holds the work or steps away from it.

Barlow Condensed at extreme weights and sizes carries the visual energy. Inter stays functional, measured, and quiet. The gap between those two registers — commanding display type against plainspoken body copy — is the typographic personality of the system. Big type shouts. Chrome steps back. Work speaks.

The system explicitly rejects Swiss/International Style grid rationality (too neutral, too impersonal), the over-templated agency case-study format (hero image, paragraph, gallery, paragraph), and the generic creative-portfolio white-card-hover-overlay cliché. It chases instead the effortless authority of a Nike campaign drop: purposeful negative space, a single dominant mark, and work that does not need explanation.

**Key Characteristics:**
- Near-black / warm-white contrast as the primary design instrument
- Carmichael gold appearing only at the brand mark — never as UI chrome
- Barlow Condensed at 700–900 weight for all display and headline moments
- Flat surfaces throughout; depth through contrast, not shadow
- Generous, asymmetric spacing that creates rhythm, not comfort
- Dark and light modes both viable — the system is designed for maximum contrast in either

## 2. Colors: The Warm Contrast Palette

Two surfaces, one mark, one supporting warm-gray scale. No secondary accent. The restraint is intentional.

OKLCH is the canonical color format for this project. Hex values appear in the frontmatter for Stitch compatibility; all implementation should use OKLCH or CSS custom properties.

### Primary
- **Carmichael Gold** (`#C5A120` / `oklch(70% 0.12 85)`): The brand mark and nothing else. Lives in the `carmic.svg` wordmark. May accent one high-impact typographic detail per screen (a single date, a category label). Never used for buttons, hover states, borders, or background fills.

### Neutral
- **Near-Black** (`#18150E` / `oklch(13% 0.008 85)`): Dark mode page background. Also the primary text color on light surfaces. Warm-tinted, not graphite — never pure black.
- **Deep Charcoal** (`#2D2920` / `oklch(24% 0.008 85)`): Primary text on light surfaces. Slightly lifted from Near-Black to preserve warmth at reading sizes.
- **Warm White** (`#F8F7F3` / `oklch(97% 0.005 85)`): Light mode page background. Micro-warm tint — never pure white.
- **Card Surface Light** (`#FEFDF9` / `oklch(99.5% 0.003 85)`): Light mode card background. Barely separated from the page — the gap is depth enough.
- **Card Surface Dark** (`#1F1C14` / `oklch(18% 0.008 85)`): Dark mode card background.
- **Off-White** (`#DEDAD3` / `oklch(88% 0.006 85)`): Primary text on dark surfaces. Placeholder backgrounds in light mode.
- **Warm Mid Light** (`#7A7569` / `oklch(52% 0.006 85)`): Secondary / supporting text on light surfaces. Card descriptions.
- **Warm Mid Dark** (`#9D9890` / `oklch(65% 0.006 85)`): Secondary text on dark surfaces.
- **Border Light** (`#E8E5DF` / `oklch(90% 0.005 85)`): Borders and dividers on light surfaces. Theme toggle border at rest.
- **Border Dark** (`#2A2720` / `oklch(26% 0.008 85)`): Borders on dark surfaces.

### Named Rules
**The Gold Mark Rule.** Carmichael Gold is the brand mark. It appears on the `carmic.svg` wordmark and may accent one typographic detail per screen. Using it as a button background, text color (other than the mark), underline, border fill, or hover state is prohibited. Its scarcity is the identity.

**The No-Pure Neutrals Rule.** No `#000000` or `#ffffff`. Every neutral carries a warm tint (hue 85°, chroma 0.005–0.01). If a neutral feels cool, generic, or digital-gray, add warmth.

**The Maximum Contrast Rule.** Minimum WCAG AA (4.5:1). Target WCAG AAA on primary text pairs. The system is built for high contrast — meeting the minimum is underperforming.

## 3. Typography

**Display / Headline Font:** Barlow Condensed (Google Fonts: `family=Barlow+Condensed:wght@700;900`)
**Body / UI Font:** Inter (Google Fonts: `family=Inter:wght@400;500`)

**Character:** Barlow Condensed at 900 is aggressive, athletic, and condensed enough to command space without needing it. Inter does not compete — it is neutral, exact, and invisible. The contrast between the two is the typographic identity: one voice shouts, one voice reports.

### Hierarchy
- **Display** (Barlow Condensed 900, `clamp(4rem, 12vw, 9rem)`, lh 0.9, ls -0.02em): Campaign headlines, hero moments, section identifiers. Always uppercase. Reserved for single words or very short phrases — not sentences.
- **Headline** (Barlow Condensed 700, `clamp(2rem, 6vw, 4.5rem)`, lh 1.0, ls -0.01em): Section labels, project category headers.
- **Title** (Inter 500, `1.125rem/18px`, lh 1.3): Project titles within case study cards.
- **Body** (Inter 400, `1rem/16px`, lh 1.65, max 65ch): Project descriptions, supporting copy. Never justify-aligned. Max line length enforced.
- **Label** (Inter 500, `0.75rem/12px`, lh 1.0, ls 0.08em, UPPERCASE): Metadata: dates, skill categories, nav links.

### Named Rules
**The Scale Rule.** There must be at least a 2× size gap between Display and Title. If Display renders at 72px, Title is 36px at most. A flat type scale is a flat page.

**The Caps Rule.** Barlow Condensed in Display and Headline roles is always uppercase. Inter is never forced uppercase except in Label. Mixed case in Barlow Condensed reads weak — commit to the full-caps authority or don't use the weight.

**The Weight Rule.** Body and Title use only Inter 400 and 500. Do not use Inter 700+ — that weight slot belongs to Barlow Condensed. Hierarchy is maintained by font-family, not by bolding Inter.

## 4. Elevation

Flat by design. No `box-shadow` on any resting surface. Depth is achieved through contrast alone: card surfaces sit 2–3 lightness steps above the page background — visible, separated, not lifted. The portfolio's restraint is what makes the work read as the focal point.

One exception: focus rings use a subtle gold glow, `0 0 0 3px oklch(70% 0.12 85 / 0.25)`, as an accessibility affordance — not a visual decoration. This appears only on keyboard focus, never on hover.

### Named Rules
**The Flat Frame Rule.** Surfaces do not cast shadows at rest. Before adding a shadow, ask whether contrast alone can separate the surface. It always can in this system.

**The Focus Ring Exception.** Focus rings may use the gold glow value. This is the one permitted use of gold outside the brand mark, and it applies only to `:focus-visible`, never to `:hover`.

## 5. Components

### Case Study Card
The primary component. A quiet container that holds the work and nothing else.

- **Shape:** 24px radius (large, confident — reduces to 16px on mobile)
- **Background:** Card Surface Light / Dark (barely separated from page)
- **Shadow:** None
- **Border:** None
- **Internal padding:** 48px (desktop), 40px (tablet 1024px), 32px (tablet 768px), 24px (mobile)
- **Internal gap:** 56px between header and media (reduces to 40px on tablet, 32px on mobile)
- **Card header layout:** Title + description in a flex row with a 153px gap (collapses to stacked on mobile with 16px gap)
- **Card title:** Inter 500, 18px, primary text color
- **Card description:** Inter 400, 16px, secondary text color, max 530px width
- **Media columns:** 8px radius, placeholder background color, full column height
- **Bottom:** Pagination dots — three 8px CSS circles, active at full opacity, inactive at 20%

### Theme Toggle
The only persistent UI chrome on the page. Fixed position.

- **Shape:** Full radius pill (9999px)
- **Background:** Card Surface (matches cards, not page background)
- **Border:** 1px solid Border color; on `:hover` shifts to `var(--gold)`
- **Focus:** `0 0 0 3px oklch(70% 0.12 85 / 0.25)` on `:focus-visible`
- **Typography:** Inter 400, 13px
- **Padding:** 8px 14px
- **Icon:** 15×15px SVG (moon in light mode, sun in dark mode); `aria-hidden="true"` since button has `aria-label`
- **Label:** Shows the next action ("Dark" when light, "Light" when dark); `aria-label` updates to match

### Pagination Dots
Pure CSS. No images, no external assets.

- Three 8px × 8px circles, `border-radius: 50%`
- Active: primary text color, `opacity: 1`
- Inactive: primary text color, `opacity: 0.2`
- Container: flex row, 10px gap, `aria-hidden="true"`

### Primary CTA Button (defined, not yet implemented)
To be used for project deep-links and contact entry points when added.

- **Shape:** 0px radius — sharp corners, athletic, not soft
- **Background:** Near-Black on light mode, Off-White on dark mode (inverted surface)
- **Text:** Inverse surface color; Inter 500, 13px, ls 0.06em, UPPERCASE
- **Padding:** 16px 40px
- **Hover:** Gold border appears (`outline: 2px solid var(--gold); outline-offset: 2px`); background unchanged
- **Focus:** Gold glow ring (same as focus exception above)
- **No shadow, no gradient, no rounded corners**

### Media Grid
Variable-column placeholder layout inside cards. Switches to a single-column with reduced height at 768px and below.

- **Columns:** 1, 2, or 3 — all `flex: 1`, equal width, 48px gap (16px on tablet/mobile)
- **Height:** Set per card to match intended imagery aspect ratio; collapses to 260px at 768px, 180px at 480px
- **Background:** Placeholder color (warm gray) until real images are placed

## 6. Do's and Don'ts

### Do:
- **Do** use Barlow Condensed at 700–900 weight for all display moments — the larger the better. If it doesn't feel too big, go bigger.
- **Do** let work breathe. Generous, asymmetric spacing makes the portfolio feel confident; tight spacing makes it feel anxious.
- **Do** maintain near-black/warm-white contrast as the primary visual tool — it should feel like a Nike campaign at a glance.
- **Do** keep Carmichael Gold as the brand mark only. One appearance on the wordmark. Optionally one small typographic detail. Never UI chrome.
- **Do** use sharp-cornered (0px radius) buttons if CTAs are added — sporty, not soft.
- **Do** load Barlow Condensed from Google Fonts alongside Inter before implementing display type: `family=Barlow+Condensed:wght@700;900&family=Inter:wght@400;500`.
- **Do** test at full-bleed widths on a large monitor — the portfolio should feel like a billboard, not a brochure.

### Don't:
- **Don't** use Swiss/International Style grid rationality — neutral columns and Helvetica rationalism are the wrong lane for this portfolio. It is too impersonal.
- **Don't** use the Carmichael Gold (`#C5A120`) as a UI color for buttons, borders, backgrounds, text, or hover states. The mark's power comes from its singularity.
- **Don't** use identical white-card grids with hover-overlay reveals — the generic creative-portfolio template this system explicitly rejects.
- **Don't** use gradient text (`background-clip: text` + gradient) — prohibited.
- **Don't** use glassmorphism — prohibited.
- **Don't** use `border-left` or `border-right` greater than 1px as a colored accent stripe — prohibited.
- **Don't** add shadows to resting card surfaces. The flat frame rule applies.
- **Don't** use over-minimal layouts that read as timid or academic — athletic minimalism has energy. If it feels empty rather than purposeful, add scale, not decoration.
- **Don't** use Inter at 700+ weight. That weight slot belongs to Barlow Condensed.
- **Don't** write long case study descriptions. The work speaks; the text supports. Two sentences is a ceiling, not a floor.
- **Don't** add decorative elements outside the work itself: no background textures, no ornamental rules, no dividers, no pattern fills.
