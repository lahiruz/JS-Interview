# Array Filter Implementation

  ```js
function filter(items, callback) {
    const mappedItems = [];

    for (let i = 0; i < items.length; i++) {
      const valueFiltered = callback(items[i], i, items);
      if (valueFiltered) {
        mappedItems.push(items[i]);
      }
    }

    return mappedItems;
}

console.log(filter([2, 3, 4], a => a > 3)); // [4]
 
  ```
