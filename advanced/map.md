# Map Implementation

  ```js
  function map(items, callback) {
    const mappedItems = [];

    for (let i = 0; i< items.length; i++){
      mappedItems.push(callback(items[i], i, items));
    }

    return mappedItems;
  }

  console.log(map([2, 3, 4], (a) => a * 5)) // [10, 15, 20]
 
  ```
