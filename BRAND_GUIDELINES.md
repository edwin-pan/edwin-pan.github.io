# Edwin Pan brand guidelines

These guidelines define a light-mode visual system for the personal site. The direction blends the site's existing academic restraint and organic gradient field with a product-system sensibility inspired by [Better Design's TV Style reference](https://www.better-design.com/design-systems/tv-style): compact surfaces, crisp typographic structure, small uppercase labels, tight component geometry, visible divider rhythm, a light split-flap motif, and restrained signal color.

## Brand character

The site should feel minimal, thoughtful, and quietly technical. It should read as an academic personal site that has learned from mature product design systems: clean hierarchy, deliberate spacing, low visual noise, and just enough interaction polish to feel alive.

Primary qualities:

- Clear before expressive.
- White-dominant, with color used as atmosphere or signal.
- Academic roots, product taste.
- Compact and scan-friendly.
- Warm, not decorative.
- Precise, not sterile.

## Visual translation from the reference

Borrow:

- Tile rhythm: repeated compact units, thin dividers, and subtle "seam" lines.
- Light split-flap modules: white tiles with midpoint hairlines, compact labels, and restrained accent states.
- Tight radii: small corners on chips, cards, buttons, and image frames.
- Label discipline: small uppercase metadata labels with generous tracking.
- Strong typographic confidence: Helvetica-inspired forms, dense but readable.
- Amber-like signaling: use yellow sparingly for primary highlights and focus moments.
- Low-chrome navigation: links and sections should be obvious through spacing and type, not heavy containers.

Do not borrow:

- Dark-mode dominance.
- Literal black split-flap boards.
- Heavy shadows or theatrical contrast.
- Overly mechanical UI that fights the softer personal-site tone.
- Saturated neon accents.

## Color system

White should dominate the page. The organic gradient should remain atmospheric, soft, and mostly behind content rather than becoming the content.

Core neutrals:

| Token | Value | Use |
| --- | --- | --- |
| `--color-canvas` | `#FFFFFF` | Dominant page field |
| `--color-canvas-warm` | `#FCFAF7` | Warm page wash |
| `--color-surface` | `rgba(255, 255, 255, 0.76)` | Light glass surface |
| `--color-surface-solid` | `#FFFFFF` | Solid cards and overlays |
| `--color-text` | `#111827` | Primary text |
| `--color-text-soft` | `rgba(17, 24, 39, 0.76)` | Paragraphs and secondary content |
| `--color-text-muted` | `rgba(17, 24, 39, 0.56)` | Captions, metadata, quiet links |
| `--color-line` | `rgba(17, 24, 39, 0.12)` | Dividers and hairlines |
| `--color-line-strong` | `rgba(17, 24, 39, 0.18)` | Interactive borders |

Accent palette:

| Token | Value | Use |
| --- | --- | --- |
| `--accent-rose` | `#F390CA` | Warm emphasis, hover wash, portrait detail |
| `--accent-green` | `#A3D576` | Research/system signal, quiet success |
| `--accent-orange` | `#FF9365` | Active detail, concise callout |
| `--accent-yellow` | `#FFE15B` | Primary highlight and focus ring |
| `--accent-blue` | `#A3BEFA` | Links, selection, technical signal |

Gradient atmosphere:

- Use the accent colors at low opacity over white.
- Keep the gradient soft, organic, and slow-moving when animated.
- Prefer large blurred fields over discrete decorative blobs.
- Target a white reading surface even when color is visible in the background.
- Avoid any single hue owning the page.

Suggested CSS variables:

```css
:root {
  color-scheme: light;
  --color-canvas: #ffffff;
  --color-canvas-warm: #fcfaf7;
  --color-surface: rgba(255, 255, 255, 0.76);
  --color-surface-solid: #ffffff;
  --color-text: #111827;
  --color-text-soft: rgba(17, 24, 39, 0.76);
  --color-text-muted: rgba(17, 24, 39, 0.56);
  --color-line: rgba(17, 24, 39, 0.12);
  --color-line-strong: rgba(17, 24, 39, 0.18);
  --accent-rose: #f390ca;
  --accent-green: #a3d576;
  --accent-orange: #ff9365;
  --accent-yellow: #ffe15b;
  --accent-blue: #a3befa;
}
```

## Typography

The site can keep Nunito as the active web font while preserving the Helvetica Neue inspiration in the system. Helvetica Neue should remain the conceptual anchor: tight, clear, unornamented, and confident.

Font stack:

```css
font-family: "Nunito", "Helvetica Neue", Helvetica, Arial, sans-serif;
```

Scale:

| Role | Size | Line height | Weight | Use |
| --- | --- | --- | --- | --- |
| Display | `48-72px` | `1.0` | `700` | Hero name |
| Standard header | `24-30px` | `1.1-1.2` | `650-700` | Section titles |
| Statement | `20px` | `1.5` | `400-600` | Opening idea |
| Body | `16px` | `1.6` | `400` | Paragraphs |
| Metadata | `11-13px` | `1.35` | `700` | Labels and section markers |
| Footer | `14-15px` | `1.4` | `400` | Footer/captions |

Rules:

- Keep each viewport to roughly three visible text sizes.
- Use uppercase only for metadata, not for body copy.
- Metadata labels may use `letter-spacing: 0.08em`.
- Avoid negative letter spacing except on the display name, where a very small adjustment is acceptable.
- Prefer sentence case for human-facing section titles.

## Layout

The page should remain single-column-first, with a compact academic rhythm. Product-system cues should appear through spacing, section structure, and divider treatment.

Structure:

- Page width: `min(960px, calc(100% - 2.5rem))`.
- Section spacing: `40-64px` on desktop, `32-44px` on mobile.
- Use thin dividers to separate dense content groups.
- Align content to a strong left edge.
- Keep side-by-side layouts only when they add meaningful scan value.
- Avoid decorative page-section cards.

Reference-inspired layout motifs:

- Section eyebrows as small uppercase labels.
- Repeated rows for affiliations and projects.
- Tiny accent squares or dots for list grouping.
- Thin horizontal seams through cards, link rows, or portrait framing.
- Small split-flap tile groups for metadata, initials, dates, project tags, and section markers.
- Compact link clusters with understated hover states.

## Surfaces and borders

Surfaces should be nearly white, light, and quiet.

Use:

- `1px` borders with `--color-line`.
- `6-8px` radii for repeated cards or compact panels.
- `10-16px` padding for dense rows.
- Very subtle shadows only when layering is needed.
- Inset top or midpoint divider lines to nod to the TV-style tile motif.

Avoid:

- Large rounded cards.
- Nested cards.
- Heavy drop shadows.
- Frosted panels that make text harder to read.

## Light split-flap motif

The split-flap motif is the most literal artifact borrowed from the TV Style reference, but it should be translated into light mode. Think "quiet airport board in daylight," not a dark terminal display.

Use the motif for:

- Short metadata: `OPENAI`, `AGENTS`, `STANFORD`, `SWE-BENCH`.
- Section markers or compact labels.
- A small hero-side detail, such as initials or current focus.
- Project tags and affiliation categories.
- Optional loading or hover states if the site later gains interaction.

Do not use the motif for:

- Full paragraphs.
- Navigation tabs.
- Large decorative walls of letters.
- Anything that competes with the hero name or portrait.

Anatomy:

| Part | Guidance |
| --- | --- |
| Tile | White or warm-white surface with a `1px` hairline border |
| Radius | `4-6px`, tighter than the portrait frame and content groups |
| Seam | A horizontal midpoint line at `rgba(17, 24, 39, 0.08)` |
| Text | Uppercase, `11-13px`, `700`, `0.06-0.1em` tracking |
| Gap | `2-4px` between tiles |
| Accent | One tile or one edge may use an approved accent, usually yellow or blue |
| Shadow | Optional, extremely subtle, mostly inset |

Recommended treatments:

- `Default`: white tile, muted border, dark text.
- `Quiet`: warm-white tile, muted text, no accent.
- `Active`: yellow top border or yellow tile background with dark text.
- `Technical`: blue border or blue dot for research/project labels.
- `Warm`: rose or orange micro-accent for personal details.

Suggested CSS sketch:

```css
.split-flap {
  display: inline-flex;
  flex-wrap: wrap;
  gap: 3px;
  align-items: center;
}

.split-flap__tile {
  position: relative;
  min-width: 1.55rem;
  height: 1.55rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 1px solid var(--color-line);
  border-radius: 5px;
  background: rgba(255, 255, 255, 0.82);
  color: var(--color-text);
  font-size: 0.72rem;
  font-weight: 700;
  line-height: 1;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.9);
}

.split-flap__tile::after {
  content: "";
  position: absolute;
  inset-inline: 0;
  top: 50%;
  height: 1px;
  background: rgba(17, 24, 39, 0.08);
}

.split-flap__tile[data-accent="yellow"] {
  border-color: color-mix(in srgb, var(--accent-yellow) 62%, var(--color-line));
  background: color-mix(in srgb, var(--accent-yellow) 26%, white);
}

.split-flap__tile[data-accent="blue"] {
  border-color: color-mix(in srgb, var(--accent-blue) 58%, var(--color-line));
}
```

Placement examples:

- Above a section title: a three-to-six tile label such as `WORK` or `LABS`.
- Next to a project: a compact category label like `BENCH` or `OSS`.
- Near the hero intro: initials `E P` or a quiet `AGI` marker.
- In a footer detail: a small `2025` tile group before the copyright line.

## Components

Links:

- Default links should use text color plus a faint underline.
- Hover may use `--accent-blue` or a low-opacity rose wash.
- External links should stay compact and text-first.

Buttons and chips:

- Use small radii, compact padding, and clear labels.
- Primary signal may use `--accent-yellow` with dark text.
- Secondary controls should be white with a hairline border.

Cards and rows:

- Prefer rows over bulky cards for education, affiliations, and projects.
- Use a small uppercase category label above or beside content.
- Add a subtle divider line between repeated items.
- One accent mark per row is enough.

Portrait:

- Keep the image human and warm.
- Frame with a thin border and one small accent detail.
- Avoid making the portrait feel like a product mockup.

## Motion

Motion should feel ambient and optional.

- Background gradient may drift slowly over `20-32s`.
- Interactive transitions should be `150-250ms`.
- Use easing that feels calm: `ease`, `ease-out`, or `cubic-bezier(0.2, 0.8, 0.2, 1)`.
- Respect `prefers-reduced-motion`.
- No bouncy, springy, or attention-seeking motion.

## Content voice

The voice should be direct, generous, and precise.

Use:

- Short, declarative statements.
- Clear role and research framing.
- Links that name the destination plainly.
- Personal details as a small human note, not a long aside.

Avoid:

- Marketing claims.
- Over-explaining the site.
- Dense résumé language.
- Generic innovation language.

## Accessibility

- Body text should meet WCAG AA contrast on white.
- Accent colors should not carry meaning alone.
- Use visible focus rings, preferably `--accent-yellow` or `--accent-blue` with an outline.
- Preserve readable line lengths.
- Do not place body copy on busy gradient areas without a solid or highly legible wash.

## Implementation checklist

- Keep white as the dominant visual field.
- Use the approved accent palette only.
- Replace dark TV-style contrast with light surfaces, black text, and soft accent signals.
- Include the light split-flap motif as a recurring but sparse pattern.
- Preserve the organic gradient as atmosphere.
- Introduce compact uppercase metadata labels.
- Use thin dividers and small-radius repeated rows for structure.
- Keep typography disciplined and avoid more than three type sizes per viewport.
- Test mobile for line length, spacing, and non-overlap.
