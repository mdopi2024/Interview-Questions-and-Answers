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