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

Destructuring is a way I use to unpack values from an array or object into separate variables in a single line. With array destructuring, I pick values based on their position. With object destructuring, I pick values based on their property names. I use it a lot because it makes my code shorter and easier to read, especially when working with function parameters or API responses.

**🇧🇩 বাংলা**

Destructuring হলো এমন একটি উপায়, যেটা আমি একটা array বা object থেকে value বের করে এক লাইনে আলাদা আলাদা variable-এ রাখার জন্য ব্যবহার করি। Array destructuring-এ আমি value-গুলো তাদের position অনুযায়ী নিই। Object destructuring-এ আমি value-গুলো তাদের property নাম অনুযায়ী নিই। আমি এটি অনেক বেশি ব্যবহার করি, কারণ এটি আমার কোড ছোট এবং পড়তে সহজ করে তোলে, বিশেষ করে function parameter বা API response নিয়ে কাজ করার সময়।

---

## Q17. What are the spread and rest operators and how are they used?

🔑 **Keywords:**
- same `...` syntax, opposite purpose
- spread = expands elements out (array/object)
- rest = collects remaining elements into array

**🇬🇧 English**

Both spread and rest use the same three-dot syntax, but they do opposite things. I use the spread operator to expand elements out — for example, copying an array, merging objects, or passing array items as function arguments. I use the rest operator to do the opposite — collecting multiple values into a single array, usually in function parameters or during destructuring.

**🇧🇩 বাংলা**

Spread এবং rest — দুটোই একই তিন-ডট syntax ব্যবহার করে, কিন্তু এদের কাজ উল্টো। আমি spread operator ব্যবহার করি element-গুলোকে ছড়িয়ে দেওয়ার জন্য — যেমন array copy করা, object merge করা, বা array item গুলো function-এর argument হিসেবে পাঠানো। আমি rest operator ব্যবহার করি এর উল্টো কাজের জন্য — একাধিক value-কে একটা single array-তে জমা করা, সাধারণত function parameter বা destructuring-এর সময়।

---

## Q18. Explain the difference between `map()`, `filter()`, and `reduce()`.

🔑 **Keywords:**
- all work on arrays, don't mutate original
- map = transforms each item, same length
- filter = keeps items matching a condition
- reduce = combines all items into a single value

**🇬🇧 English**

All three — map, filter, and reduce — I use to work with arrays, and none of them change the original array. I use `map()` when I want to transform every item and get back a new array of the same length. I use `filter()` when I want to keep only the items that match a certain condition. I use `reduce()` when I want to combine all the items into a single value, like a total or a summary object.

**🇧🇩 বাংলা**

map, filter, এবং reduce — তিনটাই আমি array নিয়ে কাজ করার জন্য ব্যবহার করি, এবং এদের কোনোটাই original array পরিবর্তন করে না। আমি `map()` ব্যবহার করি যখন প্রতিটি item transform করে একই length-এর নতুন array পেতে চাই। আমি `filter()` ব্যবহার করি যখন শুধু নির্দিষ্ট condition মিলে যাওয়া item-গুলো রাখতে চাই। আমি `reduce()` ব্যবহার করি যখন সব item-কে একটা single value-তে একত্র করতে চাই, যেমন total বা কোনো summary object।

---

## Q19. What is the difference between `for...in` and `for...of` loops?

🔑 **Keywords:**
- for...in = iterates keys/indexes
- for...of = iterates values directly
- for...of used for arrays/iterables

**🇬🇧 English**

Both for...in and for...of I use for looping, but they iterate over different things. `for...in` loops through the keys or indexes of an object or array. `for...of` loops directly through the values of an iterable, like an array, string, or map. I mostly use `for...of` when I want the actual values, and `for...in` when I need to work with object property names.

**🇧🇩 বাংলা**

for...in এবং for...of — দুটোই আমি loop করার জন্য ব্যবহার করি, কিন্তু এরা আলাদা জিনিসের উপর iterate করে। `for...in` কোনো object বা array-এর key বা index-এর উপর দিয়ে loop করে। `for...of` সরাসরি কোনো iterable-এর value-এর উপর দিয়ে loop করে, যেমন array, string, বা map। আমি বেশিরভাগ সময় `for...of` ব্যবহার করি যখন আসল value দরকার হয়, আর `for...in` তখন ব্যবহার করি যখন object-এর property নাম নিয়ে কাজ করতে হয়।

---

## Q20. What are template literals and tagged templates?

🔑 **Keywords:**
- template literals = backticks + `${}` interpolation
- support multi-line strings
- tagged templates = function processes the literal before output

**🇬🇧 English**

Template literals are strings I write using backticks instead of quotes, which let me insert variables directly inside `${}` and also write multi-line strings easily. Tagged templates take this a step further — I attach a function before the template literal, and that function processes the string and its values before returning the final result. I mostly use plain template literals in day-to-day code, and tagged templates only for special cases like styling libraries.

**🇧🇩 বাংলা**

Template literal হলো এমন string, যেটা আমি quote-এর বদলে backtick দিয়ে লিখি, যার ফলে সরাসরি `${}`-এর ভিতরে variable বসাতে পারি এবং সহজে multi-line string-ও লিখতে পারি। Tagged template এটাকে আরেক ধাপ এগিয়ে নেয় — আমি template literal-এর আগে একটা function বসাই, আর সেই function final result return করার আগে string এবং তার value-গুলো process করে। আমি বেশিরভাগ ক্ষেত্রে সাধারণ template literal ব্যবহার করি, আর tagged template শুধু কিছু special case-এ ব্যবহার করি, যেমন styling library-তে।

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

A Promise is an object that represents a value which may not be available yet, but will be at some point in the future. It has three states — pending, fulfilled, and rejected. I use `.then()` to handle the value when the promise succeeds, and `.catch()` to handle any error if it fails. I mostly use Promises when working with things like API calls or any operation that takes time to complete.

**🇧🇩 বাংলা**

Promise হলো এমন একটা object, যা এমন একটা value represent করে যেটা এখনো available নাও থাকতে পারে, কিন্তু ভবিষ্যতে একসময় পাওয়া যাবে। এর তিনটা state আছে — pending, fulfilled, এবং rejected। আমি `.then()` ব্যবহার করি যখন promise successful হয় তখন value handle করার জন্য, আর `.catch()` ব্যবহার করি কোনো error handle করার জন্য যদি সেটা fail করে। আমি Promise মূলত API call বা সময়সাপেক্ষ কোনো operation নিয়ে কাজ করার সময় ব্যবহার করি।

---

## Q23. What is `async/await` and how does it improve upon Promises?

🔑 **Keywords:**
- syntactic sugar over Promises
- makes async code look synchronous
- easier to read/write than `.then()` chaining
- `try/catch` for error handling

**🇬🇧 English**

async/await is what I use as a cleaner way to work with Promises. It's essentially syntactic sugar built on top of Promises, but it lets my asynchronous code look and read almost like normal synchronous code. Instead of chaining multiple `.then()` calls, I just write `await` before a Promise, and I handle errors using a regular `try/catch` block. I find this much easier to read and debug compared to long Promise chains.

**🇧🇩 বাংলা**

async/await আমি Promise নিয়ে কাজ করার একটা cleaner উপায় হিসেবে ব্যবহার করি। এটা মূলত Promise-এর উপর তৈরি একটা syntactic sugar, কিন্তু এটা আমার asynchronous code-কে প্রায় normal synchronous code-এর মতো দেখতে এবং পড়তে সাহায্য করে। একাধিক `.then()` chain করার বদলে, আমি শুধু কোনো Promise-এর আগে `await` লিখি, আর error handle করার জন্য সাধারণ `try/catch` block ব্যবহার করি। এটা লম্বা Promise chain-এর তুলনায় পড়তে এবং debug করতে অনেক সহজ মনে হয় আমার কাছে।

---

## Q24. What is the difference between `call()`, `apply()`, and `bind()`?

🔑 **Keywords:**
- all set the value of `this` for a function
- call = arguments passed individually, invokes immediately
- apply = arguments passed as an array, invokes immediately
- bind = returns a new function, doesn't invoke immediately

**🇬🇧 English**

Call, apply, and bind I all use to control what `this` refers to inside a function, but they work a bit differently. With `call()`, I pass arguments individually and the function runs immediately. With `apply()`, I pass arguments as an array, but it also runs immediately. With `bind()`, the function does not run right away — instead, it returns a new function with `this` already set, which I can call later.

**🇧🇩 বাংলা**

Call, apply, এবং bind — এই তিনটাই আমি কোনো function-এর ভিতরে `this` কী হবে সেটা control করার জন্য ব্যবহার করি, কিন্তু এদের কাজের ধরন একটু আলাদা। `call()`-এ আমি argument গুলো আলাদা আলাদাভাবে পাঠাই এবং function সাথে সাথেই run হয়। `apply()`-এ আমি argument গুলো একটা array হিসেবে পাঠাই, কিন্তু এটাও সাথে সাথে run হয়। `bind()`-এ function সাথে সাথে run হয় না — এর বদলে, এটা একটা নতুন function return করে যার `this` আগে থেকেই সেট করা থাকে, যেটা আমি পরে call করতে পারি।

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