## Contents

Layouts

- Floats:
  - Float left, float right
  - Collapsing Elements: Parent of floated elements collapses (clear float -> clear: both;)
  - Box sizing: Alternate box model
  - Layout entire page using Floats
- Flexbox:
  - Flex container, flex items, Main Axis, Cross Axis
  - Flex container for all items: align-items, justify-content, gap
  - Flex items for individual items: align-self, order
  - Flex property: flex-grow, flex-shrink, flex-basis, shorthand(flex: grow, shrink, basis). [These properties specifies columns width and its content behaviour. `grow` lets the column grow, `shrink` shrinks the content for smaller devices, `basis` is similar to width which defaults to `auto`. For equal width columns set `basis` to 0 or 100%]. To apply these properties to each item use `flex-container > * {}` selector.
  - Change flex direction: flex-direction defaults to `row`
  - Build layout using flexbox
- Grids:
  - Grid container, grid items, column axis, row axis
  - Grid lines, grid track/columns, gird track/rows, grid cell (filled or empty), gutter/gap
  - Grid container properties: grid-template-columns, grid-template-rows, gap, column-gap, row-gap. After specifying `grid-template-columns` we don't have to specify `grid-template-rows`
  - Placing and spanning grid items: grid-column, gird-row. For spanning across columns: `grid-coloums: span start/end`
  - Aligning grid tracks (when containter is bigger than the grid): justify-content, align-content
  - Aligning grid items inside grid cells: justify-items, align-items
  - Aligning individual grid item: justify-self, align-self
  - Use utility classes where ever possible like `.grid-cols-2, .grid-cols-span-4, etc.`
  - Build layout using grid

Design: Typography, Images, Icons, Shadows, Border radius, Colors, Spacing

ChairApp:

- Use `grid` for layouting
- Use `flex` for one dimentional components
- Use enough spacing (margin-bottom) between sections
- For site's main heading use `h1`, for each section heading use `h2`. For sub-headings use `h3` and so on
- Use a system for font sizes and spacing

Components

- Accordion:
  - Use `flex-direction: column` instead of `margin-bottom` to create vertical gaps between elements. This stacks accoridions vertically
  - Display grid for layouting of each accordian (item)
  - Open state trick: use a class (e.g. open) to style an element differently
  - Toggle open class using JS
- Carousel:
  - Create flex container that contains image and the text
  - Image scaling `transform: scale(value)`
  - For controls (buttons and dots)
    - Give `absolute positioning` to take them out of the normal flow
    - Centering absolutly positioned element using `transform: tanslate(X, Y), top, bottom, left, right` properites
- Table
- Pagination

Section Components

- Hero Section:
  - Design logic
  - Viewport height (to assing height as per current viewport): `100vh`
  - Add overlay to the image: `background-image: linear-gradient(color1, color2), url(image-path)`
  - Cover the image: `background-size: cover`
- App Layout:
  - Design logic using Grid
  - Scroll bar: `overflow: scroll`, `flex-shrink: 0` (Reset flex shrink)

Website building principles

- Website building process
- Define, Plan and Sketch
- Define CSS Design System: Typography, colors, spaces, etc
- Visual hierarchy: Space (distance between components), font-size, font-colors (tints & shades)
- Responsive desing:
  - flexible Grids unit `fr`
  - flexible images unit `%`
  - avoid horizontal scrolling using `max-width`
  - flexible fonts and spacing unit `rem` (1rem = 16px)

Omnifood

- Build 'Hero' section
- Build Navigation
- Build 'How to' section
  - Reusable grid & centered container classes
  - Pseudo elements (before, after) to add circles behind the image
- Build Meals section
  - Hide overflowing content: `overflow-hidden`
  - Animation (move element up on hover): `transform: translateY(-1.2rem);`
- Build testimonial + gallery section
  - Animation (scale element on hover): `transform: scale(1.2)`
- Build pricing section
  - Animation (rotate element): `transform: rotate(45deg)`
  - Multiple grids inside an element, Add margin to above grids but not the last grid `.grid:not(:last-child) { margin-bottom: 9.6rem; }`
- Build CTA section: Gradient, image overlay, form
- Build footer

Responsive Design (Desktop first approach)

- `@media (max-width: 600px){}` - Apply styles maximum upto `600px` only not after that
- rem and em does not depend on html font-size in media queries. Instead, 1rem = 1em = 16px
- Using `em` for media queries, e.g. media query for 1344px (1344 / 16 = 84em) will be `@media (max-width: 84em){}`
- To reduce _font-size_ set `rem` to less than 10px e.g. to set `1rem` to `9px` for Tablets `9px/16px = 0.5625px = 56.25%`, so the _font-size_ will be `html { font-size: 56.25%; }`. Now, `20rem` will be `180px` not `200px`
- Mobile navigation
  - Create navigation in CSS that covers the view port height
  - Write CSS for show/hide navigation using `opacity`.
  - Create a helper class that contains the CSS to show navigation
  - Add and remove the helper class using JS
