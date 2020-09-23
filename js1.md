# Important things to know about javascript (part 1)

## variables, functions, scope, objects

* Javascript is standardized as **ECMAScript(ES)** which is maintained by a committee called **TC39**. Each ES version decide what kind of features will be released to Javascript language.

* Everything in Javascript is an **Object**. These objects property key is always a string. Each property has attributes of **value**, **writable**, **enumerable** (can iterate via for..in loops) and **configurable**(is deletable).

* You can create variables using var, let and const.

* Javascript have **Number**, **String**, **Boolean**, **Null**, **Undefined**, **Symbol**(introduced in ES6) & **Object** data types. First 6 are primitive data types. You can use **typeof** to see the actual type of the variable. Remember Array is also a special type of an object.

* There are multiple ways to define functions. **Function Declaration**, **Function Expression**(can be used where you to pass function as a parameter), **Function Constructor**(which is not a recommended way), **Self Execution Function(IIFE)** & **Arrow Function**(introduced in ES6).

* A closure is the combination of a function and the [lexical environment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures#:~:text=A%20closure%20is%20the%20combination,state%20(the%20lexical%20environment).&text=In%20JavaScript%2C%20closures%20are%20created,created%2C%20at%20function%20creation%20time) within which that function was declared.

    ```js
    function makeFunc() {
      var name = 'Mozilla';
      function displayName() {
        alert(name);
      }
      return displayName;
    }

    var myFunc = makeFunc();
    myFunc(); // myFunc is a closure where it remembers scope within makeFunc
    ```

* Arrow functions gives you the lexical binding and allows you to access parent scope.

* Always define functions and varibales before using them. You can define variable without "var" keyword. But it is not a good practice. Therefore, make sure to declare variables. Using ES5 "use strict" directive will help help you to alert when you forget to define variables.

* Javascript has two main scopes. **Global** scope where window object exists and **Functional** scope within functions. In addition to that, let and const allows you to define **Block** level scoping.

* Javascript hoisting is important concept where all **variable and function declarations** are moved to the scope that they have defined. When hoisting happens alway Function declarations gets priority over the variables. 

* If someone declare variable and function with same name that variable declaration will be ignored (refer following image).

    <div style="align: center">
        <img src="./assests/hoisting1.png" />
    </div>


* Variables and constants declared with let and const are not hoisted. Also Function expressions are not hoisted.
