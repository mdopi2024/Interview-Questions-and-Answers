# React Interview Questions & Answers

A simple collection of React interview questions and answers for junior frontend developer interviews.

---

## Q1. What is React and what problem does it solve?

### 🇬🇧 Interview Answer

> React is a JavaScript library used to build user interfaces for web applications. It helps us create reusable components and update the UI when data changes. This makes it easier to build and manage interactive websites.

### 🇧🇩 বাংলা অর্থ

> React হলো JavaScript-এর একটি library, যা web application-এর user interface তৈরি করতে ব্যবহার করা হয়। এটি আমাদের reusable component তৈরি করতে এবং data change হলে UI update করতে সাহায্য করে। এর ফলে interactive website তৈরি ও manage করা সহজ হয়।

---

## Q2. What is JSX and why is it used in React?

### 🇬🇧 Interview Answer

> JSX is a syntax used in React that allows us to write HTML-like code inside JavaScript. It makes the UI code easier to read and write. React uses JSX to describe how the user interface should look.

### 🇧🇩 বাংলা অর্থ

> JSX হলো React-এ ব্যবহৃত একটি syntax, যার মাধ্যমে আমরা JavaScript-এর মধ্যে HTML-এর মতো code লিখতে পারি। এটি UI-এর code সহজে পড়তে এবং লিখতে সাহায্য করে। React JSX ব্যবহার করে user interface দেখতে কেমন হবে তা বুঝতে পারে।

---

## Q3. What is the difference between functional and class components?

### 🇬🇧 Interview Answer

> Functional components are simple JavaScript functions that return UI. Class components are JavaScript classes that also return UI. Functional components are more common in modern React because we can use Hooks to manage state and other React features.

### 🇧🇩 বাংলা অর্থ

> Functional component হলো একটি simple JavaScript function, যা UI return করে। আর Class component হলো একটি JavaScript class, যা UI return করে। Modern React-এ Functional component বেশি ব্যবহার করা হয়, কারণ এতে Hooks ব্যবহার করে state এবং অন্যান্য React features manage করা যায়।

---

## Q4. What is the Virtual DOM and how does React use it?

### 🇬🇧 Interview Answer

> The Virtual DOM is a lightweight copy of the real DOM. When something changes in a React application, React first updates the Virtual DOM and compares it with the previous version. Then, it updates only the necessary parts of the real DOM. This helps make UI updates more efficient.

### 🇧🇩 বাংলা অর্থ

> Virtual DOM হলো Real DOM-এর একটি lightweight copy। React application-এ কোনো কিছু change হলে, React প্রথমে Virtual DOM update করে এবং আগের version-এর সাথে compare করে। তারপর Real DOM-এর শুধু প্রয়োজনীয় অংশ update করে। এতে UI update করা আরও efficient হয়।

---

## Q5. Explain the useState Hook with an example.

### 🇬🇧 Interview Answer

> useState is a React Hook used to store and update data inside a functional component. It gives us a state value and a function to update that value. For example, we can use it to create a counter.

### 🇧🇩 বাংলা অর্থ

> useState হলো React-এর একটি Hook, যা functional component-এর ভিতরে data store এবং update করতে ব্যবহার করা হয়। এটি আমাদের একটি state value এবং সেই value update করার জন্য একটি function দেয়। যেমন, আমরা এটি দিয়ে একটি counter তৈরি করতে পারি।

---

## Q6. What is the useEffect Hook and what are its use cases?

### 🇬🇧 Interview Answer

> useEffect is a React Hook used to perform tasks after a component renders. It is commonly used for things like fetching data from an API, adding event listeners, or updating the document title.

### 🇧🇩 বাংলা অর্থ

> useEffect হলো React-এর একটি Hook, যা component render হওয়ার পরে কিছু কাজ করার জন্য ব্যবহার করা হয়। এটি সাধারণত API থেকে data আনা, event listener যোগ করা, অথবা document title update করার মতো কাজে ব্যবহার করা হয়।

---

## Q7. What is the difference between controlled and uncontrolled components?

### 🇬🇧 Interview Answer

> A controlled component is a form element whose value is managed by React state. An uncontrolled component manages its value by the DOM itself, usually using a ref. Controlled components are commonly used when we need to track and control form data.

### 🇧🇩 বাংলা অর্থ

> Controlled component হলো এমন একটি form element, যার value React state দিয়ে manage করা হয়। আর uncontrolled component-এর value DOM নিজে manage করে, সাধারণত ref ব্যবহার করে। যখন form-এর data track এবং control করতে হয়, তখন controlled component বেশি ব্যবহার করা হয়।

---

## Q8. What are props in React and how are they passed?

### 🇬🇧 Interview Answer

> Props are used to pass data from a parent component to a child component. They are passed as attributes and received inside the child component. Props are read-only, so the child component should not change them.

### 🇧🇩 বাংলা অর্থ

> Props ব্যবহার করা হয় parent component থেকে child component-এ data পাঠানোর জন্য। এগুলো attribute হিসেবে pass করা হয় এবং child component-এ receive করা হয়। Props read-only, তাই child component থেকে এগুলো change করা উচিত নয়।

---
<!-- 
## Q9. What is prop drilling and how can it be avoided?

### 🇬🇧 Interview Answer

> Prop drilling happens when we pass data through multiple components just to reach a component that needs it. It can make the code harder to manage. We can avoid it by using Context API, state management libraries, or by keeping the state closer to where it is needed.

### 🇧🇩 বাংলা অর্থ

> Prop drilling হলো যখন কোনো data প্রয়োজনীয় component-এ পৌঁছানোর জন্য মাঝখানের অনেকগুলো component-এর মাধ্যমে props pass করতে হয়। এতে code manage করা কঠিন হতে পারে। এটি এড়ানোর জন্য Context API, state management library ব্যবহার করা যায়, অথবা state-কে যেখানে প্রয়োজন তার কাছাকাছি রাখা যায়।

---

## Q10. Explain the useContext Hook with an example.

### 🇬🇧 Interview Answer

> useContext is a React Hook used to share data between components without passing props through every level. It is useful for sharing common data like user information, theme, or language.

### 🇧🇩 বাংলা অর্থ

> useContext হলো React-এর একটি Hook, যা props প্রতিটি component-এর মাধ্যমে pass না করে এক component থেকে অন্য component-এ data share করতে ব্যবহার করা হয়। এটি user information, theme বা language-এর মতো common data share করার জন্য useful।

---

## Q11. What is the useRef Hook and when would you use it?

### 🇬🇧 Interview Answer

> useRef is a React Hook used to store a value that does not cause a component to re-render when it changes. It is also commonly used to access a DOM element directly. For example, we can use it to focus an input field.

### 🇧🇩 বাংলা অর্থ

> useRef হলো React-এর একটি Hook, যা এমন কোনো value store করতে ব্যবহার করা হয় যার পরিবর্তনে component আবার render হয় না। এটি সরাসরি DOM element access করার জন্যও ব্যবহার করা হয়। যেমন, আমরা এটি ব্যবহার করে একটি input field-এ focus করতে পারি।

---

## Q12. What are React keys and why are they important in lists?

### 🇬🇧 Interview Answer

> Keys are unique values given to elements when we render a list in React. They help React identify which items have changed, been added, or removed. This helps React update the list correctly and efficiently.

### 🇧🇩 বাংলা অর্থ

> React-এ list render করার সময় প্রতিটি element-কে একটি unique value দেওয়াকে key বলা হয়। এটি React-কে বুঝতে সাহায্য করে কোন item change, add বা remove হয়েছে। এর ফলে React list-কে সঠিকভাবে এবং efficiently update করতে পারে।

---

## Q13. What is the difference between state and props?

### 🇬🇧 Interview Answer

> Props are used to pass data from a parent component to a child component, while state is used to store and manage data inside a component. Props are read-only, but state can be updated using a state update function like setState.

### 🇧🇩 বাংলা অর্থ

> Props ব্যবহার করা হয় parent component থেকে child component-এ data পাঠানোর জন্য। আর state ব্যবহার করা হয় component-এর ভিতরের data store এবং manage করার জন্য। Props read-only, কিন্তু state setState-এর মতো update function ব্যবহার করে পরিবর্তন করা যায়।

সহজভাবে মনে রাখুন:
- **Props** → Parent থেকে Child-এ data আসে
- **State** → Component-এর নিজের data manage করে

---

## Q14. How does conditional rendering work in React?

### 🇬🇧 Interview Answer

> Conditional rendering means showing different UI based on a condition. In React, we can use if-else, the ternary operator, or the && operator to render elements conditionally.

### 🇧🇩 বাংলা অর্থ

> Conditional rendering মানে হলো কোনো condition-এর উপর ভিত্তি করে different UI দেখানো। React-এ আমরা if-else, ternary operator অথবা && operator ব্যবহার করে condition অনুযায়ী UI render করতে পারি।

---

## Q15. What is React.memo and when should you use it?

### 🇬🇧 Interview Answer

> React.memo is used to prevent a component from re-rendering when its props have not changed. It can improve performance by avoiding unnecessary re-renders. We should use it when a component renders often but its props usually stay the same.

### 🇧🇩 বাংলা অর্থ

> React.memo ব্যবহার করা হয় যাতে কোনো component-এর props change না হলে সেটি আবার render না হয়। এটি unnecessary re-render কমিয়ে performance improve করতে পারে। যখন কোনো component বারবার render হয় কিন্তু তার props সাধারণত একই থাকে, তখন React.memo ব্যবহার করা যায়।

সহজভাবে মনে রাখুন:
- **React.memo** → Props change না হলে unnecessary re-render এড়াতে সাহায্য করে।

--- -->