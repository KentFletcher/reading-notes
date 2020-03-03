# HTML Text-
## Structural and Semantinc Markup-
- Structural markup- are the elements that are used to describe the structure of the page.
  - Examples are headings, subheadings, paragraphs.
- Semantic markup- are the elements that provide extra information, such as where to place emphasis, that something is within quotations and who said it, 

# CSS- Cascading Style Sheets
- Key to imagine a box around every HTML element.  CSS allows you to control the way each of those individual elements look.
- 2 Elements:
  1. Inline- flow with the text and do not start a new line, like \<b>, \<i>, etc.
  1. Block- look like they start a new line, like \<h1>, \<div>, \<p>
- Examples of styles:
  - Boxes- width, height, borders, background color and images, etc.
  - Text- Typeface, Size, color, etc.
  - Specific- These include lists, tables and forms.

## CSS associates style rules with HTML elements
- CSS rule contains 2 parts:
  - Selector- choose what from the HTML file is going to be affected
  - Declaration- declarations sit within \{} and have 2 parts property and value.
    - Properties- indicate the aspects of the element you want to change.
    - Values- specify the settings you want to use for the chosen property.
- Can use CSS from 2 sources:
  - External- separate file that is linked within your HTML code.  It is referenced with a link element within the head of your HTML doc.  The link is given an attribute of href with the path to your CSS file within. Along with the attributes type and rel, which would specify the document type being referenced and the relation ship, respectively.
  - Internal- within the HTML page, also placed in the head but with the style element

- Many types of Selectors:

### How CSS rules cascade:
- 2 rules for same element:   
    1. last rule- if selectors are identical that latter of the 2 will take precedence.
    1. specificity- if one selector is more specific than the other it will take precedence.  Ex. h1 is more specific than \*.
- Inheritance- If you specify a style for a body element, all its children would inherit the style that was assigned.

# Basic JavaScript Instructions-
- **Statements**-  Each individual instruction or step of a script.  **Should end in a \;**
- **Comments**-  These should be written to explain what your code does.  
  - Multi-line comments- often to describe how the script works.  Start with \/* and end with the \*/ characters.
  - Single-line comments- short descriptions of what the code is doing, good for when you have to look back at a script. Anything after \// will be ignored.
- **Variables**- A script will have to temporarily store the bits of information it need to do its job, it store that data as variables.  Data stored within a variable will often change each time a script runs.  Result of a script  are said to be calculated using the data stored in variables.
 - Before you can use a variable you must declare the variable so you would say var quantity;, with quantity being the variable name or identifier..  var is a *keyword*.  That keyword now represents the var.  
 - Once you have created a var, you can tell it what info you would like it to store for you.  Programmers say you would **assign**, represented by \=, a value to the var.
   EX.  \quantity = 3; with quantity the var name, \= as the assignment operator, and 3 as the var value, then always end with \;
- **Data Types**-
  * Numeric- handles numbers.
  * String- letters and other characters, within set of quotes.
  * Boolean- can have one of 2 variables, true or false.
- Rules for naming a Variable:
  1. name must begin with a letter, dollar sign, or underscore.  It cannot start with a number
  1. can have letter, \$, \_.  Cannot have dash or period.
  1. cannot use keywords of reserved words.
  1. they are case sensitive
  1. need to describe the kind of info that is stores.
  1. if it is more than one word, use a capital letter for the start of every word.
- **Arrays**- are a special types of variables that store more than one piece of related information.
- **Expressions**- result in a single value, the \= is used to assign a value.  There are 2 types:
  1. Expressions that assign a value to a variable.
  1. Expressions that us 2 or more values to return a single value.
- Expressions rely on *operators* to create a single value from one or more values.  Types of operators:
  1. Assignment operators- Assign a value.
  1. Arithmetic operators- Perform basic math.
  1. String operators- Combines 2 strings (concatenation).
  1. comparison operators
  1. logical operators-

# Evaluating conditions and Conditional Statements 
## Evaluating a condition- 
  - An expression is evaluated, which returns a value.   These generally return a value of  true or false, or **Boolean**. 
- **Comparison Operators**- 
  - Evaluating Condition for comparison operators:
    - \== : Is equal to.  Compares 2 values (numbers, strings, or Boolean) to see if they are the same.
    - \=== : Strictly equal to.  compares 2 values to check that both the data type and value are the same. 
    - \!= : Is not equal to.  Compares 2 values (numbers, strings, or Boolean) to see if they are *not* the same.
    - \!== : Strictly not equal to.   compares 2 values to check that both the data type and value are *not* the same.
    - \> : Greater than. Checks if the number on the left is *greater than* the one on the right.
    - \>= : Greater than or equal to. Checks if the number on the left is *greater than or equal to* the one on the right.
    - \< : Less than. Checks if the number on the left is *less than* the one on the right.
    - \<= : Less than or equal to. Checks if the number on the left is *less than or equal to* the one on the right.
  - Structuring Comparison Operators. Generally this is done with in parentheses, there os generally one operator and two operands on either side of the operator.  
    - Operands can be values or variables.  
    - The operand can be an *expression*, meaning it does not have to be a single variable name of value. This would be structured with in parenthesis, and can have 2 operand being combined within parenthesis on either side of a comparison operator.
- **Logical Operators**- Allow you to compare the results of more than one comparison operator.
  - \&\& : Logical And- Tests more than one condition.  If both expressions evaluate to true then the expression returns true.  If just one returns false then the expression will return false.
  - \|\| : Logical Or- Tests at least one condition. If either expression evaluates to true, then will return true.  If both are false, will return false. 
  - \! :  Logical Not- Takes a single Boolean value and inverts it.  If it was false, with a /! in front of it, it would return true. If the statement was true would return false.
  
## **Conditional Statements**- 
  - Allow your code to make decisions about what to do next.
- **IF Statements**-  evaluates or checks if a condition evaluates to true of false.  If it is true, any statements within subsequent code block are executed.
- **IF...ELSE**- checks a condition, if its true the first code block is run.  if it's false the second, or else condition is executed instead.  