# HTML- Tables
- A *table* represents information in a grid format.  Examples are financial reports, TV schedules, and sports results.
- Grids allow is to understand complex data by referencing information on two axes.  Each block in the grid is referred to as a table cell.  In HTML, a table is written out row by row.
- ![Basic Table Structure](https://image.slidesharecdn.com/htmltables-180721142906/95/html-tables-2-638.jpg?cb=1532183439)
- Table heading- <th> is used to to denote the heading of a row or a column, you would use the attribute scope followed by either "row" or "col".  
- You can make cells of a table span more than one row or column using the rowspan anl colspan attributes.
- For long tables you can split the tables you can split the table into a <thead>, <tbody>, and <tfoot>.  This helps with screen readers and also allows you to style these sections differently than the rest of the table.

# JavaScript- Functions, Methods and Objects
- Creating an Object: Constructor notation- 
1. The new keyword and object constructor function, Object(), to creates a blank object.  
1. Next you can then add properties and methods to the object, using the dot notation.  Each statement that adds a property or method should end in a semi-colon.
- Updating an object- To update the value of properties, use dot notation or square brackets.  They work on objects created using literal or constructor notation.  To delete a property, use the delete keyword.
- Creating many objects: constructor notation- When you want to create several objects to represent similar things, can use functions as a template for creating objects.  First create the template with the object's properties and methods.
- Arrays are a type of object.  They hold a related set of key/value pairs (like all objects), but the key for each value is its index number.
- you can combine arrays and objects to create complex data structures:
  - Arrays can stor a series of objects (and remember their order).
  - Objects can also hold arrays (as values of heir properties).
- Built-in objects- Browsers come with a set of built in objects that represent things like the browser window and the current web page shown in that window.  These built-in objects act as a toolkit for creating interactive web pages.  They contain functionality commonly needed by many scripts.
- 3 components of this toolkit:
1. Browser Object MOdel
1. Document Object Model
1. Global Javascript Objects
- Object model- is a group of objects, each representing related things from the real world.  Together they form a model of something larger.

# Domain modeling 
- It is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.
- A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.
- Define a constructor and initialize properties- To define the same properties between many objects, you'll want to use a constructor function. The constructor function is defined using a function expression.  When the function is called, the data inside the parameters are stored inside the respective properties.  After the constructor function definition, two objects are instantiated with the new keyword and their properties are initialized by calling the constructor function. Then the two newly created objects are logged to the console.
- To model the random nature of user behavior, you'll need the help of a random number generator. The JavaScript standard library includes a Math.random() function for use in this situation.
- While it takes longer to locate a method on the prototype object, this technique is an established best practice in JavaScript. When a prototype is shared between two or more objects, those objects execute the same code when the generateRandom() method is called. And shared code means a running program consumes less memory which is important for devices like smart phones and tablets.
- A domain model that's articulated well can verify and validate your understanding of that problem.
- Tips to follow when building your own domain models:
1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
1. Model its attributes with a constructor function that defines and initializes properties.
1. Model its behaviors with small methods that focus on doing one job well.
1. Create instances using the new keyword followed by a call to a constructor function.
1. Store the newly created object in a variable so you can access its properties and methods from outside.
1. Use the this variable within methods so you can access the object's properties and methods from inside
