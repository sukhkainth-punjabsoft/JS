# JavaScript Array Practice Assignment

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
