Images
Images are used in web pages to display content such as logos, photos, illustrations, and charts, making the interface more visually appealing and professional. When using images, it is important to choose the appropriate format, size, and optimize them to ensure faster page loading. HTML provides elements to effectively embed and display images on a webpage.
Choosing Images for your Site
Images can make a website more engaging and visually appealing.
Images help set the tone of a site and communicate information quickly.
Most images are subject to copyright, so using images from other websites without permission can cause legal issues.
If you do not have your own images, you can use stock photo websites.
Images should be relevant, convey information, and fit the overall design and color palette.
Storing Images on your Site
Images should be stored in an organized way within a website.
All images are usually stored in a separate folder (commonly named images) to keep files organized.
Images can be grouped into subfolders based on their purpose, such as interface, products, or news.
If using a CMS or blogging platform, there are built-in tools to upload and manage images, and they are often stored in dedicated folders automatically.
Adding Images
Images are added to a web page using the <img> element.
<img> : The <img> tag is an empty element (no closing tag) and must include required attributes.
“ src “ : Chỉ định đường dẫn đến tệp hình ảnh, thường là URL tương đối.
“ alt “ : Provides a text description of the image if it cannot be displayed. It is important for accessibility and search engines.
“ title “ : Adds additional information about the image and is displayed as a tooltip when the user hovers over it.
Height & Width of Images
The size of an image can be specified using attributes in the <img> element.
“ height “ : Defines the height of the image in pixels.
“ width “ : Defines the width of the image in pixels.
Where to place Images in your Code
The position of an image in the code affects how it is displayed on the webpage.
The image appears before the paragraph, and the text starts on a new line after the image.
The image is placed at the beginning, and the text aligns next to it.
The image is inserted between words, and the text flows around it.
Block elements.
Block elements (e.g., <p>, <h1>) always start on a new line. If an image is followed by a block element, the content appears below the image.
Inline elements:
Inline elements (e.g., <img>) do not start on a new line. When placed inside text, content flows around the image.
Old Code : Aligning Images Horizontally
Images can be aligned to control how text flows around them.
align = “left” : The image is placed on the left, and the text flows around it on the right.
align = “right” : The image is placed on the right, and the text flows around it on the left.
Proper alignment makes the layout look neater than simply placing the text on one side.
Old Code : Aligning Images Vertically
Images can be vertically aligned with text using different values.
align = “top”: Aligns the first line of text to the top of the image.
align = “center” : Aligns the first line of text to the center of the image.
align = “bottom” : Aligns the first line of text to the bottom of the image.
The align (left/right) property was used in older HTML but is now outdated and should be replaced with CSS.
Three Rules for Creating Images
There are three important rules when creating images for a website.
Choose the Right Format : Common formats include JPEG, GIF, and PNG. Using the wrong format can reduce image quality and slow down the website.
Use the Right Size : Images should be saved at the correct size they display on the website to avoid distortion or slow loading.
Use the Correct Resolution : Web images are typically displayed at a resolution of 72 pixels per inch. Higher resolution images will increase file size and load times unnecessarily.
Tools to edit & save Images
There are many different tools available for editing and saving images for web use.
These tools help ensure images have the correct size, format, and resolution.
Adobe Photoshop is widely used by professionals for image editing.
Alternatives include Fireworks, Pixelmator, PaintShop Pro.
Several tools are available online, allowing users to edit images without installing software.
Image Dimensions
Images should be saved at the same size they appear on the website.
Setting the correct width and height ensures images display properly without distortion.
Making an image smaller reduces file size and improves loading speed.
Enlarging a small image reduces quality and can make it look blurry or pixelated.
Images can be cropped to change shape, but important content may be lost.


Cropping Images
When cropping images it is important not to lose valuable information. It is best to source images that are the correct shape if possible.
Image Resolution
Image resolution affects both quality and file size.
Images for websites should be saved at 72 pixels per inch (ppi).
Higher resolution increases file size without improving quality on web displays.
Web images are made of pixels, while print images use dots and usually have higher resolution (e.g., 300 dpi).
Using high-resolution images on websites increases loading time and reduces performance.
Vector Images
Vector images are different from bitmap images and are resolution-independent.
They are made by placing points on a grid and connecting them with lines, which can be filled with color.
Vector images are often used for logos, illustrations, and diagrams.
They can be resized without losing quality.
Vector images are often converted to bitmap format for web use, but SVG is a newer format that allows vector images to be displayed directly.
Animated Gifs
Animated GIFs use multiple frames to create simple animations.
They display a sequence of images, such as a loading animation.
They can be created using software like Photoshop or online tools.
More frames increase file size and loading time.
GIFs are not suitable for photographs and work best for simple graphics.
Overusing animated GIFs can make a website look unprofessional.


Transparency
Transparency allows parts of an image to be see-through.
Transparent GIF: Used when transparency has straight edges and is fully transparent (no semi-transparency).
PNG: Used for more complex transparency, such as rounded edges, semi-transparent areas, or shadows.
Transparent PNGs may not be fully supported in older browsers like Internet Explorer 6.
Examining Images on the Web
You can check and download images directly from a website.
Image size can be viewed by right-clicking the image and selecting options from the menu (varies by browser).
Images can be downloaded using options like “Save Image As” from the same menu.
Different browsers provide different options to view size and download images.
Images on websites are usually protected by copyright and require permission to reuse.
HTML5 : Figure and Figure Caption
HTML5 cung cấp các phần tử để nhóm hình ảnh với chú thích.
<figure> : Used to contain images and their related content, such as captions.
A <figure> element can include more than one image if they share the same caption.
<figcaption> : Used to add a caption describing the image.
These elements help clearly associate an image with its caption.
Older browsers may not support these elements but will still display the content.
Summary Images
The <img> element is used to add images to a web page.
You must always specify a src attribute to indicate the source of an image and an alt attribute to describe the content of an image.
You should save images at the size you will be using them on the web page and in the appropriate format.
Photographs are best saved as JPEGs; illustrations or logos that use flat colors are better saved as GIFs.
