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

Prototypal inheritance is how objects in JavaScript inherit properties and methods from other objects. Every object has an internal link to another object called its prototype, and this forms what's called the prototype chain. When I try to access a property or method that doesn't exist directly on an object, JavaScript looks up the prototype chain until it finds it. This is how, for example, all arrays get access to methods like `map()` or `filter()` without me defining them on every array.

**🇧🇩 বাংলা**

Prototypal inheritance হলো এমন একটা পদ্ধতি, যেভাবে JavaScript-এর object-গুলো অন্য object থেকে property এবং method inherit করে। প্রতিটা object-এর একটা internal link থাকে আরেকটা object-এর সাথে, যাকে prototype বলা হয়, আর এভাবেই তৈরি হয় prototype chain। যখন আমি এমন কোনো property বা method access করার চেষ্টা করি যেটা সরাসরি সেই object-এ নেই, তখন JavaScript prototype chain ধরে খুঁজতে থাকে যতক্ষণ না সেটা পায়। এই কারণেই, উদাহরণস্বরূপ, সব array-ই `map()` বা `filter()`-এর মতো method access করতে পারে, প্রতিটা array-তে আলাদাভাবে সেগুলো define না করেই।

---

## Q26. Explain the concept of the `this` keyword in different contexts.

🔑 **Keywords:**
- value of `this` depends on how a function is called
- global context, object method, arrow function, explicit binding
- arrow functions inherit `this` from enclosing scope

**🇬🇧 English**

The value of `this` in JavaScript depends entirely on how a function is called, not where it's defined. In the global context, `this` refers to the global object. Inside a regular object method, `this` refers to that object. In an arrow function, `this` doesn't get its own value — instead, it inherits `this` from the surrounding scope where it was defined. I can also control `this` explicitly using `call()`, `apply()`, or `bind()`. This is actually one of the trickier parts of JavaScript, so I try to be careful with `this` inside callbacks and event handlers.

**🇧🇩 বাংলা**

JavaScript-এ `this`-এর value সম্পূর্ণভাবে নির্ভর করে function কীভাবে call করা হচ্ছে তার উপর, function কোথায় define করা হয়েছে তার উপর না। Global context-এ, `this` global object-কে refer করে। একটা সাধারণ object method-এর ভিতরে, `this` সেই object-কে refer করে। একটা arrow function-এ, `this`-এর নিজের কোনো value থাকে না — এর বদলে, এটা সেই surrounding scope থেকে `this` inherit করে যেখানে সেটা define করা হয়েছিল। আমি `call()`, `apply()`, বা `bind()` ব্যবহার করে explicitly `this` control করতে পারি। এটা আসলে JavaScript-এর একটা tricky অংশ, তাই আমি callback এবং event handler-এর ভিতরে `this` নিয়ে সাবধান থাকি।

---

## Q27. What are JavaScript modules (import/export)?

🔑 **Keywords:**
- split code into separate, reusable files
- `export` shares code out, `import` brings it in
- named exports vs default export

**🇬🇧 English**

Modules are what I use to split my JavaScript code into separate files, so I can organize and reuse code more easily. I use `export` to make a variable, function, or component available to other files, and `import` to bring that code into another file. I can either use named exports for multiple items, or a default export for the main thing a file provides. This keeps my codebase much cleaner and easier to maintain.

**🇧🇩 বাংলা**

Module হলো এমন একটা জিনিস, যেটা আমি আমার JavaScript code-কে আলাদা আলাদা file-এ ভাগ করার জন্য ব্যবহার করি, যাতে code গুছিয়ে রাখা এবং পুনরায় ব্যবহার করা সহজ হয়। আমি `export` ব্যবহার করি কোনো variable, function, বা component-কে অন্য file-এর জন্য available করার জন্য, আর `import` ব্যবহার করি সেই code-কে আরেকটা file-এ আনার জন্য। আমি একাধিক জিনিসের জন্য named export ব্যবহার করতে পারি, অথবা একটা file-এর মূল জিনিসের জন্য default export ব্যবহার করতে পারি। এতে আমার codebase অনেক পরিষ্কার এবং maintain করা সহজ হয়ে যায়।

---

## Q28. What is the difference between shallow copy and deep copy of objects?

🔑 **Keywords:**
- shallow copy = top-level copied, nested objects still shared
- deep copy = fully independent copy, including nested objects
- changing nested data affects original in shallow copy only

**🇬🇧 English**

Both shallow copy and deep copy I use to duplicate objects, but they behave differently with nested data. A shallow copy only copies the top-level properties — if the object has nested objects inside it, those nested objects are still shared between the original and the copy. A deep copy creates a fully independent copy, including all nested objects, so changing the copy never affects the original. I use shallow copy for simple, flat objects, and deep copy when I'm working with nested data that needs to stay fully separate.

**🇧🇩 বাংলা**

Shallow copy এবং deep copy — দুটোই আমি object copy করার জন্য ব্যবহার করি, কিন্তু nested data-এর ক্ষেত্রে এদের আচরণ আলাদা। Shallow copy শুধু top-level property-গুলো copy করে — যদি object-এর ভিতরে nested object থাকে, সেগুলো original এবং copy-এর মধ্যে এখনো shared থাকে। Deep copy সম্পূর্ণভাবে independent একটা copy তৈরি করে, সব nested object সহ, ফলে copy পরিবর্তন করলে original-এ কোনো প্রভাব পড়ে না। আমি simple, flat object-এর জন্য shallow copy ব্যবহার করি, আর deep copy তখন ব্যবহার করি যখন nested data নিয়ে কাজ করি যেটা সম্পূর্ণ আলাদা থাকা দরকার।

---

## Q29. What are `WeakMap` and `WeakSet` and when would you use them?

🔑 **Keywords:**
- store objects only (not primitive values)
- weakly referenced → garbage collected automatically
- not iterable, no size property
- used for private data, caching, avoiding memory leaks

**🇬🇧 English**

WeakMap and WeakSet are similar to Map and Set, but with some important differences. They can only store objects as keys or values, not primitive values. The references they hold are weak, meaning if the object isn't used anywhere else, JavaScript can automatically garbage collect it. Unlike Map and Set, they're not iterable and don't have a size property. I mainly use them when I want to attach extra data to an object without preventing that object from being garbage collected, like storing private data or building a simple cache.

**🇧🇩 বাংলা**

WeakMap এবং WeakSet অনেকটা Map এবং Set-এর মতোই, কিন্তু কিছু গুরুত্বপূর্ণ পার্থক্য আছে। এগুলো শুধু object-কে key বা value হিসেবে রাখতে পারে, কোনো primitive value না। এদের reference weak হয়, মানে যদি সেই object আর কোথাও ব্যবহার না হয়, তাহলে JavaScript নিজে থেকেই সেটা garbage collect করতে পারে। Map এবং Set-এর মতো, এগুলো iterable না এবং এদের কোনো size property নেই। আমি এগুলো মূলত তখন ব্যবহার করি যখন কোনো object-এ extra data যোগ করতে চাই কিন্তু সেই object-কে garbage collect হওয়া থেকে আটকাতে চাই না, যেমন private data রাখা বা একটা simple cache বানানো।

---

## Q30. Explain the concept of memoization with an example.

🔑 **Keywords:**
- caches results of a function
- based on input arguments
- avoids recomputation for repeated inputs
- improves performance for expensive calculations

**🇬🇧 English**

Memoization is a technique I use to cache the result of an expensive function call, based on its input. The next time the function is called with the same input, instead of recalculating, it just returns the cached result. This can significantly improve performance for functions that are called repeatedly with the same arguments, like heavy calculations or recursive functions.

**🇧🇩 বাংলা**

Memoization হলো এমন একটা technique, যেটা আমি কোনো সময়সাপেক্ষ function call-এর result তার input-এর ভিত্তিতে cache করার জন্য ব্যবহার করি। পরের বার একই input দিয়ে function call করলে, নতুন করে calculate না করে, এটা শুধু cached result return করে। এটা performance অনেকটা বাড়িয়ে দিতে পারে এমন function-এর ক্ষেত্রে যেগুলো বারবার একই argument দিয়ে call হয়, যেমন heavy calculation বা recursive function।

---

*Prepared for JavaScript technical interview practice — English + বাংলা, sentence-aligned for easy speaking practice.*
