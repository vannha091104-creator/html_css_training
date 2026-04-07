Tables
Tables are used to display data in a grid format; they help organize complex information using rows and columns.
Basic Table Structure
HTML provides elements to create and structure tables.
<table> : Used to create a table, with content written row by row.
<tr> : Defines a table row and contains one or more cells.
<td> : Represents a table cell that holds data.
Table  Heading
The <th> element is used to define table headings.
It represents headings for rows or columns.
It works similarly to <td> but is used for header cells.
Even empty cells should include <td> or <th> to ensure proper table display.
Using <th> improves accessibility, SEO, and allows better styling with CSS.
Browsers usually show <th> content in bold and centered.
Spanning Columns
Table cells can span across multiple columns.
Colspan attribute used in <td> or <th> to specify how many columns a cell should cover.
When a cell spans multiple columns, fewer cells are needed in that row.
Example: A cell with colspan="2" will extend across two columns.
Spanning Rows
Table cells can span across multiple rows.
Rowspan attribute: used in <td> or <th> to specify how many rows a cell should cover.
When a cell spans multiple rows, fewer cells are needed in the rows below.
Example: A cell with rowspan="2" will extend across two rows.
Long Tables
HTML provides elements to structure different parts of a table.
<thead> : Contains the table headings.
<tbody> : Contains the main content of the table.
<tfoot> : Contains the footer of the table.
These elements improve accessibility and allow different styling with CSS.
Old Code : Width & Spacing
Some table attributes are outdated and replaced by CSS.
Width attribute : used to set the width of the table or individual cells in pixels.
Cellpadding attribute : adds space inside each table cell.
Cellspacing attribute : adds space between table cells.
These attributes are no longer recommended and should be replaced by CSS.
Old Code : Border & Background
Some table attributes for styling are now outdated.
Border attribute : used to set the width of table borders in pixels.
Bgcolor attribute : used to set the background color of a table or its cells.
These attributes are no longer recommended and should be replaced by CSS.
Summary Tables
The <table> element is used to add tables to a web page.

A table is drawn out row by row. Each row is created with the <tr> element.
Inside each row there are a number of cells represented by the <td> element (or <th> if it is a header).
You can make cells of a table span more than one row or column using the rowspan and colspan attributes.
For long tables you can split the table into a <thead>,<tbody>, and <tfoot>.
