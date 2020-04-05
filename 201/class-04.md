# Pair Programming
Pair programming is a common technique used by many companies.  It is the practice of two developers working together on a coding task at one time, sharing a workstation and collaborating on a common goal.  It is key to foster a collaborative environment to learn and solidify topics that are necessary in the industry. 
- It commonly involves two roles:
1. Driver- the only one who actually types out the code.  They handle the mechanics of the coding.
1. Navigator- their role is to think of the big picture, using their words to guide the driver and not providing any direct input into the computer itself.  They rely what comes next, scan for typos or bugs.  They can also utilize their computer to look up solutions and documentation, but should not be writing any code.
- It helps to develop four fundamental skills:
1. Listening- hearing and interpreting the vocabulary.
1. Speaking- using the correct words to communicate an idea.
1. Reading- understanding the written language itself.
1. Writing- producing from scratch.
- Pair programming benefits are:
1. Greater efficiency
1. Engaged collaboration
1. Learning from fellow students
1. Social skills
1. Job interview readiness


# HTML Links
- *Links* allow you to move from one web page to another, which enables the very idea of browsing or surfing the web.
- Links are created using the `<a></a>` tag.  You then specify the page (with a URL) that you want to link to using the href attribute.  In between the opening and closing tag you put the text that will render on your web page that will be clicked on.  Want to think of what the person is searching for as that text. 
- Link to different parts of the same webpage- You first add an id attribute to the elements location you later want to reference, then in the `<a>` use the `#` to start the value to your href attribute, followed by the id attribute that you are attempting to move to.
- Creating links between pages within your site- Use relative URL's, which are just shorthand way of telling the browser where a page is in relation to teh current page.
- Linking to other sites-
- Email Links-  that start up your email and address a new email to someone.
- Links that open to new windows- to accomplish this you would use the target attribute with the value of `_blank` following the href attribute.

# Layout
- Controlling the position of elements.
  - Normal flow- position:static
  - Relative positioning- position:relative
  - Absolute positioning- position:absolute
  - Fixed positioning- position:fixed
  - Floating elements-  float:
- Creating site layouts
  - Fixed width layouts
  - liquid layouts
- Designing for different sized screens and for varying screen resolutions
- Key concepts in positioning elements:
  - Building blocks
    - Block-Level elements
    - Inline elements
  - Containing elements
- Layout grids- help create professional and flexible designs.
- CSS Frameworks proved rules for common tasks
- You can include multiple CSS files in one page

# Functions, Methods ands Objects
# Functions-
- Functions let you group a series of statements together to perform a specific task.  If different parts of the script repeat the same task, you can reuse the function (rather than repeating the same set of statements).
  - help to organize your code.
  - help to store your the steps needed to achieve a task.
- If you are asking a function to perform the task later, you need to give it a name.  The name should describe its assigned task.  When asked to perform its task it is called **calling** the function.
- The steps that the function needs to perform to perform its task are packaged up in code block, or one or more statements contained within {}.  No need for ; after {}.
- Some functions need to be provided with info in order to achieve a given task.  These pieces of info are **parameters**.
- when you write a function and you expect it to provide you with an answer, the response is known as the **return value**.

- Declaring a function:
![Parts of a Function](https://www.frontamentals.com/static/function-breakdown-e46e54ec2e0de641547f63411acb1d84-bf43a.png)
- Calling a function- look like: functionName();
- Declaring functions that need information- when you declare a function you give it **parameters**.  Inside of the function the parameters act like variables.
  - Ex. function getArea(width, height) /{
      return width * height;
  }
- Calling functions that need information- When you call a function that has parameters, you specify the values it should use in the () that follows its name.  The values are called **arguments**, and they can be provided as values or as variables.
  - Arguments as values- 
  - Arguments as variables-  
- Getting a single value out of a function- some functions return information to the code that called them. Ex.- when they perform a calculation, they return the result.
- Getting a single value out of a function- functions can return more than one value using an array.

- Anonymous functions and function expressions-
  - Function declaration- creates a function you can call later in your code.
  - Function expression- when you put a function right where you want it to be called.  Generally is un named or an *anonymous function*.
- Immediately invoked function expressions-
- Variable scope- 
  - Local variables
  - Global variables
- How variables and memory work-