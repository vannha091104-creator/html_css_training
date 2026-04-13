Layout
Page Layout and Positioning This chapter explains how to control the placement of elements and create page layouts for web design.
Key Concept in Positioning Elements
CSS treats every HTML element as a box. These boxes can be either block-level or inline, and they form the foundation of page layout.
Building Blocks:
Each element is displayed as a box
Boxes can be block-level or inline
Box size and spacing can be controlled using width, height, margin, padding, borders, and background
Block-level Elements: 
Start on a new line
Act as main layout structure
Examples: <h1>, <p>, <ul>, <li>
Inline Elements: 
Flow within surrounding text
Do not start on a new line
Examples: <img>, <b>, <i>
Containing Elements A containing (parent) element is a block-level element that holds other elements inside it, usually using <div>.
Nested Elements Elements can be placed inside multiple layers. The direct outer element is called the parent element.
Understanding boxes, element types, and containing elements is essential for building structured and well-designed web pages.




Controlling the Position of Elements
Positioning allows you to control layout using properties like position and float, along with offset properties (top, bottom, left, right).
Positioning Schemes:
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
Overlapping Elements When elements are moved out of normal flow, they can overlap. The z-index property controls which element appears on top.
Understanding positioning methods helps control layout effectively and create flexible, well-structured web pages.


Normal Flow
In normal flow, block-level elements are displayed one below another. Browsers automatically arrange elements without needing extra CSS positioning.
How It Works
Elements follow the order in the HTML structure
Each block-level element starts on a new line
Inline elements flow within text
Default Behavior
position: static is applied by default
No need to specify position unless changing layout
Elements expand to fit the width of their container
Example Behavior
Headings and paragraphs appear from top to bottom
Elements stretch to full width unless a width is set
Setting width (e.g., 450px) limits element size but still keeps normal flow
Normal flow is the foundation of web layout. Understanding it helps you manage how elements naturally appear before applying other positioning methods.









Relative Positioning
Định vị tương đối dịch chuyển một phần tử mà không ảnh hưởng đến bố cục của các phần tử xung quanh. Khoảng cách ban đầu của phần tử vẫn được giữ nguyên.
How It Works
Element remains in normal flow
Position is adjusted using offset properties
Common properties: top, bottom, left, right
Offset Behavior
top / bottom → move element vertically
left / right → move element horizontally
Values can be in pixels, percentages, or ems
Example Behavior
Element can move down (e.g., top: 10px)
Element can move right (e.g., left: 100px)
Other elements stay in their original positions
Relative positioning is useful for fine-tuning element placement while keeping the overall layout stable.









Absolute Positioning
Absolute positioning takes an element out of the normal layout, so it no longer affects other elements on the page.
How It Works
Element is removed from normal flow
Position is based on the nearest containing (parent) element
Uses offset properties: top, bottom, left, right
Offset Behavior
top / bottom → control vertical position
left / right → control horizontal position
Values are usually in pixels, percentages, or ems
Example Behavior
Element can be placed at a specific position (e.g., top: 0, left: 500px)
Other elements ignore it and may overlap
Width is often set to prevent content overlapping
Best Practices
Use when precise positioning is needed
Always define a containing element
Be careful with overlapping content
Absolute positioning is useful for placing elements exactly where needed, but should be used carefully to avoid layout issues.







Fixed Positioning
Fixed positioning keeps an element in the same place even when the page is scrolled. It is a type of absolute positioning.
How It Works
Element is positioned relative to the browser window
Removed from normal flow
Uses offset properties: top, bottom, left, right
Offset Behavior
top / bottom → control vertical position
left / right → control horizontal position
Element stays fixed when scrolling
Example Behavior
Element can be placed at a fixed spot (e.g., top: 0, left: 50px)
Remains visible while scrolling
Other elements ignore its space
Fixed positioning is useful for keeping important elements visible at all times, but should be used carefully to maintain a good user experience.









Overlapping Elements
When using relative, absolute, or fixed positioning, elements can overlap. By default, elements that appear later in the HTML will be displayed on top.
How It Works
z-index is used to control stacking order
Works only on positioned elements (relative, absolute, fixed)
Higher value → element appears on top
Lower value → element appears behind
Default Behavior
Without z-index, stacking follows HTML order
Later elements overlap earlier ones
Example Behavior
Element with z-index: 10 appears above z-index: 5
Helps ensure important elements stay visible
Commonly used with positioned headings or menus
Conclusion z-index helps manage overlapping elements and ensures the correct element appears on top, improving layout control and user experience.









Floating Elements
The float property moves an element out of normal flow and aligns it to the left or right, allowing other content to wrap around it.
How It Works
Element is removed from normal flow
Positioned to the left or right of its container
Other elements flow around it
Key Behavior
Floating requires setting a width for proper layout
Without width, the element may take full container width
Common values: float: left, float: right
Example Behavior
An element (e.g., blockquote) can float to the right
Text and paragraphs wrap around the floated element
Used for layouts like images with text wrapping
Conclusion Floating elements are useful for wrapping content and creating simple layouts, but should be used carefully for better control and consistency.










Using Float to Place Elements Side-By-Side
The float property is commonly used to place boxes side-by-side instead of stacking them vertically.
How It Works
Elements are floated left (or right)
Each element has a defined width
Elements line up next to each other within the container
Layout Behavior
Elements may not align perfectly if heights are different
A box may move below another if there is not enough space
Position depends on available space in the row
Example Behavior
Multiple paragraphs can appear in columns
A paragraph may drop below others if blocked by previous elements
Layout depends on content size and spacing
Using float helps create side-by-side layouts, but requires careful control of width and spacing to maintain a clean design.









Clearing Float
The clear property specifies which sides of floating elements are not allowed to touch a particular element. It is used to fix layout issues caused by float.
How It Works
Applied to elements inside the same container
Prevents elements from sitting next to floated elements
Forces elements to move below floats when needed
Clear Values
left → element does not touch left-floated elements
right → element does not touch right-floated elements
both → element does not touch any floated elements
none → default, allows elements to touch both sides
Example Behavior
An element with clear: left moves below left-floated elements
Helps prevent overlapping or wrapping issues
Ensures proper vertical alignment in layouts
Conclusion The clear property helps manage floating behavior and ensures elements are properly positioned without unwanted overlap.









Parents of Floated Elements: Problem
If a parent element contains only floated elements, the browser may treat its height as zero, causing layout problems.
How It Happens
All child elements are floated
Floated elements are removed from normal flow
Parent cannot detect their height
Resulting Issue
Parent element collapses (height becomes 0)
Borders or background may not display correctly
Layout appears broken (e.g., border looks like a thin line)
Example Behavior
A <div> with only floated elements does not expand
Border collapses and does not wrap content properly
When a parent contains only floated elements, it may collapse. This is a common issue that needs to be handled to maintain proper layout.










Parents of Floated Elements: Solution
To prevent a parent element from collapsing, developers use techniques to ensure it properly contains its floated children.
Traditional Solution
Add an extra element after floated elements
Apply clear: both to that element
Forces the parent to expand
However, adds unnecessary HTML
Modern CSS Solution
Use CSS instead of extra HTML
Apply overflow: auto to the parent element
Set width (e.g., width: 100%)
Allows parent to wrap around floated children
How It Works
overflow: auto creates a new block formatting context
Parent element expands to contain floated elements
No need for additional elements in HTML
Using CSS properties like overflow helps fix float issues efficiently and keeps the code cleaner without extra elements.








Creating Multi-Column Layouts with Floats
Multi-column layouts are created by placing <div> elements side-by-side using CSS properties like width, float, and margin.
Key Properties
width → sets the size of each column
float → positions columns next to each other
margin → creates spacing between columns
Two-Column Layout
Uses two <div> elements
One for main content, one for sidebar
Each column has its own width and float
Columns align horizontally if space allows
Three-Column Layout
Uses three <div> elements
Each column is floated left
All columns have equal or defined widths
Columns appear side-by-side in one row
Layout Behavior
Columns stay in the same row if total width fits container
If not enough space, columns move to the next line
Content inside columns can include text, images, or other elements
Float can be used to create flexible multi-column layouts, such as two-column or three-column designs, for structured web pages






Screen Sizes
Users access websites on devices with different screen sizes, so layouts must adapt to display properly on all screens.
Key Idea
Different screens show different amounts of content
Design must work well on various screen sizes
Device Differences
Small screens → mobile phones
Medium screens → tablets
Large screens → desktops and monitors
Design Challenges
Content may look different on each device
Users may see more or less information depending on screen size
Layout must remain clear and usable
Important Notes
Unlike print, web design cannot rely on fixed sizes
Screen sizes continue to change and increase
More users access websites on mobile devices
Screen size plays an important role in web design. A good design must adapt to different devices to provide a consistent user experience.







Screen Resolution
Resolution refers to the number of pixels displayed on a screen. Higher resolution means more pixels and sharper images.
Key Idea
More pixels → clearer and sharper display
Fewer pixels → less detail on screen
Device Differences
Small devices can have high resolution
Large screens may have different resolution settings
Users can adjust resolution on their devices
Display Behavior
Higher resolution makes text and elements appear smaller
Lower resolution makes content appear larger
Same website may look different depending on resolution
User Control
Operating systems allow users to change screen resolution
Common options range from low to high pixel settings 
Screen resolution impacts how content appears. Good design ensures clarity and usability across different resolution settings.








Page Sizes
Because screen sizes and resolutions vary, web pages are often designed with a width of around 960–1000 pixels to fit most users.
Key Idea
Page width is usually fixed within a common range
Design must work well across different screen sizes
Page Height
Harder to control than width
Users may not see the full page without scrolling
Important content should appear at the top
Above the Fold
Refers to the area visible without scrolling
Typically around the top 570–600 pixels
Used to show key information first
User Behavior
Users can decide quickly if a page is useful
Most users are willing to scroll for more content
Design should encourage scrolling
Design Considerations
Do not overload the top section with too much content
Provide a preview of content below
Ensure layout adapts to different devices
Page size design balances width, height, and user behavior to create effective and user-friendly web pages





Fixed Width Layouts
Fixed width layouts keep the same size regardless of screen size. Measurements are usually set in pixels.
Key Idea
Layout size remains constant
Does not adjust to different screen sizes
Advantages
Precise control over layout and positioning
Consistent appearance across devices
Text line lengths remain stable
Images keep the same size relative to layout
Disadvantages
May create empty space on large screens
Content can appear too small on high-resolution screens
Text may overflow if font size increases
Not flexible for different devices
May require more vertical scrolling
Fixed width layouts provide control and consistency but lack flexibility for modern responsive design.








Liquid Layouts
Liquid layouts expand and shrink depending on screen size. They usually use percentages instead of fixed units.
Key Idea
Layout is flexible and responsive
Adapts to different screen sizes
Advantages
Fills the entire browser width
No empty space on large screens
Reduces need for horizontal scrolling
Adapts to different font sizes
Disadvantages
Layout may look inconsistent on different screens
Text lines can become too long on wide screens
Content may be squeezed on small screens
Images or fixed elements may overflow
Liquid layouts provide flexibility and adaptability, but require careful control to maintain a consistent and readable design.
A Fixed Width Layout
To create a fixed width layout, the width of the main boxes on a page will usually be specified in pixels (and sometimes their height, too).
Here you can see several <div> elements, each of which uses an id or class attribute to indicate its purpose on the page.
In a book like this, the result of both the fixed and liquid layouts look similar. To get a real feel for them, you need to view them in your browser and see how they react when you adjust the size of the browser window.
The fixed width layout will stay the same width no matter what size the browser window is, whereas the liquid layout will stretch (or shrink) to fill the screen.
The HTML is the same for both the fixed width layout example on this page and the liquid layout example you see next.
A Liquid Layout
A liquid layout uses percentages for widths, so the design stretches or shrinks to fit the browser window.
Key Points
Uses percentages (%) instead of pixels
Layout resizes with screen
Columns float next to each other
May need min-width / max-width to control layout
Result
Flexible layout
Adapts to different screen sizes
Content stretches or shrinks automatically
Layout Grids
A grid is a structure used to organize elements on a page. Designers use grids to create balanced and consistent layouts.
Key Idea: Grids help maintain consistent spacing and proportions, making designs look more professional.
Details
A common example is the 960px grid system
Layouts are often divided into columns (e.g. 2 or 3 columns)
Many web pages are built based on grid structures
Advantages
Creates consistency across pages
Helps users navigate and find information easily
Makes it easier to add new content
Supports team collaboration in design
Result
Clean and organized layout
Professional appearance
Better user experience
Possible Layouts: 960 Pixel Wide 12 Column Grid
A 960px grid divides the page into 12 equal columns, allowing flexible layout combinations.
Structure
Total width: 960px
12 columns (each ~60px)
Columns have margins (gutters) between them
Layout Options
You can combine columns to create different widths:
12 columns → full width (940px)
6 + 6 → two columns (460px each)
4 + 4 + 4 → three columns (300px each)
Smaller combinations (220px, 140px, etc.)
Key Points
Columns can be merged to create many layouts
Gutters create spacing between columns
Same grid can be reused for multiple designs
Result
Flexible and consistent layouts
Easy to design complex pages
Widely used in web design systems







CSS Frameworks
CSS frameworks provide ready-made code for common tasks like layouts, forms, and styling, so you don’t have to write CSS from scratch.
ADVANTAGES
Save time by reusing code
Tested across browsers → fewer bugs
DISADVANTAGES
Require using class names in HTML
May include extra unused code (bloat)
EXAMPLE: 960.GS
A popular framework for grid layouts
Uses a 12-column grid system
Main container is 960px wide
Provides classes like grid_1 → grid_12
Key Points
Add framework CSS → use predefined classes
Easily create multi-column layouts
Other frameworks exist (Blueprint, Less Framework, etc.)
Result
Faster development
Consistent design
Less manual CSS coding






A Grid-Based Layout Using 960.GS 
Concept:
Uses the 960.gs grid system to build layouts.
Layout is controlled by CSS classes, not custom positioning.
How to use:
Include the CSS file:
<link rel="stylesheet" href="css/960_12_col.css" />
Main container:
<div class="container_12 clearfix">
container_12 → defines a 12-column grid
clearfix → fixes height issues caused by floated elements
Columns:
grid_12 → full width (12 columns)
grid_4 → 4 columns (1/3 width)
<div class="grid_12">Header</div>
<div class="grid_4">Column One</div>
<div class="grid_4">Column Two</div>
<div class="grid_4">Column Three</div>
<div class="grid_12">Footer</div>






Custom CSS: 
* {
   font-family: Arial, Verdana, sans-serif;
   text-align: center;
}
#nav, #feature, .article, #footer {
   background-color: #efefef;
   margin-top: 20px;
   padding: 10px;
}
Key idea:
960.gs handles:
layout structure
column widths
spacing
Your CSS handles:
colors
fonts
spacing adjustments
visual styling

Remember
960.gs = layout system (grid-based)
You = design & styling

Multiple Style Sheets ( @import) 
Concept:
CSS can be split into multiple files (layout, typography, colors…).
Helps organize and reuse styles.
Ways to use multiple CSS files:
Using <link> in HTML
<link rel="stylesheet" href="styles.css" />
Using @import in CSS
@import url("tables.css");
@import url("typography.css;
Example:
@import url("tables.css");
@import url("typography.css");

body {
    color: #666666;
    background-color: #f8f8f8;
    text-align: center;
}
Key notes:
@import must be placed at the top of the CSS file
It allows one stylesheet to include others
Helps create modular CSS structure
Advantages:
Better organization
Easier maintenance
Reusable styles
 Disadvantages:
Can slow loading (more requests)
Harder to manage if too many files
Remember:
<link> = connect CSS to 
@import = connect CSS to CSS

















Multiple Style Sheets ( link) 
Concept:
Use multiple <link> tags in HTML to include separate CSS files.
Each file can handle different parts (layout, tables, typography…).
How to use:
<link rel="stylesheet" href="css/site.css" />
<link rel="stylesheet" href="css/tables.css" />
<link rel="stylesheet" href="css/typography.css" />
How it works:
All stylesheets are loaded in the <head>
Browser applies them from top to bottom
Rules loaded later override earlier ones
Key notes:
No @import needed
Each CSS file is linked directly to HTML
Order of <link> matters
Advantages:
Faster loading than @import
Clear structure
Easy to manage separate styles
Disadvantages:
Must manage order carefully
Too many files → more HTTP requests
Remember
<link> = best practice for multiple CSS 
Last file loaded = highest priority


Summary Layout
<div> elements are often used as containing elements to group together sections of a page.
Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.
The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)
Pages can be fixed width or liquid (stretchy) layouts.
Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling).
Grids help create professional and flexible designs.
CSS Frameworks provide rules for common tasks
You can include multiple CSS files in one page.
