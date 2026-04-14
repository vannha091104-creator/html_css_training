HTML5 Layout
HTML5 introduces new elements that help define the structure of a webpage more clearly. These elements play an important role in building layouts, especially when combined with CSS.
Traditional HTML Layouts
For a long time, developers used <div> elements to group related parts of a web page, such as header, article, footer, and sidebar. They used class or id attributes to indicate the role of each <div> in the page structure.
How it behaves :
A typical layout includes:
A header at the top (with logo and navigation)
One or more articles or main content sections
A sidebar (e.g., links, search, ads) usually on the side
A footer at the bottom
How it works :
To build this layout, developers:
Use <div> elements to wrap each section
Assign class or id to describe their purpose (e.g., header, nav, content, sidebar, footer)
Note : This method was widely used before HTML5, but it relies heavily on <div> elements and is less semantic compared to modern HTML5 layout elements.







New HTML5 Layout Elements
HTML5 introduces new elements that allow developers to divide a web page into meaningful parts. The names of these elements clearly describe the type of content they contain.
How it behaves :
The layout structure is similar to traditional layouts, but uses semantic elements such as:
<header> for the top section
<nav> for navigation
<article> for main content
<aside> for sidebar
<footer> for the bottom section
How it works :
Instead of using many <div> elements, developers use these new HTML5 elements to define each part of the page. Each element represents a specific role in the layout.
Benefits :
Makes the page structure more clear and meaningful (semantic)
Helps screen readers navigate content more easily
Allows search engines to better understand important content
Makes code easier to read and maintain
Note : Although these elements are still evolving, they are already widely used in modern web development.






Headers & Footers
The <header> and <footer> elements are used to define the top and bottom sections of a page or a section.
How it behaves :
<header> is usually placed at the top, containing the site name and navigation
<footer> is placed at the bottom, containing information like copyright, policies, or links
They can also be used inside each <article> or <section>
How it works :
<header> contains introductory content (e.g., title, logo, navigation)
<footer> contains additional information (e.g., copyright, terms, related links)
Each <article> or <section> can have its own <header> and <footer>
Example use :
On a blog page, each post can be treated as a separate section
<header> can contain the title and date of the post
<footer> can include sharing links or extra information
Note : These elements help organize content clearly and make the structure more semantic.








Navigation
The <nav> element is used to contain the main navigation blocks of a website.
How it behaves :
It usually includes the primary navigation menu (e.g., Home, About, Contact)
It helps users move between the main sections of the site
How it works :
<nav> wraps a list of links (commonly using <ul> and <li>)
It is used for major navigation blocks only
Note :
Links to related posts, footer links, or secondary links are not considered main navigation and should not be inside <nav>
Some developers also use <nav> for footer links (e.g., privacy policy, terms), but this is not always standard
Articles
The <article> element is used to define a self-contained section of a webpage that can stand alone.
How it behaves :
Represents independent content such as:
Blog posts
News articles
Comments or forum posts
Each article can be read and understood separately
How it works :
Each piece of independent content is placed inside its own <article> element
A page can contain multiple <article> elements
Special case :
<article> elements can be nested inside other <article> elements
For example, a blog post can be an <article>, and each comment inside it can also be its own <article>
Note : This element helps organize content clearly and improves semantic structure.
Asides
The <aside> element is used to contain content that is related to other content, with its purpose depending on its position.
How it behaves :
It can be used inside or outside an <article>
Its meaning changes based on where it is placed
How it works :
Inside an <article>:
Contains information related to that article but not essential to its main content
Example: pull quotes, glossary, related notes
Outside an <article>:
Contains content related to the entire page
Example: sidebar, links to other sections, recent posts, search box
Note : The <aside> element helps organize supporting content without affecting the main content.
Sections
The <section> element is used to group related content together, usually with its own heading.
How it behaves :
Each <section> represents a distinct part of a page
Commonly used on a homepage to divide content (e.g., news, products, newsletter)
How it works :
Groups related elements that share a common theme or purpose
Can contain multiple <article> elements
Can also be used to split a long article into smaller sections
Note :
<section> should not be used as a wrapper for the entire page (unless the page has only one main topic)
For general page containers, <div> is still more appropriate
Heading Groups
The <hgroup> element is used to group multiple heading elements (<h1> to <h6>) so they are treated as a single heading.
How it behaves :
Combines a main heading and a subheading into one group
Example: a title (<h2>) and a subtitle (<h3>)
How it works :
Wraps multiple heading elements inside <hgroup>
Helps organize headings that belong together
Note :
This element has had mixed support and opinions among developers
Some prefer using a <p> element for subtitles instead
It is mainly useful for grouping a main heading and its subheading
Figures
The <figure> element is used to contain content that is referenced from the main flow of a page.
How it behaves :
The content inside <figure> can be moved without affecting the meaning of the main article
It is used for supporting content, not essential content
How it works :
<figure> wraps related content such as: Images, videos, graphs, diagrams, code samples, supporting text
<figcaption> is used to provide a description or caption for the content inside <figure>
Note :
The main article should still make sense even if the <figure> is removed or moved
<figure> is often used inside an <article>
It is recommended to include a <figcaption> for better description


Sectioning Elements
Although HTML5 introduces new semantic elements, the <div> element is still important for structuring web pages.
How it behaves :
<div> is used to group related elements together
It is often used as a general container when no specific semantic element is suitable
How it works :
Developers use <div> to wrap sections of a page (e.g., as a main wrapper)
It should not replace semantic elements like <header>, <section>, <article>, etc.
When to use :
When there is no appropriate HTML5 element for the content
When creating a wrapper for the entire page layout
Note :
 <div> remains useful but should be used carefully
There is no <content> element in HTML5; content outside <header>, <footer>, and <aside> is considered the main content
Linking Around Block-Level Elements
HTML5 allows developers to wrap a block-level element inside an <a> tag, turning the entire block into a clickable link.
How it behaves :
An entire section (e.g., article, image, text) can act as a single link
Users can click anywhere in the block to navigate
How it works :
The <a> element wraps block-level elements such as <article>, <figure>, <hgroup>, etc. This creates a larger clickable area instead of just linking text
Note :
This is not a new element in HTML5, but a new way of using the <a> element
In earlier HTML versions, wrapping block-level elements inside <a> was not considered correct
Helping Older Browsers Understand
Older browsers may not recognize new HTML5 elements and will treat them as inline elements by default.
How it behaves :
HTML5 elements (e.g., <header>, <section>, <footer>, <aside>, <nav>, <article>, <figure>) may not display correctly in older browsers
They need to be defined as block-level elements
How it works : 
Use CSS to set these elements to display: block
This ensures proper layout in older browsers
Support for older IE :
Older versions of Internet Explorer (especially IE8 and below) do not support HTML5 elements
A JavaScript solution called HTML5 shiv (or shim) is used to enable support
Implementation :
Include the HTML5 shiv script inside a conditional comment for IE:
Only runs when the browser is less than IE9
The script allows styling of HTML5 elements in older browsers
Note :
This solution requires JavaScript to be enabled
Without JavaScript, older browsers may not display HTML5 elements correctly
Summary HTML5 Layout
The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure.
The new elements provide clearer code (compared with using multiple <div> elements).
Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements.
To make HTML5 elements work in Internet Explorer 8 (and older versions of IE), extra JavaScript is needed, which is available free from Google.
