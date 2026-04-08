Forms
Forms are used to collect information from users on a website. They can be used for simple tasks like search boxes or more complex data collection.
Why Forms?
Forms are commonly used on websites to collect user input. Example : A common example is the search box on a website.
Forms allow users to perform actions such as searching, registering, shopping, or signing up.
They are widely used in many web applications to collect and process user data.
Forms Controls
HTML provides different types of form controls to collect user input.
Adding text : 
Text input: for single-line text (e.g. names, emails)
Password input: hides the entered characters
Text area: for multi-line text (e.g. comments)
Making choices:
Radio buttons: select one option
Checkboxes: select multiple options
Drop-down lists: choose one option from a list
Submitting forms:
Submit buttons: send form data
Image buttons: submit using an image
Uploading files:
File upload: allows users to upload files




How Forms Work
Forms send user input from the browser to the server.
Process : 
The user fills in a form and submits it
The browser sends the data to the server
The server processes the data (and may store it)
The server returns a response page
Name/Value pairs: Each form control sends data as a name/value pair.
Example : username=Ivy – vote=Herbie
How it works: 
The name identifies the form field
The value is the data entered or selected by the user
Form Structure
Forms are created using the <form> element.
<form> : Contains all form controls and usually includes action and method attributes.
Action attribute: specifies the URL where the form data is sent when submitted.
Method attribute: defines how data is sent: get or post.
GET method:
Appends data to the URL
Suitable for short forms or retrieving data
POST method:
Sends data in HTTP headers
Used for large data, file uploads, or sensitive information
Id attribute: used to uniquely identify the form or elements within it.




Text Input
The <input> element is used to create form controls.
Type="text": creates a single-line text input
Name attribute: identifies the form control and sends data to the server.
Maxlength attribute: limits the number of characters a user can enter.
Size attribute: specifies the visible width of the input (in characters), but is outdated and should be replaced by CSS.
Password Input
The <input> element with type="password" is used to create a password field.
Type="password": creates a text input where characters are hidden.
Name attribute: identifies the password field and sends its value to the server.
Size & Maxlength: control the width and maximum number of characters (similar to text input).
Text Area
The <textarea> element is used to create multi-line text input.
Unlike <input>, it has both opening and closing tags.
Text inside <textarea> appears as default content.
Cols attribute: specifies the width (in characters).
Rows attribute: specifies the height (number of lines).
Radio Button
The <input> element with type="radio" allows users to select one option from multiple choices.
type="radio": used when only one option can be selected.
Name attribute: all radio buttons in the same group share the same name.
Value attribute: specifies the value sent to the server for the selected option   
Checked attribute: sets the default selected option (only one per group).
Note: Once selected, a radio button cannot be unselected without choosing another option.
Checkbox
The <input> element with type="checkbox" allows users to select one or more options.
Type="checkbox": used when multiple options can be selected.
Name attribute: identifies the group of checkboxes and is sent with selected values.
Value attribute: specifies the value sent to the server when checked.
Checked attribute: sets the default selected checkbox.
Drop down List Box
The <select> element is used to create a drop-down list.
Allows users to select one option from a list.
<select> : Contains multiple <option> elements.
Name attribute: identifies the control and sends the selected value to the server.
<option> : defines each option in the list.
Value attribute: specifies the value sent to the server when selected.
Selected attribute: sets the default selected option.
Multiple Select Box
The <select> element can be modified to show multiple options.
Size attribute: specifies how many options are visible at once.
Multiple attribute: allows users to select more than one option.
File Input Box
The <input> element with type="file" allows users to upload files.
Type="file": creates a file selection box with a browse button.
Users can choose a file from their computer to upload.
The <form> must use method="post" to send files.
Submit Button
The <input> element with type="submit" is used to send form data to the server.
Type="submit": creates a button to submit the form.
Name attribute: optional, used to identify the button.
Value attribute: specifies the text displayed on the button.
Default button text may vary across browsers
Image Button
The <input> element with type="image" is used as a submit button with an image.
Type="image": creates a button using an image instead of text.
Attributes:
src: specifies the image source
width, height: set the image size
alt: provides alternative text
Button & Hidden Controls
HTML provides additional controls for buttons and hidden data.
<button> : allows more control over button appearance and can contain text or images.
Content is placed between <button> and </button> tags.
type="hidden": creates a hidden input that is not visible to users.\
Labelling Form Controls
When introducing form controls, the code was kept simple by indicating the purpose of each one in the text next to it. However, each form control should have its own <label> element as this makes the form accessible to vision-impaired users.
The <label> element can be used in two ways:
Wrap around both the text and the input
Separate label and input using “ for “ 
The for attribute states which form control the label belongs to : 
Its value must match the id of the input
The id must be unique on the page





Grouping Form Elements
<fieldset> : used to group related form controls together.
Helps organize long forms
Makes forms easier to understand
Browsers usually display a border around the group
<legend> : used to add a caption (title) for the <fieldset>
Placed right after <fieldset> opening tag
Describes the purpose of the group.
HTML5 : Form Validation
Form validation is the process of checking that a user has entered information correctly before it is sent to the server. 
Displays messages if input is incorrect
Ensures required fields are filled 
HTML5 introduces built-in validation, allowing browsers to handle it automatically.
Benefits of validation
Ensures correct data is sent to server
Reduces server workload
Helps users detect errors quickly
Improves user experience
The required attribute is used to indicate that a field must be filled in before submitting the form.
Notes : 
In HTML5: required can be written without value
In older HTML: required="required" is used
HTML5 : Date Input
<input>
Many forms need to collect information such as dates, emails, or URLs.
Traditionally, this was done using text inputs.
HTML5 introduces new input types to standardize data collection.
Easier for users to enter correct data
Better user experience
Supported by modern browsers
Type = “date”
The date type is used to allow users to select a date.
Creates a date picker (calendar)
Helps users input correct date format
Reduces input errors
HTML5 : Email & URL Input
<input> 
HTML5 introduces new input types for collecting specific data such as email addresses and URLs : 
Helps ensure correct data format
Improves user experience
Unsupported browsers will treat them as text inputs
Type = “email”
The email type is used to collect email addresses.
Browser checks correct email format
Shows error if invalid input
Mobile devices may show optimized keyboard (with @)
Type = “url” 
The url type is used to collect website addresses.
Browser validates URL format
Helps prevent incorrect input
Mobile keyboards may include shortcuts (e.g. “.com”)


HTML5 : Search Input
<input> 
HTML5 provides a special input type for search boxes : 
Used for search queries
Similar to a text input
Older browsers treat it as a normal text box
Type = “search”
The search type is used to create a single-line input for search.
Optimized for searching
May include extra UI features in modern browsers
Placeholder attribute
The placeholder attribute shows a hint inside the input box.
Disappears when user starts typing
Helps users understand what to enter
Summary
Whenever you want to collect information from visitors you will need a form, which lives inside a <form> element.
Information from a form is sent in name/value pairs.
Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.
HTML5 introduces new form elements which make it easier for visitors to fill in forms.
