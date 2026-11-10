# Mark's Site design system: "Sketchbook"

Slate teal and lilac on a light cream page, plum-black ink, thin line-art outlines and
grid-paper detail, like a designer's wireframe sketchbook. Flat: no gradient fills and no
blurry glows.

- Tokens: [`static/css/tokens.css`](static/css/tokens.css)
- Components: [`static/css/site.css`](static/css/site.css), loaded after each layout's inline styles

6Clues and Pub Quizzes still use the earlier green tokens. Copy these two files over when
they move to this look.

## Principles

1. **Line art over shadows.** Cards, buttons, frames and icon tiles get a 1.5px ink outline (`--line`).
   Depth comes from a *hard* offset lilac block (`--shadow-hover`), never a blur.
2. **Teal is the brand, lilac is the accent.** Teal for the hero band, buttons and links.
   Lilac for shapes behind things, icon tiles, the featured card and hover blocks.
3. **Text on lilac is always dark plum** (`--on-lilac`), in both themes.
4. **Two typefaces.** Figtree (geometric sans, 700–800) for headings, navigation and buttons.
   Bitter (sturdy serif, 400) for reading text. Both are loaded from Google Fonts.
5. **Wireframe motifs.** "Browser window" frames (title bar + three dots), grid paper and
   rounded lilac blocks offset behind content. Use them sparingly: the hero, plus one per page at most.
6. **Cream, not beige.** The page is a light, slightly pink cream (`#f6f1ea`) that only works
   next to the teal and lilac. Don't pair it with tan or brown.

## Tokens

| Token | Light | Dark | Use |
|---|---|---|---|
| `--bg` | `#f6f1ea` | `#15232a` | Page |
| `--card` | `#ffffff` | `#1d2f37` | Cards, buttons, frames |
| `--text` | `#26132a` | `#f6f1ea` | Ink: body and headings |
| `--muted` | `#55455a` | `#c6bccb` | Secondary text |
| `--line` | `#26132a` | `#c6bccb` | Line-art outlines |
| `--border` | ink 16% | cream 16% | Quiet dividers only |
| `--field-border` | `#7d6f80` | `#8a9aa1` | Inputs (3:1) |
| `--grid` | ink 10% | cream 8% | Grid-paper lines |
| `--band` / `--on-band` | `#36677a` / `#f6f1ea` | `#2c5566` / `#f6f1ea` | Hero band and its text |
| `--accent` | `#36677a` | `#8cc3d6` | Focus ring, small UI |
| `--accent-strong` (+ `-hover`) | `#2c5566` | `#2c5566` | Primary button fill, white text |
| `--accent-text` | `#2f5d6e` | `#9fd0e1` | Links and teal text |
| `--lilac` | `#f3cdf7` | `#e9b6ee` | Shapes, icon tiles, hover blocks |
| `--lilac-soft` | `#f8e4fa` | `#3a2840` | Featured card fill |
| `--lilac-text` | `#6b2d73` | `#f0c8f4` | Lilac-toned text |
| `--on-lilac` | `#26132a` | `#26132a` | Text and icons on lilac |
| `--shadow-hover` / `--shadow` | 6px / 8px lilac offset | 6px / 8px `#6b4a72` offset | Hover lift, embeds |
| `--radius` / `--radius-button` / `--radius-feature` | 10 / 8 / 24px | | Cards / buttons / lilac blocks |
| `--font-display` / `--font-body` | Figtree / Bitter | | Headings & UI / reading |

Dark mode is the `html.dark` class, set before paint by the inline script in each layout.

## Common patterns

```css
.card       { border: 1.5px solid var(--line); border-radius: var(--radius); background: var(--card); }
.card:hover { transform: translate(-3px, -3px); box-shadow: var(--shadow-hover); }
.btn-primary { background: var(--accent-strong); color: #fff; border-radius: var(--radius-button); }
.btn:hover  { background: var(--lilac); color: var(--on-lilac); }
.icon-tile  { background: var(--lilac); color: var(--on-lilac); border: 1.5px solid var(--line); }
.band       { background: var(--band); color: var(--on-band); }
:focus-visible { outline: 3px solid var(--accent); outline-offset: 3px; }
```

Grid paper is an inline SVG pattern (see `.profile-wrap` in `site.css`), not a CSS gradient.

## Accessibility (WCAG 2.1 AA)

- All text pairs are at least 4.5:1 in both themes (most 7:1+). Cream on the teal band is 5.5:1 (light) and 7.2:1 (dark).
- Outlines, input borders and focus rings are at least 3:1.
- Status is never colour alone. Keep `:focus-visible` outlines.
- Recheck contrast whenever a colour changes.
