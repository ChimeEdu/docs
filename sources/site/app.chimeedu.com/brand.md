# Source: https://app.chimeedu.com/brand

BRAND GUIDELINES

# The ChimeEdu Brand

Colors, typography, and the rules for using them. This page is the public reference for anyone presenting ChimeEdu — in the product, in the classroom, or in print. When in doubt, keep it simple: navy leads, blue interacts, and content always comes first.

## Logo

The ChimeEdu mark is a white mortarboard on a solid Chime Navy tile, set beside the wordmark in the system font at semibold weight. On dark backgrounds the tile inverts: white tile, navy mortarboard. Nothing else about the lockup changes between themes.

ChimeEdu

On light backgrounds — navy tile, white mark, navy wordmark.

ChimeEdu

On dark backgrounds — white tile, navy mark, white wordmark.

### Logo misuse

Correct — solid tile, original colors.

Never stretch or distort the tile.

Never recolor the tile or the mark.

Never place the logo on busy or gradient backgrounds.

### Download the logo

Official assets, exactly as rendered in the product — SVG for any size, PNG with transparent background. The wordmark is set in Inter SemiBold and converted to outlines, so the lockup renders identically everywhere.

![ChimeEdu mark: white mortarboard on a navy rounded tile](https://app.chimeedu.com/brand-assets/chimeedu-mark-onlight.svg)

Mark — light backgrounds

- [SVG](https://app.chimeedu.com/brand-assets/chimeedu-mark-onlight.svg)
- [PNG 512](https://app.chimeedu.com/brand-assets/chimeedu-mark-onlight-512.png)
- [PNG 1024](https://app.chimeedu.com/brand-assets/chimeedu-mark-onlight-1024.png)

![ChimeEdu mark: navy mortarboard on a white rounded tile](https://app.chimeedu.com/brand-assets/chimeedu-mark-ondark.svg)

Mark — dark backgrounds

- [SVG](https://app.chimeedu.com/brand-assets/chimeedu-mark-ondark.svg)
- [PNG 512](https://app.chimeedu.com/brand-assets/chimeedu-mark-ondark-512.png)
- [PNG 1024](https://app.chimeedu.com/brand-assets/chimeedu-mark-ondark-1024.png)

![ChimeEdu lockup: navy mark tile beside the ChimeEdu wordmark in navy](https://app.chimeedu.com/brand-assets/chimeedu-lockup-onlight.svg)

Lockup — light backgrounds

- [SVG](https://app.chimeedu.com/brand-assets/chimeedu-lockup-onlight.svg)
- [PNG 1024](https://app.chimeedu.com/brand-assets/chimeedu-lockup-onlight-1024.png)
- [PNG 2048](https://app.chimeedu.com/brand-assets/chimeedu-lockup-onlight-2048.png)

![ChimeEdu lockup: white mark tile beside the ChimeEdu wordmark in white](https://app.chimeedu.com/brand-assets/chimeedu-lockup-ondark.svg)

Lockup — dark backgrounds

- [SVG](https://app.chimeedu.com/brand-assets/chimeedu-lockup-ondark.svg)
- [PNG 1024](https://app.chimeedu.com/brand-assets/chimeedu-lockup-ondark-1024.png)
- [PNG 2048](https://app.chimeedu.com/brand-assets/chimeedu-lockup-ondark-2048.png)

[Download all assets (.zip)](https://app.chimeedu.com/brand-assets/chimeedu-brand-assets.zip)12 files + usage notes, ~190 KB

## Primary colors

Two colors do the heavy lifting. Chime Navy is the brand; Chime Blue is the interaction layer. Everything else supports them.

Chime Navy

Copy

#101533

var(--chime-primary)

The primary brand color. Navbars, primary buttons, hero backgrounds, and the logo tile. When ChimeEdu needs one color, it’s this one.

Chime Blue

Copy

#3D5AFE

var(--chime-blue)

The interactive accent — links, focus outlines, and highlights. Also exposed as --chime-accent for focus/accessibility styling. Reserved for interaction, never decoration.

### Canvas & surfaces

Canvas White

Copy

#FFFFFF

var(--chime-bg-light)

Default page background in light mode.

Blue-Tint White

Copy

#F9FAFD

var(--chime-bg-blue-light)

Card and panel background — a barely-there blue tint that keeps surfaces on-brand without coloring them.

Cool Grey

Copy

#F3F5F8

var(--chime-secondary)

Sidebar and secondary surface background; maps to Bootstrap’s secondary background.

## Secondary colors

The functional palette communicates state — success, error, warning — and the neutrals carry text and structure. The raw functional colors are for fills, badges, and decoration; when the same meaning has to be carried by _text_, use the accessible variants below.

### Functional palette

Chime Green

Copy

#00C896

var(--chime-green)

Success states, “Added” badges, and positive indicators. Decoration and fills only — use the accessible variant for text.

Chime Coral

Copy

#FF6F61

var(--chime-coral)

Errors, destructive actions, and alerts. Decoration and fills only — use the accessible variant for text.

Chime Yellow

Copy

#FFD600

var(--chime-yellow)

Warnings and “Fixed” badges. Always paired with dark text — never white.

### Neutrals

Charcoal

Copy

#212121

var(--chime-charcoal)

Body text and emphasis text in light mode.

Slate

Copy

#616161

var(--chime-slate)

Subdued text, captions, and disabled items.

Light Grey

Copy

#E0E0E0

var(--chime-light-grey)

Borders, dividers, and hairlines.

### Accessible text variants

Accessible Coral

Copy

#C2261A

var(--chime-coral-accessible)

Text-safe red — 5.0:1 contrast on white. Every danger/error message set in text uses this, not raw coral.

Accessible Green

Copy

#007A5C

var(--chime-green-accessible)

Text-safe green — 4.9:1 contrast on white. Every success message set in text uses this, not raw green.

### Content-type accents

Each content type on the platform carries a consistent accent across navigation, search, and creation flows. These are identification colors — used for icon tiles and highlights, never for text or backgrounds behind text.

- Classrooms#FF6F61
- Activities & Quizzes#00C896
- Assessments#FFD600
- Study Guides#9333ea
- Experiences & Maps#3D5AFE
- Timelines#D4956A
- Fill-in-the-Blank#06B6D4
- Quick Activities#ec4899

## Typography

ChimeEdu pairs two serif display faces with a fast, familiar system stack for the interface. Display faces set the tone; the system stack does the work.

Ring in a new way to learn.

### DM Serif Display

Display face — hero and page titles.

**Weights:** Regular 400 (+ italic). No other weights ship — never synthesize bold.

**Sizing:** Hero titles: 4rem (responsive clamp from 2.25rem), letter-spacing −2px, line-height 1.2.

Every classroom tells a story.

### Castoro

Secondary serif — section headings on marketing and documentation pages.

**Weights:** Regular 400.

**Sizing:** Section headings: 1.35–2rem, letter-spacing −0.5px, weight 400.

Readable paragraphs for long study sessions.

### Inter

Long-form reading — study guides and article layouts.

**Weights:** 400 / 500 / 600 / 700.

**Sizing:** Article body: 1–1.1rem, line-height 1.7–1.8.

R7T4XW

### Share Tech Mono

Join codes and game PINs — numeric display only, never running text.

**Weights:** Regular 400.

**Sizing:** Code slots: large sizes with generous letter-spacing.

### Interface font — system stack

Body copy and product UI use the native system font of each device — instant to load and familiar to every reader. Weights 400 through 700 are available; headings inside the product use semibold 600.

\-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif

Aa 400Aa 500Aa 600Aa 700

### Type scale

Display / hero title

DM Serif Display 400 · 4rem (clamp from 2.25rem) · letter-spacing −2px · line-height 1.2

Display heading

Marketing section heading

Castoro 400 · 1.35–2rem · letter-spacing −0.5px

Section heading

Product content heading

System stack · semibold 600 · 1.75rem (.h3) / 1.25rem (.h5)

Content heading

Body text

System stack · regular 400 · 1rem · line-height 1.5–1.65

Body copy carries most of the interface in the system stack.

Small / meta text

System stack · regular 400 · 0.875rem

Captions, footer links, and helper text.

## Using the brand

The short version: navy leads, blue interacts, status colors stay honest about contrast, and the logo is never remixed. Here is the full list.

### Approved

- **Lead with navy.** Chime Navy (#101533) is the anchor — primary buttons, navbars, hero backgrounds, and the logo tile.

- **Reserve blue for interaction.** Chime Blue (#3D5AFE) means “you can act here”: links, focus outlines, and interactive highlights.

- **Pair yellow with dark text.** Yellow badges and warnings always carry dark text for WCAG-compliant contrast.

- **Use the accessible variants for status text.** Set error and success text in #C2261A / #007A5C — the raw coral and green are for fills and decoration.

- **Keep content surfaces neutral.** Cards and panels stay white or subtly tinted in both themes, so student work and content lead.

- **Build with the design tokens.** Reference colors via the --chime-\* custom properties so light and dark themes both render correctly.

- **Give the logo room.** The logo tile sits on solid, quiet backgrounds with clear space around it of at least a quarter of the tile’s width.

### Not approved

- **Don’t alter the logo.** No recoloring, stretching, rotating, outlining, or drop shadows on the tile or the mark.

- **Don’t flood surfaces with brand color.** Brand-colored cards, panels, or content backgrounds are off-limits — accents accent.

- **Don’t set text in raw coral or green.** #FF6F61 and #00C896 fail text-contrast requirements on white. Use the accessible variants.

- **Don’t put white text on yellow.** #FFD600 with white text is unreadable and fails WCAG. Yellow takes dark text, always.

- **Don’t use display faces for body copy.** DM Serif Display, Castoro, and Share Tech Mono are for headings, accents, and codes — not paragraphs or UI labels.

- **Don’t embolden DM Serif Display.** It ships in regular 400 only; synthesized bold distorts the letterforms.

- **Don’t invent new accents or hardcode hex.** New color pairs need a contrast check and a token. One-off hex values break dark mode.

Color contrast on this page follows our [accessibility commitment](https://app.chimeedu.com/accessibility) — WCAG 2.1 Level AA. Questions about brand use? [Get in touch](https://app.chimeedu.com/contact).