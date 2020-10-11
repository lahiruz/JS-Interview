# Welcome to objects

* An object is collection of propeties. A property is key value pair. Each key is always a string and value can be anything. Each property has attributes of **value**, **writable**, **enumerable** (can iterate via for..in loops) and **configurable**(is deletable). Sample object shown in below.

    ```js
    var person = {
        firstName: 'John',
        lastName: 'Doe'
    }
    ```

* Object properties can be accessed in this way ->  person.firstName -> [objectName].[propertyKeyName]. In ES5 they have introduced getters and setters to access object properties.

* After creating an object you can assign new properties to that as follows.

    ```js
    person['age'] = 12;
    ```
    
    - Also by using [Object.defineProperty](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty) you can add new propeties as well as you can change the existing properties.
    

* There are multiple ways to create objects in Javascript. 
    - Object literal 
    
        ```js
        var person = {
            firstName: 'John',
            lastName: 'Doe'
        }
        ```
        
    - Using constructor function  
    
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
        
    - Object.create
        - The first argument you give Object.create is the object to use as the [prototype](https://github.com/lahiruz/JS-Interview/blob/master/basics/prototype.md) of the object it creates.
    
       ```js
        var person = {
            firstName: 'John',
            lastName: 'Doe'
        }
        
        var boy = Object.create(person); // This will create an empty object but person object will set as the prototype of the boy object. In Chrome you can see prototype of an object using __proto__ property. Ex: boy.__proto__ 
        ```
        - Also [read this](https://stackoverflow.com/questions/16666231/difference-between-object-createobject-prototype-object-createobject-and-o#:~:text=var%20o%20%3D%20Object.-,create(Object)%3B,a%20function%20as%20its%20prototype.) if you still have questions.
    
    - Using ES6 classes
    
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
        - check more about classes [here](https://github.com/lahiruz/JS-Interview/blob/master/basics/class.md)
    
* In Javascript objects are stored as references while primitives are stored as values. Therefore, when you try to compare two objects it will only compare object references. Check following example to understand it better. 

    ```js
    var person1 = {
        firstName: 'John',
        lastName: 'Doe'
    }
        
    var person2 = {
        firstName: 'John',
        lastName: 'Doe'
    }
        
    var person3 = person1;
        
    person1 == person2; // false, allthough both have same property set, it will return false, as it is comparing memory reference.
    person1 === person2; // false
        
    person1 == person3; // true
    person1 === person3; // true
    ```

* Also you have following specific operators to do special things with objects.

    - for ... in -> for object enumeration
    ```js
    var person = {
        firstName: 'John',
        lastName: 'Doe'
    }
        
    for (var itm in person) {
        console.log(person[itm]); // print John and Doe
    }
    ```
    
    - Object.keys, Object.values & Object.entries  -> for object enumeration via object keys, values & properties
    ```js
    var person = {
        firstName: 'John',
        lastName: 'Doe'
    }
        
    Object.keys(person).map(d => {
        console.log(d); // print firstName & lastName
    });
    
    Object.values(person).map(d => {
        console.log(d); //  // print John and Doe
    });
    
    Object.entries(person).map(d => {
        console.log(d); //  // print ["firstName", "John"] and ["lastName", "Doe"]
    });
    ```
    
        
    - Object.freeze -> for creating immutable objects
    ```js
    var person = {
        firstName: 'John',
        lastName: 'Doe'
    }
        
    Object.freeze(person);
    
    person.age = 12;
    
    console.log(person); // {firstName: "John", lastName: "Doe"} return same object and won't add age proerty as it is freezed. But if you run this code in 'use strict' mode it will throw and error.
    ```
    
    - Object cloning -> to clone existing objects. 
        ```js
        var person1 = {
            firstName: 'John',
            lastName: 'Doe'
        }

        var person2 = person1; //. Note that this is not any cloning method. In here both objects are refering to same memory location.
        ```
        - Shallow cloning - copies primitive types like strings and numbers inside object. But if there are any object references, those will not be recursively copied, but instead the new, copied object will reference the same object. You can use following ways to do it.
            
            ```js
            const original = {
                name: 'Fiesta',
                car: {
                    color: 'blue',
                }
            }
            const copied = Object.assign({}, original); // using Object.assign. In this example, name primitive type will create a copy and car object will point to same memory location of car property inside original object.
            
            
            const copied = { ...original } // using ES6 spread operator
            ```
       
        - Deep cloning - copy all properties of object. There is no readily available method to do this. You can you lodash kind of third party library to perform this.

* To see more details of objects please see follwoing videos.
   - [Objects (Fundamentals)](https://www.youtube.com/watch?v=QqO8NI7i8ts&list=PLlN2Z5_OYXFoUEkrZgxVENs-_wDdifln3&index=7&ab_channel=SCIENTIA24X7)
   - [Objects (Advanced)](https://www.youtube.com/watch?v=IHVJtBPSAVY&list=PLlN2Z5_OYXFoUEkrZgxVENs-_wDdifln3&index=8&ab_channel=SCIENTIA24X7)

