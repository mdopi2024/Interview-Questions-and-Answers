# 📘 JavaScript Interview Questions & Answers (Easy Version)
## Part 1 (Q1–Q5)

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
