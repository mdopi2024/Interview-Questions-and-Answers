# 📘 JavaScript Interview Questions & Answers (Easy Version)

---

# 1. What is the difference between `var`, `let`, and `const`?
### `var`, `let`, এবং `const`-এর মধ্যে পার্থক্য কী?

### 🇬🇧 English

`var`, `let`, and `const` are all used to create variables in JavaScript, but they work differently.

`var` is the old way to create variables. It can be redeclared and updated, which may cause unexpected bugs.

`let` is used when the value needs to change later. It can be updated, but it cannot be redeclared in the same block.

`const` is used when the value should not change. It cannot be redeclared or updated.

In my projects, I usually use `const` by default and `let` only when the value needs to change.

### 🇧🇩 বাংলা

`var`, `let`, এবং `const`—তিনটিই JavaScript-এ variable তৈরি করার জন্য ব্যবহার করা হয়, তবে এদের কাজের মধ্যে পার্থক্য রয়েছে।

`var` হলো পুরোনো পদ্ধতি। এটি একই নামে আবার লেখা যায় এবং মান পরিবর্তন করা যায়, তাই অনেক সময় অপ্রত্যাশিত bug হতে পারে।

`let` ব্যবহার করা হয় যখন পরে variable-এর মান পরিবর্তন করার প্রয়োজন হয়। এটি update করা যায়, কিন্তু একই block-এ আবার declare করা যায় না।

`const` ব্যবহার করা হয় যখন variable-এর মান পরিবর্তন করার দরকার নেই। এটি update বা redeclare—কোনোটাই করা যায় না।

আমি সাধারণত `const` ব্যবহার করি, আর যদি মান পরিবর্তন করতে হয় তাহলে `let` ব্যবহার করি।

### 💻 Example

```javascript
var name = "Opi";
var name = "Korim"; // ✅ Allowed

let age = 18;
age = 19; // ✅ Allowed

const country = "Bangladesh";
country = "India"; // ❌ Error
```

---

# 2. Explain the concept of Hoisting in JavaScript.
### JavaScript-এ Hoisting কী?

### 🇬🇧 English

Hoisting means JavaScript knows about variables and functions before running the code.

With `var`, if we use a variable before declaring it, JavaScript returns `undefined`.

With `let` and `const`, if we use them before declaring them, JavaScript gives a `ReferenceError`.

That is why I always declare my variables before using them.

### 🇧🇩 বাংলা

Hoisting মানে JavaScript কোড চালানোর আগে variable এবং function-এর declaration আগে দেখে নেয়।

`var`-এর ক্ষেত্রে declare করার আগে ব্যবহার করলে `undefined` পাওয়া যায়।

কিন্তু `let` এবং `const` declare করার আগে ব্যবহার করলে `ReferenceError` আসে।

তাই আমি সব সময় variable আগে declare করি, তারপর ব্যবহার করি।

### 💻 Example

```javascript
console.log(name); // undefined
var name = "Opi";

console.log(age); // ReferenceError
let age = 18;
```

---
# 3. What are the primitive data types in JavaScript?
### JavaScript-এর Primitive Data Types কী কী?

### 🇬🇧 English

Primitive data types are the basic data types in JavaScript.

There are **7 primitive data types**:

- String
- Number
- Boolean
- Undefined
- Null
- Symbol
- BigInt

In my projects, I mostly use String, Number, Boolean, Undefined, and Null.

### 🇧🇩 বাংলা

Primitive Data Types হলো JavaScript-এর মৌলিক বা বেসিক data type।

JavaScript-এ **৭টি Primitive Data Type** রয়েছে।

- String
- Number
- Boolean
- Undefined
- Null
- Symbol
- BigInt

আমার প্রজেক্টে আমি সবচেয়ে বেশি String, Number, Boolean, Undefined এবং Null ব্যবহার করি।

---

# 4. What is the difference between `==` and `===`?
### `==` এবং `===`-এর মধ্যে পার্থক্য কী?

### 🇬🇧 English

Both `==` and `===` are used to compare two values.

`==` compares only the values. If the data types are different, JavaScript automatically converts the data type before comparing.

`===` compares both the value and the data type. It does not convert the data type.

That is why I always use `===` because it gives more accurate results.

### 🇧🇩 বাংলা

`==` এবং `===`—দুটিই দুটি value তুলনা করার জন্য ব্যবহার করা হয়।

`==` শুধু value তুলনা করে। যদি data type আলাদা হয়, তাহলে JavaScript আগে data type পরিবর্তন করে।

অন্যদিকে `===` value এবং data type—দুটিই তুলনা করে। এটি data type পরিবর্তন করে না।

তাই আমি সব সময় `===` ব্যবহার করি, কারণ এটি বেশি সঠিক ফলাফল দেয়।

### 💻 Example

```javascript
5 == "5";   // true
5 === "5";  // false
```

---

# 5. Explain how closures work in JavaScript with an example.
### JavaScript-এ Closure কী? উদাহরণসহ ব্যাখ্যা করুন।

### 🇬🇧 English

A closure is when an inner function can access the variables of its outer function, even after the outer function has finished.

It remembers the variables of the outer function and can use them later.

Closures are useful for remembering values and keeping data private.

### 🇧🇩 বাংলা

Closure হলো এমন একটি feature, যেখানে একটি inner function, outer function শেষ হওয়ার পরও তার variable ব্যবহার করতে পারে।

অর্থাৎ, inner function outer function-এর variable মনে রাখে এবং পরে ব্যবহার করতে পারে।

Closure সাধারণত value মনে রাখা এবং private data তৈরি করার জন্য ব্যবহার হয়।

### 💻 Example

```javascript
function outer() {
  let name = "Opi";

  function inner() {
    console.log(name);
  }

  return inner;
}

const showName = outer();
showName(); // Opi
```
---
# 6. What is the difference between `null` and `undefined`?
### `null` এবং `undefined`-এর মধ্যে পার্থক্য কী?

### 🇬🇧 English

Both `null` and `undefined` mean there is no value, but they are different.

- `undefined` means a variable has been declared, but no value has been assigned yet.
- `null` means we intentionally set the value to empty.

In simple words:

- **`undefined` = No value yet.**
- **`null` = Empty value on purpose.**

### 🇧🇩 বাংলা

`null` এবং `undefined`—দুটিরই অর্থ হলো কোনো value নেই, কিন্তু এদের মধ্যে পার্থক্য আছে।

- `undefined` মানে variable তৈরি করা হয়েছে, কিন্তু এখনো কোনো value দেওয়া হয়নি।
- `null` মানে আমরা ইচ্ছা করে variable-এর value খালি রেখেছি।

সহজভাবে,

- **`undefined` = এখনো কোনো value নেই।**
- **`null` = ইচ্ছা করে খালি value রাখা হয়েছে।**

### 💻 Example

```javascript
let name;
console.log(name); // undefined

let age = null;
console.log(age); // null
```

---

# 7. What are Arrow Functions and how do they differ from Regular Functions?
### Arrow Function কী এবং এটি Regular Function থেকে কীভাবে আলাদা?

### 🇬🇧 English

Arrow functions are a shorter way to write functions in JavaScript.

The main difference is the syntax.

A regular function is written like this:

```javascript
function greet() {
  console.log("Hello");
}
```

An arrow function is written like this:

```javascript
const greet = () => {
  console.log("Hello");
};
```

Both functions do the same job, but arrow functions use less code.

In my React projects, I mostly use arrow functions because they are shorter and easier to read.

### 🇧🇩 বাংলা

Arrow Function হলো JavaScript-এ function লেখার একটি ছোট এবং সহজ উপায়।

মূল পার্থক্য হলো লেখার পদ্ধতিতে (syntax)।

Regular Function:

```javascript
function greet() {
  console.log("Hello");
}
```

Arrow Function:

```javascript
const greet = () => {
  console.log("Hello");
};
```

দুটিই একই কাজ করে, কিন্তু Arrow Function-এ কম কোড লিখতে হয়।

আমি আমার React প্রজেক্টে বেশিরভাগ সময় Arrow Function ব্যবহার করি, কারণ এটি ছোট এবং পড়তে সহজ।

---

# 8. What is the Scope Chain in JavaScript?
### JavaScript-এ Scope Chain কী?

### 🇬🇧 English

The scope chain is the way JavaScript looks for a variable.

First, JavaScript checks the current scope.

If it cannot find the variable, it looks in the outer scope.

It keeps searching until it finds the variable or reaches the global scope.

### 🇧🇩 বাংলা

Scope Chain হলো JavaScript-এর variable খোঁজার প্রক্রিয়া।

প্রথমে JavaScript current scope-এ variable খোঁজে।

যদি সেখানে না পায়, তাহলে outer scope-এ খোঁজে।

এভাবে variable পাওয়া পর্যন্ত বা global scope-এ পৌঁছানো পর্যন্ত খুঁজতে থাকে।

### 💻 Example

```javascript
let name = "Opi";

function outer() {
  let age = 18;

  function inner() {
    console.log(name);
    console.log(age);
  }

  inner();
}

outer();
```

Here, `inner()` cannot find `name` or `age` inside its own scope, so JavaScript looks in the outer scope. This process is called the **Scope Chain**.

এখানে `inner()` function নিজের scope-এ `name` বা `age` পায় না। তাই JavaScript বাইরের scope-এ খুঁজে পায়। এই প্রক্রিয়াকেই **Scope Chain** বলা হয়।
---
# 9. Explain the concept of the Temporal Dead Zone (TDZ).
### Temporal Dead Zone (TDZ) কী?

### 🇬🇧 English

The **Temporal Dead Zone (TDZ)** is the time before a `let` or `const` variable is declared.

If we try to use the variable before its declaration, JavaScript throws a **ReferenceError**.

This happens because `let` and `const` are hoisted, but they cannot be used until the declaration line is reached.

That is why I always declare `let` and `const` variables before using them.

### 🇧🇩 বাংলা

**Temporal Dead Zone (TDZ)** হলো `let` বা `const` variable declare করার আগের সময়।

এই সময়ে যদি আমরা variable ব্যবহার করি, তাহলে JavaScript **ReferenceError** দেয়।

এটি হয় কারণ `let` এবং `const` hoist হয়, কিন্তু declaration লাইনে পৌঁছানোর আগে ব্যবহার করা যায় না।

তাই আমি সব সময় `let` এবং `const` variable আগে declare করি, তারপর ব্যবহার করি।

### 💻 Example

```javascript
console.log(name); // ReferenceError

let name = "Opi";
```

---

# 10. What is a Pure Function? Give an example.
### Pure Function কী? একটি উদাহরণ দিন।

### 🇬🇧 English

A **pure function** is a function that always returns the same output for the same input.

It also does not change any outside variables or data.

Pure functions are easy to understand, test, and reuse.

### 🇧🇩 বাংলা

**Pure Function** হলো এমন একটি function, যা একই input দিলে সব সময় একই output দেয়।

এছাড়া, এটি বাইরের কোনো variable বা data পরিবর্তন করে না।

Pure Function বুঝতে সহজ, test করা সহজ এবং আবার ব্যবহার করা সহজ।

### 💻 Example

```javascript
function add(a, b) {
  return a + b;
}

console.log(add(2, 3)); // 5
console.log(add(2, 3)); // 5
```

Here, every time we pass `2` and `3`, the function returns `5`. So, it is a **Pure Function**.

এখানে প্রতিবার `2` এবং `3` দিলে function `5` return করে। তাই এটি একটি **Pure Function**।

---

# 11. What is the difference between Function Declaration and Function Expression?
### Function Declaration এবং Function Expression-এর মধ্যে পার্থক্য কী?

### 🇬🇧 English

Both Function Declaration and Function Expression are used to create functions.

A **Function Declaration** starts with the `function` keyword and is **hoisted**, so it can be called before it is declared.

A **Function Expression** stores a function inside a variable. It is **not fully hoisted**, so it cannot be called before its declaration.

In my projects, I mostly use **Function Expressions with Arrow Functions** because they are cleaner and commonly used in React.

### 🇧🇩 বাংলা

Function Declaration এবং Function Expression—দুটিই function তৈরি করার জন্য ব্যবহার করা হয়।

**Function Declaration** `function` keyword দিয়ে শুরু হয় এবং এটি **hoisted** হয়। তাই declare করার আগেও call করা যায়।

**Function Expression**-এ function-কে একটি variable-এর মধ্যে রাখা হয়। এটি **পুরোপুরি hoisted হয় না**, তাই declare করার আগে call করলে Error আসে।

আমি আমার প্রজেক্টে বেশিরভাগ সময় **Arrow Function (Function Expression)** ব্যবহার করি, কারণ এটি ছোট, পরিষ্কার এবং React-এ বেশি ব্যবহার হয়।

### 💻 Example

**Function Declaration**

```javascript
sayHello();

function sayHello() {
  console.log("Hello");
}
```

**Function Expression**

```javascript
const sayHello = function () {
  console.log("Hello");
};

sayHello();
```
---
# 12. What are Default Parameters in JavaScript?
### JavaScript-এ Default Parameters কী?

### 🇬🇧 English

Default parameters allow us to set a **default value** for a function parameter.

If we do not pass a value when calling the function, JavaScript automatically uses the default value.

Default parameters help us avoid `undefined` values and make the code cleaner.

### 🇧🇩 বাংলা

Default Parameters ব্যবহার করে আমরা function-এর parameter-এর জন্য একটি **default value** দিতে পারি।

যদি function call করার সময় কোনো value না দিই, তাহলে JavaScript সেই **default value** ব্যবহার করে।

এটি `undefined` এড়াতে সাহায্য করে এবং কোডকে আরও পরিষ্কার করে।

### 💻 Example

```javascript
function greet(name = "Guest") {
  return `Hello, ${name}`;
}

console.log(greet());      // Hello, Guest
console.log(greet("Opi")); // Hello, Opi
```

Here, if no value is passed, JavaScript uses `"Guest"` as the default value.

এখানে যদি কোনো value না দেওয়া হয়, তাহলে JavaScript `"Guest"`-কে default value হিসেবে ব্যবহার করে।

---

# 13. What is the `typeof` operator and what are its possible return values?
### `typeof` Operator কী এবং এটি কী কী return করতে পারে?

### 🇬🇧 English

The `typeof` operator is used to check the **data type** of a value or variable.

It returns the data type as a string.

The most common return values are:

- `"string"`
- `"number"`
- `"boolean"`
- `"undefined"`
- `"object"`
- `"function"`
- `"symbol"`
- `"bigint"`

I use `typeof` in my projects to check the data type before working with a value.

### 🇧🇩 বাংলা

`typeof` operator ব্যবহার করা হয় কোনো **value বা variable-এর data type** জানার জন্য।

এটি data type-কে **string** আকারে return করে।

সবচেয়ে বেশি ব্যবহৃত return values হলো:

- `"string"`
- `"number"`
- `"boolean"`
- `"undefined"`
- `"object"`
- `"function"`
- `"symbol"`
- `"bigint"`

আমি আমার প্রজেক্টে কোনো value-এর data type যাচাই করার জন্য `typeof` ব্যবহার করি।

### 💻 Example

```javascript
console.log(typeof "Hello");      // "string"
console.log(typeof 10);           // "number"
console.log(typeof true);         // "boolean"
console.log(typeof undefined);    // "undefined"
console.log(typeof null);         // "object"
console.log(typeof Symbol());     // "symbol"
console.log(typeof 10n);          // "bigint"
console.log(typeof {});           // "object"
console.log(typeof []);           // "object"
console.log(typeof function(){}); // "function"
```

> **💡 Interview Tip:**  
> `typeof null` returns **`"object"`**. This is a well-known JavaScript behavior and is a very common interview follow-up question.

---
# 14. Explain Type Coercion in JavaScript with examples.
### JavaScript-এ Type Coercion কী? উদাহরণসহ ব্যাখ্যা করুন।

### 🇬🇧 English

Type coercion means JavaScript **automatically changes one data type into another** when needed.

This usually happens when we use operators like `+`, `-`, or `==`.

For example, if we add a string and a number, JavaScript converts the number into a string.

If we subtract a string and a number, JavaScript converts the string into a number.

To avoid unexpected results, I prefer using `===` instead of `==`.

### 🇧🇩 বাংলা

Type Coercion মানে JavaScript **প্রয়োজন হলে নিজে থেকেই একটি data type-কে অন্য data type-এ পরিবর্তন করে।**

এটি সাধারণত `+`, `-` অথবা `==` operator ব্যবহার করার সময় ঘটে।

যদি string এবং number যোগ করা হয়, তাহলে JavaScript number-কে string-এ পরিবর্তন করে।

আর যদি বিয়োগ করা হয়, তাহলে JavaScript string-কে number-এ পরিবর্তন করে।

অপ্রত্যাশিত ফলাফল এড়াতে আমি সাধারণত `===` ব্যবহার করি।

### 💻 Example

```javascript
console.log("5" + 2); // "52"

console.log("5" - 2); // 3

console.log(5 == "5"); // true

console.log(5 === "5"); // false
```

---

# 15. What is an Immediately Invoked Function Expression (IIFE)?
### Immediately Invoked Function Expression (IIFE) কী?

### 🇬🇧 English

An **Immediately Invoked Function Expression (IIFE)** is a function that **runs immediately after it is created**.

We do not need to call it separately because it executes automatically.

IIFEs are useful when we want to run some code only once and avoid creating unnecessary global variables.

### 🇧🇩 বাংলা

**Immediately Invoked Function Expression (IIFE)** হলো এমন একটি function, যা **তৈরি হওয়ার সঙ্গে সঙ্গেই execute হয়।**

এটিকে আলাদা করে call করতে হয় না, কারণ এটি নিজে থেকেই execute হয়।

IIFE সাধারণত একবার কোনো কাজ করার জন্য এবং global scope-এ অপ্রয়োজনীয় variable তৈরি না করার জন্য ব্যবহার করা হয়।

### 💻 Example

```javascript
(function () {
  console.log("Hello, World!");
})();
```

---

# 🎯 JavaScript Interview Quick Revision

| No. | Question | Short Answer |
|------|----------|--------------|
| **1** | Difference between `var`, `let`, and `const` | `var` is old, `let` can change, `const` cannot change. |
| **2** | Hoisting | JavaScript knows about variables and functions before running the code. |
| **3** | Primitive Data Types | String, Number, Boolean, Undefined, Null, Symbol, BigInt. |
| **4** | `==` vs `===` | `==` compares value only, `===` compares value and data type. |
| **5** | Closure | An inner function can use the outer function's variables after the outer function finishes. |
| **6** | `null` vs `undefined` | `undefined` means no value yet, `null` means empty value on purpose. |
| **7** | Arrow Function | A shorter way to write functions. |
| **8** | Scope Chain | JavaScript looks for variables from the current scope to the outer scope. |
| **9** | Temporal Dead Zone | Using `let` or `const` before declaration causes a `ReferenceError`. |
| **10** | Pure Function | Same input always gives the same output and doesn't change outside data. |
| **11** | Function Declaration vs Expression | Declaration is hoisted, Expression is not fully hoisted. |
| **12** | Default Parameters | Provide a default value if no argument is passed. |
| **13** | `typeof` Operator | Used to check the data type of a value or variable. |
| **14** | Type Coercion | JavaScript automatically converts one data type into another. |
| **15** | IIFE | A function that runs immediately after it is created. |