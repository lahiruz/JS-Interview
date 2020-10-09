# Welcome to protptype

* Consider the following example.

  ```js
  var person = {}; // empty object
  
  console.log(person.toString()); output -> [Object Object] // print toString() method.
  ```

* Can you imagine from where this **toString** method comes in? The reason is Prototype. toString method is belongs to prototype object.

* Protptype is a special type of object which is associated with every function and object in Javascript. 

* You can access and modify prototype in functions and prototype in objects is not visible. In chrome and firefox you can check prototype properties by using **__proto__** key.
