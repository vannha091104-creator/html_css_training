Lists, Tables and Forms
CSS provides special properties designed specifically for styling lists, tables, and forms, helping you control their appearance in more detail.
Bullet Point Styles
The list-style-type property controls the appearance of bullets or numbering in lists.
Overview
Applies to <ul>, <ol>, and <li> elements
Defines the marker (bullet or number) style
Helps customize list appearance
Unordered Lists (<ul>)
Common values:
none → no bullet
disc → filled circle (default)
circle → hollow circle
square → square bullet
Ordered Lists (<ol>)
Common values:
decimal → 1, 2, 3
decimal-leading-zero → 01, 02, 03
lower-alpha → a, b, c
upper-alpha → A, B, C
lower-roman → i, ii, iii
upper-roman → I, II, III
Key Points
Can remove bullets using none
Works with both ordered and unordered lists
Improves readability and design consistency
list-style-type is essential for controlling list markers
Helps create clean and customized list layouts

Images for Bullets
The list-style-image property allows you to use an image as the bullet (marker) for list items.
Overview
Replaces default bullets with a custom image
Applies to <ul> and <li> elements
Useful for decorative and branded lists
Key Points
The image is used as the bullet for each list item
If the image cannot be loaded, the browser falls back to list-style-type
Works best with small, simple icons
Related Properties
list-style-type → fallback bullet style
list-style-position → controls bullet alignment (inside / outside)
list-style-image helps create custom and visually appealing lists
Ideal for icons, branding, and enhanced UI design










Positioning the Marker
The list-style-position property controls where the bullet or number appears in relation to the text.
Overview
Applies to <ul> and <ol> lists
Affects alignment of the marker and text
Helps control spacing and readability
Values
outside (default)
*Marker is placed outside the text block
Text aligns neatly
Common for most layouts
inside
Marker is placed inside the text block
Text wraps under the marker
Creates a more compact layout
Key Points
outside keeps text aligned cleanly
inside may affect readability for long lines
Often used with list-style-type or list-style-image
list-style-position helps fine-tune list layout and alignment
Useful for improving visual structure and spacing






List Shorthand
The list-style property is a shorthand that allows you to set multiple list properties in one declaration.
Overview
Combines:
list-style-type
list-style-position
list-style-image
Makes code shorter and cleaner
Syntax: list-style: type position image;
Possible Values
Type → disc, circle, square, decimal, etc.
Position → inside, outside
Image → url("image.png")
Key Points
You don’t need to include all values
Missing values will use default settings
Improves readability and reduces repetition
list-style is a convenient way to combine list properties
Helps write cleaner and more efficient CSS code







Table Properties
CSS provides several properties to style and control the appearance of tables.
Overview:
Used to improve readability and layout of tables
Applied to <table>, <th>, and <td> elements
Helps organize data clearly
Common Properties:
width
Sets the width of the table
padding
Adds space inside table cells
Improves readability
text-transform
Controls text style (e.g., uppercase)
letter-spacing / font-size
Adjusts spacing and size of text
border-top / border-bottom
Adds borders to table headers
text-align
Aligns content (left, right, center)
background-color
Adds color to rows or cells
:hover
Highlights rows when hovered
Key Point:
Combining these properties helps create clean, structured, and readable tables
Table properties allow precise control over data presentation
Essential for creating clean and user-friendly tables


Border on Empty Cells
CSS allows you to control how borders appear on empty table cells.
Overview:
Used with tables to handle empty <td> cells
Controls whether borders are shown or hidden
Works with the empty-cells property
Values:
show
Displays borders for empty cells
hide
Hides borders for empty cells
Key Notes:
Only works when border-collapse: separate is used
If border-collapse: collapse, this property has no effect
Useful for cleaner table design
Key Point:
Helps improve table appearance by removing unnecessary borders









Gaps Between Cells
CSS allows you to control the spacing between table cells.
Overview:
Controls space between borders of table cells
Uses border-spacing and border-collapse
Applies to <table> elements
Properties:
border-spacing
Sets the distance between cells
Can take one or two values
One value → applies to both directions
Two values → horizontal and vertical spacing
 border-collapse
Defines how borders are handled
Values of border-collapse:
separate
Cells have space between them
border-spacing works
collapse
Borders are merged together
No gaps between cells
Key Point:
Use separate + border-spacing to create gaps
Use collapse to remove spacing and merge borders





Styling Forms
CSS allows you to control the appearance of form elements to improve usability and design.
Overview:
Used to style form controls like <input>, <textarea>, <select>, and <button>
Helps make forms more attractive and user-friendly
Improves readability and interaction
Common Properties:
font-family / font-size
Controls text appearance inside form fields
color / background-color
Sets text and background colors
border
Defines the outline of form elements
padding
Adds space inside inputs for better usability
margin
Controls spacing between form elements
Useful Techniques:
Use :focus
Highlights input when user clicks on it
Use :hover
Adds interaction when hovering over buttons
Style buttons
Make them more visible and clickable
Key Point:
Well-styled forms improve user experience and make interfaces easier to use



Styling Text Inputs
CSS allows you to style text input fields to improve usability and visual design.
Overview:
Applies to <input type="text"> and <textarea>
Improves readability and user experience
Makes forms look consistent and modern
Common Properties:
font-family / font-size
Controls text appearance inside inputs
color
Sets text color
background-color
Changes input background
border
Styles the input outline
padding
Adds space inside the input
width
Controls input size
Useful Pseudo-classes:
:focus
Changes style when the input is active
:hover
Adds effect when hovering
Key Point:
Clear and well-spaced inputs make forms easier to use and more accessible




Styling Submit Buttons
CSS allows you to customize the appearance of submit buttons to make them more interactive and visually appealing.
Overview:
Applies to <input type="submit"> or <button>
Enhances usability and user interaction
Helps buttons stand out on the page
Common Properties:
color
Sets the text color
background-color
Changes button background
border
Defines button edges and thickness
text-shadow
Adds depth to button text
padding
Increases clickable area
Useful Techniques:
Use gradients
Creates a modern button look
Use border-bottom
Adds a 3D effect
Pseudo-class:
:hover
Changes appearance when user hovers
Can adjust color, border, or background
Key Point:
Well-styled buttons improve user interaction and make actions clear

Styling Fieldsets & Legends
CSS allows you to style <fieldset> and <legend> to group and label form sections clearly.
Overview:
<fieldset> groups related form elements
<legend> provides a title for the group
Improves form structure and readability
Common Properties:
border
Styles the outline of the fieldset
padding
Adds space inside the fieldset
margin
Controls spacing around the fieldset
width
Sets the size of the fieldset
Styling Legend:
font-size / font-weight
Emphasizes the title
color
Changes text color
padding
Adds spacing around the legend text
Key Point:
Using fieldsets and legends helps organize forms and makes them easier to understand




Aligning Form Controls : Problem
Form elements are often misaligned by default, making forms harder to read and use.
Overview:
Labels and inputs may not line up properly
Each element can appear on different lines
Creates an inconsistent layout
Common Issues:
Labels have different lengths
Inputs are not vertically aligned
Radio buttons and checkboxes are uneven
Form looks unstructured
Why It Matters:
Poor alignment reduces readability
Makes forms harder to complete
Affects user experience
Typical Behavior:
Each form control appears on a new line
Labels do not align with inputs
Related elements are not grouped visually
Key Point:
Proper alignment is important to create clean, user-friendly forms







Aligning Form Controls : Solution
CSS provides techniques to align form elements neatly for better layout and usability.
Overview:
Aligns labels and inputs in a straight line
Creates a clean and structured form layout
Improves readability and user experience
Key Techniques:
float
Moves labels to the left
Allows inputs to sit beside them
width
Sets equal width for labels
Ensures consistent alignment
text-align
Aligns label text (often right-aligned)
padding / margin
Adds spacing between labels and inputs
Layout Approach:
Each row contains a label and a form control
Labels are aligned in one column
Inputs are aligned in another column
Additional Styling:
Use spacing between rows for clarity
Align submit button to the right
Group related inputs together
Key Point:
Combining float, width, and spacing creates a clean, professional form layout



Cursor Styles
CSS allows you to control the appearance of the mouse cursor.
Overview:
Defines how the cursor looks when hovering over elements
Improves user interaction and feedback
Applied using the cursor property
Common Values:
auto
Default browser behavior
default
Standard arrow cursor
pointer
Hand icon (used for links)
text
Indicates text selection
move
Shows element can be moved
wait
Indicates loading or processing
help
Suggests help is available
crosshair
Precision selection cursor
Custom Cursor:
Use url()
Allows custom cursor images
Key Point:
Use cursor styles appropriately to match user expectations and improve usability


Web Developer Toolbar
The Web Developer Toolbar allows you to inspect and analyze web pages directly in your browser.
For example, you can view the HTML structure or see the CSS styles applied to an element when you hover or click on it.
Here are the most commonly used features:
Outlines:
Highlights elements by drawing borders around them to show layout and spacing.
Structure
Displays the HTML structure of the page, helping you understand how elements are nested.
CSS styles
Shows the CSS rules applied to an element, including their source.
You should use this tool to debug layouts, check styles, and better understand how web pages are built.
Summary List, Tables and Forms
In addition to the CSS properties covered in other chapters which work with the contents of all elements, there are several others that are specifically used to control the appearance of lists, tables, and forms.
List markers can be given different appearances using the list-style-type and list-style image properties.
Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent. 
Forms are easier to use if the form controls are vertically aligned using CSS.
Forms benefit from styles that make them feel more interactive.
