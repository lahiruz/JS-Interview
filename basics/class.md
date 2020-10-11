# Welcome to class

* Before ES6 this is how classes have defined in Javascript.

  ```js
  function Person(name){
      this.name = name;
  }
  
  Person.prototype.print = function(){
      console.log("Hi " + this.name);
  }
  
  var person = new Person("lahiru"); // using new keyword you can create an object using constructor function.
  person.print(); // Hi lahiru
  ```

* With ES6 it has changed to the following syntax which most of you guys familier with.

  ```js
  class Person {
      constructor(name) {
          this.name = name;
      }
      
      print() {
          console.log("Hi " + this.name);
      }
  }
  
  var person = new Person("lahiru"); // using new keyword you can create an object using ES6 classes.
  person.print(); // Hi lahiru
  ```
  
* Class declarations are not hoisted.

* Also you can define static properties and methods with classes.

  ```js
  class Person {
      constructor(name) {
          this.name = name;
      }
      
      print() {
          console.log("Hi " + this.name);
      }
      
      static sleep() {
          console.log("Sleep well");
      }
  }
  
  Person.age = 12; // this is how you can define static variables
  Person.sleep(); // Sleep well
  var person = new Person("lahiru");
  person.sleep(); // throws a type error
  ```

* You can use get and set methods with classes.

* Also you can do inheritance with classes using **extends** and **super** keywords.

  ```js
  class Person {
      constructor(name) {
          this.name = name;
      }
    
      print() {
          console.log("I am Person");
      }
  }
  
  class Boy extends Person {
      constructor(name) {
          super(name);
      }
        
      print() {
          super.print();
          console.log("I am " + this.name);
      }
  }
  
  var person = new Boy("lahiru");
  person.print(); // print "I am Person" frist and then print "I am lahiru"
  ```
