# Retro Game Discovery Portal – Capstone Project

## Project Description

This project is my Capstone Project for the BAS Application Development program. The selected project archetype is:

**C: Curation & Discovery Portal**

The final application will become a **Retro Game Discovery Portal** where users can browse, discover, and explore classic video games from different consoles, genres, and time periods.

The project is being developed incrementally through weekly milestones. Each week builds upon the previous foundation to create a complete application experience.

---

# Week 02 – Design System Foundation

## Overview

Week 02 focused on creating the design system foundation that will support the rest of the project.

The design system demonstrates modern CSS techniques including:

- OKLCH color tokens
- Light and Dark Mode color variables
- Fluid typography using `clamp()`
- Relative spacing tokens using `rem`
- CSS Cascade Layers (`@layer`)
- Responsive layout principles
- CSS custom properties

The design system serves as the foundation for future project development by creating reusable colors, spacing, and typography rules.

---

# Week 03 – Structural Frames & Semantic Navigation

## Overview

Week 03 expanded the design system into the physical structure of the Retro Game Discovery Portal.

The goal of this milestone was to create a complete visual layout wireframe without adding the final application content.

The layout follows:

**Archetype C: Curation & Discovery Portal**

The structural frame includes:

- A persistent header banner
- Primary navigation
- Left-side filter rail
- Main game catalog area
- Footer section

The layout was created using semantic HTML5 elements and CSS Grid to create an accessible and responsive application foundation.

---

# Features

## Week 02 Features

- Responsive typography using `clamp()`
- Accessible color palette using `oklch()`
- WCAG AA-friendly contrast considerations
- CSS custom properties (design tokens)
- Reusable spacing system
- CSS Cascade Layers for organized styling
- Responsive design foundation

---

## Week 03 Features

- Semantic HTML5 landmarks
- CSS Grid structural layout
- Responsive viewport-based design
- Application header system
- Primary navigation
- Filter sidebar framework
- Main catalog content area
- Footer structure
- Keyboard-accessible navigation focus states
- Mobile responsive layout behavior

---

# Project Structure

```text
my-capstone-project/
│
├── index.html
│
├── week02/
│   ├── index.html
│   └── styles.css
│
└── README.md
```

---

# Application Layout

The Week 03 layout follows the Curation Portal archetype.

## Desktop Layout

```
------------------------------------------------
|                  HEADER                      |
|        Branding + Primary Navigation         |
------------------------------------------------
|              |                               |
|   FILTER     |                               |
|   SIDEBAR    |        GAME CATALOG           |
|              |                               |
------------------------------------------------
|                  FOOTER                      |
------------------------------------------------
```

## Mobile Layout

```
------------------------
|        HEADER        |
------------------------
|       FILTERS        |
------------------------
|       CATALOG        |
------------------------
|       FOOTER         |
------------------------
```

The layout automatically adjusts based on screen size using CSS Grid and responsive media queries.

---

# Semantic HTML Structure

The project uses semantic HTML5 landmarks instead of relying on generic container elements.

Implemented structural elements:

| Element | Purpose |
|---------|---------|
| `<header>` | Contains branding and application header content |
| `<nav>` | Provides primary and secondary navigation links |
| `<main>` | Contains the central game catalog area |
| `<aside>` | Provides filtering and supporting information |
| `<footer>` | Contains copyright and secondary links |

This structure improves accessibility, organization, and future maintainability.

---

# CSS Layout System

The Week 03 structural layout uses CSS Grid.

The layout:

- Occupies the full viewport height using `100dvh`
- Uses Grid template areas
- Uses responsive columns
- Uses Week 02 spacing variables
- Uses OKLCH color variables
- Maintains reusable CSS architecture

Example Grid structure:

```css
grid-template-areas:
    "header header"
    "aside main"
    "footer footer";
```

---

# How to Run

## Option 1 (Recommended)

Open the deployed GitHub Pages website.

## Option 2

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Open the project folder.

Open either file in a modern browser:

```
week02/index.html
```

or

```
week03/index.html
```

No installation, frameworks, or dependencies are required.

---

# Technologies Used

- HTML5
- CSS3
- CSS Custom Properties
- OKLCH Color Space
- CSS Cascade Layers
- CSS Grid
- Responsive Web Design
- Semantic HTML5
- Fluid Typography (`clamp()`)
- Accessibility-focused CSS

---

# Testing & Verification

The project was tested using different viewport sizes, zoom levels, and accessibility checks.

---

# Normal Test Cases

## Test Case 1 — Responsive Typography

### Action

Resize the browser window.

### Expected Result

- Heading sizes smoothly scale.
- Text remains readable.
- No layout breaking occurs.

---

## Test Case 2 — Responsive Grid Layout

### Action

Resize the browser from desktop width to smaller screen sizes.

### Expected Result

- Sidebar and catalog adjust correctly.
- Content does not overlap.
- Layout remains organized.

---

## Test Case 3 — Keyboard Navigation

### Action

Use the Tab key to navigate through links.

### Expected Result

- Navigation links receive visible focus indicators.
- Focus order follows the document structure.

---

# Edge Test Cases

## Test Case 4 — 200% Browser Zoom

### Action

Increase browser zoom to 200%.

### Expected Result

- Text remains readable.
- Layout remains functional.
- No content becomes inaccessible.

---

## Test Case 5 — Small Mobile Viewport

### Action

Resize browser to approximately 320px width.

### Expected Result

- Layout switches to a single-column structure.
- Sidebar moves above the catalog.
- No horizontal scrolling occurs.

---

## Test Case 6 — Large Desktop Viewport

### Action

Resize browser to a large desktop size.

### Expected Result

- Layout expands correctly.
- Structural sections remain aligned.
- Content boundaries remain intact.

---

# AI Assistance

Generative AI (ChatGPT) was used as a development assistant to help plan, explain, and review implementation decisions.

All AI-generated suggestions and code were reviewed, modified, tested, and integrated by the author.

---

# Week 02 AI Prompts

## Prompt 1

```
I am building a retro gaming curation portal in OKLCH color space. I want a dark/light mode setup. Can you output a CSS :root block with color variables utilizing oklch()? The background and text colors must pass WCAG AA contrast guidelines. Please explain the math behind the Lightness (L) levels you chose for both light and dark mode to guarantee contrast.
```

---

## Prompt 2

```
I need a CSS custom property for a main title font size that scales fluidly. It should have a minimum size of 1.75rem at 375px viewport width, and a maximum size of 3rem at 1440px viewport width. Can you write the clamp() property using a mix of rem and vw, and break down exactly how the middle viewport-width expression is calculated?
```

---

# Week 03 AI Prompts

## Prompt 1

```
I am building a Curation & Discovery Portal for my capstone project called Retro Game Discovery Portal.

Write the semantic HTML5 layout wrapper utilizing header, nav, main, aside, and footer.

Then write the CSS Grid rules needed to position these zones so the layout occupies exactly 100% of the viewport height.

Use low-specificity CSS class selectors and bind the padding, gaps, and background colors to my existing CSS variables.
```

---

## Prompt 2

```
My aside element is collapsing to zero width when the screen gets narrow, and it is causing a horizontal scrollbar.

Can you explain why this is happening within the CSS Grid formatting context and how I can set a responsive minimum width constraint on my sidebar using minmax()?
```

---

# Additional AI Assistance

AI was also used to:

- Organize the project folder structure
- Explain CSS Cascade Layers
- Generate initial spacing token systems
- Review accessibility considerations
- Verify typography scaling at 200% browser zoom
- Explain CSS Grid behavior
- Review semantic HTML structure
- Assist with responsive layout debugging

---

# Author

Denniz Garza

BAS Application Development

Week 02 Capstone Project