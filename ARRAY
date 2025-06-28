# JavaScript Array Practice Assignment

## Section 1: Fundamental Array Operations

1.  **Declaration and Initialization:**

      * Declare an empty array named `myArray`.
      * Declare an array named `fruits` initialized with the values "Apple", "Banana", and "Cherry".
      * Declare an array named `numbers` initialized with the integers from 1 to 5.

2.  **Accessing Elements:**

      * From the `fruits` array, access and log the second element.
      * From the `numbers` array, access and log the last element without knowing its length beforehand.

3.  **Modifying Elements:**

      * Change the first element of the `fruits` array to "Orange".
      * Change the third element of the `numbers` array to 10.

4.  **Array Length:**

      * Log the length of the `fruits` array.
      * Log the length of the `numbers` array.

5.  **Adding and Removing Elements (End):**

      * Add "Grape" to the end of the `fruits` array.
      * Remove the last element from the `numbers` array.

6.  **Adding and Removing Elements (Beginning):**

      * Add "Strawberry" to the beginning of the `fruits` array.
      * Remove the first element from the `numbers` array.

## Section 2: Advanced Manipulations

1.  **`indexOf()` and `lastIndexOf()`:**

      * Given an array `colors = ["Red", "Green", "Blue", "Red", "Yellow"]`:
          * Find the first occurrence of "Red".
          * Find the last occurrence of "Red".
          * Find the index of "Purple" (what do you expect as the result?).

2.  **`includes()`:**

      * Check if the `fruits` array includes "Banana".
      * Check if the `numbers` array includes 7.

3.  **`join()`:**

      * Join the elements of the `fruits` array with a comma and space (e.g., "Apple, Banana, Cherry").
      * Join the elements of the `numbers` array with a hyphen.

4.  **`slice()`:**

      * Given an array `alphabets = ["a", "b", "c", "d", "e", "f"]`:
          * Create a new array containing elements from index 1 to 3 (inclusive).
          * Create a new array containing elements from index 2 to the end.
          * Create a shallow copy of the entire `alphabets` array.

5.  **`splice()`:**

      * Given an array `planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter"]`:
          * Remove "Earth" from the array.
          * Add "Saturn" and "Uranus" after "Mars".
          * Replace "Mercury" with "Sun" (this will be a tricky one, think about it).

6.  **`concat()`:**

      * Given `arr1 = [1, 2]` and `arr2 = [3, 4]`:
          * Concatenate `arr1` and `arr2` into a new array.
          * Concatenate `arr1`, `arr2`, and a new array `[5, 6]`.

7.  **`forEach()`:**

      * Iterate over the `fruits` array and log each fruit with its index (e.g., "0: Apple", "1: Banana").
      * Iterate over the `numbers` array and log the square of each number.

8.  **`map()`:**

      * Create a new array from `numbers` where each element is doubled.
      * Create a new array from `fruits` where each fruit name is in uppercase.

9.  **`filter()`:**

      * Filter the `numbers` array to create a new array containing only even numbers.
      * Filter the `fruits` array to create a new array containing fruits that start with the letter "B".

10. **`reduce()`:**

      * Calculate the sum of all elements in the `numbers` array.
      * Concatenate all elements in the `fruits` array into a single string.

## Section 3: Output Prediction

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

## Section 4: Debugging Common Mistakes

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

## Section 5: Real-World Problem Solving

1.  **Shopping List Manager:**

      * Create an array to represent a shopping list.
      * Add at least 3 initial items.
      * Implement functions (or just plain code blocks) to:
          * Add a new item to the list.
          * Remove an item by its name.
          * Check if a specific item is on the list.
          * Display all items in the list.
          * Clear the entire list.

2.  **Student Grade Calculator:**

      * Create an array of student names.
      * Create a corresponding array of their grades (numbers).
      * Implement logic to:
          * Find the average grade.
          * Find the highest grade.
          * Find the name of the student with the highest grade.
          * List all students who passed (assume passing grade is 70).

3.  **Inventory Management:**

      * Represent an inventory using an array of objects, where each object has `name`, `quantity`, and `price` properties. (e.g., `{ name: "Laptop", quantity: 5, price: 1200 }`)
      * Add at least 3 initial items.
      * Implement logic to:
          * Add a new product to the inventory.
          * Update the quantity of an existing product.
          * Remove a product by its name.
          * Calculate the total value of the entire inventory (sum of quantity \* price for all items).
          * List all products that are low in stock (e.g., quantity \< 5).
