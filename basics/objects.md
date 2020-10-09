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
    - Object.create
        - The first argument you give Object.create is the object to use as the prototype of the object it creates.
    
       ```js
        var person = {
            firstName: 'John',
            lastName: 'Doe'
        }
        
        var boy = Object.create(person); // This will create an empty object but person object will set as the prototype of the boy object. In Chrome you can see prototype of an object using __proto__ property. Ex: boy.__proto__ 
        ```
        - Also [read this](https://stackoverflow.com/questions/16666231/difference-between-object-createobject-prototype-object-createobject-and-o#:~:text=var%20o%20%3D%20Object.-,create(Object)%3B,a%20function%20as%20its%20prototype.) if you still have questions.
    
    - Using constructor function
    - Using ES6 classes
    
* In Javascript objects are stored as references while primitives are stored as values. Therefore, when you try to compare two objects it will only compare object references.

* To see more details of objects please see follwoing videos.
   - [Objects (Fundamentals)](https://www.youtube.com/watch?v=QqO8NI7i8ts&list=PLlN2Z5_OYXFoUEkrZgxVENs-_wDdifln3&index=7&ab_channel=SCIENTIA24X7)
   - [Objects (Advanced)](https://www.youtube.com/watch?v=IHVJtBPSAVY&list=PLlN2Z5_OYXFoUEkrZgxVENs-_wDdifln3&index=8&ab_channel=SCIENTIA24X7)

