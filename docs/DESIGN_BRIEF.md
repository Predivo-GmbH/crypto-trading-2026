# CRYPTO26 — Design Brief

## Product Context
Personal crypto trading dashboard for executing a disciplined accumulation strategy during the 2026 bear/consolidation phase, positioning for the expected 2027 bull cycle. Single user (Roger). Not a SaaS product.

## Brand Direction

### Visual Identity: Industrial Terminal Command Center
A high-tech dark dashboard combining near-black backgrounds with vibrant neon green accents. The design embraces industrial terminal aesthetics — monospace typography dominates, uppercase labels, code-like syntax patterns, and bracket-wrapped status indicators. Sharp corners, hairline borders, and a matrix-inspired color palette create a sophisticated command center feel.

### Key Aesthetics
- **Dark Foundation:** Near-black backgrounds create depth, reduce eye strain, and establish an immersive command center environment
- **Neon Green Accent:** Vibrant green signals activity, success, and interactivity across the entire interface
- **Monospace Dominance:** JetBrains Mono for 95% of text — immediate technical credibility and developer-native feel
- **Geometric Display:** Space Grotesk for large metrics, headlines, and page titles — authoritative and modern
- **Uppercase Convention:** Labels, navigation, buttons, badges all use CAPS for industrial authority and terminal heritage
- **Code Syntax Patterns:** Bracket status indicators `[ACTIVE]`, comment prefixes `// SYSTEM`, underscore naming `CUSTOMER_ID`
- **Zero Decoration:** No shadows, no gradients, no rounded corners — pure terminal precision with hairline borders

### Logo Direction
Geometric minimal tech — clean geometric shapes, minimal lines, monospace-inspired. Reference brands: Coinbase, Stripe, Linear. The mark should work as a favicon and be recognizable at 16px.

## Color Mode
Light + Dark mode. Dark is primary; light is secondary/alternative.

### Dark Mode Palette (Primary)
| Token | Value | Role |
|-------|-------|------|
| bg-page | #0C0C0C | Main canvas background |
| bg-sidebar | #080808 | Sidebar, deeper dark |
| bg-card | #0A0A0A | Card/component surfaces |
| bg-elevated | #141414 | Nested/elevated surfaces |
| bg-subtle | #1A1A1A | Avatar backgrounds, placeholders |
| text-primary | #FFFFFF | Primary text |
| text-secondary | #8A8A8A | Labels, metadata |
| text-muted | #6A6A6A | Placeholders, close icons |
| text-on-accent | #0C0C0C | Text on green backgrounds |
| accent-green | #00FF88 | Primary accent — active, CTAs, success |
| accent-green-20 | #00FF8820 | Badge backgrounds, subtle highlights |
| accent-green-10 | #00FF8810 | Active nav background tint |
| accent-orange | #FF8800 | Warning indicators, alerts |
| accent-orange-20 | #FF880020 | Warning badge backgrounds |
| accent-red | #FF4444 | Error states, negative values |
| border-gray | #2F2F2F | Component borders, dividers |
| border-light | #3F3F3F | Subtle borders on elevated surfaces |

### Light Mode Palette (Secondary)
| Token | Value | Role |
|-------|-------|------|
| bg-page | #FAFAFA | Main canvas background |
| bg-sidebar | #F5F5F5 | Sidebar |
| bg-card | #FFFFFF | Card surfaces |
| bg-elevated | #F0F0F0 | Nested surfaces |
| bg-subtle | #E8E8E8 | Placeholders |
| text-primary | #0C0C0C | Primary text |
| text-secondary | #6A6A6A | Labels, metadata |
| text-muted | #9A9A9A | Placeholders |
| text-on-accent | #0C0C0C | Text on green backgrounds |
| accent-green | #00CC6A | Primary accent (slightly muted for light bg) |
| accent-green-20 | #00CC6A20 | Badge backgrounds |
| accent-green-10 | #00CC6A10 | Active nav tint |
| accent-orange | #E67700 | Warning (muted for light bg) |
| accent-orange-20 | #E6770020 | Warning badges |
| accent-red | #DC3545 | Error states |
| border-gray | #E0E0E0 | Component borders |
| border-light | #D0D0D0 | Subtle borders |

## Typography
| Role | Font | Weight | Size | Letter Spacing |
|------|------|--------|------|----------------|
| Page Title | Space Grotesk | 700 | 42px | -1px |
| Metric Value | Space Grotesk | 700 | 32px | -1px |
| Section Title | Space Grotesk | 600 | 18px | 0 |
| Logo Text | JetBrains Mono | 600 | 16px | 1px |
| Page Subtitle | JetBrains Mono | 400 | 14px | 0 |
| Body/Table Cells | JetBrains Mono | 500 | 13px | 0 |
| Navigation/Meta | JetBrains Mono | 500-600 | 12px | 0.5px |
| Labels/Headers | JetBrains Mono | 500-700 | 11px | 0.5px |
| Alert Labels | JetBrains Mono | 700 | 9px | 0 |

## Spacing Scale
4px base unit. Scale: 2, 4, 6, 8, 10, 12, 16, 20, 24, 32, 40, 48, 64.

## Corner Radius
**0px everywhere.** Zero rounded corners — terminal/command-line aesthetic.

## Icons
Lucide icon family. Thin stroke icons matching terminal aesthetic.
- Navigation: 16px
- Buttons: 14px
- Status indicators: 12px
- Placeholders: 28px

## Brand Collateral
Not included — personal project.

## Component Library Scope
Full set (~59 components) with all variants and states.

## Key Screens (9 total — Desktop + Mobile)

### Primary Navigation (sidebar)
1. **Dashboard** — Overview: BTC price, portfolio value, DCA streak, next catalyst, halving cycle tracker, top narratives
2. **DCA Engine** — DCA schedules, total invested, cost basis, P&L, weekly budget, schedule table
3. **Narrative Scanner** — AI-powered narrative cards with scores, descriptions, tokens, sentiment data
4. **Catalyst Calendar** — FOMC dates, midterms, halving markers, countdowns, historical impact stats
5. **Portfolio** — Unified holdings, allocation breakdown by narrative, performance vs BTC benchmark

### Secondary Screens
6. **Login** — Auth screen with OTP or password
7. **Settings** — Preferences, API keys, notification config, DCA rules
8. **Asset Detail** — Deep dive into a specific coin/token with price history, holdings, DCA history
9. **Trade Log** — Transaction history with filters, export capability

## Anti-Slop Rules
These rules MUST be followed to prevent generic AI design output:

1. **No rounded corners** — this is a terminal aesthetic, not a friendly consumer app
2. **No gradients on backgrounds** — solid colors only, depth comes from layered near-blacks
3. **No shadows** — borders and color differentiation define hierarchy
4. **No emoji in UI** — use Lucide icons only
5. **No blue as primary** — green (#00FF88) is THE accent color
6. **No serif fonts** — JetBrains Mono + Space Grotesk only
7. **All labels uppercase** — consistency with terminal convention
8. **Status indicators use brackets** — `[ACTIVE]`, `[PENDING]`, `[ERROR]`
9. **Comment-style subtitles** — `// MARKET OVERVIEW`, `// NAVIGATION`
10. **No decorative elements** — every element must serve navigation, understanding, decision-making, or action-taking
