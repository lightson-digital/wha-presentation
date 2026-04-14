Restyle the existing wha-presentation.html using the Stripe design system from DESIGN.md. The current version uses Inter font, a light #FAFAFA background, and LOD brand blue #0A84FF. Replace all of that with Stripe's visual system. Keep all slide content, structure, speaker notes, and JS interaction logic exactly as-is.

## What to change

### Colors — replace the entire CSS :root block

| Current (LOD)              | Replace with (Stripe)                    |
|----------------------------|------------------------------------------|
| `--bg: #FAFAFA`            | `--bg: #1c1e54` (Brand Dark indigo)      |
| `--white: #1A1A1A`         | `--white: #FFFFFF`                       |
| `--near-black: #1A1A1A`    | `--near-black: #061b31` (Deep Navy)      |
| `--blue: #0A84FF`          | `--accent: #533afd` (Stripe Purple)      |
| `--brand-blue: #0D80D8`    | `--accent-hover: #4434d4`               |
| `--muted: rgba(26,26,26,0.55)` | `--muted: rgba(255,255,255,0.7)`    |
| `--dim: rgba(26,26,26,0.35)`   | `--dim: rgba(255,255,255,0.4)`      |
| `--border: rgba(26,26,26,0.09)` | `--border: rgba(255,255,255,0.1)` |
| `--green: #0A9960`         | `--green: #15be53`                       |
| `--red: #DC2626`           | `--red: #ea2261` (Stripe Ruby)           |

### Typography

- Replace `'Inter'` with `'sohne-var', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`
- All slide text gets `font-feature-settings: "ss01"` — this is Stripe's typographic DNA
- Monospace elements (prompt block): `'SourceCodePro', 'SFMono-Regular', monospace`
- Keep weight 300 for display and body (already correct), weight 400 for labels/buttons

### Shadows — add Stripe's blue-tinted shadow system

Cards, callout boxes, property cards, and elevated elements get:
```css
box-shadow: rgba(50,50,93,0.25) 0px 30px 45px -30px, rgba(0,0,0,0.1) 0px 18px 36px -18px;
```
Remove any existing plain borders on cards and replace with the shadow + a subtle `border: 1px solid rgba(255,255,255,0.1)`.

### Border radius

Cap all border-radius at 8px max. The current HTML uses 10px in several places — bring those down to 8px. Stripe is conservative: 4px for buttons/badges, 6px for standard containers, 8px for featured cards.

### Dark background adaptations

- Slide backgrounds: `--bg` (#1c1e54)
- Speaker notes panel: keep dark (`rgba(5,5,10,0.97)` is fine)
- Nav bar gradient: change from `rgba(250,250,250,0.95)` to `rgba(28,30,84,0.95)`
- Cards/callout boxes: `background: rgba(255,255,255,0.06)` with `border: 1px solid rgba(255,255,255,0.08)`
- Score badges (red): `background: rgba(234,34,97,0.15); color: #ea2261`
- Active-fix journey stages: `background: rgba(83,58,253,0.1); border-color: rgba(83,58,253,0.3)`
- Contrast columns (NOT/ARE): adapt to dark — NOT uses ruby tint, ARE uses green tint, both on dark

### Specific component tweaks

- `.section-label::after` line: use `--accent` (#533afd) instead of blue
- `.price-badge`: background `#533afd`
- `.prompt-block`: use `rgba(83,58,253,0.08)` background, `rgba(83,58,253,0.2)` border
- Progress track bar: `#533afd`
- All hover states and interactive accents: `#533afd`

## Do NOT change

- Slide content, text, or HTML structure
- Speaker notes object
- Navigation JS logic
- Slide count or order
- Any interaction behavior (arrow keys, N key, click zones)

## Output

Overwrite wha-presentation.html with the restyled version.
