# JavaScript Interview Questions & Answers (Q1–Q15)

A bilingual (English + বাংলা) collection of JavaScript interview questions with natural, speakable, interview-standard answers.

---

## Q1. What is the difference between `var`, `let`, and `const`?

🔑 **Keywords:**
- var = old way, can redeclare/update
- let = can update, not redeclare (same block)
- const = cannot update or redeclare
- default to const, use let when value changes

**🇬🇧 English**

Both var, let, and const I use to create variables in JavaScript, but they work differently. `var` is the old way to create variables — it can be redeclared and updated, which sometimes causes unexpected bugs. `let` is what I use when the value needs to change later; it can be updated but not redeclared in the same block. `const` is what I use when the value should never change — it cannot be updated or redeclared. In my projects, I usually use `const` by default and switch to `let` only when the value actually needs to change.

**🇧🇩 বাংলা**

var, let, এবং const — তিনটাই আমি JavaScript-এ variable তৈরি করার জন্য ব্যবহার করি, কিন্তু এদের কাজের ধরন আলাদা। `var` হলো পুরনো পদ্ধতি — এটি আবার declare এবং update করা যায়, যার ফলে অনেক সময় অপ্রত্যাশিত bug হতে পারে। `let` আমি তখন ব্যবহার করি যখন পরে value পরিবর্তন করতে হবে — এটি update করা যায়, কিন্তু একই block-এ আবার declare করা যায় না। `const` আমি তখন ব্যবহার করি যখন value কখনোই পরিবর্তন হবে না — এটি update বা redeclare কোনোটাই করা যায় না। আমার প্রজেক্টে আমি সাধারণত ডিফল্টভাবে `const` ব্যবহার করি, আর যদি value পরিবর্তন করতে হয় তাহলে `let`-এ switch করি।

---

## Q2. Explain the concept of Hoisting in JavaScript.

🔑 **Keywords:**
- JS knows variables/functions before running code
- var → undefined if used before declaration
- let/const → ReferenceError if used before declaration
- always declare before use

**🇬🇧 English**

Hoisting means JavaScript knows about variables and functions before it actually runs the code. With `var`, if I use a variable before declaring it, JavaScript returns `undefined`. With `let` and `const`, if I use them before declaring them, JavaScript throws a `ReferenceError` instead. That's why I always declare my variables before using them.

**🇧🇩 বাংলা**

Hoisting মানে হলো JavaScript কোড আসলে run করার আগেই variable এবং function সম্পর্কে জেনে যায়। `var`-এর ক্ষেত্রে, declare করার আগে ব্যবহার করলে JavaScript `undefined` return করে। `let` এবং `const`-এর ক্ষেত্রে, declare করার আগে ব্যবহার করলে JavaScript এর বদলে `ReferenceError` দেয়। এই কারণে আমি সবসময় variable ব্যবহারের আগে সেটা declare করি।

---

## Q3. What are the primitive data types in JavaScript?

🔑 **Keywords:**
- basic/fundamental data types
- 7 types total
- String, Number, Boolean, Undefined, Null, Symbol, BigInt

**🇬🇧 English**

Primitive data types are the basic data types in JavaScript. There are seven primitive data types in total: String, Number, Boolean, Undefined, Null, Symbol, and BigInt. In my projects, I mostly work with String, Number, Boolean, Undefined, and Null.

**🇧🇩 বাংলা**

Primitive data type হলো JavaScript-এর মৌলিক বা বেসিক data type। JavaScript-এ মোট ৭টা primitive data type আছে: String, Number, Boolean, Undefined, Null, Symbol, এবং BigInt। আমার প্রজেক্টে আমি সবচেয়ে বেশি String, Number, Boolean, Undefined, এবং Null নিয়ে কাজ করি।

---

## Q4. What is the difference between `==` and `===`?

🔑 **Keywords:**
- both compare values
- == compares value only, converts type
- === compares value + type, no conversion
- prefer === for accuracy

**🇬🇧 English**

Both `==` and `===` I use to compare two values, but they behave differently. `==` compares only the values — if the data types are different, JavaScript automatically converts one type before comparing. `===` compares both the value and the data type, without converting anything. That's why I always use `===`, since it gives more accurate and predictable results.

**🇧🇩 বাংলা**

`==` এবং `===` — দুটোই আমি দুটো value তুলনা করার জন্য ব্যবহার করি, কিন্তু এদের আচরণ আলাদা। `==` শুধু value তুলনা করে — যদি data type আলাদা হয়, তাহলে JavaScript compare করার আগে একটাকে অন্যটায় convert করে নেয়। `===` value এবং data type দুটোই তুলনা করে, কোনো conversion ছাড়াই। এই কারণে আমি সবসময় `===` ব্যবহার করি, কারণ এটি বেশি accurate এবং predictable result দেয়।

---

## Q5. Explain how closures work in JavaScript.

🔑 **Keywords:**
- inner function accesses outer function's variables
- works even after outer function finishes
- remembers values, keeps data private

**🇬🇧 English**

A closure is when an inner function can access the variables of its outer function, even after the outer function has already finished running. It remembers those variables and can keep using them later. I find closures especially useful for remembering values across calls and for keeping certain data private.

**🇧🇩 বাংলা**

Closure হলো এমন একটি বিষয়, যেখানে একটি inner function তার outer function-এর variable access করতে পারে, এমনকি outer function শেষ হয়ে যাওয়ার পরেও। এটি সেই variable-গুলো মনে রাখে এবং পরেও ব্যবহার করতে পারে। আমি closure বিশেষভাবে useful মনে করি value মনে রাখার জন্য এবং কিছু data private রাখার জন্য।

---

## Q6. What is the difference between `null` and `undefined`?

🔑 **Keywords:**
- both mean "no value" but different
- undefined = declared, no value assigned yet
- null = intentionally set to empty

**🇬🇧 English**

Both null and undefined mean there is no value, but they're used differently. `undefined` means a variable has been declared but no value has been assigned to it yet. `null` means I've intentionally set the value to empty. In short — `undefined` is "no value yet," and `null` is "empty value on purpose."

**🇧🇩 বাংলা**

null এবং undefined — দুটোরই মানে হলো কোনো value নেই, কিন্তু এদের ব্যবহার আলাদা। `undefined` মানে variable declare করা হয়েছে কিন্তু এখনো কোনো value assign করা হয়নি। `null` মানে আমি ইচ্ছাকৃতভাবে value খালি রেখেছি। সংক্ষেপে — `undefined` হলো "এখনো value নেই", আর `null` হলো "ইচ্ছাকৃতভাবে খালি value"।

---

## Q7. What are Arrow Functions and how do they differ from Regular Functions?

🔑 **Keywords:**
- shorter way to write functions
- main difference is syntax
- both do same job, arrow = less code
- common in React

**🇬🇧 English**

Both arrow functions and regular functions I use to write functions in JavaScript, but the main difference between them is syntax. Arrow functions are a shorter way to write the same logic — both do the same job, but arrow functions need less code. In my React projects, I mostly use arrow functions because they're shorter and easier to read.

**🇧🇩 বাংলা**

Arrow function এবং regular function — দুটোই আমি JavaScript-এ function লেখার জন্য ব্যবহার করি, কিন্তু এদের মূল পার্থক্য হলো syntax-এ। Arrow function একই logic লেখার একটি ছোট উপায় — দুটোই একই কাজ করে, কিন্তু arrow function-এ কম কোড লাগে। আমার React প্রজেক্টে আমি বেশিরভাগ সময় arrow function ব্যবহার করি, কারণ এটি ছোট এবং পড়তে সহজ।

---

## Q8. What is the Scope Chain in JavaScript?

🔑 **Keywords:**
- how JS searches for a variable
- checks current scope first
- then outer scope, repeatedly
- until found or reaches global scope

**🇬🇧 English**

The scope chain is the way JavaScript looks for a variable. First, JavaScript checks the current scope. If it can't find the variable there, it looks in the outer scope, and keeps searching outward until it either finds the variable or reaches the global scope.

**🇧🇩 বাংলা**

Scope chain হলো JavaScript-এর variable খোঁজার প্রক্রিয়া। প্রথমে JavaScript current scope-এ variable খোঁজে। সেখানে না পেলে outer scope-এ খোঁজে, এবং এভাবে বাইরের দিকে খুঁজতেই থাকে যতক্ষণ না variable পাওয়া যায় অথবা global scope-এ পৌঁছায়।

---

## Q9. Explain the concept of the Temporal Dead Zone (TDZ).

🔑 **Keywords:**
- time before let/const is declared
- using before declaration → ReferenceError
- hoisted but unusable until declaration line

**🇬🇧 English**

The Temporal Dead Zone, or TDZ, is the time before a `let` or `const` variable is actually declared. If I try to use that variable before its declaration, JavaScript throws a `ReferenceError`. This happens because `let` and `const` are hoisted, but they can't be used until the code actually reaches their declaration line. That's why I always declare `let` and `const` variables before using them.

**🇧🇩 বাংলা**

Temporal Dead Zone, বা TDZ, হলো একটা `let` বা `const` variable আসলে declare হওয়ার আগের সময়। এই সময়ে সেই variable ব্যবহার করার চেষ্টা করলে JavaScript `ReferenceError` দেয়। এটা হয় কারণ `let` এবং `const` hoist হয়, কিন্তু কোড আসলে সেই declaration লাইনে না পৌঁছানো পর্যন্ত সেগুলো ব্যবহার করা যায় না। এই কারণে আমি সবসময় `let` এবং `const` variable ব্যবহারের আগে declare করি।

---

## Q10. What is a Pure Function?

🔑 **Keywords:**
- same input → same output, always
- doesn't change outside variables/data
- easy to test and reuse

**🇬🇧 English**

A pure function is a function that always returns the same output for the same input. It also doesn't change any variables or data outside itself. I like pure functions because they're easy to understand, test, and reuse.

**🇧🇩 বাংলা**

Pure function হলো এমন একটি function, যা একই input দিলে সবসময় একই output দেয়। এছাড়া এটি নিজের বাইরের কোনো variable বা data পরিবর্তন করে না। আমি pure function পছন্দ করি কারণ এগুলো বুঝতে, test করতে এবং পুনরায় ব্যবহার করতে সহজ।

---

## Q11. What is the difference between Function Declaration and Function Expression?

🔑 **Keywords:**
- both create functions
- declaration = starts with `function`, fully hoisted, callable before declared
- expression = stored in variable, not fully hoisted
- prefer arrow function expressions in React

**🇬🇧 English**

Both function declarations and function expressions I use to create functions, but they behave differently. A function declaration starts with the `function` keyword and is hoisted, so I can call it even before it's declared. A function expression stores a function inside a variable — it's not fully hoisted, so I can't call it before its declaration. In my projects, I mostly use function expressions with arrow functions, since they're cleaner and commonly used in React.

**🇧🇩 বাংলা**

Function declaration এবং function expression — দুটোই আমি function তৈরি করার জন্য ব্যবহার করি, কিন্তু এদের আচরণ আলাদা। Function declaration `function` keyword দিয়ে শুরু হয় এবং hoisted হয়, তাই আমি এটাকে declare করার আগেও call করতে পারি। Function expression একটা function-কে একটা variable-এর ভিতরে রাখে — এটি পুরোপুরি hoisted হয় না, তাই declare করার আগে call করা যায় না। আমার প্রজেক্টে আমি বেশিরভাগ সময় arrow function দিয়ে function expression ব্যবহার করি, কারণ এটি cleaner এবং React-এ বেশি ব্যবহৃত হয়।

---

## Q12. What are Default Parameters in JavaScript?

🔑 **Keywords:**
- set a default value for a parameter
- used when no argument is passed
- avoids undefined, cleaner code

**🇬🇧 English**

Default parameters let me set a default value for a function parameter. If I don't pass a value when calling the function, JavaScript automatically uses that default value instead. This helps me avoid `undefined` values and keeps my code cleaner.

**🇧🇩 বাংলা**

Default parameters আমাকে একটি function-এর parameter-এর জন্য একটা default value সেট করতে দেয়। function call করার সময় যদি আমি কোনো value না দিই, তাহলে JavaScript সেই default value নিজে থেকেই ব্যবহার করে। এটি আমাকে `undefined` value এড়াতে সাহায্য করে এবং কোডকে আরও পরিষ্কার রাখে।

---

## Q13. What is the `typeof` operator and what are its possible return values?

🔑 **Keywords:**
- checks the data type of a value/variable
- returns type as a string
- values: string, number, boolean, undefined, object, function, symbol, bigint
- quirk: `typeof null` returns "object"

**🇬🇧 English**

The typeof operator is what I use to check the data type of a value or variable. It returns the data type as a string — the most common ones being `"string"`, `"number"`, `"boolean"`, `"undefined"`, `"object"`, `"function"`, `"symbol"`, and `"bigint"`. One thing worth knowing for interviews is that `typeof null` actually returns `"object"` — that's a well-known quirk in JavaScript, not a bug I introduced.

**🇧🇩 বাংলা**

typeof operator আমি কোনো value বা variable-এর data type জানার জন্য ব্যবহার করি। এটি data type-কে string আকারে return করে — সবচেয়ে common গুলো হলো `"string"`, `"number"`, `"boolean"`, `"undefined"`, `"object"`, `"function"`, `"symbol"`, এবং `"bigint"`। Interview-এর জন্য একটা গুরুত্বপূর্ণ বিষয় হলো, `typeof null` আসলে `"object"` return করে — এটা JavaScript-এর একটা well-known quirk, কোনো bug না।

---

## Q14. Explain Type Coercion in JavaScript.

🔑 **Keywords:**
- JS auto-converts one data type to another
- happens with +, -, == operators
- string + number → string; string - number → number
- prefer === to avoid unexpected results

**🇬🇧 English**

Type coercion means JavaScript automatically converts one data type into another when needed. This usually happens when I use operators like `+`, `-`, or `==`. For example, if I add a string and a number, JavaScript converts the number into a string. If I subtract a string and a number, JavaScript converts the string into a number instead. To avoid unexpected results, I prefer using `===` over `==`.

**🇧🇩 বাংলা**

Type coercion মানে হলো JavaScript প্রয়োজন হলে নিজে থেকেই একটা data type-কে অন্য data type-এ পরিবর্তন করে। এটা সাধারণত `+`, `-`, বা `==` operator ব্যবহার করার সময় ঘটে। যেমন, যদি আমি একটা string এবং number যোগ করি, JavaScript number-কে string-এ পরিবর্তন করে। আর যদি বিয়োগ করি, তাহলে JavaScript string-কে number-এ পরিবর্তন করে। অপ্রত্যাশিত result এড়াতে আমি `==`-এর বদলে `===` ব্যবহার করতে পছন্দ করি।

---

## Q15. What is an Immediately Invoked Function Expression (IIFE)?

🔑 **Keywords:**
- function runs immediately after creation
- no separate call needed
- avoids unnecessary global variables
- runs code once

**🇬🇧 English**

An Immediately Invoked Function Expression, or IIFE, is a function that runs immediately after it's created. I don't need to call it separately since it executes automatically. I find IIFEs useful when I want to run some code just once and avoid creating unnecessary variables in the global scope.

**🇧🇩 বাংলা**

Immediately Invoked Function Expression, বা IIFE, হলো এমন একটি function, যা তৈরি হওয়ার সাথে সাথেই run হয়ে যায়। আমাকে এটাকে আলাদাভাবে call করতে হয় না, কারণ এটি নিজে থেকেই execute হয়। আমি IIFE তখন useful মনে করি যখন আমি কোনো কোড শুধু একবার run করতে চাই এবং global scope-এ অপ্রয়োজনীয় variable তৈরি করা এড়াতে চাই।

---
