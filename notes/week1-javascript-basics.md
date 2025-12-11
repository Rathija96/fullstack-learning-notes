# Week 1 – JavaScript Basics (Boss × Madam LED Notes)

This week covers the most important JS fundamentals required for DOM, backend, and full-stack development.

These notes capture exactly what Madam LED learned with Boss, explained in simple, beginner-friendly, real-world style.

## 1. Arrow Functions

Arrow functions are a shorter way to write functions.

Syntax
const add = (a, b) => a + b;

Why useful?

Cleaner

Used in array methods (map, filter, reduce…)

Used in async code, React, callbacks, etc.

Important: Returning Objects

When returning an object, wrap with parentheses:

() => ({ name: "Arun", age: 28 })


Without parentheses → JS thinks {} is a function body.

## 2. Callback Functions (Very Important Concept)

A callback = function passed into another function.

Example:

setTimeout(() => console.log("Done"), 1000);


Used everywhere:

map

filter

reduce

find

events

async operations

## 3. Array Method: map()

Used to transform each value and return a new array.

Example:
let nums = [1,2,3];
let doubled = nums.map(n => n * 2);  
// [2,4,6]

Key Points:

Does NOT modify original array

Always returns new array

Used for UI rendering, formatting, transformations

## 4. Array Method: filter()

Used to keep only matching items.

Example:

let nums = [2, 5, 8, 12];
let above5 = nums.filter(n => n > 5);
// [8, 12]

Key Points:

Returns new array

Length may reduce

Very useful for search, filtering UI lists

## 5. Array Method: reduce()

Used to combine values into a single result.

Examples:

Sum:
nums.reduce((acc, n) => acc + n, 0);

Max:
nums.reduce((acc, n) => n > acc ? n : acc);

Counting objects:
items.reduce((acc, item) => {
  acc[item] = (acc[item] || 0) + 1;
  return acc;
}, {});

## 6. Array Method: find()

Returns first element matching condition.

users.find(u => u.name === "Kumar");


If nothing found → undefined.

## 7. Array Method: findIndex()

Returns index of the first matching element.

nums.findIndex(n => n > 10);


If nothing found → -1.

## 8. Array Method: some()

Returns true if AT LEAST ONE item matches.

Examples:

nums.some(n => n > 10);
users.some(u => u.role === "admin");


Real-world: password weakness checks.

## 9. Array Method: every()

Returns true ONLY IF all items match.

nums.every(n => n > 0);


Used for form validation:

fields.every(f => f.trim() !== "");

## 10. includes()

Checks if an array contains a value.

[1,2,3].includes(2); // true


But VERY IMPORTANT:

❌ Does NOT work for checking objects

Because objects are compared by reference, not content.

items.includes({name:"Bread"}) // false

## 11. forEach()

Used for looping but does not return anything.

nums.forEach(n => console.log(n));


Used for logging, updating totals, debugging.

## 12. Object Reference Basics

Objects are stored by memory reference.

let a = {x:10};
let b = a;   // b points to SAME object


Comparing objects checks reference, not content.

This explains why includes() fails for objects.

## 13. Conditional (Ternary) Operator
condition ? valueIfTrue : valueIfFalse


Example:

age >= 18 ? "Adult" : "Minor";


Used in:

reduce() max logic

UI conditional rendering

quick decisions in code

## 14. Sorting Basics (a-b & b-a)

Ascending:

arr.sort((a,b) => a - b);


Descending:

arr.sort((a,b) => b - a);


Full advanced sorting will be taught later.

## End of Week 1 Summary
✔ Arrow functions
✔ Callback functions
✔ map / filter / reduce
✔ find / findIndex
✔ some / every / includes
✔ forEach
✔ Object reference
✔ Ternary
✔ Basic sorting

These are the foundation for DOM, backend logic, and React state updates.
