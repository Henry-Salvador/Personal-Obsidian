Array.every(callback)

The Array `.every(callback)` method returns `true` when **every** item in the array satisfies the condition provided in the callback

```javascript
const numbers = [15, 10, 20];

const allAbove10 = numbers.every(number => number >= 10); // true
const allAbove15 = numbers.every(number => number >= 15); // false
```

Array.some(callback)

Similarly, the Array `.some(callback)` method returns `true` when **at least one** item in the array satisfies the condition provided in the callback

```javascript
const numbers = [15, 10, 20];

const someOver18 = numbers.some(number => number >= 18); // true
const someUnder10 = numbers.some(number => number < 10); // false
```

Recap

-   The Array .every(callback) method returns true when every item in the array satisfies the condition provided in the callback.
-   The Array .some(callback) method returns true when at least one item in the array satisfies the condition provided in the callback.

Say you've got an array and you'd like to empty it, you can do that by setting its length to 0:

Array.splice()

You can also delete specific items from an array using the `splice(start[, deleteCount])` method

Did you notice the `[, deleteCount]` syntax? You will often see this syntax in documentation, which means that the `deleteCount` parameter is **optional**

The `.splice(start[, deleteCount])` method removes items from the array starting from the `start` index that you specify. If no `deleteCount` is provided, it will remove all the remaining items as of the `start` index