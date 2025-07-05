## JavaScript Functions Practice Assignment

## Section 1: Advanced Manipulations

1.  **Function Declaration vs. Expression:**

      * **Declaration:** Create a function declaration named `greet` that takes a `name` parameter and returns "Hello, [name]\!".
      * **Expression:** Create a function expression assigned to a variable `farewell` that takes a `name` parameter and returns "Goodbye, [name]\!".
      * Call both functions with your name and log the results.

2.  **Arrow Functions:**

      * **Basic Arrow Function:** Convert the `greet` function from above into an arrow function `arrowGreet`.
      * **Arrow Function with No Parameters:** Create an arrow function `sayHi` that returns "Hi there\!".
      * **Arrow Function with Implicit Return:** Create an arrow function `double` that takes a number and implicitly returns its doubled value.
      * Call all arrow functions and log the results.

3.  **Default Parameters:**

      * Create a function `calculateArea` that takes `length` and `width` parameters. Set `width` to have a default value of `10`.
      * Call `calculateArea` with only `length` provided.
      * Call `calculateArea` with both `length` and `width` provided.
      * Explain when default parameters are useful.

4.  **Rest Parameters (`...`):**

      * Create a function `sumAll` that takes an arbitrary number of arguments and returns their sum.
      * Call `sumAll` with 2 arguments, then with 5 arguments, and log the results.
      * Explain the purpose of rest parameters.

5.  **Spread Syntax (`...`) with Functions:**

      * Given an array `numbers = [1, 2, 3, 4, 5]`, use the spread syntax to pass these numbers as individual arguments to a function `multiply(a, b, c, d, e)` that returns `a * b * c * d * e`.
      * Explain how spread syntax differs from rest parameters.

6.  **Higher-Order Functions (HOFs):**

      * **Explain HOFs:** Describe what higher-order functions are and why they are powerful in JavaScript.
      * **Example 1 (Function returning a function):** Create a function `createMultiplier(factor)` that returns a new function. The returned function should take a `number` and return `number * factor`. Use it to create a `timesTwo` and a `timesTen` function.
      * **Example 2 (Function taking a function as argument):** Create a function `executeOperation(num1, num2, operation)` where `operation` is a callback function (e.g., `add`, `subtract`, `multiply`). Pass simple addition and subtraction functions to `executeOperation`.

7.  **Callback Functions:**

      * Create a function `processData(data, callback)` that takes an array of `data` and a `callback` function. `processData` should iterate over the `data` and call the `callback` for each item.
      * Use `processData` to:
          * Log each item to the console.
          * Log each item capitalized.

8.  **Immediately Invoked Function Expressions (IIFEs):**

      * **Explain IIFEs:** Describe what an IIFE is and its primary use case.
      * **Example:** Create an IIFE that logs "This runs immediately\!" to the console.
      * Create another IIFE that takes a parameter (e.g., `message`) and logs it.

9.  **Closures:**

      * **Explain Closures:** Describe the concept of a closure in JavaScript and its significance.
      * **Example:** Create a function `makeCounter()` that returns a function. The returned function should increment and return a private counter variable. Demonstrate its usage to create independent counters.

10. **`this` Keyword in Functions:**

      * **Global Context:** Log `this` outside any function.
      * **Regular Function:** Create a regular function `showThis` and log `this` inside it. Call `showThis()` directly.
      * **Arrow Function:** Create an arrow function `showArrowThis` and log `this` inside it. Call `showArrowThis()` directly. Explain the difference in `this` binding between regular and arrow functions.
      * **Method on an Object:** Create an object `person = { name: "Alice", greet: function() { console.log(this.name); } }`. Call `person.greet()`.
      * **Challenging `this`:** Consider `let greeter = person.greet; greeter();`. Predict the output and explain why.

11. **`call()`, `apply()`, and `bind()`:**

      * Given an object `car = { brand: "Toyota", honk: function() { console.log(this.brand + " honks!"); } }`.
      * And another object `bike = { brand: "Harley" }`.
      * Use `call()` to make `car.honk` execute with `bike` as its `this` context.
      * Use `apply()` with `car.honk` and `bike`. What is the primary difference in how arguments are passed to `call` vs. `apply`?
      * Use `bind()` to create a new function `bikeHonk` that is permanently bound to `bike`, then call `bikeHonk()`.

## Section 2: Advanced Concepts & Edge Cases

1.  **Function Hoisting:**

      * **Declaration:** Write code where you call a function *before* its declaration.
      * **Expression:** Write code where you try to call a function *before* its expression assignment.
      * Explain the difference in hoisting behavior between function declarations and function expressions.

2.  **Function Arity:**

      * What is "function arity"?
      * Demonstrate how to find the arity of a function using the `length` property.
      * Example: `function sum(a, b, c) {}`

3.  **Recursion:**

      * What is recursion? Provide a simple scenario where recursion is useful.
      * Create a recursive function to calculate the factorial of a number. (e.g., `factorial(5) = 5 * 4 * 3 * 2 * 1`).
      * What is the base case in your factorial function? Why is it important?

4.  **Pure Functions:**

      * **Explain Pure Functions:** Describe the two main characteristics of a pure function.
      * **Example (Pure):** Write a pure function `add(a, b)` that returns `a + b`.
      * **Example (Impure):** Write an impure function `addToGlobal(num)` that modifies a global variable. Explain why it's impure.
      * Discuss the benefits of using pure functions.

5.  **Currying:**

      * What is function currying?
      * Transform a function `sumThree(a, b, c)` into a curried version `curriedSum(a)(b)(c)`.
      * Demonstrate how to use the curried function.

6.  **Memoization:**

      * What is memoization? Why is it used?
      * Create a function `memoizedFactorial` that memoizes the results of the factorial calculation to improve performance for repeated calls with the same argument.

7.  **`arguments` Object (Legacy):**

      * Explain what the `arguments` object is in JavaScript functions.
      * Demonstrate its use to access function arguments.
      * Discuss why `arguments` is generally discouraged in modern JavaScript and what preferred alternatives exist (e.g., rest parameters).

## Section 3: Confusing Function Output Questions

Predict the output of the following JavaScript code snippets involving functions. Explain your reasoning for each.

1.  ```javascript
    function greet() {
        console.log("Hello!");
    }
    console.log(greet());
    ```

2.  ```javascript
    let x = 10;
    function modifyX() {
        x = 20;
    }
    modifyX();
    console.log(x);
    ```

3.  ```javascript
    function outer() {
        let a = 1;
        function inner() {
            console.log(a);
        }
        inner();
    }
    outer();
    ```

4.  ```javascript
    function outer() {
        let a = 1;
        return function() {
            console.log(a);
        };
    }
    let innerFunc = outer();
    innerFunc();
    ```

5.  ```javascript
    function delayedMessage() {
        for (var i = 0; i < 3; i++) {
            setTimeout(function() {
                console.log(i);
            }, 100);
        }
    }
    delayedMessage();
    ```

6.  ```javascript
    function anotherDelayedMessage() {
        for (let i = 0; i < 3; i++) {
            setTimeout(function() {
                console.log(i);
            }, 100);
        }
    }
    anotherDelayedMessage();
    ```

7.  ```javascript
    const myObject = {
        value: 42,
        getValue: function() {
            return this.value;
        }
    };
    const getValueRef = myObject.getValue;
    console.log(getValueRef());
    ```

8.  ```javascript
    const anotherObject = {
        value: 100,
        getValue: () => {
            return this.value;
        }
    };
    console.log(anotherObject.getValue());
    ```

9.  ```javascript
    function execute(func) {
        func();
    }
    function saySomething() {
        console.log("Something");
    }
    execute(saySomething);
    ```

10. ```javascript
    function createAdder(x) {
        return function(y) {
            return x + y;
        };
    }
    const addFive = createAdder(5);
    console.log(addFive(10));
    ```

## Section 4: Output Prediction

For each of the following code snippets, predict the output and explain why:

1.  ```javascript
    function processNumbers(a, b, ...rest) {
        console.log(a);
        console.log(b);
        console.log(rest);
    }
    processNumbers(10, 20, 30, 40, 50);
    ```

2.  ```javascript
    const multiplyBy = (factor) => (number) => number * factor;
    const timesThree = multiplyBy(3);
    console.log(timesThree(7));
    ```

3.  ```javascript
    let count = 0;
    const increment = () => {
        count++;
        return count;
    };
    console.log(increment());
    console.log(increment());
    ```

4.  ```javascript
    function outerScope() {
        let val = 'outer';
        function innerScope() {
            let val = 'inner';
            console.log(val);
        }
        innerScope();
        console.log(val);
    }
    outerScope();
    ```

5.  ```javascript
    function calculate(operation, x, y) {
        return operation(x, y);
    }
    console.log(calculate((a, b) => a * b, 5, 4));
    ```

## Section 5: Debugging Common Mistakes

Identify and correct the errors in the following code snippets. Explain the mistake and your correction.

1.  **Problem:** Incorrect `this` context in an event handler (simulated).

    ```javascript
    const button = {
        text: 'Click Me',
        handler: function() {
            console.log(`Button ${this.text} was clicked.`); // 'this' is wrong here
        }
    };

    // Simulate an event listener calling the handler
    // setTimeout(button.handler, 100); // How it might be called in real-world
    button.handler(); // Direct call to observe the 'this' issue
    ```

2.  **Problem:** Accidental global variable creation without `var`, `let`, or `const`.

    ```javascript
    function setGlobalValue() {
        myValue = "I am global now!"; // Missing declaration keyword
    }
    setGlobalValue();
    console.log(myValue);
    ```

3.  **Problem:** Forgetting to return a value from a function that's expected to produce one.

    ```javascript
    function addNumbers(a, b) {
        let sum = a + b;
        // Missing return statement
    }
    let total = addNumbers(5, 3);
    console.log(total);
    ```

4.  **Problem:** Infinite recursion due to missing or incorrect base case.

    ```javascript
    function countdown(n) {
        console.log(n);
        countdown(n - 1); // No base case
    }
    // countdown(3); // Uncomment to see the error
    ```

## Section 6: Real-World Problem Solving

1.  **User Authentication Module:**

      * Create a function `createUser(username, password)` that returns a user object. The user object should contain a `username` and a method `checkPassword(attemptedPassword)`. The `checkPassword` method should *privately* store the original password and compare it to the `attemptedPassword`. (Hint: use a closure).
      * Create a function `authenticateUser(userObject, inputPassword)` that uses the `checkPassword` method of the `userObject` to determine if the input password is correct.
      * Demonstrate creating a user and then authenticating with correct and incorrect passwords.

2.  **Simple Calculator Factory:**

      * Create a higher-order function `createCalculator(operationType)` that takes a string (`"add"`, `"subtract"`, `"multiply"`, `"divide"`) and returns a new function.
      * The returned function should take two numbers (`a`, `b`) and perform the specified operation.
      * Handle division by zero within the returned function.
      * Use `createCalculator` to create `addNumbers`, `subtractNumbers`, `multiplyNumbers`, and `divideNumbers` functions.
      * Demonstrate using each created function.

3.  **Event Logger:**

      * Create a function `createLogger(prefix)` that takes a `prefix` string (e.g., "APP", "ERROR", "DEBUG"). It should return a function that takes a `message` and logs it to the console in the format: `[PREFIX] TIMESTAMP: MESSAGE`.
      * The timestamp should be generated inside the returned function (e.g., using `new Date().toISOString()`).
      * Create different loggers: `appLogger`, `errorLogger`, `debugLogger`.
      * Demonstrate logging messages using each logger.
