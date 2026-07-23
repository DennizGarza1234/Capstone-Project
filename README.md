# Retro Game Discovery Portal – Week 02 Design System

## Project Description

This project is the Week 02 milestone of my Capstone Project. The chosen archetype is **C: Curation & Discovery Portal**, and the final project will become a **Retro Game Discovery Portal** where users can browse and discover classic video games.

This week's assignment focuses on creating the design system that will be used throughout the rest of the project. The page demonstrates modern CSS techniques including:

- OKLCH color tokens
- Light and Dark Mode color variables
- Fluid typography using `clamp()`
- Relative spacing tokens using `rem`
- CSS Cascade Layers (`@layer`)
- Responsive layout principles

The design system serves as the foundation for future project development.

---

## Features

- Responsive typography using `clamp()`
- Accessible color palette using `oklch()`
- WCAG AA-friendly contrast between text and background
- Consistent spacing system
- CSS custom properties (design tokens)
- Cascade Layers for organized CSS architecture

---

## Project Structure

```
my-capstone-project/
│
├── index.html
│
├── week02/
│   ├── index.html
│   └── styles.css
|
├── week03/
│   ├── index.html
│   └── styles.css
│
└── README.md
```

---

## How to Run

### Option 1 (Recommended)

Open the live GitHub Pages website.

### Option 2

1. Clone the repository.

```
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

2. Open the project folder.

3. Open `index.html` in any modern web browser.

No installation or dependencies are required.

---

## Technologies Used

- HTML5
- CSS3
- CSS Custom Properties
- OKLCH Color Space
- CSS Cascade Layers
- Fluid Typography (`clamp()`)

---

## AI Assistance

Generative AI (ChatGPT) was used to assist with planning the design system and explaining modern CSS concepts. All code was reviewed, tested, and integrated by the author.

### Prompt 1

> I am building a retro gaming curation portal in OKLCH color space. I want a dark/light mode setup. Can you output a CSS :root block with color variables utilizing oklch()? The background and text colors must pass WCAG AA contrast guidelines. Please explain the math behind the Lightness (L) levels you chose for both light and dark mode to guarantee contrast.

### Prompt 2

> I need a CSS custom property for a main title font size that scales fluidly. It should have a minimum size of 1.75rem at 375px viewport width, and a maximum size of 3rem at 1440px viewport width. Can you write the clamp() property using a mix of rem and vw, and break down exactly how the middle viewport-width expression is calculated?

### Additional AI Assistance

AI was also used to:

- Organize the project folder structure
- Explain CSS Cascade Layers
- Generate the initial spacing token system
- Review accessibility considerations
- Verify that the typography remained responsive at 200% browser zoom

---

## Author

Denniz Garza

BAS Application Development

Week 02 Capstone Project
