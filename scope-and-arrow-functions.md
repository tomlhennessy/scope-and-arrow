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
