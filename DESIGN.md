# Design System Specification: The Fertile Canvas

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"Tactile Intelligence."** It moves away from the sterile, "dashboard-in-a-box" aesthetic and instead adopts a high-end editorial approach to agricultural data. By blending the precision of Sri Lankan agrotechnology with an organic, layered visual language, we create a platform that feels like a premium digital ledger.

The system breaks the traditional grid through **intentional asymmetry** and **overlapping surface tiers**. This isn't just a tool; it's a curated experience. We prioritize extreme readability—crucial for outdoor use under the bright Sri Lankan sun—without sacrificing the "signature" feel of a world-class digital product. 

## 2. Colors & Atmospheric Tones
The palette is a sophisticated interpretation of the Sri Lankan landscape: lush vegetation, rich cinnamon-soil, and monsoonal skies.

### The "No-Line" Rule
To achieve a premium editorial look, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined solely through background color shifts or subtle tonal transitions.
*   Use `surface-container-low` (#f4f4f0) sections sitting on a `surface` (#faf9f5) background to define distinct content areas.
*   This creates a "seamless" feel that looks more like a physical object than a digital wireframe.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine paper.
*   **Lowest Tier:** `surface` (#faf9f5) – The main canvas.
*   **Middle Tier:** `surface-container-low` (#f4f4f0) – For secondary content blocks.
*   **Highest Tier:** `surface-container-highest` (#e2e3df) – For interactive elements and high-priority cards.
*   Nesting elements within these tonal shifts creates depth without the visual noise of lines.

### Signature Textures & Glass
*   **The Glass Rule:** For floating elements like mobile navigation bars or weather tickers, use semi-transparent `surface` colors with a 20px-30px backdrop-blur. This ensures the interface feels integrated with the "environment" behind it.
*   **Gradients:** Use subtle linear gradients transitioning from `primary` (#206223) to `primary_container` (#3a7b3a) for main CTAs to add "soul" and depth.

## 3. Typography: The Editorial Voice
We utilize a dual-font strategy to balance character with data-driven clarity.

*   **Display & Headlines (Manrope):** Chosen for its geometric modernism. Large-scale headlines should feel authoritative, using `display-lg` (3.5rem) to anchor a page.
*   **Body & Labels (Inter):** The workhorse font. Inter’s high x-height and neutral character make it exceptionally legible for multi-language support (English, Sinhala, and Tamil).
*   **The Hierarchy:** Use `headline-sm` (#1a1c1a) for technical data headers to ensure they pop against light backgrounds. Labels (`label-md`) should be used sparingly but with high contrast (`on_surface_variant` #40493d) to ensure readability in direct sunlight.

## 4. Elevation & Depth
Depth in this system is achieved through **Tonal Layering** rather than heavy shadows.

*   **The Layering Principle:** Place a `surface_container_lowest` (#ffffff) card on a `surface_container_low` (#f4f4f0) section. This creates a soft, natural "lift" that mimics ambient light hitting a surface.
*   **Ambient Shadows:** When an element must float (e.g., a critical alert or a floating action button), use an extra-diffused shadow.
    *   *Value:* `0px 20px 40px rgba(26, 28, 26, 0.06)` (A tinted shadow using the `on-surface` color).
*   **The "Ghost Border" Fallback:** If a border is required for extreme accessibility needs, use the `outline_variant` (#bfcaba) at 20% opacity. **Never use 100% opaque borders.**

## 5. Components

### Buttons
*   **Primary:** Rounded-xl (1.5rem) or full (9999px). Uses the `primary` (#206223) to `primary_container` (#3a7b3a) gradient. High-contrast `on_primary` (#ffffff) text.
*   **Secondary:** `surface_container_high` (#e8e8e4) background with `on_surface` (#1a1c1a) text. No border.

### Cards & Lists
*   **Forbid Dividers:** Do not use horizontal lines to separate list items. Use vertical white space (Spacing `4` or `5`) or alternating background tints (`surface_container_low` vs `surface_container_lowest`).
*   **Agricultural Tickers:** Use `tertiary_container` (#0072b6) with a subtle Glassmorphism effect for live price tickers or weather alerts.

### Input Fields
*   **Style:** `surface_container_highest` (#e2e3df) background with a `md` (0.75rem) corner radius. 
*   **States:** On focus, use a 2px "Ghost Border" of `primary` (#206223) at 40% opacity.

### Specialized: Data Visualization
*   **Chart Aesthetics:** Use `primary` (crops), `tertiary` (water/sky), and `secondary` (soil/yield) for data points.
*   **The Topographic Map:** Charts should use semi-transparent fills to create layered, topographic area graphs, emphasizing the "Fertile Canvas" theme.

## 6. Do's and Don'ts

### Do
*   **Do** prioritize high contrast (Dark Charcoal on Off-White) for all critical data to assist farmers in the field.
*   **Do** use asymmetrical layouts for Hero sections—place a large display metric overlapping a background image or a secondary surface.
*   **Do** use the Spacing Scale religiously. Spacious layouts (using `10` or `12` units) prevent the UI from feeling cluttered.

### Don't
*   **Don't** use 1px divider lines. They create "visual friction" and look dated.
*   **Don't** use pure black (#000000). Always use `on_background` (#1a1c1a) for a softer, more premium feel.
*   **Don't** use sharp corners. Everything must feel organic; stick to `md` (0.75rem) or `xl` (1.5rem) radiuses.
*   **Don't** clutter the screen with too many metrics. Use the surface tiers to hide secondary information in "drawers" or nested containers.