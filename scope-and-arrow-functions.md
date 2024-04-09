# Scope in Javascript

* Scope Definition:
    - Scope refers to the set variables accessible within a program
    - Variables must be in the current scope to be usable
    - Variables are limited to the scope where they're declared

* Advantages of Scope:
    - Security: ensures variables are only accessed where intended
    - Reduced collisions: prevents variable name clashes, enhancing code reliability

* Types of Scope:
    - Global scope: broadest, accessible throughout the entire program
    - Local scope: bound within a function, includes function arguments and local variables
    - Block scope: limited to blocks denoted by curly braces, such as conditionals and loops

* Scope Chaining:
    - Inner scopes can access outer variables
    - JavaScript searches outer scopes for referenced variables if not found locally

* Lexical Scope:
    - Variable values determined during parsing, not execution
    - Enables determining variable values by inspecting code without running it

* Key Takeaways:
    - Understand scope types and their accessibility
    - Learn how scope chaining enables inner access to outer variables
    - Appreciate lexical scoping for pre-execution variable resolution



# Different Variables in JavaScript

* Variable Declaration:
    - Variables store information for use in a program
    - Declared using __'let'__, __'const'__, or __'var'__

* Types of Variable Declarations:
    - __'let'__: allows reassignment, scoped within blocks
    - __'const'__ immutable, scoped within blocks
    - __'var'__ can be reassigned, scoped within functions

* Hoisting and Scoping:
    - Hoisting: variables and function declarations are moved to the top of their scope before execution
    - Function-scoped: variables declared with 'var' ar limited to the function's scope
    - Block-scoped: Variables declared with 'let' and 'const' are confined within blocks

* Function vs. Block Scoping:
    - Function-scoped: variables declared with 'var' can lead to accidental overwriting
    - Block-scoped: 'let' and 'const' help prevent accidental variable overwriting, enhancing code clarity and maintainability

* Global Variables:
    - Variables declared without keywords become global, leading to potential name collisions
    - Limit global variables to enhance code maintainability and avoid conflicts

* Key Takeaways:
    - Choose 'let' and 'const' for clearer variable intentions
    - Understand scoping differences to prevent unexpected behaviour
    - Limit global variables for better code organisation and collaboration


# Arrow Functions

* Introduced in ES2015 for concise function declaration
* Utilise __"=>"__ (fat arrow) syntax
* Address two main concerns: shorter functions & context binding

* Anatomy
    __Multiple statement syntax:__
    ```javascript
    (parameters) => {
        statement1;
        statement2;
        return value;
    }
    ```

    __Single parameter, no parentheses:__
    ```javascript
    param => {
        statement;
        return value;
    }
    ```

    __No parameters, use empty parentheses:__
    ```javascript
    () => {
        statement;
        return value;
    }
    ```


* Implicit Returns:

    - Single expression functions allow implicit return
    ```javascript
    arg => expression; // same as (arg) => { return expression; }
    ```

    - Multiple statements require explicit return
    ```javascript
    arg => {
        statement1;
        statement2;
        return value;
    }
    ```

* Syntactic Ambiguity:

    - '{}' after fat arrow implies empty block
    - '() => {};' returns undefined

    - to return an empty object, wrap it in parentheses
    - '() => ({});' returns an object: {}


* Anonymous Nature:

    - Arrow functions are anonymous by default
    - Assign to variables for named functions

    ```javascript
    const functionName = parameters => {
        statement;
    };
    ```

* Key Takeaways:
    - Arrow functions offer concise syntax
    - Implicit return in single expressions
    - Care needed with context and syntactic amiguity
    - Useful for shortening code, but remember differences in behaviour


# Closures

Definition: A closure is a combination of a function and the lexical environment within which that function was declared.

Practicality: Closures occur when an inner function accesses or modifies variables in an outer function. They are crucial for creativity, flexibility, and security in JavaScript code.

* Basic Rules
    - Closures have access to variables within their own scope as well as any outer function's scope when they are declared
    - Lexical  environment includes variables available within the closure's scope, its outer function's scope, and the global scope
    - Even after an outer function has returned, an inner function retains access to the outer function's variables

* Example:

```javascript
function makeAdder(x) {
    return function(y) {
        return x + y;
    };
}

const add5 = makeAdder(5);

console.log(add5(2)); // prints 7
```

* Applications:
    - Private state: use closures to create private variables and functions
    - Passing arguments implicity: pass arguments down to helper functions without

By understanding closures, you can implement them to control scope effectively and enhance the the functionality and Security of your JavaScript code.
