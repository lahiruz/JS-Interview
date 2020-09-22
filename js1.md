# Important things to know about javascript (part 1)

* Javascript is standardized as ECMAScript(ES) which is maintained by a committee called TC39. Each ES version decide what kind of features will be released to Javascript language.

* Everything in Javascript is an Object. These objects property key is always a string. Each property has attributes of value, writable, enumerable (can iterate via for..in loops) and configurable (is deletable).

* You can create variables using var, let and const.

* Javascript have Number, String, Boolean, Null, Undefined, Symbol & Object data types. First 6 are primitive data types. You can use typeof to see the actual type of the variable. Remember Array is also a special type of an object.

* There are multiple ways to define functions. Function Declaration, Function Expression(can be used where you to pass function as a parameter), Function Constructor(which is not a recommended way) and Self Execution Function(IIFE).

* Javascript has multiple scopes. Global scope where window object exists, Functional scope and Block scope where you have variable defined with let keyword.
