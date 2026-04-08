Extra Markup
This chapter covers additional HTML features that do not belong to a specific group but are still very important in web development.
The Evolution of HTML
Since the web was first created, there have been several different versions of HTML.
Each version improves the previous one. 
Adds new features and fixes limitations.
HTML 4 (Released 1997)
Widely used version of HTML
Focused on structure and basic layout
Most features are still supported today
XHTML 1.0 (Released 2000)
Based on XML (Extensible Markup Language)
Stricter rules than HTML
Key characteristics:
Tags must be properly closed
Elements must be nested correctly
Lowercase tags required
HTML5 (Latest version)
Modern standard for web development
Supports multimedia (audio, video)
Introduces new elements and form controls
New features:
<video>, <audio>
New form inputs (email, date, search…)
Better semantics (<header>, <footer>…)
Summary : 
HTML5 (Latest version)
HTML has evolved over time
DOCTYPE ensures browser compatibility

DOCTYPES
A DOCTYPE declaration is used at the beginning of a web page to tell the browser which version of HTML is being used.
Helps browsers render the page correctly according to the specified HTML version.
Placed at the very top of the HTML document.
Comments in HTML
Comments are used to add notes in the code that are not visible in the browser.
Syntax: : <!-- comment goes here -->
Purpose:
Helps developers understand the code more easily
Makes it easier to maintain and update code later
Allows multiple developers to collaborate effectively
Usage : 
Can be added anywhere in the HTML document
Often used to mark sections of code (start/end of parts)
Can temporarily disable code by commenting it out










ID Attribute
The id attribute is used to uniquely identify an HTML element on a page.
Purpose:
Identifies a specific element uniquely
Allows styling with CSS
Helps JavaScript interact with that element
Syntax: <tag id="uniqueName">Content</tag>
Rules : 
Each id must be unique within a page
Cannot be used more than once
Should start with a letter or underscore (_)
Should not start with a number
Usage: used in CSS to apply specific styles.
            #pullquote {
                text-transform: uppercase;
            }
Class Attribute
The class attribute is used to identify one or more HTML elements as belonging to a group.
Purpose:
Groups multiple elements together
Applies the same CSS styles to many elements
Helps organize and structure web pages
Syntax : <tag class="className">Content</tag>
Usage : used in CSS to style multiple elements
.important {
  text-transform: uppercase;
}
Block Elements
Block-level elements are HTML elements that always start on a new line in the browser.
Purpose:
Structure the layout of a web page
Separate content into distinct sections
Characteristics:
Always begin on a new line
Take up the full width available
Stack vertically (one below another)
Common Block Elements:
<h1> to <h6>
<p>
<ul>, <li>
Inline Elements
Inline elements are HTML elements that appear on the same line as surrounding elements.
Purpose:
Format small parts of content within a line
Do not break the flow of text
Characteristics:
Do not start on a new line
Only take up as much width as necessary
Appear side by side with other elements
Common Inline Elements:
<a>, <b>
<em>, <img>



Grouping Text & Elements in a Block
The <div> element is used to group a set of elements together in a block-level container.
Purpose:
Groups related elements into one block
Helps structure and organize web page layout
Used with CSS to style sections of a page
Syntax: 
                <div>
                   Content here
                 </div>
Characteristics:
Is a block-level element
Starts on a new line
Does not affect appearance by itself
Usage : combine with id or class for styling.
              #header {
                 background-color: gray;
              }






Grouping Text & Elements Inline
The <span> element is used to group inline elements or a section of text.
Purpose:
Groups small parts of text within a line
Allows styling specific text using CSS
Acts as an inline container
Syntax : <span>Content</span>
Characteristics:
Is an inline element
Does not start on a new line
Does not affect appearance by default
Usage: Often used with class or id for styling
             .gallery {
                 color: red;
               }
Iframes
<iframe> : used to embed another HTML page inside the current web page.
Purpose : 
Displays external or internal web pages within a page
Commonly used to embed maps, videos, or other content
Syntax : <iframe src="URL"></iframe>
Key Attributes:
“src” : Specifies the URL of the page to display
“width & height” :  Define the size of the iframe (in pixels)
“scrolling” : Controls scrollbars inside the iframe
“frameborder” : Defines whether the iframe has a border
“seamless” : Makes iframe appear as part of the page (no visible separation)

Information about Your Pages
HTML provides the <meta> element to store information about a web page.
<meta> : Used inside the <head> section to provide metadata about the page (not visible to users).
Common Attributes:
name + content : used together to define information about the page.
Types of Meta Data:
description : describes the content of the page
keywords : contains keywords related to the page
robots : controls whether search engines index the page.
http-equiv : used to simulate HTTP headers.
author : specifies the author of the page.
pragma : prevents browser caching.
expires : sets an expiration date for the page cache.
Used to help search engines, browsers, and systems understand the web page.
Summary Extra Markup
DOCTYPES tell browsers which version of HTML you are using.
You can add comments to your code between the <!-- and --> markers.
The id and class attributes allow you to identify particular elements.
The <div> and <span> elements allow you to group block-level and inline elements
<iframes> cut windows into your web pages through which other pages can be displayed.
The <meta> tag allows you to supply all kinds of information about your web page.
Escape characters are used to include special characters in your pages such as <, >, and ©.
