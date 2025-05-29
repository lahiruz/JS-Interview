# Welcome to design patterns

* Here is few design patterns in JavaScript.

## Module Pattern

  ```js
const MathUtils = (() => {
    function add(a, b) {
      return a + b;
    }

    return { add: addNumbers };
})();

console.log(MathUtils.addNumbers(2, 4)); // 6
 
  ```

## Revealing Module Pattern

  ```js
const MathUtils = (() => {
    function add(a, b) {
      return a + b;
    }

    // module internals will be revealed as it is unlike the Module Pattern.
    // That is why it is different from Module Pattern.
    return { add };
})();

console.log(MathUtils.add(4, 4)); // 8

  ```

## Singleton Pattern

  ```js
const Config = (function () {
  let instance = null;

  function ConfigConstructor() {
    this.apiUrl = 'https://api.example.com';
    this.debug = true;
  }

  function createInstance() {
    console.log('initiating');
    return new ConfigConstructor();
  }

  function getInstance() {
    if (instance == null) {
      instance = createInstance();
    }

    return instance;
  }

  return getInstance;
})();

const a = Config();
const b = Config();
 
  ```

## Prototype Pattern

  ```js
 
  ```

## Factory Pattern

  ```js
 
  ```
