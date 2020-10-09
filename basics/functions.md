# Welcome to functions

* There are multiple ways to define functions. **Function Declaration**, **Function Expression**(can be used where you to pass function as a parameter), **Function Constructor**(which is not a recommended way), **Self Execution Function(IIFE)** & **Arrow Function**(introduced in ES6).

* You can use **call**, **apply** and **bind** with functions.
    - **call**: a function can be called with given **this** value and provided arguments.
        ```js
        myFunc.call(thisContext, arg1, arg2, ...);
        ```
    - **apply**: Behaviour is similer to call. But the arguments are provided as array.
        ```js
        myFunc.apply(thisContext, [arg1, arg2, ...]);
        ```
    
    - **bind**: a function can be bind to the given **this** value with the provided arguments. This will immediately return a function after calling with bind.
        ```js
        myFunc.bind(thisContext, arg1, arg2, ...);
        ```
    Examples

    ```js
    var person = {
        firstName: 'John',
        lastName: 'Doe'
    }
    
    function myFun(greeting) {
        console.log(`${greeting} ${this.firstName} ${this.lastName}`);
    }
    
    myFun('hello!'); // hello! undefined undefined
    myFun.call(person, 'hello!'); // hello! John Doe
    myFun.apply(person, ['hello!']); // hello! John Doe
    
    myFun.bind(person, 'hello!'); // return an invokable function
    myFun.bind(person, 'hello!')(); // hello! John Doe
    ```

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

* Arrow functions gives you the lexical binding and allows you to access parent scope. Refer age variable in the following example.
    
    ```js
    function Person() {
      this.age = 0;
      
      setInterval(() => {
        this.age++;
        console.log(this.age);
      }, 1000);
    }

    var p = Person();
    ```

* Always define functions and varibales before using them. You can define variable without "var" keyword. But it is not a good practice. Therefore, make sure to declare variables. Using ES5 "use strict" directive will help help you to alert when you forget to define variables.
