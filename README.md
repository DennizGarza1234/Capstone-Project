# 🎮 Retro Game Discovery Portal

## BAS Application Development Capstone Project

**Author:** Denniz Garza

---

# Project Overview

The **Retro Game Discovery Portal** is my capstone project for the BAS Application Development program. The selected project archetype is:

**Archetype C – Curation & Discovery Portal**

The goal of this project is to create a modern web application where users can browse, discover, and explore classic video games from different consoles, genres, publishers, and release years.

The project is being developed incrementally through weekly milestones. Each week's assignment builds upon the previous week's work, preserving earlier versions while introducing new concepts and technologies.

Throughout the project I am applying modern HTML5, CSS3, responsive design, accessibility, and contemporary layout techniques to produce a professional-quality web application.

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
- WCAG AA color contrast considerations

The design system provides reusable colors, typography, spacing, and styling rules that are used throughout every future milestone.

---

## Week 03 – Structural Frames & Semantic Navigation

Week 03 expanded the design system into the structural framework of the application.

The Retro Game Discovery Portal now includes:

- Semantic HTML5 layout
- Header banner
- Primary navigation
- Left-side filter sidebar
- Main catalog content area
- Footer
- Responsive CSS Grid layout

The goal of Week 03 was to establish the complete page architecture before adding application content.

---

## Week 04 – Responsive Asymmetric Grid

Week 04 transforms the empty catalog area into a responsive editorial-style layout.

This milestone introduces:

- Asymmetric CSS Grid
- Featured Hero Card
- Five responsive content cards
- Grid auto-placement
- Modern responsive layout techniques
- Responsive card hierarchy
- Dynamic visual balance

The featured game card spans multiple columns and rows while supporting cards automatically fill the remaining space using CSS Grid.

---

# Week 04 Features

- Responsive asymmetric CSS Grid
- Hero card spanning multiple columns and rows
- Five content cards
- Search header
- Filter sidebar
- Responsive navigation
- Fluid typography using `clamp()`
- CSS Grid auto-placement
- `grid-auto-flow: dense`
- `minmax()` responsive columns
- Fractional (`fr`) grid units
- OKLCH color system
- CSS Cascade Layers
- Design Token architecture

---

# Project Structure

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
└── week04/
    ├── index.html
    └── styles.css
```

---

# Application Layout

## Desktop Layout

```
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

```
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

```
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

The project uses semantic HTML5 landmarks to improve accessibility and maintainability.

| Element | Purpose |
|---------|---------|
| `<header>` | Branding and application header |
| `<nav>` | Primary navigation |
| `<main>` | Main game discovery content |
| `<aside>` | Search filters |
| `<section>` | Organized content groups |
| `<article>` | Individual game cards |
| `<footer>` | Copyright and project information |

Using semantic elements improves accessibility, SEO, readability, and long-term maintainability.

---

# CSS Layout System

The project uses several modern CSS layout techniques.

## CSS Grid

Used for:

- Overall page layout
- Asymmetric game card layout
- Responsive content organization

Example:

```css
.grid-container{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
    grid-auto-flow:dense;
    gap:var(--space-md);
}
```

---

## Hero Card

The featured game card establishes visual hierarchy.

```css
.hero-card{
    grid-column:span 2;
    grid-row:span 2;
}
```

---

## Design Tokens

All spacing, colors, typography, and sizing are powered using reusable CSS Custom Properties.

Examples include:

- `--space-sm`
- `--space-md`
- `--space-lg`
- `--color-primary`
- `--color-surface`
- `--color-text`

This ensures visual consistency throughout the application.

---

# Technologies Used

- HTML5
- CSS3
- CSS Grid
- Flexbox
- CSS Custom Properties
- CSS Cascade Layers
- OKLCH Color Space
- Responsive Web Design
- Semantic HTML5
- Fluid Typography (`clamp()`)
- Git
- GitHub
- GitHub Pages

---

# How to Run

## Option 1 (Recommended)

Visit the deployed GitHub Pages website.

## Option 2

Clone the repository.

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Open the project folder.

Open one of the following files in a modern web browser:

```
week02/index.html
```

```
week03/index.html
```

```
week04/index.html
```

No installation, frameworks, or dependencies are required.

---

# Testing & Verification

The Retro Game Discovery Portal was tested across multiple browsers, viewport sizes, and zoom levels to ensure a responsive and accessible user experience.

Testing focused on:

- Responsive layout behavior
- CSS Grid functionality
- Fluid typography
- Consistent spacing
- Keyboard accessibility
- Responsive navigation
- Hero card behavior
- CSS Grid auto-placement
- Mobile responsiveness
- Browser zoom compatibility

---

# Normal Test Cases

## Test Case 1 – Responsive Typography

### Action

Resize the browser window from desktop width to tablet and mobile sizes.

### Expected Result

- Headings resize smoothly using `clamp()`.
- Paragraph text remains readable.
- No overlapping or clipped text occurs.

### Result

✅ Passed

---

## Test Case 2 – Asymmetric Grid Layout

### Action

Load the page on a desktop-sized viewport.

### Expected Result

- The featured game card spans two columns and two rows.
- Supporting cards automatically fill the remaining grid.
- Layout maintains visual hierarchy.

### Result

✅ Passed

---

## Test Case 3 – Responsive Navigation & Sidebar

### Action

Navigate through the page using the navigation menu and filter sidebar.

### Expected Result

- Navigation remains accessible.
- Sidebar aligns correctly beside the content on larger screens.
- Layout adapts correctly as the viewport changes.

### Result

✅ Passed

---

# Edge Test Cases

## Test Case 4 – Browser Zoom (200%)

### Action

Increase browser zoom to 200%.

### Expected Result

- Typography scales appropriately.
- Cards remain readable.
- No overlapping or inaccessible content.

### Result

✅ Passed

---

## Test Case 5 – Mobile Viewport (320px)

### Action

Resize the browser to approximately 320 pixels wide.

### Expected Result

- Cards stack into a single column.
- Sidebar moves above the content.
- No horizontal scrolling.
- Hero card returns to a standard card size.

### Result

✅ Passed

---

## Test Case 6 – Grid Auto Placement

### Action

Resize the browser through several widths between desktop and tablet.

### Expected Result

- CSS Grid automatically reorganizes cards.
- `grid-auto-flow: dense` minimizes empty spaces.
- Cards remain aligned without awkward gaps.

### Result

✅ Passed

---

# Accessibility

Accessibility was considered throughout development by implementing:

- Semantic HTML5 landmarks
- Responsive typography using `clamp()`
- Relative sizing with `rem`
- High-contrast OKLCH color palette
- Keyboard-accessible navigation
- Responsive layouts
- Readable spacing and line height
- Consistent heading hierarchy

---

# AI Assistance

Generative AI (ChatGPT) was used as a development assistant to help explain concepts, review code, and generate draft implementations.

All AI-generated code and recommendations were reviewed, modified, tested, and integrated by the author before submission.

---

# Week 02 AI Prompts

## Prompt 1

```text
I am building a retro gaming curation portal in OKLCH color space. I want a dark/light mode setup. Can you output a CSS :root block with color variables utilizing oklch()? The background and text colors must pass WCAG AA contrast guidelines. Please explain the math behind the Lightness (L) levels you chose for both light and dark mode to guarantee contrast.
```

---

## Prompt 2

```text
I need a CSS custom property for a main title font size that scales fluidly. It should have a minimum size of 1.75rem at 375px viewport width, and a maximum size of 3rem at 1440px viewport width. Can you write the clamp() property using a mix of rem and vw, and break down exactly how the middle viewport-width expression is calculated?
```

---

# Week 03 AI Prompts

## Prompt 1

```text
I am building a Curation & Discovery Portal for my capstone project called Retro Game Discovery Portal.

Write the semantic HTML5 layout wrapper utilizing header, nav, main, aside, and footer.

Then write the CSS Grid rules needed to position these zones so the layout occupies exactly 100% of the viewport height.

Use low-specificity CSS class selectors and bind the padding, gaps, and background colors to my existing CSS variables.
```

---

## Prompt 2

```text
My aside element is collapsing to zero width when the screen gets narrow, and it is causing a horizontal scrollbar.

Can you explain why this is happening within the CSS Grid formatting context and how I can set a responsive minimum width constraint on my sidebar using minmax()?
```

---

# Week 04 AI Prompts

## Prompt 1

```text
I have a main content area containing 5 cards. I want to build a CSS Grid that is asymmetric. On desktop, I want a 3-column layout where the first card is a hero card that spans 2 columns and 2 rows, while the rest span 1 column. Write the CSS using fractional units (fr) and grid-template-areas (or explicit grid spans). Make sure it scales nicely down to a single column on mobile viewports.
```

---

## Prompt 2

```text
When I shrink my viewport to tablet sizes, my asymmetric grid leaves a large empty space because of the hero card span rules. Analyze my CSS Grid layout and show me how to use CSS Grid's auto-placement rules, like grid-auto-flow: dense, to prevent gaps while preserving the visual hierarchy.
```

---

# Additional AI Assistance

AI was also used to:

- Plan the project folder structure
- Explain CSS Cascade Layers
- Create reusable design tokens
- Explain OKLCH color values
- Review WCAG accessibility considerations
- Explain fluid typography calculations
- Explain CSS Grid concepts
- Review semantic HTML structure
- Troubleshoot responsive layouts
- Suggest responsive improvements
- Review spacing consistency
- Generate documentation
- Assist with testing procedures
- Help prepare the project demonstration script

---

# Future Enhancements

Planned features for future milestones include:

- Functional search
- Platform filtering
- Genre filtering
- Interactive game detail pages
- User ratings
- Favorite games
- Collection management
- Recently viewed games
- JavaScript-powered filtering
- Local storage support
- Animated UI interactions
- Expanded accessibility features

---

# License

This project was created for educational purposes as part of the BAS Application Development Capstone course.

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

Capstone Project

Archetype C – Curation & Discovery Portal

Retro Game Discovery Portal