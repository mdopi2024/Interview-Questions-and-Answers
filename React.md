# React Interview Questions & Answers (Q1–Q60)

A bilingual (English + বাংলা) collection of React interview questions with natural, speakable, interview-standard answers — great for interview prep.

---

## Q1. What is React and what problem does it solve?

🔑 **Keywords:**
- JavaScript library
- build user interfaces
- reusable components
- update UI on data change

**🇬🇧 English**

React is a JavaScript library that I use to build user interfaces for web applications. It lets me create reusable components and automatically update the UI whenever the data changes. This makes it much easier to build and manage interactive websites.

**🇧🇩 বাংলা**

React হলো একটি JavaScript library, যেটা আমি web application-এর user interface তৈরি করার জন্য ব্যবহার করি। এটি আমাকে reusable component তৈরি করতে এবং data change হলে automatically UI update করতে সাহায্য করে। এর ফলে interactive website তৈরি করা এবং manage করা অনেক সহজ হয়ে যায়।

---

## Q2. What is JSX and why is it used in React?

🔑 **Keywords:**
- syntax extension
- HTML-like code in JavaScript
- easier to read/write UI
- describes what UI should look like

**🇬🇧 English**

JSX is a syntax that I use in React to write HTML-like code inside JavaScript. It makes my UI code much easier to read and write. React uses JSX under the hood to understand and describe how the user interface should look.

**🇧🇩 বাংলা**

JSX হলো একটি syntax, যেটা আমি React-এ JavaScript-এর মধ্যে HTML-এর মতো code লেখার জন্য ব্যবহার করি। এটি আমার UI code-কে অনেক সহজে পড়া এবং লেখার উপযোগী করে তোলে। React JSX ব্যবহার করে বুঝতে পারে user interface দেখতে কেমন হওয়া উচিত।

---

## Q3. What is the difference between functional and class components?

🔑 **Keywords:**
- both types return UI
- functional = simple function
- class = JS class
- functional is modern standard, uses Hooks

**🇬🇧 English**

Both functional and class components I use to build UI, but they work differently. A functional component is a simple JavaScript function that returns UI. A class component is a JavaScript class that also returns UI. I mostly use functional components now because Hooks let me manage state and other React features without writing a class.

**🇧🇩 বাংলা**

Functional এবং class component — দুটোই আমি UI তৈরি করার জন্য ব্যবহার করি, কিন্তু এদের কাজ করার ধরন আলাদা। Functional component হলো একটি simple JavaScript function, যা UI return করে। Class component হলো একটি JavaScript class, যা UI return করে। আমি এখন বেশিরভাগ ক্ষেত্রে functional component ব্যবহার করি, কারণ Hooks ব্যবহার করে আমি class না লিখেই state এবং অন্যান্য React feature manage করতে পারি।

---

## Q4. What is the Virtual DOM and how does React use it?

🔑 **Keywords:**
- lightweight copy of real DOM
- compare with previous version
- update only necessary parts
- makes UI updates efficient

**🇬🇧 English**

The Virtual DOM is a lightweight copy of the real DOM that React maintains. When something changes in my application, React first updates the Virtual DOM and compares it with the previous version. Then it updates only the necessary parts of the real DOM. This process helps React make UI updates much more efficient.

**🇧🇩 বাংলা**

Virtual DOM হলো Real DOM-এর একটি lightweight copy, যেটা React maintain করে। আমার application-এ কোনো কিছু change হলে, React প্রথমে Virtual DOM update করে এবং আগের version-এর সাথে compare করে। তারপর Real DOM-এর শুধুমাত্র প্রয়োজনীয় অংশ update করে। এই process React-কে অনেক বেশি efficiently UI update করতে সাহায্য করে।

---

## Q5. Explain the `useState` Hook with an example.

🔑 **Keywords:**
- store and update data
- inside functional component
- returns state + updater function
- e.g. counter

**🇬🇧 English**

useState is a React Hook that I use to store and update data inside a functional component. It gives me a state value and a function to update that value. For example, I can use it to build a simple counter that increases every time I click a button.

**🇧🇩 বাংলা**

useState হলো React-এর একটি Hook, যেটা আমি functional component-এর ভিতরে data store এবং update করার জন্য ব্যবহার করি। এটি আমাকে একটি state value এবং সেই value update করার জন্য একটি function দেয়। যেমন, আমি এটি ব্যবহার করে একটি simple counter বানাতে পারি, যেটা button click করলে বাড়তে থাকে।

---

## Q6. What is the `useEffect` Hook and what are its use cases?

🔑 **Keywords:**
- runs after component renders
- side effects
- API calls, event listeners, title update
- dependency array controls when it runs

**🇬🇧 English**

useEffect is a React Hook that I use to perform tasks after a component renders. I commonly use it for things like fetching data from an API, adding event listeners, or updating the document title. I control when it runs using the dependency array.

**🇧🇩 বাংলা**

useEffect হলো React-এর একটি Hook, যেটা আমি component render হওয়ার পরে কিছু কাজ করার জন্য ব্যবহার করি। আমি এটি সাধারণত API থেকে data আনা, event listener যোগ করা, অথবা document title update করার মতো কাজে ব্যবহার করি। এটি কখন চলবে সেটা আমি dependency array দিয়ে control করি।

---

## Q7. What is the difference between controlled and uncontrolled components?

🔑 **Keywords:**
- controlled = value managed by React state
- uncontrolled = value managed by DOM/ref
- controlled used when tracking/validating form data

**🇬🇧 English**

Both controlled and uncontrolled components I use for handling forms, but they manage value differently. A controlled component is a form element whose value I manage using React state. An uncontrolled component manages its own value through the DOM, usually accessed with a ref. I mostly use controlled components when I need to track or validate form data.

**🇧🇩 বাংলা**

Controlled এবং uncontrolled component — দুটোই আমি form handle করার জন্য ব্যবহার করি, কিন্তু এদের value manage করার ধরন আলাদা। Controlled component হলো এমন একটি form element, যার value আমি React state দিয়ে manage করি। Uncontrolled component তার নিজের value DOM-এর মাধ্যমে manage করে, সাধারণত ref দিয়ে access করা হয়। আমি মূলত controlled component ব্যবহার করি যখন form-এর data track বা validate করতে হয়।

---

## Q8. What are props in React and how are they passed?

🔑 **Keywords:**
- pass data parent → child
- passed as attributes
- received inside child component
- read-only

**🇬🇧 English**

Props are what I use to pass data from a parent component to a child component. I pass them as attributes, and the child component receives them as an object. Props are read-only, so I never change them directly inside the child component.

**🇧🇩 বাংলা**

Props হলো এমন একটি জিনিস, যেটা আমি parent component থেকে child component-এ data পাঠানোর জন্য ব্যবহার করি। আমি এগুলো attribute হিসেবে pass করি, এবং child component সেগুলো object আকারে receive করে। Props read-only, তাই আমি কখনো child component-এর ভিতরে এগুলো সরাসরি change করি না।

---

## Q9. What is prop drilling and how can it be avoided?

🔑 **Keywords:**
- passing data through many intermediate components
- makes code harder to manage
- fix: Context API / state management library / lift state

**🇬🇧 English**

Prop drilling happens when I pass data through several components just to reach one component that actually needs it. It can make my code harder to manage. I avoid it by using the Context API, a state management library, or by keeping the state closer to where it's actually needed.

**🇧🇩 বাংলা**

Prop drilling তখন হয় যখন আমি কোনো data একটি component পর্যন্ত পৌঁছানোর জন্য মাঝখানের অনেকগুলো component-এর মধ্য দিয়ে pass করি। এতে আমার code manage করা কঠিন হয়ে যায়। আমি এটি এড়াতে Context API, কোনো state management library ব্যবহার করি, অথবা state-কে যেখানে আসলে দরকার তার কাছাকাছি রাখি।

---

## Q10. Explain the `useContext` Hook with an example.

🔑 **Keywords:**
- share data without prop drilling
- avoids passing through every level
- e.g. user info, theme, language

**🇬🇧 English**

useContext is a React Hook that I use to share data between components without passing props through every single level. I find it especially useful for sharing common data like user information, theme settings, or language preferences across many components.

**🇧🇩 বাংলা**

useContext হলো React-এর একটি Hook, যেটা আমি প্রতিটি level দিয়ে props pass না করেই component-গুলোর মধ্যে data share করার জন্য ব্যবহার করি। এটি user information, theme settings, বা language preference-এর মতো common data অনেক component-এ share করার জন্য বিশেষভাবে useful।

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

## 🔑 Keyword Quick-Recall Table — Q46 to Q60

Use this table for fast revision. Cover the "Full Answer" section below, look only at the keywords, and try to explain the topic out loud in your own words (active recall).

| Q# | Topic | Keywords to Recall |
|---|---|---|
| 46 | useReducer | complex state logic → reducer function → current state + action → new state → multiple related updates |
| 47 | useMemo | memoize value → store result → recalculate on dependency change → expensive calculation |
| 48 | useCallback | memoize function → same reference → dependencies change → memoized child / dependency array |
| 49 | React Router | navigation/routing library → routes → map to URLs → `/`, `/about`, `/contact` |
| 50 | useNavigate vs Link | Link = click navigation → useNavigate = programmatic navigation → e.g. after login redirect |
| 51 | Custom Hooks | reusable function → share stateful logic → starts with `use` → e.g. useFetch |
| 52 | Lazy Loading | load on demand → React.lazy() + Suspense → reduce initial bundle → improve load time |
| 53 | Error Boundaries | catch JS errors → component tree → fallback UI → prevent app crash |
| 54 | Context API vs Redux | Context = share data, no prop drilling → theme/auth/language → Redux = large/complex global state, predictable/centralized |
| 55 | Reconciliation | compare old vs new Virtual DOM → identify changes → update only necessary real DOM parts |
| 56 | Fragment vs `<>` | group elements, no extra DOM node → syntax difference → `<>` = short, Fragment = supports `key` prop |
| 57 | Forms (react-hook-form) | manage form state/validation/errors → `register` inputs → `handleSubmit` submission |
| 58 | Code Splitting | split JS bundle → smaller chunks → load only needed code → dynamic import / React.lazy() |
| 59 | Portals | render outside parent DOM hierarchy → modals/dialogs/tooltips/dropdowns → avoid overflow/z-index issues |
| 60 | Component Lifecycle | mounting → updating → unmounting → useEffect handles side effects at each stage |

---

## Q46. What is the `useReducer` hook and when is it preferred over `useState`?

🔑 **Keywords:**
- complex state logic
- reducer function
- current state + action
- new state
- multiple related updates

**🇬🇧 English**

useReducer is a React hook that I use to manage complex state logic. It works with a reducer function that takes the current state and an action and returns a new state. I prefer useReducer over useState when I have multiple related state updates or complex state logic.

**🇧🇩 বাংলা**

useReducer হলো React-এর একটি hook, যেটা আমি complex state logic manage করার জন্য ব্যবহার করি। এটি একটি reducer function-এর সাথে কাজ করে, যেটা current state এবং একটি action নেয় এবং একটি new state return করে। যখন আমার multiple related state updates বা complex state logic থাকে, তখন আমি useState-এর পরিবর্তে useReducer পছন্দ করি।

---

## Q47. Explain the `useMemo` hook and give a use case.

🔑 **Keywords:**
- memoize value
- store result
- recalculate on dependency change
- expensive calculation

**🇬🇧 English**

useMemo is a React hook that I use to memoize a calculated value. React stores the result and recalculates it only when its dependencies change. I use it when a calculation takes a lot of time and I want to avoid unnecessary recalculations.

**🇧🇩 বাংলা**

useMemo হলো React-এর একটি hook, যেটা আমি একটি calculated value memoize করার জন্য ব্যবহার করি। React result-টি store করে রাখে এবং শুধুমাত্র dependencies পরিবর্তন হলে আবার calculate করে। যখন কোনো calculation অনেক সময় নেয় এবং আমি অপ্রয়োজনীয় recalculation এড়াতে চাই, তখন আমি এটি ব্যবহার করি।

---

## Q48. What is the `useCallback` hook and when do you use it?

🔑 **Keywords:**
- memoize function
- same reference
- dependencies change
- memoized child / dependency array

**🇬🇧 English**

useCallback is a React hook that I use to memoize a function. It keeps the same function reference between renders until its dependencies change. I mainly use it when I pass a function to a memoized child component or when a function appears in another hook's dependency array.

**🇧🇩 বাংলা**

useCallback হলো React-এর একটি hook, যেটা আমি একটি function memoize করার জন্য ব্যবহার করি। Dependencies পরিবর্তন না হওয়া পর্যন্ত এটি renders-এর মধ্যে একই function reference ধরে রাখে। যখন আমি একটি function-কে memoized child component-এ pass করি অথবা কোনো function অন্য hook-এর dependency array-তে থাকে, তখন আমি মূলত useCallback ব্যবহার করি।

---

## Q49. What is React Router and how do you set up client-side routing?

🔑 **Keywords:**
- navigation/routing library
- routes
- map to URLs
- `/`, `/about`, `/contact`

**🇬🇧 English**

React Router is a library that I use to manage navigation and routing in React applications. I create routes for different components and map them to different URLs. For example, I can create routes like `/`, `/about`, and `/contact` and render different components for each route.

**🇧🇩 বাংলা**

React Router হলো একটি library, যেটা আমি React application-এ navigation এবং routing manage করার জন্য ব্যবহার করি। আমি বিভিন্ন component-এর জন্য route তৈরি করি এবং সেগুলোকে বিভিন্ন URL-এর সাথে map করি। যেমন, আমি `/`, `/about`, এবং `/contact`-এর মতো route তৈরি করতে পারি এবং প্রতিটি route-এর জন্য আলাদা component render করতে পারি।

---

## Q50. What is the difference between `useNavigate` and `Link` in React Router?

🔑 **Keywords:**
- Link = click navigation
- useNavigate = programmatic navigation
- e.g. after login redirect

**🇬🇧 English**

Both Link and useNavigate I use for navigation, but they have different purposes. I use Link when I want users to navigate by clicking a link. I use useNavigate when I want to navigate programmatically based on some logic or an event. For example, after a successful login, I can use useNavigate to redirect the user to the dashboard.

**🇧🇩 বাংলা**

Link এবং useNavigate — দুটোই আমি navigation-এর জন্য ব্যবহার করি, কিন্তু এদের purpose আলাদা। আমি Link ব্যবহার করি যখন আমি চাই user কোনো link-এ click করে navigate করুক। আমি useNavigate ব্যবহার করি যখন আমি কোনো logic বা event-এর ভিত্তিতে programmatically navigate করতে চাই। যেমন, successful login-এর পর আমি user-কে dashboard-এ redirect করার জন্য useNavigate ব্যবহার করতে পারি।

---

## Q51. What are custom hooks in React? Write a simple example.

🔑 **Keywords:**
- reusable function
- share stateful logic
- starts with `use`
- e.g. useFetch

**🇬🇧 English**

Custom hooks are reusable functions that I create to share stateful logic between components. A custom hook usually starts with the word `use`. For example, I can create a `useFetch` hook to handle API requests and reuse it in multiple components.

**🇧🇩 বাংলা**

Custom hook হলো এমন reusable function, যেটা আমি বিভিন্ন component-এর মধ্যে stateful logic share করার জন্য তৈরি করি। একটি custom hook সাধারণত `use` শব্দ দিয়ে শুরু হয়। যেমন, API request handle করার জন্য আমি একটি `useFetch` hook তৈরি করতে পারি এবং সেটি একাধিক component-এ পুনরায় ব্যবহার করতে পারি।

---

## Q52. What is lazy loading in React and how is it implemented?

🔑 **Keywords:**
- load on demand
- React.lazy() + Suspense
- reduce initial bundle
- improve load time

**🇬🇧 English**

Lazy loading means loading a component only when I need it instead of loading everything at the beginning. I can implement lazy loading with `React.lazy()` and `Suspense`. It helps reduce the initial bundle size and improves the initial loading performance.

**🇧🇩 বাংলা**

Lazy loading মানে হলো শুরুতেই সবকিছু load না করে, যখন আমার একটি component দরকার হয় তখনই সেটি load করা। আমি `React.lazy()` এবং `Suspense` দিয়ে lazy loading implement করতে পারি। এটি initial bundle size কমাতে সাহায্য করে এবং initial loading performance উন্নত করে।

---

## Q53. What are React error boundaries and why are they useful?

🔑 **Keywords:**
- catch JS errors
- component tree
- fallback UI
- prevent app crash

**🇬🇧 English**

Error boundaries help me catch JavaScript errors in a component tree and show a fallback UI instead of breaking the entire application. I can use them around important parts of my application to improve error handling and user experience.

**🇧🇩 বাংলা**

Error boundaries আমাকে একটি component tree-তে JavaScript error catch করতে এবং পুরো application ভেঙে না গিয়ে একটি fallback UI দেখাতে সাহায্য করে। আমি আমার application-এর গুরুত্বপূর্ণ অংশগুলোর চারপাশে এগুলো ব্যবহার করে error handling এবং user experience উন্নত করতে পারি।

---

## Q54. What is the Context API and when should you use Redux instead?

🔑 **Keywords:**
- Context = share data, no prop drilling
- theme/auth/language
- Redux = large/complex global state
- predictable/centralized management

**🇬🇧 English**

The Context API helps me share data between components without passing props through every level. I use it for things like themes, authentication information, or language settings.

I choose Redux when my application has large and complex global state, many state updates, or when I need predictable and centralized state management.

**🇧🇩 বাংলা**

Context API আমাকে প্রতিটি level দিয়ে props pass না করেই component-গুলোর মধ্যে data share করতে সাহায্য করে। আমি এটি theme, authentication information, বা language settings-এর মতো বিষয়গুলোর জন্য ব্যবহার করি।

আমি Redux বেছে নিই যখন আমার application-এ বড় এবং complex global state থাকে, অনেক state update থাকে, অথবা আমার predictable এবং centralized state management দরকার হয়।

---

## Q55. Explain the concept of reconciliation in React.

🔑 **Keywords:**
- compare old vs new Virtual DOM
- identify changes
- update only necessary real DOM parts

**🇬🇧 English**

Reconciliation is the process React uses to compare the previous Virtual DOM with the new Virtual DOM. React identifies what changed and updates only the necessary parts of the real DOM. This approach helps React update the UI efficiently.

**🇧🇩 বাংলা**

Reconciliation হলো সেই process, যেটা React আগের Virtual DOM-কে নতুন Virtual DOM-এর সাথে তুলনা করার জন্য ব্যবহার করে। React কী পরিবর্তন হয়েছে সেটি identify করে এবং real DOM-এর শুধুমাত্র প্রয়োজনীয় অংশগুলো update করে। এই approach React-কে efficient ভাবে UI update করতে সাহায্য করে।

---

## Q56. What is the difference between `React.Fragment` and empty tags (`<> </>`)?

🔑 **Keywords:**
- group elements, no extra DOM node
- syntax difference
- `<>` = short syntax
- Fragment = supports `key` prop

**🇬🇧 English**

Both React.Fragment and empty tags allow me to group multiple elements without adding an extra DOM element.

The main difference is syntax. I can write the short syntax as `<>...</>`, while React.Fragment gives me more options, such as using a `key` prop.

**🇧🇩 বাংলা**

React.Fragment এবং empty tags — দুটোই আমাকে অতিরিক্ত DOM element যোগ না করে একাধিক element group করতে দেয়।

মূল পার্থক্য হলো syntax-এ। আমি short syntax হিসেবে `<>...</>` লিখতে পারি, যেখানে React.Fragment আমাকে আরও বেশি option দেয়, যেমন `key` prop ব্যবহার করা।

---

## Q57. How do you handle forms in React? Explain with Formik or react-hook-form.

🔑 **Keywords:**
- manage form state/validation/errors
- `register` inputs
- `handleSubmit` submission

**🇬🇧 English**

I usually use react-hook-form to handle forms in React. It helps me manage form state, validation, errors, and submission efficiently. I register my inputs with the `register` function and handle form submission with `handleSubmit`.

**🇧🇩 বাংলা**

React-এ form handle করার জন্য আমি সাধারণত react-hook-form ব্যবহার করি। এটি form state, validation, error, এবং submission efficiently manage করতে সাহায্য করে। আমি `register` function দিয়ে আমার input-গুলো register করি এবং `handleSubmit` দিয়ে form submission handle করি।

---

## Q58. What is code splitting in React and how does it improve performance?

🔑 **Keywords:**
- split JS bundle
- smaller chunks
- load only needed code
- dynamic import / React.lazy()

**🇬🇧 English**

Code splitting means dividing my application's JavaScript bundle into smaller chunks. Instead of loading the entire application at once, I can load only the code that the user currently needs. I can implement it using dynamic imports and `React.lazy()`. This reduces the initial bundle size and improves loading performance.

**🇧🇩 বাংলা**

Code splitting মানে হলো আমার application-এর JavaScript bundle-কে ছোট ছোট chunk-এ ভাগ করা। পুরো application একসাথে load না করে, আমি শুধুমাত্র সেই code load করতে পারি যেটা user-এর বর্তমানে দরকার। আমি এটি dynamic import এবং `React.lazy()` ব্যবহার করে implement করতে পারি। এটি initial bundle size কমায় এবং loading performance উন্নত করে।

---

## Q59. What are portals in React and when are they useful?

🔑 **Keywords:**
- render outside parent DOM hierarchy
- modals/dialogs/tooltips/dropdowns
- avoid overflow/z-index issues

**🇬🇧 English**

React portals allow me to render a component into a different DOM node outside its parent component's DOM hierarchy. I commonly use portals for modals, dialogs, tooltips, and dropdowns because they can avoid CSS overflow or z-index problems.

**🇧🇩 বাংলা**

React portal আমাকে একটি component-কে তার parent component-এর DOM hierarchy-এর বাইরে একটি ভিন্ন DOM node-এ render করতে দেয়। আমি সাধারণত modal, dialog, tooltip, এবং dropdown-এর জন্য portal ব্যবহার করি, কারণ এগুলো CSS overflow বা z-index সমস্যা এড়াতে পারে।

---

## Q60. Explain the lifecycle of a React functional component with hooks.

🔑 **Keywords:**
- mounting
- updating
- unmounting
- useEffect handles side effects at each stage

**🇬🇧 English**

A functional component generally goes through three main stages: mounting, updating, and unmounting.

When React creates the component for the first time, I call it the mounting phase. When its state or props change, React updates and re-renders the component. When React removes the component from the UI, I call it the unmounting phase.

I use useEffect to handle side effects during these stages. For example, I can fetch data after mounting and clean up subscriptions or event listeners when the component unmounts.

**🇧🇩 বাংলা**

একটি functional component সাধারণত তিনটি প্রধান stage-এর মধ্য দিয়ে যায়: mounting, updating, এবং unmounting।

যখন React প্রথমবার component তৈরি করে, আমি সেটাকে mounting phase বলি। যখন এর state বা props পরিবর্তন হয়, React component update এবং re-render করে। আর যখন React component-কে UI থেকে remove করে, আমি সেটাকে unmounting phase বলি।

আমি এই stage-গুলোর সময় side effects handle করার জন্য useEffect ব্যবহার করি। যেমন, আমি mounting-এর পর data fetch করতে পারি এবং component unmount হওয়ার সময় subscription বা event listener clean up করতে পারি।

---

*Prepared for React technical interview practice — English + বাংলা, sentence-aligned for easy speaking practice.*