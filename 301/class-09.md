## Concepts of Functional Programming in Javascript
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia  
- ***pure functions***- a function is pure if it:
  1. Returns the same result if given the same arguments (it is also referred as deterministic).
    - EX. of an impure function:  
    ```let PI = 3.14; ```   
    ```const calculateArea = (radius) => radius * radius * PI; ``` 
    ```calculateArea(10); // returns 314.0```
      - It is considered impure because it uses a global object that was not passed as a parameter to the function.
    - EX. of a pure function:  
   ``` let PI = 3.14;```  
   ```const calculateArea = (radius, pi) => radius * radius * pi;```  
    ```calculateArea(10, PI); // returns 314.0```
      - This will always pass the PI value as a parameter to the function. So now we are just accessing parameters passed to the function. No external object.
        - For the parameters radius = 10 & PI = 3.14, we will always have the same the result: 314.0
        - For the parameters radius = 10 & PI = 42, we will always have the same the result: 4200
    - Examples of impure functions:
        - If our function reads external files, it’s not a pure function — the file’s contents can change.
        - Any function that relies on a random number generator cannot be pure.
  2. It does not cause any observable side effects.
    - Examples of observable side effects include modifying a global object or a parameter passed by reference.
    - ***mutability is discouraged in functional programming.***
- Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen.
- Pure functions benefits:  
  1. The code’s definitely easier to test.
  2. Immutability- Unchanging over time or unable to be changed.
    - When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
    - With ***recursion***, we keep our variables immutable.
- ***Referential transparency***- if a function consistently yields the same result for the same input.
- pure functions + immutable data = referential transparency
- In computing, memoization or memoisation is an optimization technique used primarily to speed up computer programs by storing the results of expensive function calls and returning the cached result when the same inputs occur again.
- ***Functions as first-class entities***- The idea of functions as first-class entities is that functions are also treated as values and used as data.
- Functions as first-class entities can:
  - refer to it from constants and variables
  - pass it as a parameter to other functions
- return it as result from other functions
- The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.
- ***Higher-order functions***: takes one or more functions as arguments, or
returns a function as its result.
  - ***Filter***- The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.
  - ***Map***- method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
  - ***Reduce***- receive a function and a collection, and return a value created by combining the items.

## Refactoring JavaScript for Performance and Readability
-  A ***hash function*** is used to map a given key to a location in the hash table.
- Strategies:
  - Return early from functions.
  - Cache variables so functions can be read like sentences.
  - Check for Web APIs before implementing your own functionality