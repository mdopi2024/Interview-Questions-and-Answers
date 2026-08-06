# 📘 JavaScript Interview Questions & Answers (Easy Version)
## Part 1 (Q1–Q5)

---

# Q1. What is the difference between `var`, `let`, and `const`?
### বাংলা: `var`, `let`, এবং `const`-এর মধ্যে পার্থক্য কী?

## 🇬🇧 English Answer

`var`, `let`, and `const` are all used to create variables in JavaScript.

- **`var`** is the old way. It can be **redeclared** and **updated**, so it may cause bugs.
- **`let`** can be **updated**, but it cannot be **redeclared** in the same block.
- **`const`** cannot be **updated** or **redeclared**, so it is used for values that should not change.

### Example

```javascript
var name = "Opi";
var name = "Korim"; // ✅ Allowed

let age = 18;
age = 19; // ✅ Allowed

const country = "Bangladesh";
country = "India"; // ❌ Error
```

**In my projects, I use `const` by default and `let` when the value needs to change.**

---

## 🇧🇩 বাংলা উত্তর

`var`, `let`, এবং `const`—তিনটিই JavaScript-এ variable তৈরি করার জন্য ব্যবহার করা হয়।

- **`var`** হলো পুরোনো পদ্ধতি। এটি আবার লেখা (redeclare) এবং মান পরিবর্তন (update) করা যায়।
- **`let`**-এর মান পরিবর্তন করা যায়, কিন্তু একই block-এ আবার লেখা যায় না।
- **`const`**-এর মান পরিবর্তন বা আবার লেখা যায় না। তাই যেসব value পরিবর্তন হবে না, সেখানে `const` ব্যবহার করা হয়।

**আমি সাধারণত `const` ব্যবহার করি, আর value পরিবর্তন করতে হলে `let` ব্যবহার করি।**

---

# Q2. Explain the concept of Hoisting in JavaScript.
### বাংলা: Hoisting কী?

## 🇬🇧 English Answer

Hoisting means JavaScript knows about **variables and functions before running the code**.

With **`var`**, using a variable before declaring it returns **`undefined`**.

With **`let`** and **`const`**, using them before declaring them gives a **ReferenceError**.

### Example

```javascript
console.log(name); // undefined
var name = "Opi";

console.log(age); // ReferenceError
let age = 18;
```

**I always declare my variables before using them to avoid errors.**

---

## 🇧🇩 বাংলা উত্তর

Hoisting মানে JavaScript **কোড চালানোর আগে variable এবং function-এর declaration আগে দেখে নেয়।**

- **`var`** আগে ব্যবহার করলে `undefined` পাওয়া যায়।
- **`let`** এবং **`const`** আগে ব্যবহার করলে `ReferenceError` আসে।

**তাই আমি সব সময় variable আগে declare করি, তারপর ব্যবহার করি।**

---

# Q3. What are the primitive data types in JavaScript?
### বাংলা: JavaScript-এর Primitive Data Types কী কী?

## 🇬🇧 English Answer

Primitive data types are the basic data types in JavaScript.

There are **7 primitive data types**:

1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. Symbol
7. BigInt

**In my projects, I mostly use String, Number, Boolean, Undefined, and Null.**

---

## 🇧🇩 বাংলা উত্তর

Primitive Data Types হলো JavaScript-এর **মৌলিক বা বেসিক data type**।

JavaScript-এ **৭টি Primitive Data Type** আছে।

1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. Symbol
7. BigInt

**আমার প্রজেক্টে আমি সবচেয়ে বেশি String, Number, Boolean, Undefined এবং Null ব্যবহার করি।**

---

# Q4. What is the difference between `==` and `===`?
### বাংলা: `==` এবং `===`-এর মধ্যে পার্থক্য কী?

## 🇬🇧 English Answer

Both **`==`** and **`===`** are used to compare two values.

- **`==`** compares only the values. If the data types are different, JavaScript changes the data type before comparing.
- **`===`** compares both the value and the data type. It does not change the data type.

### Example

```javascript
5 == "5"   // true
5 === "5"  // false
```

I always use **`===`** because it gives more accurate results.

---

## 🇧🇩 বাংলা উত্তর

`==` এবং `===`—দুটিই value তুলনা করার জন্য ব্যবহার করা হয়।

- **`==`** শুধু value তুলনা করে। Data type আলাদা হলে JavaScript আগে data type পরিবর্তন করে।
- **`===`** value এবং data type—দুটিই তুলনা করে। এটি data type পরিবর্তন করে না।

### উদাহরণ

```javascript
5 == "5"   // true
5 === "5"  // false
```

**আমি সব সময় `===` ব্যবহার করি, কারণ এটি বেশি সঠিক ফলাফল দেয়।**

---

# Q5. Explain how closures work in JavaScript with an example.
### বাংলা: Closure কী? উদাহরণসহ ব্যাখ্যা করুন।

## 🇬🇧 English Answer

A **closure** is when an **inner function** can use the variables of its **outer function**, even after the outer function has finished.

### Example

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

Here, the `inner()` function remembers the `name` variable even after `outer()` has finished. This is called a **closure**.

**Closures are useful for remembering values and keeping data private.**

---

## 🇧🇩 বাংলা উত্তর

**Closure** হলো এমন একটি feature, যেখানে **inner function**, **outer function** শেষ হওয়ার পরও তার variable ব্যবহার করতে পারে।

### উদাহরণ

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

এখানে `inner()` function, `outer()` শেষ হওয়ার পরও `name` variable ব্যবহার করতে পারছে। এটাকেই **Closure** বলা হয়।

**Closure সাধারণত value মনে রাখা এবং private data তৈরি করার জন্য ব্যবহার করা হয়।**

---

