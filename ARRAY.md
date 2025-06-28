# JavaScript Array Practice Assignment

## Section 1: Advanced Manipulations

1.  **`indexOf()` and `lastIndexOf()`:**

      * Given an array `colors = ["Red", "Green", "Blue", "Red", "Yellow"]`:
          * Find the first occurrence of "Red".
          * Find the last occurrence of "Red".
          * Find the index of "Purple" (what do you expect as the result?).

2.  **`includes()`:**

      * **Explain the `includes()` method:** Describe what the `includes()` method does and what it returns.
      * **Example:**
          * Check if the array `inventory = ["laptop", "mouse", "keyboard"]` includes "mouse".
          * Check if `inventory` includes "monitor".
          * Check if `numbers = [10, 20, 30]` includes `20`.
          * Check if `numbers` includes `'20'` (the string "20"). Explain the difference.

3.  **`every()`:**

      * **Explain the `every()` method:** Describe what the `every()` method does and what it returns. Provide a scenario where `every()` would be useful.
      * **Example:**
          * Given an array `ages = [18, 22, 25, 30]`, use `every()` to check if all ages are 18 or older.
          * Given an array `temps = [25, 28, 30, 22]`, use `every()` to check if all temperatures are strictly less than 30.
          * Given `productQuantities = [5, 12, 8, 3]`, use `every()` to check if all products have a quantity greater than 0.

4.  **`join()`:**

      * Given `sentenceParts = ["Hello", "world", "how", "are", "you?"]`, join them into a single string separated by a space.
      * Given `csvData = ["id", "name", "email"]`, join them with a comma to create a CSV header string.

5.  **`slice()`:**

      * Given an array `alphabets = ["a", "b", "c", "d", "e", "f"]`:
          * Create a new array containing elements from index 1 to 3 (inclusive).
          * Create a new array containing elements from index 2 to the end.
          * Create a new array containing the last two elements using a negative index.
          * Create a shallow copy of the entire `alphabets` array.

6.  **`splice()`:**

      * Given an array `planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter"]`:
          * Remove "Earth" from the array.
          * Add "Saturn" and "Uranus" after "Mars" (in the modified `planets` array).
          * Replace "Mercury" with "Sun" (this will be a tricky one, think about the position after previous operations).

7.  **`concat()`:**

      * Given `arr1 = [1, 2]` and `arr2 = [3, 4]`:
          * Concatenate `arr1` and `arr2` into a new array.
          * Concatenate `arr1`, `arr2`, and a new array `[5, 6]` in a single operation.
          * What is the difference between `arr1.concat(arr2)` and `[...arr1, ...arr2]`?

8.  **`forEach()`:**

      * Iterate over the array `users = [{ name: "Alice", id: 1 }, { name: "Bob", id: 2 }]` and log each user's name and ID (e.g., "User: Alice, ID: 1").
      * Iterate over an array `prices = [10.50, 20.00, 5.75]` and log each price formatted as "$X.XX".

9.  **`map()`:**

      * Create a new array from `numbers = [1, 2, 3, 4, 5]` where each element is doubled.
      * Create a new array from `products = [{ name: "Shirt", price: 25 }, { name: "Pants", price: 50 }]` containing only the product names.
      * Create a new array where each number in `temps = [0, 10, 20]` is converted from Celsius to Fahrenheit ($F = C \\times 9/5 + 32$).

10. **`filter()`:**

      * Filter the array `ages = [12, 18, 25, 6, 30]` to create a new array containing only ages 18 or older.
      * Filter the array `words = ["apple", "banana", "grape", "avocado"]` to create a new array containing words that start with "a".

11. **`reduce()`:**

      * Calculate the sum of all elements in `data = [10, 20, 30, 40]`.
      * Concatenate all elements in `chars = ["H", "e", "l", "l", "o"]` into a single string.
      * Given an array of transactions `transactions = [{ type: 'debit', amount: 50 }, { type: 'credit', amount: 100 }, { type: 'debit', amount: 20 }]`, calculate the net balance.

## Section 2: Advanced Concepts & Edge Cases

1.  **Truthiness of Arrays:**

      * Consider the following code:
        ```javascript
        let arr1 = [];
        let arr2 = [1, 2, 3];
        let arr3 = null;
        let arr4 = undefined;
        let arr5 = 0;
        let arr6 = "";

        if (arr1) {
            console.log("arr1 is truthy");
        } else {
            console.log("arr1 is falsy");
        }

        if (arr2) {
            console.log("arr2 is truthy");
        } else {
            console.log("arr2 is falsy");
        }

        if (arr3) {
            console.log("arr3 is truthy");
        } else {
            console.log("arr3 is falsy");
        }

        if (arr4) {
            console.log("arr4 is truthy");
        } else {
            console.log("arr4 is falsy");
        }

        if (arr5) {
            console.log("arr5 is truthy");
        } else {
            console.log("arr5 is falsy");
        }

        if (arr6) {
            console.log("arr6 is truthy");
        } else {
            console.log("arr6 is falsy");
        }
        ```
          * Without running the code, predict the output for each `console.log`.
          * Explain **why** an empty array (`[]`) and a non-empty array (`[1, 2, 3]`) are considered truthy in JavaScript's boolean context. Discuss the general rule for truthy/falsy values in JavaScript.

2.  **Array vs. String for `length` Property:**

      * Given the following:
        ```javascript
        let myArray = [10, 20, 30];
        let myString = "Hello";
        console.log(typeof myArray.length);
        console.log(typeof myString.length);
        console.log(myArray.length);
        console.log(myString.length);
        ```
      * What will be logged to the console?
      * Explain the similarity and difference in how `length` is used for arrays and strings.

3.  **Sparse Arrays:**

      * What is a "sparse array" in JavaScript?
      * Create a sparse array and demonstrate how its `length` property behaves, and what happens when you try to access an empty slot.
      * Example: `let sparseArr = [1, , 3];`

4.  **`delete` Operator on Arrays:**

      * Consider this code:
        ```javascript
        let fruits = ["Apple", "Banana", "Cherry"];
        delete fruits[1];
        console.log(fruits);
        console.log(fruits.length);
        console.log(fruits[1]);
        ```
      * Predict the output.
      * Explain why using `delete` is generally discouraged for removing elements from an array if you want to maintain contiguous indices. What method would be preferred instead?

5.  **`Array.isArray()`:**

      * Why is `Array.isArray()` preferred over `typeof` when checking if a variable is an array? Provide an example where `typeof` would be misleading.

6.  **Mutability of `sort()` and `reverse()`:**

      * Given an array `data = [3, 1, 4, 1, 5, 9, 2, 6];`
        ```javascript
        let originalData = [3, 1, 4, 1, 5, 9, 2, 6];
        let sortedData = originalData.sort();
        console.log("Original after sort:", originalData);
        console.log("Sorted data:", sortedData);

        let anotherArray = ["c", "a", "b"];
        let reversedArray = anotherArray.reverse();
        console.log("Another after reverse:", anotherArray);
        console.log("Reversed array:", reversedArray);
        ```
      * What will be logged to the console?
      * Explain the concept of "mutability" in the context of array methods like `sort()` and `reverse()`. How does this differ from methods like `map()` or `filter()`?

7.  **Shallow Copying Arrays:**

      * Given `originalArr = [1, [2, 3], 4];`
        ```javascript
        let originalArr = [1, [2, 3], 4];
        let copiedArr = [...originalArr]; // Using spread syntax for copying

        copiedArr[0] = 100;
        copiedArr[1][0] = 200; // Modifying an element within a nested array

        console.log("Original Array:", originalArr);
        console.log("Copied Array:", copiedArr);
        ```
      * Predict the output.
      * Explain what "shallow copy" means in JavaScript arrays, especially when dealing with nested structures. How would you achieve a "deep copy" if the array contained nested objects or arrays?

## Section 3: Confusing Array Output Questions

Predict the output of the following JavaScript code snippets involving arrays. Explain your reasoning for each.

1.  ```javascript
    console.log([] == []);
    ```

2.  ```javascript
    console.log([] === []);
    ```

3.  ```javascript
    console.log([] == ![]);
    ```

4.  ```javascript
    console.log([] + []);
    ```

5.  ```javascript
    console.log([1] + [2]);
    ```

6.  ```javascript
    console.log([] + {});
    ```

7.  ```javascript
    console.log({} + []);
    ```

8.  ```javascript
    let a = [];
    let b = [];
    console.log(a == b);
    console.log(a === b);
    ```

9.  ```javascript
    let c = [];
    let d = c;
    console.log(c == d);
    console.log(c === d);
    ```

10. ```javascript
    let result;
    result = [12] + [13];
    console.log(result);
    console.log(typeof result);
    ```

11. ```javascript
    console.log(+"");
    console.log(+"10");
    console.log(+[]);
    console.log(+["10"]);
    console.log(+["abc"]);
    ```

12. ```javascript
    let arr = [1, 2];
    arr[10] = 11;
    console.log(arr.length);
    console.log(arr[5]);
    ```

## Section 4: Output Prediction

For each of the following code snippets, predict the output and explain why:

1.  ```javascript
    let arr = [10, 20, 30];
    arr.push(40);
    console.log(arr.length);
    console.log(arr[2]);
    ```

2.  ```javascript
    let data = ["A", "B", "C", "D"];
    let slicedData = data.slice(1, 3);
    console.log(data);
    console.log(slicedData);
    ```

3.  ```javascript
    let values = [1, 2, 3, 4, 5];
    values.splice(2, 1, 10, 11);
    console.log(values);
    ```

4.  ```javascript
    let words = ["hello", "world"];
    let transformed = words.map(word => word.toUpperCase());
    console.log(transformed);
    ```

5.  ```javascript
    let scores = [85, 92, 78, 65, 95];
    let highScores = scores.filter(score => score > 80);
    console.log(highScores);
    ```

## Section 5: Debugging Common Mistakes

Identify and correct the errors in the following code snippets. Explain the mistake and your correction.

1.  **Problem:** Trying to access an out-of-bounds index.

    ```javascript
    let items = ["item1", "item2"];
    console.log(items[2]);
    ```

2.  **Problem:** Misunderstanding `splice()` parameters for replacement.

    ```javascript
    let colors = ["red", "green", "blue"];
    colors.splice(1, 0, "yellow"); // Goal was to replace "green" with "yellow"
    console.log(colors);
    ```

3.  **Problem:** Modifying an array while iterating with `forEach` and expecting a new array.

    ```javascript
    let originalNumbers = [1, 2, 3];
    originalNumbers.forEach(num => {
        originalNumbers.push(num * 2); // This will lead to an infinite loop or unexpected behavior
    });
    console.log(originalNumbers);
    ```

4.  **Problem:** Incorrect `reduce()` initial value for string concatenation.

    ```javascript
    let chars = ["a", "b", "c"];
    let result = chars.reduce((acc, char) => acc + char);
    console.log(result); // What if the array was empty?
    ```

## Section 6: Real-World Problem Solving

1.  **Shopping List Manager:**

      * Create an array to represent a shopping list.
      * Add at least 3 initial items.
      * Implement functions (or just plain code blocks) to:
          * Add a new item to the list.
          * Remove an item by its name (if multiple, remove the first occurrence).
          * Check if a specific item is on the list (case-insensitive).
          * Display all items in the list, numbered.
          * Clear the entire list.

2.  **Student Grade Calculator:**

      * Create an array of student names (e.g., `["Alice", "Bob", "Charlie"]`).
      * Create a corresponding array of their grades (numbers, e.g., `[85, 92, 78]`).
      * Implement logic to:
          * Find the average grade.
          * Find the highest grade.
          * Find the name of the student with the highest grade.
          * List all students who passed (assume a passing grade is 70).
          * List all students who failed.

3.  **Inventory Management:**

      * Represent an inventory using an array of objects, where each object has `name` (string), `quantity` (number), and `price` (number) properties. (e.g., `{ name: "Laptop", quantity: 5, price: 1200 }`)
      * Add at least 3 initial items.
      * Implement logic to:
          * Add a new product to the inventory.
          * Update the quantity of an existing product by its name. If the product doesn't exist, add it.
          * Remove a product by its name.
          * Calculate the total value of the entire inventory (sum of quantity \* price for all items).
          * List all products that are low in stock (e.g., quantity \< 5).
          * Find the most expensive product.
