# Layout

## Page Layout and Positioning
This chapter explains how to control the placement of elements and create page layouts for web design.

---

## Key Concept in Positioning Elements
CSS treats every HTML element as a box. These boxes can be either block-level or inline, and they form the foundation of page layout.

### Building Blocks
- Each element is displayed as a box
- Boxes can be block-level or inline
- Box size and spacing can be controlled using width, height, margin, padding, borders, and background

---

## Element Types

### Block-level Elements
- Start on a new line
- Act as main layout structure

Examples:
```html
<h1>, <p>, <ul>, <li>
Inline Elements
Flow within surrounding text
Do not start on a new line

Examples:

<img>, <b>, <i>
Containing Elements

A containing (parent) element is a block-level element that holds other elements inside it, usually using <div>.

Nested Elements

Elements can be placed inside multiple layers. The direct outer element is called the parent element.

Understanding boxes, element types, and containing elements is essential for building structured and well-designed web pages.

Controlling the Position of Elements

Positioning allows you to control layout using properties like position and float, along with offset properties (top, bottom, left, right).

Positioning Schemes
Normal Flow
Elements appear in order from top to bottom
Each block-level element starts on a new line
This is the default layout behavior
Relative Positioning
Moves an element relative to its normal position
Can shift top, right, bottom, or left
Does not affect surrounding elements
Absolute Positioning
Positions an element relative to its containing element
Removed from normal flow
Does not affect other elements
Fixed Positioning
Positions an element relative to the browser window
Stays in place when scrolling
Does not affect other elements
Floating Elements
Allows elements to move left or right inside a container
Removed from normal flow
Other content can flow around it
Overlapping Elements

When elements are moved out of normal flow, they can overlap.

z-index controls stacking order
Higher value → on top
Lower value → behind
Normal Flow (Detail)
Default: position: static
Elements follow HTML order
Block elements start on new line
Inline elements flow in text
Float Layout
Using Float
Moves element left or right
Requires width for proper layout

Example:

float: left;
width: 300px;
Clearing Float

Used to prevent layout issues:

clear: both;
Float Problem

If a parent contains only floated elements:

Parent height collapses (0)
Layout breaks
Solution
overflow: auto;
Multi-Column Layout
Use float + width
Elements can be placed side-by-side
Screen Sizes
Mobile
Tablet
Desktop

Layout must adapt to different devices.

Screen Resolution
More pixels → sharper display
Layout may look different across devices
Page Sizes
Common width: 960–1000px
Important content should appear at the top (above the fold)
Layout Types
Fixed Width Layout
Uses pixels
Consistent but not flexible
Liquid Layout
Uses percentages
Flexible but harder to control
Grid System
Example: 960px grid
Often uses 12 columns
CSS Frameworks

Example: 960.gs

Provides predefined grid system
Uses classes like:
grid_4, grid_12
Custom CSS Example
* {
  font-family: Arial, Verdana, sans-serif;
  text-align: center;
}
Multiple Stylesheets
Using link
<link rel="stylesheet" href="style.css">
Using @import
@import url("style.css");
Summary
HTML elements are boxes
Layout uses positioning and float
Pages can be fixed or flexible
Grid systems help design
Multiple CSS files improve organization
