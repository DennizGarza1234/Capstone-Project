# 🎮 Retro Game Discovery Portal

## BAS Application Development Capstone Project

**Author:** Denniz Garza

**Program:** Bachelor of Applied Science – Application Development

**Project Archetype:** C – Curation & Discovery Portal

---

# Project Overview

The **Retro Game Discovery Portal** is my capstone project for the BAS Application Development program.

The selected project archetype is:

> **Archetype C – Curation & Discovery Portal**

The goal of this project is to create a modern web application where users can browse, discover, and explore classic video games from different consoles, genres, publishers, and release years.

The project is being developed incrementally through weekly milestones. Each week's assignment builds upon the previous week's work while preserving earlier versions of the project.

Throughout the project, I am applying modern HTML5, CSS3, responsive design, accessibility, CSS Grid, CSS Custom Properties, OKLCH colors, fluid typography, Cascade Layers, and native CSS nesting to create a professional-quality web application.

---

# Project Archetype

## Archetype C – Curation & Discovery Portal

The Curation & Discovery Portal archetype is designed for applications that organize and present collections of content for users to browse and discover.

For this project, the concept is a retro gaming discovery platform.

The portal is designed around the following structural elements:

- Search interface
- Filter sidebar
- Responsive content gallery
- Featured content
- Supporting content cards
- Responsive navigation
- Future comparison and discovery functionality

The project can eventually be expanded into a fully interactive retro game catalog.

---

# Weekly Milestones

## Week 02 – Design System Foundation

Week 02 focused on creating the reusable design system that powers the entire application.

Implemented features include:

- OKLCH color palette
- Light and Dark Mode color variables
- Fluid typography using `clamp()`
- Relative spacing tokens using `rem`
- CSS Custom Properties
- CSS Cascade Layers
- Responsive design principles
- WCAG AA contrast considerations

The design system establishes reusable colors, typography, spacing, and sizing rules that can be used throughout the rest of the project.

### Week 02 Goals

The primary goals were to:

1. Establish a consistent visual language.
2. Create reusable CSS design tokens.
3. Use perceptual OKLCH colors.
4. Create fluid typography.
5. Establish a reusable spacing scale.
6. Prepare the project for future responsive layouts.

---

# Week 03 – Structural Frames & Semantic Navigation

Week 03 expanded the Week 02 design system into the structural framework of the application.

The Retro Game Discovery Portal now includes:

- Semantic HTML5 layout
- Header banner
- Primary navigation
- Search interface
- Left-side filter sidebar
- Main catalog content area
- Footer
- Responsive CSS Grid layout

The goal of Week 03 was to establish the complete page architecture before introducing the asymmetric content grid.

### Semantic Structure

The page uses semantic HTML elements including:

- `<header>`
- `<nav>`
- `<main>`
- `<aside>`
- `<section>`
- `<article>`
- `<footer>`

This provides a meaningful document structure and improves accessibility and maintainability.

---

# Week 04 – Responsive Asymmetric Grid

Week 04 transformed the main content area into a responsive asymmetric card layout.

The goal was to move beyond a basic uniform card grid and create a visual hierarchy using CSS Grid.

The Week 04 implementation introduced:

- Asymmetric CSS Grid
- Featured Hero Card
- Five content cards
- Grid auto-placement
- `grid-auto-flow: dense`
- `minmax()`
- Fractional `fr` units
- Responsive card sizing
- Responsive card hierarchy
- Dynamic visual balance

The featured game card spans multiple columns and rows while the supporting cards fill the remaining available grid space.

---

# Week 05 – CSS Architecture Refactor

Week 05 focuses on refactoring the existing Week 04 stylesheet without changing the appearance of the application.

The purpose of this milestone is to improve the maintainability and organization of the CSS architecture.

The Week 05 stylesheet introduces:

- Native CSS Cascade Layers
- Four organized styling layers
- Native CSS Nesting
- Parent selector `&`
- Nested pseudo-classes
- Improved component organization
- Reduced selector clutter
- Controlled style precedence

The required Cascade Layer order is:

```css
@layer reset, base, layout, components;
```

The refactor is intended to change the underlying CSS architecture while preserving the existing visual design.

---

# Week 05 Cascade Layer Architecture

The stylesheet is divided into four distinct layers.

## 1. Reset Layer

The `reset` layer establishes the baseline browser styling.

It contains rules such as:

- Universal `box-sizing`
- Margin resets
- Image defaults
- Form control inheritance
- Basic structural resets

Example:

```css
@layer reset {

    *,
    *::before,
    *::after {
        box-sizing: border-box;
    }

    body {
        margin: 0;
    }

}
```

---

## 2. Base Layer

The `base` layer contains global design tokens and default HTML element styles.

This layer includes:

- CSS Custom Properties
- OKLCH color variables
- Typography
- Spacing variables
- Global body styles
- Heading styles
- Paragraph styles
- Link styles
- Button defaults
- Accessibility utility classes

Example:

```css
@layer base {

    :root {
        --space-sm: 1rem;
        --space-md: 2rem;
        --space-lg: 4rem;
    }

}
```

---

## 3. Layout Layer

The `layout` layer contains high-level page structure.

It includes:

- Header
- Navigation
- Search area
- Page layout
- Sidebar
- Main content area
- CSS Grid
- Footer
- Responsive layout rules

Example:

```css
@layer layout {

    .page-layout {
        display: grid;
        grid-template-columns:
            minmax(220px, 260px)
            minmax(0, 1fr);
    }

}
```

---

## 4. Components Layer

The `components` layer contains reusable UI components.

It includes:

- Game cards
- Hero card
- Buttons
- Badges
- Game detail lists
- Hover states
- Focus states

Because `components` is declared after the other layers, its styles have higher cascade precedence than the earlier layers.

---

# Native CSS Nesting

Week 05 introduces native CSS nesting to make component relationships easier to understand and maintain.

Instead of writing separate selectors such as:

```css
.card h3 {
    ...
}

.card button {
    ...
}

.card button:hover {
    ...
}
```

the styles are organized inside the parent component:

```css
.card {

    h3 {
        ...
    }

    button {

        &:hover {
            ...
        }

    }

}
```

The parent selector operator `&` is used for pseudo-classes such as:

```css
&:hover
```

and:

```css
&:focus-visible
```

This allows component-related styles to remain grouped together.

---

# Week 05 Features

The current project includes:

- Responsive asymmetric CSS Grid
- Featured hero card
- Five content cards
- Search interface
- Filter sidebar
- Responsive navigation
- Fluid typography
- `clamp()`
- `minmax()`
- Fractional `fr` units
- `grid-auto-flow: dense`
- OKLCH color system
- CSS Custom Properties
- CSS Cascade Layers
- Native CSS Nesting
- Responsive design
- Semantic HTML5
- Keyboard focus states
- Accessibility-focused styling

---

# Project Structure

The project uses a progressive archive structure so that each week's work is preserved.

```text
my-capstone-project/
│
├── index.html
├── README.md
│
├── week02/
│   ├── index.html
│   └── styles.css
│
├── week03/
│   ├── index.html
│   └── styles.css
│
├── week04/
│   ├── index.html
│   └── styles.css
│
└── week05/
    ├── index.html
    └── styles.css
```

Each milestone has its own directory so previous work is not overwritten.

---

# Application Layout

## Desktop Layout

```text
-------------------------------------------------------------
|                        HEADER                             |
|        Logo • Navigation • Search                        |
-------------------------------------------------------------
|            |                                              |
|  FILTER    |        FEATURED HERO CARD                    |
|  SIDEBAR   |        (Spans 2 Columns / 2 Rows)            |
|            |---------------------------|------------------|
|            |   New Discoveries         | Highest Rated    |
|            |---------------------------|------------------|
|            | Recently Played           | Community Picks  |
-------------------------------------------------------------
|                        FOOTER                             |
-------------------------------------------------------------
```

---

## Tablet Layout

```text
-------------------------------------
|             HEADER                |
-------------------------------------
|            FILTERS                |
-------------------------------------
|         FEATURED GAME             |
-------------------------------------
|      NEW DISCOVERIES              |
-------------------------------------
|       HIGHEST RATED               |
-------------------------------------
|     RECENTLY PLAYED               |
-------------------------------------
|    COMMUNITY FAVORITES            |
-------------------------------------
|            FOOTER                 |
-------------------------------------
```

---

## Mobile Layout

```text
------------------------
|       HEADER         |
------------------------
|      SEARCH          |
------------------------
|      FILTERS         |
------------------------
|    FEATURED GAME     |
------------------------
|      CARD 2          |
------------------------
|      CARD 3          |
------------------------
|      CARD 4          |
------------------------
|      CARD 5          |
------------------------
|      FOOTER          |
------------------------
```

The layout automatically adapts to different screen sizes using CSS Grid, responsive media queries, and fluid sizing techniques.

---

# Semantic HTML Structure

The project uses semantic HTML5 landmarks to improve accessibility, readability, and maintainability.

| Element | Purpose |
|---------|---------|
| `<header>` | Branding and application header |
| `<nav>` | Primary navigation |
| `<main>` | Main game discovery content |
| `<aside>` | Search and filtering controls |
| `<section>` | Organized content groups |
| `<article>` | Individual game/content cards |
| `<footer>` | Copyright and project information |

Using semantic elements provides a meaningful document structure and supports assistive technologies.

---

# CSS Layout System

The project uses several modern CSS layout techniques.

## CSS Grid

CSS Grid is used for both the overall page structure and the asymmetric game card layout.

Example:

```css
.grid-container {
    display: grid;

    grid-template-columns:
        repeat(
            auto-fit,
            minmax(260px, 1fr)
        );

    grid-auto-flow: dense;

    gap: var(--space-md);
}
```

---

# Asymmetric Hero Card

The featured game card establishes visual hierarchy by spanning multiple grid tracks.

```css
.hero-card {
    grid-column: span 2;
    grid-row: span 2;
}
```

This allows the featured game to visually dominate the content area while the other cards occupy smaller spaces.

On smaller viewports, the hero card returns to a normal single-column layout.

---

# Grid Auto Placement

The project uses:

```css
grid-auto-flow: dense;
```

This allows CSS Grid to attempt to fill available spaces more efficiently when cards have different sizes.

The purpose is to reduce unnecessary empty areas while maintaining the visual hierarchy created by the featured card.

---

# Design Tokens

The project uses CSS Custom Properties to create a reusable design token system.

Examples include:

```css
--space-xs
--space-sm
--space-md
--space-lg
```

Color tokens include:

```css
--color-primary
--color-secondary
--color-bg
--color-surface
--color-text
--color-border
```

Typography tokens include:

```css
--size-base
--size-heading-md
--size-heading-lg
```

Using design tokens keeps the visual system consistent and makes future changes easier to manage.

---

# Fluid Typography

The project uses the CSS `clamp()` function to create responsive typography.

Example:

```css
--size-heading-lg:
    clamp(
        1.75rem,
        1.3rem + 2vw,
        3rem
    );
```

This allows the heading size to scale between a minimum and maximum value while responding to the viewport.

The use of relative units such as `rem` also helps preserve accessibility when browser zoom is increased.

---

# OKLCH Color System

The project uses the OKLCH color space for its design tokens.

Example:

```css
--color-primary:
    oklch(64% 0.20 260);
```

OKLCH provides a perceptually oriented way to define colors using:

- Lightness
- Chroma
- Hue

This allows the color system to be adjusted in a more predictable way than traditional RGB or hexadecimal values.

---

# Technologies Used

- HTML5
- CSS3
- CSS Grid
- Flexbox
- CSS Custom Properties
- CSS Cascade Layers
- Native CSS Nesting
- OKLCH Color Space
- Responsive Web Design
- Semantic HTML5
- Fluid Typography
- `clamp()`
- `minmax()`
- `fr` units
- Git
- GitHub
- GitHub Pages
- Browser Developer Tools

---

# How to Run

## Option 1 – GitHub Pages

The recommended method is to visit the deployed GitHub Pages version of the project.

Add the live project URL here:

```text
YOUR GITHUB PAGES URL
```

---

## Option 2 – Clone the Repository

Clone the repository using Git:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Navigate into the project:

```bash
cd YOUR_REPOSITORY
```

Open the desired milestone in a modern web browser.

For example:

```text
week02/index.html
```

```text
week03/index.html
```

```text
week04/index.html
```

```text
week05/index.html
```

No package installation, frameworks, or external dependencies are required.

---

# Testing & Verification

The Retro Game Discovery Portal was tested across different viewport sizes and browser zoom levels to verify responsive behavior, layout integrity, accessibility, and CSS architecture.

Testing included:

- Responsive layout behavior
- CSS Grid functionality
- Asymmetric card layout
- Fluid typography
- Consistent spacing
- Keyboard navigation
- Responsive navigation
- Hero card behavior
- CSS Grid auto-placement
- Mobile responsiveness
- Browser zoom compatibility
- Cascade Layer organization
- Native CSS Nesting syntax

---

# Week 04 Test Cases

## Normal Test Case 1 – Responsive Typography

### Action

Resize the browser window from desktop width to tablet and mobile sizes.

### Expected Result

- Headings resize smoothly using `clamp()`.
- Paragraph text remains readable.
- No overlapping or clipped text occurs.

### Result

✅ Passed

---

## Normal Test Case 2 – Asymmetric Grid Layout

### Action

Load the page on a desktop-sized viewport.

### Expected Result

- The featured game card spans two columns and two rows.
- Supporting cards automatically fill the remaining grid.
- Layout maintains visual hierarchy.

### Result

✅ Passed

---

## Normal Test Case 3 – Responsive Navigation & Sidebar

### Action

Navigate through the page using the navigation menu and filter sidebar.

### Expected Result

- Navigation remains accessible.
- Sidebar aligns correctly beside the content on larger screens.
- Layout adapts correctly as the viewport changes.

### Result

✅ Passed

---

# Week 04 Edge Test Cases

## Edge Test Case 1 – Browser Zoom (200%)

### Action

Increase browser zoom to 200%.

### Expected Result

- Typography scales appropriately.
- Cards remain readable.
- No overlapping or inaccessible content occurs.

### Result

✅ Passed

---

## Edge Test Case 2 – Mobile Viewport (320px)

### Action

Resize the browser to approximately 320px wide.

### Expected Result

- Cards stack into a single column.
- Sidebar moves above the catalog.
- No horizontal scrolling occurs.
- Hero card returns to a standard card size.

### Result

✅ Passed

---

## Edge Test Case 3 – Grid Auto Placement

### Action

Resize the browser through several widths between desktop and tablet.

### Expected Result

- CSS Grid automatically reorganizes cards.
- `grid-auto-flow: dense` minimizes unnecessary empty spaces.
- Cards remain aligned without unexpected gaps.

### Result

✅ Passed

---

# Week 05 Verification

Week 05 introduces additional tests specifically for the CSS architecture refactor.

---

## Week 05 Test 1 – Visual Continuity

### Action

Open the Week 04 and Week 05 versions of the application.

### Expected Result

The Week 05 version should maintain the same overall visual appearance as Week 04.

The CSS architecture should change without breaking the user-facing design.

### Result

✅ Passed

---

## Week 05 Test 2 – Cascade Layer Audit

### Action

Open browser Developer Tools and inspect an element inside a card.

Navigate to the Styles panel.

### Expected Result

The card's styles should appear under:

```css
@layer components
```

The stylesheet should contain the required layer order:

```css
@layer reset, base, layout, components;
```

### Result

✅ Passed

---

## Week 05 Test 3 – Native CSS Nesting

### Action

Inspect the Week 05 stylesheet.

### Expected Result

Component child styles and pseudo-classes are nested directly inside their parent components.

For example:

```css
.card {

    button {

        &:hover {
            ...
        }

    }

}
```

The implementation should use native CSS nesting rather than Sass or another preprocessor.

### Result

✅ Passed

---

# Accessibility

Accessibility has been considered throughout the development process.

The project includes:

- Semantic HTML5 landmarks
- Keyboard-accessible navigation
- Visible focus states
- Responsive typography
- Relative `rem` sizing
- High-contrast color considerations
- Consistent heading hierarchy
- Readable line lengths
- Responsive layouts
- Form labels
- Accessible structural organization

The project was also tested at 200% browser zoom to verify that content remains usable.

---

# AI Assistance

Generative AI, specifically **ChatGPT**, was used as a development assistant throughout the project.

AI was used to:

- Explain CSS concepts
- Generate draft CSS implementations
- Review CSS architecture
- Explain OKLCH color systems
- Explain fluid typography
- Analyze CSS Grid behavior
- Assist with responsive design
- Review semantic HTML
- Refactor CSS into Cascade Layers
- Explain native CSS nesting
- Assist with testing strategies
- Help create project documentation
- Help prepare the project demonstration script

All AI-generated suggestions and code were reviewed, modified, tested, and integrated by the author.

AI was used as a co-piloting and learning tool rather than as a replacement for manually reviewing and testing the implementation.

---

# Week 02 AI Prompts

## Prompt 1 – Designing the Palette

```text
I am building a retro gaming curation portal in OKLCH color space. I want a dark/light mode setup. Can you output a CSS :root block with color variables utilizing oklch()? The background and text colors must pass WCAG AA contrast guidelines. Please explain the math behind the Lightness (L) levels you chose for both light and dark mode to guarantee contrast.
```

---

## Prompt 2 – Calculating Fluid Scales

```text
I need a CSS custom property for a main title font size that scales fluidly. It should have a minimum size of 1.75rem at 375px viewport width, and a maximum size of 3rem at 1440px viewport width. Can you write the clamp() property using a mix of rem and vw, and break down exactly how the middle viewport-width expression is calculated?
```

---

# Week 03 AI Prompts

## Prompt 1 – Semantic Layout

```text
I am building a Curation & Discovery Portal for my capstone project called Retro Game Discovery Portal.

Write the semantic HTML5 layout wrapper utilizing header, nav, main, aside, and footer.

Then write the CSS Grid rules needed to position these zones so the layout occupies exactly 100% of the viewport height.

Use low-specificity CSS class selectors and bind the padding, gaps, and background colors to my existing CSS variables.
```

---

## Prompt 2 – Responsive Sidebar

```text
My aside element is collapsing to zero width when the screen gets narrow, and it is causing a horizontal scrollbar.

Can you explain why this is happening within the CSS Grid formatting context and how I can set a responsive minimum width constraint on my sidebar using minmax()?
```

---

# Week 04 AI Prompts

## Prompt 1 – Designing an Asymmetric Grid

```text
I have a main content area containing 5 cards. I want to build a CSS Grid that is asymmetric. On desktop, I want a 3-column layout where the first card is a hero card that spans 2 columns and 2 rows, while the rest span 1 column. Write the CSS using fractional units (fr) and grid-template-areas (or explicit grid spans). Make sure it scales nicely down to a single column on mobile viewports.
```

---

## Prompt 2 – Preventing Grid Gaps

```text
When I shrink my viewport to tablet sizes, my asymmetric grid leaves a large empty space because of the hero card span rules. Analyze my CSS Grid layout and show me how to use CSS Grid's auto-placement rules, like grid-auto-flow: dense, to prevent gaps while preserving the visual hierarchy.
```

---

# Week 05 AI Prompts

## Prompt 1 – Refactoring CSS to Cascade Layers

```text
Here is my CSS file [Paste CSS]. I want to modernize my code by sorting these styles into four cascade layers: reset, base, layout, and components. Can you help me group my existing rules into these layer blocks, explaining which layer each rule belongs to and why?
```

---

## Prompt 2 – Refactoring to Native CSS Nesting

```text
Analyze my CSS component styles [Paste Card/Grid CSS]. Help me refactor this code to use native CSS Nesting, making sure parent-child relationships are clean and pseudo-elements/pseudo-classes are set up using the '&' operator.
```

---

# Additional AI Assistance

AI was also used to:

- Plan the progressive project folder structure
- Explain CSS Cascade Layers
- Explain cascade precedence
- Create reusable design tokens
- Explain OKLCH color values
- Review WCAG accessibility considerations
- Explain fluid typography calculations
- Explain CSS Grid behavior
- Review semantic HTML structure
- Troubleshoot responsive layouts
- Explain `minmax()`
- Explain fractional `fr` units
- Explain `grid-auto-flow: dense`
- Refactor component styles using native CSS nesting
- Organize CSS into architectural layers
- Review spacing consistency
- Generate project documentation
- Assist with testing procedures
- Prepare the project demonstration script

---

# Future Enhancements

Future milestones may expand the Retro Game Discovery Portal with functional application behavior.

Potential enhancements include:

- Functional game search
- Platform filtering
- Genre filtering
- Release-year filtering
- Interactive game detail pages
- Game comparison functionality
- User ratings
- Favorite games
- Personal game collections
- Recently viewed games
- JavaScript-powered filtering
- Local storage support
- API-based game data
- Dynamic game cards
- Animated UI interactions
- Expanded accessibility features
- Dark/light mode controls

---

# Progressive Development Philosophy

The project uses a progressive archive architecture.

Rather than overwriting previous work, each week's implementation is preserved in its own directory.

For example:

```text
week02/
week03/
week04/
week05/
```

This approach makes it possible to compare milestones and demonstrate how the application evolved over time.

It also provides a historical record of the development process and allows individual milestones to be reviewed independently.

---

# Development Principles

Throughout the project, the following principles are being emphasized:

### Reusability

CSS Custom Properties and design tokens reduce duplicated values.

### Accessibility

Semantic HTML, keyboard navigation, responsive typography, and contrast considerations are incorporated throughout development.

### Responsiveness

The layout adapts to desktop, tablet, and mobile viewports.

### Maintainability

Cascade Layers and native CSS nesting organize styles into predictable sections.

### Progressive Enhancement

Each milestone builds upon the previous version rather than replacing it.

### Modern CSS

The project uses modern CSS features including:

- OKLCH
- `clamp()`
- `minmax()`
- CSS Grid
- Cascade Layers
- Native CSS Nesting
- Custom Properties

---

# Known Limitations

The current version is primarily a front-end capstone implementation.

Some features are currently visual placeholders rather than fully functional application features.

For example:

- Search does not yet perform database/API searches.
- Filter controls are not yet connected to game data.
- Navigation links are currently structural.
- Game cards use demonstration content.
- User accounts have not yet been implemented.
- Game comparison functionality is planned for a future milestone.

These limitations provide opportunities for future development as the capstone progresses.

---

# Deployment

The project is designed to be deployed using **GitHub Pages**.

The progressive folder structure allows individual milestones to remain accessible under the same repository.

The root `index.html` serves as the project landing page and can link to each weekly milestone.

Example:

```text
/
├── index.html
├── week02/
├── week03/
├── week04/
└── week05/
```

---

# Submission Checklist

## Project Structure

- [x] Root `index.html`
- [x] `README.md`
- [x] Week 02 folder
- [x] Week 03 folder
- [x] Week 04 folder
- [x] Week 05 folder

## Week 02

- [x] OKLCH colors
- [x] CSS Custom Properties
- [x] Fluid typography
- [x] `clamp()`
- [x] Relative spacing variables
- [x] Responsive design foundation

## Week 03

- [x] Semantic HTML5
- [x] Header
- [x] Navigation
- [x] Sidebar
- [x] Main content
- [x] Footer
- [x] CSS Grid layout

## Week 04

- [x] At least five cards
- [x] Asymmetric grid
- [x] Hero card
- [x] Multiple rows/columns
- [x] `minmax()`
- [x] `fr` units
- [x] `grid-auto-flow: dense`
- [x] Responsive mobile layout

## Week 05

- [x] CSS Cascade Layers
- [x] `reset` layer
- [x] `base` layer
- [x] `layout` layer
- [x] `components` layer
- [x] Native CSS Nesting
- [x] Parent selector `&`
- [x] Nested hover states
- [x] Nested focus states
- [x] Visual continuity with Week 04

## Verification

- [x] Responsive testing
- [x] 200% browser zoom test
- [x] Mobile viewport test
- [x] CSS Grid inspection
- [x] Cascade Layer inspection
- [x] Native nesting verification
- [x] Keyboard navigation testing

---

# License

This project was created for educational purposes as part of the **BAS Application Development Capstone**.

---

# Acknowledgments

Special thanks to:

- My course instructor
- BAS Application Development program
- MDN Web Docs
- W3C CSS Specifications
- GitHub Pages
- OpenAI ChatGPT for development assistance and technical explanations

---

# Author

**Denniz Garza**

Bachelor of Applied Science – Application Development

**Capstone Project**

**Archetype C – Curation & Discovery Portal**

🎮 **Retro Game Discovery Portal**