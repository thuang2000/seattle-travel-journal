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

### Week 04: Asymmetric Editorial Grid

Week 04 develops the primary editorial content area into an asymmetric
responsive CSS Grid.

It includes:

- Five travel content cards
- A featured hero card spanning multiple rows and columns
- A three-column desktop grid using fractional units
- Responsive two-column and one-column layouts
- `minmax()` for flexible grid tracks
- `grid-auto-flow: dense` to reduce empty grid spaces
- Week 02 spacing and OKLCH color tokens
- Responsive card content without overflow

### Week 05: CSS Architecture Refactor

Week 05 reorganizes the Week 04 stylesheet without intentionally
changing the visual design.

It includes:

- Four ordered CSS Cascade Layers
- `reset`, `base`, `layout`, and `components` architecture
- Native CSS Nesting
- Nested component child selectors
- Native `&:hover` and `&:focus-visible` states
- Nested responsive media queries
- Existing Week 02 design tokens
- Existing Week 03 structural layout
- Existing Week 04 asymmetric grid
  
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

Week 04 Prompts:
Asymmetric Grid Prompt

I have a main content area containing 5 cards. I want to build a CSS
Grid that is asymmetric. On desktop, I want a 3-column layout where
the first card is a "hero" card that spans 2 columns and 2 rows, while
the rest span 1 column. Write the CSS using fractional units and
explicit grid spans. Make sure it scales nicely down to a single
column on mobile viewports.

Grid Gap Prompt

When I shrink my viewport to tablet sizes, my asymmetric grid leaves
a large empty space in the second row because of the card span rules.
Can you analyze my grid code and show me how to use CSS Grid's
auto-placement rules, like grid-auto-flow: dense, to prevent gaps
while preserving hierarchy?


Week 05 Cascade Layer Prompt:

Here is my CSS file. I want to modernize my code by sorting these
styles into four cascade layers: reset, base, layout, and components.
Can you help me group my existing rules into these layer blocks,
explaining which layer each rule belongs to and why?

Week 05 Native Nesting Prompt:

Analyze my CSS component styles. Help me refactor this code to use
native CSS Nesting, making sure parent-child relationships are clean
and pseudo-elements/pseudo-classes are set up using the `&` operator.

### Week 06: Component-Level Container Queries

Week 06 adds component-level responsive behavior to the reusable travel
cards.

It includes:

- Named CSS container contexts
- `container-type: inline-size`
- CSS Container Queries
- Horizontal cards in wide containers
- Vertical cards in narrow containers
- The same reusable card component in the main grid and sidebar
- Container query width units (`cqw`)
- Existing Cascade Layers
- Existing native CSS Nesting
- Existing design-system variables
- Page-level media queries kept separate from component-level queries

### Week 06 Container Query Prompt

I have a reusable card element called `.card` containing an image
and some text. I want to convert this card's styling to use CSS
Container Queries instead of Media Queries. If its parent element is
wider than 450px, the card should display horizontally. If its parent
is narrower, it should stack vertically. Can you write the HTML
structure and the nested CSS using `@container`?

### Week 06 Container Layout Refactoring Prompt

In my project, I have cards in my main asymmetric grid and cards in
my sidebar aside. They currently look messy because the sidebar cards
are being squished. Can you help me set `container-type: inline-size`
on the parent elements of these card slots and show me how to refactor
the cards to self-adjust perfectly?

### Week 07: Motion & Interactions

Week 07 adds polished CSS-only motion and interaction feedback to the
editorial interface.

It includes:

- High-performance transform and opacity transitions
- Hover, active, and keyboard focus states
- Card interactions using `:focus-within`
- High-contrast `:focus-visible` rings
- A CSS-only reading progress indicator
- `animation-timeline: scroll(root)`
- Transform-based progress animation
- Reduced-motion accessibility support
- Existing Container Queries
- Existing native CSS Nesting
- Existing Cascade Layers

### Week 07 High-Performance Hover Prompt

I have a card component called `.card`. I want to design a subtle
micro-interaction when a user hovers or tabs onto it. The card should
scale up very slightly (1.02x) and drop a clean shadow. Show me how to
write this transition using only CSS transforms and opacity so that
it is hardware-accelerated. Also, include an accessible
`:focus-visible` ring.

### Week 07 Scroll-Driven Animation Prompt

I want to create a scroll-reveal animation for my layout cards using
native modern CSS scroll-driven animations. As each card enters the
viewport, it should fade from opacity 0 to 1 and slide up by 20px.
Can you write the CSS using `animation-timeline: view()` and explain
how the view-timeline bounds are determined?
