# CSS Layout
## Key concepts in positioning elements
- **Building blocks**- CSS treats each element as if it is in its own box.  This box can either be:
  - **Block-level** boxes-  These start on  a new line and act as the main building blocks of any layout.
  - **Inline** boxes- These flow between surrounding text.  
- You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, also).  To separate boxes, you can use borders, margins, padding, and background colors.
- **Containing elements**- If one block-level element sits inside of another block-level element the outer box is known as the *containing* or *parent* element.  Its is common to group a number of elements together inside of a div (or other block-level) elements.  For ex, you might group together all elements that form the header of a site, such as the logo and main navigation.  The div would be known as the *containing* element.
- **Controlling the position of elements**- CSS has a number of **positioning schemes** that allow you to control the layout of a page:
  - Normal Flow-  *position:static*- Every element appears on a new line, causing each element to appear lower down the page then the previous one.  This is the browser default if no other positioning is set.
  - Relative Positioning- *position:relative*- This moves and element from the position it would be in normal flow, shifting it tot the top, right, bottom or left of where it would have been placed.  This will not affect the surrounding elements.
  - Absolute Positioning- *position:absolute*- This positions an element in relation to its containing element.  It is taking out of the normal flow, not affecting the surrounding elements.
  - Fixed Positioning- *position:fixed*- This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element.  These do not affect the other elements on the page and will not move when you scroll up or down a page.
  - Floating Elements- *float* Allows you to take an element out of normal flow and position it to the far left or right of a containing box.  These elements become block-level elements around which other content can flow.
    - You can use float to place elements side-by-side.  A lot of layouts place boxes next to each other.  
    - Parents that contain only floated elements may have their border collapse, to get around this you would add an additional child element and then set the clear property to have a value of both.
- When you move any element from normal flow, boxes can overlap.  The **z-index** property allows you to control which box appears on top, the element that appears later will appear on top.
- Different visitors to your site will have different sized screens that show different amounts of info, so your design needs to be able to work on a range of different sized screens.
- Resolution refers o the number of dots (pixels) a screen shows per inch.  Some devices have higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.  The higher the resolution the smaller the text will appear.  Many mobile devices have screens that are higher resolution than their desktop counterparts.
- Screen sizes vary so much, developers often will create pages of around 960-1000 pixels wide.  Which will allow most users to be able to see designs this wide on their screens.
- Fixed width layouts- These do not change size as the user increases or decreases the size of their browser window.  Generally given in pixels.
- Liquid layouts- These designs stretch and contract as the user increases or decreases hte size of the browser window.  Generally they use percentages.
  - Because liquid layouts can stretch the entire width of the browser, resulting in log lines of text that are hard to read, some liquid layouts only let part of the page expand and contract.
- **Layout Grids**- Composition in any visual art is the placement or arrangement of visual elements- how they are organized on a page.  Many designers use a grid structure to help them position items on a page, and the same is true for web designers. 
  - Grids set proportions and spaces to create a professional looking design.
  - Sets continuity between different pages which use different designs.
  - Helps the users predict where to find info on various pages.
  - Makes it easier to add new content to the site in a consistent way.
  - Helps people collaborate on design of a site in a consistent way. 
- **CSS Frameworks**- Aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages, etc.  You can also include CSS framework code in your projects rather that writing it from scratch.
  - Advantages- They save you from writing code for the same tasks. They will also have been tested across different browser versions, which will help avoid browser bugs.
  - Disadvantages- They often require that you use class names in your HTML code that only control the presentation of the page (rather than describe it content).  Also in order to satisfy a variety of needs, they often contain more code that you need for your particular web page (commonly referred to as code "bloat").