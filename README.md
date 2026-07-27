# The Cascadia Journal

The Cascadia Journal is a responsive editorial travel publication
featuring destinations, experiences, and travel journals from Seattle
and the surrounding Pacific Northwest.

This project is being developed incrementally as a seven-week web
development capstone. Each weekly milestone is preserved in a separate
subdirectory so that the project's development can be reviewed over time.

## Project Archetype

Archetype B: Modern Editorial / Tech Publication

Planned structural elements include:

- Dynamic editorial header
- Asymmetric story grid
- Reading-progress indicator
- Fluid long-form typography
- Responsive travel article layouts
- Light and dark color modes

## Current Milestone

### Week 02: Design System Token Page

The Week 02 page establishes the visual design system for the project.

It includes:

- An OKLCH color palette
- Light and dark mode color tokens
- WCAG AA-conscious text and background contrast
- Fluid typography using `clamp()`
- A reusable spacing scale using `rem`
- CSS custom properties
- CSS cascade layers

## AI Tools
ChatGPT was utilized to assist with this project.

## AI Prompts
I am building a modern editorial travel publication about travel
journals near Seattle in OKLCH color space. I want a warm editorial
dark/light mode setup. Can you output a CSS :root block with color
variables utilizing oklch()? The background and text colors must
pass WCAG AA contrast guidelines. Please explain the math behind the
Lightness (L) levels you chose for both light and dark mode to
guarantee contrast.

I need a CSS custom property for a main title font size that scales
fluidly. It should have a minimum size of 1.75rem at a 375px
viewport width, and a maximum size of 3rem at a 1440px viewport
width. Can you write the clamp() property using a mix of rem and
vw, and break down exactly how the middle viewport-width expression
is calculated?

## Repository Structure

```text
seattle-travel-journal/
├── index.html
├── README.md
└── week02/
    ├── index.html
    └── styles.css
