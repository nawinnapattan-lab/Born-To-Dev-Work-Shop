# Design System Strategy: The Quiet Canvas

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"The Quiet Canvas."** In an era of digital noise, this system functions as a sanctuary. We are moving away from the rigid, grid-locked "app" feel toward a high-end editorial experience that prioritizes the space between elements as much as the elements themselves.

To achieve this, we reject standard container-based layouts in favor of **Intentional Asymmetry** and **Organic Layering**. By utilizing expansive white space (breathing room), overlapping typography, and soft, nested surfaces, we create a UI that feels grounded and rhythmic—mimicking the natural flow of a guided meditation.

---

## 2. Colors & Tonal Depth
The palette is a sophisticated blend of earth and sky: Sage Greens (`primary`), Muted Blues (`secondary`), and Warm Neutrals (`surface`).

### The "No-Line" Rule
To maintain a sense of tranquility, **1px solid borders are strictly prohibited** for sectioning or containment. Boundaries must be defined through:
*   **Background Shifts:** Transitioning from `surface` to `surface-container-low`.
*   **Soft Transitions:** Using `surface-container-highest` to define a header area against a `surface` body.

### Surface Hierarchy & Nesting
Treat the interface as a physical stack of fine, handmade paper.
*   **The Foundation:** Use `surface` (#fcf9f2) as the base for all screens.
*   **The Content Block:** Use `surface-container-low` (#f6f3ec) for primary content areas.
*   **The Elevated Detail:** Use `surface-container-lowest` (#ffffff) for interactive cards sitting atop container-low backgrounds to create a "pollen-light" lift.

### The "Glass & Gradient" Rule
For floating elements, such as music players or navigation bars, use **Glassmorphism**. Apply `surface` colors at 80% opacity with a `24px` backdrop blur. 
*   **Signature Textures:** For primary CTAs and hero backgrounds, use a subtle radial gradient: `primary` (#4a654e) to `primary_container` (#8ba88e). This adds a "living" depth that flat colors lack.

---

## 3. Typography
The typographic system creates a dialogue between the traditional (`notoSerif`) and the contemporary (`manrope`).

*   **Display & Headlines (Noto Serif):** These are the "voice" of the app. Use `display-lg` for mindfulness quotes and `headline-md` for section titles. The serif choice provides a sense of authority, heritage, and calm.
*   **Body & Labels (Manrope):** All functional text uses Manrope. Its clean, geometric nature ensures readability during low-light meditation sessions. 
*   **Editorial Scaling:** Don't be afraid of scale. A `display-lg` quote should have significant "air" around it, often taking up the top 40% of a screen to set a contemplative mood.

---

## 4. Elevation & Depth
In this system, depth is a feeling, not a technical effect. We utilize **Tonal Layering** to guide the eye.

*   **The Layering Principle:** Instead of shadows, stack surface tiers. Place a `surface-container-lowest` card on a `surface-container` background. The slight shift in "warmth" creates natural hierarchy.
*   **Ambient Shadows:** If a floating action requires a shadow, it must be "Ambient."
    *   **Blur:** 32px to 64px.
    *   **Opacity:** 4%–6%.
    *   **Color:** Use a tinted shadow based on `on_surface` (#1c1c18) rather than pure black.
*   **The "Ghost Border" Fallback:** If a container requires a boundary for accessibility, use the "Ghost Border"—the `outline-variant` (#c2c8c0) at **15% opacity**.
*   **Glassmorphism & Depth:** Use semi-transparent layers for persistent elements (like a bottom play bar). This allows the colors of the meditation artwork to bleed through, keeping the user grounded in the visual experience.

---

## 5. Components

### Buttons
*   **Primary:** Pill-shaped (`full` roundedness). Use the signature gradient from `primary` to `primary_container`. Type is `title-sm` in `on_primary`.
*   **Secondary/Tertiary:** `surface-container-high` background with `primary` text. No borders.

### Cards & Lists
*   **Forbid Dividers:** Do not use lines to separate list items. Use 24px–32px of vertical white space (Spacing Scale) or subtle background shifts using the `surface-container` tiers.
*   **Cards:** Use `lg` (2rem) or `xl` (3rem) corner radius. Cards should feel like "stones" in a garden—smooth and substantial.

### Interactive Inputs
*   **Input Fields:** Use `surface-container-highest` as the fill. The active state is signaled by a "Ghost Border" of `primary` at 40% opacity and a soft `primary_container` glow.
*   **Chips:** Pill-shaped (`full`). Use `secondary_container` for selected states to provide a cool, calming contrast to the sage green primary actions.

### Mindfulness Components
*   **The Breath Pacer:** A large, centered circle using `primary_fixed_dim`. Use a slow, eased scale animation.
*   **Progress Rings:** Use `secondary` with a soft gradient to `secondary_fixed_dim`. Avoid high-contrast "completion" visuals; the progress should feel like a soft filling of a vessel.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Asymmetry:** Align text to the left but place supporting imagery slightly off-center to create a bespoke, editorial feel.
*   **Prioritize Negative Space:** If a screen feels "busy," increase the padding. The goal is to make the user feel they have "room to breathe."
*   **Use Subtle Motion:** All transitions should use long durations (500ms+) with "cubic-bezier(0.4, 0, 0.2, 1)" easing to mimic natural movement.

### Don't:
*   **Don't use 100% Black:** Even for text. Use `on_surface` (#1c1c18) to maintain a soft, organic contrast.
*   **Don't use sharp corners:** Every element must have at least `sm` (0.5rem) rounding; hero elements should use `xl` (3rem).
*   **Don't crowd the edges:** Maintain a minimum 24px screen margin at all times. High-end design requires "luxury of space."