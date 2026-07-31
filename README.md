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

### Week 03: Structural Layout Frame

Week 03 establishes the primary editorial page skeleton without adding
final article content.

It includes:

- A sticky semantic `<header>`
- Primary navigation using `<nav>`
- A centered editorial `<main>` area
- A secondary `<aside>` side rail
- A semantic `<footer>`
- A full-height page frame using CSS Grid
- A responsive sidebar using `minmax()`
- Mobile, tablet, and desktop layouts
- High-contrast keyboard focus indicators
- Week 02 design tokens reused through CSS variables
  
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

Week 03 Prompts:
Prompt 1 (Drafting Semantic Layout Scaffolding): "I am building a [Insert Chosen Archetype, e.g., Developer Workspace Dashboard] for my capstone project. Write the semantic HTML5 layout wrapper utilizing , , , , and . Then, write the CSS Grid rules needed to position these zones so the layout occupies exactly 100% of the viewport height. Use low-specificity CSS class selectors and bind the padding, gaps, and background colors to my existing CSS variables."

Prompt 2 (Grid Frame Debugging): [Paste your HTML & CSS draft] "My aside element is collapsing to zero width when the screen gets narrow, and it is causing a horizontal scrollbar. Can you explain why this is happening within the CSS Grid formatting context and how I can set a responsive minimum width constraint on my sidebar using minmax()?"

