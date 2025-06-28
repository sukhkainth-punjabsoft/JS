Confusing Object Output Questions
Predict the output of the following JavaScript code snippets involving objects. Explain your reasoning for each.

JavaScript

const obj1 = { a: 1 };
const obj2 = { a: 1 };
console.log(obj1 == obj2);
console.log(obj1 === obj2);
JavaScript

const objA = { b: 2 };
const objB = objA;
console.log(objA == objB);
console.log(objA === objB);
JavaScript

const myObj = { value: 10 };
const anotherObj = myObj;
myObj.value = 20;
console.log(anotherObj.value);
JavaScript

let obj = {};
if (obj) {
    console.log("Object is truthy");
} else {
    console.log("Object is falsy");
}
JavaScript

console.log({} + []);
JavaScript

console.log([] + {});
JavaScript

let x = { a: 1 };
let y = { b: 2 };
console.log(x + y);
JavaScript

const key = "name";
const person = { [key]: "Alice" };
console.log(person.name);
JavaScript

const dynamicKey = "age";
const value = 30;
const info = { [dynamicKey]: value };
console.log(info.age);
JavaScript

const obj = {
    prop: 10,
    getProp: function() {
        return this.prop;
    }
};
const getIt = obj.getProp;
console.log(getIt());
JavaScript

const user = {
    name: "Bob",
    greet: () => {
        console.log(`Hello, my name is ${this.name}`);
    }
};
user.greet();
JavaScript

const data = {
    value: 5,
    double: () => {
        return this.value * 2;
    }
};
console.log(data.double());
Section 3: Output Prediction
For each of the following code snippets, predict the output and explain why:

JavaScript

const car = {
    make: "Toyota",
    model: "Camry",
    year: 2020
};
car.year = 2023;
console.log(car.year);
console.log(car.color); // Accessing non-existent property
JavaScript

const student = { name: "Eve", age: 22 };
student.course = "Computer Science";
console.log(Object.keys(student).length);
delete student.age;
console.log(student);
JavaScript

const book = { title: "1984", author: "George Orwell" };
for (let key in book) {
    console.log(`${key}: ${book[key]}`);
}
JavaScript

const settings = { volume: 50, brightness: 80 };
const newSettings = { ...settings, brightness: 90, mode: "dark" };
console.log(newSettings);
console.log(settings);
JavaScript

const album = {
    title: "Thriller",
    artist: "Michael Jackson",
    year: 1982,
    getDetails: function() {
        return `${this.title} by ${this.artist}, released in ${this.year}.`;
    }
};
console.log(album.getDetails());
Section 4: Debugging Common Mistakes
Identify and correct the errors in the following code snippets. Explain the mistake and your correction.

Problem: Trying to access a property with a space in its name using dot notation.

JavaScript

const movie = { "movie title": "Inception", director: "Christopher Nolan" };
console.log(movie.movie title);
Problem: Accidentally creating a global variable instead of an object property within a method due to this context.

JavaScript

const counter = {
    count: 0,
    increment: function() {
        setTimeout(function() {
            this.count++; // 'this' is not what you expect here
            console.log(this.count);
        }, 100);
    }
};
counter.increment();
Problem: Attempting to iterate over an object using forEach.

JavaScript

const scores = { math: 90, science: 85, history: 75 };
scores.forEach((value, key) => {
    console.log(`${key}: ${value}`);
});
Problem: Modifying a "constant" object property in a way that doesn't cause an error, but might be unexpected.

JavaScript

const CONFIG = {
    API_KEY: "abc123",
    MAX_RETRIES: 5
};
CONFIG.API_KEY = "new_key"; // This is allowed!
console.log(CONFIG.API_KEY);
How would you prevent API_KEY from being modified if CONFIG itself cannot be reassigned?

Section 5: Real-World Problem Solving
User Profile Manager:

Create an object to represent a user profile with properties like username, email, age, isActive, and roles (an array of strings).

Implement functions (or plain code blocks) to:

Initialize a new user profile with default values.

Update a user's email.

Toggle a user's isActive status.

Add a new role to the roles array (ensure no duplicates).

Remove a specific role from the roles array.

Check if a user has a specific role.

Display the full user profile details.

Product Catalog:

Represent a product using an object with properties: id, name, price, stock, and categories (an array of strings).

Create an array to act as your product catalog, containing several product objects.

Implement logic to:

Add a new product to the catalog.

Find a product by its id.

Update a product's stock by id.

Filter products by a given category.

Calculate the total inventory value for all products (sum of price * stock).

List all products that are out of stock (stock === 0).

Blog Post System:

Represent a blog post as an object with id, title, content, author, tags (an array of strings), and comments (an array of comment objects, where each comment has commentId, user, and text).

Create an array to hold multiple blog post objects.

Implement functions to:

Add a new blog post.

Add a new comment to a specific blog post (by id).

Find all posts by a specific author.

Find all posts that contain a specific tag.

Delete a comment from a specific post by commentId.

Count the total number of comments for a given post.
