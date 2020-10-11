# Javascript Basics

* Javascript is standardized as **ECMAScript(ES)** which is maintained by a committee called **TC39**. Each ES version decide what kind of features will be released to Javascript language.

* Javascript is **interpreted** and **compiled** language. ([more details can be found here](https://medium.com/@lsampath999/do-you-know-how-exactly-browser-works-9f510321ee9e))

* Currently Javascript is used as both client-side([Angular](https://angular.io/), [React](https://reactjs.org/), etc.) and server-side([NodeJS](https://nodejs.org/en/)) language.

* V8 (Google Chrome, NodeJS, Electron), SpiderMonkey (Firefox), Chakra (Microsoft Edge), Javascript Core (Safari, React Native), etc… are samples for available Browser Javascript Engines out there. (If you want clear idea about how this works check my article [here](https://medium.com/@lsampath999/do-you-know-how-exactly-browser-works-9f510321ee9e))

* Everything in Javascript is an **Object** (refer [objects](https://github.com/lahiruz/JS-Interview/blob/master/basics/objects.md) section for more details).

* Javascript also called as a multi-paradigm language. That means you can do **Functional Programming** as well as **Object Oriented Programming** with JavaScript. Javascript supports OOP with [**prototypal inheritance**](https://github.com/lahiruz/JS-Interview/blob/master/basics/prototype.md).

* Javascript is automatically garbage collected language. That means, in Javascript, it automatically allocates memory when variables/objects are created and frees it when they are not used anymore.

* Javascript is a single threaded language. That means, it does one thing at a time. Now you may have a question, how it handles asynchronous operations and how it do other things that people say Javascript can do. To understand that better you need to look for [Javascript Event Loop](https://www.youtube.com/watch?v=8aGhZQkoFbQ&ab_channel=JSConf).

* as a summery we can see **Javascript is interpreted or compiled, multi-paradigm, garbage collected and single threaded language which is used in both client and server side programming**.

## variables & data types

* You can create variables using **var**, **let** and **const**.

* Javascript have **Number**, **String**, **Boolean**, **Null**, **Undefined**, **Symbol**(introduced in ES6) & **Object** data types. First 6 are primitive data types. You can use **typeof** to see the actual type of the variable. Remember Array is also a special type of an object.
