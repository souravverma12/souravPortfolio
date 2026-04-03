# Design System Document: The Cinematic Developer Portfolio

## 1. Overview & Creative North Star: "The Neon Architect"
The Creative North Star for this design system is **"The Neon Architect."** 

We are moving away from the "template-heavy" look of standard developer portfolios. Instead, we are building a high-end, editorial experience that feels like a premium digital terminal. This system treats code as art, using expansive negative space, intentional asymmetry, and depth-driven layering. We bypass rigid grids in favor of a "floating" layout where elements breathe within a deep, nocturnal atmosphere. The goal is to convey Sourav Verma’s technical precision through a sophisticated, futuristic lens.

---

## 2. Colors: Depth Over Definition
Our palette is rooted in the deep void of `#060e20` (Background), punctuated by the vibrant energy of tech-centric cyans and purples.

### The "No-Line" Rule
**Traditional 1px borders are strictly prohibited for layout sectioning.** 
Boundaries must be defined through tonal shifts. A section break is not a line; it is a transition from `surface` to `surface-container-low`. By utilizing the Material surface tiers, we create a "machined" look that feels integrated and expensive.

### Surface Hierarchy & Nesting
To create a sense of professional polish, we use **Nesting Logic**:
- **Base Layer:** `surface` (#060e20)
- **Primary Sections:** `surface-container-low` (#091328)
- **Interactive Cards:** `surface-container` (#0f1930)
- **High-Focus Elements:** `surface-container-highest` (#192540)

### The Glass & Gradient Rule
To achieve the "Futuristic" requirement, use **Glassmorphism** for floating UI (e.g., Navigation Bars, Hovering Tooltips). 
*   **Formula:** `surface-variant` at 40% opacity + `backdrop-blur: 20px`.
*   **Gradients:** Use "Soul Gradients" for primary CTAs and active states. Transition from `primary` (#72dcff) to `primary-container` (#00d2ff) at a 135-degree angle to simulate a light source emitting from the top-left.

---

## 3. Typography: Editorial Technicality
We utilize a dual-sans-serif approach to balance "High-Tech" with "High-Readability."

*   **Display & Headlines (Space Grotesk):** This is our "Technical Signature." Its geometric quirks provide a futuristic, architectural feel. Use `display-lg` (3.5rem) for hero statements with tight letter-spacing (-0.02em) to create an authoritative, editorial impact.
*   **Body & Titles (Manrope):** Chosen for its exceptional legibility and modern proportions. Use `body-lg` (1rem) for project descriptions to ensure the user’s focus remains on the content.
*   **Labels (Manrope):** Small-caps or increased tracking should be applied to `label-md` when used for "Tech Stack" tags to give them a "micro-chip" metadata aesthetic.

---

## 4. Elevation & Depth: The Layering Principle
We reject the standard "Drop Shadow." Instead, we use **Tonal Layering** and **Ambient Light**.

*   **The Layering Principle:** Depth is achieved by placing a `surface-container-lowest` card inside a `surface-container-high` section. This creates "recessed" depth, making the UI feel carved rather than pasted.
*   **Ambient Shadows:** For floating elements, use a shadow color derived from `on-surface` (#dee5ff) at 5% opacity with a 32px blur. It should feel like a soft glow, not a dark smudge.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline-variant` (#40485d) at **15% opacity**. This creates a "vapor-thin" edge that suggests a boundary without interrupting the visual flow.

---

## 5. Components: Precision Primitives

### Buttons (The Kinetic Trigger)
- **Primary:** Gradient fill (`primary` to `primary-container`), no border, `md` (0.375rem) roundedness. Text color: `on-primary`.
- **Secondary:** Transparent background with a `Ghost Border` and `primary` text.
- **Hover State:** Increase the `backdrop-blur` and slightly shift the gradient angle.

### Cards (The Project Module)
- **Rule:** Forbid divider lines within cards.
- **Structure:** Use `surface-container-low` with `xl` (0.75rem) roundedness. Use `title-lg` for project names and `label-md` for metadata.
- **Interaction:** On hover, transition the background to `surface-container-highest` and apply a subtle `primary` outer glow (4px blur).

### Chips (Tech Stack Tags)
- **Selection Chips:** Use `secondary-container` (#6e208c) with `on-secondary-container` text. 
- **Shape:** `full` roundedness (pills).
- **Aesthetic:** Backgrounds should be semi-transparent (80%) to allow the underlying surface to ground the element.

### Input Fields
- **Base:** `surface-container-lowest` background. 
- **Active State:** A 1px `Ghost Border` using `primary` at 40% opacity. 
- **Typography:** `body-md` for user input, `label-sm` for floating labels.

### Additional Component: The "Terminal List"
- For the "Experience" or "Services" section, avoid standard lists. Use a vertically stacked layout where each item is separated by a 48px `vertical-spacer` (no lines). Use a `primary` colored vertical accent bar (2px width) only on the active/focused item.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts (e.g., a large display heading on the left with a project card offset to the right).
*   **Do** use `on-surface-variant` (#a3aac4) for secondary text to maintain the dark-mode atmosphere.
*   **Do** lean into `surface-container-lowest` (#000000) for high-contrast "Inky" depth in feature sections.

### Don't:
*   **Don't** use pure white (#FFFFFF). Always use `on-surface` (#dee5ff) to prevent eye strain.
*   **Don't** use standard "box-shadows" that look like they belong on a light-themed SaaS app.
*   **Don't** use 1px dividers. If you need to separate content, use an 80px gap or a subtle change in surface tier.
*   **Don't** use "default" roundedness. Stick strictly to the `xl` (0.75rem) for containers and `md` (0.375rem) for interactive elements to maintain a custom feel.