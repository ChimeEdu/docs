# Source: https://app.chimeedu.com/accessibility

ACCESSIBILITY

# Accessibility Statement

ChimeEdu is committed to making interactive learning available to every student and teacher, regardless of ability. This page documents our conformance with WCAG 2.1 Level AA, what we ship today, what we’re actively fixing, and how to reach us with feedback.

[Download as PDF](https://app.chimeedu.com/api/accessibility/export.pdf)

Effective: July 23, 2026Report version: 1.7Standard: WCAG 2.1 AAFormat: VPAT 2.5 Rev WCAG

Lighthouse Accessibility

\-0.0%

Average across 10 public routes

Based on automated axe-core / Lighthouse Accessibility checks as of April 29, 2026. Automated tooling detects approximately 40–50% of WCAG violations; the remainder (screen-reader pronunciation, keyboard task completion, contrast on dynamic states, motion / cognitive impact) requires manual testing — see §9.

## 1\. Our Commitment

ChimeEdu’s mission is interactive education for every classroom. That mission only works if every student can use the platform — including students who navigate by keyboard, who use a screen reader, who need extra time, who rely on captions, who can’t perceive certain colors, or who use the platform with reduced motion or high contrast preferences.

We treat accessibility as a non-negotiable engineering requirement, not a polish step. Our internal guidelines (binding on every code change) target the Web Content Accessibility Guidelines version 2.1 at Level AA, with selected WCAG 2.2 success criteria adopted ahead of formal targeting. New features go through a per-feature accessibility checklist before merge.

## 2\. Scope of This Statement

This statement covers the **authenticated ChimeEdu web application** at [app.chimeedu.com](https://app.chimeedu.com) — including the homepage, marketing pages, sign-up and sign-in flows, classrooms, all seven activity types (Map, Quiz, Flash Cards, Timeline, Assessment, Experience, Study Guide), and the user dashboard.

The following are **out of scope** for this report:

- The internal API documentation surface at `/api-docs` (admin-authenticated developer tooling, not part of the user-facing product).
- Generated PDF exports: **timeline PDF exports are server-side rendered with WeasyPrint and PDF/UA-1 tagged** (real text, heading hierarchy, alt text, document metadata preserved). Study-guide and Knowledge Base “Print” flows use the browser’s native print-to-PDF, which inherits the source document’s accessibility properties. Assessment exports do not currently exist as a product feature.
- Pre-release feature previews on the staging environment.
- User-generated content (the platform’s authoring tools provide accessibility affordances such as alt-text fields, but the accessibility of any individual classroom’s content is the author’s responsibility).
- Third-party services embedded within the product (Google Analytics, YouTube embeds, Mailchimp newsletter widgets, Cloudflare-served reCAPTCHA when enabled).

## 3\. Conformance Status

The Web Content Accessibility Guidelines (WCAG) define requirements for designers and developers to improve accessibility for people with disabilities. They define three levels of conformance: **Level A**, **Level AA**, and **Level AAA**.

ChimeEdu is **partially conformant** with WCAG 2.1 Level AA. _Partially conformant_ means that some parts of the content do not fully conform to the accessibility standard. The specific success criteria that are not yet fully supported, and our remediation timelines for each, are listed in §6 (Known Limitations) and detailed against every WCAG 2.1 success criterion in §7 (Detailed Conformance Table).

**Audit baseline:** A full internal audit conducted in April 2026 surfaced 36 findings across all severity levels. As of July 23, 2026, all 10 Critical findings AND all 11 High findings have been remediated and shipped to production. **3 findings remain open (0 High, 1 Medium, 2 Low / best-practice)**. The single open Medium finding is an intentional deferral tied to a specific product milestone (multilingual authoring); the 2 Low findings are best-practice / AAA hygiene. See §6 below for the complete list.

## 4\. Standards Applied

- **WCAG 2.1 Level AA** — primary conformance target, as published by the World Wide Web Consortium (W3C).
- **WCAG 2.2 selected criteria** — we have adopted SC 2.4.11 (Focus Not Obscured) and SC 2.5.7 (Dragging Movements) ahead of any formal WCAG 2.2 targeting, and are tracking SC 2.5.8 (Target Size, Minimum) as a remediation goal.
- **VPAT 2.5 Rev WCAG** — format used for the conformance report below, published by the Information Technology Industry Council (ITI).
- **Section 508 of the Rehabilitation Act** — the WCAG 2.1 AA conformance documented here aligns with the Revised Section 508 standards (which incorporate WCAG 2.0 AA by reference). A Section 508 specific report is available on request from [accessibility@chimeedu.com](mailto:accessibility@chimeedu.com).

## 5\. Compatibility With Browsers and Assistive Technology

ChimeEdu is designed to be compatible with the following:

- **Browsers:** The most recent two major versions of Chrome, Firefox, Safari (macOS and iOS), and Microsoft Edge. The platform is not optimized for Internet Explorer.
- **Screen readers:** NVDA (with Firefox or Chrome) and VoiceOver (macOS Safari, iOS Safari) are the primary screen readers we test against. JAWS compatibility is expected via the same standards-based ARIA implementation but is not part of our regular test rotation.
- **Operating systems:** Recent versions of Windows, macOS, iPadOS, iOS, ChromeOS, and Android.
- **Input methods:** Mouse, keyboard, touch, and voice control. The platform avoids drag-only interactions for primary tasks. Map activities offer non-drag alternatives for both pin repositioning (Teacher-Mode Move-pin overlay) and map panning (directional pad paired with Leaflet’s built-in zoom +/−).
- **Zoom & reflow:** All page content reflows to 320 CSS pixels at 200% browser zoom without horizontal scrolling, except where two-dimensional content (data tables, maps, code) requires it.
- **User preferences honored:** `prefers-reduced-motion`, `prefers-color-scheme` (dark mode), and browser-set font sizes.

## 6\. Known Limitations

Despite our best efforts, the following accessibility limitations are present in the current production build. Each item below references the WCAG success criterion it touches and our target remediation window. We track these openly because procurement reviewers and adopting institutions deserve an honest picture of what to expect.

### 6.1 High-priority items

**All High-priority items previously listed in this section have been remediated and shipped to production.** Closure shipped across the April 2026 cycle:

- **Dropdown and mega-menu keyboard navigation** (WCAG 2.1.1, 4.1.2) — closed; Account dropdown, Features mega-menu, marketing-site theme dropdown, and authenticated-app theme dropdown all implement the WAI-ARIA Authoring Practices menu-button keyboard pattern.
- **Mobile hamburger focus restoration** (WCAG 2.4.3) — closed; Escape and outside-click both restore focus to the hamburger trigger.
- **Quiz timer accommodations** (WCAG 2.2.1) — closed; per-quiz teacher-toggleable “extended time mode” triples per-question countdowns when on.
- **Assessment one-sitting accommodation override** (WCAG 2.2.1) — closed; per-student `allows_extended_time` flag set per IEP / 504 plan via the classroom roster bypasses one\_sitting and extends per-question timers.
- **Map list-view alternative** (WCAG 1.3.1, 2.1.1, 4.1.2) — closed; Leaflet map activities now offer a toggleable List View with a semantic, keyboard-operable list of pins.
- **Video caption guarantee** (WCAG 1.2.2, 1.2.5) — closed; YouTube embeds request captions on by default and the Study Guide editor surfaces a publish-time accessibility reminder.
- **Placeholder text contrast on join-code slots** (WCAG 1.4.3) — closed; placeholder color now meets ~7:1 light / ~5.5:1 dark.
- **Icon-only button accessible names** (WCAG 4.1.2) — closed; modal close buttons across the application carry descriptive `aria-label` values.
- **TipTap rich-text editor naming** (WCAG 1.3.1, 4.1.2) — closed; all five editor surfaces expose `role="textbox"` + `aria-label` on the editing region and `aria-pressed` on toggleable toolbar buttons.
- **Toast notification region** (WCAG 4.1.3) — closed; both polite and assertive live regions pre-render at provider mount so screen readers observe them before the first toast arrives.

_The full audit closure trail (commit SHAs, deploy dates, per-finding diffs) is available on request from [accessibility@chimeedu.com](mailto:accessibility@chimeedu.com)._

### 6.2 Medium-priority items (intentionally deferred to specific product milestones)

- **Language of parts** (WCAG 3.1.2): The TipTap authoring UI does not yet provide a way to mark non-English passages with a `lang` attribute. No production content is currently known to require this; queued for the multilingual authoring milestone.

### 6.3 Low-priority & best-practice items

- Modal backdrop-click dismissal behavior could be more clearly documented for keyboard-equivalent dismissal.
- Spinner + textual loading-state pattern could be wrapped in a single `role="status"` block for additional robustness.

## 7\. Detailed Conformance Table (VPAT 2.5 Rev WCAG)

The following table reports conformance against every Level A and Level AA success criterion in WCAG 2.1, plus three Level AA criteria new in WCAG 2.2 that we are voluntarily tracking. Conformance levels follow the VPAT 2.5 specification:

- **Supports:** the functionality of the product has at least one method that meets the criterion without known defects.
- **Partially Supports:** some functionality of the product does not meet the criterion.
- **Does Not Support:** the majority of product functionality does not meet the criterion.
- **Not Applicable:** the criterion is not relevant to the product.

### 7.1 WCAG 2.1 — Level A

WCAG 2.1 Level A success criteria conformance for ChimeEdu
| SC | Criterion | Conformance | Remarks |
| --- | --- | --- | --- |
| 1.1.1 | Non-text Content | Supports | Alt-text data layer and authoring UI shipped across all platform image surfaces (flashcards, assessment options, activities, study guides, experiences, experience locations and posts, timeline events, per-image map pins, and the assessment-question featured-images JSON array). Author-supplied alt text is honored on render; empty-string alt is preserved as the intentional decorative marker. Server-side timeline PDF exports (WeasyPrint, PDF/UA-1 tagged) preserve the same alt text in the PDF’s structure tree. |
| 1.2.1 | Audio-only and Video-only (Prerecorded) | Not Applicable | The product does not include audio-only or video-only prerecorded media authored by ChimeEdu. User-uploaded YouTube embeds are governed by SC 1.2.2/1.2.5. |
| 1.2.2 | Captions (Prerecorded) | Partially Supports | The platform now requests closed captions on all YouTube embeds by default (cc\_load\_policy=1) and surfaces a publish-time accessibility reminder in the Study Guide editor. Captions still depend on the embedded source video having a caption track — the platform cannot guarantee captions on third-party content authors paste in. |
| 1.2.3 | Audio Description or Media Alternative (Prerecorded) | Partially Supports | Same as 1.2.2 — depends on audio-description tracks being present on the embedded source video. |
| 1.3.1 | Info and Relationships | Supports | Forms, headings, lists, and ARIA landmarks are correctly structured across the application. Leaflet map activities offer a toggleable List View as a parallel keyboard-operable navigation surface. TipTap rich-text editors expose role="textbox" + aria-label naming and toolbar grouping. Heading hierarchy across all 10 public routes descends sequentially without skips (Lighthouse heading-order audit passes 100%). Server-side timeline PDF exports preserve heading hierarchy and list structure in the PDF/UA-1 structure tree. |
| 1.3.2 | Meaningful Sequence | Supports | Reading order matches visual order across the application. Server-side timeline PDF exports preserve event sequence (chronological order) in the PDF’s tagged structure tree. |
| 1.3.3 | Sensory Characteristics | Supports | Instructions do not rely solely on shape, size, or position. |
| 1.4.1 | Use of Color | Supports | Form errors and status messages are paired with text labels and icons; color is never the sole means of conveying information. |
| 1.4.2 | Audio Control | Supports | The platform does not auto-play audio. YouTube embed autoplay parameter is being removed as part of the §6.1 caption work. |
| 2.1.1 | Keyboard | Supports | All primary user flows are keyboard-operable. Account, Features mega-menu, and theme dropdowns implement the WAI-ARIA Authoring Practices menu-button pattern (ArrowUp/Down, Home/End, Escape, focus restoration). Leaflet map activities now offer (a) a List View toggle for keyboard pin selection, (b) a Move-pin overlay with arrow-key + on-screen-button repositioning of selected pins (Teacher Mode), and (c) a directional pad for keyboard / pointer-operable map panning that pairs with the built-in zoom +/− control. |
| 2.1.2 | No Keyboard Trap | Supports | Modal focus traps are correctly bounded; Escape and outside-click both restore focus to the trigger element. |
| 2.1.4 | Character Key Shortcuts | Not Applicable | The product does not implement single-key keyboard shortcuts. |
| 2.2.1 | Timing Adjustable | Partially Supports | Two complementary accommodation paths: (a) per-quiz teacher-toggleable "extended time" mode that triples per-question countdowns for the entire roster, and (b) per-student "extended time" flag (set per IEP / 504 plan via the classroom roster) that bypasses one\_sitting refuse-to-pause and extends per-question timers on assessments. Both paths shipped April 2026. The per-student flag applies to logged-in students only — anonymous assessment takers cannot yet carry the accommodation and are instead prompted, before starting a timed assessment, to log in so it can be applied. Server-side extended-time handling for anonymous takers is planned. |
| 2.2.2 | Pause, Stop, Hide | Supports | No content auto-updates outside user-initiated AI streaming, which the user controls via the modal close action. |
| 2.3.1 | Three Flashes or Below Threshold | Supports | No content flashes more than three times in any one-second window. |
| 2.4.1 | Bypass Blocks | Supports | Skip link to main content is present on every page and is reliably keyboard-focusable as of April 2026. |
| 2.4.2 | Page Titled | Supports | Every route sets a route-specific document title using the convention “ChimeEdu ∙ \[Page Name\]” (bullet operator U+2219, brand-first). Authentication, dashboard, content listing, creation, and player flows all carry their own title; static index.html title remains as the pre-hydration fallback. |
| 2.4.3 | Focus Order | Supports | Focus order matches visual order across the application. Mobile hamburger panel restores focus to the trigger button on Escape and outside-click; modal Escape returns focus to the activating element via the useModalA11y hook. |
| 2.4.4 | Link Purpose (In Context) | Supports | Link text is descriptive within its surrounding context; no “click here” style links remain. |
| 2.5.1 | Pointer Gestures | Supports | No multi-point or path-based gestures are required for any feature. |
| 2.5.2 | Pointer Cancellation | Supports | Single-point activations occur on up-event; abort or undo is available where applicable. |
| 2.5.3 | Label in Name | Supports | Visible button text matches the accessible name on every interactive element. |
| 2.5.4 | Motion Actuation | Not Applicable | The product does not use device-motion or user-motion as an input. |
| 3.1.1 | Language of Page | Supports | The HTML document declares lang=”en”. |
| 3.2.1 | On Focus | Supports | Focus does not trigger context changes. |
| 3.2.2 | On Input | Supports | Input does not trigger context changes; explicit submission is always required. |
| 3.3.1 | Error Identification | Supports | Form errors are programmatically announced via aria-invalid and aria-describedby pointing to icon-prefixed error text. Implementation centralized in the FormField component. |
| 3.3.2 | Labels or Instructions | Supports | Every form carries visible labels and, where asterisks denote required fields, an explanatory legend ("Fields marked \* are required.") with aria-hidden on the asterisk so screen readers receive the textual cue rather than punctuation noise. |
| 4.1.2 | Name, Role, Value | Supports | The component library exposes accessible names, roles, and states for every interactive surface. Dropdown menus use the WAI-ARIA Authoring Practices menu-button pattern with proper role/aria-pressed/aria-checked semantics; icon-only buttons across navbars, modals, and editors carry aria-label; theme dropdowns are now fully React-state-driven with aria-controls linking trigger to menu. |

### 7.2 WCAG 2.1 — Level AA

WCAG 2.1 Level AA success criteria conformance for ChimeEdu
| SC | Criterion | Conformance | Remarks |
| --- | --- | --- | --- |
| 1.2.4 | Captions (Live) | Not Applicable | The product does not include live audio content. |
| 1.2.5 | Audio Description (Prerecorded) | Partially Supports | Same as 1.2.2/1.2.3 — depends on audio-description tracks being present on the embedded source video. |
| 1.3.4 | Orientation | Supports | No content is restricted to a specific display orientation. |
| 1.3.5 | Identify Input Purpose | Supports | Sign-in / registration / forgot-password / reset-password forms set autoComplete for every personal-data field (email, current-password, new-password, given-name, family-name, organization, username). One-time codes (invitation tokens, classroom join codes) intentionally use autoComplete="off" since browser-saved-credential autofill would be noise on those fields. |
| 1.4.3 | Contrast (Minimum) | Supports | Text contrast meets 4.5:1 across the application; brand danger and success colors mapped to accessible variants; classroom join-code placeholder text uses var(--chime-slate) (~7:1 light / ~5.5:1 dark). Server-side timeline PDF export inherits the HTML template’s color tokens (var(--chime-primary) #3D5AFE on white = 7.4:1 for body text, well above the 4.5:1 floor). |
| 1.4.4 | Resize Text | Supports | Text scales to 200% without loss of content or functionality. The application uses relative units throughout the typography scale. |
| 1.4.5 | Images of Text | Supports | Text content is rendered as text, not images, except where decorative branding marks are used. |
| 1.4.10 | Reflow | Supports | Content reflows at 320 CSS pixels at 200% zoom without two-dimensional scrolling, except for genuinely two-dimensional content (data tables, maps). |
| 1.4.11 | Non-text Contrast | Supports | Interactive control borders, focus indicators, and meaningful icons meet 3:1 against their background as of April 2026. |
| 1.4.12 | Text Spacing | Supports | No loss of content or functionality occurs when users override line-height, paragraph spacing, letter spacing, or word spacing within the WCAG-specified ranges. |
| 1.4.13 | Content on Hover or Focus | Supports | Hover/focus-triggered tooltips are dismissible, hoverable, and persistent. |
| 2.4.5 | Multiple Ways | Supports | Pages can be located via primary navigation, footer links, sitemap-like dashboard listings, and direct routing. |
| 2.4.6 | Headings and Labels | Supports | Headings and form labels describe the topic or purpose of the section/control. |
| 2.4.7 | Focus Visible | Supports | Every interactive element shows a visible focus indicator. The .focus-ring-accent utility class enforces a consistent ring across components that previously stripped the default outline. |
| 3.1.2 | Language of Parts | Partially Supports | The platform does not currently surface a UI affordance for authors to mark non-English passages within content. No production content is known to include foreign-language passages today; this becomes priority once multilingual authoring is requested. |
| 3.2.3 | Consistent Navigation | Supports | Navigation appears in the same relative order across pages within the same authentication state. |
| 3.2.4 | Consistent Identification | Supports | Components with the same functionality are identified consistently across the application. |
| 3.3.3 | Error Suggestion | Supports | Form-validation errors include corrective suggestions wherever the cause is known. |
| 3.3.4 | Error Prevention (Legal, Financial, Data) | Not Applicable | The product does not process legal commitments or financial transactions in scope of this report. Account deletion includes a confirmation step. |
| 4.1.3 | Status Messages | Supports | Quiz and assessment timers announce at thresholds via a polite live region; AI streaming output uses the documented off/polite pattern; toast notification regions (polite + assertive) pre-render at provider mount so screen readers observe them before any toast arrives; multi-step modal step progress (Quick-Activity creation) announces transitions as “Step 2 of 4: Add Quiz Questions” via a polite live region. |

### 7.3 WCAG 2.2 — Selected Level AA Criteria (Voluntary Tracking)

The following success criteria are not yet a formal conformance target for this report, but we track them as remediation goals. Inclusion here reflects intent, not a binding claim.

Selected WCAG 2.2 Level AA success criteria voluntarily tracked by ChimeEdu
| SC | Criterion | Conformance | Remarks |
| --- | --- | --- | --- |
| 2.4.11 | Focus Not Obscured (Minimum) | Supports | The April 2026 focus-ring sweep ensures that focused elements receive a visible 2px outline with offset that is not obscured by sticky headers or modals. |
| 2.5.7 | Dragging Movements | Supports | Both drag-driven map surfaces now have non-drag alternatives. Map pin repositioning offers a Teacher-Mode “Move pin” overlay with arrow-key + on-screen-button nudging (Shift for a 10× step; Enter saves; Esc exits). Map panning offers a 4-button directional pad anchored bottom-left of the map, paired with Leaflet’s built-in keyboard arrow-pan when the map container has focus. |
| 2.5.8 | Target Size (Minimum) | Partially Supports | Most interactive controls meet or exceed the 24×24 CSS-pixel minimum. A small number of icon-only controls (e.g., mobile avatar, notification bell) sit below this threshold. Remediation queued in §6.2. |

## 8\. Accessibility Features Supported

The following features are part of the platform’s baseline accessibility support:

- **Skip-to-main-content link** visible on keyboard focus on every page.
- **Programmatic form validation** via a centralized FormField component that wires `aria-invalid` and `aria-describedby` automatically; errors are prefixed with an icon and a textual cue.
- **Modal focus management**: dialogs trap focus, restore focus to the trigger on close, support Escape, and declare `aria-modal` with a labelled heading.
- **Visible focus indicators** on every interactive element via a shared `.focus-ring-accent` utility (2px outline with 2px offset, ≥3:1 contrast).
- **Accessible color tokens**: text-level danger and success colors are mapped to WCAG-AA-conformant variants distinct from the decorative brand palette.
- **Decorative-icon hygiene**: 855+ decorative Bootstrap icons carry `aria-hidden="true"`; icon-only interactive controls carry `aria-label`.
- **Reduced-motion support**: A global `prefers-reduced-motion` rule disables non-essential animation; the quiz confetti effect is JS-gated on the same media query.
- **Threshold live-region announcements** for quiz and assessment timers (60s, 30s, 10s\\u20131s, “Time is up”) with no per-second flooding.
- **Per-image alt text** on flashcards, assessment options, activity covers, study-guide media, experience covers and locations and posts, timeline events, and individual map pin images.
- **Dark mode** with WCAG-conformant contrast on text and meaningful UI elements.
- **OpenDyslexic font option** available for Study Guides.
- **Keyboard-operable activities**: Quiz, Flash Cards, Timeline, Assessment, Study Guide, and Experience flows are operable without a mouse.
- **200% zoom and reflow** at 320 CSS pixels without horizontal scrolling on text content.
- **Pinch-to-zoom preserved**: the platform does not set `user-scalable=no`.

## 9\. How We Assess Conformance

This report is based on the following assessment methods:

- **Internal audit** against WCAG 2.1 Level AA conducted in April 2026, covering all primary user flows, all seven activity types, the dashboard, and authentication. Audit methodology and findings are tracked in our internal `ACCESSIBILITY_AUDIT_APRIL_2026` document and remediated against in source-control history that is publicly browseable on request.
- **Manual testing** with NVDA on Firefox (Windows), VoiceOver on Safari (macOS and iOS), keyboard-only navigation across all primary flows, and 200% browser zoom verification.
- **Automated testing**: Two automated gates run on every pull request to `main`: `eslint-plugin-jsx-a11y` (recommended ruleset) at author time, and `axe-core` via Playwright as a smoke pass on 10 user-facing public routes. Both gates fail the build on any violation with impact ≥ “serious” or any new lint-level a11y error. Wired into CI since 2026-04-27.
- **Per-feature checklist**: Every frontend pull request follows a binding accessibility checklist (keyboard pass, screen-reader smoke, 200% zoom, reduced-motion, contrast ratios) before merge.
- **External audit**: An external third-party accessibility audit is on our roadmap for the post-Alpha release window. Once conducted, the results will be incorporated into a future revision of this report.

## 10\. Feedback & Contact

We welcome feedback on the accessibility of ChimeEdu. If you encounter an accessibility barrier, if you need content in an alternative format, or if you have suggestions for how we can improve, please contact us:

**Email:** [accessibility@chimeedu.com](mailto:accessibility@chimeedu.com) 
**Web form:** [/contact](https://app.chimeedu.com/contact) (please mention “accessibility” in the subject) 
**Response target:** within five business days.

When reporting a barrier, please include: the page URL, a brief description of what you were trying to do, the assistive technology and browser you were using (if any), and what happened (or what didn’t). Screenshots help but are not required.

## 11\. Procurement & Formal Requests

Educational institutions, school districts, and procurement offices are welcome to use this page as the public Accessibility Conformance Report (ACR) for ChimeEdu. The report is published in the VPAT 2.5 Rev WCAG format. For questions about Section 508 alignment, EN 301 549 alignment, or to request a signed and dated PDF mirror of this report, contact [accessibility@chimeedu.com](mailto:accessibility@chimeedu.com).

## 12\. Continuous Improvement

Accessibility is treated as an ongoing engineering commitment, not a one-time project. This statement is reviewed at minimum semi-annually and republished after any audit cycle, after the closure of remediation phases noted in §6, and whenever new functionality materially expands the scope of conformance claims. The most recent review date is shown at the top of this page.

Effective July 23, 2026 · Report version 1.7 · Format VPAT 2.5 Rev WCAG · Standard WCAG 2.1 AA

[Email Accessibility Team](mailto:accessibility@chimeedu.com)