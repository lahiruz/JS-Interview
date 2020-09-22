# Important things to know about javascript (part 1)

## variables, functions, objects

* Javascript is standardized as **ECMAScript(ES)** which is maintained by a committee called **TC39**. Each ES version decide what kind of features will be released to Javascript language.

* Everything in Javascript is an **Object**. These objects property key is always a string. Each property has attributes of **value**, **writable**, **enumerable** (can iterate via for..in loops) and **configurable**(is deletable).

* You can create variables using var, let and const.

* Javascript have **Number**, **String**, **Boolean**, **Null**, **Undefined**, **Symbol**(introduced in ES6) & **Object** data types. First 6 are primitive data types. You can use **typeof** to see the actual type of the variable. Remember Array is also a special type of an object.

* There are multiple ways to define functions. **Function Declaration**, **Function Expression**(can be used where you to pass function as a parameter), **Function Constructor**(which is not a recommended way), **Self Execution Function(IIFE)** & **Arrow Function**(introduced in ES6).

* Arrow functions gives you the lexical binding and allows you to access parent scope.

* Javascript has two main scopes. **Global** scope where window object exists and **Functional** scope within functions. In addition to that, let and const allows you to define **Block** level scoping.

* Javascript hoisting is important concept where all **variable and function declarations** are moved to the scope that they have defined. When hoisting happens alway Function declarations gets priority over the variables. If someone declare variable and function with same name that 

* Variables and constants declared with let and const are not hoisted. Also Function expressions are not hoisted.
