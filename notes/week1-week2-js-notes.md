WEEK 1 — JavaScript Foundations

1. Arrow Functions

Shorter function syntax

Syntax: () => {}

If returning directly → no {}

If returning object → wrap in ({ })

Examples:

const add = (a, b) => a + b;
const greet = name => `Hello ${name}`;
const getObj = () => ({ name: "Boss" });

2. Array Methods
   map() – transform each item

Returns NEW array.

[1,2,3].map(n => n \* 2); // [2,4,6]

filter() – keep matching items
[1,2,3].filter(n => n > 2); // [3]

some() – at least ONE item satisfies
[1,2,3].some(n => n > 2); // true

every() – ALL items satisfy
[1,2,3].every(n => n > 0); // true

includes() – primitive only
[1,2,3].includes(2); // true

sort() – compare two values
nums.sort((a, b) => a - b); // ascending
nums.sort((a, b) => b - a); // descending

3. reduce() – summarize array
   [1,2,3].reduce((acc, n) => acc + n, 0);

WEEK 2 — DOM + EVENTS + ASYNC

1. DOM Basics

DOM = JS view of HTML.

Selectors:

document.getElementById("id");
document.querySelector(".class");
document.querySelectorAll("p");

Element properties:

innerText

innerHTML

value

style

id

className

classList

2. classList
   el.classList.add("active");
   el.classList.remove("hidden");
   el.classList.toggle("open");
   el.classList.contains("error");

3. Events
   element.addEventListener("click", handler);

Event types:

click

input

change

keydown

submit

Avoid:

input.addEventListener inside another event

4. preventDefault()

Stops page refresh on form submit.

5. Async JavaScript

JS is:

non-blocking

single-threaded

async by default

Browser handles:

timers

network

user input

JS continues while waiting.

6. Promises
   new Promise((resolve, reject) => { ... });

States:

pending

fulfilled

rejected

Use:

p.then(res => ...)
.catch(err => ...)

7. async / await

Rules:

Function must be async

await pauses only inside that function

UI does NOT freeze

async function demo() {
let data = await p;
console.log(data);
}

8. try / catch with async
   async function load() {
   try {
   let d = await p;
   console.log(d);
   } catch (err) {
   console.log("Error:", err);
   }
   }

Success → inside try
Failure → jump to catch

9. DOM + Async Example
   btn.addEventListener("click", async () => {
   msg.innerText = "Loading...";

try {
let data = await fakeCall();
msg.innerText = data;
} catch (err) {
msg.innerText = "Error: " + err;
}
});
