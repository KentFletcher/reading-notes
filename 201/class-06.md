# Understanding The Problem Domain Is The Hardest Part Of Programming- by John Sonmez 
- In coding understanding the problem is the most critical piece to the equation. It is very difficult to solve a problem before you know the question.
- What can you do about it?  You can do one of two things:  
1. Make the problem domain easier- Often you can make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.  Take a part of the problem and fully understand that part before expanding the problem domain.
1. Get better at understanding the problem domain- It is easy to fall into the trap of thinking you understand enough of the problem to get started coding it.  Best to resist the temptation to “not waste anymore time talking” and make sure you understand a problem inside and out before you try and solve it with code.  It is much more expensive and time consuming to do things over than it is to do them right the first time. 

# Objects
- Objects group together a set of variables and functions to create a model of something that you would recognize from the real world.  In an object variables and functions take on different names:
  - Variables become known as *properties*.  properties tell us about the object.
  - Functions become known as *methods*.  Methods represent tasks that are associated with the object.
- The names of objects are known as a *key*.  An object cannot have two keys with the same name, because they are used to access their corresponding values.
- The value of a property can be a string, Boolean, array or evan an object. 
- The value of a method is always a function.
- Literal notation is the easiest and most popular way to create objects.  Thought there are several ways to create objects.
- Accessing an object and dot notation- you can access the properties or methods of an object using dot notation, which is the name of the object followed by a period the the name of the property or method you want to use. The period is know as a *member operator*.  The property or method on the right is the member of the object on the left.
  - You can also access properties using square brackets.  Most commonly used when:
    - The name of the property or method contains special characters.
    - The name of the property is a number, which is allowed but should generally be avoided.
    - A variable is being usd i place of the property name.

# Document Object Model (DOM)
- The DOM specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.  The DOM is also referred to as the Application Programming Interface (API), user interfaces allow humans to interact with programs; APIs let programs and scripts talk to each other.
- The DOM states what your script can ask the browser about the current page, ans how to tell the browser to update what is being shown to the user.
- The browser represents the page using a DOM tree.
- DOM trees have four types of nodes:
  - Document nodes- This is one node and represent the entire page.  The starting point for all visits to the DOM tree.
  - Element nodes- Describe the structure of an HTML page. These are selected by their id or class attributes, tag name, or using CSS selector syntax.
  - Attribute nodes- They are part of the element , not the children of an element.
  - Text nodes- these cannot have children
- Each node is an object with methods and properties.
- Scripts access and update the DOM tree, not the source HTML file.  Any change made to the DOM tree is reflected in the browser. 
- Accessing and updating the DOM tree involves 2 steps:
1. Locate the node that represents the element you want to work with.
1. Use its text content, child elements, and attributes.
- Whenever a DOM query can return more than one node, it will always return a NodeList.
- From an element node, you can access adn update it content using properties such as textContent and innerHTML or using DOM manipulation techniques.
- An element node can contain multiple text nodes and child elements that are siblings of each other.
- Browsers offer tool for viewing DOM tree.