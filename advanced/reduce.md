# Array Reduce Implementation

  ```js
function reduce(items, callback, initialValue) {
    let accumulator = initialValue;

    for (let i = 0; i < items.length; i++) {
      accumulator = callback(accumulator, items[i], i, items);
    }

    return accumulator;
}

console.log(reduce([2, 3, 4], (a, c) => a + c, 0)); // 9
 
  ```
  
## Optimized reduce Function with Optional initialValue

  ```js
function reduce(items, callback, initialValue) {
    let hasInitial = arguments.length >= 3;
    let accumulator = hasInitial ? initialValue : items[0];
    let startIndex = hasInitial ? 0 : 1;

    for (let i = startIndex; i < items.length; i++) {
      accumulator = callback(accumulator, items[i], i, items);
    }

    return accumulator;
}

console.log(reduce([2, 3, 4], (a, c) => a + c, 0)); // 9
 
  ```
