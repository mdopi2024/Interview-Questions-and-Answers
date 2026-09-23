# JavaScript Interview Questions & Answers — Day 2 (Q16–Q30)

**Topic: Arrays, Objects, ES6+ & Async**

A bilingual (English + বাংলা) collection of JavaScript interview questions with natural, speakable, interview-standard answers.


---

## Q16. What is destructuring in JavaScript? Explain with array and object examples.

🔑 **Keywords:**
- unpack values from array/object
- assign to separate variables
- shorter, cleaner syntax

**🇬🇧 English**

Destructuring is a way to take values from an array or object and store them directly in separate variables. In array destructuring, values are taken based on their position. In object destructuring, values are taken based on their property names. It makes the code shorter and easier to read.

**🇧🇩 বাংলা**

Destructuring হলো এমন একটি উপায়, যেটা ব্যবহার করে array বা object থেকে value বের করে সরাসরি আলাদা variable-এ রাখা যায়। Array destructuring-এ value position অনুযায়ী নেওয়া হয়। আর object destructuring-এ value property name অনুযায়ী নেওয়া হয়। এতে code ছোট, সহজ এবং পড়তে সুবিধা হয়।

---

## Q17. What are the spread and rest operators and how are they used?

🔑 **Keywords:**
- same `...` syntax, opposite purpose
- spread = expands elements out (array/object)
- rest = collects remaining elements into array

**🇬🇧 English**

Spread and Rest both use the three-dot (...) syntax, but they work differently. Spread expands the values of an array or object. It can be used to copy arrays, merge objects, or pass values to a function. Rest collects multiple values into a single array. It is usually used in function parameters or destructuring.

**🇧🇩 বাংলা**

Spread এবং Rest — দুটোতেই তিনটি dot (...) ব্যবহার করা হয়, কিন্তু এদের কাজ আলাদা। Spread কোনো array বা object-এর value-গুলোকে ছড়িয়ে দেয়। এটি array copy, object merge বা function-এ values পাঠাতে ব্যবহার করা যায়। Rest একাধিক value-কে একসাথে সংগ্রহ করে একটি array-তে রাখে। এটি সাধারণত function parameter বা destructuring-এর সময় ব্যবহার করা হয়।

---

## Q18. Explain the difference between `map()`, `filter()`, and `reduce()`.

🔑 **Keywords:**
- all work on arrays, don't mutate original
- map = transforms each item, same length
- filter = keeps items matching a condition
- reduce = combines all items into a single value

**🇬🇧 English**

map(), filter(), and reduce() are all used to work with arrays, but they have different purposes. map() changes each item and creates a new array. filter() keeps only the items that match a condition. reduce() combines all the items into a single value, such as a total. In general, these methods do not change the original array.

**🇧🇩 বাংলা**

map(), filter(), এবং reduce() — তিনটিই array নিয়ে কাজ করার জন্য ব্যবহার করা হয়, কিন্তু এদের কাজ আলাদা। map() প্রতিটি item পরিবর্তন করে নতুন array তৈরি করে। filter() একটি condition অনুযায়ী শুধু দরকারি item-গুলো রাখে। আর reduce() সব item-কে একসাথে করে একটি single value তৈরি করে, যেমন total। সাধারণভাবে, এগুলো original array পরিবর্তন করে না।

---

## Q19. What is the difference between `for...in` and `for...of` loops?

🔑 **Keywords:**
- for...in = iterates keys/indexes
- for...of = iterates values directly
- for...of used for arrays/iterables

**🇬🇧 English**

for...in and for...of are both used for looping, but they work differently. for...in loops through the keys or indexes of an object or array. for...of loops directly through the values of an array, string, or other iterable. Simply, for...in → key/index and for...of → value.

**🇧🇩 বাংলা**

for...in এবং for...of — দুটোই loop করার জন্য ব্যবহার করা হয়, কিন্তু এদের কাজ আলাদা। for...in object-এর key বা array-এর index নিয়ে loop করে। আর for...of সরাসরি array, string বা অন্য iterable-এর value নিয়ে loop করে। সহজভাবে, for...in → key/index এবং for...of → value।

---

## Q20. What are template literals and tagged templates?

🔑 **Keywords:**
- template literals = backticks + `${}` interpolation
- support multi-line strings
- tagged templates = function processes the literal before output

**🇬🇧 English**

A template literal is a string written using **backticks ()**. It allows us to put variables directly inside ${}` and easily write multi-line strings. A tagged template uses a function with a template literal, and the function can process the string and its values. Template literals are commonly used, while tagged templates are used for special cases.

**🇧🇩 বাংলা**

Template literal হলো এমন একটি string, যেটা **backtick ()** দিয়ে লেখা হয়। এতে ${}` ব্যবহার করে string-এর মধ্যে সরাসরি variable রাখা যায় এবং সহজে multi-line string লেখা যায়। Tagged template হলো template literal-এর সাথে একটি function ব্যবহার করা, যেখানে সেই function string এবং variable-এর value process করতে পারে। সাধারণ code-এ template literal বেশি ব্যবহার হয়, আর tagged template বিশেষ কিছু ক্ষেত্রে ব্যবহার করা হয়।

---

## Q21. What is the event loop in JavaScript?

🔑 **Keywords:**
- JavaScript is single-threaded
- call stack + callback/task queue
- event loop moves tasks from queue to stack when stack is empty
- allows async operations without blocking

**🇬🇧 English**

The event loop is the mechanism JavaScript uses to handle asynchronous code, even though JavaScript itself is single-threaded. My code runs on the call stack. When I have async tasks, like a `setTimeout` or an API call, they get moved to a queue once they're ready. The event loop constantly checks if the call stack is empty, and if it is, it takes the next task from the queue and pushes it onto the stack. This is what lets JavaScript handle things like timers and network requests without blocking the rest of the code.

**🇧🇩 বাংলা**

Event loop হলো এমন একটা mechanism, যেটা JavaScript asynchronous code handle করার জন্য ব্যবহার করে, যদিও JavaScript নিজে single-threaded। আমার কোড call stack-এর উপর run করে। যখন আমার কাছে async task থাকে, যেমন `setTimeout` বা কোনো API call, সেগুলো ready হয়ে গেলে একটা queue-তে চলে যায়। Event loop সবসময় চেক করে call stack খালি আছে কিনা, আর খালি থাকলে queue থেকে পরবর্তী task নিয়ে stack-এ push করে। এই কারণেই JavaScript timer বা network request-এর মতো কাজ বাকি কোড block না করেই handle করতে পারে।

---

## Q22. Explain how Promises work in JavaScript.

🔑 **Keywords:**
- represents a future value
- three states: pending, fulfilled, rejected
- `.then()` handles success, `.catch()` handles error

**🇬🇧 English**

A Promise is an object that represents a value that may be available later. It has three states: pending, fulfilled, and rejected. We use .then() to handle the result when the Promise succeeds, and .catch() to handle errors when it fails. Promises are commonly used for API calls and other asynchronous operations.

**🇧🇩 বাংলা**

Promise হলো এমন একটি object, যা এমন একটি value-এর জন্য ব্যবহার হয় যেটা এখন পাওয়া যায় না, কিন্তু পরে পাওয়া যেতে পারে। Promise-এর তিনটি state আছে — pending, fulfilled, এবং rejected। কাজ সফল হলে .then() দিয়ে result নেওয়া যায়, আর error হলে .catch() দিয়ে error handle করা যায়। Promise সাধারণত API call বা asynchronous কাজের জন্য ব্যবহার করা হয়।

---

## Q23. What is `async/await` and how does it improve upon Promises?

🔑 **Keywords:**
- syntactic sugar over Promises
- makes async code look synchronous
- easier to read/write than `.then()` chaining
- `try/catch` for error handling

**🇬🇧 English**

async/await is a simple and clean way to work with Promises. async makes a function asynchronous, and await waits for a Promise to finish and gives its result. It makes asynchronous code easier to read and understand. We usually use try/catch to handle errors.

**🇧🇩 বাংলা**

async/await হলো Promise নিয়ে কাজ করার সহজ এবং পরিষ্কার উপায়। async function-কে asynchronous করে, আর await কোনো Promise-এর result পাওয়া পর্যন্ত অপেক্ষা করে। এতে asynchronous code অনেকটা normal code-এর মতো সহজে পড়া যায়। Error handle করার জন্য সাধারণত try/catch ব্যবহার করা হয়।

---

## Q24. What is the difference between `call()`, `apply()`, and `bind()`?

🔑 **Keywords:**
- all set the value of `this` for a function
- call = arguments passed individually, invokes immediately
- apply = arguments passed as an array, invokes immediately
- bind = returns a new function, doesn't invoke immediately

**🇬🇧 English**

call(), apply(), and bind() are used to set the value of this inside a function. call() and apply() run the function immediately. The difference is that call() takes arguments separately, while apply() takes arguments as an array. bind() does not run the function immediately; it returns a new function that can be called later.

**🇧🇩 বাংলা**

call(), apply(), এবং bind() — তিনটিই function-এর ভিতরে this কী হবে তা ঠিক করতে ব্যবহার করা হয়। call() এবং apply() function-কে সাথে সাথে চালায়। পার্থক্য হলো, call()-এ argument আলাদা আলাদা করে দিতে হয়, আর apply()-এ argument array হিসেবে দিতে হয়। bind() function-কে সাথে সাথে চালায় না; এটি একটি নতুন function return করে, যেটা পরে call করা যায়।

---

## Q25. What is prototypal inheritance in JavaScript?

🔑 **Keywords:**
- objects inherit properties/methods from other objects
- connected via the prototype chain
- shared methods/properties, saves memory

**🇬🇧 English**

Prototypal inheritance is a system in JavaScript where one object can get properties and methods from another object. Every object has a prototype. If a property or method is not found in the object, JavaScript looks for it in its prototype. If it is not there, it continues through the prototype chain. This is why arrays can use methods like map() and filter() without defining them in every array.

**🇧🇩 বাংলা**

Prototypal inheritance হলো JavaScript-এর এমন একটি system, যেখানে একটি object অন্য object থেকে property এবং method পেতে পারে। প্রতিটি object-এর একটি prototype থাকে। কোনো property বা method object-এর মধ্যে না থাকলে JavaScript তার prototype-এ খোঁজে। সেখানেও না পেলে পরের prototype-এ খোঁজে। এভাবেই prototype chain তৈরি হয়। যেমন, array-এর মধ্যে map() বা filter() আলাদাভাবে লেখা না থাকলেও সেগুলো ব্যবহার করা যায়।

---

## Q26. Explain the concept of the `this` keyword in different contexts.

🔑 **Keywords:**
- value of `this` depends on how a function is called
- global context, object method, arrow function, explicit binding
- arrow functions inherit `this` from enclosing scope

**🇬🇧 English**

In JavaScript, the value of this depends on how the function is called. In the global context, this usually refers to the global object. Inside an object method, this refers to that object. An arrow function does not have its own this; it gets this from the surrounding scope. We can also set this using call(), apply(), or bind().
**🇧🇩 বাংলা**

JavaScript-এ this-এর value function কীভাবে call করা হয়েছে তার উপর নির্ভর করে। Global context-এ this সাধারণত global object-কে refer করে। কোনো object-এর method-এর ভিতরে this সেই object-কে refer করে। আর arrow function নিজের this তৈরি করে না; এটি বাইরের scope থেকে this নেয়। এছাড়া call(), apply(), এবং bind() ব্যবহার করে this নিজের মতো করে সেট করা যায়।

---

## Q27. What are JavaScript modules (import/export)?

🔑 **Keywords:**
- split code into separate, reusable files
- `export` shares code out, `import` brings it in
- named exports vs default export

**🇬🇧 English**

A module is a way to split JavaScript code into separate files. It makes code easier to organize and reuse. We use export to make a function, variable, or component available to another file, and import to use that code in another file. We can use named exports for multiple items and default export for one main item.

**🇧🇩 বাংলা**

Module হলো JavaScript code-কে আলাদা আলাদা file-এ ভাগ করে রাখার একটি উপায়। এতে code গুছিয়ে রাখা এবং reuse করা সহজ হয়। export দিয়ে কোনো function, variable বা component অন্য file-এ ব্যবহার করার জন্য পাঠানো হয়। আর import দিয়ে সেই code অন্য file-এ আনা হয়। একাধিক জিনিস export করার জন্য named export, আর একটি main জিনিস export করার জন্য default export ব্যবহার করা যায়।

---

## Q28. What is the difference between shallow copy and deep copy of objects?

🔑 **Keywords:**
- shallow copy = top-level copied, nested objects still shared
- deep copy = fully independent copy, including nested objects
- changing nested data affects original in shallow copy only

**🇬🇧 English**

Shallow copy and deep copy are both used to copy objects, but they work differently with nested data. A shallow copy copies only the top-level properties, so nested objects are still shared with the original. A deep copy creates a fully separate copy, including nested objects. So, changing the deep copy does not affect the original object.

**🇧🇩 বাংলা**

Shallow copy এবং deep copy — দুটোই object copy করার জন্য ব্যবহার করা হয়। Shallow copy শুধু বাইরের property-গুলো copy করে, তাই nested object থাকলে সেটা original-এর সাথে shared থাকে। আর deep copy nested object-সহ পুরো data-এর আলাদা copy তৈরি করে। তাই deep copy পরিবর্তন করলে original object পরিবর্তন হয় না।

---

## Q29. What are `WeakMap` and `WeakSet` and when would you use them?

🔑 **Keywords:**
- store objects only (not primitive values)
- weakly referenced → garbage collected automatically
- not iterable, no size property
- used for private data, caching, avoiding memory leaks

**🇬🇧 English**

WeakMap and WeakSet are similar to Map and Set, but they have some differences. WeakMap can only use objects as keys, and WeakSet can only store objects. Their references are weak, so if an object is no longer used anywhere else, JavaScript can remove it through garbage collection. They are not iterable and do not have a size property. They are mainly useful for storing extra data related to objects or creating a simple cache.

**🇧🇩 বাংলা**

WeakMap এবং WeakSet অনেকটা Map এবং Set-এর মতো, কিন্তু এদের কিছু পার্থক্য আছে। WeakMap-এ শুধু object-কে key হিসেবে রাখা যায়, আর WeakSet-এ শুধু object রাখা যায়। এদের reference weak, তাই object-এর আর কোনো reference না থাকলে JavaScript সেটাকে garbage collection-এর জন্য সরিয়ে দিতে পারে। এগুলো loop করা যায় না এবং এদের size property নেই। এগুলো সাধারণত object-এর সাথে extra data রাখা বা simple cache-এর জন্য ব্যবহার করা হয়।

---

## Q30. Explain the concept of memoization with an example.

🔑 **Keywords:**
- caches results of a function
- based on input arguments
- avoids recomputation for repeated inputs
- improves performance for expensive calculations

**🇬🇧 English**

Memoization is a technique where the result of a function is stored or cached. If the function is called again with the same input, it uses the cached result instead of calculating it again. This can improve performance, especially for heavy calculations or recursive functions.

**🇧🇩 বাংলা**

Memoization হলো এমন একটি technique, যেখানে কোনো function-এর result cache করে রাখা হয়। পরে একই input দিয়ে function আবার call হলে, নতুন করে calculation না করে আগের result ব্যবহার করা হয়। এতে একই কাজ বারবার করার দরকার হয় না এবং performance ভালো হয়। এটি সাধারণত heavy calculation বা recursive function-এর ক্ষেত্রে কাজে লাগে।

---

*Prepared for JavaScript technical interview practice — English + বাংলা, sentence-aligned for easy speaking practice.*
