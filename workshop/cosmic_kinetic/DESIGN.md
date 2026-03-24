# Design System Strategy: Cosmic Precision & Ethereal Depth

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Celestial Grid."** 

Unlike standard "tech" templates that rely on rigid borders and flat backgrounds, this system mimics the experience of looking at a drone light show against the night sky: deep, infinite depth punctuated by precise, vibrant points of light. We achieve a "High-End Editorial" feel by using extreme typographic scale contrasts and intentional asymmetry. Elements should feel like they are orbiting a central narrative, utilizing overlapping "Glassmorphism" layers to create a sense of physical space and advanced technology. 

This is not a flat interface; it is a three-dimensional environment where light defines form.

---

## 2. Color & Surface Architecture
The palette is rooted in the `background` (#0A0E1A), a deep midnight indigo that serves as our "canvas."

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Traditional borders flatten the experience. Instead, boundaries must be defined through:
*   **Tonal Shifts:** Transitioning from `surface` to `surface-container-low` (#0E1320).
*   **Luminous Glows:** Using a subtle `primary` (#C1FFFE) outer glow (5-10% opacity) to suggest an edge.
*   **Negative Space:** Utilizing the Spacing Scale (e.g., `12` or `16` tokens) to create rhythmic separation.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, semi-transparent lenses.
*   **Base:** `surface` (#0A0E1A).
*   **Secondary Content:** `surface-container` (#141928).
*   **Elevated Elements:** `surface-container-high` (#1A1F2F).
*   **Active "Drone" Nodes:** `surface-container-highest` (#202537).

### The "Glass & Gradient" Rule
To capture the "Cosmic Tech" aesthetic, use `backdrop-blur` (20px+) on elements using `surface-variant` at 60% opacity. For primary CTAs, apply a linear gradient from `primary` (#C1FFFE) to `primary_dim` (#00E6E6) at a 135-degree angle to provide "visual soul."

---

## 3. Typography: Futuristic Editorial
We pair **Space Grotesk** (Display/Headlines) with **Inter** (Body) to balance technical precision with human readability.

*   **Display-LG (3.5rem):** Reserved for hero moments. Use tight letter-spacing (-0.04em) and `on-background` color.
*   **Headline-MD (1.75rem):** Use `secondary` (#FF51FA) for emphasis words within headlines to mimic "light-leak" highlights.
*   **Body-MD (0.875rem):** Always use `on-surface-variant` (#A7AABB) for long-form text to maintain a sophisticated, low-contrast hierarchy that reduces eye strain against the dark background.
*   **Label-SM (0.6875rem):** All-caps with +0.1em tracking. Use this for "technical data" readouts or drone coordinates.

---

## 4. Elevation & Depth
In this system, light is the primary architect.

*   **The Layering Principle:** Depth is achieved by placing a `surface-container-lowest` card on a `surface-container-low` section. This creates a "recessed" look, making the content feel like it's integrated into the hardware of the drone platform.
*   **Ambient Shadows:** Shadows are never black. Use a `0px 20px 40px` blur with the color `primary` at 6% opacity. This mimics the "glow" of a drone light reflecting off a surface.
*   **The "Ghost Border" Fallback:** If a container needs more definition, use `outline-variant` (#444756) at **15% opacity**. It should feel felt, not seen.
*   **Glassmorphism:** Use `surface-bright` (#252B3F) with 40% opacity and a `backdrop-filter: blur(12px)` for floating navigation menus.

---

## 5. Signature Components

### Buttons (The "Light Source")
*   **Primary:** Gradient of `primary` to `primary_dim`. Corner radius: `full`. No border. Add a `primary` drop shadow at 20% opacity.
*   **Secondary:** Ghost style. `outline` (#717584) at 20% opacity with `on-primary` text.
*   **Tertiary:** Text-only in `tertiary` (#BF81FF), using `label-md` styling.

### Cards & Data Clusters
*   **Strict Rule:** No dividers. Use `surface-container-low` backgrounds and `1.4rem` (token `4`) internal padding.
*   **Drone Status Chips:** Use `secondary_container` (#A900A9) with `on-secondary_container` text. Apply a subtle pulse animation to the background to signify "live" telemetry.

### Input Fields
*   Background: `surface-container-lowest` (#000000).
*   Active State: Transition the `outline` to `primary` with a 2px inner glow.
*   Corner Radius: `md` (0.75rem).

### The "Nebula" Tooltip
*   Background: `tertiary_container` (#9C42F4) at 80% opacity with heavy blur.
*   Text: `on-tertiary_container` (#FFFFFF).
*   Animate: A soft fade-in with a 2px vertical slide.

---

## 6. Do's & Don'ts

### Do:
*   **Do** use asymmetrical layouts. Place a large `Display-LG` title on the left and a small `Body-SM` technical description on the far right.
*   **Do** overlap elements. Let a "Glass" card partially cover a background gradient to create depth.
*   **Do** use `secondary` (#FF51FA) and `tertiary` (#BF81FF) for "interactive points" only—treat them like beacons in the dark.

### Don't:
*   **Don't** use pure white (#FFFFFF) for body text. It is too harsh. Use `on-surface` (#E2E4F6).
*   **Don't** use 90-degree corners. Everything must use at least the `DEFAULT` (0.5rem) radius to feel "approachable."
*   **Don't** use solid "divider lines" between list items. Use a 1px shift in `surface` color or simply 0.7rem of whitespace.
*   **Don't** clutter the screen. If a drone show needs space to breathe, the UI does too.