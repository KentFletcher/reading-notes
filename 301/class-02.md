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

# jQuery
 jQuery offers a simple way to achieve a variety of common JavaScript tasks quickly and consistently.  It is a JavaScript file that you include in web pages. First it uses CSS-style selectors to find elements and second it then does something to them with jQuery methods.  
1. You can target one or more elements using a jQuery function that looks like this: ```$('')```with a parameter passed within, a css selector.
   - EX. ```$('li.hot')```- selects a li with the class of hot.
2. Allows you to do something with the elements using jQuery methods.  The jQuery object has many methods that you can use to work with elements you select.  The methods represent tasks that you commonly need to perform with elements.
    - EX.```$('li.hot').addClass('complete');```There is the (.) which is the member operator which indicates that the method on the right should update the elements in the jQuery object on the left, followed by the method, 'complete' is the parameter.

### Similarities and Differences between jQuery and the DOM.
   - Similar to the DOM in that it performs the same task, in simpler syntax.  You can also store jQuery object in a var. Also you can manipulate the nodes that you select, using methods and properties.
   - The main differences are that jQuery is cross-browser, meaning there is no need for fallback code.  Selecting the elements is easier and more accurate.  Event handling is simpler as it uses one method that works in all major browsers.  Methods affect all the selected ele's without the need to loop through each one.  There are additional methods to handle animations.  Once you have made a selection you can apply multiple methods to it.<br>

The first thing that you to do is include the jQuery script in your page, generally before the end of the body tag.  Second is to add a secondary js file that includes the jQuery selectors and methods to update the content of the HTML page.<br>

### It makes code simpler and is used on over 1/4 of sites on the web:
1. Simple Selectors
2. Common Tasks in less code- "Write less, do more"
3. Cross-Browser Compatibility- uses ***feature detection*** to find the best way to achieve a task, which uses many conditional statements to see if the browser supports certain ways to achieve a goal,, it starts with the optimal way and then continues to the next best method.

### Matched Set or jQuery selection
- When you select one or more ele's, a jQuery object is returned, and that is known as a Matched Set or jQuery selection.
  - An example of a single ele selected would be ```$('ul')```, the jQuery object contains a reference to just one ele node.
  - An example of a selector returning several ele's would be ```$('li')```, the jQuery object contains a reference to each ele nodes.
### jQuery methods that get and set data
- Some jQuery methods both retrieve info from, and update the contents of, elements. They do not apply to all ele's.

### jQuery objects store references to (location of) ele's, they do not make copies of them.
  - Caching a jQuery object store a reference to it in a variable, in case it need to reference the same selection more than once.

### jQuery offers methods that make it quick and simple to achieve a range of tasks that JavaScript programmers commonly need to perform.
- Looping- It is easier because you just need to return multiple elements by selecting them, no need to write a loop.
- Chaining- You can list several methods at a time using the dot notation to separate each one, resulting in a far more compact code.
  - Methods used to update selections can be chained, but methods to retrieve information cannot.
### 4 Methods that update the content of all elements in  ajQuery selection.
1. .html()
2. .text()
3. .replaceWith()
4. .remove()
- If you want to use and amend the content of the current selection, these methods take a function as a parameter.  That function can be used to create new content.
#### Inserting new ele's involves 2 steps:
1. Create new ele's in a jQuery object.
2. Use a method to insert the content into the page.
   - methods to add content to the DOM tree:<br>
     1. .before()- before the selected ele
     2. .after()- after the selected ele
     3. .prepend()- after the selected ele's opening tag
     4. .append()- before the selected ele's closing tag
#### Getting an setting attribute values
- You can create attributes or access and update their contents using 4 methods:
1. .attr()
2. .removeAttr()
3. .addClass()
4. .removeClass()
#### Getting and setting CSS properties.
- The .css() method lets you ***get*** and ***set*** the values of CSS properties
- You can set multiple properties using the object literal notation.

