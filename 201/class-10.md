# Error Handling and Debugging in JavaScript
- Knowing the order of execution is crucial, because knowing the order in which scripts are statements are processed can be complex and some tacks cannot be complete until another statement or function has been run.
- Executive contexts- Every statement in a script lives in one of three execution contexts:
1. Global context- Code that is in the script, but not in a function.  There is only one global context in any page.
1. Function context- Code that is being run in a function.
1. Eval context- text is executed like a code in an internal function called eval().
- The first 2 of the above evaluation context correspond with the notion of scope:
1. Global scope- If a variable is declared outside a function, it can be used anywhere because it has a global scope.  If you do not use the var keyword when creating a variable, it is place in global scope.
1. function-level scope- when a variable is declared within a function then it can only be used with in that function.
- The javascript interpreter processes one line of code at a time.  When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.
- Each time a script enters a new execution context, there are 2 phases of activity:
1. Prepare- The new scope is created.  Variables, functions and arguments are created.
1. Now it can assign values to variables.  Reference functions and run their code.  Execute statements.
- KNowing the 2 phases of activity happen helps you understand a concept called *hoisting*. The preparation phase of creating variables and functions before they are executed.  Or you can think of them as having been prepared.
- Understanding scope- In the interpreter, each execution context has its own variables object.  It holds the variables, functions, and parameters available within it.  Each execution context can also access it parent's variable object.
  - Functions in JS are said to have *lexical scope*.  They are linked to the object they were defined within. For each execution context, the scope is the current execution context's variables object, plus the variable object for each parent execution context.  Imagine each function is a nesting doll, the children can ask the parents for information in their variables, but the parents cannot get variables from their children. Each child will get the same answer from teh parent.
- Debugging is the process of finding errors.  It involves a process of deduction.
- The console helps narrow down the area in which the error is located, so you can try to find the exact error.
- Error objects can help you find where your mistakes are and browsers have tool to help you read them.
- JavaScript has 7 different errors. Each creates its own error object, which can tell you its line number and gives a description of the error.
1. Error- generic error
1. SyntaxError- syntax has not been followed
1. ReferenceError- Tried to reference a variable that is not declared/ within scope
1. TypeError- unexpected data type
1. RangeError- number not in acceptable range
1. URIError- 
1. EvalError-
- Debugging is about deduction: eliminating potential causes of an error.  
1. Where is the problem?
1. What exactly is the problem?
- You can pause the execution of a script on any line using breakpoints.  Then you can check the values stored in variables at that point in time.
- If you know that you may get an error, wou can handle it gracefully using the try, catch, finally statements.  Use them to give your users helpful feedback.