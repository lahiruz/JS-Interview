# Welcome to class

* Here is few design patters in JavaScript.

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
 
  ```

## Prototype Pattern

  ```js
 
  ```

## Factory Pattern

  ```js
 
  ```
