# HTML 
## Forms
- Forms are used whenever you would want to collect info from visitors, in HTML they live inside a <form> element.
- They allow users to search (Google is probably the most well know form on the web), they also are used to register as a member of a website, when shopping online, and when signing up for newsletters and mailing lists.
- Info from a form is sent in a name/value pairs.
- *Form Controls* there are several used to collect info on the web:
1. Adding text- text inputs, password input, text area(like comment section).
1. Making choice- Radio buttons, checkboxes, drop down boxes.
1. Submitting forms- the submit button, image buttons, upload or browse buttons.
- Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.
- The form element always carries the action attribute and its value is the URL for the page on the server that will receive the information in the form when it is submitted.  The form element will also often carry the methods attribute which is the way the form can be sent, it can have 2 values: get or post.  It can also have the id attribute, which is often referenced by the scripts, can also be use to identify the distinctly from other elements on the page.
- The input element is used to create several different form controls.  The value of the type attribute determines what kind of input they will be creating. the attributes of the input include:
  - type="text" it creates a single line text input.
    - name- tells the server which control each piece of data was entered into
    - maxlength- this can be used to limit the number of characters that the user can enter into the form.
    - size- this one is no longer really sed.
  - type="password"- will act as a text box, except the characters will be blocked out.

# CSS
## List, Tables and Forms
- There are several CSS properties that are specifically used to control the appearance of lists, tables and forms.
- List markers (bullet point styles) can be given different appearances using the list-style-type (discs, circles, squares for unordered lists, and for ordered lists decimal, decimal leading zero, lower-alpha, upper-alpha, lower-roman numeral, upper-roman numeral)and list-style image properties. You can also choose the position of the marker.
- Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.
- It is a good idea to make forms more visually appealing to the user, they are then more likely to fill them in.
- Forms are easier to use if the form controls are vertically aligned using CSS.  Nice to use the float to give more space in between features.
- Forms benefit from styles that make them feel more interactive.
- You can style text inputs, submit buttons, fieldset' and legends.
- Can change he style of the cursor when it hovers over a feature, or just on your page.

# JavaScript
## Events
- *Events* are the browser's way of indicating when something has happened (such as when a page has finished loading or a button has been clicked).
- How events trigger JS code:
1. Select- Select the elements node(s) you want the script to respond to.
1. Specify- Indicate which event on the selected node(s) will trigger the response.
1. Call Code- State the code you want to run when the event occurs.
- *Binding* is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon.  3 ways to bind an event to an element:
1. HTML event handlers- this is considered bad practice, not to be used.
1. Traditional DOM event handlers- let you separate the JS from the HTML.
1. DOM level 2 event listeners- These are the newest and also the preferred way of handling events.

- When and event occurs on an element, it can trigger a JS function.  When this function then changes the web page in some way, it feels interactive because it has responded tot the user.
- You can use event delegation to monitor for events that happen on all of the children of an element.
- The most commonly used events are W3C DOM events.
