Color
Color plays an important role in making web pages visually appealing and engaging. CSS provides several ways to define and control colors.
Foreground Color
The color property in CSS is used to define the text color inside an element. It is one of the most basic and important styling properties.
CSS provides three common ways to define text color:
Color Names: Use predefined color names supported by browsers
Example:
h1 {
  color: DarkCyan;
}
Hex Codes: Six-digit codes representing red, green, and blue values, start with #.
Example:
h2 {
  color: #ee3e80;
}
RGB Values: Define colors using red, green, and blue intensity (0–255)
Example: 
p {
  color: rgb(100, 100, 90);
}

Background Color
The background-color property in CSS is used to set the background color of an element.
CSS treats each HTML element as a box, and this property defines the color behind that box.
Ways to Specify Background Color: 
RGB Values
body {
  background-color: rgb(200, 200, 200);
}
Color Names
h1 {
  background-color: DarkCyan;
}
Hex Codes
h2 {
  background-color: #ee3e80;
}
Important Notes:
If no background color is specified, the background is transparent.
By default, most browsers use a white background.
It is recommended to set a background color for the <body> to ensure consistency across browsers.
The padding property is often used with background color to create space between text and the edges of the box.
The background-color property helps improve visual design and readability by controlling the background of elements. It is commonly used together with text color and spacing for better UI design.



















Understanding Color
Every color on a computer screen is created by mixing red, green, and blue (RGB).
Each pixel on the screen displays a color based on different combinations of these three values.
When the screen is off → it is black (no light).
When the screen is on → pixels emit light to create colors.
Color Selection: 
You can use color picker tools (e.g., in Photoshop or GIMP) to choose colors.
These tools show:
RGB values
Hex codes
Ways to Represent Colors:
RGB Values:
Format: rgb(red, green, blue)
Each value ranges from 0 to 255
Hex Codes:
Format: #RRGGBB
Uses hexadecimal numbers (0–9, A–F)
Color Names: 
Predefined color names supported by browsers
Limited in number (~147 colors)
Color Terminology: 
Hue: 
The basic idea of a color (red, green, blue, etc.)
Saturation: 
The amount of gray in a color
High saturation → vivid color
Low saturation → more gray
Brightness (Value): 
How light or dark a color is
High brightness → lighter color
Low brightness → darker color
Understanding RGB, Hex, and color properties like hue, saturation, and brightness helps you choose better colors and design more visually effective web pages.
Contrast
When choosing foreground (text) and background colors, it is important to ensure there is enough contrast so the text is easy to read.
Levels of Contrast:
Low Contrast:
Text is hard to read
Problematic for:
People with visual impairments
Color blindness
Poor screens or bright environments
Should generally be avoided.
High Contrast:
Text is very easy to read
Best for:
Important content
Accessibility
However, too much contrast can be tiring for reading long text
Medium Contrast: 
Best for long paragraphs
Improves reading comfort
Additional Tip: 
If using light text on a dark background, improve readability by:
Increasing line spacing
Using slightly thicker fonts
Good contrast improves readability, accessibility, and user experience. Choosing the right contrast level is essential in web design.

CSS3: Opacity
CSS3 introduces ways to control transparency of elements using: opacity and rgba()
These help create modern visual effects such as overlays and layered designs.
Opacity Property:
Controls the transparency of an entire element
Value range: 0.0 → 1.0
0.0 → hoàn toàn trong suốt
1.0 → hoàn toàn mờ đục
Key Point:
Applies to the whole element, including text and children

RGBA Colors:
Similar to RGB, but adds an alpha (opacity) value
Format: rgba(red, green, blue, alpha)
Key Point:
Only affects the background color
Does NOT affect child elements or text
Conclusion:
Use opacity when you want to fade the entire element
Use rgba() when you only want to make the background transparent
Always consider fallbacks for better compatibility





CSS3: HSL Colors
CSS3 introduces a more intuitive way to define colors using:
Hue (H)
Saturation (S)
Lightness (L)
Hue (H):
Represents the type of color
Measured as an angle: 0° → 360°
0° → Red
120° → Green
240° → Blue
Saturation (S):
Represents the intensity of the color
Expressed as a percentage:
100% → full color (vivid)
0% → grayscale (no color)
Lightness (L):
Represents how light or dark the color is
Expressed as a percentage:
0% → black
50% → normal color
100% → white
Important Note: 
Lightness ≠ Brightness:
Lightness includes both white and black
Brightness mainly adds black
HSL provides a clearer and more flexible way to work with colors, especially useful for design and fine-tuning visual styles.


CSS3: HSL & HSLA 
CSS3 provides the HSL color model as an alternative to RGB, and HSLA adds transparency (alpha).
These models make it easier to understand and adjust colors:
HSL Format: 
hsl(hue, saturation, lightness)
Hue (H): color type (0°–360°)
Saturation (S): intensity (0%–100%)
Lightness (L): brightness (0%–100%)
HSLA Format: 
hsla(hue, saturation, lightness, alpha)
Adds alpha (A) → transparency
0 → fully transparent
1 → fully opaque
Conclusion: 
HSL makes color selection more intuitive
HSLA allows adding transparency
Always provide fallbacks for better compatibility
Summary Color
Color not only brings your site to life, but also helps convey the mood and evokes reactions.
There are three ways to specify colors in CSS: RGB values, hex codes, and color names.
Color pickers can help you find the color you want.
It is important to ensure that there is enough contrast between any text and the background color (otherwise people will not be able to read your content).
CSS3 has introduced an extra value for RGB colors to indicate opacity. It is known as RGBA.
CSS3 also allows you to specify colors as HSL values, with an optional opacity value. It is known as HSLA.
