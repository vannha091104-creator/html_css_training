Text (2)
Text styling in CSS is divided into two groups: properties that control the font itself (such as typeface, size, bold, italic) and properties that affect text appearance regardless of the font (such as color and spacing). Proper text formatting improves readability and makes web pages more visually appealing.
Typeface Terminology
Typography includes different font categories and properties that affect how text appears and how readable it is.
Font Categories:
Serif Fonts:
Have decorative strokes (serifs) at the ends of letters
Key Point:
Easier to read in printed text and long passages
Sans-Serif Fonts:
Do not have decorative strokes
Clean and modern design
Key Point:
More suitable for screens, especially at small sizes
Monospace Fonts:
Each character has equal width
Key Point:
Commonly used for code and structured text
Font Structure:
Baseline: Line where letters sit
Cap Height: Height of uppercase letters
X-Height: Height of lowercase letters (e.g., “x”)
Ascender: Part of a letter that extends above the cap height
Descender: Part of a letter that goes below the baseline
Font Properties:
Weight:
Light, Medium, Bold, Black
Key Point:
Affects emphasis, spacing, and contrast
Style:
Normal, Italic, Oblique
Key Point:
Italic is more cursive, Oblique is slanted version of normal text
Stretch:
Condensed, Regular, Extended
Key Point:
Condensed = narrower letters
Extended = wider letters
Font choice and properties impact readability and design
Different styles and structures help create hierarchy and visual interest
Choosing the right typeface improves user experience












Choosing a Typeface for Your Website
Choosing the right typeface is important to ensure text displays correctly and remains readable across different devices.
Basic Principle:
A browser can only display fonts that are installed on the user’s device
If a font is not available, it will fall back to another font
Common Typeface Categories:
Serif:
Fonts with decorative strokes
Examples: Georgia, Times, Times New Roman
Sans-Serif:
Clean fonts without decorative strokes
Examples: Arial, Verdana, Helvetica
Monospace:
Fixed-width fonts (each character has equal width)
Examples: Courier, Courier New
Cursive:
Fonts with a handwritten or cursive style
Examples: Comic Sans MS, Monotype Corsiva
Fantasy:
Decorative and stylized fonts
Examples: Impact, Haettenschweiler
Key Point:
Browsers support at least one font from each category
It is recommended to include a generic font family as a fallback
Font Stack:
You can define multiple fonts in order of preference
Example: font-family: Georgia, Times, serif;
Always consider availability of fonts on user devices
Use font stacks to ensure consistent display
Choose appropriate font categories based on content and purpose
Techniques that offer a Wider Choice of Typefaces
There are several techniques that allow websites to use more fonts beyond those installed on a user’s device. However, these methods are affected by licensing and performance considerations.
Font-Family (System Fonts):
Uses fonts already installed on the user’s computer
No need to download additional files
Key Point:
Limited choice of typefaces but high compatibility
@font-face:
Allows fonts to be downloaded from a specified source
Enables use of custom fonts on websites
Key Point:
Requires proper licensing
May affect page load performance
Service-Based Font-Face:
Uses third-party services (e.g., Google Fonts)
Provides access to a wide range of fonts
Key Point:
Services handle licensing and font delivery
May involve subscription or usage limits
Other Techniques:
Images:
Text is saved as an image to preserve design
Key Point:
Not selectable and less accessible
SIFR:
Uses Flash and JavaScript to display custom fonts
Key Point:
Requires plugins and is less commonly used today
Cufon:
Uses JavaScript to render fonts as vector shapes
Key Point:
Does not require Flash but still has limitations
Fonts may render differently on Mac and Windows systems
Always test designs across platforms
@font-face and font services provide the most flexibility
System fonts ensure compatibility
Always balance design, performance, and licensing requirements
Specifying Typefaces
CSS allows you to specify which typeface should be used for text using the font-family property.
Font-Family:
Defines the typeface used for text inside an element
Applied using CSS rules
Values: 
The value is the name of the typeface
Can include multiple fonts in order of preference
How It Works:
The browser will try to use the first font listed
If it is not available, it will use the next one
Example:
font-family: "Times New Roman", Times, serif;
Key Point:
Always include a generic font family (e.g., serif, sans-serif) at the end
Ensures text is displayed even if specific fonts are not available
font-family controls how text appears on a webpage
Using multiple fonts improves compatibility
Helps maintain consistent design across different devices



Size of Type
CSS provides ways to control the size of text to improve readability and layout design.
Font-Size Property:
Used to specify the size of text
Can be applied to any HTML element
Units of Measurement:
Pixels (px):
Fixed size
Commonly used for precise control
Percent (%):
Relative to the parent element
Helps create flexible layouts
Ems (em):
Relative to the font size of the parent
Allows scalable and responsive design
Key Point:
Relative units (%, em) are more flexible than fixed units (px)
Help improve accessibility and responsiveness
font-size controls how large or small text appears
Choosing the right unit is important for usability
Use relative units for better adaptability across devices







Type Scales
Type scales are used to create a consistent system for sizing text across a design.
Definition:
A type scale is a set of predefined font sizes
Helps maintain consistency and visual hierarchy
Purpose:
Organizes text into levels (e.g., headings, subheadings, body text)
Makes content easier to read and understand
How It Works:
Sizes are usually based on a ratio (e.g., 1.2, 1.5)
Each level increases or decreases proportionally
Key Point:
Creates clear hierarchy between different text elements
Improves readability and design structure
Type scales ensure consistency in typography
Help guide users through content
Important for building clean and professional layouts
Units of Type Size
CSS provides different units to control text size, each with its own advantages.
Pixels (px):
Fixed-size unit
Gives precise control over text size
Key Point:
Not flexible for responsive design
Percent (%):
Relative to the parent element’s font size
Allows scalable layouts
Key Point:
Useful for maintaining proportions
Ems (em):
Relative to the font size of the parent element
Commonly used for flexible and responsive design
Key Point:
1em equals the size of the parent’s font
Key Point:
Relative units (%, em) adapt better to different screen sizes
Fixed units (px) are more consistent but less flexible
Choosing the right unit affects responsiveness and accessibility
Use relative units for scalable designs
Use pixels when precise control is needed
More Font Choice
CSS provides the @font-face rule to use custom fonts that are not installed on the user’s device.
@font-face Rule:
Allows you to define and load external fonts
The browser downloads the font if it is not available locally
Font-Family:
Specifies the name of the custom font
Used later in CSS like a normal font-family value
src (Source):
Defines the path to the font file
May include multiple formats for browser compatibility
format:
Specifies the type of font file (e.g., woff, ttf)
Helps browsers understand how to load the font
Key Point:
Fonts must have proper licenses to be used on websites
Multiple font formats may be needed for full browser support
Font Sources:
Open-source font libraries (e.g., Font Squirrel, Google Fonts)
Commercial font services (e.g., Typekit)
@font-face enables greater flexibility in design
Always check licensing before using fonts
Helps create unique and consistent typography on websites
Understanding Font Formats
Different browsers support different font formats, so multiple formats are needed to ensure compatibility.
Why Multiple Formats:
Browsers do not support the same font formats
Fonts must be provided in several versions to work across all browsers
Common Font Formats:
EOT: Used mainly for older versions of Internet Explorer
WOFF: Modern and widely supported format
TTF/OTF: Standard font formats for many systems
SVG: Used for older mobile browsers
Key Point:
Fonts should be listed in a specific order for best compatibility:
eot → woff → ttf/otf → svg
Performance Consideration:
Fonts need to be downloaded before being displayed
This may cause a flash of unstyled text (FOUT)
Optimization Tips:
Remove unused characters (glyphs) to reduce file size
Use faster hosting or CDNs for font delivery
Using multiple font formats ensures cross-browser support
Proper optimization improves performance and user experience
Always follow best practices when defining fonts in CSS





Bold
The font-weight property is used to control how bold or light text appears.
Font-Weight Property:
Specifies the thickness of text
Commonly used to emphasize important content
Values:
normal:
Default text weight
bold:
Makes text thicker and more prominent
Key Point:
Can be used as an “on/off” switch for bold text
Useful when overriding inherited styles
Usage:
Often applied to headings or important text
Can be set for specific elements using CSS
font-weight helps create emphasis and hierarchy
Improves readability by highlighting key information








Italic
The font-style property is used to control the style of text, such as making it italic.
Font-Style Property:
Specifies the style of the text
Commonly used to emphasize or differentiate content
Values:
normal:
Default text style
italic:
Displays text in an italic style
oblique:
Slants the text at an angle
Key Point:
Italic is usually a designed version of the font
Oblique is a slanted version of the normal text
Behavior:
If an italic version is not available, the browser may use oblique instead
font-style helps add emphasis and variation to text
Improves readability and visual hierarchy in content








Uppercase & Lowercase
The text-transform property is used to control the capitalization of text.
Text-Transform Property:
Changes the case of text without modifying the original content
Useful for styling and consistency
Values:
uppercase:
Converts all text to capital letters
lowercase:
Converts all text to small letters
capitalize:
Capitalizes the first letter of each word
Key Point:
Does not change the actual HTML content, only the display
Helps maintain consistent formatting across a website
text-transform improves visual consistency
Useful for headings, buttons, and labels
Enhances readability and design structure









Underline & Strike
The text-decoration property is used to add or remove decorative lines on text.
Text-Decoration Property:
Controls visual decorations such as lines on text
Commonly used for links and emphasis
Values:
none:
Removes any existing decoration
underline:
Adds a line under the text
overline:
Adds a line above the text
line-through:
Adds a line through the text
blink:
Makes text blink (rarely used and not recommended)
Key Point:
Often used to remove default underline from links
Can also be used to add emphasis or indicate changes (e.g., deleted text)
text-decoration enhances text styling
Useful for links and highlighting content
Should be used carefully to maintain readability






Leading
The line-height property is used to control the vertical space between lines of text.
Definition:
Leading refers to the vertical spacing between lines of text
Measured from one baseline to the next
Line-Height Property:
Sets the height of each line of text
Controls the distance between lines
Key Point:
Increasing line-height creates more space between lines
Improves readability, especially for long text
Usage:
Should be larger than the space between words
Common values are around 1.4em to 1.5em for body text
Behavior:
Relative values adjust based on the font size
Helps maintain consistent spacing across different devices
line-height improves readability and text flow
Important for creating comfortable reading experiences
Should be carefully adjusted for better design and usability







Letter & Word Spacing
CSS provides properties to control spacing between letters and words to improve readability and design.
Letter-Spacing:
Controls the space between individual letters
Also related to kerning in typography
Key Point:
Useful for uppercase text and headings
Word-Spacing:
Controls the space between words
Helps adjust text readability
Key Point:
Applied in addition to the default spacing
Units:
Values are usually set in em
Added on top of the default spacing defined by the font
Key Point:
Increasing spacing can improve readability
Too much spacing can make text harder to read
letter-spacing and word-spacing help fine-tune text layout
Important for readability and visual balance
Should be used carefully for best results






Alignment
The text-align property is used to control the horizontal alignment of text within an element.
Text-Align Property:
Defines how text is positioned horizontally
Applied to block-level elements
Values:
left:
Aligns text to the left (default for most languages)
right:
Aligns text to the right
center:
Centers the text
justify:
Stretches text so both edges align evenly
Key Point:
Justified text can create a clean look but may affect readability
Alignment should match the design and content purpose
text-align controls text layout and structure
Helps create visually balanced designs
Should be used appropriately for better readability








Vertical Alignment
The vertical-align property is used to control the vertical positioning of inline elements.
Vertical-Align Property:
Aligns elements vertically relative to surrounding content
Commonly used with inline or table-cell elements
Important Note:
Does NOT vertically align block-level elements (e.g., <div>, <p>)
Works best with inline elements (e.g., <img>, <span>)
Values:
baseline:
Aligns with the baseline of the text
top / text-top:
Aligns to the top of the text
middle:
Aligns to the middle of the line
bottom / text-bottom:
Aligns to the bottom of the text
sub / super:
Positions text as subscript or superscript
Other Values:
Can use length (px, em) or percentage for fine control
vertical-align is useful for aligning inline elements
Not suitable for general layout alignment
Helps improve positioning of small elements like icons and images





Indenting Text
The text-indent property is used to control the indentation of the first line of text.
Text-Indent Property:
Indents the first line of text inside an element
Commonly used for paragraphs
Values:
Can be set using units like px or em
Can also use negative values
Key Point:
Positive values indent text to the right
Negative values move text to the left (can hide text off-screen)
Usage:
Used for styling paragraphs
Can hide text while keeping it accessible (e.g., for logos or SEO)
text-indent helps control text layout
Useful for both design and accessibility techniques
Should be used carefully to maintain readability









CSS3: Drop Shadow
The text-shadow property is used to add shadow effects to text.
Text-Shadow Property:
Creates a shadow behind text
Helps enhance visual depth and readability
Syntax:
Can include multiple values: horizontal offset, vertical offset, blur radius, and color
Values:
Horizontal offset:
Controls left/right position of the shadow
Vertical offset:
Controls top/bottom position of the shadow
Blur radius (optional):
Defines how blurred the shadow appears
Color:
Sets the color of the shadow
Key Point:
More blur creates a softer shadow
Can simulate embossed or glowing effects
Compatibility Note:
Not fully supported in older browsers
Widely supported in modern browsers
text-shadow enhances text appearance
Useful for visual effects and emphasis
Should be used subtly for best readability




First Letter or Line
CSS provides pseudo-elements to style specific parts of text such as the first letter or first line.
Pseudo-Elements:
:first-letter and :first-line are pseudo-elements
Allow styling of only part of the text inside an element
:first-letter:
Targets the first letter of text
Commonly used for decorative effects (e.g., drop caps)
:first-line:
Targets the first line of text
Useful for emphasizing the beginning of a paragraph
Key Point:
These do not change HTML structure
Act like styling an extra “virtual” element
Behavior:
The first line can change depending on screen size
Responsive to layout and text flow
Additional Note:
Different from pseudo-classes (e.g., :hover, :visited)
Pseudo-elements style parts of elements, not states
:first-letter and :first-line enhance text presentation
Useful for styling specific portions of content
Help create more visually engaging typography






Styling Links
CSS provides pseudo-classes to style links based on their state.
Default Behavior:
Browsers display links in blue with an underline
Visited links change color to indicate they have been clicked
Pseudo-Classes:
Allow different styles for links depending on user interaction
:link
Targets links that have not been visited
Used to define the default appearance
:visited
Targets links that have been clicked
Helps users identify visited pages
Key Point:
Commonly used to control colors and text decoration (e.g., underline)
Improves navigation and user experience
Related Pseudo-Classes:
:hover – styles when the user moves the mouse over a link
:active – styles when the link is being clicked
:link and :visited help differentiate link states
Enhance usability and navigation clarity
Often combined with :hover and :active for better interaction design






Responding to Users
CSS provides pseudo-classes to style elements based on user interaction.
Overview:
These pseudo-classes change the appearance of elements when users interact with them
Commonly used for links, buttons, and form inputs
:hover
Applied when a user moves the cursor over an element
Commonly used to highlight links or buttons
Note: Not effective on touch devices (no cursor)
:active
Applied when an element is being clicked or pressed
Can create a “pressed” effect for buttons or links
:focus
Applied when an element is selected or ready for input
Common with form fields and interactive elements
Can also be triggered using keyboard navigation (e.g., Tab key)
Key Point:
These states improve user interaction and feedback
Help users understand what actions are possible
:hover, :active, and :focus enhance interactivity
Improve usability and accessibility
Essential for creating responsive and user-friendly interfaces






Attribute Selectors
Attribute selectors allow you to target HTML elements based on their attributes and values.
Overview:
Select elements using attributes instead of tag names or classes
Provide more precise and flexible styling
Common Selectors:
[attribute]:
Selects elements that have a specific attribute
[attribute="value"]:
Selects elements with an exact attribute value
[attribute~="value"]:
Selects elements where the value is one of a space-separated list
[attribute^="value"]:
Selects elements whose attribute value starts with a given value
[attribute$="value"]:
Selects elements whose attribute value ends with a given value
[attribute="value"]:*
Selects elements whose attribute value contains a given value
Key Point:
Useful for styling elements without adding extra classes or IDs
Commonly used with links, forms, and data attributes
Attribute selectors provide powerful targeting options
Improve flexibility and maintain cleaner HTML
Helpful for advanced CSS styling techniques





Summary Text (2)
 There are properties to control the choice of font, size, weight, style, and spacing.
There is a limited choice of fonts that you can assume most people will have installed.
If you want to use a wider range of typefaces there are several options, but you need to have the right license to use them.
You can control the space between lines of text, individual letters, and words. Text can also be aligned to the left, right, center, or justified. It can also be indented.
You can use pseudo-classes to change the style of an element when a user hovers over or clicks on text, or when they have visited a link.
