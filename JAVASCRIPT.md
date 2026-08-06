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