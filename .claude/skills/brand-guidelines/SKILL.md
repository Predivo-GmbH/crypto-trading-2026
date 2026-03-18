# CRYPTO26 Brand Guidelines — Auto-Enforced Skill

## When This Applies
This skill is automatically enforced during ALL frontend coding tasks for the Crypto Trading 2026 project.

## Token Source of Truth
`docs/design-tokens.json` is the canonical reference. Never hardcode values — always use CSS variables or token references.

## Mandatory Rules

### Colors
- Dark theme is PRIMARY. All dev/preview defaults to dark.
- Use CSS custom properties: `--bg-page`, `--text-primary`, `--accent-green`, etc.
- Green (#00FF88 dark / #00CC6A light) is the ONLY accent color for CTAs, active states, success
- Orange for warnings only. Red for errors/negative values only.
- Never use blue as an accent or primary color.

### Typography
- **Space Grotesk**: Page titles (42px), metric values (32px), section titles (18px) ONLY
- **JetBrains Mono**: Everything else — body, labels, nav, buttons, tables, badges, inputs
- ALL CAPS for: labels, navigation, buttons, badges, table headers, status indicators
- Mixed case ONLY for: body paragraphs, descriptions, long-form text

### Layout
- Corner radius: **0px on everything**. No `rounded-*` classes. No `border-radius`.
- No shadows. No `shadow-*` classes. No `box-shadow`.
- No gradients on backgrounds. Solid colors only.
- Borders: 1px hairline using `--border-default` color
- 4px grid system. All spacing values must be multiples of 4.

### Components
- Status badges use bracket format: `[ACTIVE]`, `[PENDING]`, `[ERROR]`
- Subtitles use comment syntax: `// MARKET OVERVIEW`
- Active nav items: green left border + green-10 background + green text
- Sidebar width: 240px fixed

### Icons
- Lucide icon family ONLY
- Sizes: 12px (status), 14px (buttons), 16px (navigation)
- No emoji in the UI. Ever.

### Dark/Light Theme
- Implement with CSS custom properties on `:root` and `[data-theme="light"]`
- Dark mode variables applied by default
- Light mode overrides via data attribute

### Anti-Patterns (NEVER do these)
- `border-radius: *` (anything > 0)
- `box-shadow: *`
- `background: linear-gradient(*)`
- `font-family: serif` or `font-family: sans-serif` (must specify exact fonts)
- Lowercase labels, navigation, or button text
- Blue accent colors
- Emoji in interface elements
- Rounded badges or pills (use square with 0 radius)
