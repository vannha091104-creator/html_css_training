Text
In this section, I've explored how to use markup language (tags) to structure and convey meaning to web page content. Markup language helps browsers understand how to display information correctly.
There are two main types of markup language:
Structural markup language : Used to define the structure of a web page, such as headings and paragraphs.
Semantic markup language : Used to provide additional meaning to content, such as emphasis, quotations, and abbreviations.
Overall, markup language plays a crucial role in making web pages clear, organized, and meaningful to both users and browsers.
Heading 
HTML has six “levels” of headings from <h1> to <h6>
<h1> is used for main headings
<h2> is used for subheadings
If there are further sections under the subheadings then the <h3> element is used, and so on…
Browsers display the contents of headings at different sizes. The contents of an <h1> element is the largest, and the contents of an <h6> element is the smallest
 Users can also adjust the size of text in their browser
Paragraphs
To create a paragraph, surround the words that make up the paragraph with the opening tag <p> and the closing tag </p>
By default, the browser will display each paragraph on a new line with a certain amount of space between it and any subsequent paragraph.


Bold & Italic
<b> : By enclosing words in the tags <b> and </b> we can make characters appear bold.
<i>  : By enclosing words in the tags <i> and </i> we can make characters appear italic.
Superscript & Subscript
<sup> : Is used to contain characters that need to be written as superscripts
<sub> : Is used to contain characters that need to be written as subscripts
Horizontal Rules
<br /> : Used to break a line in the middle of a paragraph
<hr /> : Used to add a horizontal line between sections, creating space between topics
Strong & Emphasis
<strong> : Used to bold the content within the tag. Emphasizes the importance of that content.
<em> : The <em> tag indicates emphasis and changes the meaning of the sentence. The browser will display the content of the <em> tag in italics.
Quotations
<blockquote> : Used to contain a long quotation (an entire paragraph). The content is still written inside using the <p> tag. The browser will display it differently.
<q> : Used for short quotations within a line/paragraph. The browser usually adds quotation marks to it automatically.
Abbreviations & Acronyms
<abbr> : Used as an abbreviation, and the 'title' attribute is used to specify the meaning of the word. HTML4 added <acronym>, but HTML5 only uses <abbr>.




Citations & Definitions
<cite> : Used to indicate the source of a work (book, film, research paper, etc.), and browsers usually display the content within the <cite> tag in italics.
<dfn> : Used to mark the first time a new term is defined. Often used for academic concepts or specialized terminology. Some browsers display the content in the <dfn> tag in italics (Safari and Chrome do not).
Author Details
<address> : Used to contain contact information for the author/website, which may include address, email, and phone number. Browsers usually display italicized.
Changes to Content 
<ins> : is used to mark added content; the content within the <ins> tag is usually underlined.
<del> : is used to mark deleted content; the content within the <del> tag is usually slashed.
<s> : is used when content is no longer correct/appropriate, but not deleted; the content within the <s> tag is usually slashed.
Summary Text
HTML elements are used to describe the structure of the page (e.g. headings, subheadings, paragraphs).
They also provide semantic information (e.g. where emphasis should be placed, the definition of any acronyms used, when given text is a quotation).
