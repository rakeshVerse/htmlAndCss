## Contents

Layouts:

- Floats:
  - Float left, float right
  - Collapsing Elements: Parent of floated elements collapses (clear float -> clear: both;)
  - Box sizing: Alternate box model
  - Layout entire page using Floats
- Flexbox:
  - flex container, flex items, Main Axis, Cross Axis
  - Flex container: align-items, justify-content, gap
  - Flex items: align-self, order
  - Flex property: flex-grow, flex-shrink, flex-basis, shorthand(flex: grow, shrink, basis)
  - Build layout using flexbox
- Grids:
  - Grid container, grid items, column axis, row axis
  - Grid lines, grid track/columns, gird track/rows, grid cell (filled or empty), gutter/gap
  - Grid container properties: grid-template-columns, grid-template-rows, gap, column-gap, row-gap
  - Placing and spanning grid items: grid-column, gird-row
  - Aligning grid tracks (when containter is bigger than the grid): justify-content, align-content
  - Aligning grid items inside grid cells: justify-items, align-items
  - Aligning individual grid item: justify-self, align-self
  - Build layout using grid

Design: Typography, Images, Icons, Shadows, Border radius, Colors, Spacing

Components:

- Accordion:
  - Use `flex-direction: column` instead of `margin-bottom` to create vertical gaps between elements
  - Display grid for layouting
  - Open state trick: use a class (e.g. open) to style an element differently
- Carousel:
  - Image scaling `transform: scale(value)`
  - Removing flex item using absolute positioning
  - Centering absolutly positioned element using `transform: tanslate(X, Y)`
- Table
- Pagination

Section Components:

- Hero Section:
  - Design logic
  - Viewport height (to assing height as per current viewport): `100vh`
  - Add overlay to the image: `background-image: linear-gradient(color1, color2), url(image-path)`
  - Cover the image: `background-size: cover`
- App Layout:
  - Design logic using Grid
    - Scroll bar: `overflow: scroll`, `flex-shrink: 0` (Reset flex shrink)
