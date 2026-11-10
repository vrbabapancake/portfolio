# Mark's design system

One look across Mark's Site, 6Clues and Pub Quizzes: flat, warm and green.
The tokens live in [`static/css/tokens.css`](static/css/tokens.css), the same file 6Clues
and Pub Quizzes use. Copy it into a project and build on the variables. Don't hard-code colours.

## Principles

1. **No gradients, glows or purple.** Solid fills only, including headings, buttons and progress bars.
2. **Green carries the brand.** Deep green for buttons, links, headings and progress.
   Brass (`--highlight`) is the only second colour, and it's saved for winners and special moments.
3. **Warm, not clinical.** Off-white "paper" background and green-black ink, not cool slate greys.
4. **Borders over shadows.** Cards get a 1px border and a faint shadow. No big floating drop shadows.
5. **Modest corners.** 14px cards, 10px buttons, 8px tiles. Pills (999px) only for chips and toggles.
6. **System fonts.** `--font` is the native UI stack, heavy weights (800–900) for headings and labels.

## Tokens

| Token | Light | Dark | Use |
|---|---|---|---|
| `--bg` | `#f5f3ec` | `#111713` | Page background |
| `--card` | `#fffefa` | `#1a221d` | Cards, buttons, panels |
| `--text` | `#18211c` | `#e6ebe5` | Body text and headings |
| `--muted` | `#4a564e` | `#b1bbb3` | Secondary text, eyebrows |
| `--card-muted` | `#56625a` | `#a7b2aa` | Secondary text on cards, placeholders |
| `--border` | `#e0ddd2` | `#2c3830` | Decorative dividers only |
| `--field-border` | `#7b847d` | `#6e7b72` | Input outlines (must stay 3:1) |
| `--accent` | `#1e6b45` | `#5cb983` | Focus ring, dots, timers, hover borders |
| `--accent-strong` | `#1a5f3d` | `#22754a` | Primary button fill (white text) |
| `--accent-strong-hover` | `#144a2f` | `#1b643f` | Primary button hover |
| `--accent-text` | `#185a3a` | `#7fd1a2` | Green text: links, brand headings, points |
| `--icon-bg` | `#e2ede4` | `#203a2b` | Pale green chips, selected rows, icon tiles |
| `--ring` | green 28% | green 35% | Focus glow around inputs |
| `--highlight` / `--highlight-text` | `#f4dd9a` / `#3d2f05` | `#4a3d12` / `#f6e3a6` | Winner row, special callouts |
| `--success` / `--success-bg` | `#1d6b3a` / `#e5f1e7` | `#6fcf93` / `#18301f` | Correct, saved |
| `--danger` / `--danger-bg` | `#b3261e` / `#fbeceb` | `#f28b82` / `#3a1c1a` | Errors, delete |

Dark mode is the `html.dark` class (set by `theme.js` from the toggle or the system setting).

## Common patterns

```css
.btn-primary { background: var(--accent-strong); color: #fff; border-radius: var(--radius-button); }
.btn-primary:hover { background: var(--accent-strong-hover); }
.brand-text { color: var(--accent-text); }            /* replaces old gradient headings */
.card { background: var(--card); border: 1px solid var(--border); border-radius: var(--radius); box-shadow: var(--shadow-card); }
.field { border: 1px solid var(--field-border); }
.field:focus { outline: none; border-color: var(--accent); box-shadow: 0 0 0 3px var(--ring); }
:focus-visible { outline: 3px solid var(--accent); outline-offset: 3px; }
.feature { border-left: 6px solid var(--accent); }    /* emphasis without a gradient wash */
```

In dark mode, text on `--success` and `--danger` fills switches to dark (`#052e16`, `#450a0a`), because those fills turn light.

## Accessibility (WCAG 2.1 AA)

- Every text/background pair above is at least **4.5:1** in both themes; most are 6:1 or higher.
- Input borders, focus rings and progress marks are at least **3:1** against their background.
- Status is never shown by colour alone: correct and wrong always carry ✓ / ✗ or words.
- Keep visible focus outlines and don't remove `:focus-visible`.
- When you change a colour, recheck its contrast (e.g. webaim.org/resources/contrastchecker).

## How Mark's Site uses it

Both layouts (`layouts/index.html`, `layouts/_default/list.html`) link `{{ "css/tokens.css" | relURL }}`
and keep only site-specific extras (`--topbar`, `--shadow-soft`) inline. Dark mode is the `html.dark`
class, set before paint by the inline script in each layout. Buttons inside content pages
(e.g. `content/programming/_index.md`) use `var(--accent-strong)` too.
