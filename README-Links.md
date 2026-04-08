Links
Links are the defining feature of the web because they allow you to move from one web page to another — enabling the very idea of browsing or surfing.
Writing Links 
Links are created using the <a> element. Users can click on anything between the opening <a> tag and the closing </a> tag. You specify which page you want to link to using the href attribute
<a href=”http://www.imdb.com”>IMDB</a>
Link text is the content between the <a> and </a> tags, and is what the user clicks on
It should clearly describe the content of the landing page, avoiding vague terms like "click here"
This helps users find information more easily and improves the user experience
Linking to other Sites
The <a> tag is used to create links in HTML. The href attribute specifies the destination page of the link
The content between <a> and </a> is the part that the user can click on. When the user clicks, the browser will go to the URL in the href
A URL is the address of a webpage. When linking to another website, use an absolute URL (Uniform Resource Locator)

Linking to other Pages on the same Site.
When linking within the same website, you don’t need a domain
Use relative URL
If they are in the same directory, use only the filename for the href. If they are in different directories, use a relative path
Relative URL make links shorter and easier to manage when the website has many pages


Directory Structure
Directory structure helps organize files on a website
Websites are often divided into different folders, making file management easier in large projects
Pages can be linked using relative paths; understanding file locations is essential for writing the correct paths
The root directory usually contains the index.html file. Other files (images, CSS, JS) should be placed in separate folders
A clear structure makes the code easier to read and maintain
Relative URLS
Relative paths are used to link between pages within the same website
There's no need to include the domain (e.g., https://...), just specify the file's location relative to the current page
This helps to write shorter code, makes it easier to use when developing web applications on a local machine, and avoids repeating the domain multiple times
Relative link types : 
Same Folder : When the target file is in the same directory, only the file name is needed. EX : reviews.html
Child Folder : When linking to a file inside a subfolder, include the folder name followed by the file name. EX : music/listings.html
Grandchild Folder : For deeper folder structures, include multiple folder levels. EX : movies/dvd/reviews.html
Parent Folder : To move up one directory level, use ../ before the file name. EX : ../index.html
Grandparent Folder : To move up two levels, use ../../. EX : ../../index.html




Opening Links in a New Window
To open a link in a new window, use the target attribute with the value _blank inside the opening <a> tag.
This is commonly used when linking to external websites. It allows users to view another site without leaving the current page, so they can easily return afterward.
Generally, opening links in a new window should be avoided because it may affect user experience. However, if it is used, you should clearly inform users before they click the link.
target="_blank" opens the link in a new tab or window depending on the browser. Always consider user experience when deciding to use this feature.
Linking to a specific part of the Same Page
On long web pages, you may want to create a list of contents at the top that links to different sections below. You can also add a link to return to the top of the page, helping users avoid scrolling.
Before linking to a specific part of a page, you need to identify that section using the id attribute. The id can be added to any HTML element and must be unique within the page.
ID Rules : 
Must start with a letter or underscore (_)
Cannot start with a number or special character
Must be unique (no duplicate values on the same page)
To create a link to a specific section, use the <a> tag with the href attribute starting with #, followed by the id value.
How it works : 
#arc_shot → jumps to the element with id="arc_shot"
#top → jumps to the top section of the page



Linking to a specific part of the Another Page
You can link to a specific part of a different page by using the id attribute defined on that page. This works for both internal pages (same website) and external websites.
The target page must contain an element with the corresponding id. If the id does not exist, the link will not jump to any specific section.
How it behaves : The browser first opens the target page, then automatically scrolls to the element with the matching id
How it works : To create this type of link, the href attribute must include:
The page URL (absolute or relative)
The # symbol and the value of the id attribute
Summary Links
Links are created using the element
The element uses the href attribute to indicate the page you are linking to
 If you are linking to a page within your own site, it is best to use relative links rather than qualified URLs
You can create links to open email programs with an email address in the "to" field
You can use the id attribute to target elements within a page that can 

