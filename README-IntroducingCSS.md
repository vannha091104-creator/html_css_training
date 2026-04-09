Introducing CSS
CSS (Cascading Style Sheets) is used to control the appearance and layout of web pages.
It allows you to define how HTML elements should be displayed.
Understanding CSS : Thinking Inside the Box
The key concept of CSS is that every HTML element is treated as a box.
These boxes are invisible by default but can be styled using CSS.
Each HTML element (e.g., <body>, <h1>, <p>) creates its own box
Boxes can contain other boxes (nested structure)
CSS controls how each box is displayed
Block vs Inline Elements
Block Elements:
Start on a new line
Take full width
Examples: <h1>, <p>, <div>
Inline Elements:
Stay on the same line
Only take needed space
Examples: <a>, <span>, <img>, <em>
What CSS Can Control: 
Box Properties
Width and height
Borders (color, width, style)
Background (color, image)
Position
Text Properties
Font (typeface)
Size
Color
Style (italic, bold, uppercase)
CSS creates rules to control how each box and its content are displayed.
CSS Associates style Rules with HTML Elements
CSS works by linking style rules to HTML elements.
These rules control how content is displayed on a web page.
A CSS rule has two main parts:
p {
  font-family: Arial;
}
Selector: p → targets HTML elements
Specifies which elements the rule applies to
Can target multiple elements using commas
Declaration: font-family: Arial; → defines the style
Defines how elements are styled
Consists of: Property (e.g., color) and Value (e.g., blue)
Written as: property: value;









CSS Properties Affect how Elements are displayed
CSS controls how elements appear using properties and values.
Each declaration defines specific styles for HTML elements.
Structure of Declarations:
h1, h2, h3 {
  font-family: Arial;
  color: yellow;
}
Multiple properties can be included
Each property is separated by a semicolon ;
Property: Defines what you want to change
Value: Specifies the setting for that property
Format : property: value;
You can apply the same styles to multiple elements:
h1, h2, h3 {
  color: yellow;
}





Using External Css
External CSS allows you to separate the design (CSS) from the structure (HTML).
It helps keep code clean, reusable, and easier to maintain.
The <link> element is used inside the <head> section to connect an HTML page to a CSS file. It is an empty element (no closing tag).
Syntax: <link href="css/styles.css" type="text/css" rel="stylesheet">
Key Attributes:
href: Defines the type of document (usually text/css).
rel: Describes the relationship between HTML and CSS 
type: Defines the type of document (usually text/css).
Advantages: 
Keeps HTML clean and organized
Allows reuse across multiple pages
Makes maintenance easier
Enables consistent design across a website
Using Internal Css
Internal CSS allows you to define styles directly inside an HTML page using the <style> element.
The <style> element is placed inside the <head> section.
It contains CSS rules that apply only to that specific page.
Key points:
The type="text/css" attribute specifies that the content is CSS.
CSS rules inside <style> follow the standard format: 
selector + declaration (property + value)
Easy to use for small or single-page websites
No need to create a separate CSS file
Not reusable across multiple pages
Harder to maintain for large websites
Repeats code if used on many pages
CSS Selectors
CSS selectors are used to target specific HTML elements so that styles can be applied to them. They define which elements a CSS rule affects.
Key Points:
There are many types of selectors for different purposes.
Selectors must be case-sensitive → they must match HTML exactly.
Some selectors are simple, while others are more advanced (based on attributes or relationships).
Common Types of Selectors: 
Element selector → targets HTML tags. Example: p, h1
Class selector → targets elements with a class. Example: .menu
ID selector → targets a specific element. Example: #header
Descendant selector → targets elements inside another. Example: div p
Child selector → targets direct children. Example: div > p
Sibling selectors → target elements next to others. Example: h1 + p, h1 ~ p
Advanced selectors can target elements based on attributes and values.
Some selectors (like sibling selectors) were supported later (e.g., from Internet Explorer 7), so they are less commonly used in older code.
How CSS Rules Cascade
When multiple CSS rules apply to the same HTML element, the browser decides which rule to use based on three main principles:
Last Rule (Order): If two selectors have the same specificity, the last rule written in the CSS will be applied.
Specificity: More specific selectors override less specific ones.
!important: The !important rule overrides all other rules, regardless of order or specificity.



Inheritance
Inheritance in CSS means that some properties applied to a parent element are automatically passed down to its child elements. This helps reduce repetition and keeps stylesheets simpler.
When you set properties like font-family or color on the <body> element, they are inherited by most child elements.
This allows you to define common styles once instead of repeating them for each element.
Using inherit Value: You can force an element to inherit a property using:
padding: inherit;
This makes the element take the same value as its parent.
Benefits: 
Reduces duplicated CSS code
Makes stylesheets cleaner and easier to maintain
Ensures consistent styling across elements
