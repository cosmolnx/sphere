# LANUX — Web Colour Theme

LANUX uses a restrained blue-grey technical colour system: a near-black dark theme by default, a clean soft-white light theme, and a single locked accent family that ties both together. All values below are extracted directly from the LANUX stylesheet (`:root` and `[data-theme="light"]`) — nothing here is a new design.

## Core Identity

The four locked colours form the foundation of every accent, hover and active state across both themes.

| Colour | HEX | Role |
|---|---|---|
| Primary Strong | `#ABBED3` | Button gradient end, brand mark |
| Primary | `#B0BFD1` | Core accent, button gradient start |
| Primary Tint | `#B9C3D0` | Brand mark gradient |
| Primary Pale | `#CFDEEA` | Reserved / lightest accent tint |

## Dark Theme

Default theme, defined in `:root`.

| Colour | HEX | Purpose |
|---|---|---|
| Main background | `#0B0E14` | Base page background (`--bg`) |
| Secondary background | `#0E1219` | Alternate section background (`--bg-alt`) |
| Surface / card | `#131824` | Cards, inputs, secondary buttons (`--surface`) |
| Elevated surface | `#1A2130` | Hover state for service/work cards (`--surface-elevated`) |
| Primary text | `#EDEFF3` | Headings and body copy (`--text`) |
| Muted text | `#8B93A7` | Nav links, labels, secondary copy (`--text-muted`) |
| Border | `#232B3B` | Default hairline border / nav border-bottom (`--border`) |
| Border — strong | `#2E374A` | Input & secondary-button borders (`--border-strong`) |
| Primary accent | `#B0BFD1` | Accent colour, button gradient start (`--primary`) |
| Accent — strong | `#ABBED3` | Button gradient end, brand mark (`--primary-strong`) |
| Accent — hover/active | `#CBD5E0` | Link underline, focus ring, icon accent (`--icon-accent`, 55% primary / 45% text) |
| On-primary text | `#10141C` | Text on primary button fill (`--on-primary`) |
| Success | `#4CAF7D` | Form success message |
| Error | `#E4685D` | Form validation & error message |

## Light Theme

Override theme, defined in `[data-theme="light"]`.

| Colour | HEX | Purpose |
|---|---|---|
| Main background | `#F6F9FD` | Base page background (`--bg`) |
| Secondary background | `#EEF4FB` | Alternate section background (`--bg-alt`) |
| Surface / card | `#FFFFFF` | Cards, inputs, secondary buttons (`--surface`) |
| Elevated surface | `#FFFFFF` | Hover state for service/work cards (`--surface-elevated`) |
| Primary text | `#12161F` | Headings and body copy (`--text`) |
| Muted text | `#5B6478` | Nav links, labels, secondary copy (`--text-muted`) |
| Border | `#E2E9F3` | Default hairline border / nav border-bottom (`--border`) |
| Border — strong | `#CBD9EC` | Input & secondary-button borders (`--border-strong`) |
| Primary accent | `#B0BFD1` | Accent colour — unchanged from dark (`--primary`) |
| Accent — strong | `#ABBED3` | Button gradient end — unchanged from dark (`--primary-strong`) |
| Accent — hover/active | `#697381` | Link underline, focus ring, icon accent (`--icon-accent`, 55% primary / 45% text) |
| On-primary text | `#12161F` | Text on primary button fill (`--on-primary`) |
| Success | `#4CAF7D` | Form success message (same value as dark theme) |
| Error | `#E4685D` | Form validation & error message (same value as dark theme) |

## CSS Variables

Actual variable names from the LANUX stylesheet:

```css
:root{
  --bg:#0B0E14;
  --bg-alt:#0E1219;
  --surface:#131824;
  --surface-elevated:#1A2130;
  --text:#EDEFF3;
  --text-muted:#8B93A7;
  --border:#232B3B;
  --border-strong:#2E374A;
  --primary:#B0BFD1;
  --primary-strong:#ABBED3;
  --primary-tint:#B9C3D0;
  --primary-pale:#CFDEEA;
  --on-primary:#10141C;
  --icon-accent: color-mix(in srgb, var(--primary) 55%, var(--text) 45%);
}

[data-theme="light"]{
  --bg:#F6F9FD;
  --bg-alt:#EEF4FB;
  --surface:#FFFFFF;
  --surface-elevated:#FFFFFF;
  --text:#12161F;
  --text-muted:#5B6478;
  --border:#E2E9F3;
  --border-strong:#CBD9EC;
  --primary:#B0BFD1;
  --primary-strong:#ABBED3;
  --primary-tint:#B9C3D0;
  --primary-pale:#CFDEEA;
  --on-primary:#12161F;
}
```

**Components:**
- **Buttons** — primary: `linear-gradient(180deg, var(--primary), var(--primary-strong))`, text `var(--on-primary)`. Secondary: transparent fill, `var(--border-strong)` border; hover fills with `var(--surface)` and border becomes `var(--primary)`.
- **Inputs** — background `var(--surface)`, border `var(--border-strong)`, focus border `var(--icon-accent)` with a 30%-opacity primary focus ring.
- **Links** — `var(--text-muted)` at rest, `var(--text)` on hover, underline in `var(--icon-accent)`.
- **Status** — success `#4CAF7D`, error `#E4685D` (16% background fill, 40% border opacity), identical in both themes.

## Usage Rules

- Use the existing LANUX theme tokens — do not introduce random colours.
- Preserve the blue-grey identity; all accents derive from the four locked colours.
- Keep dark and light themes visually consistent.
- Maintain readable contrast, especially for muted text and borders.
- Use semantic colours (`#4CAF7D` success, `#E4685D` error) for status states.

## Design Direction

LANUX uses a restrained blue-grey technical aesthetic with a near-black dark theme and a clean light theme.
