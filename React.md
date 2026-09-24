# React Interview Questions & Answers (Q1–Q15)

A bilingual (English + বাংলা) collection of React interview questions with natural, speakable, interview-standard answers — great for junior frontend developer interview prep.

---

## 🔑 Keyword Quick-Recall Table

Use this table for fast revision. Cover the full answer below, look only at the keywords, and try to explain the topic out loud in your own words (active recall).

| Q# | Topic | Keywords to Recall |
|---|---|---|
| 1 | What is React | JS library → build UI → reusable components → update UI on data change |
| 2 | JSX | syntax → HTML-like code in JS → easier to read/write → describes UI |
| 3 | Functional vs Class Components | functions vs classes → both return UI → functional = modern, uses Hooks |
| 4 | Virtual DOM | lightweight copy of real DOM → compare with previous version → update only necessary parts |
| 5 | useState | store/update data → returns state + updater function → e.g. counter |
| 6 | useEffect | runs after render → side effects → API calls, event listeners, title update |
| 7 | Controlled vs Uncontrolled | controlled = value in React state → uncontrolled = value in DOM/ref |
| 8 | Props | parent → child data → passed as attributes → read-only |
| 9 | Prop Drilling | passing data through many components → hard to manage → fix: Context API / state management / lift state |
| 10 | useContext | share data without prop drilling → common data → user info, theme, language |
| 11 | useRef | store value without re-render → access DOM directly → e.g. focus input |
| 12 | Keys in Lists | unique identifier per item → helps React track changed/added/removed → efficient list updates |
| 13 | State vs Props | props = parent→child, read-only → state = internal, updatable |
| 14 | Conditional Rendering | show UI based on condition → if-else, ternary, && operator |
| 15 | React.memo | prevent re-render if props unchanged → performance → best for frequently rendering, stable-props components |

---

## Q1. What is React and what problem does it solve?

🔑 **Keywords:**
- JavaScript library
- build user interfaces
- reusable components
- update UI on data change

**🇬🇧 English**

React is a JavaScript library used to build user interfaces for web applications. It allows developers to create reusable components and efficiently update the UI when data changes. It solves the problem of managing complex and interactive user interfaces by making the UI easier to build, update, and maintain.

**🇧🇩 বাংলা**

React হলো একটি JavaScript library, যেটা web application-এর user interface তৈরি করার জন্য ব্যবহার করা হয়। এটি reusable component তৈরি করতে এবং data change হলে efficiently UI update করতে সাহায্য করে। এটি complex এবং interactive UI manage করার সমস্যার সমাধান করে, ফলে UI তৈরি, update এবং maintain করা সহজ হয়।

---

## Q2. What is JSX and why is it used in React?

🔑 **Keywords:**
- syntax extension
- HTML-like code in JavaScript
- easier to read/write UI
- describes what UI should look like

**🇬🇧 English**

JSX is a syntax used in React to write HTML-like code inside JavaScript. It makes UI code simpler and cleaner. JSX helps describe what the user interface should look like.

**🇧🇩 বাংলা**

JSX হলো একটি syntax, যেটা React-এ JavaScript-এর মধ্যে HTML-এর মতো code লেখার জন্য ব্যবহার করা হয়। এটি UI code-কে আরও সহজ এবং পরিষ্কার করে। JSX-এর মাধ্যমে React-কে বোঝানো যায় UI দেখতে কেমন হবে।

---

## Q3. What is the difference between functional and class components?

🔑 **Keywords:**
- both types return UI
- functional = simple function
- class = JS class
- functional is modern standard, uses Hooks

**🇬🇧 English**

Functional and Class Components are both used to build UI, but their structure is different. A Functional Component is a simple JavaScript function that returns UI. A Class Component is a JavaScript class that returns UI. Functional Components are mostly used now because Hooks allow us to manage state and other React features without using a class.

**🇧🇩 বাংলা**

Functional এবং Class Component — দুটোই UI তৈরি করার জন্য ব্যবহার করা হয়, কিন্তু এদের structure আলাদা। Functional Component হলো একটি simple JavaScript function, যা UI return করে। Class Component হলো একটি JavaScript class, যা UI return করে। এখন Functional Component বেশি ব্যবহার করা হয়, কারণ Hooks ব্যবহার করে class না লিখেই state এবং অন্যান্য React features manage করা যায়।

---

## Q4. What is the Virtual DOM and how does React use it?

🔑 **Keywords:**
- lightweight copy of real DOM
- compare with previous version
- update only necessary parts
- makes UI updates efficient

**🇬🇧 English**

The Virtual DOM is a lightweight copy of the Real DOM that React maintains. When something changes in the application, React first updates the Virtual DOM and compares it with the previous version. Then, it updates only the necessary parts of the Real DOM. This makes UI updates more efficient.

**🇧🇩 বাংলা**

Virtual DOM হলো Real DOM-এর একটি lightweight copy, যেটা React maintain করে। Application-এ কোনো কিছু change হলে, React প্রথমে Virtual DOM update করে এবং আগের Virtual DOM-এর সাথে compare করে। এরপর Real DOM-এর শুধু প্রয়োজনীয় অংশ update করে। এতে UI update করা আরও efficient হয়।

---

## Q5. Explain the `useState` Hook with an example.

🔑 **Keywords:**
- store and update data
- inside functional component
- returns state + updater function
- e.g. counter

**🇬🇧 English**

useState is a React Hook used to store and update data inside a functional component. It gives us a state value and a function to update that value. For example, we can use useState to create a simple counter that increases when we click a button.

**🇧🇩 বাংলা**

useState হলো React-এর একটি Hook, যেটা functional component-এর ভিতরে data store এবং update করার জন্য ব্যবহার করা হয়। এটি একটি state value এবং সেই value update করার জন্য একটি function দেয়। যেমন, useState ব্যবহার করে একটি simple counter বানানো যায়, যেটা button click করলে বাড়ে।

---

## Q6. What is the `useEffect` Hook and what are its use cases?

🔑 **Keywords:**
- runs after component renders
- side effects
- API calls, event listeners, title update
- dependency array controls when it runs

**🇬🇧 English**

useEffect is a React Hook used to handle side effects in a component. For example, it can be used for fetching data from an API, adding event listeners, running timers, or updating the document title. The dependency array helps control when the side effect runs.

Without a dependency array → useEffect runs after every render.
With an empty array [] → useEffect runs once after the first render.
With a dependency [value] → useEffect runs after the first render and whenever the value changes.

**🇧🇩 বাংলা**

useEffect হলো React-এর একটি Hook, যেটা component-এর side effect handle করার জন্য ব্যবহার করা হয়। যেমন API থেকে data fetch করা, event listener যোগ করা, timer চালানো বা document title update করা। Dependency array ব্যবহার করে side effect কখন চলবে তা control করা যায়।

Dependency array না দিলে → component প্রতিবার render হওয়ার পরে useEffect চলে।
Empty array [] দিলে → component প্রথমবার render হওয়ার পরে একবার চলে।
Dependency দিলে [value] → component প্রথমবার render হওয়ার পরে এবং সেই value পরিবর্তন হলে useEffect চলে।

---

## Q7. What is the difference between controlled and uncontrolled components?

🔑 **Keywords:**
- controlled = value managed by React state
- uncontrolled = value managed by DOM/ref
- controlled used when tracking/validating form data

**🇬🇧 English**

Controlled and Uncontrolled Components are both used to handle forms, but they manage values differently. A Controlled Component has its value managed by React state. An Uncontrolled Component has its value managed by the DOM, and we usually access it using a ref. Controlled Components are commonly used when we need to track or validate form data.

**🇧🇩 বাংলা**

Controlled এবং Uncontrolled Component — দুটোই form handle করার জন্য ব্যবহার করা হয়, কিন্তু এদের value manage করার পদ্ধতি আলাদা। Controlled Component-এর value React state দিয়ে manage করে। আর Uncontrolled Component-এর value DOM নিজে manage করে, এবং সাধারণত ref দিয়ে সেই value access করা হয়। Form-এর data track বা validate করতে হলে Controlled Component বেশি ব্যবহার করা হয়।

---

## Q8. What are props in React and how are they passed?

🔑 **Keywords:**
- pass data parent → child
- passed as attributes
- received inside child component
- read-only

**🇬🇧 English**

Props are used to pass data from a parent component to a child component. Props are usually passed as attributes, and the child component receives them as an object. Props are read-only, so they cannot be changed directly inside the child component.

**🇧🇩 বাংলা**

Props হলো এমন একটি উপায়, যেটা parent component থেকে child component-এ data পাঠানোর জন্য ব্যবহার করা হয়। Props সাধারণত attribute হিসেবে pass করা হয়, এবং child component এগুলো object হিসেবে receive করে। Props read-only, তাই child component-এর ভিতরে এগুলো সরাসরি change করা যায় না।

---

## Q9. What is prop drilling and how can it be avoided?

🔑 **Keywords:**
- passing data through many intermediate components
- makes code harder to manage
- fix: Context API / state management library / lift state

**🇬🇧 English**

Prop drilling happens when data needs to be passed through several components using props just to reach a child component that needs it. This can make the code harder to manage. We can avoid it by using the Context API, a state management library, or by keeping the state closer to where it is needed.

**🇧🇩 বাংলা**

Prop drilling তখন হয়, যখন কোনো data একটি child component-এ পৌঁছানোর জন্য মাঝখানের অনেকগুলো component-এর মাধ্যমে props pass করতে হয়। এতে code manage করা কঠিন হতে পারে। এটি এড়ানোর জন্য Context API, state management library ব্যবহার করা যায়, অথবা state-কে যেখানে দরকার তার কাছাকাছি রাখা যায়।

---

## Q10. Explain the `useContext` Hook with an example.

🔑 **Keywords:**
- share data without prop drilling
- avoids passing through every level
- e.g. user info, theme, language

**🇬🇧 English**

useContext is a React Hook used to share data between multiple components without passing props through every level. It helps avoid or reduce prop drilling. It is useful for sharing common data like user information, theme settings, or language preferences across many components.

**🇧🇩 বাংলা**

useContext হলো React-এর একটি Hook, যেটা অনেকগুলো component-এর মধ্যে data share করার জন্য ব্যবহার করা হয়, যাতে প্রতিটি level-এর মধ্যে props pass করতে না হয়। এটি prop drilling এড়াতে বা কমাতে সাহায্য করে। এটি user information, theme settings, বা language preference-এর মতো common data অনেক component-এর মধ্যে share করার জন্য useful।

---

## Q11. What is the `useRef` Hook and when would you use it?

🔑 **Keywords:**
- store value without causing re-render
- access DOM element directly
- e.g. focus an input field

**🇬🇧 English**

useRef is a React Hook that I use to store a value that doesn't cause a re-render when it changes. I also commonly use it to access a DOM element directly. For example, I can use useRef to focus an input field automatically.

**🇧🇩 বাংলা**

useRef হলো React-এর একটি Hook, যেটা আমি এমন একটি value store করার জন্য ব্যবহার করি যেটা change হলে component আবার render হয় না। আমি এটি সরাসরি একটি DOM element access করার জন্যও ব্যবহার করি। যেমন, আমি useRef দিয়ে একটি input field automatically focus করতে পারি।

---

## Q12. What are React keys and why are they important in lists?

🔑 **Keywords:**
- unique value per list item
- helps React identify changed/added/removed items
- makes list updates correct and efficient

**🇬🇧 English**

Keys are unique values that I give to each element when I render a list in React. They help React identify which items have changed, been added, or been removed. This helps React update the list correctly and efficiently, instead of re-rendering everything.

**🇧🇩 বাংলা**

Keys হলো unique value, যেটা আমি React-এ list render করার সময় প্রতিটি element-কে দিই। এগুলো React-কে বুঝতে সাহায্য করে কোন item change হয়েছে, কোনটা add হয়েছে বা কোনটা remove হয়েছে। এতে React পুরো list আবার render না করে সঠিকভাবে এবং efficiently update করতে পারে।

---

## Q13. What is the difference between state and props?

🔑 **Keywords:**
- props = parent → child, read-only
- state = internal to component, updatable
- both hold data, different purpose

**🇬🇧 English**

Both state and props I use to handle data in React, but they serve different purposes. Props are used to pass data from a parent component to a child component, and they are read-only. State is used to store and manage data inside a component itself, and I can update it using a function like `setState` or a `useState` updater.

**🇧🇩 বাংলা**

State এবং props — দুটোই আমি React-এ data handle করার জন্য ব্যবহার করি, কিন্তু এদের purpose আলাদা। Props ব্যবহার করা হয় parent component থেকে child component-এ data পাঠানোর জন্য, এবং এগুলো read-only। State ব্যবহার করা হয় component-এর নিজের ভিতরের data store এবং manage করার জন্য, এবং আমি এটি `setState` বা `useState`-এর updater function দিয়ে পরিবর্তন করতে পারি।

**Quick recall:**
- **Props** → Parent থেকে Child-এ data আসে
- **State** → Component নিজের data manage করে

---

## Q14. How does conditional rendering work in React?

🔑 **Keywords:**
- show different UI based on condition
- if-else, ternary operator, `&&` operator

**🇬🇧 English**

Conditional rendering means I show different UI based on a condition. In React, I usually use if-else statements, the ternary operator, or the `&&` operator to render elements conditionally, depending on how simple or complex the condition is.

**🇧🇩 বাংলা**

Conditional rendering মানে হলো আমি কোনো condition-এর উপর ভিত্তি করে different UI দেখাই। React-এ আমি সাধারণত if-else statement, ternary operator, অথবা `&&` operator ব্যবহার করি condition অনুযায়ী element render করার জন্য, condition কতটা simple বা complex তার উপর নির্ভর করে।

---

## Q15. What is `React.memo` and when should you use it?

🔑 **Keywords:**
- prevents re-render if props unchanged
- improves performance
- best when props usually stay the same

**🇬🇧 English**

React.memo is what I use to prevent a component from re-rendering when its props haven't changed. It helps improve performance by avoiding unnecessary re-renders. I use it when a component renders often but its props usually stay the same.

**🇧🇩 বাংলা**

React.memo হলো এমন একটি জিনিস, যেটা আমি ব্যবহার করি যাতে কোনো component-এর props change না হলে সেটি আবার render না হয়। এটি unnecessary re-render এড়িয়ে performance improve করতে সাহায্য করে। আমি এটি তখন ব্যবহার করি যখন কোনো component বারবার render হয় কিন্তু তার props সাধারণত একই থাকে।

**Quick recall:**
- **React.memo** → props change না হলে unnecessary re-render এড়াতে সাহায্য করে

---

*Prepared for React technical interview practice — English + বাংলা, sentence-aligned for easy speaking practice.*
