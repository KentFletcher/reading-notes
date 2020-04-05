# HTML
## Lists
- With in HTML there is three types of lists:
1. Ordered lists-  Ordered lists use numbers.  A good example of when to use this type of list is when writing a recipe in cooking to be strictly adhered to for best results.
  - These  elements are made up of an opening and closing tags, `<ol>` and  `</ol>` respectively, and have list items `<li> </li>` nested within the opening and closing tags of the element. 
  - Browsers indent lists by default.
1. Unordered lists- Ordered lists use bullets.  A good example of when to use these lists is when listing ingredients for a recipe, they do not need to be in any specific order.
  - These elements are made up of an opening and closing tags, `<ul>` and  `</ul>` respectively, and have list items `<li> </li>` nested within the opening and closing tags of the element.
   -Browsers indent lists by default.
1. Definition lists- Definition lists are used to define terminology.
  - These elements are made up of an opening and closing tags, `<dl>` and  `</dl>` respectively, and have term to be defined `<dt> </dt>` nested within the opening and closing tags of the element. A major difference with this list is with in the `<dt> </dt>` element, you have `<dd> </dd>` which is the definition of the term.
  - Browsers indent the definition will be indented under the term by default.
- You can can put a second list within a list item to create a secondary list.

# CSS
## Boxes
- CSS treats each HTML element as if it has it sits within its own box.  You can then use CSS to manipulate and control those boxes.  There are many ways that you can control the boxes:
  - You control the dimensions, and the height and width.  This can really help to improve legibility with boxes that contain text elements, such as`<p>`. 
  - You control the borders such as style, margins and padding, which specifies how much space will be left between the contents of the box and the border.
  - You can center content.
  - You can change the display of inline or block elements, or even create an inline-block element.
  - You can also hide items using the display and visibility properties, good for things coming soon leaves a place open where the hidden item would be.
  - You can create border images and box shadows, and even round the edges or give it an elliptical shape to the borders of the boxes.
  
# JavaScript
## Switch Statements and Loops
- **Switch Statements**- starts with a variable called the *switch value*.  Each case indicated a possible value for this variable and the code that should run if the variable matches that value.
  - You also include a default option if none of the cases match.
  - If a match is found, that code is run; then the break statement stops the rest of the switch statement from running.
   - These move quicker than IF statements, because once it has found a match it runs the code for that match and then breaks, where as the IF statement would continue to evaluate even if the match was found.

- **Type coercion and weak typing**
  - If you use a data type JS did not expect, it tries to make sense of the operation rather than report an error.  JS can convert data types behind the scenes tp complete an operation,  This is *type coercion*
  - JS uses *weak typing* because the data type for a value can change.
  - Type coercion can lead to unexpected values or errors; therefore it is best to use strictly equals to `(===)` and strictly not equals to `(!==)`, as these will check the value and data types match.
- 5 Data Types and purpose:
1. string- text
1. number- number
1. Boolean- true or false
1. null- empty value
1. undefined- Variable has been declared but not yet assigned a value.

- **Truthy and Falsy Values**-  Due to coercion, every value in JS can be treated as if it were true or false.
  - Falsy are treated as though they are false.  Falsy values can also be treated as the number 0.
    - Ex. Boolean false, number 0, empty string, NaN, variable with no value assigned.
  - Truthy are treated as true.  Almost anything that is not false can be treated as true.
    - Ex. boolean true, numbers other than 0, strings with content, number calculations, true written as a string, 0 written as a string, false written as a string

- **Loops**- check a condition.  If it returns true, a code block will run.  Then the condition will be checked agin and if it still returns true, the code block will run again. It repeats until the condition returns false.
- Three common types of loops:
  * **For** - If you need to run code a specific number of times, use a **for** loop.  The condition is usually a counter which is used to tell how many times the loop should run. 
    * Loop Counters- Uses a counter as a condition, made up of 3 statements:
    1. Initialized- Create a variable and set it to 0. This variable is commonly i, and acts as the counter. EX. var i = 0;
    1. Condition - The loop should continue to run until the counter reaches a specified number.  Ex. i < 10;
    1. Update - Every time the loop has run the statements in the {}, it adds one to the counter.  Ex. i++
  * **While** - If you do not know how many times the code should run.  The condition can be something other than the counter, and the code will continue to loop for as long as the condition is true.
  
  * **Do While** - Similar to the while loop, but a key difference: it will always run the statements inside the curly brackets at least once, even if the condition evaluates to false.