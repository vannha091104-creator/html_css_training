Images(2)
Control image size and alignment using CSS instead of HTML. Keeps presentation rules separate from content.
Controlling Sizes of Image in CSS
Concept:
Use CSS width and height to control image sizes.
Keeps layout consistent and faster to load.
How to use:
HTML:
<img src="image-large.jpg" class="large" />
<img src="image-medium.jpg" class="medium" />
<img src="image-small.jpg" class="small" />
CSS:
img.large {
 width: 500px; height: 500px;
}
img.medium {
 width: 250px; height: 250px;
}
img.small {
 width: 100px; height: 100px;
}

Key idea:
Define common image sizes used across the site
Assign them as class names (small, medium, large)
Why it matters:
Browser can reserve space before image loads
Improves page performance
Keeps design consistent
Remember:
 CSS controls image dimensions
 Use classes for reusable sizes














Aligning Images Using CSS
Images can be aligned using CSS (instead of HTML attributes) to control layout and allow text to wrap around them.
Key Points
Use the float property to move images left or right.
Text will automatically wrap around floated images.
Alignment is usually handled with CSS classes.
Common Methods
Float left
img.align-left {  float: left; margin-right: 10px; }
Float left
img.align-right { float: right; margin-left: 10px; }
Image Size Example
img.medium { width: 250px; height: 250px; }
Usage in HTML
<img src="image.jpg" class="align-left medium" alt="Image" />
<img src="image.jpg" class="align-right medium" alt="Image" />
Notes
Add margin to prevent text from touching the image.
Combine alignment + size classes for flexible design.
Using CSS keeps presentation separate from HTML structure.





Centering Images Using CSS
Images are inline by default, so to center them, you must convert them to block-level elements and apply alignment techniques.
Key Point:
Use display: block to make the image behave like a block element
Center images horizontally using margin auto or text-align.
Works best when the image has a defined width.
Common Methods
Using margin (most common)
img.align-center {display: block; margin: 0 auto;}
Using text-algin on parent
.container {text-align: center;}


Image Size Example
img.medium { width: 250px;  height: 250px; }
Usage in HTML
<img src="image.jpg" class="align-center medium" alt="Image" />
Notes
margin: 0 auto only works on block elements.
Always define width for proper centering.
Can be reused for other elements (div, video, etc.).





Background Images
The background-image property allows you to place an image behind an HTML element (or the whole page). By default, the image repeats (tiles) to fill the area.
Basic Usage
Apply to the whole page
body { background-image: url("images/pattern.gif"); }
Apply to a specific element
p {  background-image: url("images/pattern.gif"); }
Key Points
Image path is written inside url().
Background images repeat by default.
Can be applied to any HTML element.
Notes
Background images are usually decorative, not content.
Large images can slow down page loading.
Often used for patterns, textures, or visual effects.









Repeating Images
These properties control how a background image repeats and whether it scrolls or stays fixed on the page.
background-repeat Values
body {background-image: url("images/header.gif");background-repeat: repeat-x; }
repeat → repeats both horizontally & vertically (default)
repeat-x → repeats horizontally only
repeat-y → repeats vertically only
no-repeat → shows image once
background-attachment Values
body { 
   background-image: url("images/tulip.gif"); 
   background-repeat: no-repeat;
   background-attachment: fixed;
}
fixed → image stays in place when scrolling
scroll → image moves with the page (default)
Key Points
Combine both properties for better control.
Useful for headers, patterns, or full-page backgrounds.
fixed can create a parallax-like effect.
Notes
Avoid large images to improve performance.
Use no-repeat for logos or single images.
Combine with background-position for precise placement.

Background Position
The background-position property specifies where a background image is placed inside an element (especially when it is not repeated).
Basic Usage
body { background-image: url("images/tulip.gif");background-repeat: no-repeat;  background-position: center top; }
Common Position Values
left top, left center, left bottom
center top, center center, center bottom
right top, right center, right bottom
Using Percentages
body {  background-image: url("images/tulip.gif"); background-repeat: no-repeat; background-position: 50% 50%; }
First value → horizontal position
Second value → vertical position
50% 50% → perfectly centered
Key Points
Accepts keywords, percentages, or pixel values.
If only one value is given → second defaults to center.
Works best with no-repeat.
Notes
(0% 0%) = top-left corner
Pixels/percentages measure distance from top-left
Useful for precise placement of background images




Shorthand
The background property is a shorthand that combines multiple background properties into one line.
Basic Usage
body { background: #ffffff url("images/tulip.gif") no-repeat top right; }
Order of Values
You can include these properties (in order):
background-color
background-image
background-repeat
background-attachment
background-position
You can omit any value you don’t need.
Multiple Backgrounds (CSS3)
div {
  background:
    url("image1.jpg") top left no-repeat,
    url("image2.jpg") bottom left no-repeat,
    url("image3.jpg") center top repeat-x;
}
First image → on top
Last image → at the bottom
Key Points
Saves time and keeps CSS cleaner
Default values are used for omitted properties
Supports multiple background images
Notes
Not all older browsers fully support multiple backgrounds
Use shorthand carefully to avoid overriding values unintentionally

Image Rollovers & Sprites
Image rollovers change the appearance of a button or link when users hover or click. This is often done using a single image (sprite) that contains multiple states.
Basic HTML
<a class="button" id="add-to-basket">Add to basket</a>
<a class="button" id="framing-options">Framing options</a>
CSS Example
a.button {
   height: 36px;
   background-image: url("images/button-sprite.jpg"); 
   text-indent: -9999px; 
   display: inline-block; 
}
#add-to-basket {
  width: 174px;  background-position: 0px 0px; }
#framing-options {
  width: 210px;   background-position: -175px 0px; }
Hover & Active States
#add-to-basket:hover {
  background-position: 0px -40px; }
#add-to-basket:active {
  background-position: 0px -80px; }


Key Points
Sprite = one image containing multiple button states
Use background-position to show different parts
:hover → when mouse is over
:active → when clicked
text-indent: -9999px hides text visually
Advantages
Faster loading (only one image request)
Consistent design for UI elements
Smooth hover effects without extra files
Notes
Use display: inline-block to control size of links
Works best for buttons, icons, navigation
Touch devices may not support :hover










CSS3: Gradients
CSS3 allows you to create gradients (smooth color transitions) using the background-image property instead of image files.
Basic Usage (Linear Gradient)
#gradient {
  background-image: linear-gradient(#336666, #66cccc);
}
With Fallback (Older Browsers)
#gradient {
  background-color: #66cccc; /* fallback color */
  background-image: url("images/fallback-image.png"); /* fallback image */
  background-image: linear-gradient(#336666, #66cccc);
}
Key Points
Gradients are created using two or more colors
Defined inside background-image
No need for extra image files
Can specify direction or angle
Notes
Older browsers may require vendor prefixes (-webkit-, -moz-)
Fallbacks ensure compatibility
Supports other types like radial gradients (less commonly used)


Contrast of Background Images
Contrast plays an important role when placing text on top of background images. If the contrast is not handled properly, the text can become difficult or even impossible to read.
High Contrast
A high contrast background image contains strong differences between light and dark areas.
This makes overlaid text hard to read because the text blends with parts of the image.
Most photographs naturally have high contrast, which is why they are not always suitable as backgrounds.
Low Contrast
A low contrast background image has more subtle differences in tones.
This allows text to stand out more clearly and improves readability.
Designers often reduce contrast using tools like Photoshop or GIMP before using images as backgrounds.
Screen
When using a high contrast image, you can improve readability by adding a semi-transparent layer (often called a “screen”) behind the text.
This layer reduces the visual intensity of the image in that area.
It helps the text become clearer without needing to change the original image.
Summary
High contrast → visually strong but harder for text readability
Low contrast → better for readable text overlays
Screen overlay → a practical solution when you must use high contrast images





Summary Images (2)
You can specify the dimensions of images using CSS. This is very helpful when you use the same sized images on several pages of your site.
Images can be aligned both horizontally and vertically using CSS.
You can use a background image behind the box created by any element on a page.  
Background images can appear just once or be repeated across the background of the box.
You can create image rollover effects by moving the background position of an image.
To reduce the number of images your browser has to load, you can create image
