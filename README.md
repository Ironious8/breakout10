1. What is scope in javascript and why is it important?

  Is the concept of where something is available or in js, as an area in which a variable  value is relevant.

  Alternatively, its an area where variables and functions are declared and can be accessed.

  Scope is important in javascript because it determines and controls the accessibility of variables and
  functions in different parts of the code and maintains code organization thereby preventing variable conflicts.


2. Can you explain the difference between global scope and local scope?

   In JavaScript, local scope refers to variables declared within a function or block (using let, const, or var), accessible only within that specific context and existing only for the duration of its execution. Global scope refers to variables declared outside any function or block, accessible from anywhere in the code, and existing for the entire lifespan of the program. Local scope ensures variable isolation, while global scope allows for broader accessibility.


 3. How does JavaScript handle scope in functions compared to block-level scope?

   JavaScript uses function scope for 'var' variables, accessible throughout the function. Block-level scope with 'let' and 'const' confines variables to specific blocks, enhancing predictability and avoiding hoisting issues present with var.


 4. How do var, let, and const differ in terms of scope?

    In JavaScript, var declares variables with function scope, meaning they are accessible throughout the function in which they are declared. let and const declare variables with block scope, meaning they are accessible only within the block (e.g., within curly braces) in which they are declared. Additionally, const variables must be initialized at the time of declaration and cannot be reassigned, while let variables can be reassigned but not re-declared within the same scope.


 5. What are the implications of declaring a variable without any keyword (i.e., no var, let, or const)?

    Variables created without a const, let, or var keyword are always globally-scoped, regardless of where they sit in your code.
    If you create one inside of a block, it's still available globally.

 
 
 
 6. What is the scope chain, and how does JavaScript use it to resolve variable access?
   
    The scope chain in JavaScript is the mechanism that determines the order in which nested scopes are accessed to resolve variable names. When a variable is referenced, JavaScript first looks in the local scope of the current function. If not found, it searches through each containing scope, moving outward, until it reaches the global scope. This hierarchical structure ensures variables are found based on their lexical context, allowing JavaScript to resolve variable access efficiently.




 7. What are some differences between lexical scope and dynamic scope? Which one does JavaScript use?

    Lexical scope and dynamic scope differ in how they determine variable accessibility. Lexical scope, used by JavaScript, determines variable scope based on the location of variable declarations within the source code. It uses the function's definition context to resolve variables, meaning a function can access variables from its own scope and parent scopes, but not from the scope of the calling function.
    Dynamic scope, in contrast, resolves variables based on the call stack at runtime. It looks up variables in the scope of the calling function and its callers, moving up the call stack, rather than the lexical environment where the function was defined.



 8. What is a closure, and how does it relate to scope in JavaScript?

CLOSURE:
   > A closure in JavaScript is a function that has access to its own scope, the scope of the outer function, and the global scope. Closures are created every time a function is created, at function creation time.

   >A closure is formed when an inner function is declared within an outer function, and the inner function retains access to the variables and parameters of its outer function, even after the outer function

Key Characteristics of Closures:
Access to Outer Scope: A closure gives you access to an outer function’s scope from an inner function.
Persistent Lexical Environment: Even after the outer function has executed and returned, the inner function maintains a reference to its lexical environment, allowing it to access the outer function’s variables.
Private Variables: Closures can be used to create private variables, encapsulating the state within the function's scope.

Closures are closely related to the concept of scope in JavaScript as follows:

Lexical Scope: Closures take advantage of lexical scope, which determines variable accessibility based on where the functions are declared in the source code.

Scope Chain: When a closure is created, it forms a scope chain that includes the scope where the function was defined. This allows the inner function to access variables from its outer function's scope.

Preserved Environment: Even after the outer function finishes execution, the inner function retains access to its lexical environment due to the closure.


Summary:
Closures are a fundamental concept in JavaScript, allowing functions to retain access to their lexical scope even after the outer function has executed. This feature is powerful for data privacy, function factories, partial application, and maintaining state in asynchronous operations. Understanding closures and how they relate to scope is crucial for effective JavaScript programming.

