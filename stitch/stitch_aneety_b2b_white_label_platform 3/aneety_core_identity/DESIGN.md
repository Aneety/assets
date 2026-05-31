---
name: Aneety Core Identity
colors:
  surface: '#fdf7ff'
  surface-dim: '#ded8e0'
  surface-bright: '#fdf7ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f8f2fa'
  surface-container: '#f2ecf4'
  surface-container-high: '#ece6ee'
  surface-container-highest: '#e6e0e9'
  on-surface: '#1d1b20'
  on-surface-variant: '#494551'
  inverse-surface: '#322f35'
  inverse-on-surface: '#f5eff7'
  outline: '#7a7582'
  outline-variant: '#cbc4d2'
  surface-tint: '#6750a4'
  primary: '#4f378a'
  on-primary: '#ffffff'
  primary-container: '#6750a4'
  on-primary-container: '#e0d2ff'
  inverse-primary: '#cfbcff'
  secondary: '#63597c'
  on-secondary: '#ffffff'
  secondary-container: '#e1d4fd'
  on-secondary-container: '#645a7d'
  tertiary: '#765b00'
  on-tertiary: '#ffffff'
  tertiary-container: '#c9a74d'
  on-tertiary-container: '#503d00'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e9ddff'
  primary-fixed-dim: '#cfbcff'
  on-primary-fixed: '#22005d'
  on-primary-fixed-variant: '#4f378a'
  secondary-fixed: '#e9ddff'
  secondary-fixed-dim: '#cdc0e9'
  on-secondary-fixed: '#1f1635'
  on-secondary-fixed-variant: '#4b4263'
  tertiary-fixed: '#ffdf93'
  tertiary-fixed-dim: '#e7c365'
  on-tertiary-fixed: '#241a00'
  on-tertiary-fixed-variant: '#594400'
  background: '#fdf7ff'
  on-background: '#1d1b20'
  surface-variant: '#e6e0e9'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  headline-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  data-mono:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 16px
  label-caps:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 12px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  container-margin-desktop: 32px
  container-margin-mobile: 16px
  gutter: 16px
  density-dense: 8px
  density-comfortable: 16px
---

## Brand & Style
The design system is engineered for high-utility B2B operations, prioritizing clarity, trust, and speed of decision-making. The aesthetic is **Corporate Modern**, blending systematic efficiency with a refined, understated interface that recedes to highlight user data.

The target audience includes back-office operators, dental technicians, and field representatives. The UI must evoke a sense of "reliable machinery"—stable, predictable, and precise. We utilize a high-density layout to minimize scrolling for power users, balanced by generous whitespace in mobile-first views to ensure accessibility for field activities.

## Colors
The color architecture is built on **Semantic White-labeling**. 

1.  **Primary Brand Token:** Used for headers, primary actions, and active states. Aneety defaults to a professional Navy, while Lia utilizes a medical-grade Teal.
2.  **Operational Status:** These are immutable across tenants to ensure safety. The `financial` token (Indigo) is reserved specifically for custody-related data and pricing.
3.  **Neutral Scale:** A cool-gray palette is used to define the "container" of the application, ensuring that tenant-specific brand colors pop without creating visual fatigue.

## Typography
This design system uses **Inter** for all UI elements to ensure maximum legibility and a neutral, professional tone. 

- **Data Legibility:** For IDs, tracking numbers, and financial values, we utilize **JetBrains Mono** to prevent character confusion (e.g., 0 vs O) and ensure tabular alignment.
- **Hierarchy:** Use `label-caps` for secondary metadata and table headers. 
- **Mobile scaling:** Headlines larger than 24px should downscale by one level (e.g., Display-LG becomes Headline-MD) on mobile viewports to preserve horizontal space.

## Layout & Spacing
The layout follows a **Fluid-Fixed Hybrid** model.
- **Desktop:** A 12-column grid with a max-width of 1440px for content. Sidebars are fixed at 240px or 64px (collapsed).
- **Density:** We employ an 8px grid system. For "Power User" views like Data Tables and Order Lists, internal padding is reduced to 8px (`density-dense`). For consumer-facing or mobile views, we increase this to 16px (`density-comfortable`).
- **Mobile-First:** For field activities, we use a single-column stack with 16px safe-area margins. Touch targets for buttons and inputs must never drop below 44px in height regardless of visual density.

## Elevation & Depth
Depth is managed through **Tonal Layers** rather than heavy shadows to maintain a clean, "flat-plus" dashboard aesthetic.

- **Level 0 (Background):** `neutral.background`. Used for the main app canvas.
- **Level 1 (Surface):** `neutral.surface` with a 1px `neutral.border`. Used for the main cards and table containers.
- **Level 2 (Overlay):** Used for modals and dropdowns. These utilize a soft, 15% opacity shadow (Primary color tinted) with a 12px blur to indicate temporary interaction.
- **Contextual Depth:** In mobile views, use a subtle 4px bottom-shadow on the navigation bar to indicate its fixed position over scrolling content.

## Shapes
The shape language is **Soft and Structural**.
- **Standard Radius:** 4px (0.25rem) for inputs, buttons, and small containers to maintain a professional, sharp-edged look.
- **Large Radius:** 8px (0.5rem) for primary dashboard cards.
- **Status Pills:** Always use a `3` (Pill-shaped) setting for status badges to distinguish them from interactive buttons.

## Components

### Status Badges
Pill-shaped with a 10% opacity background of the status color and a 100% opacity text label. This ensures high contrast without overwhelming the visual field in dense tables.

### Data Tables
- **Row Height:** 40px for dense, 56px for comfortable.
- **Alignment:** Numbers are right-aligned; text is left-aligned.
- **Row Actions:** Hidden until hover on desktop; always visible as a "More" icon on mobile.

### Operational Timelines
A vertical 2px dashed line connecting circular status nodes. Completed steps use `primary`, active steps use `info` with a pulse animation, and pending steps use `neutral.border`.

### Multi-step Forms
Progress is shown via a top-anchored stepper. On mobile, this collapses to a "Step X of Y" text indicator to maximize screen real estate for input fields.

### Mobile Offline Indicator
A persistent, slim bar at the top of the viewport using `status.warning` if the device is offline, transitioning to `status.success` briefly when sync is complete.