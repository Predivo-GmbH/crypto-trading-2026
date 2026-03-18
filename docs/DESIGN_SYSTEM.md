# CRYPTO26 — Design System Specification

## Overview
Design system for the Crypto Trading 2026 personal dashboard. Industrial terminal command-center aesthetic with dark-first design, neon green accents, and monospace typography.

## Foundations

### Color System
Two themes: **Dark (primary)** and **Light (secondary)**. See `design-tokens.json` for exact values.

**Semantic roles:**
- `bg-page` — deepest background layer
- `bg-sidebar` — navigation background (slightly darker/lighter than page)
- `bg-card` — card and component surface
- `bg-elevated` — nested elements within cards
- `bg-subtle` — placeholders, avatar backgrounds
- `accent-green` — primary interactive color, success, CTAs
- `accent-orange` — warning, caution indicators
- `accent-red` — error, negative values, loss indicators
- `border-default` — structural borders, dividers
- `border-light` — subtle borders on elevated surfaces

### Typography
**Font families:**
- **Space Grotesk** — Display font for page titles, metric values, section headers
- **JetBrains Mono** — System font for everything else (body, labels, navigation, buttons, tables, badges)

**Type scale:** 9px → 11px → 12px → 13px → 14px → 16px → 18px → 32px → 42px

**Convention:** ALL CAPS for labels, navigation, badges, buttons, table headers. Mixed case for body text and descriptions only.

### Spacing
4px base grid. All spacing values are multiples of 4.
- Component internal padding: 8-24px
- Card padding: 20-24px
- Page content padding: 32px vertical, 40px horizontal
- Section gaps: 24px
- Card grid gaps: 16px

### Corner Radius
**0px on all elements.** No exceptions.

### Shadows & Elevation
**No shadows.** Hierarchy established through:
- Color layering (bg-page → bg-card → bg-elevated)
- Border strokes (1px hairline borders)
- Accent color highlights

### Icons
- Family: **Lucide** (thin stroke, terminal-compatible)
- Sizes: 12px (status), 14px (buttons), 16px (navigation), 28px (placeholders)
- Colors follow semantic meaning: green (active/success), orange (warning), red (error), muted gray (inactive)

---

## Component Categories

### Actions
- Button (primary, secondary, outline, ghost, destructive, link)
- Icon Button
- States: default, hover, active, disabled, focus, loading

### Forms
- Input, Textarea, Select, Checkbox, Radio, Switch, Slider, Date Picker, OTP Input, Label
- Form Field (label + input + helper + error)
- States: default, hover, focus, filled, error, disabled

### Display
- Card, Badge/Status Badge, Avatar, Metric Card, Progress, Skeleton, Separator, Tooltip, Kbd
- Status badges use bracket convention: `[ACTIVE]`, `[PENDING]`, `[ERROR]`

### Navigation
- Sidebar, Nav Item (default + active), Breadcrumb, Tabs, Pagination, Menubar
- Active nav: left border accent + green tint background + green text
- Inactive nav: no background + gray text

### Tables
- Table Header, Table Row, Table Cell, Data Table (composed)
- Monospace text, uppercase column headers, hairline row dividers

### Feedback
- Alert, Toast/Sonner, Dialog, Sheet/Drawer
- Variants: info (green), success (green), warning (orange), error (red)

### Overlays
- Modal, Popover, Dropdown Menu, Context Menu, Command Palette

### Layout
- Section Label (comment-style: `// SECTION NAME`), Page Shell, Content Area, Split Pane

---

## Pattern Library

### Metric Card
```
Frame: bg-card, border-default 1px, padding 20, gap 8, vertical layout
  Label: JetBrains Mono 11px 500, text-muted, uppercase, 0.5px tracking
  Value: Space Grotesk 32px 700, text-primary, -1px tracking
  Change: JetBrains Mono 11px 700, accent-green/red, uppercase
```

### Status Badge
```
Frame: accent-*-20 background, padding [4, 8], no radius
  Text: JetBrains Mono 9px 700, accent-* color, "[STATUS]" format
```

### Nav Item (Active)
```
Frame: accent-green-10 bg, left border 2px accent-green, padding [12, 20], horizontal, gap 12
  Icon: Lucide 16px, accent-green
  Text: JetBrains Mono 12px 700, accent-green, uppercase
```

### Comment-Style Subtitle
```
Text: "// SECTION DESCRIPTION", JetBrains Mono 14px 400, text-secondary
```

### Table
```
Table Card: bg-card, border-default 1px, vertical, clip
  Header: padding [16, 20], space_between, bottom border
    Title: JetBrains Mono 11px 700, text-primary, uppercase
    Badge: status badge
  Column Headers: padding [12, 20], bottom border
    Cells: JetBrains Mono 11px 500, text-muted, uppercase
  Rows: padding [16, 20], bottom border (except last)
    Cells: JetBrains Mono 13px 500-600, fill_container
```

---

## Screen Architecture

### Page Shell
- Sidebar (240px fixed) + Main Content (fill_container)
- Main content: 32px/40px padding, 24px section gap
- Header: page title (42px) + comment subtitle + right-side status/action

### Responsive Behavior
| Desktop Element | Mobile (375px) |
|----------------|----------------|
| Sidebar | Bottom tab bar (5 icons) |
| Metric card row | Vertical stack, full-width |
| Data tables | Card list view |
| Two-column layout | Single column stack |
| Side panel | Full-width below main |
| Modal | Full-screen sheet |

---

## Anti-Slop Rules
1. No rounded corners (0px everywhere)
2. No gradients on backgrounds
3. No shadows
4. No emoji in UI
5. No blue as primary accent
6. No serif fonts
7. All labels uppercase
8. Status indicators use `[BRACKETS]`
9. Subtitles use `// COMMENT` style
10. No decorative elements without functional purpose
