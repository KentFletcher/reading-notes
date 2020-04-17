## Call stack
A ***call stack*** is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.
  - When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
  - Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
  - When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
  - If the stack takes up more space than it had assigned to it, it results in a "***stack overflow***" error.
  - We start with an empty Call Stack, and whenever we invoke a function, it is automatically added to the Call Stack, after executing all of its codes, it is automatically removed from the Call Stack. At the end, we ended up with an empty stack too.   

The JavaScript engine is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
- The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
- The understanding of the call stack is vital to Asynchronous programming.
  - In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

A call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
  - When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
  - The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

A **stack overflow** occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
## JavaScript error messages
Types of error messages:
  - Reference Errors- when you try to use a variable that is not yet declared.
    - This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).
      - Whatever you are using (var, let or const) the fix is as simple has declaring the variable before any declaration is made.
  - Syntax errors- this occurs when you have something that cannot be parsed in terms of syntax.
  - Range errors- Try to manipulate an object with some kind of length and give it an invalid length.
  - Type errors- show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.  
## Debugging
To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools.